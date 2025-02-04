# Designing an herbicide-tolerant rhizobium 

## Herbicide selection:

Various pesticides have been shown to inhibit nitrogenase activity in soil bacteria (both symbiotic and free-living) (Fox et al., 2007).  This then limits the availability of usable nitrogen for plants which requires farmers to supplement their crops with nitrogen fertilizers (Fox et al., 2007).  However, nitrogen fertilizers cause nutrient pollution and contaminate water-ways leading to algal blooms and ecological damage (Heisler et al., 2008).

The goal of this project is to provide a solution in which rhizobia (legume root symbionts) contain pesticide metabolic genes to generate root nodules and exhibit nitrogenase activity in the presence of pesticides. This would limit the need for nitrogen rich fertilizers and lower pollution caused by both fertilizers.

Thus, a target pesticide for this project would be able to be degraded or biotransformed to less toxic products that can be more readily degraded by common soil microflora.  Additionally, a pesticide of interest would be one that is used prominently in Canada, specifically in the regions of southern ontario.  Lastly, for the symbiotic rhizobia to form symbiotic relationships with the plant, the pesticide must be applied to a leguminous crop.

Linuron was identified as an herbicide that fits all three criteria since literature has identified some genes and metabolic pathways involved in the degradation or transformation of linuron (xenobiotic phenylurea pesticide).  These genes are further described below in ‘choosing the genes’.  It is also an herbicide used in Canada of particular interest as its use is currently in the process of being re-evaluated by Health Canada (Health Canada, 2012). It is used to control broadleaf and grassy weeds prior to planting and is used as a staple ingredient in many herbicide applications for Canadian growers (Health Canada, 2012).  Lastly, linuron in North America is used for the treatment of tubers and legumes including soybean plants which are capable of forming root nodules with various rhizobia species (Health Canada, 2012).


## Plant selection:

As above, for increased root nodule formation and symbiotic nitrogen fixation in the presence of linuron, the plant chosen must also satisfy certain criteria. These included being used in Canada/Southern Ontario, being a crop onto which linuron is applied, and also being capable of forming root nodules with rhizobia. The soybean plant was chosen as it satisfies these criteria by (1) comprising 2 million acres of crop land in Ontario, (2) being a known crop to which linuron is applied to as a pre-emergence herbicide, and (3) being able to form root nodules with certain species of rhizobia such as Rhizhobia fredii, Bradyrhizobium Diazoefficiens, and Bradyrhizobium elkanii (OMAFRA, 2018 and Farm Journal AgPro, 2014). 

Furthermore, although soybean is not quite a model organism, it is well-studied due to its agricultural importance (Pitzschke, 2013). It also germinates, grows, and shows evidence of root nodulation relatively quickly compared to other crops to which linuron is applied (Pitzschke, 2013).  Thus, by using soybeans as a plant symbiont for rhizobia, nodulation in the presence of pesticide could be directly assayed through nodule counts.


## Rhizobium selection:

Once soybean was selected as the target plant, the choice of bacteria was limited to three rhizobia species, Rhizhobia fredii, Bradyrhizobium diazoefficiens, and Bradyrhizobium elkanii (Farm Journal AgPro, 2014).  From these three, Bradyrhizobium diazoefficiens USDA110 was selected in part because it is also well-studied (with literature including that done under the species’ former name Bradyrhizobium japonicum). It is also used in commercial rhizobia inoculants for soils designed to improve the nitrogen fixation yield of soybean crops (Prevost & Bromfield, 2003). Despite its slow growth (several days are required to get visible growth), Bradyrhizobium diazoefficiens USDA110 was chosen for this project due to its prevalent use as an inoculant in Ontarian soils (Prevost & Bromfield, 2003).

## DNA design:

### Vector selection:
For assembly of the system to be used in both E. coli for construction and Bradyrhizobium Diazoefficiens the plasmid pRJPaph was used. Different versions of this plasmid encode a variety of fluorescence or enzymatic reporters (Ledermann et al., 2015). We chose to use the pRJPaph-mCHERRY and pRJPaph-GFP fluorescent reporter versions of the plasmid for our project as we could easily measure fluoresence with our lab equipment. We decided to use the GFP plasmid for further cloning (to insert degradation genes) to create the engineered strains. mCherry will act as an empty vector control in our later experiments. 

These plasmids were designed for stable integration into the B. diazoefficiens genome (Ledermann et al., 2015). We could edit them/ do our construction in E. coli and then conjugate them into B. diazoefficiens. The plasmids integrate into the B. diazoefficiens genome, downstream of the of the scoI gene, without affecting the bacteria's ability to form root nodules (Ledermann et al., 2015).   

### The degradation genes:

Linuron is a chlorinated urea-based herbicide, and despite being a synthetic herbicide - a xenobiotic that is foreign to ecological systems - quite a few degradation/biotransformation pathways have been identified (Stoker & Kavlock, 2010).  These pathways and associated genes were identified through a thorough literature search.

However, for some of these pathways the genes required are not yet fully identified.  For others, the gene segments are identified but riddled with other functional DNA sequences that make identification of the aspects required and controlled engineering difficult.  Additionally, in each case, the goal is to either fully mineralize linuron or end-up with a product less toxic than linuron itself and other naturally occurring degradation products.  Therefore, the final genes chosen represent a biotransformation pathway taking elements from a couple different sources.

The aim of the project was to confer an increased tolerance, if not a resistance, to linuron in our engineered rhizobia. There are a multitude of evolutionary distinct pathways that could be taken from - but the final genes selected belonged to two different pathways that are not known to be associated. 

The advantages and disadvantages brought on by all found pathways and degradation-related genes were taken into consideration when deciding upon the final pathway for this project.  Below is a description of the chosen pathway, as well as those considered during our design process.

##### Chosen Pathway: nat1 and libA

![Chosen Pathway](https://2019.igem.org/wiki/images/8/80/T--Waterloo--Chosenpathway_linurondegradation.png)

In this case, linuron is not fully degraded but instead is biotransformed to N-acetyl-3,4-Dichloroaniline (N-acetyl-3,4-DCA). This strategy is beneficial in that herbicide that is transformed into 3,4-Dichloroaniline (3,4-DCA) can be acetylate into a less toxic product (Dupret et al., 2011). In fact, the acetylated product is considered as a plausible endpoint for bioremediation of soil contaminated with the same class of herbicide as linuron (Dupret et al., 2011).  

The first degradation step in this pathway is the conversion of linuron to 3,4-DCA by libA. LibA itself is a linuron hydrolase with activity specific to linuron (it lacks activity towards other phenylurea herbicides tested) (Bers et al., 2011).  It was originally identified in Variovorax sp. Strain SRS16 and has orthologues present in other tested linuron-degrading Variovorax strains (Bers et al., 2011).  This step also leads to the production of the byproduct N,O-dimethylhydroxylamine (N,O-DMHA) (Bers et al., 2011).  However, while DCA is toxic and resistant to decomposition, N,O-DMHA is not harmful and easily degraded (Bers et al., 2011).  Therefore, while N,O-DMHA does not need any additional processing steps, 3,4-DCA necessitates additional transformation before a non-toxic product can be yielded (Bers et al., 2011).

![LibA Pathway](https://2019.igem.org/wiki/images/0/0e/T--Waterloo--Chosenpathway_libApath.png)

The second degradation step is the conversion of 3,4-DCA to N-acetyl-3,4-DCA by nat1.  Nat1 is an arylamine N-acetyltransferase (NAT) (Rodrigues-Lima et al., 2016). These are xenobiotic-metabolizing enzymes involved in detoxification, such as the detoxification of 3,4-DCA to N-acetyl-3,4-DCA (Rodrigues-Lima et al., 2016).  The gene used for nat1 in this project was originally cloned from Mesorhizobium loti which is another root-nodule forming bacterium (Rodrigues-Lima et al., 2016). Nat1 was chosen from other NAT’s identified as it was shown to be much more effective at acetylating 3,4-DCA (ex: more than 136 times more effective than nat2) (Rodrigues-Lima et al., 2016). Additionally, the paper through which this gene was identified represents the first evidence for xenobiotic detoxification pathway via plant symbiosis with soil microorganisms, which forms the foundation for this project (Rodrigues-Lima et al., 2016). Again, this step is important since linuron is not the only toxic chemical, but accumulation of 3,4-DCA in the soil must be avoided which is solved through this transformation step (Rodrigues-Lima et al., 2016).

As a whole, this pathway benefits from being complete with well-documented genes and enzymatic processes. The selected genes aim to deter the accumulation of toxic and recalcitrant compounds by producing the non-harmful compounds N,O-DHMA and N-acetyl-3,4-DCA as a result of biotransformation of linuron.

However, seeing that the presence of N-acetyl-3,4-DCA is difficult to assay, the experimental design to measure activity of nat1 and libA expression was two-pronged. The first aim was to identify effectiveness of nodulation by both the engineered and un-engineered rhizobia strains, in the presence of linuron, and without the herbicide present. 

For this, soybean plants grown in facilities at the University of Waterloo by the iGEM team would be inoculated, by seed-coating or flooding techniques, and then allowed to grow for 3-4 weeks. Nodulation would be the major quantitative measure of effectiveness of the bacteria, using the dry weight of nodules for each plant as a measure. However, if there is a distinct increase in nitrogen fixation, it could potentially be seen reflected in plant growth. 

The second approach would be to use end-point MICs, minimal inhibitory concentrations, to determine changes in tolerance between the engineered rhizobia and unengineered wild-type. This would not reflect their survival in soil environments, but would give an indication to the comparative effect of the herbicide on the two bacteria. If it is detected that the MICs increased for the engineered strain, it would indicate that the genes provided confer an increased tolerance to the herbicide or its tested derivatives.  

##### Alternative pathway: full Mineralization

Microbial degradation is an important mechanism in the dissipation of linuron and other phenylurea herbicides in the environment.  Therefore the ideal goal would be to achieve full mineralization of the linuron as a substrate.  With this in mind, linuron could be used as a substrate to sustain the growth of the bacteria (bacteria would grow on agar plates containing just linuron).  This has been observed in Variovorax sp. Strain SRS16, which is able to fully mineralize linuron, and some genes involved in this metabolic pathway have already been identified (Bers et al., 2011). The mineralization is conducted through a pathway initiated by the hydrolysis of linuron to 3,4-DCA, by libA,  which is then converted to Krebs cycle intermediates (Bers et al., 2011).

The entire pathway is shown below:

![Full Mineralization Pathway](https://2019.igem.org/wiki/images/2/2d/T--Waterloo--fulldegradationpathway.png)

(Image sourced from Bers et al., 2011)

However, the dcaQTA1A2BR and ccdRCFDE gene clusters ORF’s only been identified by their possible products and enzymatic function bioinformatically (Bers et al., 2011). Additionally, it is indicated that the dcaQTA1A2BR gene cluster is located within a transposon-like structure (Bers et al., 2011). Therefore, due to the complexity and time associated with identifying and experimentally validating the necessary ORF’s in house and working with a transposon-containing gene cluster, this pathway was not chosen (Bers et al., 2011).  If further publications, show additional information on these gene clusters, this pathway could become an ideal solution later on as it leads to full mineralization.

If this pathway were to be used, an experimental method to determine the success of this strategy would be to grow Bradyrhizobium diazoefficiens on agar containing linuron as the sole carbon source (Bers et al., 2011). Growth would indicate that the bacteria is successfully metabolizing linuron into Kreb’s cycle intermediates used for energy production.

## Additional herbicide: 
While the literature indicated that the transformation of linuron and 3,4-dichloroaniline into 3,4-dichloroacetanilide should reduce the toxicity of the bacteria’s environment, there were still many unknowns at this stage of the project design such as the relative kinetics of these two enzymatic transformations and whether the partial degradation of linuron would be sufficient. As such, we wanted to design another herbicide tolerance system using a more well-studied herbicide. 

We found that the commonly-used glyphosate herbicide also inhibited nitrogen fixation in root nodules (Zablotowicz & Reddy, 2004). We also found a relatively simple pathway for the degradation of glyphosate to metabolic intermediates by C-P lyase and sarcosine oxidase (Grandcoin et al., 2017). However, we decided to engineer glyphosate tolerance via a different mechanism. 

Glyphosate is typically utilized with “Round-Up Ready” plants by Monsanto which have been genetically engineered to be resistant to the pesticide. This was accomplished by replacing the wild type copy of the enzyme inhibited by glyphosate, 5-enolpyruvylshikimate-3-phosphate (EPSP) synthase, with a copy of the gene found in agrobacterium sp. strain CP4, which demonstrates low levels of inhibition. When this glyphosate-resistant gene is engineered into soybeans, the shikimate pathway, which is required for the production of aromatic amino acids, is no longer inhibited and the plant is able to survive (Funke et al., 2006). We envisioned that by integrating this CP4 EPSP synthase gene from the original Monsanto patent (which we codon optimized for B. diazoefficiens) into the genome of our rhizobia, we could introduce glyphosate tolerance, in the same way it is done for plants. We chose to pursue this project alongside our linuron project in hopes of demonstrating that rhizobia could be made tolerant to different herbicides by a variety of ways and that mechanisms to accomplish this could be tailored to each herbicide.


# Citations:

Bers, K., Leroy, B., Breugelmans, P., Albers, P., Lavigne, R., Sørensen, S. R., … Springael, D. (2011). A Novel Hydrolase Identified by Genomic-Proteomic Analysis of Phenylurea Herbicide Mineralization by Variovorax sp. Strain SRS16. Applied and Environmental Microbiology, 77(24), 8754–8764. https://doi.org/10.1128/AEM.06162-11

Dupret, J.-M., Dairou, J., Busi, F., Silar, P., Martins, M., Mougin, C., … Cocaig, A. (2011). Pesticide-Derived Aromatic Amines and Their Biotransformation. Pesticides in the Modern World - Pests Control and Pesticides Exposure and Toxicity Assessment. https://doi.org/10.5772/18279

Farm Journal AgPro. (2014, January 10). Attention Required! | Cloudflare. Retrieved October 19, 2019, from https://www.agprofessional.com/article/soybeans-and-rhizobia-mutually-beneficial-relationship

Fox, J. E., Gulledge, J., Engelhaupt, E., Burow, M. E., & McLachlan, J. A. (2007). Pesticides reduce symbiotic efficiency of nitrogen-fixing rhizobia and host plants. Proceedings of the National Academy of Sciences, 104(24), 10282–10287. https://doi.org/10.1073/pnas.0611710104 

Funke, T.; Han, H. Healy-Fried, M. L.; Fischer, M.; Schönbrunn, E. (2006). Molecular basis for the herbicide resistance of Roundup Ready crops. PNAS, 103(35), 13010-13015.

Grandcoin, A.; Piel, S.; Baurès, E. (2017). AminoMethylPhosphonic acid (AMPA) in natural waters: Its sources, behavior and environmental fate. Water Research, 117, 187-197.

Health Canada. (2012). Proposed Re-evaluation Decision PRVD2012-02, Linuron - Canada.ca. Retrieved October 19, 2019, from https://www.canada.ca/en/health-canada/services/consumer-product-safety/pesticides-pest-management/public/consultations/proposed-re-evaluation-decisions/2012/linuron.html 

Heisler, J., Glibert, P. M., Burkholder, J. M., Anderson, D. M., Cochlan, W., Dennison, W. C., … Suddleson, M. (2008). Eutrophication and harmful algal blooms: A scientific consensus. Harmful Algae, 8(1), 3–13. https://doi.org/10.1016/j.hal.2008.08.006 

Ledermann, R., Bartsch, I., Remus-Emsermann, M. N., Vorholt, J. A., & Fischer, H.-M. (2015). Stable Fluorescent and Enzymatic Tagging ofBradyrhizobium diazoefficiensto Analyze Host-Plant Infection and Colonization. Molecular Plant-Microbe Interactions, 28(9), 959–967. https://doi.org/10.1094/MPMI-03-15-0054-TA

Ontario Ministry of Agriculture, Food, and Rural Affairs (OMAFRA). (2018, February 8). Soybean Production in Ontario. Retrieved October 19, 2019, from http://www.omafra.gov.on.ca/english/crops/field/soybeans.html

Pitzschke, A. (2013). From Bench to Barn: Plant Model Research and its Applications in Agriculture. Advancements in Genetic Engineering, 02(02). https://doi.org/10.4172/2169-0111.1000110

Prévost and E. S P. Bromfield, D. (2003). Diversity of symbiotic rhizobia resident in Canadian soils. Canadian Journal of Soil Science, 83(Special Issue), 311–319. https://doi.org/10.4141/S01-066

Rodrigues-Lima, F., Dairou, J., Diaz, C. L., Rubio, M. C., Sim, E., Spaink, H. P., & Dupret, J.-M. (2006). Cloning, functional expression and characterization of Mesorhizobium loti arylamine N-acetyltransferases: rhizobial symbiosis supplies leguminous plants with the xenobiotic N-acetylation pathway. Molecular Microbiology, 60(2), 505–512. https://doi.org/10.1111/j.1365-2958.2006.05114.x 
Stoker, T. E., & Kavlock, R. J. (2010). Pesticides as Endocrine-Disrupting Chemicals. Hayes’ Handbook of Pesticide Toxicology, 551–569. https://doi.org/10.1016/B978-0-12-374367-1.00018-5

Zablotowicz, R. M. & Reddy, K. N. (2004). Impact of glyphosate on the Bradyrhizobium japonicum symbiosis with glyphosate-resistant transgenic soybean: a minireview. J. Environ Qual., 33(3), 825-831.
