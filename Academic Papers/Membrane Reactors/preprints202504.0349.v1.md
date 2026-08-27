

##### Article 

##### Not peer-reviewed version 

## Segmented Plug Flow Reactor Modeling of Hydrogen Separation from Syngas in Palladium Membrane Reactors under Different Operational Conditions 

<u>Osama Marzouk</u><sup>*</sup> 

Posted Date: 4 April 2025 doi: 10.20944/preprints202504.0349.v1 

Keywords: hydrogen; palladium; membrane reactor; MR; syngas 



Preprints.org is a free multidisciplinary platform providing preprint service that is dedicated to making early versions of research outputs permanently available and citable. Preprints posted at Preprints.org appear in Web of Science, Crossref, Google Scholar, Scilit, Europe PMC. 

Copyright: This open access article is published under a Creative Commons CC BY 4.0 license, which permit the free download, distribution, and reuse, provided that the author and preprint are cited in any reuse. 

**_Preprints.org_ (www.preprints.org)  |  NOT PEER-REVIEWED  |  Posted: 4 April 2025** 

**<u>doi:10.20944/preprints202504.0349.v1</u>** 

Disclaimer/Publisher’s Note: The statements, opinions, and data contained in all publications are solely those of the individual author(s) and contributor(s) and not of MDPI and/or the editor(s). MDPI and/or the editor(s) disclaim responsibility for any injury to people or property resulting from any ideas, methods, instructions, or products referred to in the content. 

_Article_ 

### **Segmented Plug Flow Reactor Modeling of Hydrogen Separation from Syngas in Palladium Membrane Reactors under Different Operational Conditions** 

###### **Osama A. Marzouk** 

College of Engineering, University of Buraimi, Al Buraimi, Sultanate of Oman; osama.m@uob.edu.om 

**Abstract:** A one-dimensional plug-flow reactor modeling procedure was developed and used to investigate the performance of a membrane reactor (MR) for hydrogen separation from syngas. A feed syngas enters from one side, while a sweep gas of nitrogen enters from the opposite side. The model treats the membrane reactor as a series of 200 segments with a constant cross section and temperature. The adopted spatial resolution was verified to be accurate based on a conducted resolution sensitivity analysis. Permeation is modeled as happening through thin palladium membranes that are selectively permeable to hydrogen, depending on the temperature and membrane thickness. After analyzing the hydrogen permeation profile in a base case corresponding to reference operational temperature and pressures, the temperature of the module, the retentateside pressure, and the permeate-side pressure were varied individually and their influence on the permeation performance was investigated. In all the simulation cases, fixed targets of 95% hydrogen recovery and 40% mole-fraction of hydrogen at the permeate exit were demanded. The module length is allowed to change to satisfy these targets, with a shorter module requiring less space and reflecting better hydrogen permeation mass flux. Other dependent permeation-performance variables that were investigated include the logarithmic mean pressure-square-root difference, the hydrogen apparent permeance, and the efficiency factor. Various linear and nonlinear regression models were proposed based on the obtained results. This work gives general insights about hydrogen permeation via palladium membranes. 

**Keywords:** hydrogen; palladium; membrane reactor; MR; syngas 

###### **1. Introduction** 

Gasification is a thermos-chemical process in which a carbonaceous solid fuel (such as coal or biomass) is converted into synthetic gas, also known as syngas (Couto et al., 2013; Sarafraz et al., 2019). In other words, gasification is a partial oxidation process consisting of physical processes, such as pyrolysis; and chemical reactions, such as gasification with steam (NETL, 2022). Syngas is a mixture of gases, primarily carbon dioxide and hydrogen, with possible additional impurities such as carbon dioxide, methane, water vapor, and nitrogen (Poudel et al., 2019; Kumar and Aarthi, 2020). Syngas is also produced from natural gas or light crude oil fractions through steam reforming (Talmadge et al., 2013). The molar ratio of molecular hydrogen (H2) to carbon monoxide (CO) increases as the ratio of hydrogen atoms to carbon atoms in the feedstock increases. Thus, ideal steam reforming of carbon gives a molar ratio of H2:CO equal to 1:1, while the ideal steam reforming of natural gas gives a molar ratio of H2:CO equal to 3:1 (Matar et al., 1989). 

While syngas by itself is a gaseous fuel that can be used in gas turbines or boilers (Fortunato et al., 2013; Stork, 2022), it is also a feedstock for the production of hydrogen, methanol, and synthetic gasoline (Marco and Carlo, 2015; Ni et al., 2021). Producing hydrogen is of special environmental importance, as it enables production of electricity through fuel cells without the harmful carbondioxide emissions (Felseghi et al., 2019). Hydrogen also can be used as an alternative fuel in hydrogen vehicles, leading to reduced greenhouse gas emissions in the transportation sector. ). Separating 



©  2025 by the author(s). Distributed under a Creative Commons CC BY license. 

**_Preprints.org_ (www.preprints.org)  |  NOT PEER-REVIEWED  |  Posted: 4 April 2025** 

**<u>doi:10.20944/preprints202504.0349.v1</u>** 

2 of 38 

hydrogen from the syngas increases the concentration of carbon dioxide, thereby facilitating the carbon capture afterwards (Ghiat and Al-Ansari, 2021; Madejski et al., 2022). Carbon dioxide can be captured from syngas, preventing its polluting release to the atmosphere (Dinca et al., 2018). Such captured carbon dioxide may be either stored underground or utilized commercially (Adu et al., 2019). This scenario is classified as a pre-combustion capture, because carbon dioxide is segregated from the fuel stream (syngas in this gas) before it is sent to the combustion facility (OFECM, 2022The two processes (hydrogen separation followed by carbon capture) improve the utilization of syngas. 

Hydrogen separation from a hydrogen-containing gas mixture can be accomplished by various methods, including membrane separation (Adhikari and Fernando, 2006). Palladium-based (Pdbased) membranes allow the production of high purity hydrogen (Iulianelli et al., 2014), which is important for effective operation of proton exchange membrane (PEM) fuel cells (Piemonte et al., 2014). Palladium-based membranes are known for selectively separating hydrogen from a gas stream (Peters and Caravella, 2019), which undergoes a dehydrogenation process as hydrogen is removed and passes across the membrane. Compared to the pressure swing adsorption (PSA), where adsorbing the impurities is used for hydrogen purification; membrane purification allows higher hydrogen recovery. Compared to cryogenic distillation, where impurities are condensed at low temperatures for purifying hydrogen; membrane purification is less energy intensive (Vermaak et al., 2021). Membrane-based hydrogen purification here refers to a pressure-driven process, where the selective permeation of hydrogen through the thin membrane is stimulated by a difference in the partial pressure of hydrogen as it is transferred from the retentate side (where hydrogen has a higher partial pressure) to the permeate side (where hydrogen has a lower partial pressure). 

This work considers hypothetical membranes that are unsupported (bulk), relatively-thick, dense (non-porous) palladium foils (Alique et al., 2018) for hydrogen separation. The mechanism of permeation through the membrane involves dissociation of molecular hydrogen at the surface of the palladium membrane as hydrogen atoms, which then diffuse into the palladium membrane (Oh et al., 2020). An isothermal (thus, having a uniform temperature) hydrogen separation module is adopted here. The spatial variation of the chemical composition of the permeate stream and retentate stream is modeled numerically as a plug-flow reactor. The permeation performance is examined under a reference set of representative conditions, as well as when each of three control (design) variables is changed from the reference (base) case. These control variables are: (1) the reactor temperature, (2) the retentate-side pressure, and (3) the permeate-side pressure. The study is based on computational modeling using principles in membrane-based hydrogen permeation. 

In the next section, the research method is described. Then, details about the geometric and inlet parameters are provided. Most of these settings remain fixed throughout the entire study. Then, the modeling procedure is described for the hydrogen permeation in the reactor. After this, five quantitative scalar quantities are introduced as criteria for evaluating the overall permeation performance. This is followed by presentation of results for a base case, combined with a discretization-sensitivity analysis that confirms the adequacy of the spatial resolution utilized. Then, the influence of three control variables is explored, with some regression models relating the value of each control variable to the five permeation metrics of the hydrogen permeation. Finally, concluding remarks are provided. 

The contribution of this work to the fields of energy systems, computational modeling, hydrogen production, and carbon capture includes: 

- Presenting a simple plug-flow reactor computational model for the membrane-based hydrogen separation, which takes a short time to give rough predictions as a precursor of time-consuming three-dimensional computational fluid dynamics (CFD) models. The simple plug-flow reactor model can be automated using spreadsheet software without the resorting to complicated computer programming or expensive software packages. It was checked for accuracy in terms of spatial resolution, and it passed successfully a resolution-independence test. 

- Providing results of a representative case of hydrogen separation out of a feedstock flow of pressurized syngas, giving insights about the distribution of the permeation flux along the unit, when 95% hydrogen recovery is attained 

**_Preprints.org_ (www.preprints.org)  |  NOT PEER-REVIEWED  |  Posted: 4 April 2025** 

**<u>doi:10.20944/preprints202504.0349.v1</u>** 

3 of 38 

- Demonstrating examples of consolidated metrics for comparing and judging the permeation performance of hydrogen. This can guide researchers when analyzing or interpreting similar problems. 

- Showing the impact of three different design variables on the hydrogen permeation performance, accompanied by good-fit regression models. This step helps in having a broad estimation of the advantage of manipulating each of these variable, which can be weighed against the expenses or practical difficulty in a realistic setting, thus helps in selecting optimum operational conditions. 

- Facilitating the validation of computational fluid dynamics (CFD) models for membrane reactors, by making available necessary details about geometric, inlet, and mass transport conditions with results from a plug-flow reactor model. While the CFD results may not agree perfectly with the presented plug-flow reactor results (due the additional complexity in the CFD models), the results of the plug-flow reactor model can still guide a researcher or modeler while validating their CFD models through approximate matching of aggregate scalar quantities or distribution profiles. Although specific cross-section details are not necessary for the performing the plug-flow reactor simulations, an imagined geometric configuration in the form of a shell-and-tube reactor is proposed, making the model upgradable to threedimensional simulation by the interested reader. The expected high slenderness ratio (lengthto-width ratio), lack of turbulators, and symmetry in the model here are advantageous in terms in reducing the gap between the plug-flow reactor performed here, and a three-dimensional CFD model. 

###### **2. Research Method** 

The research conducted here is computational in principle, and it relies on the modeling of hypothetical units for the permeation of hydrogen from a feedstock (feed) gases stream to a destination stream called permeate. 

The feed stream is representative of a realistic syngas flow in an integrated gasification combined cycle (IGCC), in which coal is converted into syngas (Krishnana et al., 2009; Berstad et al., 2011; GE, 2022). This syngas drives gas turbines as the first source of power generation, and the heat content in the exhaust gases is partially recovered to produce steam as a working fluid for steam turbines, serving as the second source of power generation (Wang, 2017). An IGCC power plant has an efficiency (with respect to the lower heating value, LHV) of about 48%, which means it has a higher efficiency (10-15% increase) and lower harmful emissions (10-15% reduction) compared to a conventional coal-fired power plant (Mitsubishi, 2022). 

The computational modeling is performed through spreadsheets (Microsoft Excel software program), where the mathematical equations governing the hydrogen permeation along the membrane length are implemented as dependent formulas. The built-in tool (Goal Seek) tool in this software was utilized for solving the nonlinear equation relating the unknown membrane length to the specified hydrogen recovery target (95%). Obtaining a solution using this nonlinear solver tool is nearly immediate on a personal computer. 

The variables that are subject to change in this work as independent parameters are: 

- The temperature of the membrane reactor (while keeping the retentate-side pressure and the permeate-side pressure at reference values of a base case) 

- The retentate-side pressure (while keeping the temperature and the permeate-side pressure at reference values of a base case) 

- The permeate-side pressure (while keeping the temperature and the retentate-side pressure at reference values of a base case) 

- For each of the three scenarios listed above, the influence of the isolated design variable on the 

- hydrogen permeation and fluid flow is investigated. 

A number of assumptions are made in the present work, which reduces interaction of factors and makes the interpretation of cause-effect dependence more evident. Such assumptions include the uniformity of the temperature, and ignoring the effect of permeation on the pressures. 

**_Preprints.org_ (www.preprints.org)  |  NOT PEER-REVIEWED  |  Posted: 4 April 2025** 

**<u>doi:10.20944/preprints202504.0349.v1</u>** 

4 of 38 

###### **3. General Model Settings** 

###### _3.1. Fixing Common Parameters_ 

This section illustrates various elements of the hydrogen separation modeling that remain unchanged for all simulation cases. They may be classified into two groups: (1) geometric parameters, (2) flow parameters. It should be noted that this work is not primarily intended to solve a particular problem or recommend a specific design. Instead, more value is provided through examining variations of permeation parameters when three operational variables are changed. Thus, any reasonable selection of settings is considered satisfactory here to establish a starting design point in the design space. 

###### _3.2. Underlying Geometry_ 

All the hydrogen separation modules investigated in this study share the same presumed geometric configuration except the length. The module is in the form of a shell-and-tube reactor, with 8 cylindrical tubes placed inside a cylindrical shell. The sum of the cross-sectional areas of the tubes is 50% of the cross-sectional area of the outer enclosing cylinder, which forms the outer boundaries of the shell. In this work, the term “shell” means the part of the outer enclosing cylinder that remains after subtracting the tubes. Thus, it refers to the passage available for the gaseous stream to flow around the tubes but within the outer enclosing cylinder. This stream is referred to as the (shell stream) or the (retentate). It is the fluid stream where the syngas feedstock enters and loses hydrogen during a dehydrogenation process to the other stream located inside the tubes. The retentate stream entering the shell is referred to as the (feed), which means the raw syngas supplied before any processing by the hydrogen permeation membranes. 

The other stream located inside the 8 tubes is the (tubes stream) or the (permeate). It is the destination of the hydrogen that is transported from the retentate through the palladium membranes. At the inlet of the permeate, a non-hydrogen gas of molecular nitrogen (N2) is supplied. This intentionally-added nitrogen is referred to as the (sweep gas) of the (sweep). While the use of such sweep gas is strictly-speaking optional, it helps improve the permeation process by ensuring that the permeate side can never be saturated with hydrogen, and it increases the difference in hydrogen partial pressures across the membrane, leading to an increased hydrogen permeation flux (Barbieri, 2015; Li et al., 2019). The added sweep gas can play another function of controlling the temperature (Chein et al., 2015), but this is not considered here as we assume the membrane reactor to be isothermal for simplicity. Other gases can also be used as a sweep gas, such as argon, Ar (Balachandran et al., 2011); steam, H2O (Chiesa et al., 2013); or helium, He (Brunetti et al., 2017). The use of nitrogen here seems adequate (GTI, 2007; Kinouchi et al., 2012). 

Figure 1 shows a proposed cross-section of the membrane reactor, indicating the areas of the 8 tubes (yellow color) and the area of the shell (white color). To obtain more-uniform gaps between walls, one of the tubes is placed exactly at the center of the shell. The remaining 7 tubes are arranged with equal circumferential spacing. It should be mentioned that the plug-flow reactor modelling conducted here utilizes the details about the layout of tubes when calculating the total perimeter of the palladium membranes (but the shell outer diameter is not utilized in the permeation calculation). In addition, such layout provides justification for the adopted membrane perimeter, and also helps the reader envision how the membrane reactor looks like in a real situation. 

# Oe Ore OC 



<!-- Start of picture text -->
Shell<br>Retentate (Shell) side<br>eed (hydrogen decreases)<br>(50% CO Cc<br>30% H, Tubes (only one<br>20% CO>) J of 8 shown)<br>Permeate (Tubes) side<br>(hydrogen increases) (100% N>)<br>Hydrogen Palladium<br>permeation membrane<br>= (tubes surface)<br>Feed Retentate (Shell) side<br>(hydrogen decreases)<br>‘Distance (x)<br><!-- End of picture text -->

**_Preprints.org_ (www.preprints.org)  |  NOT PEER-REVIEWED  |  Posted: 4 April 2025** 

**<u>doi:10.20944/preprints202504.0349.v1</u>** 

7 of 38 

|Inlet mole fraction, CO|50%|
|---|---|
|Inlet mole fraction, CO2|20%|
|Molecular weight, H2|2.01588 kg/kmol (NIST, 2021a)|
|Molecular weight, CO|28.0101 kg/kmol (NIST, 2021b)|
|Molecular weight, CO2|44.0095 kg/kmol (NIST, 2021c)|
|Molecular weight, mixture|23.412 kg/kmol|
|Inlet mass fraction, H2|0.025832|
|Inlet mass fraction, CO|0.598207|
|Inlet mass fraction, CO2|0.375961|
|Mass flow rate|60 kg/hr (132.28 lbm/hr)|
|Standard volume flow rate|970,068 sccm (standard cubic centimetersper minute)|
|Target hydrogen recovery|95% (bymass, bymole, or bystandard volume - identical)|



The mixture molecular weight of the feed (MWmix) is calculated from the mole fractions and molecular weights of the constituent gases as follows (Kuo, 2005): 

𝑴𝑾𝒎𝒊𝒙 = 𝐌𝐖𝐇𝟐 𝑿𝑯𝟐 + 𝐌𝐖𝐂𝐎 𝑿𝑪𝑶 + 𝐌𝐖𝐂𝐎𝟐 𝑿𝑪𝑶𝟐 (1) 

where (MW) refers to the molecular weight, (X) refers to the mole fraction, and the subscripts refer to the individual gases. 

The mass fraction (Y) for each constituent gas in the feed is dependent upon its mole fraction (X) according to (Poinsot and Veynante, 2005) 



where the subscript (i) refers to any gas of the constituent gases in the feed. 

The standard volume flow rate is the virtual volume flow if the temperature and pressure are at standard values, which are taken here as Tstnd = 0  C (32  C, 273.15 K) and Pstnd = 10<sup>5</sup> Pa (0.9869 atm, 14.504 psi). These two standard values are based on the International Union of Pure and Applied Chemistry, IUPAC (IUPAC, 1997). 

An ideal gas is a gas that obeys the ideal-gas equation of state: 𝑷 𝑽= 𝑵 𝑹̅ 𝑻, where (P) is the pressure, (V) is the volume, (N) is the number of moles, (R̅) is the universal gas constant, and (T) is the absolute temperature. For an ideal gas, each mole occupies a volume of 22,711 cm<sup>3</sup> (22.711 liters) at the standard pressure and temperature mentioned earlier. Thus, the standard volume is directly proportional to the number of moles, which is turn (and assuming no change occurs in chemical composition of the gas) is directly proportional to the mass. This value can be obtained from the idealgas equation of state by solving for the standard volume per mole (Vstnd/N) as: 

> 𝑽𝒔𝒕𝒏𝒅𝑵 = 𝐑̅ 𝑷𝑻𝒔𝒕𝒏𝒅𝒔𝒏𝒅 = (𝟏, 𝟎𝟎𝟎) (𝟖, 𝟑𝟏𝟒. 𝟓 𝐦𝐨𝐥.𝐊𝐉 ~~)~~ (𝟐𝟕𝟑.𝟏𝟓 𝐊𝟏𝟎<sup>𝟓</sup> 𝐏𝐚 ) = 𝟐𝟐, 𝟕𝟏𝟏 𝐜𝐦𝐦𝐨𝐥<sup>𝟑</sup> (3) 

where the multiplier (1,000) is inserted to convert from the volume unit from liters (L) to cubic centimeters (cm<sup>3</sup> ), and the value of the universal gas constant (R̅) is a physical constant is taken from the National Institute of Standards and Technology (NIST, 2018). The shown value in the above equation is a truncated version of the published one used in the computation, which is 8,314.462618 J/mol.K. 

Table 3 shows some details about the permeate stream, whose inlet conditions correspond to the sweep gas supplied to the membrane reactor. The temperature and pressure are considered uniform in that stream. 

**Table 3.** Some common details about the permeate stream. 

|**Condition**|**Value**|
|---|---|
|Inlet gas|100% N2|



**_Preprints.org_ (www.preprints.org)  |  NOT PEER-REVIEWED  |  Posted: 4 April 2025** 

**<u>doi:10.20944/preprints202504.0349.v1</u>** 

8 of 38 

|Molecular weight, N2|28.0134 kg/kmol (NIST, 2021d)|
|---|---|
|Mass flow rate|30.692 kg/hr (67.664 lbm/hr)|
|Standard volume flow rate|414,704 sccm (standard cubic centimeters per<br>minute)|
|Target outlet mole fraction of H2|40%|



The flow rate of the sweep gas is decided based on the target mole fraction of hydrogen in the permeate outlet (XH2,per-out), the mass flow rate of hydrogen in the syngas (ṁH2,feed), and the target hydrogen recovery (β). To demonstrate this dependence, consider a non-dimensional factor (α) defined as 

𝑴𝑾𝑵𝟐 (𝟏− 𝑿𝑯𝟐,𝒑𝒆𝒓−𝒐𝒖𝒕) 𝜶= 𝑴𝑾𝑯𝟐 𝑿𝑯𝟐,𝒑𝒆𝒓−𝒐𝒖𝒕 (4) 

The above equation is valid when having only nitrogen in the sweep gas (which is true in all the simulations in the present work). 

Then, the matching mass flow of the sweep gas (ṁsweep) is governed by 



The above equation is valid when not having any hydrogen in the sweep (which is true in all the simulations in the present work). 

In the present work, β = 0.95, XH2,per-out = 0.4, and ṁH2,feed = 1.5499 kg/hr (this is the product of the feed mass flow: 60 kg/hr, and the mass fraction of hydrogen in the feed: 0.025832). With the previously mentioned molecular weights of hydrogen (Table 2) and nitrogen (Table 3), we get ṁsweep = 30.692 kg/hr as mentioned in Table 3. 

The mass flow rates (and the standard volume flow rates) and the chemical compositions of the sweep gas and the feed gas are fixed in all the simulations of this work. 

###### **4. Modelling Hydrogen Permeation** 

###### _4.1. Segmental Plug-Flow Reactor_ 

For simulating the hydrogen permeation in the membrane reactor, piece-wise constant profiles are utilized to replace the continuous distributions along the membrane reactor. The membrane reactor is divided into (n) number of segments, having a small thickness and a constant cross-section. Each segment is assumed to have a uniform gas composition in either the permeate stream or in the retentate stream, and a uniform permeation flux. The flow is steady (time-independent), with a feed syngas entering from the left end (and leaving from the right after losing 95% of its hydrogen moles), and a sweep gas entering from the right end (and leaving from the left end after gaining the same amount of hydrogen lost from the syngas, and having a composition of 40% hydrogen and 60% nitrogen, by moles or volume). Such segmental approach for handling the one-dimensional evolution of the permeation process along the membrane reactor resembles a discretized version of a plug-flow reactor, PFR (AIChE, 2022). Instead of having infinitely-small segments (or plugs) in a true PFR, these segments here are finite. Also, instead of solving ordinary differential equations to find the composition distribution as a function of the longitudinal coordinate as in true PFR problems (Tuckerman, 2020), a numerical approach is used to describe that composition in adjacent segments, by ensuring continuity of the permeate flow and the retentate flow at the interfaces of each pair of adjacent segments. The hydrogen permeation occurs through the palladium membranes from the retentate to the permeate, with a single permeation rate assigned to each segment. 

###### _4.2. Modeling Algorithm_ 

Figure 3 explains the segmentation of the hypothetical membrane reactor. It shows a portion of its left end, with the two most-left segments. The left end of the membrane reactor is where the coordinate (x) is assigned the value zero. Because the segmental PFR model is aimed to capture the hydrogen permeation with no consideration of the flow pattern, only the membrane surface is of 



<!-- Start of picture text -->
Qaret-RHS,1 Qaret-RHS,2<br>Qua,Ret-RHS,1 Quz2,Ret-RHS,2<br>Retentate | Qretins1 Qret-ts,2 Qret-Ls,3<br>inlet Quz Ret-LHs,1 Quz,ret-LHs,2 Qua,Ret-LHs,3<br>(30% H, ines<br>by mole) > Hydrogen —<br>ry (\<br>Permeate IN<br>40%outletHy» <a mm <ol P| om<br>by mole) Palladium membrane<br>ON PermeateRetentate sideside J PermeateRetentate sideside<br>Retentate<br>inlet<br>(30% H> Segment 1 Segment 2<br>by mole) x Ax Ax<br><<<br>Qbper-LH5,1 Qper-tHs,2 Qper-LHs,3<br>Qu2,Per-LHs,1 Qua, Per-LHs,2 Quz,Per-LHs,3<br>Qber-RHS,1 Qber-RHs,2<br>Quz,Per-RHS,1 Quz,Per-RHs,2<br><!-- End of picture text -->

**_Preprints.org_ (www.preprints.org)  |  NOT PEER-REVIEWED  |  Posted: 4 April 2025** 

**<u>doi:10.20944/preprints202504.0349.v1</u>** 

10 of 38 

In the last equation, the product (XH2,Ret-LHS,1 QRet-LHS,1) gives the standard volume flow rate of the hydrogen content in the feed syngas. 



In the last equation, multiplying the standard volume flow rate of the hydrogen content in the feed syngas (QH2,Ret-LHS,1) by the target hydrogen recovery (  ) gives the target standard volume flow rate of the hydrogen content in the permeate stream as it exits the entire membrane reactor from its left end. Dividing this value further by the target mole fraction of the exiting permeate stream (XH2,PerLHS,1) gives the target standard volume flow of the exiting permeate stream (QPer-LHS,1), which is composed of molecular hydrogen and molecular nitrogen. Performing these calculations gives QPerLHS,1 = 691,173 sccm. 

For other segments except the first one (i = 2, 3, … n), the connectivity condition of the segments (interfacing condition) can be used as follows 



where the values of (XH2,Ret-RHS,i–1), (QRet-RHS,i–1), (QH2,Ret-RHS,i–1), (XH2,Per-RHS,i–1), and 

- (QRet-RHS,i–1) should be available from the analysis of the previous segment (numbered i–1). 

- b) Compute (QH2,Per-LHS,i), which is the standard volume flow rate of the hydrogen content in the permeate stream at the LHS of the current segment being analyzed (say segment i), as follows: 

   - 𝑸𝑯𝟐,𝑷𝒆𝒓−𝑳𝑯𝑺,𝒊 = 𝑿𝑯𝟐,𝑷𝒆𝒓−𝑳𝑯𝑺,𝒊  𝑸𝑷𝒆𝒓−𝑳𝑯𝑺,𝒊 (16) 

- c) Compute (ΔPH2<sup>0.5</sup> )LHS,i, which is the difference in the partial pressures of hydrogen raised to the power of 0.5 (which is the driving force for hydrogen permeation through the palladium membrane) at the LHS of the current segment being analyzed (say segment i), as follows: 

(𝚫𝑷𝟎.𝟓𝑯𝟐)𝑳𝑯𝑺,𝒊 = (𝑿𝑯𝟐,𝑹𝒆𝒕−𝑳𝑯𝑺,𝒊  𝑷𝑹𝒆𝒕)𝟎.𝟓 −(𝑿𝑯𝟐,𝑷𝒆𝒓−𝑳𝑯𝑺,𝒊  𝑷𝑷𝒆𝒓)𝟎.𝟓 (17) 

where (PRet) is the absolute pressure of the retentate stream, and (PPer) is the absolute pressure of the permeate stream. Since the retentate stream is assumed to have a constant pressure, there is no need to add details (a subscript index) about the location for its value to be used in the above equation. The same reason justifies not specifying a particular location for the permeate pressure. 

- d) Compute ( ~~JH~~ 2,i), which is a predicted (first-iteration) segment-level molar flux of permeating hydrogen through the palladium membrane based on the conditions at LHS of the current segment being analyzed (say segment i), as follows: 



This predicted flux value is an initial estimation, based on LHS conditions only. In a subsequent step of the present algorithm, it is refined by including effects of RHS conditions. 

The above equation is referred to as Richardson’s equation (Campo et al., 2011) or Sieverts’ law (Alraeesi and Gardner, 2021). The factor (k’) is an ideal (or local, or actual) permeance for hydrogen permeation, and it is calculated as 



where (A) is a pre-exponential factor for hydrogen permeation, (  ) is the thickness of the palladium membrane, (E) is an activation energy for hydrogen permeation, and (T) is the absolute temperature (in kelvins). The values of (A) and (E) used here are (Koffler et al., 1969; Morreale et al., 2003) 

A = 2.2  10<sup>–7</sup> mol/m/s/Pa<sup>0.5</sup> 

E = 15,670 J/mol 

The thickness of the palladium membrane is set to 80  m, which is considered a reasonable value (Marzouk, 2017; Yuan et al., 2019). 

- e) Convert the LHS-based first-iteration molar flux ( ~~J~~ H2,i) to a predicted (first-iteration) segmentlevel standard volume flow rate of permeating hydrogen ( ~~QH~~ 2,i) for the current segment being analyzed (say segment i). 

**_Preprints.org_ (www.preprints.org)  |  NOT PEER-REVIEWED  |  Posted: 4 April 2025** 

**<u>doi:10.20944/preprints202504.0349.v1</u>** 

11 of 38 

This temporary standard volume flow rate value is an initial estimation, based on LHS conditions only. In a subsequent step of the present algorithm, it is refined by including effects of RHS conditions. It is computed as follows: 

~~𝑸𝑯~~ 𝟐,𝒊<sup>= 𝝀</sup><sup>~~𝑱~~</sup> ~~𝑯~~ 𝟐,𝒊<sup>𝑨</sup> 𝒔𝒆𝒈 (20) 

where (Aseg) is the membrane surface area in one segment, and (  ) is a constant that arises from a necessary unit conversion, as follows: 

𝝀= 𝟐𝟐, 𝟕𝟏𝟏 𝐦𝐨𝐥𝐬𝐜𝐜 𝟔𝟎 𝐦𝐢𝐧𝐬 (21) 

where (scc) stands for (standard cubic centimeters). This gives  = 1.36266  10<sup>6</sup> scc.s/mol.min. 

When computing the segmental membrane area, the envisioned tubes layout in the shell-andtube design and its specified dimensions become necessary. 

If the tube diameter is designated by the symbol (d), and the length of the entire membrane reactor is designated by the symbol (L), then for 8 tubes and (n) segments, the length of a single segment is 



and the membrane area within a single segment is 



where (  = 3.14159) is the traditional mathematical constant. 

- f) Compute ( ~~XH~~ 2,Ret-RHS,i) and ~~(XH~~ 2,Per-RHS,i), which are predicted (first-iteration) mole fractions of hydrogen in the retentate stream and the permeate stream, respectively at the RHS of the current segment being analyzed (say segment i), as follows: 



- g) Compute (ΔPH2<sup>0.5</sup> )RHS,i, which is the difference in the partial pressures of hydrogen raised to the power of 0.5 (as the driving force for hydrogen permeation) at the RHS of the current segment being analyzed (say segment i), as follows: 

   - (𝚫𝑷𝟎.𝟓𝑯𝟐)𝑹𝑯𝑺,𝒊 = (𝑿𝑯𝟐,𝑹𝒆𝒕−𝑹𝑯𝑺,𝒊  𝑷𝑹𝒆𝒕)𝟎.𝟓 −(𝑿𝑯𝟐,𝑷𝒆𝒓−𝑹𝑯𝑺,𝒊  𝑷𝑷𝒆𝒓)𝟎.𝟓 (26) 

- h) Compute (ΔPH2<sup>0.5</sup> )i, which is the difference in the partial pressures of hydrogen raised to the power of 0.5 assigned to the current segment being analyzed (say segment i). It is taken as the arithmetic average of the LHS value and the RHS value, as follows: 

      - 𝟎.𝟓 𝟎.𝟓 𝟎.𝟓 

      - (𝚫𝑷𝑯𝟐)𝒊 = 𝟎. 𝟓 ((𝚫𝑷𝑯𝟐)𝑳𝑯𝑺,𝒊 + (𝚫𝑷𝑯𝟐)𝑹𝑯𝑺,𝒊) (27) 

- i) Compute (JH2,i), which is a corrected (second-iteration) segment-level molar flux of permeating hydrogen through the palladium membrane, which includes driving forces for permeation at both sides of the current segment being analyzed (say segment i), as follows: 

         - 𝑱𝑯𝟐,𝒊 = 𝒌<sup>′</sup> (𝚫𝑷𝟎.𝟓𝑯𝟐)𝒊 (28) 

- j) Convert the corrected, segment-level molar flux (JH2,i) to a corresponding updated (refined) segment-level standard volume flow rate of permeating hydrogen (QH2,i) for the current segment being analyzed (say segment i), as follows: 



This is considered the final representation of the segment-level permeation of hydrogen. 

- k) Compute (RH2,i), which is the hydrogen recovery due to the current segment being analyzed (say segment i), as follows: 

𝑹𝑯𝟐,𝒊 = 𝑸𝑯𝟐,𝒊⁄𝑸𝑯𝟐,𝑹𝒆𝒕−𝑳𝑯𝑺,𝟏 (30) 

The denominator (QH2,Ret-LHS,1) in the previous equation is basically the standard volume flow rate of hydrogen in the inlet feed syngas. Thus, it is the standard volume flow of hydrogen available for permeation. 

The segmental contribution to the overall recovery (RH2,i) can help in studying the distribution of the permeation, and thus identifying portions of the membrane reactor that are more effective than others. 

**_Preprints.org_ (www.preprints.org)  |  NOT PEER-REVIEWED  |  Posted: 4 April 2025** 

**<u>doi:10.20944/preprints202504.0349.v1</u>** 

12 of 38 

- l) <u>Optional: Compute (RH2,i), which is the cumulative hydrogen recovery, due to all previous</u> segments of the membrane reactor in addition to the current segment being analyzed (say segment i), as follows: 

𝑹̂𝑯𝟐,𝒊 = ∑𝒊𝒎=𝟏 𝑹𝑯𝟐,𝒊 (31) 

While this value is not necessary for continuing the calculation process, it is part of the data visualization of results here. It is thus beneficial to explain how it is obtained. 

- m) Compute (QRet-RHS,i) and (QH2,Ret-RHS,i), which are the standard volume flow rate of the retentate stream and the hydrogen content in that retentate stream, respectively at the RHS of the current segment being analyzed (say segment i), as follows: 

         - 𝑸𝑹𝒆𝒕−𝑹𝑯𝑺,𝒊 = 𝑸𝑹𝒆𝒕−𝑳𝑯𝑺,𝒊 −𝑸𝑯𝟐,𝒊 (32) 

      - 𝑸𝑯𝟐,𝑹𝒆𝒕−𝑹𝑯𝑺,𝒊 = 𝑸𝑯𝟐,𝑹𝒆𝒕−𝑳𝑯𝑺,𝒊 −𝑸𝑯𝟐,𝒊 (33) 

- n) Compute (XH2,Ret-RHS,i), which is the corrected (second-iteration) mole fraction of hydrogen in the retentate stream at the RHS of the current segment being analyzed (say segment i), as follows: 

   - 𝑿𝑯𝟐,𝑹𝒆𝒕−𝑹𝑯𝑺,𝒊 = 𝑸𝑯𝟐,𝑹𝒆𝒕−𝑹𝑯𝑺,𝒊⁄𝑸𝑹𝒆𝒕−𝑹𝑯𝑺,𝒊 (34) 

- o) Compute (QPer-RHS,i) and (QH2,Per-RHS,i), which are the standard volume flow rate of the permeate stream and the hydrogen content in that permeate stream, respectively at the RHS of the current segment being analyzed (say segment i), as follows: 

      - 𝑸𝑷𝒆𝒓−𝑹𝑯𝑺,𝒊 = 𝑸𝑷𝒆𝒓−𝑳𝑯𝑺,𝒊 −𝑸𝑯𝟐,𝒊 (35) 

𝑸𝑯𝟐,𝑷𝒆𝒓−𝑹𝑯𝑺,𝒊 = 𝑸𝑯𝟐,𝑷𝒆𝒓−𝑳𝑯𝑺,𝒊 −𝑸𝑯𝟐,𝒊 (36) 

- p) Compute (XH2,Per-RHS,i), which is the corrected (second-iteration) mole fraction of hydrogen in the permeate stream at the RHS of the current segment being analyzed (say segment i), as follows: 

   - 𝑿𝑯𝟐,𝑷𝒆𝒓−𝑹𝑯𝑺,𝒊 = 𝑸𝑯𝟐,𝑷𝒆𝒓−𝑹𝑯𝑺,𝒊⁄𝑸𝑷𝒆𝒓−𝑹𝑯𝑺,𝒊 (37) 

- q) Set the obtained RHS conditions of current segment being analyzed (say segment i) as LHS conditions at the next adjacent segment to be analyzed (segment i+1), and repeat the computation procedure sequentially for all remaining segments until the last membrane segment (segment n). 

The following values should be obtained for each segment: 

- (ΔPH2<sup>0.5</sup> )LHS,i 

- ~~JH~~ 2,i 

- ~~QH~~ 2,i 

- ~~XH~~ 2,Ret-RHS,i and ~~XH~~ 2,Per-RHS,i 

- (ΔPH2<sup>0.5</sup> )RHS,i 

- (ΔPH2<sup>0.5</sup> )i 

- JH2,i 

- QH2,i 

- RH2,i 

- <u>Optional: RH2,i</u> 

- QRet-RHS,i and QH2,Ret-RHS,i 

- XH2,Ret-RHS,i 

- QPer-RHS,i and QH2,Per-RHS,i 

- XH2,Per-RHS,i 

- r) Compute (RH2,n), which is the cumulative hydrogen recovery at the last segment. It is the overall hydrogen recovery by the entire membrane reactor, and it is obtained by simply adding the segment-level hydrogen recovery (RH2,i) for all the (n) segments of the membrane reactor. The total cumulative value is itself the target hydrogen recovery (  ). Therefore 

𝜷 𝐨𝐫 𝑹̂𝑯𝟐,𝒏 = ∑𝒏𝒎=𝟏 𝑹𝑯𝟐,𝒊 (38) 

The hydrogen recovery is an important success criterion not only from the chemical perspective, but also from an economic perspective. A higher hydrogen recovery leads to a lower cost per unit mass of hydrogen produced (Nordio et al., 2021). 

In the presented algorithm, the length of the entire membrane (L) is a nonlinear function of the overall hydrogen recovery (  ). Since (  ) is fixed at a desired value of 95% (in all the simulation cases of this study), a matching membrane length (L) should be solved for. Solving such non-linear system of equations is achieved here using the (Goal Seek) tool in the Microsoft Excel software program. This 

**_Preprints.org_ (www.preprints.org)  |  NOT PEER-REVIEWED  |  Posted: 4 April 2025** 

**<u>doi:10.20944/preprints202504.0349.v1</u>** 

13 of 38 

tool is useful only when the equation or system of equations relate a single independent variable to a single dependent variable (Microsoft, 2022). This condition is satisfied in the segmented plug-flow reactor problems here, with the independent variable being the membrane length, and the dependent variable being the hydrogen recovery. 

###### **5. Assessing Hydrogen Permeation** 

###### _5.1. Permeation Metrics_ 

After performing a complete steady-state simulation for the palladium membrane permeation of hydrogen in a segmented plug-flow reactor, assessment of the overall permeation process is facilitated using a number of quantitative scalar quantities (referred to here as performance metrics or permeation metrics), that are convenient to utilize for comparing the performance of different simulations. In this section, five performance metrics for hydrogen separation are discussed. 

###### _5.2. Membrane Length_ 

The first permeation performance metric adopted here is the needed membrane length to achieve the target hydrogen recovery (  = 95%). This is designated by the symbol (L). 

A smaller membrane length is desired, because it means a shorter membrane reactor, which is a better design due to reduced cost and space. 

###### _5.3. Average Hydrogen Permeation Mass Flux_ 

The second permeation performance metric adopted here is average mass flux (mass flow rate per unit area) of the permeated hydrogen through the membrane. It is designated by the symbol (M̅H2). Since the local mass flux of the permeated hydrogen is subject to variation from one segment to another in the membrane reactor model, the average of all segmental values is used. This metric is related to the corrected (second-iteration) segment-level molar flux of permeating hydrogen through the palladium membrane (JH2,i) as 

𝑴̅𝑯𝟐 = 𝟑. 𝟔 𝑴𝑾𝑯𝟐 𝒏𝟏 ∑𝒏𝒊=𝟏 𝑱𝑯𝟐,𝒊 (39) 

where (MWH2 = 2.01588 kg/kmol) is the molecular weight of the molecular hydrogen, and the factor (3.6) appears to enable unit conversion such that the average mass flux is expressed in (kg/m<sup>2</sup> .hr) when the segmental mole flux (JH2,i) is expressed in (mol/m<sup>2</sup> .s). 

A higher average mass flux is desired, as it shows more intense utilization of the membrane surface (better use of each unit area). 

In the present study, because the total permeated hydrogen is fixed (by fixing the inlet mass flow of hydrogen in the syngas feed and fixing the target hydrogen recovery), and the membrane perimeter is also fixed, the average hydrogen mass flux (M̅H2) and the membrane length (L) are not independent. Instead, they are inversely proportional to each other, and their product should be invariant. 

###### _5.4. Log Mean Pressure-Square-Root Difference_ 

The third permeation performance metric adopted here is a global (membrane-level, not a segment-level) pressure-square-root difference, which is a membrane-level difference of the hydrogen partial pressure raised to the power of 0.5, between the retentate stream (higher value) and the permeate stream (lower value). It is designated here by the symbol (LMPsrD) or simply (LMPD), and is called log (or logarithmic) mean pressure-square-root difference. This difference in the square root of the hydrogen partial pressure (PsrD) stimulates the permeation through the palladium membrane. Because this stimulus driving force can vary along the membrane segments, an average value is sought. Instead of a simple arithmetic average over all segments, a logarithm-based average is used, which takes into account the differences at the left end and at the right end of the entire membrane reactor (where the flow inlets and outlets are located). This resembles an approach of 

**_Preprints.org_ (www.preprints.org)  |  NOT PEER-REVIEWED  |  Posted: 4 April 2025** 

**<u>doi:10.20944/preprints202504.0349.v1</u>** 

14 of 38 

calculating an overall temperature difference in the field of heat transfer within heat exchangers, which is called log mean temperature difference, or LMTD (Utamura et al., 2008). The global log mean pressure-square-root difference is calculated as follows: 



where ( Δ PH2<sup>0.5</sup> )LHS,1 is the driving force at the left end of the membrane reactor (at x = 0), ( Δ PH2<sup>0.5</sup> )RHS,n is the driving force at the right end of the membrane reactor (at x = L), and the (ln) function is the natural logarithm. The LMPD should lie between ( Δ PH2<sup>0.5</sup> )LHS,1 and ( Δ PH2<sup>0.5</sup> )RHS,n, regardless of which of them is larger than the other. 

A higher log mean pressure-square-root difference (LMPD) is desired, as it is an indicator of the average driving force for hydrogen permeation between the left end and the right end of the membrane reactor, and is interpreted in a similar way to the LMTD in heat exchanges, being the driving force for heat transfer (Lienhard IV and Lienhard V, 2019). 

###### _5.5. Global Apparent Permeance_ 

The fourth permeation performance metric adopted here is the global apparent permeance (k’app), which is a solution-dependent variable that represents the effective permeance based on the obtained profile of hydrogen permeation in the membrane reactor. It has the same unit of the actual (ideal) permeance (k’), which is an input parameter that depends on the temperature and the membrane length, and thus can be computed prior to the numerical simulation of the plug-flow reactor. Despite being the same for all segments for any simulation in this work, the actual permeance (k’) in general is a local value, corresponding to a specific segment (or even a specific point), whereas the apparent permeance is computed based on the overall performance of the membrane reactor as a whole, as follows: 



The numerator in the above equation is the arithmetic average of the molar flux of permeating hydrogen through the palladium membrane (average of the n segmental values), while the denominator is the log mean pressure-square-root difference (LMPD). 

A higher apparent permeance is desired, as it shows that the membrane reactor yields a higher useful output (hydrogen molar flux) for a given average input (hydrogen pressure driving force). 

###### _5.6. Efficiency Factor_ 

The fifth and last permeation performance metric adopted here is the efficiency factor (  k), which is simply the ratio of the global apparent permeance to the local actual permeance, expressed as a percentage. Therefore, 



The efficiency factor is the only permeation metric presented here that is non-dimensional, which makes it unambiguous and identical in any system of units. 

The “efficiency factor” is not strictly an efficiency as used in energy conversion by a heat engine, being an output useful energy that is a fraction of an input heat energy, thus limited to a ceiling value of 100% (Bandyopadhyay, 2021). Instead, the “efficiency factor” is a ratio between two quantities that have the same dimensional units but have different meanings and either of them is allowed to exceed the other. Thus, the “efficiency factor” used here can exceed 100%. 

A higher efficiency factor is desired, as it is directly proportional to the global apparent permeance, thus it is related to the goodness of the membrane reactor operation with regard to hydrogen permeation. 

###### **6. Results** 

_6.1. Base Case and Spatial Resolution Test_ 

**_Preprints.org_ (www.preprints.org)  |  NOT PEER-REVIEWED  |  Posted: 4 April 2025** 

**<u>doi:10.20944/preprints202504.0349.v1</u>** 

15 of 38 

The first implementation of the plug-flow membrane reactor model is referred to as the base case or reference simulation. Three needed thermodynamic properties for the two flowing fluids in the reactor are needed to run a simulation, which are 

- Temperature (assumed uniform in the entire reactor) 

- Retentate pressure (assumed uniform in the retentate stream) 

- Permeate pressure (assumed uniform in the permeate stream) 

The uniform-temperature assumption avoids ambiguity when computing the actual (ideal) permeance of the palladium membrane, which is temperature dependent. Thus, the actual permeance is also uniform in the entire membrane, and this eliminates an undesirable distracting influence from a varying permeance. 

The three aforementioned thermodynamic properties are to be varied individually later, deviating from their base values. And the influence of each of them on the hydrogen permeation is examined. 

The base case is considered to have representative (realistic) values of the membrane streams (Tan et al., 2015; Leonzio, 2018; Vita and Italiano, 2020), which they are summarized in Table 4. 

**Table 4.** Temperature and pressures of the base case (reference simulation). 

|**Fluid property**|**Value**|
|---|---|
|Temperature|300C (572.00F)|
|Absolute retentatepressure|40.0 atm (587.84psia)|
|Absolute permeate pressure|20.0 atm (293.92 psia)|



The local actual hydrogen permeance (k’) for the base temperature of (300  C, 573.15 K) is 10.263  10<sup>–4</sup> mol/m<sup>2</sup> .s.Pa<sup>0.5</sup> . 

Table 5 gives numerical results for the base case after a complete simulation of the segmented plug-flow reactor for it. The normal resolution of 200 segments is compared with another resolution with twice the number of segments (400 segments) having the same membrane length found necessary for the 200-segment case. 

Also, the absolute percentage deviations of these results between the two resolutions are shown in the table. Such comparison reveals small deviations not exceeding 2% in all the four permeation performance metrics other than the membrane length, which was forced to be identical in the two simulations. Namely, these metrics are: (1) average hydrogen permeation mass flux, (2) log mean pressure-square-root difference, (3) global apparent hydrogen permeance, and (4) efficiency factor. For the hydrogen recovery, it was a specified input in the case of using 200 segments, 

where the membrane length was a computed output. In the case of using 400 segments, the membrane length was the specified input (to ensure geometric consistency between the two simulations), while the hydrogen recovery was computed from the segmented plug-flow reactor model, in an inverse simulation mode. There is an insignificant difference (0.01% absolute change) in the two values of the hydrogen recovery. 

**Table 5.** Some results obtained for the base case with 200 segments (normal resolution) and 400 segments (refined resolution for testing only). 

|**Result**|**Va**<br>n = 200|**lue**<br>n = 400|**Absolute percentage**<br>**change**<br>|Value(200)–Value(400)||
|---|---|---|---|
||segments|segments|Value(200)|











<!-- Start of picture text -->
feed Tygments Cumulative H, Recovery sweep<br>== 400 segments Total length: 407.359 cm am<br>100% =<br>90% Pt tT tT tT TT | ETT |<br>ee70%60% EEE PtEEEtT tT ee eeTT tT<br>40%50% - | | | | o>.~ac| | | | | |<br>A |<br>30% leo tit ttt tT tt tt<br>10%<br>EEE EEE<br>oor | | tt tt tT ETT | |<br>o w wi wn N wn om wn st w wn nw wo wn Ss w oo w oo nw ei<br>gegesegs<br>esse Re Fses Fs s<br>Normalized distance from the left edge of the reactor (feed inlet)<br><!-- End of picture text -->



<!-- Start of picture text -->
feed | H, Recovery by Each Membrane Segment sweep<br>— 200 segments<br>= 400 segments Total length: 407.359 cm om<br>0.8% =<br>0.7% So fo a<br>h —<br>0.5%<br>0.4% ORE |__| _|_ 1<br>0.3% = eas a= T { 4<br>, 7<br>0.1% Oo<br>0.0%<br>°o wn ei n N n m wn t wn n wn wo wn Ss wn o wn 0) n S|<br>Sco AH 6 XN SG MS BTS HSELSEHR SBS BD<br>o o o o °o °o °o o o o<br>Normalized distance from the left edge of the reactor (feed inlet)<br><!-- End of picture text -->



<!-- Start of picture text -->
—200 segments H, Mole Fraction (Retentate) sweep<br>30% = sme 400 segments Total length: 407.359 cm oJ<br>25% TSA LEE EEE EEE EEL<br>_— _<br>15% TT<br>"COE~an<br>0%5% LETTETT ETT ETT ET TEES<br>con eA HN HM HOt HH Hh HH © HR H OD H D HH A<br>So HAH o KN 6G Mo Fo f#RK SG Bs EG A SG BB<br>°o o o °o °o i=) o o o o<br>Normalized distance from the left edge of the reactor (feed inlet)<br><!-- End of picture text -->



<!-- Start of picture text -->
| feed | --+» 200 segments H, Mole Fraction (Permeate) sweep<br>40% = ~ — 400 segments Total length: 407.359 cm oJ<br>~~<br>” a Oe<br>EH | | | | | | | | | |<br>CEES<br>ot tt| Pa<br>wt tttET es<br>wm |tttttt tt Tee, t<br>wx tttttt tt i =<br>o wn A | nw N wn m w vt wn w wn wo nw Ss wn oo nw t+) w ei<br>SCso oG26 oNG oMR SGXTSOHRGLSEARo i=) o i=) GBSo B®°o<br>Normalized distance from the left edge of the reactor (feed inlet)<br><!-- End of picture text -->

**_Preprints.org_ (www.preprints.org)  |  NOT PEER-REVIEWED  |  Posted: 4 April 2025** 

**<u>doi:10.20944/preprints202504.0349.v1</u>** 

19 of 38 

With such observed good agreement between the normal spatial resolutions and the testing high resolution, the choice of 200 segments (normal resolution) is considered satisfactory, and is adopted in all remaining simulations. 

###### _6.2. Influence of Temperature_ 

After completing the segmented flow reactor under a set of representative operational conditions, the temperature of the flows in the membrane reactor is varied in a discrete manner, leading to a number of temperatures higher than the base value of 300  C.  The base value and the 6 additional temperatures are: 

1. 300  C (base) 

2. 350  C 

3. 400  C 

4. 500  C 

5. 600  C 

6. 700  C 

7. 800  C 

It is understood that high temperatures may pose practical challenge for the materials and the process feasibility. Despite this, the model allows exploring the change in the permeation performance due to elevated temperatures. This is achieved by monitoring the changes in the five performance metrics due to the changes in the temperature alone. The other two design variables (retentate pressure and permeate pressure) are kept at their base values (40 atm absolute and 20 atm absolute, respectively). 

Figure 8 shows the influence of the temperature on the first hydrogen permeation metric, which is the membrane length. There is a nonlinear decline, which can be described by a nonlinear powertype regression model. In the equation shown within the figure, (x) refers to the temperature in degrees Celsius, T(  C), while (y) refers to the membrane length in meters, L(cm). Therefore, 

𝑳(𝐜𝐦) = 𝟑. 𝟎𝟑𝟔𝟒× 𝟏𝟎<sup>𝟔</sup> 𝑻(°𝐂)<sup>−𝟏.𝟓𝟔𝟕𝟔</sup> (43) 

Thus, the temperature is an instrumental variable to limit the membrane length (for a given target hydrogen recovery) to less than 25% of its base value. Thus, it is equally instrumental to increase the hydrogen recovery for a given geometric length. 



<!-- Start of picture text -->
Membrane Length (cm)<br>450<br>400 y = 3.0364E6 x 19676<br>&<br>350<br>300<br>250<br>200<br>150<br>100<br>50<br>0<br>300 400 500 600 700 800<br>Temperature (°C)<br><!-- End of picture text -->



<!-- Start of picture text -->
Average Hydrogen Permeation Mass Flux (kg/m2.hr)<br>6<br>y = 0.0084087 x — 1.4491<br>5 R? = 0.9990<br>4<br>3<br>2<br>1°<br>0<br>300 400 500 600 700 800<br>Temperature (°C)<br><!-- End of picture text -->



<!-- Start of picture text -->
Pressure-square-root Difference - PsrD (Pa®>)<br>1,100<br>Left<br>1,000<br>4-Right<br>900<br>-—@-Log mean<br>800<br>700<br>600<br>500<br>400<br>300<br>200 @ §@ @ @ #@ # #g@ 4<br>300 400 500 600 700 800<br>Temperature (°C)<br><!-- End of picture text -->



<!-- Start of picture text -->
Hydrogen Permeance (mol/m72.s.Pa®>), and Efficiency Factor (%)<br>0.0060 120%<br>-2-Local actual permeance<br>0.0050 110%<br>Global apparent permeance °<br>0.0040 —-Efficiency factor 100%<br>0.0030 90%<br>0.0020 80%<br>0.0010 70%<br>S13 $ 9 $$$ $a $a —_ ><br>0.0000 60%<br>300 350 400 500 600 700 800<br>Temperature (°C)<br><!-- End of picture text -->

#### Membrane Length (cm) 



<!-- Start of picture text -->
450<br>400 y = 4.3331E-5 x? - 0.015423 x? + 2.0356 x? - 119.74x +<br>2,812.2<br>350<br>300<br>250<br>200 SS<br>150<br>a<br>100 "8 oC e eee err Te<br>50<br>0<br>40 50 60 70 80 90 100 110 120<br>Retentate Absoulte Pressure (atm)<br><!-- End of picture text -->



<!-- Start of picture text -->
Average Hydrogen Permeation Mass Flux (kg/m2.hr)<br>6<br>y = 0.051720 x — 0.75288 =<br>;<br>R? = 0.9931<br>4a<br>|.<br>;<br>0<br>40 50 60 70 80 90 100 110 120<br>Retentate Absoulte Pressure (atm)<br><!-- End of picture text -->



<!-- Start of picture text -->
Pressure-square-root Difference - PsrD (Pa®->)<br>1,100<br>—e—Left<br>1,000<br>900 A~ Right y = 442.40 In(x) - 1,412.6<br>800<br>—@-— Log mean<br>700 —e<br>600<br>500 A<br>+<br>400 A<br>A<br>1<br>300 =<br>200 &<br>40 50 60 70 80 90 100 110 120<br>Retentate Absoulte Pressure (atm)<br><!-- End of picture text -->



<!-- Start of picture text -->
Hydrogen Permeance (mol/m2.s.Pa®°5), and Efficiency Factor (%)<br>0.0050 120%<br>0.0040 => 100%<br>-2-Local actual permeance 80%<br>0.0030<br>Global apparent permeance 60%<br>0.0020 —1- Efficiency factor 40%<br>0.0010 70%<br>0.0000 0%<br>40 45 50 60 70 80 100 120<br>Retentate Absoulte Pressure (atm)<br><!-- End of picture text -->

**_Preprints.org_ (www.preprints.org)  |  NOT PEER-REVIEWED  |  Posted: 4 April 2025** 

**<u>doi:10.20944/preprints202504.0349.v1</u>** 

27 of 38 

###### _6.4. Influence of Permeate Pressure_ 

In this subsection, the impact of the permeate pressure (the last design variable considered in this study) on the permeation metrics is discussed. Seven additional simulations with different values of the absolute permeate pressure were conducted with the aim of capturing the trend of the permeation performance when the permeate pressure decreases from the base value of 20 atm (absolute) to a small value near absolute vacuum. The base value and 7 additional absolute permeate pressures are: 

1. 20 atm (base) 

2. 17.5 atm 

3. 15 atm 

4. 10 atm 

5. 5 atm 

6. 1 atm 

7. 0.5 atm 

8. 0.2 atm 

The other two design variables (temperature and retentate pressure) are kept at their base values (300  C and 40 atm absolute, respectively). Unlike the temperature and the retentate pressure, where larger values than the base values were investigated, smaller values of permeate pressures are investigated here for seeking better permeation, since this permeation pressure has a resistive effect for permeation (not a supportive effect as the temperature and the retentate pressure). 

Figure 16 shows the influence of the permeate pressure on the first hydrogen permeation metric, which is the membrane length. There is a nonlinear (nearly exponential) increase in the membrane length as the retentate pressure increases. This relation can be described by the following regression model: 

###### 𝑳(𝐜𝐦) = 𝟗𝟑. 𝟏𝟎𝟓 𝒆<sup>𝟎.𝟎𝟕𝟏𝟗𝟐 𝑷𝑷𝒆𝒓(𝐚𝐭𝐦,𝐚𝐛𝐬𝐨𝐥𝐮𝐭𝐞)</sup> (49) 

Although manipulating the permeate pressure can reduce the membrane length (for a given target hydrogen recovery) to less than 25% of its base value (which was also achievable by manipulating the temperature or the retentate pressure), partial vacuum is needed for achieving this, with pressures below the normal atmospheric pressure of 1 atm. This imposes complications and expense, and may not be acceptable. However, the reduction in the permeate pressure within morerealistic values (like 10 atm, absolute) has still a favorable effect and the membrane length can decrease to less than half of its base value by halving the absolute permeate pressure. 



<!-- Start of picture text -->
Membrane Length (cm)<br>450<br>400 y = 93.105 e9.07192 x<br>,<br>y,<br>350<br>90 ee — y<br>200<br>150<br>-<br>100<br>50<br>0<br>° ° 10 15 50<br>Permeate Absoulte Pressure (atm)<br><!-- End of picture text -->



<!-- Start of picture text -->
Average Hydrogen Permeation Mass Flux (kg/m2.hr)<br>6<br>5 @<br>; ee<br>.<br>y = 5.0339 7007192<br>1<br>0<br>0 5 10 15 20<br>Permeate Absoulte Pressure (atm)<br><!-- End of picture text -->



<!-- Start of picture text -->
Pressure-square-root Difference - PsrD (Pa®->)<br>1,100<br>1,000 O° Left<br>900 A~— Right<br>800 y = 571.05 @-0.04471 x<br>—@— Log mean<br>700<br>600<br>500 Se. ee,<br>°<br>400<br>300 mwa + i<br>200<br>0 5 10 15 20<br>Permeate Absoulte Pressure (atm)<br><!-- End of picture text -->



<!-- Start of picture text -->
Hydrogen Permeance (mol/m2.s.Pa®°), and Efficiency Factor (%)<br>0.0050 120%<br>0.0040 100%‘0,<br>0.0030 -=Local actual permeance 80%<br>Global apparent permeance >><br>a 60%<br>—-Efficiency factor<br>0.0020<br>40%<br>a—__a-_4+-<br>0.0010 =. ——_242__-—_2—"__8) 20%<br>0.0000 0%<br>0.2 0.5 1 5 10 15 17.5 20<br>Permeate Absoulte Pressure (atm)<br><!-- End of picture text -->



<!-- Start of picture text -->
+ T = 800°C sweep<br>— P(premeate) = 0.2 atm<br>100% —_ ~ > P(retentate) = 120 atm Cumulative H, Recovery oo<br>ox, 1! i itt tt i tt dE rt Tt TT bee<br>vox 1! | | it | | | | dt dt dT cL eee<br>moo }|ti ttt | tt | | peer tT fT tT<br>cox {+ _ ||} i | | | | beeper] | tt tt<br>sox ||] | | | | eee TT Tt tt<br>wx | | | | eet TE tT tT TE TE ET<br>wx | | | Leet TT | | tt | ET |<br>ee Os scaOO<br>pa a ck eeee<br>woet_| i | | | Td | dT dT dT | | tT tT ET TT<br>o So So So o So So So o So<br>Normalized distance from the left edge of the reactor (feed inlet)<br>-<br>| feed | se T = 800 °C<br>- = P(retentate)= 120 atm H, Recovery byEach ><br>—P(permeate)= 0.2 atm Membrane Segment nm<br>0.8% =<br>Le Tee ee<br>ox boast| | | | | | TE | P| Pg<br>ox |teers| | | | | Et<br>eRe: eee<br>owt ttt tt i tt ttt | seer<br>oxi ttt ttt ttt tt tt yt | | eRe<br>oxi tt ttt tt? ett? tet tt ty fy<br>ox tit tt tt? Ett ye tet yy ty<br>o o o oO o o oO oO oS o<br>Normalized distance from the left edge of the reactor (feed inlet)<br><!-- End of picture text -->



<!-- Start of picture text -->
feed | - T = 800 °C sweep<br>——P(permeate)= 0.2 atm<br>30% Cc ~- piretentate) = 20 atm H, Mole Fraction (Retentate) oo<br>Se eee=G<br>= COPS<br>> COTSee<br>CEC ee<br>: STE PE EET TT TP PSssered<br>wi tl tt ET EE<br>-F 6€é se asta Bas eReBnassorkseseegset<br>6 Fe 6 PF OF OP KF PK OP KF OP Sb FP 6 OF Ss<br>Normalized distance from the left edge of the reactor (feed inlet)<br><!-- End of picture text -->



<!-- Start of picture text -->
T= 800°C sweep<br>40% Cc ———P(permeate) — P(retentate)  =0.2= 120 atm atm ‘12 Mole Fraction.  (Permeate) oq<br>se} ot | | | | |} Pt tt tt tt<br>wx | | | |e | | | | | EE EP |<br>ee ee<br>oe} {i [tt | pei ttt tt tt |<br>vo |} | | tT | tT PS sheet tp Py<br>mt tt ttt Et ty | RSE LT<br>wx tii |} tt tt | tt See<br>we tit tEtT tT | Ey | et yt yy Ss<br>- 6 grasa eas eezBnreesesibirseseegeet<br>6 Fe 6 FP oF OP KF OP KF OPK OP KF OP 6b OP 6 8 Ss<br>Normalized distance from the left edge of the reactor (feed inlet)<br><!-- End of picture text -->

**_Preprints.org_ (www.preprints.org)  |  NOT PEER-REVIEWED  |  Posted: 4 April 2025** 

**<u>doi:10.20944/preprints202504.0349.v1</u>** 

34 of 38 

A discrete plug-flow reactor model was established for simulating the one-dimensional isothermal permeation of hydrogen through palladium membranes, and were applied for separating hydrogen from a pressurized hot syngas stream. The model assumes a shell-and-tube cross-section for estimating the exact membranes area. A set of inlet conditions for the feed syngas and an inlet sweep nitrogen were made. Also, a target hydrogen recovery of 95% and a target hydrogen mole fraction of 40% at the permeate exit were enforced. The required membrane length was computed to achieve these targets. The model consists of 200 segments, with each segment having the length of about 2 cm. After a validity test, it was found that this spatial segmentation is adequate. 

Then, the impact of three operational variables was investigated, when varied individually starting from reference values such that better hydrogen permeation can be obtained. These design variable are the temperature, retentate-side pressure, and permeate-side pressure. For quantitative evaluation of the permeation improvement, five assessment metrics were discussed, including the apparent global permeance and the efficiency factor. Linear or nonlinear regression models were provided for the membrane length, the average permeation mass flux, and the log mean pressuresquare-root difference. In addition, the one-dimensional profiles of some permeation-related quantities (such as the segmental hydrogen recovery) at the extreme value of each design variable were contrasted. The present study can serve as a rough guide for palladium-based hydrogen separation, showing designers potential gains in hydrogen permeation by manipulating some operational conditions. The designers may then seek optimum compromise between the expected gain and the incurred complications or implementation cost. For example, it was shown that increasing the reactor temperature or the retentate pressure results in proportional gain in the mass flux, while decreasing the permeate pressure has an exponential correlation with that mass flux. 

Considering the relative changes in the three investigated design variables and the dependent hydrogen permeation metrics in 21 simulations (one reference simulation and 20 additional ones), the temperature is the most effective for improving the permeation performance. The retentate pressure comes in the second place. The permeate pressure is the least-powerful way to improve hydrogen permeation. 

**Author Contributions:** O.A.M. (the sole author) contributed to the conceptual design, computational modelling, simulations, data analysis, visualization, and manuscript writing. 

**Funding:** This research received no funding. 

**Data Availability Statement:** No dataset was used. The results reflect own calculations as described in the modeling procedure and mentioned input parameters. 

**Acknowledgments:** <mark>The author deeply appreciates the valuable support and shared data by former colleagues E. David Huckaby, Michael V. Ciocco, Bryan D. Morreale (National Energy Technology Laboratory of the United States Department of Energy – NETL/DoE), and Michael Matuszewski (University of Pittsburgh, U.S.A).</mark> 

**Conflict of Interest:** The author declares that the research was conducted in the absence of any commercial or financial relationships that could be construed as a potential conflict of interest. 

###### **References** 

1. Couto, N., Rouboa, A., Silva, V., Monteiro, E., Bouziane, K. (2013). Influence of the biomass gasification processes on the final composition of syngas. Energy Procedia 36, 596–606. <u>https://doi.org/10.1016/j.egypro.2013.07.068</u> 

2. Sarafraz, M.M., Safaei, M.R., Jafarian, M., Goodarzi, M., Arjomandi, M. (2019). High Quality Syngas Production with Supercritical Biomass Gasification Integrated with a Water–Gas Shift Reactor. Energies. 12:2591. https://doi.org/10.3390/en12132591 

3. NETL [National Energy Technology Laboratory of the United States Department of Energy]. (no date). Reactions & Transformations. <u>https://netl.doe.gov/research/coal/energysystems/gasification/gasifipedia/reaction-transformations [Accessed May 5, 2022].</u> 

**_Preprints.org_ (www.preprints.org)  |  NOT PEER-REVIEWED  |  Posted: 4 April 2025** 

**<u>doi:10.20944/preprints202504.0349.v1</u>** 

35 of 38 

4. Poudel, J., Choi, J.H., Oh, S.C. (2019). Process Design Characteristics of Syngas (CO/H2) Separation Using Composite Membrane. Sustainability 11:703. https://doi.org/10.3390/su11030703 

5. Kumar, R.N., and Aarthi, V. (2020). From Biomass to Syngas, Fuels and Chemicals – A Review. AIP Conference Proceedings 2225:070007. https://doi.org/10.1063/5.0005864 

6. Talmadge, M., Biddy, M., Dutta, A., Jones, S., Meyer, A. (2013). Syngas Upgrading to Hydrocarbon Fuels Technology Pathway [Technical Report by the National Renewable Energy Laboratory “NREL” and the Pacific Northwest National Laboratory “PNNL” of the United States Department of Energy]. Available at: <u>https://www.nrel.gov/docs/fy13osti/58052.pdf</u> 

7. Matar, S., Mirbach, M.J., Tayim, H.A. (1989). Production and Uses of Synthesis Gas. In: Catalysis in Petrochemical Processes. Springer, Dordrecht. https://doi.org/10.1007/978-94-009-1177-2_6 

8. Fortunato, B., Camporeale, S.M., Torresi, M. (2013). A Gas-Steam Combined Cycle Powered by Syngas Derived from Biomass. Procedia Comput. Sci. 19, 736–745. https://doi.org/10.1016/j.procs.2013.06.097 

9. Stork. (2022). Syngas Fired Steam Boiler. https://www.stork.com/en/client-cases/syngas-fired-steam-boiler [Accessed May 6, 2022]. 

10. Marco, R., and Carlo, P. (2015). "9. Use of bio-sourced syngas," in Biorefineries: An Introduction, ed. M. Aresta, A. Dibenedetto, F. Dumeignil (Berlin, München, Boston: De Gruyter), 219–234. <u>https://doi.org/10.1515/9783110331585-013</u> 

11. Ni, Y., Wang, K., Zhu, W., Liu, Z. (2021). Realizing high conversion of syngas to gasoline-range liquid hydrocarbons on a dual-bed-mode catalyst. Chem Catal. 1(2), 383–392. <u>https://doi.org/10.1016/j.checat.2021.02.003</u> 

12. Felseghi, R.-A., Carcadea, E., Raboaca, M.S., TRUFIN, C.N., Filote, C. (2019). Hydrogen Fuel Cell Technology for the Sustainable Future of Stationary Applications. Energies 12:4593. <u>https://doi.org/10.3390/en12234593</u> 

13. Ghiat, I., and Al-Ansari, T. (2021). A review of carbon capture and utilisation as a CO2 abatement opportunity within the EWF nexus. J. CO2 Util. 45:101432. https://doi.org/10.1016/j.jcou.2020.101432 

14. Madejski, P., Chmiel, K., Subramanian, N., Kuś, T. (2022). Methods and Techniques for CO2 Capture: Review of Potential Solutions and Applications in Modern Energy Technologies. Energies 15:887. <u>https://doi.org/10.3390/en15030887</u> 

15. Dinca, C., Slavu, N., Cormoş, C.-C., Badea, A. (2018). CO2 capture from syngas generated by a biomass gasification power plant with chemical absorption process. Energy 149, 925–936. <u>https://doi.org/10.1016/j.energy.2018.02.109</u> 

16. Adu, E., Zhang, Y., Liu, D. (2019). Current situation of carbon dioxide capture, storage, and enhanced oil recovery in the oil and gas industry. Can. J. Chem. Eng. 97(5), 1048–1076. https://doi.org/10.1002/cjce.23393 

17. OFECM [Office of Fossil Energy and Carbon Management at the United States Department of Energy]. (no date). Pre-Combustion Carbon Capture Research. <u>https://www.energy.gov/fecm/scienceinnovation/carbon-capture-and-storage-research/carbon-capture-rd/pre-combustion-carbon</u> [Accessed May 6, 2022]. 

18. Iulianelli, A., Ribeirinha, P., Basile, A. (2014). Methanol steam reforming for hydrogen generation via conventional and membrane reactors: A review. Renew. Sust. Energ. Rev. 29, 355–368. <u>https://doi.org/10.1016/j.rser.2013.08.032</u> 

19. Piemonte, V., Di Paola, L., De Falco, M., Iulianelli, A., Basile, A. (2014). "11 - Hydrogen production using inorganic membrane reactors," in Advances in Hydrogen Production, Storage and Distribution, ed. A. Basile and A. Iulianelli (Woodhead Publishing), 283–316. https://doi.org/10.1533/9780857097736.3.283 

20. Peters, T., and Caravella, A. (2019). Pd-Based Membranes: Overview and Perspectives. Membranes 9(2):25. <u>https://doi.org/10.3390/membranes9020025</u> 

21. Vermaak, L., Neomagus, H.W.J.P., Bessarabov, D.G. (2021). Hydrogen Separation and Purification from Various Gas Mixtures by Means of Electrochemical Membrane Technology in the Temperature Range 100– 160 °C. Membranes 11:282. https://doi.org/10.3390/membranes11040282 

22. Alique, D., Martinez-Diaz, D., Sanz, R., Calles, J.A. (2018). Review of Supported Pd-Based Membranes Preparation by Electroless Plating for Ultra-Pure Hydrogen Production. Membranes 8:5. <u>https://doi.org/10.3390/membranes8010005</u> 

**_Preprints.org_ (www.preprints.org)  |  NOT PEER-REVIEWED  |  Posted: 4 April 2025** 

**<u>doi:10.20944/preprints202504.0349.v1</u>** 

36 of 38 

23. Oh, D.-K., Lee, K.-Y., Park, J.-S. (2020). Hydrogen Purification from Compact Palladium Membrane Module Using a Low Temperature Diffusion Bonding Technology. Membranes 10(11):338. <u>https://doi.org/10.3390/membranes10110338</u> 

24. Krishnan, G., Steele, D., O'Brien, K., Callahan, R., Berchtold, K., Figueroa, J. (2009). Simulation of a Process to Capture CO2 From IGCC Syngas Using a High Temperature PBI Membrane. Energy Procedia 1(1), 4079– 4088. https://doi.org/10.1016/j.egypro.2009.02.215 

25. Berstad, D., Nekså, P., Gjøvåg, G.A. (2011). Low-temperature syngas separation and CO2 capture for enhanced efficiency of IGCC power plants. Energy Procedia 4, 1260–1267. <u>https://doi.org/10.1016/j.egypro.2011.01.182</u> 

26. GE Power Systems. (no date). GE IGCC Technology and Experience with Advanced Gas Turbines [Online - - 

resource]. Available at: <u>https://www.ge.com/content/dam/gepower new/global/en_US/downloads/gas new-site/resources/reference/ger-4207-ge-igcc-technology-experience-advanced-gas-turbines.pdf</u> (Accessed May 6, 2022). 

27. Wang, T. (2017). "1 - An overview of IGCC systems," in Integrated Gasification Combined Cycle (IGCC) Technologies, ed. T. Wang and G. Stiegel (Woodhead Publishing), 1-80. https://doi.org/10.1016/B978-0-08- <u>100167-7.00001-9</u> 

28. Mitsubishi Heavy Industries, Ltd. Energy Systems. (no date). IGCC Integrated coal Gasification Combined Cycle Power Plants [Catalogue document]. Available at: <u>https://power.mhi.com/catalogue/pdf/igcc.pdf</u> (Accessed May 6, 2022). 

29. Barbieri, G. (2015). "Sweep Gas in a Membrane Reactor," in: Encyclopedia of Membranes, ed. E. Drioli (Berlin, Heidelberg: Springer). https://doi.org/10.1007/978-3-642-40872-4_768-1 

30. Li, Z., Polfus, J.M., Xing, W., Denonville, C., Fontaine, M.-L., Bredesen, R. (2019). Factors Limiting the Apparent Hydrogen Flux in Asymmetric Tubular Cercer Membranes Based on La27W3.5Mo1.5O55.5−δ and La0.87Sr0.13CrO3−δ. Membranes 9:126. https://doi.org/10.3390/membranes9100126 

31. Chein, R.Y., Chen, Y.C., Chung, J.N. (2015). Sweep gas flow effect on membrane reactor performance for hydrogen production from high-temperature water-gas shift reaction. J. Membr. Sci. 475, 193-203. <u>https://doi.org/10.1016/j.memsci.2014.09.046</u> 

32. Balachandran, U., Dorris, S.E., Emerson, J.E., Lee, T.H., Lu, Y., Park, C.Y., Picciolo, J.J. (2011). Hydrogen Separation Membranes [Annual Report by the Argonne National Laboratory “ANL” of the United States Department of Energy for FY 2010]. Available at: https://publications.anl.gov/anlpubs/2011/03/69523.pdf 

33. Chiesa, P., Romano, M.C., Kreutz, T.G. (2013). "10 - Use of membranes in systems for electric energy and hydrogen production from fossil fuels," in Handbook of Membrane Reactors, Reactor Types and Industrial Applications, ed. A. Basile (Woodhead Publishing), 416–455. https://doi.org/10.1533/9780857097347.2.416 

34. Brunetti, A., Caravella, A., Drioli, E., Barbieri, G. (2017). "CHAPTER 1: Membrane Reactors for Hydrogen Production," in Membrane Engineering for the Treatment of Gases: Volume 2: Gas-separation Issues Combined with Membrane Reactors: Edition 2, ed. E. Drioli, G. Barbieri, A. Brunetti (The Royal Society of Chemistry), 1–29. https://doi.org/10.1039/9781788010443-00001 

35. GTI [Gas Technology Institute] (2007). Direct Hydrogen Production from Biomass Gasifier Using Hydrogen-Selective Membrane [Final Report, prepared for Xcel Energy]. Available at: - - 

<u>https://www.xcelenergy.com/staticfiles/xe/Corporate/RDF DirectHydrogenProduction Report%5B1%5D.pdf</u> 

36. Kinouchi, K., Katoh, M., Horikawa, T., Yoshikawa, T., Wada, M. (2012). Hydrogen Permeability of Palladium Membrane for Steam-reforming of Bio-Ethanol Using the Membrane Reactor. Int. J. Mod. Phys. Conf. Ser. 6, 7–12. https://doi.org/10.1142/S2010194512002851 

37. Thermex. (2022). Why counter flow heat exchangers are more efficient. <u>http://www.thermex.co.uk/news/blog/605-why-counter-flow-heat-exchangers-are-more-efficient</u> [Accessed May 7, 2022]. 

38. Enerquip. (2022). What’s the difference between parallel flow, counter flow and crossflow heat exchangers? <u>https://www.enerquip.com/whats-the-difference-between-parallel-flow-counter-flow-and-crossflow-heatexchangers [Accessed May 7, 2022].</u> 

**_Preprints.org_ (www.preprints.org)  |  NOT PEER-REVIEWED  |  Posted: 4 April 2025** 

**<u>doi:10.20944/preprints202504.0349.v1</u>** 

37 of 38 

39. NIST [National Institute of Standards and Technology]. (2021a). NIST Chemistry WebBook - Hydrogen. <u>https://webbook.nist.gov/cgi/cbook.cgi?Name=h2&Units=SI [Accessed May 7, 2022].</u> 

40. NIST [National Institute of Standards and Technology]. (2021b). NIST Chemistry WebBook - Carbon monoxide. https://webbook.nist.gov/cgi/cbook.cgi?Name=CO&Units=SI [Accessed May 7, 2022]. 

41. NIST [National Institute of Standards and Technology]. (2021c). NIST Chemistry WebBook - Carbon dioxide. https://webbook.nist.gov/cgi/cbook.cgi?ID=C124389&Units=SI [Accessed May 7, 2022]. 

42. Kuo, K.K. (2005). Principles of Combustion, 2nd ed. New Jersey, USA: John Wiley & Sons. 

43. Poinsot, T., and Veynante, D. (2005). Theoretical and Numerical Combustion, 2nd ed. USA: R.T. Edwards, Inc. 

44. IUPAC [International Union of Pure and Applied Chemistry]. (1997). Compendium of Chemical Terminology, 2nd ed. (the "Gold Book"). Compiled by A.D. McNaught and A. Wilkinson. Oxford: Blackwell Scientific Publications. Online version (2019-) made by S.J. Chalk. <u>https://doi.org/10.1351/goldbook.</u> 

45. NIST [National Institute of Standards and Technology]. (2018). CODATA [Committee on Data for Science and Technology] Value: molar gas constant. <u>https://physics.nist.gov/cgi-bin/cuu/Value?r|search_for=gas</u> [Accessed May 7, 2022]. 

46. NIST [National Institute of Standards and Technology]. (2021d). NIST Chemistry WebBook - Nitrogen. <u>https://webbook.nist.gov/cgi/cbook.cgi?Name=n2&Units=SI [Accessed May 7, 2022].</u> 

47. Tuckerman, M.E. (2020). Lecture 25: Plug flow reactors and comparison to continuously stirred tank reactors. <u>https://chem.libretexts.org/Courses/New_York_University/CHEMUA_652%3A_Thermodynamics_and_Kinetics/Lecture_25%3A_Plug_flow_reactors_and_comparison_to_ continuously_stirred_tank_reactors [Accessed May 9, 2022].</u> 

48. AIChE [American Institute of Chemical Engineers] (no date). Plug Flow Reactor (PFR). <u>https://www.aiche.org/ccps/resources/glossary/process-safety-glossary/plug-flow-reactor-pfr</u> [Accessed May 9, 2022]. 

49. Campo, M., Tanaka, A., Mendes, A., Sousa, J.M. (2011). "3 - Characterization of membranes for energy and environmental applications," in Advanced Membrane Science and Technology for Sustainable Energy and Environmental Applications, ed. A. Basile and S.P. Nunes (Woodhead Publishing), 56–89. <u>https://doi.org/10.1533/9780857093790.1.56</u> 

50. Alraeesi, A., and Gardner, T. (2021). Assessment of Sieverts Law Assumptions and ‘n’ Values in Palladium Membranes: Experimental and Theoretical Analyses. Membranes 11:778. <u>https://doi.org/10.3390/membranes11100778</u> 

51. Koffler, S.A., Hudson, J.B., Ansell, G.S. (1969). Hydrogen permeation through alpha-palladium, Trans. Metall. Soc. AIME 245, 1735–1740. 

52. Morreale, B.D., Ciocco, M.V., Enick, R.M., Morsi, B.I., Howard, B.H., Cugini, A.V., Rothenberger, K.S. (2003). The permeability of hydrogen in bulk palladium at elevated temperatures and pressures. J. Membr. Sci 212(1-2), 87–97. https://doi.org/10.1016/S0376-7388(02)00456-8 

53. Marzouk, O.A. (2017). Performance Analysis of Shell-and-Tube Dehydrogenation Module. Int. J. Energy Res. 41(4), 604–610, http://doi.org/10.1002/er.3637 

54. Yuan, M., Lee, K., Van Campen, D.G., Liguori, S., Toney, M.F., Wilcox, J. (2019). Hydrogen Purification in Palladium-Based Membranes: An Operando X-ray Diffraction Study. Ind. Eng. Chem. Res. 58(2), 926–934. <u>https://doi.org/10.1021/acs.iecr.8b05017</u> 

55. Nordio, M., Wassie, S.A., Annaland, M.V.S., Tanaka, D.A.P., Sole, J.L.V., Gallucci, F. (2021). Technoeconomic evaluation on a hybrid technology for low hydrogen concentration separation and purification from natural gas grid. Int. J. Hydrog. Energy 46(45), 23417–23435. https://doi.org/10.3390/pr6030020 

56. Microsoft corporation. (2022). Use Goal Seek to find the result you want by adjusting an input value. <u>https://support.microsoft.com/en-us/office/use-goal-seek-to-find-the-result-you-want-by-adjusting-aninput-value-320cb99e-f4a4-417f-b1c3-4f369d6e66c7 [Accessed May 11, 2022].</u> 

57. Bandyopadhyay, S. (2021). All forms of energy are equal, but some forms of energy are more equal than others. Clean Techn. Environ. Policy 23, 2775–2776. https://doi.org/10.1007/s10098-021-02228-3 

**_Preprints.org_ (www.preprints.org)  |  NOT PEER-REVIEWED  |  Posted: 4 April 2025** 

**<u>doi:10.20944/preprints202504.0349.v1</u>** 

38 of 38 

58. Tan, E.C.D., Talmadge, M., Dutta, A., Hensley, J., Schaidle, J., Biddy, M., Humbird, D., Snowden-Swan, L.J., Ross, J., Sexton, D., Yap, R., Lukas, J. (2015). Process Design and Economics for the Conversion of Lignocellulosic Biomass to Hydrocarbons via Indirect Liquefaction Thermochemical Research Pathway to High-Octane Gasoline Blendstock Through Methanol/Dimethyl Ether Intermediates [Technical Report prepared for the United States Department of Energy - Bioenergy Technologies Office]. Available at: <u>https://www.nrel.gov/docs/fy15osti/62402.pdf</u> 

59. Leonzio, G. (2018). Methanol Synthesis: Optimal Solution for a Better Efficiency of the Process. Processes 6:20. https://doi.org/10.3390/pr6030020 

60. Vita, A., and Italiano, C. (2020). "Chapter 4 - Fuel and hydrogen related problems for conventional steam reforming of natural gas," in Current Trends and Future Developments in (Bio-) Membranes: Membranes - 

in Environmental Applications, ed. A. Figoli, Y. Li, A. Basile (Elsevier), 71–89. https://doi.org/10.1016/B978 <u>0-12-816778-6.00004-7</u> 

61. Utamura, M., Nikitin, K., Kato, Y. (2008). A generalised mean temperature difference method for thermal design of heat exchangers. Int. J. Nucl. Energy Sci. Technol. 4(1), 11–31. <u>https://doi.org/10.1504/IJNEST.2008.017545</u> 

62. Lienhard IV, J.H., and Lienhard V, J.H. (2019). A Heat Transfer Textbook, 5th ed. Cambridge, Massachusetts, USA. 

63. Heumann, C., Schomaker, M., Shalabh (2016). Introduction to Statistics and Data Analysis With Exercises, Solutions and Applications in R, Switzerland: Springer. 

**Disclaimer/Publisher’s Note:** The statements, opinions and data contained in all publications are solely those of the individual author(s) and contributor(s) and not of MDPI and/or the editor(s). MDPI and/or the editor(s) disclaim responsibility for any injury to people or property resulting from any ideas, methods, instructions or products referred to in the content. 

