

<!-- Start of picture text -->
at International a<br>HYDROGEN<br>ENERGY<br>i] =<br><!-- End of picture text -->

|xWEA KAY<br>aS 4<br>hoyNae|at<br>Internationala<br>HYDROGEN<br>ENERGY|
|---|---|
|ELSEVIER<br>**e**eereereeeeee<br>eeee|i] =<br>e|



® updates 



<!-- Start of picture text -->
©<br><!-- End of picture text -->



<!-- Start of picture text -->
©<br><!-- End of picture text -->

© © 



<!-- Start of picture text -->
©<br><!-- End of picture text -->

© 

> _M.M. Alrshdan et al.                                                                                                                                                                                                                           International Journal of Hydrogen Energy 162 (2025) 150705_ 

|(_continued_)||
|---|---|
|CFD|Computational fuid dynamics|
|SMR|<br>Steam methane reforming|



# **1. Introduction** 

Rapid population growth and urban expansion have driven a significant surge in global energy demand, necessitating a shift toward alternative energy sources to reduce reliance on traditional Finite energy resources such as fossil fuels [1]. This transition aims to mitigate environmental degradation and ensure sustainable energy supply [2]. Among the emerging solutions, hydrogen has gained considerable interest because of its potential to address global warming and climate change challenges effectively. Unlike the direct combustion of methane, which releases carbon dioxide, hydrogen combustion produces only water as a by-product, which aligns with the global decarbonization goals [3]. Due to its chemical properties, hydrogen serves as a flexible energy carrier that can store renewable energy and act as a cleaner alternative to gasoline and diesel [4]. Hydrogen is acknowledged for its high energy yield and efficiency, making it a promising substitute to – conventional fossil fuels. It is approximately 2 3 times more efficient than traditional fossil fuels, particularly when used in hydrogen fuel cell vehicles [5], making it a compelling option for green energy transformation [4–6]. 

Currently, hydrogen is predominantly produced through steam reforming processes, accounting for approximately 90 % of global hydrogen production and achieving efficiencies of up to 75 % [7]. Hydrogen produced via SMR combined with carbon capture and storage (CCS) is commonly referred to as blue hydrogen. This establishes SMR as the second most efficient production method after electrolysis [3,8]. SMR is a heat-absorbing process in which methane reacts with steam at high temperatures, generally ranging from 700 to 1000<sup>◦</sup> C, using a nickel-based catalyst [9,10]. In addition to the energy required for the reforming process, energy is also supplied during the separation process, which utilizes cryogenic separation or pressure swing adsorption. [11, 12]. Hydrogen losses typically occur during the separation process, but these losses can be mitigated by using membrane reactors (MRs). Membrane reactors integrate hydrogen purification with the reforming reaction stage, leading to the minimization of system size [13], and lowering the operating temperature ( _<_ 600<sup>◦</sup> C) and energy consumption [14,15]. Palladium-based membranes are widely utilized for hydrogen separation because of their near-100 % selectivity and exceptional permeability [16]. However, they are costly and sensitive to impurities such as sulfur and CO, which can impair their performance and long-term durability [17–20]. Experimental studies on Palladium-based membrane reactors have demonstrated significant improvements in hydrogen recovery and methane conversion compared to traditional steam methane reformers. For instance, using MRs achieved methane conversion rates of up to 94 % at 511<sup>◦</sup> C, with hydrogen purity exceeding 99.2 % over extended operation periods [21]. 

To gain deeper insights into MR performance characteristics, numerous experimental analyses and computational fluid dynamics (CFD) investigations have been performed, examining how various design parameters influence system performance. Angelo Basile et al. [22] reavled that MR loaded with a Ni–ZrO catalyst exhibited superior performance compared to one using Ni–Al2O3. Optimal operating conditions were identified at 450<sup>◦</sup> C and a 4-bar pressure difference across the membrane, achieving approximately 65 % methane conversion. Similar conclusions were observed in another study in which 50 % CH4 conversion was achieved at 450<sup>◦</sup> _C_ and 3 bar by using A Pd–Ag membrane reactor containing a Ni-based catalyst [23]. The scalability of MRs was tested by De Falco et al. [24] in which a hydrogen production plant rated at 20Nm<sup>3</sup> /h was constructed and tested. It achieved a feed conversion rate of 57.3 % at 600<sup>◦</sup> C over 1000 h of operation and total of 70 thermal cycles. Moreover, a practical Palladium MR operating under 

representative conditions (580<sup>◦</sup> C, 28 bar, and a Gas Hourly Space Velocity reaching 950 h<sup>−1</sup> ) achieved methane conversion of 86 % on average over a duration of 1100 h, though this was accompanied by a reduction in H2 purity [25]. An experimental and mathematical model study, emphasizing the reaction kinetics of both water-gas shift and reforming processes within a Pd MR, found that CO products were reduced to less than 2 % compared to conventional fixed bed reactors. Additionally, a methane conversion of 80 % was attained at 500<sup>◦</sup> C and 20 bar, attributed to the ongoing extraction of hydrogen through the sweep side [26]. In the work by Chompupun et al. [27], a lab-scale cylindrical membrane reactor loaded with 10 wt% Ni/Al2O3 catalyst was evaluated across a range of temperatures, pressures, and steam-to-methane ratios to validate a numerical model formulated using COMSOL. This model was used for scaling-up strategies, resulting in the development of square-shaped annular honeycomb monolith structure. The optimal MR utilizing this monolith arrangement was achieved with a surface area-to-reactor volume ratio of 255 m<sup>2</sup> /m<sup>3</sup> . Kim et al. [28] concluded that increasing the pressure variation across the membrane led to a rise in methane conversion reaching ~77.5 % at 250 kPa with low CO (~2 %) composition in a tubular Pd–Ru membrane with Ni/Al2O3 catalyst. The study by Bryce Anzelmo et al. [29] demonstrated – that using pipeline-sourced natural gas in a Pd Au MR resulted in higher hydrogen production than pure methane, because of the high conversion rates of other hydrocarbons in the mixture (92 % for propane, 93 % for ethane,and 83 % for butane). Albasry et al. [30] investigated a Pd–Au membrane embedded in a catalytic bed, operating under pressures ranging from 10 to 30 bar at 550<sup>◦</sup> C. Methane conversion rates of 91 % and 65 % were achieved using methane and pre-reformed naphtha feeds, respectively, at 30 bar, with hydrogen purity exceeding 98.5 %. Numerous CFD studies have been performed to explore different attributes of MR. Few studies investigated the structure of the catalyst packing bed on SMR performance. Wang et al. [31] examined three distinct catalyst packing configurations: body-centered cubic (BCC), simple cubic (SC), and face-centered cubic (FCC). Among these, the FCC arrangement demonstrated the highest efficiency for the SMR reaction, followed by BCC and then SC. In a separate study, Qian et al. [32] analyzed the performance of grille-sphere composite packed beds (GSCPB) and randomly packed beds, finding that the methane conversion rate was greater in GSCPB. Ji et al. [33] investigated a sorption-assisted palladium membrane reactor configured to achieve simultaneous hydrogen extraction and carbon dioxide removal. The Sorption membrane enhanced H2 production, decreased CO2 fraction, and minimized CO membrane poisoning. Hyunjun Lee et al. [34] developed a numerical model for sorption-enhanced membranes utilized MATLAB® along with the ode45 solver, which adopts the 4th-order Runge-Kutta method, to evaluate the performance of six different membrane types. Among them, the Pd–Ru membrane delivered the – greatest hydrogen yield, whereas the Pd Ag/MPSS membrane demonstrated most favourable results in terms of hydrogen purity. Additionally, the counterflow arrangement improved H2 separation. Pashchenko et al. [35] studied the impact of computational domain dimensionality on SMR. 2D and 3D simulations were found to be more appropriate for low residence times and relative lengths. A study by Sanusi et al. [35] assessed the performance of a membrane-based reformer-combustor reactor for hydrogen production. Enhanced hydrogen yield and reduced CO concentrations were observed at elevated reformer pressures and lower gas hourly space velocities. A two-dimensional planar model of a Pd-based membrane was employed to study the influence of different conditions, including temperature, flow rate, and input stream formulation. The study concluded that utilizing vacuum pressure on the sweep gas side is beneficial under conditions of a low-pressure difference across the membrane. Conversely, using pressurized gas on the feed side is beneficial with high pressure difference [36]. Ben-Mansour et al. [37] performed a study into the influence of different parameters on CH4 conversion and H2 recovery. Their findings indicated that raising the S/C ratio improved CH4 conversion when the feed flow rate was held 

2 



<!-- Start of picture text -->
(a)<br>Retentate outlet | | Feed Inlet CH, + H,O<br>Permeate outlet __Sweep inlet H,O<br>H,O+ H,<br>(b)<br>O O O O Feed flow<br>OOG'OO0O CH,+ H,O<br>O OOGO OO O Sweep flow<br>O OO O O OO O * embron tubes<br>OOO0OO0O<br>OOOO<br>(c) H,O+ CH, H,0 + CO, + CH,+H2 +€0<br>H,0 + CH,®> + CO<br>420 TV tube ——<br>sett CO + H,0@CO0, +H |<br><!-- End of picture text -->



<!-- Start of picture text -->
2.8 Se<br>—#— This study<br>26; =—e—=<#—} NumericalExperimentstudydata (Pashchenko)(Hoang et al.)<br>wt<br>5 2.4<br>2<br>2 2.2<br>“A<br>Tt 20<br>2<br>e)<br>E 18<br>1.6<br>20 25 30 35 40 45 5.0<br>Steam to carbon ratio<br><!-- End of picture text -->



<!-- Start of picture text -->
(a) b)<br>&2<br>=>20 =—m— Methane conversion]  6.3E-7iS)<br>5 —=@®=— Hydrogen recovery 2<br>® 40 —t— Hydrogen selectivity} © 8.4E-8<br>® = 6.25E-7<br>2 2<br>= 2 6.2E-7<br>$ E 8.3E-8<br>8 20 2 6.15E-7<br>2 3<br>ee<br>o 10 o =<br>17) > Sea —#— Retentate outlet<br>g Ss —@— Permeate outlet<br>5 0 r 8.2E-8<br>GO<br>4 6 8 0 412 «14 ~~ «416 4 ae 10 Ne 14 = ‘ts<br>Feed pressure (barg) Sed pressure: (Batg)<br>()<br>26 x10<br>~ 95 —m@— 5 barg<br>we —t— 10 barg<br>c= 24 =@— 15 barg<br>2 23<br>x 2.2<br>=<br>in 2.1<br>8 2.0<br>5 1.9<br>sf 1.7<br>XI 1.6<br>1.5<br>0.0 0.1 0.2 0.3 0.4 0.5<br>Membrane length (m)<br><!-- End of picture text -->



<!-- Start of picture text -->
0 0.015 0.03 0.045 0.06 0.075 0.09 0.105 0.12 0.135 0.15 0.165 0.18 0.195 0.21 0.225 0.24 0.255 O27 0.285 03<br>a) 5 barg<br>et<br>Nee<br>03 0 Os agoomes 0.03) 10.255; tonne as!<br>10.075) 10.015}<br>b) 10 barg<br>220) — -<br>D62010.03105)0.03) mee: 10.03} 010 ener.10.03}105<br>c) 15 barg<br>0.165) ms (mt<br>ii 0.165me 0.165} 0.165) Ms 0.165<br>ee ee ee ee a |<br>0 0.1 0.2 0.3 0.4 0.5<br>Membrane length (m)<br><!-- End of picture text -->



<!-- Start of picture text -->
(a) (b)<br>50 20<br>sx<br>540 > 15<br>D oO<br>o5<br>Z8 39 3<br>c 10<br>= 20 S 5<br>= —m—5bag | + —m—5 barg<br>== 10 barg —=®— 10 barg<br>40 a==t== 15 barg 0 —t— 15 barg<br>0 1 2 3 4 0 1 2 3 4<br>Sweep flow rate/feed flow rate Sweep flow rate/feed flow rate<br>(c) (d)<br>16.0 96-104<br>215.5 Ki ,_<br>2 15.0 x<br>oO<br>2 3<br>wn 14.5 = 2.2<br>c wn<br>3 ID<br>1135> = D m= No sweep<br>‘ bak g =—@— Sweep ratio= 1<br>13.0 Ce@—15baagg z= 1.8 —=t——v— SweepSweep ratio=ratio= 2 3<br>0 1 2 3 4<br>Sweep flow rate/feed flow rate on om va a os Os<br>Membrane length (m)<br>(e) (f)<br>gz «10° B14 7107<br>o1 —m—5 barg °° —m—5 barg<br>209 —O=10 barg 1 —e— 10 barg<br>& —#= 15 barg) o= —#t—15 barg<br>0.8<br>2 0.8<br>2 0.7 a<br>EE<br>@—0.6 2 0.6<br>> Ss /<br>2 05 5 0.4<br>gaDS SS 0.2<br>£04 0 1 2 3 4 £00 0 1 2 3 4<br>Sweep flow rate/feed flow rate Sweep flow rate/feed flow rate<br><!-- End of picture text -->



<!-- Start of picture text -->
Taleh)O 0,015 0.03 0.045 0.06 0.075 0.09 0.105 0.12 0.135 0.15 0.165 018 0.195 021| 0225| 0.24~ 0255T 0.27| 0.285Tt 037)<br>a) No sweep<br>—<br>= aes 0.255) 0.255 0.255 Poaeside<br>001 Sina 0.015 a OT) 0.0 1500.01 Suan Sweep side<br>b) Sweep ratio = 1<br>220) =<br>OAR1S0105 mers 0.105 aren EO.195<br>10.0.3 0.03) 10.03} 10.03}<br>c) Sweep ratio = 2<br>= 0.015 0.01 520.21 0.015) 0.015)<br>d) Sweep ratio = 4<br>eee eee ee ee a |<br>0 0.1 0.2 0.3 0.4 0.5<br>Membrane length (m)<br><!-- End of picture text -->

( 

_ 

( 



<!-- Start of picture text -->
(a) (b)<br>50 40<br>=— Counter current —@— Counter-current<br>—e—Co-current —®—Co-current<br>seoC 45 =<br>S =<br>40 =o<br>6 35 =<br>2 3)<br>© aD<br>x=& 30 220<br>8 =<br>= 25<br>20 10 ———_—_-———————"*<br>4 6 8 10 12 14 16 4 6 8 10 12 14 16<br>Feed pressure (barg) Feed pressure (barg)<br>(c) (d)<br>x10<br>20 == Counter-current —e— Counter-current 5 barg<br>—e—Co-current & aa —4— Counter-current 10 barg<br>x 1B £ —=— Counter-current 15 barg<br>> © 35 —e—Co-current 5 barg<br>2 = —4— Co-current 10 barg<br>o 5 3.0 —=— Co-current 15 barg<br>@ 16 =<br>wB<br>= o 2.5<br>SeM = | Wasssagy uaa<br>se} © 2.0 fyate<br>z ©D 1<br>" B15<br>* 1.0 [Stee —_eccceoery |<br>4 6 8 10 12 14 16 0.0 0.1 0.2 0.3 0.4 0.<br>Feed pressure (barg) Membrane length (m)<br>(e)<br>@ 5 x10°<br>2 —=— Counter-current retentate outlet<br>* —®— Co-current retentate outlet<br>i *-m- Counter-current permeate outlet<br>= **@-+ Co-current permeate outlet<br>2 1<br>w<br>1)© ———<br>&<br>S<br>gz eo . err nanan<br>£01<br>i} Qe cccccccccnccsecs@ecccccscccccsccee®<br>6 0.05 4 6 8 10 12 14 1€<br>Feed pressuer (barg)<br><!-- End of picture text -->



<!-- Start of picture text -->
Leeman0 0.015 0.03 0.045 0.06 0.075 0.09 0.105 0.12 0.135 0.15 0.165 0.18 0.195 0.21 0.225 0.24 0.255 0.27 0.285 0.3<br>Co-current 5 barg<br>ee<br>0.27 0.27 ———— 0.271<br>aes 05) 0. Os ese O03 asa Os a<br>10.075) 10.015)<br>Counter-current 5 barg<br>‘ ORE 0, 16 eee 0.18) 0.18) OE:<br>0.045} 10.045) (0.045) 0.045) Wee gs?<br>Co-current 10 barg<br>OLN220) 10.035185 0.031 mee 10.03} 0105 pment. 10.03}195<br>Counter-current 10 barg<br>: WAL = J = 10.195)<br>. 0.045) — 0.0.45) 10.045)<br>10).03) 10.03}<br>Co-current 15 barg<br>0.165) 0.18) 0.18)<br>005 10.165) 0.165) 10.165<br>(ae coat.<br>Counter-current 15 barg 0<br>es 2<br>re Ss<br>cone tO My Sey 0.09} oe ae s<br>0.07580.0 + 02<br>0eS0.1 0.2Oe0.3 ee0.4i 0.5|<br>Membrane length (m)<br><!-- End of picture text -->



<!-- Start of picture text -->
(a) (b)<br>> 210-10"<br>= 60 Methane conversion | 2 —m— Retentate outlet<br>3 Hydrogen recovery @ —=e®— Permeate outlet<br>3 50 Hydrogen selectivity | © 0.8<br>hd =<br>22<br>>©<br>$ 30 £<br>8 § 0.4<br>wr 20 o<br>ro)5 ——— ir Zor5<br>55 0 i6 asa<br>oO 1 2 3 4 5 1 2 3 4 5<br>Steam to carbon ratio Steam to carbon ratio<br><!-- End of picture text -->



<!-- Start of picture text -->
(a) (b)<br>s e<br>S270 —®— Methane conversion rs)x —l— Retentate outlet |<br>8 60 —=@®=— Hydrogen recovery ® 49-4 == Permeate outlet<br>oO ==t= Hydrogen selectivity ©<br>o<br>3<br>c 50 =<br>©. = 10°<br>40 a<br>g E<br>58 of % 106<br>« 20 3<br>5<br>: 5 107<br>g2<br>S10° 10" 10° 107 ~ 40% 10° 104 «910% = 102104<br>Feed flow rate (kg/s) Feed flow rate (kg/s)<br>(c)<br>45-10-4<br>_ —E— 10? kg/s<br>+i 4.0 —e— 10° kg/s<br>= —t—= 10% kg/s<br>D 35 :<br>= —v— 10> kg/s<br>5 3.0<br>=<br>“oe,<br>a 25<br>| /aaeaeaeeaeaeeaL<br>c 5 0 Ra te —<br>|<br>© /<br>S 1.5<br>KS<br>z= 1.0<br>0.5<br>0.0 0.1 0.2 0.3 0.4 05<br>Membrane length (m)<br><!-- End of picture text -->



<!-- Start of picture text -->
0 0.025 0.05 0.075 0.1 0.125 0.15 0.175 0.2 0.225 0.25<br>0.00001 kg/s<br>a<br>; 0.2: 0<br>op 10.05) 10.05}<br>Ss 10.0375)<br>0.0001 kg/s<br>°<br>M0229 00.0 = 0.2 re<br>4<br>0.001 kg/s<br>Ww<br>= L<br>OMG M9 9 0.2375 $$aA $A S$ a 2375<br>0 072mm 029 001251001 opm 0.02 Siero 755<br>0.01 kg/s<br>‘ i<br>| eS ee ee ee ee |<br>(@) 0.1 0.2 0.3 0.4 0.5<br>Membrane length (m)<br><!-- End of picture text -->



<!-- Start of picture text -->
(a) (b)<br>45 28<br>—®— Tube-8 mm == Tube-8 mm<br>—®=Tube-10 mm 26 —@=Tube-10 mm<br>& 40 —t—Tube-12 mm S04 —te=Tube-12 mm<br>5><br>B© 22<br>gee 8<br>© 30 ie<br>o © 16<br>< 2<br>S 25 a 4<br>12<br>20 10<br>4 6 8 10 12 14 16 4 6 8 10 12 14 16<br>Feed pressure (barg) Feed pressure (barg)<br>(C) (d)<br>19 x10~4<br>18 == Tube-8 mm 24 —— Tube-8 mm<br>x =@®=—Tube-10 mm L —@=— Tube-10 mm<br>£17 emt Tube-12 mm £ 2.3 —t<- Tube-12 mm<br>= 2<br>® 22<br>B 16 =o,y<br>7 oO<br>> 15 ca<br>514 3<br>= fe) 1.9<br>13 Sg<br>218<br>12<br>4 6 8 10 12 14 16 0.0 0.1 0.2 0.3 0.4 0.5<br>Feed pressure (barg) Membrane length (m)<br><!-- End of picture text -->



<!-- Start of picture text -->
aa ee<br>Tube-8 mm<br>Nd<br>0.225) y= 0.2125 0.214255 0.2125) 0.2125<br>a, © (amu 0.05 0.05 0.05<br>KS (0.0375a 0.0375) (0.0375)<br>Tube-10 mm<br>wo.<br>S /<br>3\9222—— 0.24250. 2125<br>———e———E we, 0.2<br>0.0375 0.0375} ova<br>6.01251 10.0125 (0.0125 0.0125)<br>Tube-12 mm<br>°<br>0.229 0.2125) 0.2125: 0.2125<br>iC 9.30.2 = 0.2 0.2 aw<br>Caisy ieee) 055) 0.025 won0.0375)<br>ee ee ee ee ee |<br>(6) 0.1 0.2 0.3 0.4 0.5<br>Membrane length (m)<br><!-- End of picture text -->



<!-- Start of picture text -->
(a) (b)<br>s oe<br>£ HM Methane conversion) 2 -  Permeate outlet<br>B 40 [Hydrogen recovery |G 10 [I Retentate outlet<br>£ |_| Hydrogen selectivity} 6<br>ls 30.8 = oe<br>TD 30 [e)<br>7 =<br>oO 26 wn 10°"<br>>G<br>©8 20 raS4810<br>© 14.3 14.2 =<br>a 11.7 3 10°<br>§ 10 8.72 =<br>Fa D 10"?<br>72<br>O50 ; S101<br> Tube-12 mm modified — Tube-12 mm Tube-12 mm modified | Tube-12 mm<br>(c)<br>x10<br>— —=@=— Tube-12 mm<br>Ye” t= Tube-12 mm modified<br>E<br>x<br>ire}=} ——— a<br>2o1Q2 }<br>©<br>=<br>©<br>219<br>2<br>ie}<br>= 1.8<br>0.0 0.1 0.2 0.3 0.4 0.5<br>Membrane length (m)<br><!-- End of picture text -->

_International Journal of Hydrogen Energy 162 (2025) 150705_ 

> _M.M. Alrshdan et al.                                                                                                                                                                                                                           International Journal_ 

## **Table 5** 

Optimal operating and design parameters. 

|Parameter|Optimal Value|Justifcation|
|---|---|---|
|Feed pressure|10-15 barg|Higher pressures enhance hydrogen permeation but reduce methane conversion.|
|Operating temperature|873 K–1073 K<sup>a</sup>|Higher temperatures improve methane conversion and hydrogen recovery but reduce<br>selectivity.|
|Steam-to-carbon ratio<br>(S/C)<br>|3–5|Higher S/C improves methane conversion but reduces hydrogen recovery due to dilution.|
|Flow Confguration<br>|Counter-current at high pressure, Co-current at low pressure<br>|Counter-current maintains a more uniform hydrogen driving force, improving<br>performance at higher pressures.|
|Sweep fow rate<br>|Equal to or greater than feed fow rate|Enhances methane conversion and H2recovery by reducing H2partial pressure on the<br>sweep side.<br>|
|Feed fow rate|0.00001 kg/s|Lower fow rates allow longer residence time, improving CH4conversion and H2recovery.|
|Membrane tube|8 mm for best hydrogen recovery, 12 mm for highest|Smaller tubes enhance hydrogen recovery, while larger tubes improve methane|
|diameter|methane conversion|conversion.|
|Shell volume|Larger shell volume preferred|Enhances hydrogen recovery and methane conversion.|



> a Temperatures up to 1073 K are used for theoretical analysis under ideal conditions. While long-term Pd membrane operation is typically limited to ≤873 K, higher temperatures have been considered in short-term or modeled studies [56]. 

recovery capacity under diluted retentate conditions. For optimal – methane conversion, higher S/C ratios (around 4 5) are preferred. However, if hydrogen recovery is the primary objective, a lower S/C ratio of approximately 1–2 is ideal. 

# _3.5. Effect of feed flow rate_ 

The feed flow rate plays a critical role in determining the overall efficiency of hydrogen production in methane reforming, as it directly influences the residence time of gases within the reformer. To optimize system performance, the influence of feed flow rate on hydrogen production was evaluated using the Tube-12 mm MR configuration at flow rates of 10<sup>−5</sup> , 10<sup>−4</sup> , 10<sup>−3</sup> , and 10<sup>−2</sup> kg/s Fig. 10 shows the impact of feed flow rate on MR performance under the following operating conditions: an S/C ratio of 3, a temperature of 873 K, and a pressure of 10 barg. Methane conversion decreases as the feed flow rate increases. At low flow rates (1 × 10<sup>−5</sup> kg/s), methane conversion is relatively high, reaching approximately 57 %. However, as the feed flow rate increases, conversion gradually declines, dropping to around 6 % at the highest tested flow rate. This trend occurs because lower flow rates allow methane to remain in the reactor longer, providing sufficient time for conversion. On the contrary, at higher flow rates, the reduced residence time prevents the reaction from reaching equilibrium, resulting in lower conversion rates. Similarly, hydrogen recovery decreases significantly with increasing feed flow rates. At low flow rates, hydrogen recovery exceeds 31 %, but as the flow rate rises to 0.01 kg/s, recovery drops sharply to 1 %. The higher hydrogen recovery at low flow rates indicates that more hydrogen passes through the membrane due to the extended reaction and separation time. However, at higher feed flow rates, the reduced residence time limits hydrogen permeation, leading to a greater proportion of hydrogen exiting through the retentate outlet, as shown in Fig. 10(b). Additionally, hydrogen selectivity over carbon monoxide and carbon dioxide decreases as feed flow rates increase. This decline occurs because the slower reaction kinetics of secondary reactions (Reactions 2 and 3) lead to a greater formation of carbon species at higher flow rates. 

The hydrogen flux rate reaches its highest value at the maximum feed flow rate of 0.01 kg/s, as depicted in Fig. 10(c). The mass flux increases with rising flow rates due to the greater hydrogen production 

resulting from the increased methane input. Furthermore, at reduced feed flow rates, the peak hydrogen flux is attained over a shorter reformer length, owing to the increased residence time associated with lower flow velocities. The longer residence time allows the reaction to proceed to completion within a shorter section of the reformer. 

The hydrogen mole fraction on the MR changes with the feed flow rate Fig. 11. The hydrogen contour plots indicate that the lowest hydrogen mole fraction at the reformer side is located near the inlet. Region with low hydrogen mole fraction at sweep side (dark blue) extends axially as the feed flow rate increases due to the shorter residence time of reactants. At lower feed flow rates, more hydrogen is observed on the tube side (sweep side), leading to higher hydrogen recovery. 

# _3.6. Effect of membrane tube configuration_ 

Three membrane reactor (MR) geometries were examined, featuring tube diameters of 8 mm, 10 mm, and 12 mm, with corresponding pitch sizes of 17.5 mm, 20 mm, and 22.3 mm, respectively. All tubes have a length of 500 mm. The reformer volume was adjusted to maintain a constant membrane surface area-to-reformer volume ratio of 98 m<sup>−1</sup> across all configurations. Fig. 12 summarizes CH4 conversion, H2 recovery, and H2 selectivity for the three tube configurations at reformer side pressures of 5 barg, 10 barg, and 15 barg in panels (a), (b), and (c), respectively. The operating conditions were set at a temperature of 873 K, a S/C ratio of 3, and equal flow rates for feed and sweep at 0.0001 kg/ s. 

Methane conversion slightly increases as the tube diameter increases. Tube-12 mm initially shows a methane conversion of about 42 % at 5 barg, decreasing to around 29 % at 15 barg, for Tube-10 mm starts around 41 % at 5 barg and decreases to approximately 26 % at 15 barg, and for Tube-8 mm the methane conversion drops from about 39 % at 5 barg to 25 % at 15 barg. Methane conversion declines with increasing pressure, this is likely due to reaction kinetics and equilibrium limitations at higher pressure as explained in section 3.1. Tube-12 mm remains the most efficient for CH4 conversion. This can be explained by the fact that using smaller tubes (smaller tube pitch) results in higher pressure in reformer side compared to the other two configurations as explained previously based on Le Chatelier’s principle. 

## **Table 6** 

– Number of required tubes for operating temperature of a 5 10 MWth hydrogen plant. 

|Case|Operating|5 MWth||||10 MWth||||
|---|---|---|---|---|---|---|---|---|---|
||Temperature (K)|Number of<br>Tubes|Reactor<br>Diameter (m)|Reactor<br>Volume (m<sup>3</sup>)|Pd membrane<br>area (m<sup>2</sup>)|Number of<br>Tubes|Reactor<br>Diameter (m)|Reactor<br>Volume (m<sup>3</sup>)|Pd membrane<br>area (m<sup>2</sup>)|
|1|873|124,375|7.87|24.4|1953.68|248,750|11.13|48.7 m<sup>3</sup>|3907.36|
|2|973|21,675|3.28|4.22|340.47|43,350|4.64|8.45 m<sup>3</sup>|680.94|
|3|1073|16,825|2.90|3.3|264.29|33,650|4.10|6.6 m<sup>3</sup>|528.57|



15 

> _M.M. Alrshdan et al.                                                                                                                                                                                                                           International Journal of Hydrogen Energy 162 (2025) 150705_ 

Hydrogen recovery in Fig. 12(b) increases with pressure but varies with tube diameter. The 8 mm tube consistently shows the highest hydrogen recovery across all pressures. This performance is attributed to the higher H2 partial pressure in the 8 mm tube, which enhances the driving force for hydrogen permeation. This suggests that the 8 mm tube may be the most suitable for efficient H2 recovery at higher pressures compared to the other configurations. H2 selectivity shows a similar trend to hydrogen recovery. The 8 mm tube demonstrates the highest selectivity across all pressures, justifying its higher hydrogen recovery. 

Fig. 12(d) illustrates the hydrogen flux rate across three membrane tubes of varying diameters. The membrane reactor with 8 mm and 10 mm tube diameter achieve the highest hydrogen flux along the membrane length. This is due to the higher partial pressure of hydrogen that can be achieved in a smaller volume reactor. This is performance is clearly observed in mole fraction contours as shown in Fig. 13 in which higher hydrogen molar fraction concentrating is observed in 8-mm tube in the sweep side compared to the other configurations. 

# _3.7. Effect of shell volume_ 

The influence of shell volume on MR performance was examined by comparing the standard 12 mm-tube configuration, which features a membrane area-to-volume ratio of 98 m<sup>−1</sup> , with a modified 12 mm-tube configuration (12 mm-modified) that has an enhanced membrane areato-volume ratio of 131 m<sup>−1</sup> . In the 12 mm-modified setup, the tube pitch was reduced from the standard 22.3 mm– 20 mm. Both configurations were evaluated under identical operating conditions: a feed and sweep flow rate of 0.001 kg/s, (S/C) ratio of 3, and a feed pressure of 10 barg. Results indicate that methane conversion decreased to 26 % in the modified configuration, compared to 30 % in the standard Tube-12 mm setup, as shown in Fig. 14(a). Additionally, hydrogen recovery declined from 11.7 % in the standard configuration to 8 % in the modified version. However, hydrogen selectivity showed a slight increase in the 12 mm-modified tube. Reducing the shell volume leads to an increase in hydrogen partial pressure, which inhibits further hydrogen production and subsequently lowers the methane conversion rate. As a result, total hydrogen recovery through the membrane tube is lower in the modified configuration due to the reduced hydrogen concentration at the retentate outlet, as depicted in Fig. 14(b). These findings align with previous research by Bian et al. [55]. Furthermore, the modified Tube-12 mm design exhibits an increased hydrogen flux along the membrane length, due to the higher hydrogen partial pressure, as shown in Fig. 14(c). 

# _3.8. Optimized and scaled-up reactor_ 

The optimized design parameters facilitate an effective scale-up strategy for a membrane-based hydrogen production reactor, leading to enhancements in hydrogen recovery and methane conversion while ensuring operational feasibility and efficiency for large-scale applications. According to the optimized conditions specified in Table 5, key design factors such as feed pressure, operating temperature, and flow configurations must be accurately crafted to accommodate the required quantity of membrane tubes. By applying the average H2 flux and the membrane surface area, we can estimate the hydrogen flow rate per tube. This estimation aids in determining the precise number of tubes required for reactor scale-up. Higher pressures boost hydrogen permeation but may hinder methane conversion, while elevated operating temperatures enhance both CH4 conversion and H2 recovery, albeit at a cost to selectivity. Smaller tubes promote better hydrogen recovery, while larger tubes enhance methane conversion. Additionally, higher pressures facilitate hydrogen permeation but reduce methane conversion. To balance these effects, a tube diameter of 10 mm was selected at an operating pressure of 10 barg. 

The scale-up calculations assumed uniform catalyst packing and flow distribution across all tubes. Pressure drop per tube was assumed constant, with no additional losses due to manifold or channel interactions. 

Heat integration (e.g., external heating or recuperation) was not explicitly modeled but assumed to be sufficient to maintain target operating temperatures. These assumptions allow for estimation of reactor volume and membrane surface area, while more detailed process integration remains a subject for future work. A similar approach was adopted by Mancini and Mitsos [40], who defined scale-up targets for ion transport membrane (ITM) reactors based on the system-level requirement of oxidizing 1 kmol/s of methane (corresponding to 300–500 MWe) and subsequently designed the reactor geometry and flow configuration to meet those targets. This reinforces the validity of using thermal load and process-level performance criteria as the foundation for reactor scaling, as applied in this study’s design of a 5–10 MWth membrane-based hydrogen production system. 

Based on existing data, Table 6 presents the required number of tubes at various operating temperatures to meet the energy demands of a 5–10 MWth hydrogen plant, using 120 MJ/kg [52] as the lower heating value (LHV) of hydrogen. The analysis considers membrane tubes with a 10 mm diameter and 0.5 m length, operating at 10 barg with a co-current feed and a sweep flow rate of 0.0001 kg/s. This upscaling was performed based on the premise that the physical modeling framework, including reaction kinetics and transport phenomena had been previously validated against literature data for a single-channel configuration. The same validated model was extended to the multi-channel geometry to investigate system-level performance, under the assumption that geometric scaling does not fundamentally alter the underlying transport or reaction mechanisms. 

As the temperature rises, more tubes are necessary due to shifts in hydrogen permeation rates and conversion efficiencies. For a 5 MWth hydrogen plant, the required tube count varies from 124,375 at 873 K to 16,825 at 1073 K, while for a 10 MWth plant, it ranges from 248,750 to 33,650 tubes across the same temperature spectrum. This increase in tube quantity with rising temperatures underscores the importance of optimizing reactor design to achieve a balance between hydrogen production efficiency and material as well as operational constraints. Additionally, the estimated total palladium membrane surface area, calculated based on a tube diameter of 10 mm and length of 0.5 m, is included in Table 6. These values provide a useful indication of the relative material requirements and associated cost implications for different operating conditions and plant scales. 

# **4. Conclusions** 

The potential for scaling up membrane reactors for industrial hydrogen production emphasizes the need for optimal reactor design and operational conditions. Optimizing the membrane reactor helps minimize methane leakage, thus reducing greenhouse gas emissions and enhancing the environmental viability of blue hydrogen as a cleaner energy source. These conclusions provide a comprehensive realization of the critical factors that impact the efficiency of steam methane reforming in MR, facilitating progress toward greener and more effective hydrogen production solutions. 

- While higher feed pressures are essential for efficient hydrogen separation in membrane reactors, they often lead to a decrease in methane conversion efficiency. This inverse relationship highlights the importance of carefully optimizing pressure to balance CH4 conversion and H2 recovery. Higher sweep flow rates enhance hydrogen separation by creating a larger H2 partial pressure across the membrane. This results in improved CH4 conversion, as well as increased H2 recovery and selectivity in the reactors. 

- A counter-current flow configuration can achieve higher hydrogen recovery, excelling at high feed pressures. Conversely, the co-current configuration performs better at low feed pressures. Increasing the S/ C ratio improves methane conversion but negatively impacts hydrogen recovery due to the dilution effect of excess steam. 

16 

> _M.M. Alrshdan et al.                                                                                                                                                                                                                           International Journal of Hydrogen Energy 162 (2025) 150705_ 

- The feed flow rate is a critical parameter in methane reforming processes, as it directly affects CH4 conversion, H2 recovery, and permeation. Lower feed flow rates favor higher methane conversion and higher H2 recovery due to the longer residence time of reactants. 

- Higher operating temperatures improve reactor performance by increasing CH4 conversion and H2 recovery. However, hydrogen selectivity is reduced, indicating the formation of by-products at higher temperatures. 

- Larger membrane tube diameter shows the best methane conversion. And the smaller tube diameter configure shows best the hydrogen recovery, and selectivity across all pressure levels. These results suggest that the choice of tube has a significant impact on hydrogen recovery and optimizing pressure conditions could further enhance recovery. 

- The larger shell side volume enhances CH4 conversion and H2 recovery. 

- The method was built up to the level of a 5–10 MWth hydrogen plant based on optimum operating and design parameters, and the resulting membrane reactor included 16,825–33,650 membrane tubes, a shell diameter of 2.9–4.1 m, and a reactor capacity of 3.3–6.6 m<sup>3</sup> . 

Further investigating the membrane reformer dimensions of the tube and pitch size is recommended under higher feed pressure, to underline the tube and pitch size for best CH4 conversion and H2 recovery. Additionally, studying the impact of the membrane length on the hydrogen recovery. Moreover, Future work may include a detailed technoeconomic analysis incorporating membrane material costs, fabrication methods, and system integration factors to better evaluate the practical feasibility of large-scale implementation. 

# **CRediT authorship contribution statement** 

**Minas M. Alrshdan:** Writing – original draft, Validation, Methodology, Investigation. **Usama Ahmed:** Writing – review & editing, Supervision, Methodology, Conceptualization. **Khalid Elserfy:** Writing – original draft, Software, Methodology, Investigation. **Medhat A. Nemitallah:** Writing – review & editing, Supervision, Software, Project administration, Methodology, Funding acquisition, Conceptualization. 

# **Declaration of competing interest** 

The authors declare that they have no known competing financial interests or personal relationships that could have appeared to influence the work reported in this paper. 

# **5 Acknowledgement** 

The authors would like to acknowledge the financial support from the Dhahran Techno Valley Holding Company (DTVC) at King Fahd University of Petroleum and Minerals (KFUPM) through the Dhahran Techno Valley Research Collaborative Grant number DTV23202 between KFUPM and Air Products Middle East Industrial Gases Llc. The support received from Air Products Middle East Industrial Gases Llc through grant number CHTC2222 is also appreciated. 

# **Appendix A. Supplementary data** 

Supplementary data to this article can be found online at https://doi. org/10.1016/j.ijhydene.2025.150705. 

# **References** 

- [1] Soltani R, Rosen MA, Dincer I. Assessment of CO2 capture options from various points in steam methane reforming for hydrogen production. Int J Hydrogen Energy Dec. 2014;39(35):20266–75. https://doi.org/10.1016/j. ijhydene.2014.09.161. 

- [2] Ahmad T, Zhang D. A critical review of comparative global historical energy consumption and future demand: the story told so far. Elsevier Ltd.; Nov. 01, 2020. https://doi.org/10.1016/j.egyr.2020.07.020. 

- [3] Levalley TL, Richard AR, Fan M. The progress in water gas shift and steam reforming hydrogen production technologies - a review. Elsevier Ltd.; Oct. 13, 2014. https://doi.org/10.1016/j.ijhydene.2014.08.041. 

- [4] da Silva Veras T, Mozer TS, da Costa Rubim Messeder dos Santos D, da Silva C´esar A. Hydrogen: trends, production and characterization of the main process worldwide. Elsevier Ltd.; Jan. 26, 2017. https://doi.org/10.1016/j. ijhydene.2016.08.219. 

- [5] Suleman F, Dincer I, Agelin-Chaab M. Environmental impact assessment and comparison of some hydrogen production options. Int J Hydrogen Energy Jun. 2015;40(21):6976–87. https://doi.org/10.1016/j.ijhydene.2015.03.123. 

- [6] Khan MI, Al-Ghamdi SG. Hydrogen economy for sustainable development in GCC countries: a SWOT analysis considering current situation, challenges, and prospects. Int J Hydrogen Energy Apr. 2023;48(28):10315–44. https://doi.org/ 10.1016/j.ijhydene.2022.12.033. 

- [7] Le PA, Trung VD, Nguyen PL, Bac Phung TV, Natsuki J, Natsuki T. The current status of hydrogen energy: an overview. Royal Society of Chemistry; Sep. 25, 2023. https://doi.org/10.1039/d3ra05158g. 

- [8] Sarmah MK, Singh TP, Kalita P, Dewan A. Sustainable hydrogen generation and storage - a review. Royal Society of Chemistry; Aug. 23, 2023. https://doi.org/ 10.1039/d3ra04148d. 

- [9] Basile A, Iulianelli A, Tong J. Single-stage hydrogen production and separation from fossil fuels using micro-and macromembrane reactors. In: Compendium of hydrogen energy. Elsevier; 2015. p. 445–68. 

- [10] V Twigg M. Catalyst handbook. Routledge; 2018. 

- [11] Martin-Gil V, Ahmad MZ, Castro-Munoz R, Fila V. Economic framework of ˜ membrane technologies for natural gas applications. Separ Purif Rev 2019;48(4): 298–324. 

- [12] Simpson AP, Lutz AE. Exergy analysis of hydrogen production via steam methane reforming. Int J Hydrogen Energy 2007;32(18):4811–20. 

- [13] Vigneault A, Grace JR. Hydrogen production in multi-channel membrane reactor via steam methane reforming and methane catalytic combustion. Int J Hydrogen Energy 2015;40(1):233–43. 

- [14] De Falco M, Piemonte V, Di Paola L, Basile A. Methane membrane steam reforming: heat duty assessment. Int J Hydrogen Energy 2014;39(9):4761–70. 

- [15] Kassi AH, Al-Hattab TA. A review: membrane reactor for hydrogen production: modeling and simulation. Eng Chem Aug. 2023;4:17–31. https://doi.org/10.4028/ p-xakne1. 

- [16] El-Shafie M, Kambara S, Hayakawa Y. Comparative study on the numerical simulation of hydrogen separation through palladium and palladium–copper membranes. Int J Hydrogen Energy Jun. 2022;47(54):22819–31. https://doi.org/ 10.1016/j.ijhydene.2022.05.094. 

- [17] Ryi S-K, Park J-S, Kim S-H, Cho S-H, Kim D-W, Um K-Y. Characterization of Pd–Cu–Ni ternary alloy membrane prepared by magnetron sputtering and Cureflow on porous nickel support for hydrogen separation. Sep Purif Technol 2006; 50(1):82–91. 

- [18] Jaid GM, AbdulRazak AA, Meskher H, Al-Saadi S, Alsalhy QF. Metal-organic frameworks (MOFs), covalent organic frameworks (COFs), and hydrogen-bonded organic frameworks (HOFs) in mixed matrix membranes. Mater Today Sustain 2024:100672. 

- [19] Merlet RB, Pizzoccaro-Zilamy M-A, Nijmeijer A, Winnubst L. Hybrid ceramic membranes for organic solvent nanofiltration: state-Of-The-Art and challenges. J Membr Sci 2020;599:117839. 

[20] Easa J, Yan C, Schneider WF, O’Brien CP. CO and C3H6 poisoning of hydrogen permeation across Pd77Ag23 alloy membranes: a comparative study with pure palladium. Chem Eng J 2022;430:133080. 

- [21] Abu El Hawa HW, Lundin STB, Patki NS, Douglas Way J. Steam methane reforming in a Pd-Au membrane reactor: long-Term assessment. Int J Hydrogen Energy Jun. 2016;41(24):10193–201. https://doi.org/10.1016/j.ijhydene.2016.04.244. 

- [22] Basile A, et al. Methane steam reforming in a Pd–Ag membrane reformer: an experimental study on reaction pressure influence at middle temperature. Int J Hydrogen Energy 2011;36(2):1531–9. 

- [23] Iulianelli A, et al. H2 production by low pressure methane steam reforming in a Pd–Ag membrane reactor over a Ni-based catalyst: experimental and modeling. Int J Hydrogen Energy 2010;35(20):11514–24. 

- [24] De Falco M, Iaquaniello G, Salladini A. Experimental tests on steam reforming of natural gas in a reformer and membrane modules (RMM) plant. J Membr Sci 2011; 368(1–2):264–74. 

- [25] Sari´c M, van Delft YC, Sumbharaju R, Meyer DF, de Groot A. Steam reforming of methane in a bench-scale membrane reactor at realistic working conditions. Catal Today 2012;193(1):74–80. 

- [26] Lin Y-M, Liu S-L, Chuang C-H, Chu Y-T. Effect of incipient removal of hydrogen through palladium membrane on the conversion of methane steam reforming: experimental and modeling. Catal Today 2003;82(1–4):127–39. 

- [27] Chompupun T, Limtrakul S, Vatanatham T, Kanhari C, Ramachandran PA. Experiments, modeling and scaling-up of membrane reactors for hydrogen production via steam methane reforming. Chem Eng Process Process Intensif 2018; 134:124–40. 

- [28] Kim C-H, Han J-Y, Lim H, Kim D-W, Ryi S-K. Methane steam reforming in a membrane reactor using high-permeable and low-selective Pd-Ru membrane. Kor J Chem Eng 2017;34:1260–5. 

- [29] Anzelmo B, Wilcox J, Liguori S. Hydrogen production via natural gas steam reforming in a Pd-Au membrane reactor. Comparison between methane and natural gas steam reforming reactions. J Membr Sci 2018;568:113–20. 

17 

> _M.M. Alrshdan et al.                                                                                                                                                                                                                           International Journal of Hydrogen Energy 162 (2025) 150705_ 

- [30] Albasry AA, et al. Membrane reformer technology for sustainable hydrogen production from hydrocarbon feedstocks. Int J Hydrogen Energy 2024. https://doi. org/10.1016/j.ijhydene.2024.10.257. 

- [31] Wang J, Yang J, Sunden B, Wang Q. Hydraulic and heat transfer characteristics in structured packed beds with methane steam reforming reaction for energy storage. Int Commun Heat Mass Tran 2021;121:105109. https://doi.org/10.1016/j. icheatmasstransfer.2021.105109. 

- [32] Qian P, Wang J, Wu Z, Yang J, Wang Q. Performance comparison of methane steam reforming in a randomly packed bed and a grille-sphere composite packed bed. Energy Convers Manag 2019;193:39–51. https://doi.org/10.1016/j. enconman.2019.04.052. 

- [33] Ji G, Zhao M, Wang G. Computational fluid dynamic simulation of a sorptionenhanced palladium membrane reactor for enhancing hydrogen production from methane steam reforming. Energy 2018;147:884–95. 

- [34] Lee H, Kim A, Lee B, Lim H. Comparative numerical analysis for an efficient hydrogen production via a steam methane reforming with a packed-bed reactor, a membrane reactor, and a sorption-enhanced membrane reactor. Energy Convers Manag 2020;213:112839. 

- [35] Sanusi YS, Mokheimer EMA. Performance analysis of a membrane-based reformercombustor reactor for hydrogen generation. Int J Energy Res 2019;43(1):189–203. 

- [36] Ben-Mansour R, Abuelyamen A, Habib MA. CFD modeling of hydrogen separation through Pd-based membrane. Int J Hydrogen Energy 2020;45(43):23006–19. https://doi.org/10.1016/j.ijhydene.2020.06.141. 

- [37] Ben-Mansour R, et al. Comprehensive parametric investigation of methane reforming and hydrogen separation using a CFD model. Energy Convers Manag 2021;249:114838. https://doi.org/10.1016/j.enconman.2021.114838. 

- [38] Nemitallah MA. Characteristics of hydrogen separation and methane steam reforming in a Pd-based membrane reactor of shell and tube design. Case Stud Therm Eng 2023;45:102939. https://doi.org/10.1016/j.csite.2023.102939. 

- [39] Choi H, et al. CFD analysis and scale up of a baffled membrane reactor for hydrogen production by steam methane reforming. Comput Chem Eng 2022;165: 107912. https://doi.org/10.1016/j.compchemeng.2022.107912. 

- [40] Mancini ND, Mitsos A. Ion transport membrane reactors for oxy-combustion–Part II: analysis and comparison of alternatives. Energy 2011;36(8):4721–39. https:// doi.org/10.1016/j.energy.2011.05.024. 

- [41] Nemitallah MA, Habib MA, Badr HM. Design of a multi-can carbon-free gas turbine combustor utilizing multiple shell-and-tube OTRs for ZEPP applications. J Nat Gas Sci Eng 2017;46:172–87. https://doi.org/10.1016/j.jngse.2017.06.031. 

- [42] Ansys Fluent Theory Guide. Ansys fluent theory guide. ANSYS Inc, USA 2021; 15317(November). 

- [43] Sharma R, Kumar A, Upadhyay RK. Characteristic of a multi-pass membrane separator for hydrogen separation through self-supported Pd–Ag membranes. Int J Hydrogen Energy Mar. 2018;43(10):5019–32. https://doi.org/10.1016/j. ijhydene.2018.01.127. 

- [44] Hoang DL, Chan SH, Ding OL. Kinetic and modelling study of methane steam reforming over sulfide nickel catalyst on a gamma alumina support. Chem Eng J 2005;112(1–3):1–11. 

- [45] Ergun S, Orning AA. Fluid flow through randomly packed columns and fluidized beds. Ind Eng Chem 1949;41(6):1179–84. 

- [46] Upadhyay M, Lee H, Kim A, hun Lee S, Lim H. CFD simulation of methane steam reforming in a membrane reactor: performance characteristics over range of operating window. Int J Hydrogen Energy Aug. 2021;46(59):30402–11. https:// doi.org/10.1016/j.ijhydene.2021.06.178. 

- [47] Xu J, Froment GF. Methane steam reforming, methanation and water-gas shift: I. Intrinsic kinetics. AIChE J 1989;35(1):88–96. 

- [48] “methane steam reforming, methanation and water-gas shift: 1. Intrinsic kinetics.”. 

- [49] Xu J, Froment GF. Methane steam reforming, methanation and water-gas shift: I. Intrinsic kinetics. AIChE J 1989;35(1):88–96. 

- [50] Fernandes FAN, Soares Jr AB. Modeling of methane steam reforming in a palladium membrane reactor. Lat Am Appl Res 2006;36(3):155–61. 

- [51] Gallucci F, van Sint Annaland M, Kuipers JAM. Modeling of membrane reactors for hydrogen production and purification. 2011. 

- [52] Xu J, Froment GF. Methane steam reforming, methanation and water-gas shift: I. Intrinsic kinetics. AIChE J 1989;35(1):88–96. 

- [53] Elnashaie SSEH. Modelling, simulation and optimization of industrial fixed bed catalytic reactors. Routledge; 2022. 

- [54] Pashchenko D. Effect of the geometric dimensionality of computational domain on the results of CFD-modeling of steam methane reforming. Int J Hydrogen Energy 2018;43(18):8662–73. 

- [55] Bian Z, et al. A CFD study on H2-permeable membrane reactor for methane CO2 reforming: effect of catalyst bed volume. Int J Hydrogen Energy Nov. 2021;46(77): 38336–50. https://doi.org/10.1016/j.ijhydene.2021.09.098. 

- [56] Al-Mufachi NA, V Rees N, Steinberger-Wilkens R. Hydrogen selective membranes: a review of palladium-based dense metal membranes. Renew Sustain Energy Rev 2015;47:540–51. https://doi.org/10.1016/j.rser.2015.03.026. 

18 

