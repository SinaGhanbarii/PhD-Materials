

# **_processes_** 



_Project Report_ 

## **Process Intensification in Fuel Cell CHP Systems, the ReforCELL Project** 

**José Luis Viviente**<sup>**1,**</sup> ***, Sylvie Escribano**<sup>**2**</sup> **, Giampaolo Manzolini**<sup>**3**</sup> **, Marit Stange**<sup>**4**</sup> **, Carlo Tregambe**<sup>**5**</sup> **, Leonardo Roses**<sup>**6**</sup> **, Arjan J. J. Koekkoek**<sup>**7**</sup> **, Cécile Guignard**<sup>**8**</sup> **, Arnaud Dauriat**<sup>**8**</sup> **and Fausto Gallucci**<sup>**9**</sup> 

- 1 Funación Tecnalia Research and Innovation, Mikeletegi Pasealekua 2, 20009 Donostia—San Sebastian, Spain 

- 2 CEA/LITEN, 17 rue des Martyrs, 38054 Grenoble CEDEX 9, France; sylvie.escribano@cea.fr 

- 3 Politecnico di Milano, Deparment of Energy, via Lambruschini 4, 20156 Milano, Italy; giampaolo.manzolini@polimi.it 

- 4 SINTEF, P.O. Box 124 Blindern, N-0314 Oslo, Norway; marit.stange@sintef.no 

- 5 ICI caldaie S.P.A., Via G.Pascoli 38, Zevio, 37059 Verona, Italy; carlo.tregambe@icicaldaie.com 

- 6 HyGear B.V., P.O. Box 5280, 6802 EG Arnhem, The Netherlands; leonardo.roses@hygear.nl 

- 7 Hybrid Catalysis B.V., P.O. Box 513, 5600 MB Eindhoven, The Netherlands; a.j.j.koekkoek@tue.nl 

- 8 Quantis Sàrl, EPFL Innovation Park, Bât. D, 1015 Lausanne, Switzerland; cecile.guignard@quantis-intl.com (C.G.); arnaud.dauriat@quantis-intl.com (A.D.) 

- 9 Chemical Process Intensification, Department of Chemical Engineering and Chemistry, Eindhoven University of Technology, P.O. Box 513, 5612 AZ Eindhoven, The Netherlands; f.gallucci@tue.nl 

- Correspondence: joseluis.viviente@tecnalia.com; Tel.: +34-610-767-840 

#### Academic Editor: Michael Henson 

Received: 29 July 2016; Accepted: 1 October 2016; Published: 17 October 2016 

**Abstract:** This paper reports the findings of a FP7/FCH JU project (ReforCELL) that developed materials (catalysts and membranes) and an advance autothermal membrane reformer for a micro Combined Heat and Power (CHP) system of 5 kWel based on a polymer electrolyte membrane fuel cell (PEMFC). In this project, an active, stable and selective catalyst was developed for the reactions of interest and its production was scaled up to kg scale (TRL5 (TRL: Technology Readiness Level)). Simultaneously, new membranes for gas separation were developed. In particular, dense supported thin palladium-based membranes were developed for hydrogen separation from reactive mixtures. These membranes were successfully scaled up to TRL4 and used in lab-scale reactors for fluidized bed steam methane reforming (SMR) and autothermal reforming (ATR) and in a prototype reactor for ATR. Suitable sealing techniques able to integrate the different membranes in lab-scale and prototype reactors were also developed. The project also addressed the design and optimization of the subcomponents (BoP) for the integration of the membrane reformer to the fuel cell system. 

**Keywords:** palladium membrane; fluidized membrane reactor; hydrogen production; micro-CHP system; PEM fuel cell; ATR; SMR 

### **1. Introduction** 

Major concerns on anthropogenic CO2 emissions and related greenhouse effect have pushed several governments to support greenhouse gas emission reduction policies. The EU, for example, set a very high target for reduction of greenhouse gas emissions by 40% compared to 1990 levels within 2030 (at least 80% by 2050), together with an increase by 27% of energy efficiency and renewable share in the energy consumption [1]. Stationary fuel cells offer a clean and efficient source of electricity in systems ranging from 1 kW up to 1 MW or more [2]. With an appropriate fuel processing technology, fuel cells are able to tap into established or accessible sources of fuels such as natural gas but also various other fuels including biofuels and bio-gases. Combined heat and power (CHP), 

_Processes_ **2016** , _4_ , 37; doi:10.3390/pr4040037 

www.mdpi.com/journal/processes 

2 of 34 

_Processes_ **2016** , _4_ , 37 

which consists of simultaneous production and use of heat and power, is certainly one of the cheapest options to increase energy efficiency with consequent primary energy savings and CO2 emission reduction [2–6]. In a distributed generation scenario, fuel cells systems lead to particularly high efficiencies (electrical efficiency up to 60%, first law efficiency in cogeneration of more than 90%), thereby attaining considerable primary energy saving whilst avoiding transmission losses. When using natural gas (thereby building on existing infrastructure), stationary fuel cells can substantially reduce CO2 emissions as a highly efficient conversion of low-carbon natural gas replaces the central supply from a still predominantly fossil-fuels based electricity mix. Depending on the fuel used and its fuel, the technology can potentially eliminate CO2 and other emissions altogether [2]. 

In addition, the better fuel exploitation of the CHP systems compared to conventional generation systems (i.e., power plants and boilers) allows economic savings which can cover the additional investment costs. Among CHP systems, micro-cogeneration systems (cogeneration unit with a maximum capacity below 50 kWe; (2004/8/EC)) are a very interesting option because of the significant share of the overall primary energy consumptions (about 30%) of residential applications [7,8]. Moreover, with its flexible modulation capabilities and high efficiencies at partial loads, the technology shows strong potential for grid balancing in the context of a power mix with more intermittent renewables and electric heating solutions like heat pumps [2,9]. 

In this work, an overview of the main results of the ReforCELL project is presented. The aim of the ReforCELL project was to develop a highly efficient polymer electrolyte membrane (PEM) fuel cell micro Combined Heat and Power cogeneration system (net energy efficiency >42% and overall efficiency >90%) based on a novel, more efficient and cheaper hydrogen reformer production unit together with the new design of the subcomponent for the BoP. This new high efficiency PEM fuel cell m-CHP system is based on the design, construction and testing of an advanced membrane reactor for pure hydrogen production (5 Nm<sup>3</sup> /h) from reforming. In addition, the design and optimization of the subcomponents (BoP) for the integration of the membrane reformer to the fuel cell system were also addressed. 

The main idea of ReforCELL was to apply the concept of process intensification [10] in the production of hydrogen feeding the Fuel Cell. The technology of membrane reactors was developed in the last decades and it has demonstrated a high degree of process intensification where the combination of a membrane based separation and a catalytic chemical reaction in one unit take place [11–18]. In equilibrium limited reaction systems, such as in fuel reforming or dehydrogenations, the selective separation of a product of the reaction (i.e., H2), implies a displacement of the thermodynamic equilibrium towards the products, thus achieving higher fuel conversions and direct product separation (a separation unit downstream is not required) [19]. 

The traditional reformers include several steps for producing H2 with adequate quality to feed the fuel cell stack (Figure 1) [8,20–25]. Two commercial technologies based on a steam-methane reforming reactor (Figure 1) and on an autothermal reformer (ATR) were modelled to assess the performance of reference technologies. The main indexes of the two reference cases are summarized in Table 1. Results are consistent with available information of commercial systems based on this technology [26–29]. 

**Table 1.** Performances of reference case. 

|**Result**|**SMR**|**ATR**|
|---|---|---|
|Net electric effciency (%LHV)|34.2%|32.3%|
|Net thermal effciency (%LHV)|46.3%|50.5%|
|Overall effciency (%LHV)|80.5%|82.8%|
|Second law effciency (%Ex)|37.59%|36.21%|
|Fuel Cell single cell voltage (V)|0.740|0.728|











<!-- Start of picture text -->
6<br>NGrai<br>a CMPre<br>57<br>' NGern<br><> SMR uv<br>16<br>19 => 18 Aitor<br>Burner<br>34 HX-8<br>na (Recov)<br>(sH)4 4—_|9 (ES)HT-WGS 10 8 . =°<br>2 P-2<br>HX-2 41 _—_ ve *<br>(SG) e—) ©) NI Y<br>3 21 LT-WGS La, FI q Exhaust<br>(Ee) > BLi127 cated =<br>5 Aitprox 26 xX Aiteatn Cota,<br>G = (W) Ssep-1<br>AX-7 25<br>PROX 14 WY)NN HX-6 Water<br>—_<br>P-4<br><!-- End of picture text -->



<!-- Start of picture text -->
—<br><<br>« |<br>| A zi D o-&<br>Bs CA VA:<br>By<br>(Vyena(a) =<br>i © W —s5<br>|_|<br>—<br>| Y<br><!-- End of picture text -->



4 of 34 

_Processes_ **2016** , _4_ , 37 

The ReforCELL work plan consisted on activities related to the whole product chain: i.e., development of materials/components (catalysts, membranes, supports, sealings, etc.) through integration/validation at lab-scale, until development/validation of pilot scale Autothermal membrane reformer (ATR-MR) and the proof of concept/validation of the new PEM fuel cell m-CHP system. Additionally, assessment of environmental, health and safety issues—in relation to the new intensified chemical processes and m-CHP—was also carried out thanks to a screening life cycle analysis considering all components and steps involved to build the system. 

For a maximum impact on the European industry, this research was carried out covering the complete value chain of micro-CHP fuel cell systems. It gathered together a multidisciplinary and complementary team having the right expertise, including top level European Research Institutes and Universities (6 RES) working together with representative top industries (4 SME and 1 IND) in different sectors (from materials to micro-CHP systems developers). 

The ReforCELL Project was funded under the FP7 for the Fuel Cell and Hydrogen Joint Undertaking. The Project started the 1st of February 2012 and it has run for 47 months. In the following, the main results in terms of catalysts, membranes and membrane reactors are highlighted. 

### **2. Experimental Section** 

### _2.1. Catalyst_ 

The high reaction temperatures associated with Autothermal Reforming (ATR) requires the use of catalysts with extreme thermal stability and high catalytic activity. These requirements put strenuous demands on the catalyst material in their agglomeration and vaporization resistance and structural/morphological stability. The carbon formation and deactivation by sulphur are also key challenges for ATR catalysts. For clean gas the main risk in reforming reactions is the formation of carbon. This has to be avoided since the formation of carbon may rapidly reduce the activity of the catalyst [31,32]. 

At present, the state-of-the-art ATR catalysts consist of the following materials: Ni catalysts on thermally stable supports, group VIII noble metals (Pt, Ru, and Rh) supported onto various high surface area oxide substrates, catalysts with a perovskite structure ABO3 [33–36], carbides of group VI metals [37,38], (noble) metal substituted pyrochlores A2B2O7 [39,40], and alumina supported catalysts containing nickel and uranium oxides (developed at BIC), with high activity and stability and a decrease in coke formation [41–43]. Commercial catalysts for both authotermal reforming (ATR) and steam methane reforming (SMR) are based on nickel with differences on the support. 

The integration of the membrane reactor in the reforming system for hydrogen separation will allow a higher hydrogen yield at much lower temperatures than in the benchmark ATR and SMR technologies. However, the feasibility of such integration requires the development of innovative ATR catalysts with improved catalytic activity and high resistance to carbon formation. Catalyst poisoning by sulphur was not addressed because a desulphurisation unit was considered on the feed line. The deactivation of the catalyst by carbon formation is a structure sensitive reaction. Specifically, the deactivation mechanism is influenced by the cluster size of the active metal, where the larger metal clusters show a much stronger interaction with carbon than smaller, well-dispersed, metal particles [44,45]. Based on this fact, the control of the electronic structure and size of the active metal surfaces has been the strategy followed in the development of innovative ATR catalysts with improved catalytic activity and stability. The reforming catalyst developed was designed based on conventional supported catalysts. The optimal selection of the catalyst was performed by carrying out ATR and SMR studies varying the composition of the active phase (Ni, Ru, Rh, Pt), the support (α-Al2O3, γ-Al2O3, MgAlO2, SiO2, CeO2; CeO2-ZrO2), and the method of preparation (impregnation, co-precipitation, etc.). Of particular interest are the CeO2 and CeO2-ZrO2 based supports, as these are known to greatly improve catalytic performance due to support metal interaction and oxygen storage capabilities [46,47]. As a comparison with the new catalyst, several commercial catalysts were characterized as well. 

5 of 34 

_Processes_ **2016** , _4_ , 37 

The elemental analysis of the catalyst was done by ICP-OES technique. The loss of material from the samples was measured by gravimetry before and after a thermal treatment at 900<sup>_◦_</sup> C. The textural properties of the supported catalyst (i.e., pore size distribution, surface area) were determined by physisorption analysis (BET) in a Micromeritics ASAP 2020 instrument. X-ray Diffraction analysis (Bruker D8 Advance equipment) was used to determine the crystalline structure and crystalline sizes. Finally, transmission electron microscopy (TEM) analysis (FEI Tecnai F30) was used for a deeper study of the morphology, size, and distribution of the catalyst particles onto the supports as well as of the support. Both fresh and used samples were characterized. 

The optimization of the selected catalyst was done by catalytic screening in the ATR and SMR reaction of methane in a 8 mm i.d. quartz fixed-bed reactor. A feed composition of Ar:CH4:H2O:O2 equal to 80:5:15:0/75:5:15:5 in SMR and to 30:15:50:5 in ATR was used. The tests were carried out under atmospheric pressure and temperatures ranging from 500 to 600<sup>_◦_</sup> C and inlet gas flow rate to obtain a Gas Hourly Space Velocity (GHSV) of 15,000 h<sup>_−_1</sup> . Afterward, carbonaceous deposits on the catalyst were tested using Temperature Programmed Oxidation (TPO). In order to obtain the desired properties of the catalyst support, a deep characterization of fresh and used samples of all catalytic series prepared was performed. The main structural and surface characteristics of the catalysts that have a strong influence on the ATR/SMR catalytic activity and stability were identified. From catalytic screening tests, durability tests and characterization of ATR/SMR catalysts, the optimal composition and preparation method of catalyst was selected, which is based on Ru catalysts deposited on optimized Zr/Ce-oxide based support. 

The catalyst preparation was optimized for production on a kilogram scale using a 10 L batch reactor (Figure 3), and a 0.5 kg batch of the catalyst having a particle size of 125–250 µm was prepared. 



**Figure 3.** A 10 L double walled glass reactor used for support synthesis and loading of the ruthenium onto the support. 

### _2.2. Membranes_ 

Much effort has been put into the development of Pd-based membranes for selective H2 separation in the literature in order to overcome the barrier towards large-scale industrial applications [11,12]. In general, membrane stability over a long period of time with sufficient perm-selectivity is the key parameter which would make these membranes interesting for the industrial scale. The selection of the proper support where Pd-layers are deposited becomes important in order to achieve this goal. Asymmetric porous ceramic supports have good surface quality suitable for the preparation of very thin (<5 µm) Pd-based membranes. Surface roughness and the presence of large pores inhibit the deposition of thin palladium layers. Another important issue to be considered is the strong interaction between 





<!-- Start of picture text -->
es i a<br>oe |<br><!-- End of picture text -->



<!-- Start of picture text -->
eee<br>’ ZrO, 110 nm on AlL,O;<br>ay “~ ft iy<br>Fee aa. oo 3 e s e l<br><!-- End of picture text -->













<!-- Start of picture text -->
Retentate feed<br>ee_<br>DY - “ xa oh, oe<br>Sata eih Retentate<br>eyin |<br>permeate sweep<br><!-- End of picture text -->



<!-- Start of picture text -->
—$————$_—<br>yyy ‘<br>id<br>48<br>=)<br>mo —————_—_— th m<br>44 yy<br>_— 4 Ly - te } "<br>SF A ' al .<br>by<br>I + i 4 ba \ .<br><!-- End of picture text -->



<!-- Start of picture text -->
(te) Veer Exhaust<br>le (Fa) i * &, ‘<br>(Fc) | il) vac onanPHT<br>Nz —bx] i] | | |<br>cH @ TH |] © |<br>H; bad 6)Pad |RS Ee HXaa<br>fe Ee HS<br>Air =< © © i<br>© eit we TX<br>co —p<}—_ p<] | t<br>el” SekGMSsi5r<br>N; —o<J [>]<br>, re Legend __ simamiine<br>“aori (Fc)Z 6) (ce) (tc) T —FC-yrases GreenFlow Controler né<br>SI PA (te) (tc) FE—lAlow Indicator<br>Nz water! TE-TO- TemperatureTemperature ContrlierIndicator<br><!-- End of picture text -->



<!-- Start of picture text -->
hi : \ —— se<br>Inlet/ ; ok he 2 = “ge<br>outletconn. Ap , | 4s eo -<br>353 i ite | F ¥ 2<br>“Bild “ os yan Control = = -<br><!-- End of picture text -->



<!-- Start of picture text -->
10ppm — 50ppm.5%AB & pure H2<br>100 fr sf . me oat +f. i .<br>~ "| saneeeeeeensencenseesessneeeneeenseneeensenssenseespessesenesensensesnnesenssnasenesenasesens<br>ol" 240260280 300320 340360 380 400<br>Temps (h)<br>G5 I<br>‘| ppecccccccecececececetecetetetetctetetetstetetetceceaf fn ed an ee eeecceseceneceeeenecenesanecananenenazes<br>S 5.5 Wht tet | --—- Hb bape Pee de tLA tg fbb abd fb<br>=2 |<br>5B} a ae TW ean naan |<br>A ffeweeeeeneeeneceeeeneeeneeeneeneerneeent coeeenpeeneeeneeeeeee| Tension |<br>240 260 280 300 320 340 360 380 400<br>Temps (h)<br><!-- End of picture text -->



<!-- Start of picture text -->
ry Short stack test - i-V curves after load cycles<br>0,90 LS<br>0,80 _——<br>= 0,70 =~<br>& :<br>><br>0,60 Pure H2<br>50ppm+10ppm  0,5% AB :“\<br>0,50<br>70C- RH50%<br>P fuel/Air= 1,2/ 1,3 bar<br>0 01 0,2 03 04 05 06 07 08<br>i(A/em*)<br><!-- End of picture text -->



<!-- Start of picture text -->
350<br>® current<br>300<br>™ ppm CO max (Ucell<500mV)<br>o 20 BTC)<br>rt mP Air<br>= 200<br>a<br>&<br>o 150<br>2%<br>= 100<br>50<br>0<br>% Air Bleeding<br><!-- End of picture text -->



<!-- Start of picture text -->
he<br>a a<br>_— \Qbagea abve oes ieee ‘<br>- — 7<br>“MMinnningnifiltY ti aa <T~ .<br>bad :<br>/ =<br>aeLt<br><!-- End of picture text -->



<!-- Start of picture text -->
90 12<br>%° 10<br>7” ee 8<br>Pa<br>= a =<br>> 60 6 z<br>*a<br>x<br>50 4 4<br>Ax<br>40 A 5<br>/a -e-Stack Voltage (V)<br>= -x-Stack Power (kW)<br>30 x 0<br>) 50 100 150 200<br>1(A)<br><!-- End of picture text -->



<!-- Start of picture text -->
1<br>0.9<br>0.8<br>S 0.7<br>o<br>©><br>5 06<br>os -= 8-Cells stack<br>. -_ 85-Cells=f  stack<br>0.4<br>0 0.2 0.4 06 08 1<br>i (A/cm?)<br><!-- End of picture text -->



<!-- Start of picture text -->
200<br>—— commerical CeO, CeO, —— small scale (5 (5 g)<br>—— Ce,Zr,O, method method 1 180 —— large scale (0.25 kg)<br>—— Ce,Zr,O, method Ce,Zr,O, methodZr,O, method method 2 160<br>140<br>z55 120<br>°<br>3<br>Be5a.5a.a. 100 i\<br>2 80 |<br>=|<br>588 60<br>40<br>i i F 20<br>0<br>asasa 30 40 7 60 7 80 2 30 40 «50 60) 70 80s 9s«100s10—S—120<br>degrees 20 20 degrees 20 20<br><!-- End of picture text -->



<!-- Start of picture text -->
200<br>—— commerical CeO, CeO, —— small scale (5 (5 g)<br>—— Ce,Zr,O, method method 1 180 —— large scale (0.25 kg)<br>—— Ce,Zr,O, method Ce,Zr,O, methodZr,O, method method 2 160<br>140<br>z55 120<br>°<br>é 3<br>is) 100 \<br>Be5a.5a.a. i\<br>2 80 |<br>=|<br>588 60<br>40<br>i i F 20<br>0<br>asasa 30 40 7 60 7 80 2 30 40 «50 60) 70 80s 9s«100s10—S—120<br>degrees 20 20 degrees 20 20<br><!-- End of picture text -->



<!-- Start of picture text -->
1404 —*—Ce,,,Zr,,,0,<br>—s RUOCe Zr, ..0.<br>120 ars Mas<br>a<br>Po 100<br>g =eeeb<br>zy5Z3 806 eean ea.<br>Bol<br>S he<br>20<br>0<br>0.0 0.2 0.4 0.6 0.8 1.0<br>P/P.<br><!-- End of picture text -->



<!-- Start of picture text -->
250<br>— incipient wetnes impregnation<br>—— controlled precipitation<br>— surfactant assisted<br>200<br>150<br>n<br>aQ 100<br>50 '<br>0<br>20 30 40 50 60 70 80<br>degrees 20<br><!-- End of picture text -->



<!-- Start of picture text -->
SMR.600°C SMRS00°C:! TPO} SMRS00°C =} SMR SOO" =} f— ATRSOO'C<br>zat a 5F 9: oo ’-‘ ‘:<br>E400 a ‘Vy:<br>= 200 ‘ ‘ 4 Wi :<br>0:5+,:<br>‘: ‘ ‘i § maximum prociution ax<br>Z 4 1 based SMR catalyst<br>tel<br>a i<br>=:<br>024 48 72 96 120 144 168 192 216 240 264 288 312 336 360<br>time (h)<br><!-- End of picture text -->



<!-- Start of picture text -->
e “<br>\<br><!-- End of picture text -->



<!-- Start of picture text -->
ba)<br><!-- End of picture text -->



<!-- Start of picture text -->
‘3:iam,i<br>y.: su<br><!-- End of picture text -->



<!-- Start of picture text -->
1 18<br>= 0.8 NN a 42<br><!-- End of picture text -->



<!-- Start of picture text -->
2 o 06 y=“. ;—* 9 a€<br>5 ° Z<br><!-- End of picture text -->



<!-- Start of picture text -->
2 04 6 =<br>o ° =<br>é@ 02 3 z<br>=<br> 00<br>05 10 15 20 25 30<br><!-- End of picture text -->

17 of 34 

_Processes_ **2016** , _4_ , 37 

### 3.2.2. Fluidized Bed Membrane Reactor 

The procedure followed to validate the fluidized bed membrane reactor concept was similar to the line-time presented for the microchannel reactor. The catalyst and membrane stability were first investigated separately. Later on, both were integrated in the reactor and tested under steam reforming and autothermal reforming of methane in fluidized bed membrane reactors. Two different types of membranes were tested: Pd-based tubular ceramic supported membranes (Figure 4) and Pd-based tubular metallic supported membranes (Figure 5) both developed by direct simultaneous Pd and Ag electroless plating (ELP) deposition [51–54] in a one step process. 

Characterization of the Ru supported catalyst showed that the catalyst particles are mechanically stable in fluidized bed operation and no loss of particle size was observed even under high temperature operation in a bubbling fluidization regime. 

The stability and sealing of the ceramic supported Pd-based membranes were also investigated. The Pd-based tubular ceramic supported membranes were sealed using commercial standard Swagelok connectors (316 SS) together with graphite gaskets for 10 mm OD tubes provided by CHROMalytic TECH(nology) Pty Ltd (Boronia, Victoria 3155, Australia). The graphite gaskets were sized to the outer membrane diameter of 10.1–10.5 mm and pretreated with a membrane dummy to the standard Swagelok connector. Figure 19 shows a schematic of the sealing (a) and a picture of the sealed tubular Pd-alloy membrane with graphite gaskets to a standard Swagelok connector (b). The bottom part of the connector was specially designed for membranes that will be immersed vertically in the fluidized bed to avoid gas holdup below the membrane. In case of integration in packed bed reactors, simple Swagelok caps could be used. 





**Figure 19.** ( **a** ) Schematic of the graphite based sealing and ( **b** ) photograph of sealed tubular membrane. Reproduced with permission from [51] Copyright, 2015, Elsevier. 

The membranes were tested for single gas permeation, mixed gas permeation, and for steam reforming and autothermal reforming of methane in fluidized bed membrane reactors. The hydrogen flux through a sealed membrane at different hydrogen partial pressures and different temperatures between 380–600<sup>_◦_</sup> C, and after the stability tests were performed, is shown in Figure 20a. The hydrogen permeation rate increases with increasing transmembrane partial pressure difference and temperature, as expected. The tested membrane shows an almost perfect linear behaviour for the pressure exponential factor _n_ = 0.5 ( _R_<sup>2</sup> >0.995), which is typical for Pd-alloy membranes at low pressures, if bulk-diffusion through the membrane is the rate limiting step according to Sieverts’ law [77]. The membrane parameters for the tested membrane were determined at 10 kJ _·_ mol<sup>_−_1</sup> for the activation energy (∆Eact) and 6.93 _×_ 10<sup>_−_8</sup> mol _·_ m<sup>_−_2</sup> Pa<sup>_−_0.5</sup> _·_ s<sup>_−_1</sup> for the pre-exponential factor (P0) using the plot of the logarithm of the permeance against the reciprocal temperature (shown in Figure 20b). 



<!-- Start of picture text -->
-5.4<br><!-- End of picture text -->



<!-- Start of picture text -->
-5.4<br>—4<br>aS.A aa ad a a =<br>:J<br>H |g ™y7 ' .<br>k a 58<br>», | as a<br>WY Equation y=a+b*x<br>annnnenennnnephip finaneninnsnanenannnnsndeanannenene - 6.0 -||Adi: R-Square 0.97519 a<br>| : Value Standard<br>| aa Intercept -4.173 0.126<br>me) Slope -9994 795<br>6.2<br>0.00010 0.00012 0.00014 0.00016 0.00018 0.00020<br>1/RT [mol J]<br><!-- End of picture text -->



19 of 34 

_Processes_ **2016** , _4_ , 37 

conversion obtained during the experiments, especially in the second day, a significant increase was detected. Analysing the surface of the membranes and the sealing after these tests, it was observed that the sealing was damaged, which could be the reason for the CO increase in the permeate gas stream. The membrane surface was free of defects, which assures that the membranes can survive under reforming conditions for this test duration. 



<!-- Start of picture text -->
100<br>20<br>18<br>Reaction and separation<br>80<br>16 600 °C<br>CO in permeate = 160 to 200 ppm<br>14 Reaction and separation<br>550 °C  60<br>12 CO<br>CO in permeate = 120 ppm<br>CO2<br>10<br>CH4<br>8 H2 40<br>CH4 conversion (%)<br>6<br>4 20<br>2<br>0 0<br>0 50 100 150 200 250 300<br>Time (min)<br>Retentate composition (vol%) CH4 conversion (%)<br><!-- End of picture text -->

**Figure 22.** Steam methane reforming (SMR) in a FBMR with five tubular ceramic supported membranes at 550 and 600<sup>_◦_</sup> C. Feed: S/C of 3 and a N/C of 8.4 with a total flow rate of 10.3 NL/min to ensure fluidization. Reproduced with permission from [51] Copyright, 2015, Elsevier. 

**Table 3.** Summary of SMR in the FBMR with tubular Pd–Ag/ZrO2 membranes at 1.3 bar at several temperatures. Reproduced with permission from [51] Copyright, 2015, Elsevier. 

|**Day of Membrane Tests**|**Da**|**y 1**|**Da**|**y 2**|
|---|---|---|---|---|
|System pressure (bar)|1.3|1.3|1.3|1.3|
|System temperature (<sup>_◦_</sup>C)|500|550|550|600|
|<br>CH4 eq. conversion (%)|55.7|73.0|73.0|88.1|
|_u_/_umf_ (-)|1.3|1.3|1.3|1.3|
|Volumetric fow rate in reactor (L/min)|20.9|22.3|22.3|24|
|CH4 conversion (%)|55.5|73.1|76.4|89.3|
|Exhaust H2/CO ratio (-)|22.6|16.1|15.8|11|
|CO selectivity (-)|0.12|0.16|0.18|0.25|
|H2 selectivity (-)|3.85|3.79|3.83|3.74|
|H2 recovery factor (HRF) (-)|0.17|0.22|0.2|0.23|
|H2 separation factor (HSF) (-)|0.31|0.31|0.28|0.28|
|Hydrogen permeate impurity (ppm CO)|50|70|120|200|
|Hydrogen permeate fow (NmL/min)|550|740|700|800|



I ~~n a second test, ATR of methane was performed on these membranes. The retentate~~ stream composition and methane conversion are shown in Figure 23. The feed conditions were different to the test performed with the REB membranes, so the results obtained in terms of conversion of methane cannot be directly ascribed to the different membranes, while the hydrogen recovery and separation can. 

20 of 34 

_Processes_ **2016** , _4_ , 37 



<!-- Start of picture text -->
100<br>20<br>18<br>Reaction and separation 80<br>16 600 °C<br>CO in permeate = >800 ppm<br>14<br> CO 60<br>12  CO2<br> CH4<br>10<br> H2<br>8  CH4 conversion (%) 40<br>6<br>4 20<br>2<br>0 0<br>0 50 100 150 200 250 300<br>Time (min)<br>Retentate composition (vol%) CH4 conversion (%)<br><!-- End of picture text -->

**Figure 23.** Autothermal reforming of methane (ATR) in a FBMR with five membranes at 600<sup>_◦_</sup> C. Feed: S/C of 3, O/C of 0.25 and an N/C of 8.2. Total feed flow rate 10.3 NmL/min. Reproduced with permission from [51] Copyright, 2015, Elsevier. 

Comparing the results obtained for ATR reforming without and with the TECNALIA membranes, which are shown in Table 4, the methane conversion increased by 7.2% from 89.5% to 96.7%. The total amount of produced hydrogen increased by 7.7% resulting in a total flow rate of hydrogen of <u>2.71 L/min. The hydrogen recovery and the purity of the hydrogen stream are still comparable.</u> Detailed information on the preparation, characterization, and stability tests of thin-film Pd–Ag ceramic supported membranes for high-temperature fluidized bed membrane reactor applications can be found in Fernandez et al. [51]. 

**Table 4.** Comparison of ATR without membranes, with REB membranes and with tubular ceramic supported membranes. Reproduced with permission from [51] Copyright, 2015, Elsevier. 

||**Without Membranes**|**REB Membranes**|**TECNALIA Membranes**|
|---|---|---|---|
|CH4 eq. conversion (%)|93.2|91|93.2|
|_u_/_umf_ (-)|1.5|1.5|1.5|
|CH4 conversion(%)|89.5|92.9|96.7|
|Exhaust H2/CO ratio (-)|12.3|7.3|10.4|
|CO selectivity (-)|0.31|0.29|0.22|
|H2 selectivity (-)|3.59|2.77|3.41|
|H2 recovery (-)|-|0.2|0.35|
|H2 separation factor (-)|-|0.24|0.31|
|H2 permeate impurities (ppm)|-|<1.5|>500|
|H2 permeate fow (NmL/min)|-|845|870|



The ATR was also performed with Pd/Ag on metallic supports. First, the membrane stability was assessed between 500–600<sup>_◦_</sup> C for around 800 h (Figure 24). The main aim of this test was to check the stability of the hydrogen permeance and the nitrogen leakage through the membrane as a function of time on stream. It can be concluded that the membrane shows a really good stability for hydrogen permeation during the whole test (~1.3 _×_ 10<sup>_−_6</sup> mol _·_ m<sup>_−_2</sup> _·_ s<sup>_−_1</sup> _·_ Pa<sup>_−_1</sup> ). However, at a certain temperature the hydrogen permeance slightly decreased over time, as also reported in the literature before for this type of membranes. The nitrogen leakage through the metallic supported membrane was extremely low and even below the detection limit of the Bronkhorst flow meter (0.01 mL/min) for almost 800 h, which resulted in an ideal H2/N2 perm-selectivity higher than 200,000. 

21 of 34 

_Processes_ **2016** , _4_ , 37 



<!-- Start of picture text -->
2.8E-06 350000<br>500 °C 525 °C 550 °C 575 °C 600 °C<br>2.4E-06 300000<br>2.0E-06 250000<br>1.6E-06 200000<br>1.2E-06 150000<br>8.0E-07 100000<br>4.0E-07 50000<br>S<br>H2/N2 = 2650<br>0.0E+00 0<br>0 100 200 300 400 500 600 700 800<br>Time (h)<br>/Pa)<br>2 2<br>/N<br>2<br> (mol/s/m<br>2<br>Ideal  selectivity H<br>Permeance H<br><!-- End of picture text -->

**Figure 24.** H2 permeance (open circles) and H2/N2 ideal permselectivity (closed circles) of the metallic supported membrane as a function of time on stream at 500–600<sup>_◦_</sup> C. Reproduced with permission from [53] Copyright, 2015, Elsevier. 

The test was carried out at different temperatures with a stepwise increase of 25<sup>_◦_</sup> C. However, once at 600<sup>_◦_</sup> C and after 795 h of permeation tests, the nitrogen permeated through the membrane resulting in a pronounced decrease in the ideal perm-selectivity which quickly dropped to a value of 2650. Nevertheless, this value of ideal perm-selectivity is still relatively high when compared to other state-of-the-art metallic supported membranes. A table with the comparison of different Pd-based membranes investigated in the literature can be found in Fernandez et al. [51,52]. 

Catalyst interaction with the Pd–Ag layer was not observed since H2 permeance is the same for single gas tests with empty tube configuration and fluidized bed configuration. This also implies the absence of mass transfer resistances caused by the particles. (Close to) thermodynamic equilibrium is achieved both in ATR and SMR membrane-assisted processes. However, a full conversion of CH4 is never achieved. This can be partially explained by the large amount of inert gas fed together with the CH4:H2O. This dramatically decreases the partial pressure of the other components. After all the experiments a decrease in ideal H2/N2 selectivity was n observed due to the defects created in the surface. As determined through a test with the membrane submerged in ethanol, all defects are associated with micropores in the surface, which were also observed with SEM images. 

The methane conversion as a function of different experimental conditions for the two different reactor configurations studied in this work is shown in Figure 25. 

As can be observed, chemical equilibrium is obtained in the fluidized bed reactor configuration due to the good performance of the catalyst, assuring absence of kinetic limitations. Furthermore, for all cases an important increase in the yield of the reaction for H2 production as a consequence of the displacement of the equilibrium is observed when the membrane reactor configuration is employed. It is especially interesting to highlight that the equilibrium displacement is more pronounced for conditions where the driving force for H2 permeation is maximized, such as an increase in the pressure of the reactor and the steam-to-carbon ratio, or a decrease in the total flow rate with the corresponding increase in residence time. Under the new scenario with configuration of the FBMR, the expected thermodynamic equilibrium was also calculated with Aspen Plus. As observed from Figure 25, again thermodynamic equilibrium is almost achieved in this new configuration. The difference observed might relate to the small amount of catalyst in the freeboard, which may not be enough to achieve the expected equilibrium. For all the cases studied in this work, a maximum error in the carbon balance of around 5%–8% is obtained as a consequence of experimental errors mainly related to the analyser 

22 of 34 

_Processes_ **2016** , _4_ , 37 

calibration. Detailed information on the characterization and stability tests of thin-film Pd–Ag metallic supported membranes for high-temperature fluidized bed membrane reactor applications can be found in Medrano et al. [53]. 



<!-- Start of picture text -->
80% 80%<br>70% ( a )  70% ( b )<br>60% 60%<br>50% 50%<br>40% 40%<br>30% 30%<br>20% Thermodynamic equilibrium FBR 20% Thermodynamic equilibrium FBR<br>Thermodynamic equilibrium FBMR Thermodynamic equilibrium FBMR<br>10% FBR 10% FBR<br>FBMR FBMR<br>0% 0%<br>450 500 550 600 650 0 1 2 3 4 5 6 7<br>Temperature (°C) Pressure (bar)<br>80% 80%<br>70% ( c )  70% ( d )<br>60% 60%<br>50% 50%<br>40% 40%<br>30% 30%<br>20% Thermodynamic equilibrium FBR 20% Thermodynamic equilibrium FBR<br>Thermodynamic equilibrium FBMR Thermodynamic equilibrium FBMR<br>10% FBR 10% FBR<br>FBMR FBMR<br>0% 0%<br>0 1 2 3 4 5 6 2 3 4 5 6 7<br>Steam to Carbon ratio Total inlet flow (L/min)<br>CH conversion4 CH conversion4<br> conversion  conversion<br>4 4<br>CH CH<br><!-- End of picture text -->

**Figure 25.** Methane conversion as a function of ( **a** ) temperature; ( **b** ) pressure; ( **c** ) steam-to-carbon ration and ( **d** ) inlet flow rate for the two reactor configurations studied with reference case conditions and the thermodynamic equilibrium for steam methane reforming calculated in Aspen Plus v7.3.2. Reproduced with permission from [53] Copyright, 2015, Elsevier. 

### _3.3. ATR Prototype_ 

The membrane reactor was tested for different operating conditions with ranging pressure, temperature and S/C ratio. Difficulties were found in fragility of the ceramic supports of the membranes which failed early in the testing phase. An improved protocol for handling, assembling and testing the membranes was defined for further developments to reduce this risk. The remaining tests were performed at lower flows and without extraction of hydrogen. During the testing, the ATR reactor reached a stable production of 1.7 Nm<sup>3</sup> of H2 per Nm<sup>3</sup> of CH4 feed. Flow patterns, heat transfer limits, and integration possibilities of the reactor were identified. During testing, the performance was checked in the SCADA panel view. Several parameters (e.g., pressures, temperatures, flow rate, valve position, etc.), were also monitored by the graphical control panel. 

A model was developed based on the results to simulate the fluidized bed membrane reactor. The model was used for calculation of membrane area and to analyse the influence of some variables such as reactor temperature, heat loss and operating load. The model also evaluates the required NG, air and steam flow rates to achieve the H2 production target, operating at autothermal condition. 

Another model of the complete fuel processor including peripheral components of the balance of plant was also developed to describe the ATR-MR system performance. The system includes the ATR membrane reactor and the auxiliary units to recover the heat source from permeate and retentate streams. The model analyses the influence of some variables such as reactor temperature, heat loss and operating load, allowing an optimization procedure (CAPEX minimization) of the heat exchanging network. The results of the ATR-MR system model provide a sort of map of the required operating 

23 of 34 

_Processes_ **2016** , _4_ , 37 

condition as a function of the H2 production target. By decreasing the hydrogen output, the O/C ratio increases, and the requirements for feed of steam relative to the Natural Gas feed (S/C) decreases. 

### _3.4. Integration and Validation in m-CHP System_ 

The technical objective of this activity was the definition of the optimal lay-out for the micro-CHP system when integrating the membrane reactor and the assessment of its performance. Firstly, the indexes adopted for comparing the different configurations were defined. They are the net electric efficiency, net thermal efficiency, and overall efficiency which are defined in the EU directive for cogeneration (2004/8/EC)). 



where 

. _m f uel·LHVf uel_ Thermal input power _PNet_ . _AC_ Net power output _Q_ . _cog_ Net thermal power output 

In addition to these, the second law analysis of the micro-CHP system is carried out to assess the overall energy losses in the conversion process. In the second law analysis, the net thermal power output is weighed by means of the efficiency of an ideal process converting the heat into work as expressed below. 



The ideal efficiency is evaluated with reference to the Lorentz cycle, because the heat produced by the micro-CHP system is available at variable temperature rather than at constant temperature. The second law efficiency is calculated as follows: 



Starting from the measured performance of the fuel stack prototype (see Section 2.5) and the membrane reactor characteristics (see Section 3.3) measured in the project, the m-CHP system layout was optimised for integrating the membrane reactor and the PEM FC stack. The optimization took into account both efficiency and cost aspects: in particular, the membrane surface area was monitored in the optimization being the component with the largest variation. 

Two different membrane reactors lay-outs were investigated: the main difference being the adoption of a sweep flow at the permeate side to reduce the membrane surface area instead of a vacuum pump. For both cases, several design parameters of the membrane reactor (i.e., temperature, S/C ratio, feed, and permeate pressures) as well as other components (i.e., fuel cell current density, burner temperature, etc.) were considered. 

The net electric efficiency as a function of the membrane surface area and diverse reactor configuration and operating conditions is plotted in Figure 26. In general, the higher the membrane 



<!-- Start of picture text -->
—e-—600°C —e— 575°C =m 550°C<br>40.6%<br>7 bar<br>& bar & bar<br>8 bar<br>i; 40.2% G/c2.5) r<br>x 8 bar<br>a 7 bar<br>c Tbar ee<br>@ 39.8% = ==<br>= . 7 Bar<br>£ 12 bar Fae<br>wu aw oe<br>=] x * a<br>5 39.4% 4.2 “S/C3.0°)<br>oe . bar gf ? i oe<br>x] 14 bar nd ae<br>rrr] # fw 12 bar<br>” ¥)<br>a af<br>2 bar @’<br>39.0% i<br>#12 bar<br>t<br>*<br>/<br>f<br>®<br>38.6%<br>0.00 0.20 0.40 0.60 0.80 1.00<br>Membrane Area (m7)<br><!-- End of picture text -->

25 of 34 

_Processes_ **2016** , _4_ , 37 

**Table 5.** Performances of ReforCELL cases. Reproduced with permission from [26] Copyright, 2015, Elsevier. 

|**~~Results~~**|**~~Units~~**|**~~Sweep~~**|**~~Case~~**|**~~Vacuum~~**|**~~Pump~~**|
|---|---|---|---|---|---|
|S/C|-|2.5|3|2.5|3|
|Pressure reaction side|bar|8|8|8|8|
|Pressure permeate side|bar|1.2|1.2|0.3|0.3|
|NG power input (LHV base)|kW|12.50|12.71|13.22|13.05|
|NG power input (HHV base)|kW|13.84|14.08|14.64|14.46|
|Net AC power output|kW|5.00|5.00|5.00|5.00|
|Fuel Cell AC power output|kW|6.31|6.32|6.64|6.63|
|NG compressor|kW|0.15|0.15|0.16|0.15|
|Air compressor|kW|0.35|0.35|0.37|0.37|
|Cathode air blower|kW|0.18|0.19|0.20|0.19|
|Vacuum pump|kW|-|-|0.27|0.27|
|Balance of plant|kW|0.64|0.62|0.65|0.65|
|Thermal recovery|kW|6.49|6.72|6.93|6.77|
|Net electric effciency (LHV base)|%LHV|40.02|39.35|37.85|38.32|
|Net electric effciency (HHV base)|%HHV|36.13|35.52|34.16|34.59|
|Net thermal effciency|%LHV|51.97|52.87|52.45|51.86|
|Overall effciency (LHV base)|%LHV|91.99|92.22|90.30|90.18|
|Overall effciency (HHV base)|%HHV|83.05|83.26|81.52|81.41|
|Second law effciency (Exergy base)|%Ex|43.77|43.22|41.74|42.13|
|Total membrane area|m<sup>2</sup>|0.29|0.24|0.21|0.19|





<!-- Start of picture text -->
 BioGas LF  BioGas AD  NG<br>39.0%<br>Base case  8 bar<br>9 bar<br>38.0% @ T 600 °C S/C 3.0 10 bar<br>12 bar<br>37.0%<br>36.0% 10 bar<br>12 bar<br>14 bar<br>35.0%<br>14 bar 12 bar<br>34.0%<br>0.00 0.05 0.10 0.15 0.20 0.25 0.30<br>Mem. Area (m 2 )<br>Net El. Eff. (%)<br><!-- End of picture text -->

**Figure 27.** Efficiency vs. Membrane area for three different natural gasses assuming the ReforCELL concept. 

An important result concerns the flexibility of the system with respect to the fuel composition. The membrane reactor can handle and separate pure hydrogen even from diluted methane as in biogas. Biogas requires higher membrane reactor pressures and membrane surface areas because of the methane dilution, which reduces the hydrogen partial pressure and consequently the permeation driving force. In the case of the vacuum pump the efficiency penalty is between 3% and 4%, while it reduces to 1% for the sweep case. The net electrical efficiency with the same reactor design of NG case ranges from 34% to 39%. Energy penalties in the flexible conversion system dealing with different natural gas also occur in commercial systems (i.e., the internal combustion reciprocating engine). 

26 of 34 

_Processes_ **2016** , _4_ , 37 

Based on the optimized system layout fed with NG, BoP components were investigated. The selection and design of components and of the full system were carried out taking into account the compatibility of the main magnitudes (pressure, temperature etc.) and materials in the system, as well as costs. To manage the CHP system, a PLC is used. It is composed of two identical controllers (IOBLOCK): one communicates with the fuel processor PLC, and the other is used to measure each single cell voltage. Interface components (mechanical and electrical interface) and the system control strategy were also defined. However, the final integration and test of the system was not finalized due to liquidation of the company in charge of testing near the end of the project. 

On the other side, system size scale up was also assessed, investigating the three main components of the CHP system (ATR, fuel cell stack, balance of plant); technical feasibility and economical aspects were taken into account. The maximum size considered is 50 kWe according to European Directive 2012/27/EU on energy efficiency. 

Once technical feasibility for sizes up to 50 kWe was verified, the final specific cost (€/kW) of the whole system was evaluated. The best size should be a system suited to supply 50 kWe. The specific cost decrease (€/kW) of the whole system liken to size increase is around 78%. 

Furthermore the flexibility of the CHP system scaled-up was evaluated, confirming the feasibility of partial load operations (as the system developed within the project) ensuring load decrease until 40%. 

Finally, the aspect of which size is more marketable across Europe was assessed: it is preferable to have small size systems (10–20 kWe) for the smallest buildings with a few dwellings, ensuring bigger sizes (30–50 kWe) with a modular approach. 

### _3.5. Life Cycle Assessment and Safety Analysis_ 

The polymer electrolyte membrane fuel cell (PEMFC) micro combined heat and power (m-CHP) system investigated in the ReforCELL project was assessed by means of a life cycle assessment (LCA), a method standardized by the International Organisation for Standardization (ISO) 14040-44 standards [78,79]. The general objective was to perform a LCA which evaluates the environmental burdens of conventional PEMFC m-CHP systems (both steam methane reforming (SMR) and autothermal reforming (ATR)) over their whole life cycle (“cradle to grave”) and to compare them with the developed ReforCELL technology system. The type of use considered is the production of heat and electricity for several dwellings. To have also an idea of the position of the PEMFC m-CHP systems in comparison with other technologies, their impact was also compared with the impact of a natural gas conventional CHP, an alternative where electricity and heat come from the average mix (European electricity mix and country average heat mix) and a last one where electricity and heat come from a green available technology (called “GAT”, wind power and solar thermal). Finally, there were six systems compared in the detailed LCA: 

- Fuel cell micro-CHP conventional system with steam methane reforming (SMR) 

- Fuel cell micro-CHP conventional system with autothermal reforming (ATR) 

- Fuel cell micro-CHP ReforCELL developed technology: autothermal reforming with membrane reformer (ATR MR) 

- Natural gas fuelled CHP system (50 kWe) 

- System without CHP conventional (using electricity from the grid and an average heat mix) 

- System without CHP green available technology (using wind power and solar thermal) 

The LCA was performed using the ecoinvent v2.2 life cycle inventory database [80] and the life cycle impact assessment method IMPACT 2002+ [81,82]. The indicators assessed are climate change, resources consumption, impact on human health and on ecosystem quality and water withdrawal. The systems studied include the CHP production, its maintenance and its end-of-life treatment, the natural gas input, the direct emissions during use, the auxiliary boiler (including its production, end-of-life and use, i.e., natural gas production and combustion), the purchased heat (for the systems without CHP) and purchased electricity as described in Figure 28. 



<!-- Start of picture text -->
| Natural gas extraction and refining .<br>Micro-CHP production Micro-CHP<br>al ce Shar use Micro-CHP<br>Fuel cell Stack Balance- ;<br>production production Bolan {operation and end-of-life<br>DFR a maintenance)<br>Fuel processor production q<br>production /<br>Additional heat and electricity from the grid | '<br><!-- End of picture text -->



<!-- Start of picture text -->
100%<br>80% — — —<br>‘CHP production<br>60% © Natural gas input<br>® Direct emissions<br>| Maintenance<br>40% = CHP end-of-life<br>© Auxiliary boiler<br>= Purchased heat<br>20% @ Purchased electricity<br>* Net impacts<br>0% [4 ceca > > co cao > coe ca > x ec ca > coc a ><br>se S583 S2shtF FESR FESERE FRESE EF — refocus<br>xf Eg 2 ¢ ef EF g2 & ef g2 e ef EF g2 82 =f Ege<br>am C2es22 $e 3582 & 9 gee Sos 58s e353<br>peees ogee ze og vz zB pee ze pvzges<br>geg222 $s 5222 838222 §$SR222 FS5222<br>c c e c c<br>-40% aoe & 3 eof & 8 eof && eof Sk aon S88<br>S bs S S =<br>a ig & = 2<br>Climate change | Resources Ecosystem quality Water withdrawal Human health<br><!-- End of picture text -->

28 of 34 

_Processes_ **2016** , _4_ , 37 

Among PEMFC m-CHP systems, the ReforCELL developed technology has slightly lower impacts than the others for climate change and resources consumption while they all have similar impacts for the other indicators considered (slight differences are visible but due to the uncertainty on these indicators, they cannot be considered as different). The large natural gas CHP has a lower impact than the m-CHPs systems assessed but it is not destined to provide a small-scale local supply as the PEMFC m-CHP systems are. These results were obtained for the Italian market, for scenarios where excess electricity can be injected on the grid but not sold and with a dimensioning for 14 dwellings. The exercise has been done for the German market, leading to similar conclusions. Scenarios where the electricity could be sold at a good price (up to 70% of the purchasing price) were also assessed and they lead to a slight reduction of the impacts compared to the score presented above. A sensitivity analysis on the dimensioning would give different conclusions: if the CHP system is dimensioned to fulfil a higher fraction of the needs in heat and the surplus electricity is injected to the grid, the results become better. Indeed, injecting electricity to the grid enables conventional electricity production to be avoided and represents a benefit. Other sensitivity analyses were performed on the electricity mix choice, the electric efficiency of the ReforCELL system, the energy use for manufacturing, the treatment of the ReforCELL m-CHP at the end-of-life or the type of heat considered for the conventional supply but they do not show a big influence on the conclusions, or at least not for all indicators. Normalized and weighted results show the importance of climate change and resources indicators for systems such as those studied. 

Regarding safety analysis, HyGear identified and evaluated specific safety reactor/membrane parameters for the membrane reactor using tools such as HAZOP and heat and mass transfer transport reaction models, whereas ICI identified and evaluated the safety parameters on the complete system. 

### **4. Conclusions** 

The ReforCELL project aimed at the development of high efficient PEM fuel cell micro Combined Heat and Power cogeneration systems based on a novel hydrogen membrane reforming unit together with a new design of the subcomponent for the BoP. 

The approach for the development involved the whole product chain: development of active catalysts and membranes for H2 permeation were investigated. Stability over time and mechanical resistance were the two main characteristics aimed for in this project. Subsequently, the interaction between the catalyst and the membranes, and the performance of the reactor concept were proven at lab-scale when combining both at reactive conditions in two different layouts: micro-channel reactor and fluidized bed membrane reactor. Afterward, and following HAZOP procedures, the fluidized bed membrane reactor was scaled up to prototype scale. 

In parallel, modelling and testing activities enabled the investigation of the fuel cell system and operating conditions; a new PEM fuel cell stack was designed and a new configuration of the optimized m-CHP system was defined for the targeted application. Additionally, assessment of environmental, health and safety issues in relation to the new intensified chemical processes and m-CHP was carried out. 

The Ru based catalyst, supported on Ceria/Zirconia, showed good activity and long-term stability at lower temperature (500–600<sup>_◦_</sup> C) compared to the Ni based commercial catalyst in use at a high temperature (800<sup>_◦_</sup> C). Moreover the fluidization regime allowed the prevention of the formation of hot spots thus increasing its lifetime. 

Three different types of membranes were improved within the project: Pd-based tubular ceramic supported membranes, Pd-based tubular metallic supported membranes, and Pd-based micro-channel supported membranes. Stability of the membranes was confirmed through single gas permeation tests at operating temperatures over several days without any decrease in the membrane performance. Furthermore, new sealing methods for the tubular membranes were tested and proposed in order Permeances and selectivities obtained with the 

29 of 34 

_Processes_ **2016** , _4_ , 37 

different membranes are among the best ever reported in the literature and well above the targets for the ReforCELL project. 

Both reactor configurations (micro-channel reactor and fluidized bed membrane reactor were validated at lab-scale under SMR and/or ATR. However, the process should be performed at lower temperatures than expected (<550<sup>_◦_</sup> C) to improve long term stability of the membranes. Fluidized bed membrane reactor configuration was selected for the prototype reactor. Difficulties were found related to the fragility of the ceramic supports of the membranes which failed early in the testing phase. An improved protocol for handling, assembling and testing the membranes was defined for further developments to reduce this risk. 

A Fuel Cell stack prototype was manufactured and validated and an optimized m-CHP system layout defined. Based on the optimized system layout fed with NG, BoP components were investigated. The selection and design of components and of the full system was carried out taking into account the compatibility of main magnitudes (pressure, temperature, etc.) and materials in the system, as well as costs. However, the final integration and test was not finalized due to liquidation of the company in charge of the full system testing in the frame of the project. The simulations assessed that the net electric and overall efficiency of the Reforcell concept when using NG as fuel can be higher than 40% and 90% respectively. Biogas can also be adopted to feed the membrane reactor with penalties in terms of net electric efficiency due to the presence of CO2 and inerts in the biogas which dilutes the hydrogen. 

According to the results obtained in the ReforCELL project, the m-CHP system could not yet be considered at prototype level. Much effort is still required to improve the standard sealing methods and durability of the membranes at high temperature in a cost effective way. 

**Acknowledgments:** The research leading to these results has received funding from the European Union’s Seventh Framework Programme (FP7/2007–2013) for the Fuel Cells and Hydrogen Joint Technology Initiative under grant agreement n<sup>_◦_</sup> 278997 (ReforCELL project). 





**Disclaimer:** The present publication reflects only the author’s views and the FCH JU and the Union are not liable for any use that may be made of the information contained therein. 

**Author Contributions:** All authors contributed to writing and correcting the paper. José Luis Viviente was the Project Coordinator and contributed to the development of Pd-based membranes onto tubular supports, Sylvie Escribano contributed to all the steps concerning the fuel cell, Giampaolo Manzolini was the Dissemination Manager and contributed to the design and optimization of the m-CHP system, Marit Stange developed Pd-based membranes for the micro-channel reactor and validated this reactor at lab-scale, Carlo Tregambe contributed to the optimization of the m-CHP system, Leonardo Roses was the Exploitation Manager and designed, build and tested the membrane reactor prototype, Arjan J. J. Koekkoek developed the catalyst, Cécile Guignard and Arnaud Dauriat performed the Life Cycle Analysis and Fausto Gallucci was the Technical Manager and contributed to the membranes characterization as well as designing, building and validating the fluidized bed membrane reactor at lab-scale. 

### **Abbreviations** 

The following abbreviations are used in this manuscript: 

|ATEX|Appareils destinés à être utilisés en ATmosphères EXplosibles|
|---|---|
|ATR|Autothermal reformer|
|ATR-MR|Autothermal membrane reformer|
|BET|Brunauer–Emmett–Teller|
|BoP|Balance of plant|
|BIC|<br>Boreskov Institute of Catalysis|
|CAPEX|<br>Capital expenditure|
|CEM|Controlled evaporation and mixer|
|CHP|Combined heat and power|



30 of 34 

_Processes_ **2016** , _4_ , 37 

|CMP|Compressor|
|---|---|
|ELP|Electroless plating|
|FBR|<br>Fluidized bed reactor|
|FBMR|Fluidized bed membrane reactor|
|FC|Fuel cell|
|FP7|Seventh Framework Programme|
|GAT<br>|Green available technology<br>|
|GHSV|gas hourly space velocity|
|HAZOP|Hazard and operability study|
|HHV|<br>High heating value|
|HRF|H2 recovery factor|
|HSF|<br>H2 separation factor|
|HT-WGS|<br>High temperature water gas shift|
|HX|heat exchanger|
|ICP-OES|Inductively coupled plasma optical emission spectrometry|
|ID|Inside diameter|
|IMDBL|Inter-metallic diffusion barrier layer|
|kW|kilowatt|
|LCA|Life cycle assessment|
|LHV|<br>Low heating value|
|LT-WGS<br>|Low temperature water gas shift<br>|
|m-CHP|micro combined heat and power|
|MR|membrane reactor|
|N/C|Nitrogen-to-Carbon ratio|
|NG|<br>Natural gas|
|O/C|<br>Oxigen-to-carbon ratio|
|OD|<br>outside diameter|
|PEM|Polymer electrolyte membrane type<br>|
|PEMFC|Polymer electrolyte membrane fuel cell|
|PEM m-CHP|Polymer electrolyte membrane fuel cell micro combined heat and power|
|PFD|Process fow diagram|
|PLC|Programmable logic controller|
|PROX|<br>Preferential oxidizer|
|PSS|Porous stainless steel|
|SMR|steam methane reforming|
|S/C|<br>Steam-to-Carbon ratio|
|TEM|Transmission electron microscopy|
|TPO|Temperature programmed oxidation|
|TRL|<br>Technology Readiness Level|
|u|<br>fuidization velocity|
|umf|<br>minimum fuidization velocity|
|WGS|<br>Water gas shift|
|W/F ratio|<br>Weight to feed ratio|
|XPS|X-ray photoelectron spectroscopy<br>|
|XRD|X-ray diffraction|
|YSZ|<br>Yttria-stabilized zirconia|



### **References** 

1. European Commission. A Policy Framework for Climate and Energy in the Period from 2020 to 2030 (COM(2014) 15). Available online: https://ec.europa.eu/energy/en/topics/energy-strategy/2030-energystrategy (accessed on 31 March 2016). 

2. _Advancing Europe’s Energy System: Stationary Fuel Cell in Distributed Generation_ ; FCH JU, Luxemburg Publications Office of the European Union: Luxemburg City, Luxemburg, 2015. Available online: http://www.fch.europa.eu/studies (accessed on 31 March 2016). 

3. Alanne, K.; Saari, A. Sustainable small-scale CHP technologies for buildings: The basis for multi-perspective decision-making. _Renew. Sustain. Energy Rev._ **2004** , _8_ , 401–431. [CrossRef] 

4. Campanari, S.; Macchi, E.; Manzolini, G. Membrane reformer PEM cogeneration systems for residential applications—Part B: Techno-economic analysis and system layout. _Asia Pac. J. Chem. Eng._ **2009** , _4_ , 311–321. [CrossRef] 

5. Elmer, T.; Worall, M.; Wu, S.; Riffat, S.B. Fuel cell technology for domestic built environment applications: State of-the-art review. _Renew. Sustain. Energy Rev._ **2015** , _42_ , 913–931. [CrossRef] 

31 of 34 

_Processes_ **2016** , _4_ , 37 

6. Dodds, P.E.; Staffell, I.; Hawkes, A.D.; Li, F.; Grünewald, P.; McDowall, W. Hydrogen and fuel cell technologies for heating: A review. _Int. J. Hydrog. Energy_ **2015** , _40_ , 2065–2083. [CrossRef] 

7. International Energy Agency. Key World Energy Statistics, OECD/IEA. 2015. Available online: https://www.iea.org/publications/freepublications/publication/KeyWorld_Statistics_2015.pdf (accessed on 31 March 2016). 

8. Dorer, V.; Weber, R.; Weber, A. Performance assessment of fuel cell micro-cogeneration systems for residential buildings. _Energy Build._ **2005** , _37_ , 1132–1146. [CrossRef] 

9. International Energy Agency. Medium-Term Renewable Energy Market Report 2014: Market Analysis and Forecast to 2020, OECD/IEA. 2014. Available online: http://www.iea.org/publications/freepublications/ publication/medium-term-renewable-energy-market-report-2014.html (accessed on 31 March 2016). 

10. Reay, D.; Ramshaw, C.; Harvey, A. _Process Intensification_ ; Elsevier: Oxford, UK, 2008. 

11. Gallucci, F.; Fernandez, E.; Corengia, P.; van Sint Annaland, M. Recent advances on membranes and membrane reactors for hydrogen production. _Chem. Eng. Sci._ **2013** , _92_ , 40–66. [CrossRef] 

12. _Palladium Membrane Technology for Hydrogen Production, Carbon Capture and Other Applications_ , 1st ed.; Doukelis, A.; Panopoulos, K.; Koumanakos, A.; Kakaras, E., Eds.; Woodhead Publishing: Amsterdam, The Netherlands, 2015. 

13. Gallucci, F.; Comite, A.; Capannelli, G.; Basile, A. Steam Reforming of Methane in a Membrane Reactor: An Industrial Case Study. _Ind. Eng. Chem. Res._ **2006** , _45_ , 2994–3000. [CrossRef] 

14. Matsumura, Y.; Tong, J. Methane Steam Reforming in Hydrogen-permeable Membrane Reactor for Pure Hydrogen Production. _Top. Catal._ **2008** , _51_ , 123–132. [CrossRef] 

15. Yakabe, H.; Kurokawa, H.; Shirasaki, Y.; Yasuda, I. Operation of palladium membrane reformer system for hydrogen production: The case of Tokio Gas. In _Palladium Membrane Technology Hydrogen Production Carbon Capture Other Applications_ ; Woodhead Publishing: Amsterdam, The Netherlands, 2015; p. 311. 

16. Deshmukh, S.A.R.K.; Heinrich, S.; Mörl, L.; van Sint Annaland, M.; Kuipers, J.A.M. Membrane assisted fluidized bed reactors: Potentials and hurdles. _Chem. Eng. Sci._ **2007** , _62_ , 416–436. [CrossRef] 

17. Brunetti, A.; Drioli, E.; Barbieri, G. Energy and mass intensities in hydrogen upgrading by a membrane reactor. _Fuel Process. Technol._ **2014** , _118_ , 278–286. [CrossRef] 

18. Barbieri, G.; Brunetti, A.; Caravella, A.; Drioli, E. Pd-based membrane reactors for one-stage process of water gas shift. _RSC Adv._ **2011** , _1_ , 651–661. [CrossRef] 

19. Roses, L.; Gallucci, F.; Manzolini, G.; Campanari, S.; van Sint Annaland, M. Comparison between fixed bed and fluidized bed membrane reactor configurations for PEM based micro-cogeneration systems. _Chem. Eng. J._ **2011** , _171_ , 1415–1427. [CrossRef] 

20. Campanari, S.; Macchi, E.; Manzolini, G. Innovative membrane reformer for hydrogen production applied to PEM micro-cogeneration: Simulation model and thermodynamic analysis. _Int. J. Hydrog. Energy_ **2008** , _33_ , 1361–1373. [CrossRef] 

21. Mathiak, J.; Heinzel, A.; Roes, J.; Kalk, T.; Kraus, H.; Brandt, H. Coupling of a 2.5 kW steam reformer with a 1 kWel PEM fuel cell. _J. Power Sources_ **2004** , _131_ , 112–119. [CrossRef] 

22. Gandiglio, M.; Lanzini, A.; Santarelli, M.; Leone, P. Design and optimization of a proton exchange membrane fuel cell CHP system for residential use. _Energy Build._ **2014** , _69_ , 381–393. [CrossRef] 

23. Xie, D.; Wang, Z.; Jin, L.; Zhang, Y. Energy and exergy analysis of a fuel cell based micro combined heat and power cogeneration system. _Energy Build._ **2012** , _50_ , 266–272. [CrossRef] 

24. Gigliucci, G.; Petruzzi, L.; Cerelli, E.; Garzisi, A.; La Mendola, A. Demonstration of a residential CHP system based on PEM fuel cells. _J. Power Sources_ **2004** , _131_ , 62–68. [CrossRef] 

25. Seo, Y.T.; Seo, D.J.; Jeong, J.H.; Yoon, W.L. Development of compact fuel processor for 2 kW class residential PEMFCs. _J. Power Sources_ **2006** , _163_ , 119–124. [CrossRef] 

26. Di Marcoberardino, G.; Roses, L.; Manzolini, G. Technical assessment of a micro-cogeneration system based on polymer electrolyte membrane fuel cell and fluidized bed autothermal reformer. _Appl. Energy_ **2016** , _162_ , 231–244. [CrossRef] 

27. Nuvera. Avanti<sup>®</sup> Fuel Cell Power System. 2010. Available online: https://www.hydrogen.energy.gov/pdfs/ htac_may2012_nuvera.pdf (accessed on 12 September 2016). 

28. Nishizaki, K.; Tokyo Gas Co. The Japanese Experience in Micro CHP for Residential Use, Gas Industry Micro CHP Workshop, Macrogaz. 2008. Available online: http://www.marcogaz.org/index.php/workshops/ micro-chp-ws (accessed on 12 September 2016). 

32 of 34 

_Processes_ **2016** , _4_ , 37 

29. FuelCell Energy. Combined Heat & Power. Available online: http://www.fuelcellenergy.com/why-fuelcellenergy/benefits/combined-heat-power-chp/ (accessed on 12 September 2016). 

30. Campanari, S.; Macchi, E.; Manzolini, G. Membrane reformer PEM cogeneration systems for residential applications-Part A: full load and partial load simulation. _Asia Pac. J. Chem. Eng._ **2009** , _4_ , 301–310. [CrossRef] 

31. Aasberg-Petersen, K.; Dybkjær, I.; Ovesen, C.V.; Schjødt, N.C.; Sehested, J.; Thomsen, S.G. Natural gas to synthesis gas—Catalysts and catalytic processes. _J. Nat. Gas Sci. Eng._ **2011** , _3_ , 423–459. [CrossRef] 

32. Horn, R.; Schlögl, R. Methane Activation by Heterogeneous Catalysis. _Catal. Lett._ **2015** , _145_ , 23–39. [CrossRef] 

33. Erri, P.; Dinka, P.; Varma, A. Novel perovskite-based catalysts for autothermal JP-8 fuel reforming. _Chem. Eng. Sci._ **2006** , _61_ , 5328–5333. [CrossRef] 

34. Liu, D.; Krumpelt, M. Activity and Structure of Perovskites as Diesel-Reforming Catalysts for Solid Oxide Fuel Cell. _Int. J. Appl. Ceram. Technol._ **2005** , _2_ , 301–307. [CrossRef] 

35. Mawdsley, J.R.; Krause, T.R. Rare earth-first-row transition metal perovskites as catalysts for the autothermal reforming of hydrocarbon fuels to generate hydrogen. _Appl. Catal. A_ **2008** , _334_ , 311–320. [CrossRef] 

36. Devi, R.N.; Chilukuri, S.V.V. CeAlO3 Perovskites Containing Transition Metal Perovskites Containing Transition Metal for Hydrogen Production. US 20120264597 A1, 18 October 2012. 

37. Cheekatamarla, P.K.; Thomson, W.J. Hydrogen generation from 2,2,4-trimethyl pentane reforming over molybdenum carbide at low steam-to-carbon ratios. _J. Power Sources_ **2006** , _156_ , 520–524. [CrossRef] 

38. Ismagilov, Z.R.; Kuntsevich, S.V.; Kuznetsov, V.V.; Shikina, N.V.; Kerzhentsev, M.A.; Rogov, V.A.; Ushakov, V.A. Characterization of new catalysts based on uranium oxides. _Kinet. Catal._ **2007** , _48_ , 511–520. [CrossRef] 

39. Tada, M.; Zhang, S.H.; Malwadkar, S.; Ishiguro, N.; Soga, J.; Nagai, Y.; Tezuka, K.; Imoto, H.; Otsuka-Yao-Matsuo, S.; Ohkoshi, S.; et al. The active phase of nickel/ordered Ce2Zr2Ox catalysts with a discontinuity (x = 7–8) in methane steam reforming. _Angew. Chem._ **2012** , _124_ , 9495–9499. [CrossRef] 

40. Fang, X.; Zhang, X.; Guo, Y.; Chen, M.; Liu, W.; Xu, X.; Peng, H.; Gao, Z.; Wang, X.; Li, C. Highly active and stable Ni/Y2Zr2O7 catalysts for methane steam reforming: On the nature and effective preparation method of the pyrochlore support. _Int. J. Hydrog. Energy_ **2016** , _41_ , 11141–11153. [CrossRef] 

41. Ismagilov, Z.R.; Kuntsevich, S.V. Advanced uranium containing catalysts for methane reforming. In Proceedings of the NHA Annual Hydrogen Conference, San Antonio, TX, USA, 19–22 March 2007. 

42. Kuznetsov, V.V.; Ismagilov, Z.R.; Shikina, N.V.; Lazarchuk, V.V.; Balakhonov, V.G.; Matyuha, V.A.; Drobyaz, A.I.; Khlytin, A.L. New uranium oxide catalysts for hydrogen production by partial oxidation and reforming of methane. In Proceedings of the International Conference “CATALYSIS: FUNDAMENTALS AND APPLICATION”, Novosibirsk, Russia, 4–8 July 2007. 

43. Ismagilov, Z.R.; Kuntsevich, S.V.; Kuznetsov, V.V.; Shikina, N.V. Advanced uranium containing catalysts for methane reforming. In Proceedings of the International Symposium on Catalysis Engineering, Delft, The Netherlands, 14 June 2007; pp. 63–64. 

44. Barbier, J.; Corro, G.; Marecot, P.; Bournonville, J.P.; Frank, J.P. Structure sensitivity and coke formation on Pt/Al2O3 catalysts. _Reat. Kinet. Catal. Lett._ **1985** , _28_ , 245–250. [CrossRef] 

45. Barbier, J. Catalyst Deactivation 1987. In Proceedings of the 4th International Symposium, Antwerp, Belgium, 29 September–1 October 1987; Delmon, B., Froment, G.F., Eds.; Elsevier: Amsterdam, The Netherlands, 1987. 

46. Di Monte, R.; Kašpar, J. Nanostructured CeO2–ZrO2 mixed oxides. _J. Mater. Chem._ **2005** , _15_ , 633–648. [CrossRef] 

47. Guzman, J.; Carrettin, S.; Corma, A. Spectroscopic Evidence for the Supply of Reactive Oxygen during CO Oxidation Catalyzed by Gold Supported on Nanocrystalline CeO2. _J. Am. Chem. Soc._ **2005** , _127_ , 3286–3287. [CrossRef] [PubMed] 

48. Okazaki, J.; Ikeda, T.; Pacheco Tanaka, D.A.; Llosa Tanco, M.A.; Wakui, Y.; Sato, K.; Mizukami, F.; Suzuki, T.M. Strong Interaction at the Palladium/Alumina Interface of Membrane during Hydrogen Permeation at Elevated Temperature. _Chem. Lett._ **2008** , _37_ , 1004–1005. [CrossRef] 

49. Okazaki, J.; Ikeda, T.; Pacheco Tanaka, D.A.; Llosa Tanco, M.A.; Wakui, Y.; Sato, K.; Mizukami, F.; Suzuki, T.M. Importance of the support material in thin palladium composite membranes for steady hydrogen permeation at elevated temperatures. _Phys. Chem. Chem. Phys._ **2009** , _11_ , 8632–8638. [CrossRef] [PubMed] 

50. Okazaki, J.; Ikeda, T.; Pacheco Tanaka, D.A.; Sato, K.; Suzuki, T.M.; Mizukami, F. An investigation of thermal stability of thin palladium–silver alloy membranes for high temperature hydrogen separation. _J. Membr. Sci._ **2011** , _366_ , 212–219. [CrossRef] 

33 of 34 

_Processes_ **2016** , _4_ , 37 

51. Fernandez, E.; Coenen, K.; Helmi, A.; Melendez, J.; Zuñiga, J.; Tanaka, D.A.P.; van Sint Annaland, M.; Gallucci, F. Preparation and characterization of thin-film Pd–Ag supported membranes for high-temperature applications. _Int. J. Hydrog. Energy_ **2015** , _40_ , 13463–13478. [CrossRef] 

52. Fernandez, E.; Medrano, J.A.; Melendez, J.; Parco, M.; Viviente, J.L.; van Sint Annaland, M.; Gallucci, F.; Pacheco Tanaka, D.A. Preparation and characterization of metallic supported thin Pd–Ag membranes for hydrogen separation. _Chem. Eng. J._ **2016** , _305_ , 182–190. [CrossRef] 

53. Medrano, J.A.; Fernandez, E.; Melendez, J.; Parco, M.; Tanaka, D.A.P.; van Sint Annaland, M.; Gallucci, F. Pd-based metallic supported membranes: High-temperature stability and fluidized bed reactor testing. _Int. J. Hydrog. Energy_ **2016** , _41_ , 8706–8718. [CrossRef] 

54. Pacheco Tanaka, D.A.; Llosa Tanco, M.A.; Niwa, S.; Wakui, Y.; Mizukami, F.; Namba, T.; Suzuki, T.M. Preparation of palladium and silver alloy membrane on a porous α-alumina tube via simultaneous electroless plating. _J. Membr. Sci._ **2005** , _247_ , 21–27. [CrossRef] 

55. Bredesen, R.; Klette, H. Method of Manufacturing Thin Metal Membrane. U.S. Patent 6,086,729, 2000. 

56. Mejdell, A.L.; Peters, T.A.; Stange, M.; Venvik, H.J.; Bredesen, R. Performance and application of thin Pd-alloy hydrogen separation membranes in different configurations. _J. Taiwan Inst. Chem. Eng._ **2009** , _40_ , 253–259. [CrossRef] 

57. Peters, T.A.; Stange, M.; Sunding, M.F.; Bredesen, R. Stability investigation of micro-configured Pd–Ag membrane modules—Effect of operating temperature and pressure. _Int. J. Hydrog. Energy_ **2015** , _40_ , 3497–3505. [CrossRef] 

58. Peters, T.A.; Stange, M.; Bredesen, M. On the high pressure performance of thin supported Pd–23%Ag membranes-Evidence of ultrahigh hydrogen flux after air treatment. _J. Membr. Sci._ **2011** , _378_ , 28–34. [CrossRef] 

59. Pacheco Tanaka, D.A.; Melendez, J.; Fernandez, E.; Helmi, A.; Gallucci, F.; Arias, P.L. Preparation and characterization of ultra-thin (<1 micron) Pd–Ag membranes on porous alumina support (100 nm pore size). In Proceedings of the 12th International Conference on Catalysis in Membrane Reactors, Szczecin, Poland, 22–25 June 2015. 

60. Vicinanza, N.; Svenum, I.-H.; Næss, L.N.; Peters, T.A.; Bredesen, R.; Borg, A.; Venvik, H.J. Thickness dependent effects of solubility and surface phenomena on the hydrogen transport properties of sputtered Pd77%Ag23% thin film membranes. _J. Membr. Sci._ **2015** , _476_ , 602–608. [CrossRef] 

61. Pacheco Tanaka, D.A.; Okazaki, J.; Llosa Tanco, M.A.; Suzuki, T.M. Fabrication of supported palladium alloy membranes using electroless plating techniques. In _Palladium Membrane Technology for Hydrogen Production, Carbon Capture and Other Applications_ , 1st ed.; Doukelis, A., Panopoulos, K., Koumanakos, A., Kakaras, E., Eds.; Woodhead Publishing: Amsterdam, The Netherlands, 2015; pp. 83–99. 

62. Shi, L.; Goldbach, A.; Xu, H. High-flux H2 separation membranes from (Pd/Au)n nanolayers. _Int. J. Hydrog. Energy_ **2011** , _36_ , 2281–2284. [CrossRef] 

63. Damle, A.; Acquaviva, J. Membrane Reactor for Hydrogen Production. In Proceedings of the AlChE 2008 Annual Meeting, Philadelphia, PA, USA, 8–13 November 2008. Available online: http://www.pall.com/ pdfs/OEM-Media-Membranes-and-Materials/Hydrogen_Reactor_for_Hydrogen_Production.pdf (accessed on 12 September 2016). 

64. Helmi, A.; Fernandez, E.; Melendez, J.; Pacheco Tanaka, D.A.; Gallucci, F.; van Sint Annaland, M. Fluidized Bed Membrane Reactors for Ultra Pure H2 Production—A Step forward towards Commercialization. _Molecules_ **2016** , _21_ , 376–394. [CrossRef] [PubMed] 

65. Fernandez, E.; Helmi, A.; Coenen, K.; Melendez, J.; Viviente, J.L.; Pacheco Tanaka, D.A.; van Sint Annaland, M.; Gallucci, F. Development of thin Pd–Ag supported membranes for fluidized bed membrane reactors including WGS related gases. _Int. J. Hydrog. Energy_ **2015** , _40_ , 3506–3519. [CrossRef] 

66. Media and Process Technology Inc. Available online: http://www.mediaandprocess.com/products/ products02.html (accessed on 12 September 2016). 

67. Goldbach, A.; Bao, F.; Qi, C.; Bao, C.; Zhao, L.; Hao, C.; Jiang, C.; Xu, H. Evaluation of Pd composite membrane for pre-combustion CO2 capture. _Int. J. Greenh. Gas Control_ **2015** , _33_ , 69–76. [CrossRef] 

68. Veenstra, P.; Iyer, M.; Nijmeijer, A.; Geuzebroek, F.; Moene, R.; Saukaitis, J. Integrated Approach to CO2 Capture: Fuel Gas Decarbonisation. _Energy Procedia_ **2014** , _63_ , 2054–2059. [CrossRef] 

34 of 34 

_Processes_ **2016** , _4_ , 37 

69. Li, A.; Boyd, T.; Gulamhusein, A.; Mahecha-Botero, A.; Grace, J.; Lim, J.; Xu, N. Towards Industrial Applications: Membrane and Fluidized Bed Reactor Research at MRT and NORAM. In Proceedings of ECN Workshop on Pd-Membrane Technology Scale-Up, Petten, The Netherlands, 20–21 November 2014. 

70. Hysep: ECN, Hydrogen Seperation Modules. Available online: http://www.hysep.com/fileadmin/hysep/ user/documents/B-09-010-hysep.pdf (accessed on 12 September 2016). 

71. Dittmar, B.; Behrens, A.; Schödel, N.; Rüttinger, M.; Franco, T.; Straczewski, G.; Dittmeyer, R. Methane steam reforming operation and thermal stability of new porous metal supported tubular palladium composite membranes. _Int. J. Hydrog. Energy_ **2013** , _38_ , 8759–8771. [CrossRef] 

72. Gallucci, F.; van Sint Annaland, M.; Kuipers, J.A.M. Autothermal Reforming of Methane with Integrated CO2 Capture in a Novel Fluidized Bed Membrane Reactor. Part 2 Comparison of Reactor Configurations. _Top. Catal._ **2008** , _51_ , 146–157. [CrossRef] 

73. Wang, Y.; Chen, K.S.; Mishler, J.S.; Cho, C.; Cordobes Adroher, X. A review of polymer electrolyte membrane fuel cells: Technology, applications, and needs on fundamental research. _Appl. Energy_ **2011** , _88_ , 981–1007. [CrossRef] 

74. Koski, P.; Pérez, L.C.; Ihonen, J. Comparing Anode Gas Recirculation with Hydrogen Purge and Bleed in a Novel PEMFC Laboratory Test Cell Configuration. _Fuel Cells_ **2015** , _15_ , 494–504. [CrossRef] 

75. Pérez, L.C.; Rajala, T.; Ihonen, J.; Koski, P.; Sousa, J.M.; Mendes, A. Development of a methodology to optimize the air bleed in PEMFC systems operating with low quality hydrogen. _Int. J. Hydrog. Energy_ **2013** , _38_ , 16286–16299. [CrossRef] 

76. Chattot, R.; Escribano, S. Ageing studies of a PEM Fuel Cell stack developed for reformate fuel operation in µCHP units: Development of an accelerated degradation procedure. _Int. J. Hydrog. Energy_ **2015** , _40_ , 5367–5374. [CrossRef] 

77. Kikuchi, E.; Uemiya, S.; Matsuda, T. _Natural Gas Conversion_ ; Elsevier: Amsterdam, The Netherlands, 1991; Volume 61. 

78. ISO 14040. _Environmental Management—Life Cycle Assessment—Principles and Framework_ ; International Standard Organization: Geneva, Switzerland, 2006. 

79. ISO 14044. _Environmental Management—Life Cycle Assessment—Requirements and Guidelines_ ; International Standard Organization: Geneva, Switzerland, 2006. 

80. Ecoinvent. Ecoinvent Database v2.2. 2010. Available online: http://www.ecoinvent.ch (accessed on 12 September 2016). 

81. Jolliet, O.; Margni, M.; Charles, R.; Humbert, S.; Payet, J.; Rebitzer, G.; Rosenbaum, R. Impact 2002+: A New Life Cycle Impact Assessment Methodology. _Int. J. Life Cycle Assess._ **2003** , _8_ , 324–330. [CrossRef] 

82. Humbert, S.; de Schryver, A.; Margni, M.; Jolliet, O. _IMPACT 2002+ User Guide: Draft for Version 2.2_ ; Quantis: Lausanne, Switzerland, 2012. Available contacting: sebastien.humbert@quantis-intl.com (accessed on 1 October 2016). 



- © 2016 by the authors; licensee MDPI, Basel, Switzerland. This article is an open access article distributed under the terms and conditions of the Creative Commons Attribution (CC-BY) license (http://creativecommons.org/licenses/by/4.0/). 

