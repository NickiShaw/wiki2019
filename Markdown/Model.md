# Environmental Model

An important goal of our project is to determine whether, in the viscinity of a root nodule, the Linuron concentration is 
significant enough to damage the Rhizosphere and inhibit nodule growth as plants continue to develop. 

In order to model this, we introduce a diffusion-reaction-advection model, which is a standard method in environmental engineering practices. As a consequence of this we are able to develop heuristics for whether Linuron and 3,4-DCA runoff is significant in addition to the original purpose of the model. The model is compared to a similar model by *Owsianiak et al* [1] for Linuron degradation in bioaugmentation beads. The paper by Owsianiak relied on the use of *Variovorax sp.*, which is one of the species responsible for our system - as such we credit many of our parameters to them.

**Insert Video**

## Introducing the Model

As partial differential equation models are quite rare in the world of iGEM, we will introduce this model from the ground up. The first component of the model is Fick's Law.

$$ C = [\textrm{Linuron}] $$

$$ D = \textrm{diag}(D_x,D_y,D_z) $$

$$ \nabla\cdot(D\nabla C) = \frac{\partial C}{\partial t} $$

The object D is called the diffusion matrix, which determines the speed of diffusion in different directions. Next, we add an advection term in order to model the movement of Linuron being carried by water.

$$ \nabla \cdot (D\nabla C) - \vec{v}_e \cdot \nabla C = \frac{\partial C}{\partial t}$$

This advection term relies on the hydraulic head, which is a measure of water pressure in the soil. However, water tends to flow around the root nodules, so Linuron transport is diffusion-dominated inside the nodule. Therefore we must use the Navier-Stokes equation in order to find the advection velocity. In order to model degradation, we couple this with our kinetic model to find the following coupled system of PDEs.

$$ \nabla \cdot (D\nabla C) - \vec{v}_e \cdot \nabla C = \frac{\partial C}{\partial t} + \chi_n \frac{V_{max}C}{K_m-C} $$

$$ \varrho \left( \frac{\partial v_e}{\partial t} - v_e \cdot \nabla v_e \right) = \nabla \cdot \sigma(v_e,p)+f $$
$$ \nabla \cdot v_e = 0 $$

## Assumptions

In the above model, we are assuming an averaged rate of water intake - this is necessary due to the difficulties with rain models. One can see that this assumption should produce a reasonable approximation since the timescale we are working with is over weeks to months, whereas the rate of rainfall is on the order of days.

We also needed to verify that the rate of water transport into the nodule tissue is not limited by physiological factors such as membrane transport. In order to do this, we used the Octanol-Water partition coefficient in order to predict the rate of membrane transport using Overton's Rule [2]:

$$ P=\frac{K_{ow}D}{\ell} $$

From this we found that the transport of Linuron into plant cells is not membrane-transport limited. In addition, the paper [1] found that background degradation of Linuron by the same pathway is negligible compared to degradation by *Variovorax sp.*, as such we ignore it in the model.


## Numerical Methods

In order to solve this model we first convert the system into variational form. The Navier-Stokes terms are solved by a midpoint discretization method called Chorin's Method, while the remainder is just solved using the backwards Euler method. The following equations are obtained by integrating the above PDEs and applying integration by parts.

$$\int_\Omega \frac{\partial C}{\partial t} w d\tau = \int_\Omega \left[\nabla \cdot (D \nabla C)w - w v_e\cdot \nabla C - \frac{V_{max}C}{K_m-C}\right] d \tau =$$

$$\int_\Omega \left[(-\nabla C)^T D^T \nabla w -wv_e\cdot \nabla C - \frac{V_{max}C}{K_m-C}\right] d \tau + \int_{\partial \Omega} w( \nabla C)\cdot d \vec{s}$$

We then write these equations into python using the framework *FeNiCS* [3], which is a free library for solving PDEs using the Finite Element Method. Teams interested in using PDE solvers for their iGEM project should consider FeNiCS as a good alternative to expensive or large-scale programs. Using *ParaView* one can export animations and data from pythons' results. We also used the python library *meshio* in order to convert meshes generated by *Gmsh* into a format compatible with FeNiCS. As a note to iGEM teams in the future considering PDE transport models, your discretization must meet the Courant-Freidrichs-Lewy (CFL) condition in order to be stable.

[1] Owsianiak, M., Dechesne, A., Binning, P. J., Chambon, J. C., Sørensen, S. R., & Smets, B. F. (2010). Evaluation of Bioaugmentation with Entrapped Degrading Cells as a Soil Remediation Technology. Environmental Science & Technology, 44(19), 7622–7627. doi: 10.1021/es101160u

[2] Grime, J. M. A., Edwards, M. A., Rudd, N. C., & Unwin, P. R. (2008). Quantitative visualization of passive transport across bilayer lipid membranes. Proceedings of the National Academy of Sciences, 105(38), 14277–14282. doi: 10.1073/pnas.0803720105

[3] Zakharov, P. E. (2018). The FEniCS project. Spark. doi: 10.1515/spark.18.13