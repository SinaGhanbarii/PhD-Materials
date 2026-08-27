Energy 344 (2026) 140143 



Contents lists available at ScienceDirect 

# Energy 

journal homepage: www.elsevier.com/locate/energy 



## Enhancing hydrogen production from methane steam reforming using a palladium-based membrane reactor inserted with triple-helix structure 



Xin-Yuan Tang<sup>a,b</sup> , Jia-Chen Li<sup>a</sup> , Zhan-Bin Liu<sup>a</sup> , Sheng-Song Xia<sup>a</sup> , Wei-Wei Yang<sup>a,*</sup> , Ya-Ling He<sup>a</sup> 

a _Key Laboratory of Thermo-Fluid Science and Engineering of MOE, School of Energy and Power Engineering, Xi'an Jiaotong University, Xi'an, 710049, China_ b _School of Chemical Engineering and Technology, Xi'an Jiaotong University, Xi'an, Shaanxi, 710049, China_ 

|A R T I C L E I N F O|A B S T R A C T|
|---|---|
|_Keywords:_<br>Hydrogen separation<br>Membrane reactor<br>Nickel catalyst<br>Palladium membrane<br>Steam reforming<br>Triple-helix insert|Membrane reactor (MR) represents an ideal technology for simultaneously producing and purifying hydrogen,<br>holding signifcant potential in future clean energy systems. This study developed a new triple-helix insert<br>enhanced membrane reactor (I-MR) for hydrogen production via methane steam reforming. By combining ex-<br>periments with theoretical limit calculations, the performance of conventional reactor (CR), original MR (O-MR),<br>and I-MR was systematically compared. Results demonstrate that MRs achieve forward reaction shift through<br>hydrogen separation, enabling methane conversion exceeding those of CR and even thermodynamic equilibrium<br>states. Compared to CR, I-MR achieves 27.1–75.8 % higher conversion within the 400–500 <sup>◦</sup>C range, with more<br>pronounced improvements at higher temperatures. Furthermore, the triple-helix insert effectively suppressed<br>concentration polarization by promoting hydrogen mixing and redistribution, signifcantly boosting reaction<br>effciency. At 450 <sup>◦</sup>C, the I-MR achieved an average 19.5 % higher methane conversion than the O-MR and<br>demonstrated superior low-temperature activity across a broader temperature range. Moreover, under the CR<br>reaction benchmark at 700 <sup>◦</sup>C, I-MR maintained equivalent conversion capability while reducing the required<br>temperature by ~199.1 <sup>◦</sup>C. Compared to O-MR, I-MR achieved a maximum temperature reduction of ~52.6 <sup>◦</sup>C,<br>demonstrating potential for effcient hydrogen production under mild conditions. Also, the I-MR achieved stable<br>operation for 25 h without noticeable carbon buildup or deactivation. The above results demonstrate the reliable<br>role of the new triple-helix insert structure in enhancing hydrogen production within membrane reactors,<br>indicating the potential of low-energy hydrogen production technologies.|



Nomenclature ( _continued_ ) 

|I-MR|insert-enhanced membrane reactor<br>|
|---|---|
|MF|mass fow controller|
|MR|membrane reactor|
|O-MR|original membrane reactor|
|TG|thermogravimetric|



|_E_|membrane permeation activation energy (J⋅mol<sup>−1</sup>)<br>|MF<br>mass fow controller|
|---|---|---|
|_J_H2|hydrogen permeation fux (kg⋅m<sup>−2</sup>⋅s<sup>−1</sup>)|<br>MR<br>membrane reactor|
|_p_re|reaction side pressure (bar)|O-MR<br>original membrane reactor|
|_p_se|separation side pressure (Pa)<br>|TG<br>thermogravimetric|
|_Q_CH4|methane feed fow rate (ml⋅min<sup>−1</sup>)||
|_SMR_|steam-to-methane ratio||
|_T_|reaction temperature (<sup>◦</sup>C)||
|**_Greek symbols_**|||
|Δ_T_|temperature drop at equal methane conversion in CR (<sup>◦</sup>C)|**1. Introduction**|
|_η_CH4|methane conversion (%)||
|_φ_<br>**_Abbreviations_**|gas component proportion (%)|To address the signifcant pressures on energy resources and the|
|CR|conventional reactor|ecological environment, a steady transition toward an energy structure|
|GC|gas chromatograph|dominated by renewable sources is crucial [1–3]. Hydrogen energy, as a|
|Gmin|Gibbs minimum state|clean, zero-carbon secondary energy carrier, features high energy den-|
||(_continued on next column_)|sity, stable storage characteristics, and strong practicality, making it an|



- Corresponding author. 

_E-mail address:_ yangww@mail.xjtu.edu.cn (W.-W. Yang). 

https://doi.org/10.1016/j.energy.2026.140143 

Received 10 November 2025; Received in revised form 1 January 2026; Accepted 20 January 2026 Available online 20 January 2026 

0360-5442/© 2026 Elsevier Ltd. All rights are reserved, including those for text and data mining, AI training, and similar technologies. 

_X.-Y. Tang et al._ 

_Energy 344 (2026) 140143_ 

essential component of future renewable energy systems [4,5]. However, as hydrogen is naturally scarce in the environment, it typically needs to be extracted from hydrogen-containing compounds [6–8]. Consequently, technologies for hydrogen production and purification have attracted significant attention [9,10]. Steam methane reforming is currently one of the most established methods for hydrogen production, accounting for nearly half of the global hydrogen supply [11]. Due to limitations in energy and feed sources, the hydrogen produced by this method is still considered "gray hydrogen" [12]. To reduce the substantial heat requirements of reforming reactions, integrating solar thermal energy into the reforming process has become a research hotspot, as it nearly eliminates the need for additional energy input [13–15]. Moreover, renewable resources such as biogas and bioethanol are emerging as alternative feedstocks for hydrogen production, offering significant sustainability benefits [16–18]. The integration of solar energy with biogas further highlights the immense potential of this process for the future [19]. 

In hydrogen production systems, the separation and purification of hydrogen from the products are also key to the efficient and large-scale utilization of hydrogen. Conventional methods, such as cryogenic separation, pressure swing adsorption, and membrane separation, often incur additional spatial and economic costs [20,21]. Moreover, achieving integrated hydrogen production and purification that is efficient, mild, and simple is crucial for subsequent industrial applications [22]. Among these, compact membrane reactors that incorporate membrane separation technology represent an effective approach that combines hydrogen production, separation, and purification functions, while enhancing the economic feasibility and conversion performance of conventional processes [23–25]. Membranes currently used for separation can be broadly classified into organic and inorganic membranes [26]. Organic membranes, also known as polymeric membranes, are — sensitive to operating conditions factors such as high temperature, pH, and moisture can cause denaturation or deformation, making them unsuitable for thermochemical applications [27]. Inorganic membranes mainly include two types: porous membranes based on a sieving mechanism, and dense membranes based on a solution-diffusion mechanism [28]. Porous membranes (e.g., ceramic, zeolite, and carbon membranes) generally possess self-supporting capability, along with good mechanical, chemical, and thermal stability, offering favorable economics [29–31]. However, they need to consider improving selectivity and separation efficiency. Dense membranes, mainly made of metals or metal oxides, exhibit high selectivity and considerable permeability, performing particularly well under high-temperature conditions, which makes them well-suited for high-temperature processes [32–34]. Among them, Pd has emerged as the mainstream material for hydrogen separation due to its outstanding hydrogen permeability, selectivity, and stability [35,36]. Also, Jiang et al. [37] found that among modified MFI zeolite membranes, carbon molecular sieve membranes, and Pd-Ag membranes, the Pd-Ag membrane exhibited the highest hydrogen permeability and selectivity. However, its practical application still faces two major challenges: First, hydrogen embrittlement at low temperatures ( _<_ 300<sup>◦</sup> C), where hydride phase transitions cause membrane material brittleness; second, membrane poisoning caused by impurities such as sulfur compounds and carbon monoxide in the feed gas. These impurities chemically adsorb or clog the membrane surface, severely reducing its performance and lifespan [38]. To solve these issues, alloying Pd with other metal elements has resulted in Pd-based membranes with enhanced thermal and chemical stability, leading to broader applications [39,40]. Additionally, the efficient and safe operating range of Pd-based membranes aligns well with medium-to-high-temperature reactions such as methane reforming and ammonia cracking, and has been verified to operate stably for over 1000 h [41]. Thus, considering operating conditions, separation performance, and membrane durability, Pd-based membranes remain the preferred separation component in numerous membrane reactor studies [32,41]. Notably, due to the inherent properties of precious metals, Pd 

membranes inevitably carry a higher cost. Thus, fully and stably leveraging the superior performance of Pd membranes within reactors is of paramount importance. Of course, while Pd-based membranes are currently the most commonly used separation materials in membrane reactors, several new, relatively inexpensive materials also show potential (such as ceramic ion-conducting membrane [9]), particularly after further improvements in their permeability and selectivity. 

However, while membrane materials primarily determine the kinetics of hydrogen separation, a more critical yet often overlooked challenge lies in the performance limitations imposed by the reactor structure on membrane utilization [42,43]. The mismatch between hydrogen permeation through the membrane and hydrogen diffusion from the reaction zone leads to significant concentration gradients, hindering efficient separation, a phenomenon known as concentration polarization [44,45]. This effect is observed in all membrane reactors, including those with Pd membranes. Researchers have begun addressing this issue through theoretical and experimental work aimed at mitigating concentration polarization and enhancing separation performance in reactor design improvements [46–48]. For instance, in simulation-based design, Sharma et al. [49] proposed a modular multi-channel membrane separator with baffles, demonstrating a 33 % increase in hydrogen recovery compared to a single-channel configuration. Inspired by the efficient production and transport mechanisms in plant leaves, Tang et al. [50] designed a bionic solar-driven membrane reactor catalytic bed that mimics the structure of mesophyll and veins to synergize reaction and separation processes. Wang et al. [51] introduced a concept for alternately separating hydrogen and CO2 using a combined membrane to enhance reaction driving force in solar thermochemical processes. Experimentally, Nakajima et al. [42] investigated the impact of concentration polarization on hydrogen production by downsizing the reactor. The reduced distance for hydrogen transport to the membrane enhanced reaction and separation efficiencies by 2.2 % and 11 %, respectively. Mori et al. [43] similarly pursued reactor downsizing, further investigating the effect of adding flat baffles on membrane reactor performance. By forcing component transfer toward the membrane to enhance hydrogen partial pressure on the membrane side, they achieved a 5.8 % increase in methane conversion. Sharma et al. [52] tested a four-channel membrane reactor, finding that this multi-channel design enabled more efficient membrane-gas contact, significantly boosting hydrogen recovery. Moreover, in multi-product separation, Ling et al. [53] reported a membrane reactor that combined CO2 adsorption and H2 separation, reaching 99 % methane conversion at 400<sup>◦</sup> C. However, performance declined as CO2 adsorption saturated, requiring regeneration and leading to operational discontinuity. In summary, the development and broad application of membrane reactors still face challenges related to safety, efficiency, and stable long-term operation. The above research findings indicate that the primary membrane reactor intensification methods in simulations and experiments focus on reducing reactor size, catalytic bed design, multi-product separation, and baffles/inserts. However, smaller reactor sizes inevitably constrain overall production scale; while specialized catalytic bed designs hold significant potential, their manufacturing poses challenges; multi-product separation primarily targets CO2 separation, necessitating timely regeneration of adsorbent materials, which results in an intermittent production process. In contrast, adding inserts represents a cost-effective and readily implementable improvement. However, the discontinuous design of conventional flat or annular inserts may create dead zones in mass transfer, thereby inhibiting the full exchange of all hydrogen components. 

Currently, membrane reactors have garnered considerable attention in both theoretical simulations and experimental studies, demonstrating their potential to reduce reaction temperature requirements. Achieving equivalent performance at lower temperatures not only means reduced process energy consumption but also eases the high-temperature tolerance requirements for reactors and membrane materials, thereby extending system lifespan. Thus, to fully exploit this potential and 

2 



<!-- Start of picture text -->
A Reactor exterior<br>- _ = H,<br>/CH,/H,0/Ar_ > ; -—- ! Internal=<br>v Hee eee eee eee<br>Conventional reactor (CR) |= Membrane reactor (O-MR) 7Insert-enhanced MR (I-MR);<br>B Cc 'D<br>l as I<br>I att® : ¥ I<br>1 g@%>:: I<br>I NZ I<br>I I<br>SSS 5S 5 So<br>OsSO,: y Exploded I<br>Ni !<br>: 4 Wy, I<br>y I<br>I~ Pd-Ag Membrane “Helical insert (3) Ni/Al,O3 catalyst }<br><!-- End of picture text -->



<!-- Start of picture text -->
A<br>CH. MF Vacuum }4<br>Pressure es pump 2<br>Mass flo gaugeu Permeation side =»<br>ter SISSHIGh<br>Ar P ectric furnace j © ~<br>MF" Gyyy° —_Sectic<br>= tur (5,)<br>* (Membrane) reactor fell<br>ey 5 r= ON<br>130°C Condenser ast]<br>Steam Reaction side Gas<br>peneratar chromatography<br>B a) ¢-~>~=% (Membrane) \<br>. ——" Fie = Be reactor<br>4 wee: Gene! fer |<br>4 | | Mass flow 1) | au Bi iy ul ee A<br>reg. meters Mier tia) ihe cas at | oe iat? il<br>o - | Bike Ww =~ (Gc9790P tus) =’ Dae<br>i me : : : RK nA \ . eG aa | aie EA he<br>——<br>=a | * Amaia? | — a= |et<br>ct 88<br>ie ee a - Lt a ONdeNSE re I<br>eee ae kd =——— ed<br><!-- End of picture text -->

_X.-Y. Tang et al._ 

_Energy 344 (2026) 140143_ 



where _φ_ denotes the dry component fraction of CH4, CO2, CO, and H2. During hydrogen permeation through a Pd membrane, the hydrogen permeation flux ( _J_ H2) follows Sieverts' law [35], typically depending on the temperature and hydrogen partial pressures on both sides of the membrane, and can be expressed as follows: 



where Mem denotes the intrinsic physical properties of the Pd membrane, such as effective membrane area, thickness, and permeation index coefficient; _E_ represents the permeation activation energy; _p_ H2,re and _p_ H2,se denote the reaction-side and separation-side pressures at the membrane surface; _n_ is the partial pressure index, with a value range of 0–1, typically determined by the intrinsic properties and defects of the membrane, and generally set to 0.5 in Sieverts' law, respectively. 

The above outlines the experimental testing procedure for the conversion and production in the reactor. Additionally, due to the unique properties of the Pd membrane, it is essential to prevent oxygen exposure at elevated temperatures (above 200<sup>◦</sup> C) and hydrogen exposure at low temperatures (below 300<sup>◦</sup> C). Oxygen exposure causes membrane oxidation and brittleness, while hydrogen exposure leads to hydrogen embrittlement. Thus, both the heating and cooling processes require continuous Ar flow to maintain an inert environment, and the catalyst reduction process must be strictly conducted after stabilization at 400<sup>◦</sup> C. 

### _2.2.1. Reaction conditions_ 

Table 2 summarizes the reaction condition categories and ranges tested for the reactors (CR, O-MR, and I-MR) in this study. The specific control process is implemented by the controller: the programmable thermostat and electric furnace control the reaction temperature, the mass flow meter regulates the feed flow rate and steam-to-methane ratio, while the back-pressure valve (Xiongchuan Ltd., SS-99, pressure – adjustment range is 0 6.8 bar) adjusts the outlet pressure to control the reaction zone pressure. Each reaction condition was tested 3 times, with the average value taken after performance results stabilized. To prevent performance degradation caused by catalyst decay, hydrogen was introduced after each experimental run to reduce and clean the catalyst. 

### _2.3. Experimental error analysis_ 

To analyze the error in testing methane conversion within this experimental platform, an error propagation analysis model was constructed using the root mean square synthesis method. The relative error for each detected gas _i_ (Δ _φi_ ) in the GC's detection of outlet gas composition comprises noise error, integration error, and precision. Combined with the precision parameters in Tables 1 and it can be expressed as: 



where _i_ represents one of the detectable gases CH4, H2, CO2, and CO in the GC. 

Thus, the root mean square synthetic error propagation formula for 

#### **Table 2** 

Reaction conditions and their ranges for hydrogen production experiments. 

|Parameter|Symbol (Unit)|Range|Interval|
|---|---|---|---|
|Reaction temperature<br>|T (<sup>◦</sup>C)|400–600|50|
|Methane feed fow rate|QCH4(ml⋅min<sup>−1</sup>)|20–100|20|
|<br>Steam-to-methane ratio|SMR|2.5–3.5|0.5|
|Reaction side pressure|pre(bar)|1–1.8|0.4|



methane conversion detection error (Δ _η_ CH4) is as follows: 



Taking a typical composition of dry export products as an example: CH4: 5 %, CO2: 36 %, CO: 0.04 %, H2: 2 %. At this point, the methane conversion is 87.82 %, with the maximum relative error in methane conversion calculated at 4.43 %. Overall, performance metric errors remain within 5 %, falling within an acceptable tolerance range. Also, the study employs a three-measurement averaging method to further reduce performance measurement errors. 

Additionally, GC and MF controllers are calibrated monthly to ensure the reliability of analytical results. The GC is calibrated using the external standard method, which involves multiple measurements directly from a standard gas sample (30 %-H2/10 %-CO/10 %-CH4/20 %-CO2/30 %-Ar) to establish a quantitative relationship between the concentration of the analyte and the instrument's response signal. This relationship is then applied to quantify unknown reaction tail gas samples. The MF controllers are recalibrated using a soap bubble flowmeter to verify gas flow rates. The soap film flowmeter is filled with soap solution and connected to the outlet where the gas flow rate is to be measured. After introducing the gas, a stopwatch measures the time taken for the soap film to rise from 0 to 50 mL, converting this time into gas flow rate in mL⋅min<sup>−1</sup> . To prevent contamination of the gas line, ensure the gas line maintains positive pressure and the soap solution level remains below the gas line to prevent the soap film solution from flowing into the gas line. 

### _2.4. Reactor theoretical limit calculation model_ 

To highlight the superior performance of MRs over CRs, this study employs the Gibbs energy minimization method previously used in Ref. [54] to calculate the maximum reaction performance achievable in CRs. This model disregards all kinetic factors, targeting the final state of each component in the reaction system to investigate the ultimate equilibrium state attainable by conventional reactors at a specified temperature. The primary components considered include: CH4, H2, H2O, CO, CO2, and Ar. 

Moreover, to investigate the performance limits of MRs, this study employs the one-dimensional ideal membrane reactor model used in Ref. [55]. The reaction process still assumes thermodynamic equilibrium, while the separation process is based on actual separation kinetics, neglecting radial mass transfer resistance (i.e., assuming complete radial concentration uniformity). For detailed computational procedures and principles, please refer to the previous works [54,55]. 

### **3. Results and discussion** 

### _3.1. Comparison between traditional reactor and membrane reactors_ 

To investigate the role of membrane separation and inserts in reactors and their potential for reducing reaction temperature demand, corresponding reaction tests were conducted within the permissible temperature range for the conventional reactor (CR), the original membrane reactor (O-MR), and the insert-enhanced membrane reactor (I-MR). Experiments were conducted under conditions of 400–600<sup>◦</sup> C, a methane flow rate ( _Q_ CH4) of 40 mL min<sup>−1</sup> , a steam-to-methane ratio ( _SMR_ ) of 3, atmospheric pressure at the reaction side outlet (1 bar), and vacuum extraction on the permeation side (2 Pa). Notably, experiments at 600<sup>◦</sup> C were not performed for MRs due to potential membrane structural damage at such high temperatures. Furthermore, thermodynamic equilibrium calculations based on _G_ min were introduced [54], while a one-dimensional ideal MR model neglecting heat and mass 

5 



<!-- Start of picture text -->
A Experiment: paam, MR (0) MR —O—CR B I-MR A—O-MR<br>Calculate: + {|CRG,., MR-limit scp os 100<br>100 a Equilibrium by G,,,<br>_ 5-0<br>S 1 aa 1<br>s 164.9% 2° ><br>: 80 aa & 98 3.9%!<br>a I ad = I<br>5 | ai ry I<br>‘a 60 a c<br>g oo 5 96<br>< ad I 4<br>8 40 Oo 1 ae 4<br>rl aad Qeya=40 mL-min? | = Qe4g=40 ML-min<br>- SMR=3 94 ova<br>20- a” P,.=1 bar Pre=1 bar<br>, 27.1% Pp=2 Pa Pe=2 Pa<br>0 92<br>400 450 500 550 600 650 700 400 450 500 550<br>Temperature T (2 ) Temperature T (fl )<br>Cc 200 -O--G_,,>0-MR —A— Gpin->I-MR Max drop AT: 199.18)<br>--O--CRSO-MR —\7—CRI-MR<br>a<br>+160 oO<br>3 a ai<br>= 120 Y oe<br>I wr wr<br>oOa ~73.7°C%| oy,it a<br>= 8 La<br>o ~52.6°C ae ae wat<br>Fe Oo Qeyg=40 mL-min<br>5 40r | a SMR=3<br>Q I Pe<br>E 1 oye P,e=1 bar<br>= 0 oO1 4? P..=2 Pa<br>450 500 550 600 650 700<br>Reaction temperature in CR T (fl )<br><!-- End of picture text -->



<!-- Start of picture text -->
7 ~ eo |<br>oeoy© Tooe<br>ye tS =<br>VC =e) QH HCO, =<br>MR (woo Boa Pe<br>Mt (GaSe , “<br>B Wings E:<br>AIF) 4|#\|/°<br>Triple helix insert “<br>Wyby y Y swirl flow<br><!-- End of picture text -->



<!-- Start of picture text -->
Arool aD,----- meee B ic<br>90 rom ata<br>O-.0. mee-6g<br>= 80 Oxon (average) _ 98<br>& +f “Tae. al = —_—<br>= 60 Insert: -free -enhance = 96 o.. eee<br>is) 5508 :- Oy > mee mA<br>4 , 5008:--O- “@- $ tia Sn<br>o. Dd 002 —o— a Insert: -free -enhance “too<br>Fa} “> 1 Relative increase 5502: --O--<br>20 SMR=3 “SS |~19.5% (average) oo SMR=3 5008 : --O-- —@—<br>p..=1 bar Pe Pre=lbar 4sog : --A-- —ae—<br>pr? Pa — Pce=2Pa 4008 : oe<br>0 se 90<br>20 40 60 80 100 20 40 60 80 100<br>CH, flow rate Qc, (mL-min”) CH, flow rate Qoyq (mL-min”)<br>Cc 100 co, CH, co H,<br>a<br>& 28% 26%<br>B 30<br>8 49%<br>5 60 80% geo<br>3<br>5<br>So 68% 72%<br>mo]<br>5 47%<br>= 20<br>oO<br>x 15% 4%<br>0 Ys ao oe. 2227p ~ 10% a<br>a<br>Temperature T (2 )<br><!-- End of picture text -->

_ 



<!-- Start of picture text -->
100 I-MR (solid line) As<br>Hi 9<br>T=500 8 3.2% __.-----27772 6.3%<br>x ae ae Pressure Pye: Poe<br>fo{= 70 O-MR (dash line) o 1.8 bar:. 2 Pa<br>2< 60 , —O——A—11.4bar: bar:2 2Pa Pa<br>c : 5.8%<br> ——8 40 21aaaa<br>+<br>S 30 T=400 8 os9<br>20 : 7.6%<br>10 Qcyq=60 mL-min™<br>2.4 2.6 2.8 3.0 3.2 3.4 3.6<br>Feed steam-to-methane ratio SWR<br><!-- End of picture text -->



<!-- Start of picture text -->
A Fluctuate: -4.1%~+1.2%] B 100<br>100 Py wwywwywywwwwrwywWwywwywWnary iY 4<br>x f As ZN Xe \A<br>= l QEPRCQEECEECEEHECHRGHECEESEEOSCHECAECOS oof rs 80F MP ARRAY<br>& 80P Fluctuate: -0.6%~+2.9%) = V<br>5 —— ee = 60F 8 —o-H Qeyg=40 mLmin”<br>2 60 Insert-free MR: o 1.4 bar: 1 bar j e —o— ; SMR=3<br>g5 " |O=14bar: 2 Pa! 2 ba T=5008<br>S Insert-enhanced MR: !—Ahepanemiee 1.4 anne bar:2 er ese Pa aee| 3e 40 —A— CH,= P,.=1.4 bar<br>s5 ORR Fluctuate: -4.3%~+6.7%| fo}8 Vv 2 peg=2 Pa<br>() PeeO4 GES ee Pe = = = = = = ES<br>= oy Qcua=40mL-min? | —6 20<br>SMR=3 _ O_O LEE ODPL.<br>T=500 © Ayo sGOCSeGOnESqCneasconsecqOlssecdesacHs<br>0 El 0 POOOOCCOOOCCOOOSCOOOSGOOOSCOOOSCOOOSCGO0O0O<br>0 5 10 15 20 a5 0 5 10 15 20<br>Cc Time (h) D Time (h)<br>100 101.0 Uo eoecececesecececeeetsesese<br>S 80 V “| = 100.0 !<br>2 2 99.5<br>S 60 H Qey4=40 mL-min™ 99.0<br>&26 —O— CO SMR=3= 98.5 Region 1 ''H  Region2 !‘H Region 3<br>25 h catalyst<br>= 40 —A— CH, BataibanT=500 e°0.20 1 ' ——<br>8 —7— CO, os ion<br>z P.o=2 Pa = 0.10<br>5 20 F 005<br>2 A o | 2 oool---------------. YN<br>i 0 LaerCIFEPO eeeewwywwwetwa SEES erewe yyw“Gren Ae AY Oy 23°g 7 fiH 1H<br>Deane eens eee Renee Serene -0.10 H H<br>0 5 a i i 7 0 100 200 300 400 500 600 700 800 900<br>Time (h) Temperature (°C)<br><!-- End of picture text -->

- - 



<!-- Start of picture text -->
Strict<br>10 or a Methane conversion<br>ee<br>Ov 95<br>“ Mori et al. 2007 [43] —*—'<br>Mild<br>8 = 80<br>=a 8 NakajimaChoi et etal. al.2022 2015[56] [42]~—— <— @<br>1s)<br>55 6 Chenetal. 2014 [57] — 65<br>e5 @ Bo<br>2<br>3 4 Sharma et al. 2021 [52] Hydrogen recovery<br>o (Methanol reforming)<br>= f 9599<br>2 This study<br>~ 83<br>79<br>75<br>0 71<br>350 400 450 500 550 67<br>Temperature (PI )<br><!-- End of picture text -->

_X.-Y. Tang et al._ 

_Energy 344 (2026) 140143_ 

temperature, high-efficiency hydrogen production. During continuous operation exceeding 25 h, performance fluctuation was only 4.1 % with no significant carbon buildup, demonstrating the reactor's operational stability. 

This study provides new insights into optimizing mass transfer processes through active insert design, thereby enhancing overall membrane reactor performance. Future work will focus on parameter optimization for helical configurations or other morphologies of inserts, along with extended-duration and more demanding application testing, to advance the reactor's next-stage development. 

### **CRediT authorship contribution statement** 

**Xin-Yuan Tang:** Writing – review & editing, Writing – original draft, Visualization, Validation, Software, Methodology, Investigation, Data curation, Conceptualization. **Jia-Chen Li:** Writing – review & editing, Writing – original draft, Visualization, Validation, Investigation. **ZhanBin Liu:** Writing – review & editing, Writing – original draft, Methodology, Investigation. **Sheng-Song Xia:** Writing – review & editing, Writing – original draft, Investigation. **Wei-Wei Yang:** Writing – review & editing, Writing – original draft, Supervision, Project administration, Funding acquisition, Formal analysis. **Ya-Ling He:** Writing – review & editing, Writing – original draft, Resources, Project administration, Funding acquisition. 

### **Declaration of competing interest** 

The authors declare that they have no known competing financial interests or personal relationships that could have appeared to influence the work reported in this paper. 

### **Acknowledgement** 

This work was financially sponsored by the National Natural Science Foundation of China (No. 52341601 and No. 52090063), the Postdoctoral Fellowship Program of CPSF under Grant Number (GZB20250165), and the Young Talent Support Plan of Xi'an Jiaotong University. 

### **Data availability** 

Data will be made available on request. 

### **References** 

- [1] UNITED NATIONS. Sustainable development goal 7: ensure access to affordable, reliable, sustainable and modern energy. U N Sustain Dev 2025. https://www.un. org/sustainabledevelopment/energy/. [Accessed 20 September 2025]. 

- [2] Rogelj J, Huppmann D, Krey V, Riahi K, Clarke L, Gidden M, et al. A new scenario logic for the paris agreement long-term temperature goal. Nature 2019;573: 357–63. https://doi.org/10.1038/s41586-019-1541-4. 

- [3] Tang XY, Yang WW, Liu Z, Li JC, Ma X. Deep learning performance prediction for solar-thermal-driven hydrogen production membrane reactor via bayesian optimized LSTM. Int J Hydrog Energy 2024;82:1402–12. https://doi.org/10.1016/ j.ijhydene.2024.08.073. 

- [4] Zainal BS, Ker PJ, Mohamed H, Ong HC, Fattah IMR, Rahman SMA, et al. Recent advancement and assessment of green hydrogen production technologies. Renew Sustain Energy Rev 2024;189:113941. https://doi.org/10.1016/j. rser.2023.113941. 

- [5] Guan D, Wang B, Zhang J, Shi R, Jiao K, Li L, et al. Hydrogen society: from present to future. Energy Environ Sci 2023;16:4926–43. https://doi.org/10.1039/ D3EE02695G. 

- [6] Yang WW, Ma X, Tang XY, Dou PY, Yang Y-J, He YL. Review on developments of catalytic system for methanol steam reforming from the perspective of energy-mass conversion. Fuel 2023;345:128234. https://doi.org/10.1016/j.fuel.2023.128234. 

- [7] Dang VH, Nguyen TA, Le MV, Nguyen DQ, Wang YH, Wu JCS. Photocatalytic hydrogen production from seawater splitting: current status, challenges, strategies and prospective applications. Chem Eng J 2024;484:149213. https://doi.org/ 10.1016/j.cej.2024.149213. 

- [8] Szablowski L, Wojcik M, Dybinski O. Review of steam methane reforming as a method of hydrogen production. Energy 2025;316:134540. https://doi.org/ 10.1016/j.energy.2025.134540. 

- [9] Gan Z, Dewangan N, Wang Z, Liu S, Tan X, Kawi S. Highly efficient and stable hydrogen permeable membrane reactor for propane dehydrogenation. J Membr Sci 2024;701:122724. https://doi.org/10.1016/j.memsci.2024.122724. 

- [10] Li Q, Zhang Q, Zhang L, Lang J, Yuan W, An G, et al. A comprehensive review of advances and challenges of hydrogen production, purification, compression, transportation, storage and utilization technology. Renew Sustain Energy Rev 2026;226:116196. https://doi.org/10.1016/j.rser.2025.116196. 

- [11] Farhana K, Shadate Faisal Mahamude A, Kadirgama K. Comparing hydrogen fuel cost of production from various sources - a competitive analysis. Energy Convers Manag 2024;302:118088. https://doi.org/10.1016/j.enconman.2024.118088. 

- [12] Hermesmann M, Müller TE. Green, turquoise, blue, or grey? Environmentally friendly hydrogen production in transforming energy systems. Prog Energy Combust Sci 2022;90:100996. https://doi.org/10.1016/j.pecs.2022.100996. 

- [13] Tang XY, Dou PY, Dai ZQ, Yang WW. Structural design and analysis of a solar thermochemical reactor partially filled with phase change material based on shape optimization. Sol Energy 2022;236:613–25. https://doi.org/10.1016/j. solener.2022.03.041. 

- [14] Ma W, Han W, Liu Q, Song X, Li J, Zhang N, et al. Hydrogen generation system with zero carbon emission based on synergistic conversion of methane and solar energy. Energy 2025;316:134609. https://doi.org/10.1016/j.energy.2025.134609. 

- [15] Bhattacharjee S, Linley S, Reisner E. Solar reforming as an emerging technology for circular chemical industries. Nat Rev Chem 2024;8:87–105. https://doi.org/ 10.1038/s41570-023-00567-x. 

- [16] Godoy V, Martín-Lara MA,<sup>´</sup> Garcia-Garcia G, Arjandas S, Calero M. Environmental impact assessment of the production of biomethane from landfill biogas and its use as vehicle fuel. Renew Energy 2024;237:121685. https://doi.org/10.1016/j. renene.2024.121685. 

- [17] Jain S, Kumar S. A comprehensive review of bioethanol production from diverse feedstocks: current advancements and economic perspectives. Energy 2024;296: 131130. https://doi.org/10.1016/j.energy.2024.131130. 

- [18] Gonçalves A, Puna JF, Guerra L, Campos Rodrigues J, Gomes JF, Santos MT, et al. Towards the development of syngas/Biomethane electrolytic production, using liquefied biomass and heterogeneous catalyst. Energies 2019;12:3787. https://doi. org/10.3390/en12193787. 

- [19] D'Adamo I, Ribichini M, Tsagarakis KP. Biomethane as an energy resource for achieving sustainable production: economic assessments and policy implications. Sustain Prod Consum 2023;35:13–27. https://doi.org/10.1016/j.spc.2022.10.014. 

- [20] Du Z, Liu C, Zhai J, Guo X, Xiong Y, Su W, et al. A review of hydrogen purification technologies for fuel cell vehicles. Catalysts 2021;11:393. https://doi.org/ 10.3390/catal11030393. 

- [21] Kumar R, Kumar A, Pal A. Overview of hydrogen production from biogas reforming: technological advancement. Int J Hydrog Energy 2022;47:34831–55. https://doi.org/10.1016/j.ijhydene.2022.08.059. 

- [22] Solowski G, Shalaby MS, Abdallah H, Shaban AM, Cenian A. Production of hydrogen from biomass and its separation using membrane technology. Renew Sustain Energy Rev 2018;82:3152–67. https://doi.org/10.1016/j. rser.2017.10.027. 

- [23] Saeidi S, Najari S, Hessel V, Wilson K, Keil FJ, Concepcion P, et al. Recent advances´ in CO2 hydrogenation to value-added products — current challenges and future directions. Prog Energy Combust Sci 2021;85:100905. https://doi.org/10.1016/j. pecs.2021.100905. 

- [24] Hafeez S, Al-Salem SM, Manos G, Constantinou A. Fuel production using membrane reactors: a review. Environ Chem Lett 2020;18:1477–90. https://doi. org/10.1007/s10311-020-01024-7. 

- [25] Masud MAA, Khuu NH, Sanyal O, Tian Y. Advances in membrane-assisted reactors: an integrative review for modeling and experiments. Sep Purif Technol 2025;371: 133095. https://doi.org/10.1016/j.seppur.2025.133095. 

- [26] Sun S, Li S, Wang S, Chen Y. Design and development of highly selective and permeable membranes for H2/CO2 separation—A review. Chem Eng J 2024;494: 152972. https://doi.org/10.1016/j.cej.2024.152972. 

- [27] Karki S, Hazarika G, Yadav D, Ingole PG. Polymeric membranes for industrial applications: recent progress, challenges and perspectives. Desalination 2024;573: 117200. https://doi.org/10.1016/j.desal.2023.117200. 

- [28] Cardoso SP, Azenha IS, Lin Z, Portugal I, Rodrigues AE, Silva CM. Inorganic membranes for hydrogen separation. Sep Purif Rev 2018;47:229–66. https://doi. org/10.1080/15422119.2017.1383917. 

- [29] Yuan Z, He G, Li SX, Misra RP, Strano MS, Blankschtein D. Gas separations using nanoporous atomically thin membranes: recent theoretical, simulation, and experimental advances. Adv Mater 2022;34:2201472. https://doi.org/10.1002/ adma.202201472. 

- [30] Bhowmick A, Koybasi HH, Ku C-E, Chen G, Hwang S, Zhang C, et al. Vacuumassisted carbon molecular sieve membrane reactor for non-oxidative ethane dehydrogenation. Chem Eng J 2025;518:164563. https://doi.org/10.1016/j. cej.2025.164563. 

- [31] Jung S, Sharafi SM, Lin JYS. Carbon dioxide hydrogenation to methanol: a performance comparison of water- and methanol-selective zeolite membrane reactors. Chem Eng J 2025;505:158835. https://doi.org/10.1016/j. cej.2024.158835. 

- [32] Wang W, Olguin G, Hotza D, Seelro MA, Fu W, Gao Y, et al. Inorganic membranes for in-situ separation of hydrogen and enhancement of hydrogen production from thermochemical reactions. Renew Sustain Energy Rev 2022;160:112124. https:// doi.org/10.1016/j.rser.2022.112124. 

- [33] Xue K, Hu Z, Li C, Wang M, Tan X, Wang Z, et al. Hydrogen production by glucose reforming using a nickel hollow fiber membrane reactor. J Membr Sci 2024;695: 122488. https://doi.org/10.1016/j.memsci.2024.122488. 

11 

_Energy 344 (2026) 140143_ 

_X.-Y. Tang et al._ 

- [34] Wang J, Yuan C, Li C, Geng G, Song J, Yang N, et al. Nickel-based metallic membranes for hydrogen production in membrane reactor: a brief overview. Sep Purif Technol 2025;358:130435. https://doi.org/10.1016/j.seppur.2024.130435. 

- [35] Al-Mufachi NA, Rees NV, Steinberger-Wilkens R. Hydrogen selective membranes: a review of palladium-based dense metal membranes. Renew Sustain Energy Rev 2015;47:540–51. https://doi.org/10.1016/j.rser.2015.03.026. 

- [36] Yang WW, Tang XY, Ma X, Cao XE, He YL. Synergistic intensification of palladiumbased membrane reactors for hydrogen production: a review. Energy Convers Manag 2025;325:119424. https://doi.org/10.1016/j.enconman.2024.119424. 

- [37] Jiang J, Dong Q, McCullough K, Lauterbach J, Li S, Yu M. Novel hollow fiber membrane reactor for high purity H2 generation from thermal catalytic NH3 decomposition. J Membr Sci 2021;629:119281. https://doi.org/10.1016/j. memsci.2021.119281. 

- [38] Yun S, Ted Oyama S. Correlations in palladium membranes for hydrogen separation: a review. J Membr Sci 2011;375:28–45. https://doi.org/10.1016/j. memsci.2011.03.057. 

- [39] Gallucci F, Fernandez E, Corengia P, van Sint Annaland M. Recent advances on membranes and membrane reactors for hydrogen production. Chem Eng Sci 2013; 92:40–66. https://doi.org/10.1016/j.ces.2013.01.008. 

- [40] Nayebossadri S, Speight JD, Book D. Pd-Cu-M (M = Y, Ti, Zr, V, Nb, and Ni) alloys for the hydrogen separation membrane. Acs Appl Mater Interfaces 2017;9: 2650–61. https://doi.org/10.1021/acsami.6b12752. 

- [41] Cerrillo JL, Morlan´es N, Kulkarni SR, Realpe N, Ramírez A, Katikaneni SP, et al. High purity, self-sustained, pressurized hydrogen production from ammonia in a catalytic membrane reactor. Chem Eng J 2022;431:134310. https://doi.org/ 10.1016/j.cej.2021.134310. 

- [42] Nakajima T, Kume T, Ikeda Y, Shiraki M, Kurokawa H, Iseki T, et al. Effect of concentration polarization on hydrogen production performance of ceramicsupported Pd membrane module. Int J Hydrog Energy 2015;40:11451–6. https:// doi.org/10.1016/j.ijhydene.2015.03.088. 

- [43] Mori N, Nakamura T, Noda K, Sakai O, Takahashi A, Ogawa N, et al. Reactor configuration and concentration polarization in methane steam reforming by a membrane reactor with a highly hydrogen-permeable membrane. Ind Eng Chem Res 2007;46:1952–8. https://doi.org/10.1021/ie060989j. 

- [44] Ji G, Yin X, Fu W, Kou X, Hotza D, Wang Y, et al. Enhancement of hydrogen clean energy production from greenhouse gas by in-situ hydrogen separation with a cobalt-silica membrane. J Clean Prod 2023;388:135874. https://doi.org/10.1016/ j.jclepro.2023.135874. 

- [45] de Nooijer N, Gallucci F, Pellizzari E, Melendez J, Pacheco Tanaka DA, Manzolini G, et al. On concentration polarisation in a fluidized bed membrane reactor for biogas steam reforming: modelling and experimental validation. Chem Eng J 2018;348:232–43. https://doi.org/10.1016/j.cej.2018.04.205. 

- [46] Wang J, Wang L, Shen Y, Shen L, Wang Y. Performance analysis and comparison of solar-driven membrane reactor with multi-membrane tubes for hydrogen production. Int J Hydrog Energy 2025;136:139–50. https://doi.org/10.1016/j. ijhydene.2025.05.064. 

- [47] Chompupun T, Limtrakul S, Vatanatham T, Kanhari C, Ramachandran PA. Experiments, modeling and scaling-up of membrane reactors for hydrogen production via steam methane reforming. Chem Eng Process Process Intensif 2018; 134:124–40. https://doi.org/10.1016/j.cep.2018.10.007. 

- [48] Barelli L, Bidini G, Gallorini F, Servili S. Hydrogen production through sorptionenhanced steam methane reforming and membrane technology: a review. Energy 2008;33:554–70. https://doi.org/10.1016/j.energy.2007.10.018. 

- [49] Sharma R, Kumar A, Upadhyay RK. Characteristic of a multi-pass membrane separator for hydrogen separation through self-supported PdAg membranes. Int J Hydrog Energy 2018;43:5019–32. https://doi.org/10.1016/j. ijhydene.2018.01.127. 

- [50] Tang XY, Yang WW, Ma X, He YL. Bionic leaf-inspired catalyst bed structure for solar membrane reactor aiming at efficient hydrogen production and separation. Appl Energy 2024;355:122281. https://doi.org/10.1016/j.apenergy.2023.122281. 

- [51] Wang H, Hao Y. Thermodynamic study of solar thermochemical methane steam reforming with alternating H2 and CO2 permeation membranes reactors. Energy Proc 2017;105:1980–5. https://doi.org/10.1016/j.egypro.2017.03.570. 

- [52] Sharma R, Kumar A, Upadhyay RK. Characteristics of a multi-pass membrane reactor to improve hydrogen recovery. Int J Hydrog Energy 2021;46:14429–40. https://doi.org/10.1016/j.ijhydene.2020.05.079. 

- [53] Ling YY, Wang HS, Liu MK, Wang B, Li S, Zhu X, et al. Sequential separation-driven solar methane reforming for H2 derivation under mild conditions. Energy Environ Sci 2022;15:1861–71. https://doi.org/10.1039/D1EE03870B. 

- [54] Tang XY, Zhang KR, Yang WW, Dou PY. Integrated design of solar concentrator and thermochemical reactor guided by optimal solar radiation distribution. Energy 2023;263:125828. https://doi.org/10.1016/j.energy.2022.125828. 

- [55] Tang XY, Yang WW, Ma X, Cao XE. An integrated modeling method for membrane reactors and optimization study of operating conditions. Energy 2023;268:126730. https://doi.org/10.1016/j.energy.2023.126730. 

- [56] Choi H, Kim SH, Bae J, Katikaneni SPR, Jamal A, Harale A, et al. CFD analysis and scale up of a baffled membrane reactor for hydrogen production by steam methane reforming. Comput Chem Eng 2022;165:107912. https://doi.org/10.1016/j. compchemeng.2022.107912. 

- [57] Chen Y, Mahecha-Botero A, Lim CJ, Grace JR, Zhang J, Zhao Y, et al. Hydrogen production in a sorption-enhanced fluidized-bed membrane reactor: operating parameter investigation. Ind Eng Chem Res 2014;53:6230–42. https://doi.org/ 10.1021/ie500294k. 

12 

