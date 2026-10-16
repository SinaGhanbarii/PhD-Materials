* 

a **Process Intensification of Hydrogen Production via Steam** x 

|**Methane Reforming with Palladium Membrane Technology**|
|---|



|**MINAS MOHAMMAD AL-RASHDAN**<br>AThesis Presented tothe<br>COLLEGEOFGRADUATEANDINTERDISCIPLINARYSTUDIES<br>KINGFAHDUNIVERSITYOFPETROLEUM&MINERALS<br>DHAHRAN,SAUDIARABIA|
|---|
|In Partial Fulfillment ofthe<br>RequirementsfortheDegreeof|
|MASTEROFSCIENCE|
|In|
|**CHEMICAL ENGINEERING**|
|**December 2024**|



II 

- © Minas Mohammad Al-Rashdan 

2024 

iii 

To the little girl I once was, 

iv 

# **ACKNOWLEDGMENTS** 

In the name of Allah, the Most Gracious, the Most Merciful, who has blessed me by turning my greatest dream into reality and allowing me to achieve success once again. 

I would like to express my deep gratitude to KFUPM, an iconic institution to which I have always felt a strong sense of belonging. My sincere thanks also go to my professors in the Chemical Engineering Department, especially Dr. Nayef Alsaifi, whose unwavering support from my very first day at university has been invaluable. 

I am also immensely grateful to my advisors, Dr. Usama and Dr. Medhat, and committee member Dr. Umer, for their unwavering encouragement throughout my research journey. Your insightful feedback, and continuous guidance, have enriched my academic experience. 

This thesis is dedicated to my father, an honorable man who has always done his utmost for me and continues to do so. To my mother, her prayers have been my greatest source of comfort and motivation, guiding me through every challenge. 

Words cannot express my gratitude to my devoted husband, Wathiq, who believed in me and provided all the support I needed. To my dear sons, Omar and Assil, thank you for your understanding and patience during this journey. 

To my little sister, Sham, who never stopped cheering me on. To my friend Reem, from whom I have learned so much, thank you for your wisdom and friendship. And to my friend Jana, thank you for your encouraging words from day one. 

v 

Lastly, I want to take a moment to thank myself. I stood strong for my dream, even though the hardest of times. I believed in myself when it mattered most, and I am proud of this journey I have taken. 

vi 

# **<u>TABLE OF CONTENTS</u>** 

|**ACKNOWLEDGMENTS ...................................................................................... V**|
|---|
|**TABLE OF CONTENTS .................................................................................... VII**|
|**LIST OF TABLES.................................................................................................. X**|
|**LIST OF FIGURES ............................................................................................... XI**|
|**LIST OF ABBREVIATIONS ............................................................................ XVI**|
|**LIST OF NOMENCLATURE ........................................................................ XVIII**|
|**ABSTRACT .......................................................................................................... XX**|
|**ملخص الرسالة ....................................................................................................... XXII**|
|**CHAPTER 1 INTRODUCTION .......................................................................... 1**|
|1.1 Background ................................................................................................................... 1|
|1.2 Motivation ..................................................................................................................... 4|
|1.3 Objectives ..................................................................................................................... 5|
|vii<br>**CHAPTER 2 LITERATURE REVIEW .............................................................. 6**|



|2.1 Global Demands on Energy .......................................................................................... 6|
|---|
|2.2 Hydrogen Energy .......................................................................................................... 9|
|2.2.1 Hydrogen Production Cost and Economy....................................................................................... 10|
|2.2.2 Environmental Impact..................................................................................................................... 12|
|2.3 Hydrogen Types .......................................................................................................... 13|
|2.4 Steam Methane Reforming ......................................................................................... 18|
|2.4.1 Catalyst........................................................................................................................................... 20|
|2.4.2 Reaction Kinetics............................................................................................................................ 20|
|2.5 Hydrogen Permeation Membrane Material ................................................................ 24|
|2.6 Membrane Reactor ...................................................................................................... 27|
|**CHAPTER 3 COMPUTATIONAL MODELING ............................................. 47**|
|**CHAPTER 4 MODEL VALIDATION AND SETUP ....................................... 51**|
|**CHAPTER 5 RESULTS AND DISCUSSION ................................................... 57**|
|5.1 Effect of sweep flow rate ............................................................................................ 66|
|5.2 Effect of Feed Pressure ............................................................................................... 71|
|5.3 Effect of Steam to Carbon Ratio ................................................................................. 75|
|5.4 Effect of Feed Flow Rates........................................................................................... 77|



viii 

|5.5 Effect of Flow Configuration ...................................................................................... 82|
|---|
|5.6 Effect of Membrane Tube Configuration ................................................................... 89|
|5.7 Effect of Shell Volume ............................................................................................... 94|
|**CHAPTER 6 CONCLUSIONS, RECOMMENDATIONS, AND**|
|**LIMITATIONS .................................................................................................... 99**|
|**APPENDIX [A]: REACTION RATE CODE .................................................. 101**|
|**APPENDIX [B]: HYDROGEN PERMEATION CODE ............................... 107**|
|**REFERENCES .................................................................................................. 112**|
|**VITAE ................................................................................................................ 119**|



ix 

# **LIST OF TABLES** 

|Table**1**: Merits and demerits of various hydrogen production methods. ........................... 2|
|---|
|Table**2**:  Current state and potential of hydrogen types in KSA [18]. ............................. 16|
|Table**3**: Experimental and modeling results of gas-based products, at 700 C, 1 bar, and 3<br>S/C, [28]. ............................................................................................................ 24|
|Table**4**:  Membrane materials and films with their properties. ........................................ 25|
|Table**5**:  Overview of experiments on membrane reforming reactors. ............................ 33|
|Table**6**: Summarized steam methane reforming Membrane Reactor modeling and<br>simulation Studies. ............................................................................................. 41|
|Table**7**: Numerical model validation results. ................................................................... 53|
|Table**8**: Performance comparison between steam methane reformer and membrane<br>reactor. ................................................................................................................ 59|



x 

# **LIST OF FIGURES** 

Figure **1** : Electricity production (in PWh) across OECD, Non-OECD, EU, and the World 

|[10]. ...................................................................................................................... 7|
|---|
|Figure**2**: Global electricity production from 2016 to 2021 [10]. .......................................... 7|
|Figure**3**: Electricity production by renewable energy from 2018 to 2021 [10]. .................. 8|
|Figure**4**:  KSA electrical energy production and consumption 2015-2022 [12]. ................. 9|
|Figure**5**: Greenhouse gas footprint level of different hydrogen types [17]. ....................... 15|
|Figure**6**: Schematic diagram of axis-symmetric tube and shell membrane reactor model. 50|
|Figure**7**: Cross-sectional view of shell and tubes MR in a square-pitch arrangement. ...... 50|
|Figure**8**:  Schematic diagram of the mesh used in the developed 2D axisymmetric model<br>............................................................................................................................ 52|
|Figure**9**: Comparison of experimental data and numerical results at different S/C ratios|
|[59] [61]. ............................................................................................................. 53|
|Figure**10**:  Results of the 2D Steam Methane Reformer Model at Different S/C ratios, 5|
|bar Pressure, and a temperature of 873 K. .......................................................... 55|
|Figure**11**: Results of the 2D Steam Methane Reformer Model at Different S/C ratios, 10|
|bar Pressure, and a temperature of 873 K. .......................................................... 56|
|Figure**12**: a) Schematic diagram of the MR mesh on the x-y-z axis, b) Mesh front view on<br>the x-z axis. ......................................................................................................... 58|
|Figure**13**: Geometries of membrane reactor (tube and shell) numerical domain. .............. 61|
|Figure**14**: The pressure profile along the reformer at (a) 5 bar, (b) 10 bar, and (c) 15 bar|
|feed pressure. ...................................................................................................... 62|
|Figure**15**: The temperature profile along the reformer. ...................................................... 62|



xi 

|Figure**16**: Species mole fraction on reformer side for Tube-12 mm MR at feed rate 1 × 10<sup>-</sup>|
|---|
|4kg/s of 3 S/C, 873 K, and 5 bar feed pressure. ................................................ 63|
|Figure**17**: Species mole fraction on reformer side for Tube-12 mm MR at feed rate 1 × 10<sup>-</sup>|
|4kg/s, 3 S/C, 873 K, and 10 bar feed pressure. ................................................. 64|
|Figure**18**: Species mole fraction on reformer side for Tube-12 mm MR at feed rate 1 × 10<sup>-</sup>|
|4kg/s, 3 S/C,  873 K, and 15 bar feed pressure. ................................................. 65|
|Figure**19**: Hydrogen flux rate along the membrane length for Tube-12 mm MR at feed rate|
|1 × 10<sup>-4</sup>kg/s, 3 S/C, and 873 K. Under 5,10, and 15 bar feed pressure.............. 66|
|Figure**20**: Effect of sweep flow rate on methane conversion on Tube-12 mm at different|
|reformer pressures, 3 S/C ratio, and 873 K. ....................................................... 67|
|Figure**21**: Effect of sweep flow rate on hydrogen recovery on Tube-12 mm at different|
|reformer pressures, 3 S/C, and 873 K. ................................................................ 68|
|Figure**22**: Effect of sweep flow rate on hydrogen selectivity on Tube-12 mm at different|
|reformer pressures, 3 S/C ratio, and 873 K. ....................................................... 69|
|Figure**23**: Mass flow rate of hydrogen at retentate outlet of Tube-12 mm for 0.0001 kg/s|
|feed flow rate, 873 K operating temperature, and different reformer pressure. . 70|
|Figure**24**: Mass flow rate of hydrogen at permeate outlet of Tube-12 mm for 0.0001 kg/s|
|feed flow rate, 873 K operating temperature, and 10 bar reformer pressure. ..... 71|
|Figure**25**: Effect of feed pressure on the performance of Tube-12 mm MR. Feed flow rate|
|1*E-4 kg/s, 3 S/C, and 873 K. ............................................................................ 72|
|Figure**26**: Hydrogen mole fraction on Tube-12 mm MR at feed rate 1 × 10<sup>-4</sup>kg/s, 873 K, 3|
|S/C, and different feed pressures. ....................................................................... 74|



xii 

Figure **27** : Mass flow rate of hydrogen at the Tube-12 mm outlets for 0.0001 kg/s  feed 

flow rate, 873 K operating temperature, and different feed pressure. ................ 75 

Figure **28** : Effect of steam to methane ratio on Tube-12 mm MR performance at 873 K, 10 bar feed pressure. ................................................................................................ 76 Figure **29** : Mass flow rate of hydrogen at the Tube-12 mm outlets for 0.0001 kg/s feed 

flow rate, 873 K operating temperature, and different steam-to-carbon ratios. . 77 Figure **30** : Effect of feed flow rate on Tube-12 mm MR performance, 3 S/C, 873 K, and 10 

bar. ...................................................................................................................... 79 

Figure **31** : Hydrogen mole fraction distribution on Tube-12 mm at different feed flow 

rates, under 10 bar feed pressure, 873 K, and 3 S/C. ......................................... 80 

Figure **32** : Mass flow rate of hydrogen at the Tube-12 mm outlets at 873 K operating 

temperature, 10 bar reformer pressure, and different feed flow rates. ............... 81 Figure **33** : Hydrogen flux rate along the membrane length for Tube-12 mm membrane 

reactor at different feed flow rates, at 10 bar feed pressure, 3 S/C, and 873 K. . 82 Figure **34** : Methane conversion on Tube-12 mm at 873 K, feed flow rate 1*10<sup>-4</sup> kg/s, and 3 

S/C, for co-current and counter-current flow configurations. ............................ 83 

Figure **35** : Hydrogen recovery on Tube-12 mm at 873 K, feed flow rate 1*10<sup>-4</sup> kg/s, and 3 

S/C, for co-current and counter-current flow configurations. ............................ 84 

Figure **36** : Hydrogen selectivity on Tube-12 mm at 873 K, feed flow rate 1*10<sup>-4</sup> kg/s, and 

3 S/C, for co-current and counter-current flow configurations. ......................... 85 

Figure **37** : Co-current and counter-current flow configurations hydrogen flux rate along the 

membrane length for Tube-12 mm MR at feed rate 1 × 10<sup>-4</sup> kg/s, 3 S/C, and 873 K. ........................................................................................................................ 86 

xiii 

|Figure**38**: Co-current and counter-current flow configurations mass flow rate of hydrogen|
|---|
|at Tube-12 mm outlets for 0.0001 kg/s feed flow rate, 873 K  operating|
|temperature, and different pressure. ................................................................... 87|
|Figure**39**: Hydrogen mole fraction distribution on Tube-12 mm for co-current and<br>counter-current flow directions under 10 bar feed pressure, 873 K, and 3 S/C.|
|.......................................................................................................................... 88|
|Figure**40**:  Methane conversion for the three MR configures. Reformer feed pressure of 5,|
|10, and 15 bar, temperature at 873 K, and 3 S/C. ............................................... 90|
|Figure**41**:  Hydrogen recovery for the three MR configures. Reformer feed pressure of 5,<br>10, and 15 bar, temperature at 873 K, and 3 S/C. ............................................... 91|
|Figure**42**: Hydrogen selectivity for the three MR configures. Reformer feed pressure of 5,|
|10, and 15 bar, temperature at 873 K, and 3 S/C. ............................................... 92|
|Figure**43**: Hydrogen flux rate along the membrane length for three MR configures at feed|
|rate 1 × 10<sup>-4</sup>kg/s, 3 S/C, and 873 K. .................................................................. 93|
|Figure**44**: Hydrogen mole fraction distribution for different MR configures under 10 bar|
|feed pressure, 873 K, and 3 S/C. ........................................................................ 94|
|Figure**45**: Methane conversion, Hydrogen recovery, and selectivity on Tube-10 mm,<br>Tube-12 mm, and modified Tube-12 mm, at 0.0001 kg/s feed flow rate, 873 K,|
|10 bar, and 3 S/C. ............................................................................................... 96|
|Figure**46**: Mass flow rate of hydrogen at the Tube-12 mm and Tube-12 mm modified<br>outlets for 0.0001 kg/s feed flow rate, 873 K operating temperature, and<br>different steam-to-carbon ratios. ........................................................................ 97|



xiv 

Figure **47** : Hydrogen flux rate along the membrane length for Tube-12 mm and Tube-12 mm modified MR configures at feed rate 1 × 10<sup>-4</sup> kg/s, 3 S/C, and 873 K. ....... 98 

xv 

# **LIST OF ABBREVIATIONS** 

|**CCS**|**:**Carbon Capture System|
|---|---|
|**CFD**|**:**Computational Fluid Dynamics|
|**DEN**|**:**Denominator term|
|**GCC**|**:**Gulf Cooperation Council|
|**GDP**|**:**Gross Domestic Product|
|**GHSV**|**:**Gas Hourly Space Velocity|
|**GW**|**:**Giga Watt|
|**HE**|**:**Hydroelectric Energy|
|**HTS**|**:**High-Temperature Shift Reaction|
|**LT**|**:**Low-Temperature Shift Reaction|
|**MR**|**:**Membrane Reactor|
|**NG**|**:**Natural Gas|
|**NE**|**:**Nuclear Energy|
|**POX**|**:**Autothermal Reforming|
|**POX**|**:**partial Oxidation|
|**PWh**|**:**Petawatt Per Hour|



xvi 

|**RDS**|**:**|The Rate-Determining Step|
|---|---|---|
|**Ren**|**:**|Renewable Energy|
|**S/C**|**:**|Steam To Carbon Ratio|
|**SMR**|**:**|Steam Methane Reformer|
|**TWh**|**:**|Terawatt Per Hour|
|**WGS**|**:**|Water Gas Shift Reaction|



xvii 

# **LIST OF NOMENCLATURE** 

𝝉⃗  ⃗⃗ :            Viscous Stress Tensor 𝒈⃗⃗ :            Gravitational Acceleration 𝒖⃗⃗ :             Velocity Vector 𝜺 :            Porosity 𝒑 :           Static Pressure 𝑺𝒊 : Source Term of Species 𝑖 𝝆𝒇 : Fluid Density 𝜷 : Porous Medium Resistance Coefficient 𝒉 : Enthalpy 𝒌𝒆 : Effective Thermal Conductivity 

𝑻 : Temperature 𝝆𝒄 : Solid Phase Fraction 

𝑹𝒋 : Chemical Reactions Rate for Reaction 𝑗 

∆𝑯𝒋 :           Enthalpy Change for Reaction 𝑗 𝒉𝒊 : Specific Enthalpy Species 𝑖 

𝒋𝒊 : Flux of Species 𝑖 

xviii 

|𝒎𝒊|:|Mass Fraction of Species𝑖|
|---|---|---|
|𝑴𝒊|:|Molar Mass of Species𝑖|
|𝑫𝒊,𝒆|:|Effective Diffusion Coefficient of Species𝑖|
|𝜶𝒊𝒋|:|The Stoichiometric Coefficient of Species𝑖in Reaction𝑗|
|𝑪𝟐|:|Inertial Resistance|
|𝟏<br>𝜶<br>|:|Viscous Resistance|
|𝒅𝒑|:|Diamer of Particle|
|𝐤𝐢|:|Reaction Rate Constant|
|𝛁|:|Gradient Operator|
|𝑷𝒊|:|Partial Pressure of Species𝑖|
|**_Ea_**|:|Reaction Activation Energy|



xix 

# **ABSTRACT** 

Full Name : Minas Mohammad Al-Rashdan 

- Thesis Title : Features of steam methane reforming and hydrogen separation in a shell-and-tube-designed Palladium-based membrane reactor for blue hydrogen production 

Major Field : Chemical Engineering 

Date of Degree : December 2024 

Hydrogen is a critical element in the global energy transition, offering a cleaner alternative 

to fossil fuels. Currently, steam methane reforming (SMR) is the most widely used technology for hydrogen production, accounting for over 90% of global supply. However, the SMR process produces significant carbon emissions, limiting its environmental benefits. To address this, integrating SMR membrane reactors (MR) has emerged as a promising solution for producing hydrogen that minimizes greenhouse gas emissions through carbon capture and separation. 

This study investigates the impacts of various operation and design parameters on hydrogen production in a membrane-based steam methane reformer (SMR) with a shelland-tube design. The catalytic bed on the shell side facilitates reforming reactions to produce hydrogen, and the membrane tubes are arranged in a square configuration to purify the produced hydrogen. A computational fluid dynamics (CFD) model of a nickel catalystpacked SMR was developed and validated against experimental data from the literature. Methane conversion and hydrogen recovery were analyzed across a range of conditions, including different pressures, membrane tube diameters, feed gas flow rates, and concentrations. The study also examines the impact of flow configurations—counter- 

xx 

current and co-current—on reactor performance. Ultimately, this research aimed to optimize SMR design and operation, providing insights into scalable industrial applications to enhance hydrogen production efficiency. 

The results demonstrated that introducing sweep flow enhances methane conversion and hydrogen recovery, although maximum methane conversion is observed when the sweep flow rate is equal to feed flow rate. Higher hydrogen recovery is observed when sweep flow exceeds the feed flow rate. Methane conversion decreased from 0.42 at 5 bar feed pressure to 0.29 at 15 bar, while hydrogen recovery and selectivity improved with pressure, reaching values of 0.12 and 0.14, respectively, at 15 bar. Higher feed flow rates led to lower methane conversion and hydrogen recovery due to decreased reaction time. Co-current flow outperforms counter-current flow in methane conversion. Larger tube diameter configure has the highest methane conversion, and smaller tube diameter configure has the highest hydrogen recovery and selectivity across all pressures. Increasing the shell volume increases hydrogen recovery and methane conversion, while the smaller shell volume increases the hydrogen selectivity. 

xxi 

# **ملخص الرسالة** 

ميناس محمد الرشدان: **السم الكامل** 

**.** ديوملا مكثفة لعمليات إنتاج الهيدروجين عبر إعادة تشكيل غاز الميثان بالبخار باستخدام تقنية غشاء البدراسة **عنوان الرسالة:** 

الهندسة الكيميائية **:التخصص** 

٤٢٠٢  كانون األول: **تاريخ الدرجة العلمية** 

،الهيدروجين عنصر أساسي في التحول العالمي للطاقة، حيث يقدم بديالً أنظف للوقود األحفوري. حاليًا ت عد عملية إعادة من٪ التكنولوجيا األكثر استخدامًا إلنتاج الهيدروجين، حيث يمثل أكثر من90تشكيل غاز الميثان بالبخار (SMR) العالمية للهيدروجين . ومع ذلك، ينتج عن عملية اإلصالح البخاري للميثان انبعاثات كربونية كبيرة، مما يحد اإلمدادات في عمليات اإلصالح البخاري للميثان كحلمن فوائدها البيئية. وللتغلب على ذلك، برز دمج مفاعالت األغشية (MR) واعد إلنتاج الهيدروجين مع تقليل انبعاثات الغازات الدفيئة من خالل التقاط الكربون وفصله. 

بتصميم غالف ي التشغيلية والتصميمية على إنتاج الهيدروجين(MR)الظروف  تتناول هذه الدراسة تأثيرات مختلف التفاعالت إلنتاج الهيدروجين. تم تطوير نموذج ديناميكا الموائعي جانب الغالفال فيمحفزة ال.انبوبي  ت سهل الحبيبات معبأ بمحفز النيكل وتم التحقق من صحته مقابل نتائج مخبرية .من األدبيات العلمية )SMR لمفاعل(الحسابية (CFD) تم تحليل تحويل الميثان واسترداد الهيدروجين عبر درجات حرارة وضغوط وأقطار أنابيب الغشاء ومعدالت تدفق على أداء المتعاكس والمتوازي-  التدفق- اتجاه  الدراسة تأثيروجدت  المختلفة. كماالميثان والبخار  وتركيزات مزيج وتقديم رؤى حول التطبيقات الصناعية القابلة ،)SMR المفاعل. هدفت هذه الدراسة إلى تحسين تصميم وتشغيل مفاعل( للتطوير لتعزيز كفاءة إنتاج الهيدروجين. 

الميثان واسترداد الهيدروجين، حيثتحويل  معدليعزز  لبخار الماء داخل أنبوب الغشاءوجود تدفق  أظهرت النتائج أن ء  مساوي لمعدل تدفق تغذية مزيج الميثان والبخار . ي الحظلبخار الما  يتحقق أقصى تحويل للميثان عند معدل تدفق عند ضغط لجتياح معدل تدفق التغذية. انخفض تحويل الميثان من0.42 استرداد أعلى للهيدروجين عندما يتجاوز تدفق **ا** بار، بينما تحسن استرداد وانتقائية الهيدروجين مع الضغط، حيث بلغت قيمهما0.12 عند15 بار إلى0.29 تغذية5 

xxii 

بار. تقل معدالت تحويل الميثان واسترداد الهيدروجين عند زيادة معدالت تدفق التغذية على التوالي عند15 و0.14 لنبوب، ومزيج الميثان والبخار في الغالف  لبخار الماء داخل **ا** بسبب تقليل وقت التفاعل. يتفوق التدفق المتوازي ذات األقطارباستمرار على التدفق المتعاكس في تحويل الميثان خاصة عند الضغوط العالية. أظهرت األنابيب الغشائية األنابيب الغشائية ذات األقطار األ صغر كان لديها اعلى بينماللميثان،  األكبر أداءً أفضل، حيث حققت أعلى تحويل وتحويل الميثان ، استرداد للهيدروجين وانتقائية عند جميع الضغوط. يزيد حجم الغالف األكبر من استرداد الهيدروجين بينما يزيد حجم الغالف األصغر من انتقائي ة.الهيدروجين 

xxiii 

# **CHAPTER 1** 

# **<u>INTRODUCTION</u>** 

## **1.1 Background** 

The rapid global population growth has significantly increased energy demand, encouraging the exploration of alternative energy sources to meet these needs. Recent research highlights hydrogen as a viable megawatt-scale alternative to fossil fuels, particularly for electricity generation. Various production methods, including electrolysis, partial oxidation, steam reforming, and biomass gasification, have demonstrated the capability to produce hydrogen on a conventional scale. 

Steam methane reforming (SMR) is one of the most efficient and widely used technologies for hydrogen production, mainly due to the abundance and affordability of natural gas. However, SMR releases significant carbon emissions, which contribute to greenhouse gases. Another method, partial oxidation (POX), involves producing hydrogen and carbon monoxide by reacting hydrocarbons with oxygen. Furthermore, combining POX with steam reforming in a single reactor produces the Autothermal Reforming (ATR) process. 

Hydrogen can also be produced via water electrolysis, a process in which an electrical current is used to split water molecules into oxygen and hydrogen. This method allows for hydrogen generation close to the point of use, avoiding the costs and energy demands of long-distance transportation. When powered by renewable energy sources, it results in zero 

1 

carbon emissions. Additionally, biomass can be converted into hydrogen and other byproducts through high-temperature gasification. 

Hydrogen is classified into different colors based on its production method and 

environmental impact. Some commonly recognized hydrogen colors include: 

- Grey-Hydrogen produced without carbon capture from conventional fuels, 

- Blue-Hydrogen with capturing carbon and storing it, 

- Green-Hydrogen uses sustainable energy sources 

- Pink-Hydrogen uses nuclear energy. 

**Table 1** highlights some hydrogen production methods' advantages (merits) and demerits. 

**Table 1: Merits and demerits of various hydrogen production methods.** 

|Ref.|Method|Merits|Demerits|Color|
|---|---|---|---|---|
|[1]|Steam Methane<br>Reforming (SMR)|Mature technology,<br>economically viable, high<br>efficiency|CO2emissions, fossil fuel<br>dependency|Grey, Blue|
|[2]|Partial Oxidation<br>(POX)|Variety of feedstocks,<br>simpler and faster than SMR|Lower hydrogen yield,<br>CO2emissions|Grey, Blue|
|[3]|Autothermal<br>Reforming (ATR)|Better thermal efficiency,<br>suitable for large-scale<br>production|Complex reactor design,<br>high capital investment|Grey, Blue|
|[4]|Electrolysis|Zero emissions if renewable<br>energy is used, pure<br>hydrogen|High electricity<br>consumption, expensive|Green,<br>Pink|
|[4]|Biomass Gasification|Renewable feedstock, waste<br>management|Lower hydrogen yield,<br>extensive pre-treatment<br>needed|Brown,<br>Grey|



2 

|[5]|Photo fermentation|Renewable feedstocks, low<br>energy requirement|Low hydrogen yield, not<br>commercially viable|Green (if<br>organic<br>waste)|
|---|---|---|---|---|
|[5]|Photoelectrochemical<br>Splitting|Direct solar to hydrogen<br>conversion, zero emissions|Still in the research phase,<br>low efficiency, high cost|Green|



Currently, hydrogen is primarily produced through various steam reforming processes, which account for approximately 90% of global hydrogen production, achieving up to 75% efficiency [6]. This makes the steam methane reforming process the second most efficient method, following electrolysis, which operates at around 80% efficiency [4], [7]. Among all production methods, steam methane reforming offers the most cost-effective way for hydrogen generation [4]. 

Methane is combusted in gas turbines or steam generators, producing less carbon dioxide compared to other fossil fuels used for power generation. In addition, converting methane into non-toxic hydrogen offers a cleaner fuel option with significant advantages in storage and transportation over traditional fossil fuels. Hydrogen combustion for electricity generation is a promising green energy source, delivering an energy yield up to 2.7 times higher than fossil fuels [4], Moreover, hydrogen combustion produces only water as a byproduct, unlike the direct combustion of methane, which releases carbon dioxide—a major greenhouse gas—into the atmosphere [7]. 

3 

## **1.2 Motivation** 

Steam methane reforming is considered the top practical method for hydrogen production, making it essential to study membrane reformers (MR) for potential future scale-up. The rising need for hydrogen as a green energy source and alternative fuel, along with its appeal for ammonia and methanol production, underscores the need for efficient SMR processes [8]. 

Operating conditions in membrane reformers, including temperature, pressure, and inlet steam-to-carbon (S/C) ratio, significantly influence reactant conversion, product yield, and hydrogen recovery rates. Investigating the impact of each parameter independently is crucial for optimizing the process and determining the ideal S/C ratio. The energy required for steam generation is another crucial factor in evaluating the net energy output and the overall efficiency of the SMR process. Additionally, ensuring complete methane conversion is vital to prevent methane leakage, which significantly contributes to greenhouse gas emissions. 

Current studies on membrane reformers for blue hydrogen production have focused on various operating conditions. However, limited research has examined how reactor design affects methane conversion across different input concentrations, temperatures, and pressures. Moreover, there is limited investigation into how reformer volume influences hydrogen flux rate. 

To address this gap, this study proposes optimizing the membrane reformer system by evaluating the advantages of sizing the reformer volume, particularly in the permeate zone. 

In the retentate zone, hydrogen permeation is restricted to a narrow region near the membrane’s surface, where operational factors like the S/C ratio have minimal impact on 

4 

this region’s width [9]. This research aims to bridge the existing knowledge gap and 

advance membrane reformer design to improve hydrogen production efficiency. 

## **1.3 Objectives** 

The specific objectives are: 

- Design an integrated shell-and-tube reformer membrane reactor system to produce blue 

hydrogen by steam methane reforming. 

- Develop a computational fluid dynamics (CFD) model that simulates the SMR process 

and hydrogen separation within the integrated reformer-membrane reactor system. 

- Validate the CFD model with data from the literature. 

- Analyze the effects of various factors, including flow configurations (counter-current and co-current), operating conditions (temperature and pressure), membrane tube diameter, tube pitch distance, and gas feed rates and concentrations on methane conversion and hydrogen recovery. 

- Propose a scalable and optimized reactor design for industrial applications, aiming to 

enhance performance and maximize hydrogen output. 

5 

# **<u>CHAPTER 2</u>** 

# **<u>LITERATURE REVIEW</u>** 

## **2.1 Global Demands on Energy** 

The usage of renewable energy sources has significantly increased due to the rise in 

worldwide energy demand. **Figure 1** illustrates global electricity generation trends. In 2020, the COVID-19 pandemic caused a drop in global electricity production, interrupting 

the steady rise observed in previous years. For instance, 22.8 PWh of electricity was generated in 2012, compared to 28.5 PWh in 2021. **Figure 2** shows the estimated contributions of various energy sources to global electricity output. Coal remains the dominant source of power generation worldwide, while nuclear and renewable energy sources account for a substantial share of electricity production, particularly in EU nations. [10]. 

The portion of renewable energy in electricity production worldwide has shown consistent growth over the years. In 2016, renewables contributed 7.4% of the global power output, rising to 12.8% by 2021. **Figure 3** illustrates the total electricity generated from various renewable sources, including wind, solar, biomass, geothermal, and others. Notably, solar energy production has experienced significant growth during this period. In non-OECD (Organization for Economic Cooperation and Development) countries, electricity generated from solar energy has doubled every four years, rising globally from 582.8 TWh to 1032.5 TWh. 

6 



<!-- Start of picture text -->
World Electricity Production<br>30<br>25<br>20<br>15<br>10<br>5<br>0<br>2012 2013 2014 2015 2016 2017 2018 2019 2020 2021<br>Year<br>OECD Non-OECD EU World<br>PWh<br><!-- End of picture text -->

**Figure 1: Electricity production (in PWh) across OECD, Non-OECD, EU, and the World [10].** 



<!-- Start of picture text -->
Electricity production by fuel from 2016 to 2021 in<br>the world<br>12000<br>10000<br>8000<br>6000<br>4000<br>2000<br>0<br>Oil NG coal NE HE Rcn. Other<br>Source<br>2016 2017 2018 2019 2020 2021<br>TWh<br><!-- End of picture text -->

**Figure 2: Global electricity production from 2016 to 2021 [10].** 

7 



<!-- Start of picture text -->
Electricity production by renewables sources<br>from 2018 to 2021<br>2000<br>1800<br>1600<br>1400<br>1200<br>1000<br>800<br>600<br>400<br>200<br>0<br>OECD Non-OECDD EU World<br>2018 2019 2020 2021<br>TWh<br>Wind Solar Other Wind Solar Other Wind Solar Other Wind Solar Other<br><!-- End of picture text -->

**Figure 3: Electricity production by renewable energy from 2018 to 2021 [10].** 

Oil and gas reserves, long regarded as the cornerstone of Saudi Arabia's energy sector, are 

among the nation's most abundant natural resources [10]. Saudi Arabia ranks second globally in terms of oil reserves and is a leading producer and exporter of oil. The Kingdom's economy is heavily reliant on the oil and gas sector, which accounts for 90% of export revenues, 70% of government revenues, and 50% of GDP [11]. Given these figures, the oil and gas sector plays a central role in shaping Saudi Arabia's economic and geopolitical influence. 

Both electricity production and consumption in Saudi Arabia have steadily increased in recent years. In 2019, the country generated 318.5 TWh of energy to meet a high demand of 80.4 GW. The majority of this electricity (90%) was produced using fossil fuels, primarily gas and oil. **Figure 4** illustrates Saudi Arabia's energy production and consumption trends from 2015 to 2022[12]. This continued reliance on fossil fuels 

8 

highlights the challenges the Kingdom faces in transitioning to more sustainable energy sources. 



<!-- Start of picture text -->
500<br>— 450 Production<br>338.5 k<br>ze Seonenein 3a9.6 360.5 © 368.7 376.5 388.8<br>3501 3107 3243<br>3300 _<br>2 306.9 318.5 «3256 333.7 .<br>© 250 os<br>° 259.9 .<br>g 200<br>r= 150<br>3<br>2 100<br>W 50<br>0<br>2015 2016 +=«2017 +=-2018»=— 2019S 2020S 2021 = 2022<br><!-- End of picture text -->

**Figure 4:  KSA electrical energy production and consumption 2015-2022 [12].** 

## **2.2 Hydrogen Energy** 

Hydrogen recently unfolded as a highly promising renewable energy source, primarily due 

to its potential to significantly reduce carbon emissions, contributing effectively to mitigating global warming and climate change. Hydrogen serves various purposes, including its role as an alternative to natural gas for household purposes and its use in numerous industrial applications. 

One of hydrogen's key advantages is its chemical properties, which facilitate renewable 

energy storage, making it a viable alternative to gasoline and diesel. It is considered a 

9 

versatile energy source that supports daily human activities and enhances modern living. However, since hydrogen gas is not naturally abundant, it is classified as an energy carrier rather than a primary energy source [12]. 

Hydrogen is increasingly regarded as the "fuel of the future" and a sustainable alternative to fossil fuels, reducing reliance on petroleum. This transition significantly lowers greenhouse gas and carbon dioxide emissions, particularly in transportation. Hydrogen boasts a high energy yield, with an efficiency of 2.75 times greater than conventional fossil fuels. Its energy conversion efficiency for transportation is also notable, exceeding gasoline by 2.5 times. 

Additionally, hydrogen helps alleviate environmental issues by reducing air pollution caused by carbon emissions from fossil fuels. Beyond its use as a transportation fuel, hydrogen can be converted into electricity when needed, making it a versatile energy solution. The growing interest in hydrogen-powered vehicles highlights its ability to store more energy compared to gasoline, positioning hydrogen as a cornerstone of sustainable energy innovation [12]. 

### **2.2.1 Hydrogen Production Cost and Economy** 

The global shift towards hydrogen as an energy source and environmentally clean fuel is gaining momentum. Unlike gasoline, which releases harmful gases when burned, hydrogen combustion results in water, which is harmless to the environment. However, for hydrogen to be truly environmentally friendly, the method to produce it must also have minimal environmental impact. 

10 

Hydrogen costs can be divided into two categories: direct and indirect. Direct costs refer to the expenses required to produce hydrogen, while indirect costs are associated with the negative environmental impacts of hydrogen use, such as air pollution, global warming, and climate change. [13]. Industries that emit gases contributing to these issues often face high costs due to their environmental impact. To mitigate this, a tax could be imposed on emissions that exceed permitted limits. Such taxes aim to make renewable energy more cost-competitive while potentially increasing the cost of fossil fuel-based energy generation. This approach encourages companies and societies to invest in renewable energy technologies. 

Based on the reviewed studies, electrolysis-produced hydrogen currently has the highest production costs. In comparison, hydrogen derived from Steam Methane Reforming (SMR) and SMR with carbon capture technologies is significantly cheaper, with electrolysis prices more than double those of SMR-based methods. While the costs of electrolysis are expected to decrease as technology improves, SMR and its variations will likely remain the lowest-cost options through 2050 [14]. This cost disparity is largely due to the established infrastructure and lower operational costs associated with SMR, as well as the current inefficiencies in electrolysis at scale. 

Currently, the cost of hydrogen production varies depending on the technology employed, with SMR costs around $2.4/kg, Carbon Capture and Storage (CCS) priced at $2/kg, and Electrolysis stands at $4/kg. However, by 2030, advancements in technology, economies of scale, and increased investment in hydrogen production infrastructure are expected to drive significant cost reductions. Projections indicate that the cost of SMR could drop to $1.28/kg, SMR with CCS to $1.95/kg, and Electrolyzed Hydrogen to $2.16/kg. These 

11 

developments highlight the growing potential for hydrogen to become a more accessible and cost-effective energy solution shortly [15]. 

### **2.2.2 Environmental Impact** 

Rapid population growth and urban expansion have driven a significant surge in global energy demand, prompting a global shift toward alternative energy sources to reduce reliance on conventional non-renewable resources such as fossil fuels and natural gas. Addressing the urgent need to decarbonize electricity generation and the transportation sector is a critical priority. 

Currently, over 100 technologies are employed for hydrogen production. Approximately 80% of these utilize steam conversion of fossil fuels, with 70% relying specifically on steam reforming of natural gas [12]. 

The environmental impact of hydrogen production largely depends on the methods and materials used in the process. Hydrogen produced from fossil fuels, which is currently the dominant method, significantly increases carbon dioxide emissions and has an environmental impact similar to that of directly burning fossil fuels. In contrast, hydrogen generated from renewable sources, such as solar energy, has no adverse environmental effects[13]. 

The SMR exhibited the most significant negative environmental impacts, making it the least favourable method in terms of global warming potential and gas emissions. SMR also recorded the highest abiotic depletion value, measured at 0.131 kg of anthracite equivalent, surpassing all other hydrogen production techniques. In comparison, the electrolysis 

12 

method ranked second, with an abiotic depletion value of 0.00786 kg of anthracite equivalent [16]. 

The SMR method had the most detrimental impact on ozone layer depletion, marking it as the worst contributor to ozone layer depletion. The SMR method recorded the highest carbon dioxide equivalent emissions, contributing approximately 12 kg [16]. 

## **2.3 Hydrogen Types** 

Hydrogen is categorized into different types based on the energy sources used for its production **Figure 5** . Green hydrogen is based on renewable energy and has a negligible greenhouse gas footprint. Pink hydrogen is derived from nuclear energy, also maintaining a minimal footprint. Yellow hydrogen is generated using grid electricity from mixed sources, resulting in a moderate greenhouse gas footprint. 

In contrast, hydrogen production from fossil fuels employs various technologies, including auto-thermal reforming, SMR, coal gasification, and pyrolysis. Blue hydrogen is produced using conventional fuels like coal and natural gas combined with CCS, resulting in low carbon emissions. Turquoise hydrogen, produced from natural gas, yields solid carbon as a by-product and achieves minimal to low carbon emissions. Hydrogen produced from lignite or black coal is named brown hydrogen and black hydrogen, which are associated with high greenhouse gas emissions. 

Additionally, hydrogen production through biomass gasification with CCS remains uncategorized but is considered to have a potentially negative greenhouse gas footprint. However, it offers the potential to reduce overall emissions [17]. 

13 

Saudi Arabia produces various types of hydrogen, including grey, blue, green, and turquoise, as detailed in **Table 2** . This table provides a comparative summary of hydrogen types, focusing on their production methods and environmental impacts based on the findings of [18]. 

14 



<!-- Start of picture text -->
Greenhouse<br>Feedstock/energy source gas footprint<br>aaa (Pe8ees eee)<br>t ) | ;<br>(Scapa) ; eteewable > Minimal !|<br>electricity ;<br>A Pink |_|\ Nicioar ? '<br>83° pees 1!i1 Minimal<br>é !<br>|{ t |<br>3 Yellow |_| Mixed origin grid i! !<br>ah mee an |<br>a<br>Autothermal reforming, steam Bue i? |<br>rc) methane reforming or coal hydrogen Low }<br>3 gasification + CCS el f \<br>3 ‘ | | Minimal to low |<br>io} Pyrolysis Lm (sold carbon |<br>I i |<br>rn \ | | as by product) ;<br>S| Autothermal reforming or Gan | |!<br>§ | steam methane reforming —>| hydrogen ! Medium |<br>8 |<br>: | it |<br>a Coal gasification a Brown coal (lignite) )-! High<br>I Pt |<br>t 1 ' |<br>oo<br>Coal gasification aBlack i Black coal i!t Highig '<br>. 1<br>Biomass ~ || 1|| Potentially |<br>gasification + CCS } Bass >) ¥ negative |<br>(Geeeseeoseeseee ..-....-.---<br><!-- End of picture text -->

**Figure 5: Greenhouse gas footprint level of different hydrogen types [17].** 

15 

**Table 2:  Current state and potential of hydrogen types in KSA [18].** 

|**Hydrogen Form**|**Current state and potential in KSA**|
|---|---|
|**Grey**|Saudi Arabia employs steam methane reforming in several processing<br>plants to produce grey hydrogen. However, this method is at odds with<br>the country’s sustainability goals, which aim to reduce carbon emissions.|
|**Blue**|With increasing investments in CCS technologies and abundant natural<br>gas resources, Saudi Arabia is well-positioned to lead in the production<br>of blue hydrogen. Initiatives such as the Saudi Carbon Capture and<br>Utilization Company and plans to develop the world’s largest carbon<br>capture facility demonstrate the country’s commitment to reducing<br>greenhouse emissions and advancing its sustainability goals.|
|**Green**|Saudi Arabia’s abundant solar resources and substantial investments in<br>renewable energy lay a strong foundation for green hydrogen production.<br>Although in its early stages, the country has potential for large-scale<br>production, driven by its ambitious renewable energy targets and<br>ongoing infrastructure development.|
|**Turquoise**|Saudi Arabia's substantial natural gas reserves and increasing investment<br>in renewable energy present potential for turquoise hydrogen. While still<br>in its early development and relatively costly, the country's established<br>renewable natural gas infrastructure underscores its strong positioning<br>for future advancements in this sector.|



16 

Grey and blue hydrogen are currently the most prevalent forms of hydrogen production in Saudi Arabia, mainly due to the nation's abundant natural gas reserves and reliance on nonrenewable energy sources. However, as the price of renewable energy drops and the kingdom steps up its attempts to lessen its carbon footprint, interest in green hydrogen is growing [18]. 

In the short to mid-term, the hydrogen economy in the Gulf Cooperation Council (GCC) region is expected to primarily depend on blue hydrogen, capitalizing on the region's abundant natural gas resources. However, with the anticipated decline in green hydrogen costs by 2030, the focus is likely to shift towards green hydrogen in the long term. This shift will leverage the GCC’s vast renewable energy potential, particularly solar and wind power, which positions the region to play a key role in the global transition to clean energy. 

The region boasts significant advantages, including expansive land availability, low-cost natural gas, and a strategic geographic location. Nevertheless, several challenges remain, such as heavy reliance on oil and gas revenues, limited involvement of the private sector, and low domestic hydrogen demand. Additionally, exporting hydrogen to markets like Europe may face obstacles due to high landing costs and potential regulatory hurdles, which could impact the competitiveness of the region's hydrogen exports. 

Despite these challenges, the hydrogen economy presents substantial opportunities for the GCC, including reducing carbon emissions, attracting investment, and generating employment. However, slow progress in transitioning and competition from faster-moving countries could threaten the region's potential leadership in the global hydrogen market 

[19]. 

17 

## **2.4 Steam Methane Reforming** 

Steam Methane Reforming SMR is a widely used method for producing hydrogen by breaking down methane gas into hydrogen and carbon monoxide. In the reformer, methane reacts with steam, which provides the required energy for the reaction. SMR offers several advantages over alternative methane reforming methods, such as being more energy efficient compared to dry methane reforming  [20]. 

During the process, natural gas methane, along with steam, is introduced into a preheated reactor at a temperature range of 700–900 °C. The endothermic reaction between CH4 and steam occurs over catalyst beds in a series of reactions. Keeping the high temperature required for the reaction typically involves supplying heat either by burning a portion of the methane feedstock or utilizing external heat sources such as electrical heaters or the combustion of auxiliary fuel. 

The resulting product stream is first cooled before entering the exothermic water-gas shift reactor, where CO reacts with H₂O to produce CO₂ and additional hydrogen. This shift process occurs in two stages: a high-temperature shift reaction at approximately 400 °C, followed by a low-temperature shift reaction at around 200 °C [7]. Finally, the hydrogen is purified in a separation unit. During the high-temperature stage, the reaction is driven by the elevated temperature, while the low-temperature stage allows for the further conversion of CO to CO₂, enhancing the overall hydrogen yield. Finally, the hydrogen is purified in a separation unit, where impurities such as CO₂ and CH₄ are removed to ensure the production of high-purity hydrogen. 

18 

Several parameters significantly influence the design of the SMR process, including pressure, temperature, inlet steam-to-methane ratio (S/C), and the physical properties of the catalyst. A thorough understanding of the impact of each variable on the steam reformer is crucial for optimizing hydrogen yield, achieving maximum methane conversion, and minimizing the energy required for the process. 

At low S/C ratios, excess methane and hydrogen produced during the reforming reaction proceed to the purification stage. During this stage, methane is combusted with oxygen to purify the hydrogen and generate additional heat. This heat is then recycled back to the main reactor, supported by an independent steam supply, to facilitate the conversion of fresh methane. At a reforming temperature of 1100 K and a pressure of 26.32 bar, an S/C ratio of 4 has been identified as the optimal stoichiometric ratio for high reforming temperatures [21] 

In molecular simulation studies based on equilibrium data [22], the effect of the steam-tocarbon (S/C) ratio on the SMR process was analyzed. It was observed that increasing the S/C ratio enhances the conversion rate of CH₄ and the yield of H₂. At an S/C ratio of 3 and a pressure of 1 atm, CH₄ conversion showed a linear increase with temperature. At 1073 K, the conversion rates were 89.25% for CH₄ and 91.97% for H₂O, with a H₂ yield of 2.7 mol/mol CH₄. The yield of CO₂ peaked at approximately 830 K before declining due to the exothermic nature of the water-gas shift reaction. 

The study also revealed that CH₄ conversion decreases exponentially with increasing pressure at 873 K and an S/C ratio of 3 [22]. Regarding inlet conditions, inlet pressure had a negligible effect on methane conversion, whereas raising the inlet temperature positively 

19 

influenced hydrogen yield. Conversely, an increase in the inlet flow rate led to a decrease in hydrogen production [21]. 

### **2.4.1 Catalyst** 

Nickel (Ni) is a widely used metal catalyst for the SMR due to its affordability compared to other commercial catalysts, high activity, and good resistance to coke formation. Ni/αAl₂O₃ is particularly preferred because it ensures a uniform temperature distribution during the chemical reaction [23]. The reactor's gas molecules encounter minimal resistance when diffusing to the nickel active sites, enabling the hydrogen reforming reaction to occur simultaneously across porous surfaces. Nickel's high activity even at lower temperatures allows for reduced reactor volume, lower heat input, and shorter gas-phase residence times. 

Nickel also offers excellent corrosion resistance, supported by its large pore structure, and remains stable with a long operational lifespan under high-temperature and oxidative environments [24]. In conventional SMR processes, a regeneration step is required after the catalyst reaches its mature operating time, as its activity diminishes due to fouling. This loss of activity is often caused by blockages from carbon dioxide and impurities in feedstock, such as sulfur [7]. 

### **2.4.2 Reaction Kinetics** 

The conversion rate of reactants to products in SMR relies on the concentration of reactants, pressure, and temperature. Typically, the rate-determining step (RDS) involves the reactions occurring at the active sites within the catalyst's pores [25]. In SMR, the process is governed by three primary global reactions (1), (2), and (3) that occur at the active sites, which are identified as the RDS. 

20 

Although methane reforming follows a more complex heterogeneous reaction mechanism involving up to twenty steps, these ultimately converge into the three main RDS. The simplest representation of SMR is an endothermic reaction occurring at 650–750 °C, driven by the thermal energy of steam. This process favors the forward reaction, increasing the yield of purified hydrogen [26]. Additionally, WGS a secondary step occurs at 200–400 °C (reaction 2). This reaction produces an additional hydrogen molecule and results in the formation of carbon dioxide, yielding a total of four hydrogen molecules. 













The rate equations for SMR were initially derived by Xu and Froment, incorporating a dimensionless parameter, DEN, which accounts for the reaction dynamics [27]. This 

21 

foundational study on SMR reaction kinetics, followed by the exothermic WGS reaction, remains a key reference in modern research. It effectively accounts for the effect of steam partial pressure on the reaction kinetics and the diffusion resistance of reactant molecules toward the catalyst's active sites [28]. 

To determine rate constants and activation energies, experiments are conducted using a preheated tubular reactor loaded with Ni/MgAl₂O₄ catalyst particles (0.18–0.25 mm) containing 15.2% nickel. These experiments involve reforming reactions at varying temperatures and pressures, enabling measurement of reactant and product concentrations over time. This setup ensures sufficient activation of the catalyst for optimal reaction performance. 

During the initial 24 hours of operation, the catalyst experienced rapid deactivation due to sulfur contamination in the feedstock. Sulfur reacted with steam to produce H₂S, which blocked active sites on the catalyst surface [7]. Additionally, carbon accumulation further inhibited catalytic activity. Measurements were recorded after 70 hours, once catalyst deactivation became negligible and its activity stabilized. 

To regenerate the spent catalyst, conditions for the reverse water-gas shift reaction were calculated, reducing the temperature to 573–673 K, as the overall reforming reaction is endothermic. For modeling methanation and the reverse water-gas shift reaction, the catalyst activity factor was adjusted to 1.225 to account for carbon accumulation from previous use. For a fresh catalyst, the estimated parameters were scaled by a factor of 2.246 [27]. 

22 

Computing the results with the three rates equation to numerically estimate the reaction rate parameters (k). Further, using the Arrhenius equation Eq (8), and the estimated parameters to find the reaction activation energy at the reference temperature [27]. The stoichiometry of the reaction and the catalyst used affect the reaction activation energy. 



An experiment was conducted using a Ni/MgAl₂O₄ catalyst with 18 wt % nickel, applying the kinetic model developed by Xu and Froment, widely regarded as one of the most comprehensive models for SMR [28]. Data were collected from 100 points along an adiabatic axial plug flow reactor, assuming no concentration or temperature gradients in the radial direction, no temperature variations within the catalyst particles, and constant porosity throughout the reactor. 

A preliminary experiment was performed under fixed reaction conditions, varying only the particle diameter to determine the minimum size required to minimize diffusion limitations. At smaller catalyst particle sizes, the effectiveness factor approached unity. For a particle diameter of 0.2 mm, the effectiveness factor was determined to be 0.92. 

The main experiment was conducted using 0.2 mm catalyst particles across a temperature range of 550–700 °C for SMR and 300–375 °C for WGS reaction. Experimental results were compared with data generated by a model-building program, achieving an accuracy of 95%, as summarized in **Table 3.** 

23 

**Table 3: Experimental and modeling results of gas-based products at 700 C, 1 bar, and 3 S/C, [28].** 

|Gas|Experimental data %|Modeling data%|
|---|---|---|
|Methane|7.6|5.4|
|Carbon monoxide|47|49.8|
|Carbon dioxide|45.5|44.8|



Far from the equilibrium conditions of 3 S/C, 700 °C, and 1 bar, methane undergoes complete conversion. At equilibrium, increasing the S/C ratio results in higher methane conversion. However, an optimal feed ratio is required to achieve the best conversion while minimizing the energy needed to generate steam. Experimental results indicate that increasing the operating pressure decreases methane conversion, which aligns with the reaction stoichiometry, where two moles of reactants produce four moles of products [28]. 

## **2.5 Hydrogen Permeation Membrane Material** 

Hydrogen-permeable membranes play a critical role in membrane reactors, particularly in the production of blue hydrogen. These membranes enable the selective separation of hydrogen from gas mixtures, allowing for the purification and recovery of hydrogen at high concentrations. The choice of membrane material significantly influences the overall efficiency, performance, and stability of the membrane reactor. Numerous membrane materials have been developed and tested for hydrogen permeability, each offering distinct advantages and limitations. **Table 4** below outlines various membrane materials and their properties. 

24 

**Table 4:  Membrane materials and films with their properties.** 

|**Material**|**Description**|
|---|---|
|**Palladium-**<br>**Based**<br>**Membranes**|PD or Palladium and its alloy are considered a great standard for H2<br>permeation because of their exceptional selectivity and permeability to<br>hydrogen. Pd membranes operate based on a solution diffuses mechanism,<br>where hydrogen dissociates into atoms on the surface, consequently, diffuses<br>via the metal lattice, and then combines again on the other side. This<br>mechanism allows for nearly 100% hydrogen selectivity. However, the<br>popularity of palladium films is limited for several reasons, the most<br>important of which is their high cost, their vulnerability to poisoning by<br>impurities; for example, sulfur and CO, and problems with long-term stability<br>which is encountered at elevated temperatures.[29].|
||These membranes operate through a proton conduction mechanism, where<br>hydrogen ions are conducted through the ceramic lattice, materials like|
|**Ceramic**|BaCeO3 and doped zirconia have been extensively studied for this purpose.|
|**Membranes**|There are many advantages to using this material, like high thermal stability<br>and high chemical stability, resistance to poisoning, and the aptitude to work<br>at elevated temperatures [30].|
|**Metal Organic**<br>**Frameworks**<br>**(MOF)**|MOFs have emerged as a promising category of materials for hydrogen<br>separation because of their tenable pore sizes, high surface areas, and the<br>ability to incorporate functional groups that enhance hydrogen selectivity.<br>When used thin films or coatings on other membrane materials. For example,|



25 

||MOFs based on zinc, copper, and Zirconium have shown promising hydrogen<br>permeation properties. Challenges like stability under operating conditions<br>and the need for further optimization of hydrogen selectivity remain areas of<br>improvement[31].|
|---|---|
|**Membrane film ty**|**pes for hydrogen purification:**|
|**Porous Ceramic**<br>**membranes**|Porous Ceramic membranes made from materials like alumina, silica, and<br>titania provide an alternative to dense metal films. These types of membranes<br>operate through a molecular sieving mechanism, whereas the pore size is<br>tailored to selectively allow the passage of hydrogen while blocking larger<br>gas molecules. The main benefit of this type is resistance to high temperatures<br>and chemical inertness that leads to making them suitable for demanding<br>applications in hydrogen purification[32].|
||They are composed of Pd or its alloys and have high permeability. These films<br>are fabricated by different techniques like sputtering, chemical vapor|
|**Dense Metal**<br>**films**|deposition, and electroplating. These types of films provide complete<br>hydrogen selectivity, but their application is limited due to the high cost and<br>the need for protective layers to prevent degradation in harsh environments<br>[33].|
|**Mixed matrix**<br>**membranes**|They represent a hybrid approach, integrating the advantageous properties of<br>both polymeric and inorganic materials. Inorganic fillers such as Silica<br>nanoparticles are dispersed within a polymer matrix, resulting in a membrane|



26 

that exhibits enhanced hydrogen permeability and selectivity. The selection of polymer and inorganic fillers has a considerable role in defining the performance of mixed matrix membranes. Polymers with high hydrogen solubility and diffusivity like polyimides are commonly used for hydrogen purification. This type of membrane provides a balance between cost, performance, and scalability [34]. 

## **2.6 Membrane Reactor** 

The last step in hydrogen production is to purify the hydrogen from the product mixture employing typical separation methods like pressure swing adsorption, distillation, membrane separation, and liquid absorption. This separation unit consumes plenty of energy and results in a loss of a portion of the final hydrogen production rate, which increases the total production cost and process efficiency. A lower-cost hydrogen generation process that minimizes the number of processing steps and merges hydrogen purification with the reforming reaction stage using a membrane reforming reactor (MR). In a double-tube reactor or a multi-tube-shell system, one side is assigned to a reformer porous zone and the other to a permeate zone where the adjoining micro thin wall is infinitely selective for hydrogen membrane [35]. Pure steam at an adjusted flow rate enters the permeate zone as sweep flow that can be condensed later to recover hydrogen. The no sweep flow MR isn’t improving the reforming of the SMR [35]. The co-current flow direction leads to a higher H2 permeation flux rate when compared to the counter-current type [9]. 

27 

A porous ceramic and palladium film coating membrane is an inorganic palladium-based membrane, which does not produce an oxide layer. The metal on the membrane enhances H2 permeability and mechanical strength with no loss of selectivity [36]. Hydrogen flows across the membrane as a result of the differences in the H2 partial pressure between the two sides. The pressure gradient between the retention zone and the permeation zone. As hydrogen is continuously disposed of from the reformer zone, the reaction equilibrium shifts forward and increases the methane conversion; therefore, the methane conversion required by SMR can be achieved at lower temperatures using MR[36]. 

The process in which H2 flows toward the permeate zone from the retentate zone depends on the H2 partial pressure on both sides plus the operation temperature based on Sievert’s Law, the H2 flux unit is mol/m<sup>2</sup> /s as given in equation 9. 



Where; 

- 𝛿𝐻2 Is the membrane thickness (10<sup>-6</sup> m in this case), 





- 𝑃𝐻2𝐹.𝑆And 𝑃𝐻2𝑝.𝑆 Denote the partial pressure of H2 on the retentate zone and permeate 

zone, respectively. 

For MR as reformer pressure rises, methane conversion decreases. However, a rise in reformer pressure causes a greater partial pressure difference of hydrogen, which increases hydrogen permeation. Additionally, as the flow rate of the reactants increases, the rate of 

28 

methane conversion drops. CH4 conversion is increased when the S/C value is high at a lower input flow rate. However, the H2 flux through the membrane's ability is limited with no sweep flow case, even if greater S/C and low feed flow rates may cause more hydrogen to develop in the reforming zone [35]. 

**Table 5** summarizes experiments recorded in the literature on fixed bed catalytic membrane methane reformer reactors. Experiments on a Pd-Ag membrane reactor were conducted at different pressures and temperature ranges. At equal reformer and permeate sides pressure, methane conversion remained above 50% with a hydrogen selectivity of 80%. The difference in pressure of 4.0 bar between the reformer and permeate portions resulted in 65% conversion of CH4 and 80% recovery of H2. The results mean that maintaining a higher-pressure difference between the reformer and permeate zone improves CH4 conversion and H2 recovery [37]. Another study investigates Pd-MR to evaluate the impact of operational conditions on CH4 conversion, H2 recovery, and carbon selectivity [38]. At 773 K, methane conversion rose from 67.6% at 300 kPa to 88.7% at 900 kPa, while CO selectivity dropped from 6.1% to 2.3%. The higher reaction pressure also enhanced hydrogen recovery, with the rate increasing from 71.0% at 300 kPa to 91.8% at 900 kPa at 773 K. CH4 conversion changed from 98.6% to 86.0% as GHSV went from 4000 to 8000 at 823 K and 900 kPa. CO selectivity increased with higher GHSV, from 2.4% at 4000 to 6.3% at 8000. CH4 conversion improved with an increasing S/C ratio, peaking at 99.0% for an S/C of 3.5. However, H2 recovery decreased from 97.5% to 94% with the same S/C increase due to dilution effects. CO selectivity also decreased with higher S/C, from 6.5% at S/C of 2.5 to 2.4% at S/C of 3.5. Methane conversion increased significantly with the 

29 

use of sweep gas. Without sweeping gas, conversion was 64.0%, which improved to 84.6% with a sweep ratio of 1.7 [38]. 

A test on an industrial plant scale MR plant was set to enhance hydrogen production from syngas feed [39]. The reformer operated within the 550–650 °C range within four membrane types, Hydrogen permeability, and flux showing variations in performance based on the type of membrane and operating conditions. A total reactant conversion of 57.3% was at 600 °C, about 26% more than conventional reformers at the same temperature. The MR effectively reduced the required thermal level for reforming, enhancing overall efficiency and reducing greenhouse gas emissions. Experiments on MR at low-pressure operations (1-3 bar) refer to small-scale power generation units [40]. A palladium-based MR was analyzed versus a fixed bed reactor (FBR). The MR significantly outperformed the FBR in terms of the conversion of CH4 and H2 purity. At 450 °C and 3.0 bar, CH4 conversion in the MR was approximately 50%, while the FBR achieved only 6%. 

The performance and stability of the membrane reactor over long durations, up to 1100 hours was studied under varying feed pressure, operating temperature, and GHSV [41]. hydrogen recovery and methane conversion were recorded for long-term performance. Methane Conversion was 98% at reactants inlet pressure which was about 28 bar and a 580 °C temperature compared with an equilibrium conversion of 26% at the same conditions. Hydrogen purity on the permeate side ranged from 80% to 95%, with recovery rates between 60% and 80%. Higher feed pressures led to higher H2 purity and recovery. In longterm tests, the MR showed stability performance with an average CH4 conversion of approximately 86% over 1100 hours. While a decrease in H2 purity over time was recorded, due to leak flow and membrane selectivity reduction [41]. 

30 

To overcome the endothermic nature of the MSR process, Pd membrane reactors were tested at lower temperatures, around 500°C, due to the ongoing removal of H2, which shifts the equilibrium toward the product. The use of MR significantly enhances conversion efficiencies and reduces CO production at lower temperatures compared to conventional methods [42]. 

A honeycomb monolith MR design was proposed to study MR scale-up for industrial hydrogen production [43]. Methane conversion increases with feed pressure on the MR, also methane conversion increases with temperature and S/C ratio. Scaling up requires a proportional increase in membrane surface area for hydrogen separation. Insufficient membrane area limits hydrogen permeation and reactor performance. Raising the reactor size without increasing the membrane area reduced the MR performance [43]. 

Gas permeation test carried out at 773 K and 31.4 kPa of pressure difference between retentate and permeate sides in a tubular Pd-Ru MR [44]. the hydrogen permeation rate is around 0.1050 mol / m<sup>2</sup> .s. The MSR reaction was under temperature 773 K and pressure 100-250 kPa, gas hourly space velocity (GHSV) 837 h−1, and S/C of 3. The SMR reaction result showed that methane conversion increased with increasing pressure difference and reached 77.5% at 250 kPa[44]. 

The reforming of natural gas for hydrogen production was tested on Pd-Au MR [45]. Methane conversion was 48% for pure methane and 37% for natural gas at 300 kPa. The presence of higher hydrocarbons in natural gas reduced methane conversion, but it led to higher total hydrogen production. This was due to the higher hydrocarbon components, such as ethane (93%), propane (92%), and butane (83%). Hydrogen recovery was higher 

31 

for natural gas, benefiting from the additional hydrogen produced from these heavier hydrocarbons [45]. 

The Pd-Au MR with no sweeping gas in the membrane side was studied under 2.8 MPa pressure on the reformer side for a temperature range [47]. Methane conversion reached up to 94% at 511°C, far surpassing the equilibrium limit of 30% on SMR under similar conditions. Hydrogen purity consistently exceeded 99.2%, with flux stability maintained throughout a 530-hour test [47]. 

The performance of the membrane reactor (MR) for hydrogen production was evaluated using various hydrocarbon feedstocks, including methane (CH₄) and pre-reformed naphtha (PRN). The tests were conducted under a feed pressure range of 15 to 30 bar [46]. Methane conversion increases with pressure increases on MR and decreases on PRN. Operating at 30 bar, it achieved methane conversions of 91% with CH₄ and 65% with PRN, surpassing the equilibrium conversion limits of conventional reactors. The hydrogen produced maintained a high purity of over 98.5% throughout the testing period. The system also facilitated cost-effective carbon dioxide capture, with CO₂ concentrations in the retentate stream reaching 76 mol% [46]. 

32 

**Table 5:  Overview of experiments on membrane reforming reactors.** 

|**Ref**|**Reactor**|**Catalyst**|**Sweep gas**<br>**flow**|**Experimental**<br>**conditions**|**Results**|
|---|---|---|---|---|---|
|[37]|Pd-Ag MR|Ni-ZrO|- Nitrogen<br>- co-current|- 450°C<br>- Constant total<br>pressure on<br>retentate and<br>permeate sides<br>- Variables<br>permeate pressure<br>(feed at 9.0 bar,<br>permeate 5.0-9.0<br>bar)<br>- H2rich gas<br>mixtures|- Constant pressure:<br>>50% conversion, ~80%<br>H2selectivity.<br>- Variables permeate<br>pressure: ~65%<br>conversion at 4.0 bar<br>pressure difference, 80%<br>H2recovery.|
|[38]|Pd MR|Nickel-<br>based|- Argon<br>- (0 to 3.4)<br>ratio to Feed<br>flow.|- 773, 823 K<br>-300 to 2000 kPa<br>- 2.5 to 3.5 S/C<br>- 4000 to 8000<br>GHSV|- Higher temperatures<br>and pressures up to 900<br>kPa increase CH4<br>conversion and H2<br>recovery.|



33 

||||- Counter-<br>current, and<br>co-current||- CH4conversion<br>increases with pressure<br>up to 900 kPa, then<br>stabilizes.<br>- CH4conversion<br>decreases with higher<br>GHSV|
|---|---|---|---|---|---|
||||||- Higher S/C ratios<br>increase CH4conversion|
||||||- H2recovery decreases<br>at high S/C.|
||||||- Sweep gas improves<br>CH4conversion up to a<br>sweep ratio of 1.7.<br>- A higher H2recovery at<br>counter-current sweep<br>gas|
||Four types|Noble metal|- Steam and|- Natural gas and|- Varying performance|
|[39]|of Pd-<br>based or<br>Pd-Ag|catalyst<br>(Rh–Pt)|H2|steam feed<br>- 550–650 °C and|based on membrane type<br>and conditions|



34 

||alloy<br>membranes|||- Up to 20 bar|- Effective operation<br>within 550–650 °C,<br>good thermal<br>management.<br>- 57.3% at 600 °C, 26%<br>more than conventional<br>reformers at the same<br>temperature|
|---|---|---|---|---|---|
|[40]|Pd-Ag MR|Ni/Al₂O₃|- Nitrogen<br>-Sweep factor<br>(SF) of 1.2.|- 400-500°C<br>-1.0-3.0 bar<br>- S/C 2<br>-GHSV of 3710 h⁻¹|- CH4Conversion 50%<br>at 450 °C and 3.0 bar in<br>MR and 6% conversion<br>in FBR under the same<br>conditions.<br>- H2Recovery of 70% at<br>450 °C and 3.0 bar with<br>SF of 1.6 in MR.|
|[41]|Pd MR|Nickel-<br>based|- Nitrogen<br>-Co-current<br>- 0.05 to 0.1<br>L/min.|- 550 °C to 580 °C<br>-12 to 28 bar<br>- GHSV: 760 to 950<br>(L. h<sup>−1</sup>/ kg catalyst)|- Membrane selectivity<br>for H2decreased after<br>long use time<br>- H2flux remained<br>constant|



35 

|[42]|Pd MR|Nickel-<br>based|-1 atm<br>- Nitrogen<br>-100-500<br>ml/min|- 500 °C<br>- 9-20 atm<br>- S/C 3|- CH4conversion: >80%<br>at 500 °C<br>- CO yields less than 2%<br>in MR reactor vs up to<br>50% in conventional<br>FBR|
|---|---|---|---|---|---|
||Pd-MR|Ni/Al₂O₃|No sweep gas|- 773–873 K.<br>- 300–500 kPa.<br>- S/C: 3–5|- CH4conversion<br>(87.1%) on MR<br>compared to (61.5%) on<br>SMR|
|[43]|||||- optimal membrane<br>surface area-to- reformer<br>volume ratio (S/V = 255<br>m²/m³) to balance<br>hydrogen separation and<br>reaction efficiency|
|[44]|Pd-Ru MR|Ni/Al₂O₃|No sweep gas|- 773 K<br>- 100 – 250 kPa<br>- GHSV: 873 h<sup>-1</sup><br>- S/C 3|After 100 h methane<br>conversion and the<br>hydrogen yield remained<br>constant.|



36 

||Pd-Au MR|Nickel-<br>based|- Steam<br>- 100 ml/ min<br>- 100 kPa|- 450 °C<br>- 100 – 300 kPa<br>- GHSV: 873 h<sup>-1</sup>|- Higher methane<br>conversion than natural<br>gas under the same<br>conditions|
|---|---|---|---|---|---|
|[45]||||- S/C 3.5|-The reactor achieved<br>100% hydrogen purity<br>without coke formation,<br>maintaining stability for<br>over 1000 hours.|
||Pd-Au MR|Ru/Al₂O₃|- No sweep<br>gas|- 2.8 MPa<br>- 480°C to 580°C|- Stable hydrogen flux<br>and methane conversion|
|[47]|||-1 atm|-S/C 3|over time.<br>- Hydrogen purity above<br>99.2% after 530-hour|
|[46]|Pd-Au MR|R-88(R)-<br>HEAT-X™<br>(commercial<br>catalyst)|-Hydrogen<br>- 3 bar|- 15-30 bar<br>- 550 °C<br>-S/C 4<br>- GHSV: 976 h<sup>-1</sup>|- Hydrogen purity 98.5<br>at 30 bar, and 99.2% at<br>15 bar<br>- Membrane maintained<br>high stability after 400+<br>hours|



37 

Theoretical investigation studies of MR for hydrogen production techniques using modeling and simulation of membrane reactors are summarized in **Table 6** . A membraneintegrated reformer reactor was examined in a CFD model under different conditions, such as the S/C, flow rate, sweeping direction and flow rate, pressure, and membrane length [48]. The increasing S/C ratio boosts CH4 conversion for a fixed feed flow rate. Specifically, the CH4 conversion rate rose from 34 percent to 63 percent as the ratio of S/C was raised from two to six. H2 recovery increased with a decreased flow rate of the feed for a constant S/C. For instance, H2 recovery dropped from 28 percent to 2 percent as the mass flow rate of CH4 increased from 0.00005 to 0,0018 kg/sat a constant value of S/C of about 4. Methane conversion decreases with feed pressure while hydrogen yield increases with pressure rise.  Introducing sweeping flow significantly improved hydrogen recovery, which increased from 15 percent to 33 percent when the flow rate of the sweep was identical to the flow rate of the feed at a CH4 mass flow rate. Further increases in the sweep flow rate enhanced the H2 recovery a little, equal flow rates are optimal to minimize sweeping steam usage [48]. 

The effectiveness of the WGS on the MR was studied to record the influence of CO alteration on the recovery of H2 [49]. The study analyzed the significance of improving the operational parameters to maximize the efficiency of WGSR-MR systems for H2 production. Raising the sweeping flow rate enhances the conversation rate of CO and the recovery rate of H2. The low sweep flow of 18 sccm (Standard cubic centimeters per minute) resulted in a low conversion rate of CO and a low recovery rate of H2 due to the reduction in the permeation of H2. On the other hand, the high sweep flow of about 1800 sccm improves both metrics significantly. However, additional increases in sweep gas flow 

38 

yield diminishing returns beyond a certain point. Counterflow produces more CO conversion and H2 recovery when compared to the co-current flow for the reason of higher permeation that occurred alongside the overall length of the reactor. Varying the value of the S/C from 0.5 to two, showed that higher S/C ratios improve the conversion rate of CO and the recovery rate of H2, but the benefits diminish at higher ratios. Lower S/C ratios are beneficial in reducing CO2 capture costs in IGCC applications [49]. 

A study aims to address the integration of traditional SMR processes by introducing a novel reactor at a scale-up design [50]. The scalability of the design is supported by the simulation results, which show that the reactor maintains high performance even at larger scales. The addition of a carbon sorption material within MR was investigated [51]. The addition of CO2 sorbents in SEMR significantly increased CH4 conversion by shifting reaction equilibrium. H2 yield and generation rate increased with space velocity and pressure due to the more effective removal of H2 and CO2. Over 95% reduction in outlet CO2 and CO concentrations, doubling both MSR reactions and WGS reactions. Higher space velocities resulted in decreased CH4 conversion because of shorter reaction time, while increasing the generation rate of H2 and total H2 yield. Elevated pressures improved CH4 conversion and overall H2 yield due to enhanced reaction dynamics and effective gas permeation through the membrane. The SEMR showed superior performance in CH4 conversion and H2 yield better than traditional membrane reactors, especially during the initial phase when CO2 sorption was most active [51]. 

Research demonstrated the efficiency of a packed bed MR to generate hydrogen using a 2D-(CFD) model [52]. This study focuses on the low-temperature reactor that is heated using molten salt, examining a range of space velocities and operating conditions. Lower 

39 

space velocities (e.g., GHSV of 6000 h⁻¹) conduct higher CH4 conversion rates. High space velocities still achieved significant H2 recovery, with optimal conditions reducing CO concentrations, and improving overall H2 yield and purity. Higher S/C led to increased H2 recovery because of enhanced WGS reaction with excess steam and reduced CO concentrations, minimizing coke formation risks. Below 720 K, the performance was limited by low catalyst activity. Above 720 K, H2 recovery increased significantly due to higher reaction rates [52], [53]. 

A three-dimensional CFD simulation model studied the performance of MR to examine the influences of key operating circumstances on the efficiency and output of the SMR process[53]. Higher temperatures generally increased hydrogen production but required careful management of membrane durability. The sweep gas flow pattern significantly influenced hydrogen permeation, especially the counter-current flow. An increase in gas flow rate reduces overall residence time, leading to decreased H2 permeation. Raising the S/C from 1 to 3 raised the conversion rate of CH4 from 45% to 49%, with an exception at a ratio of 4. Higher sweep flow rates enhance CH4 conversion and H2 permeation[53]. 

40 

**Table 6: Summarized steam methane reforming Membrane Reactor modeling and simulation Studies.** 

|**Ref**|**Reactor**|**Catalyst**|**Software**|**Conditio**<br>**ns**|**Sweep gas**|**Results**|
|---|---|---|---|---|---|---|
|[49]|- 4 Tubes<br>(shell and<br>tube)<br>- Pd MR|Catalyzed<br>Pd<br>membrane|3D<br>COMSOL|- 900 °C<br>- S/C:<br>0.5-2<br>- 2000<br>kPa|-Argon<br>-Co-current and<br>counter-current|- Counter-flow is<br>superior to co-flow<br>- Higher S/C ratios<br>rise CO<br>- Increasing the<br>sweep flow rate<br>enhances CO<br>conversion|
|[51]|- Pd MR<br>- Pd SEMR|Ni/Al2O3<br>mixed<br>with<br>Na2ZrO3<br>sorbent.|3D Ansys|- 500 °C<br>- 3 MPa<br>- GHSV<br>1120,|- Nitrogen<br>- co-current|Impact of carbon<br>Sorbents:<br>-CH4conversion<br>increased|
|||||2240, and<br>3360 h<sup>-1</sup>||-H2yield and<br>generation rate<br>increased with|



41 

|- S/C: 3|space velocity and|
|---|---|
||pressure.|
||- Over 95%<br>reduction in CO2<br>and CO<br>concentrations.)|
||- Higher space|
||velocities:<br>Decreased CH4<br>conversion but<br>increased H2<br>generation rate and<br>yield|
||- Elevated|
||pressures:<br>Improved CH4<br>conversion and H2|
||yield.|



42 

|[50]|- Pd MR<br>Annular<br>- Pd MR<br>monolith|Ni/Al₂O₃|2D and 3D<br>COMSOL|-S/C 3–5<br>-773–873<br>K -300–<br>500 kPa|-N/A|- Efficient H2<br>permeability<br>validated by<br>Sievert's law<br>- 3D model shows<br>optimal reactor<br>configuration with<br>monolith<br>arrangement<br>- Higher CH4<br>conversion with H2<br>removal|
|---|---|---|---|---|---|---|
|[48]|Pd MR|Ni-based|2D Ansys|- 600 ◦C<br>- S/C: 2-6<br>- CH4<br>flow:<br>0.00005-|<br>-Steam<br>- co and<br>counter-current<br>- 600 ◦C<br>- 0 bar|- CH4conversion<br>increases with a<br>higher S/C and<br>decreases with an<br>increased feed flow<br>rate. - H2recovery<br>improves under<br>sweeping|



43 

|||||0.0018<br>kg/s<br>-<br>pressure:<br>5-40 bar<br>Membran<br>e: 1.0, 1.5<br>and 2.0 m<br>-Reactor:<br>1 m|- flow rate: 0–<br>0.04 kg/s|conditions and<br>counter-current<br>flow<br>- Increased<br>reformer pressure<br>leads to more<br>hydrogen<br>- Longer reactor<br>length increases<br>CH4conversion|
|---|---|---|---|---|---|---|
|[52]|Pd MR|Ni/Al₂O₃|2D Ansys|-773 K<br>-S/C:1-3<br>- 10 bar<br>GHSV:<br>6000-<br>15000-h<sup>-1</sup>|-Steam<br>-1 bar<br>-counter<br>currents|- Higher S/C ratios<br>improved H2<br>recovery and<br>reduced CO level<br>-773 K lower limit<br>preferred for<br>conversion|



44 

|||||||- the peak for<br>methane at 20,000 h<br>GHSV|
|---|---|---|---|---|---|---|
||Pd MR|Ni/Al₂O₃|3D Ansys|- 673–<br>1273 K<br>- 200–<br>250 kPa<br>-S/C:1-4|100 kPa|- Better<br>performance of<br>counter-current<br>flow<br>- The optimal<br>temperature range|
|[53]||||-GHSV<br>837 to<br>10,000<br>h⁻¹||for permeation and<br>reaction<br>performance is 673<br>K to 973 K.<br>- More CH4<br>conversion and H2<br>at raised GHSV|



Membrane reactors and steam methane reforming (SMR) differ in cost structures for 

hydrogen production. The MR demonstrated superior efficiency, achieving higher methanol conversion and hydrogen yields by integrating reaction and separation processes, 

45 

enabling a 23% cost reduction on MR over the cost for SMR. The elimination of a costly PSA system and lower operating temperatures contributed to the savings [54].  Membrane reactors typically have higher capital costs due to specialized membranes but offer energy savings and integration benefits, achieving Levelized Costs of Hydrogen (LCOH) around £1.78–2.80/kg H₂. In contrast, SMR systems have lower upfront costs but require additional purification and carbon capture for low-carbon hydrogen, with LCOH ranging from £1.42–2.84/kg H₂. While SMR remains cost-effective for large-scale production, membrane reactors provide higher efficiency and simpler designs, making them attractive for future low-carbon hydrogen technologies [55] Carbon taxes greatly influence the economics of hydrogen production. While traditional SMR is initially cheaper, membrane reactors become more economical under high carbon taxes, offering both financial and environmental advantages [56]. Costs for Pd-alloy membrane reactors are predicted to fall as manufacturing develops [57]. The high cost of palladium-based membranes significantly impacts economic feasibility, particularly given their replacement needs over time [58] 

46 

# **CHAPTER 3** 

# **COMPUTATIONAL MODELING** 

The computational fluid dynamics (CFD) numerical model integrates chemical (kinetic) and physical (thermodynamics) modules in various geometries, making it suitable for a wide range of problems. The CFD simulation solver successfully worked with numerous systems and fit the experimental data. Using a simulator solution is a cost-effective casestudy strategy that eliminates the need to deal with a real process model [59]. The CFD model accurately represented the steam methane reformer by taking account of mass transfer and diffusion between bulk and catalyst beads, as well as the kinetics of the SMR and WGS reactions occurring, in addition to the reformer's thermodynamic model, which represented the actual SMR reactor [36]. In addition, the CFD simulator covers the continuity, momentum, and energy equations. 

The reaction rate from Ferment and Xu [27] is used in the SMR kinetics model; this intrinsic reaction kinetic mechanism considers the influence of gas diffusion through catalyst beads on the conversion rate. The three reaction rate equations were constructed in C language and integrated into the simulation model via a user-defined function (UDF), Appendix [A]. 

The appropriate geometry dimensional model for CFD of SMR was chosen based on the residence time, relative length (reformer length to radius ratio), and the parameter under investigation. For residence times of more than 8 kg catalysts/mol CH4 and relative lengths greater than 15, the one-dimensional model is appropriate. For less residence duration and relative length values, two and three dimensions were used [59]. At the laminar region's 

47 

Reynolds number, the feed velocity on the porous zone is relatively slow. Fluent build-in mass, momentum, and energy equations (10), (11), and (12), respectively [60], solve for the flow through the assumed pseudo-homogeneous catalyst bed. 

Mass conservation: 



Momentum conservation: 



Energy conservation: 



Where 𝛽 the friction pressure drops in the reformer zone, the particle diameter is 1.75 mm 

assuming uniform bead size, and bed void fraction ε is 0.6. The friction pressure drop is an expression of internal resistance (C2), and viscose resistance (1/α). 



Viscose resistance:<sup>1</sup> = 150 (1 −𝜀)<sup>2</sup> (14) 𝛼 𝜀<sup>3</sup> 𝑑𝑝<sup>2</sup> 

The membrane film is combined with the reformer to purify the hydrogen from the reformer. Shell and tube MR is most employed in the conventional scale **Figure 6** , with the feed inlet to the shell porous side and pure steam at atmospheric pressure inlet to the 

tube membrane as a sweeping gas to maintain a low hydrogen pressure on the permeate 

48 

side [9]. Steam is preferred as a sweep gas for its high specific heat, availability from refineries, and ease of separation from hydrogen. A quarter of a single tube and the adjacent shell space were hired for the model calculation domain to save componential time **Figure** 

**7** . Feed is methane and steam, sweep gas is steam, Permeate is hydrogen and steam, and retentate is a mixture of unreacted methane and steam plus hydrogen, carbon dioxide, and carbon monoxide. 

The CH4 conversion and H2 recovery at the permeate output, as well as H2 selectivity over carbon, were studied for various operation pressures on the retentate side at numerous temperatures and an S/C ratio, and by varying the feed and sweep flow rates. Radial gradients are accounted for using the three-dimensional model. H2 flux is derived from the difference in H2 partial pressures between the membrane's two sides. Finally, the impacts of membrane diameter were explored as a means of optimizing design. The species transfer is given by Equation (15) [60]. The hydrogen permeation is written in C language code and is coupled with the fluent model as a UDF, Appendix [B]. 

Species transfer: 



49 



<!-- Start of picture text -->
H,0 +CO, + CH, +H, H,0+ CH,<br>Shell 20 + CHy>GH1)+ CO<br>H,0+ Hz H20<br>CO + H069COz +H)<br><!-- End of picture text -->

**Figure 6: Schematic diagram of axis-symmetric tube and shell membrane reactor model.** 



<!-- Start of picture text -->
O O O O Feed flow<br>r<br>00 A000 CH,+H,0<br>O OO O O © Sweep flow<br>O OO O O OO O H,OMembrane tubes<br>OOO0OO0O<br>OOOO<br><!-- End of picture text -->

**Figure 7: Cross-sectional view of shell and tubes MR in a square-pitch arrangement.** 

50 

# **CHAPTER 4** 

# **MODEL VALIDATION AND SETUP** 

A steam methane reformer (SMR) simulation model was created in ANSYS Fluent to validate the CFD numerical model. Before using the model in subsequent projects, the outcomes were checked against experimental and numerical data from the reference research to make sure it was accurate. The study uses symmetry to save computational time, where the geometry and boundary conditions are symmetric about the X-axis only half of the physical domain is modelled. 

The reformer geometry is a 2D rectangular representation (150 cm in length and 1 cm in width) representing a cross-section of a cylindrical steel pipe with a diameter of 150 cm and a wall thickness of 1 mm. The meshing involves edge meshing with an element size of 0.05 mm, a method that ensures high resolution and accuracy in capturing flow dynamics. This approach uses edge-sizing techniques to create a structured quadrilateral mesh, with a focus on refining the boundary regions for better flow characterization and computational efficiency. The meshing also applies biasing near critical areas to ensure optimal element distribution. The reactor area was discretized into a mesh comprising 12,000 elements (cells) with an orthogonal quality of 1.0 and a skewness of 0.2. Fine meshing was applied near the cylinder wall to account for boundary layer effects **Figure 8** . 

After the mesh is created and imported into Fluent, the boundary conditions, fluid properties, and solver options are defined. Solver controls are set, and the domain is initialized with estimated flow conditions to provide a starting point for iteration. The 

51 

simulation runs until the residuals of key variables (e.g., velocity, continuity, species mole fraction) converge to a selected value a stable solution. 

A steady-state, pressure-based solver with axisymmetric assumptions was employed to 

reduce computational time. All simulation parameters were aligned with those specified in the reference paper [59]. 

- Reformer geometry: 150 mm × 5mm 

- Catalyst particles size1.75×10<sup>-3</sup> mm, 0.6 porosity 

- Boundary conditions: T= 873 K (inlet, outlet, wall, and catalyst bed for law S/C 

ratio) 

- P= 1.5 bar 

- Inlet velocity = 0.71 m/s 

- S/C: 2, 2.5, 3, 3.5, 4, and 5 

- Laminar flow 

- Ideal gas mixing low 

- The residual of the conversion is 1×10<sup>−6</sup> 



<!-- Start of picture text -->
z<br><!-- End of picture text -->

**Figure 8:  Schematic diagram of the mesh used in the developed 2D axisymmetric model** 

**Table 7** and **Figure 9** show the validity of this model, where the hydrogen yield results fit 

the base paper results [59] and the experimental data [61] under the same conditions. At 

1.5 bar pressure, the methane conversion increases with S/C. 

52 

𝑚𝑜𝑙𝑒 𝐻2 𝐻2 𝑌𝑖𝑒𝑙𝑑= 𝑚𝑜𝑙𝑒 𝐶𝐻4 𝑖𝑛 

**Table 7: Numerical model validation results.** 

|S/C|H2Yie<br>This study<br>(CFD)|ld(mole H2/ mole<br>Pashchenko’s<br>modeling<br>data [59]|CH4 in)<br>Experimental<br>data [61]|
|---|---|---|---|
|2|1.675|1.6|1.68|
|2.5|1.861|1.84|1.87|
|3|2.0336|2|2.036|
|3.5|2.101|2.13|2.107|
|4|2.24|2.2|2.22|
|5|2.45|2.33|2.406|





<!-- Start of picture text -->
28<br>— This study<br>—®— Pashchenko [59]<br>26 —4— Experiment data [61]<br>24<br>=<br>x=<br>GC<br>22<br>2°2<br>~<br>x<br>5o 20<br>[=<br>18<br>1.6<br>20 25 3.0 3.5 40 45 5.0<br>Steam to carbon ratio<br><!-- End of picture text -->

**Figure 9: Comparison of experimental data and numerical results at different S/C ratios [59] [61].** 

53 

The 2D CFD model was utilized to analyze the SMR process at higher operation pressures of 5 and 10 bar, as hydrogen membrane removal required at least 10 bar of pressure to separate hydrogen effectively [62]. The feed gas residence duration on the porous reaction zone must be carefully adjusted to exceed the equilibrium residence time at which methane is completely converted. 

**Figure 10** and **Figure 11** show SMR conversion, H2 yield, and H2 mole fraction at various S/C ratios and feed pressures (5 bar and 10 bar, respectively). The high operation pressure inhibited methane conversion as the reaction kinetics shifted backward to the lower stoichiometric pressure. At constant pressure, the S/C has little effect on CH4 conversion. However, as the H2O mole fraction in the reaction zone grows, the hydrogen yield increases; because pressure does not affect the WGS reaction equilibrium, which occurs when two moles react to produce two moles. As a result, when building the membrane reformer, the pressure factor must be tuned to achieve the most hydrogen recovery on the permeate zone while maintaining optimal methane conversion. 

54 



<!-- Start of picture text -->
0.345 0.58<br>— Hydrogen mole fraction 1.4<br>0.340 — — MethaneHydrogen conversionyield 0.56<br>§ 14 0.54<br>=80.335 24D414 2S<br>2 2 0.52 8<br>E < Z<br>5 0.330 D4. 8<br>D> 8 0.50 ©<br>5 no} i=}<br>30.325 Fa £<br>= 14 | o4s=<br>1. 0.46<br>0.320<br>1.0 +044<br>0.315 bd<br>2.0 25 3.0 3.5 4.0<br>Steam to carbon ratio<br><!-- End of picture text -->

**Figure 10:  Results of the 2D Steam Methane Reformer Model at Different S/C ratios, 5 bar Pressure, and a** 

**temperature of 873 K.** 

55 



<!-- Start of picture text -->
— Hydrogen mole fraction<br>—— Methane conversion 0.42<br>— Hydrogen yield 1,<br>¢<br>Re}<br>3 i=<br>o 1.4 Ss<br>= 3 0.40'°D<br>2 sy g<br>P<br>> B. 8<br>8 0.28 3 2<br>3 = 0.38 S<br>> 1.0 oD<br>= =<br>og<br>0.36<br>2.0 25 3.0 3.5 4.0<br>Steam to carbon ratio<br><!-- End of picture text -->

**Figure 11: Results of the 2D Steam Methane Reformer Model at Different S/C ratios, 10 bar Pressure, and a** 

**temperature of 873 K.** 

56 

# **CHAPTER 5** 

# **RESULTS AND DISCUSSION** 

The MR is modeled using 168,000 mesh cells, as shown in **Figure 12.a** (with an 1.0 orthogonal quality and 0.2 skewness), and this configuration is based on a mesh sensitivity test [9]. Additionally, the boundary conditions for temperature and pressure are specified, with the inlet and outlet boundary temperatures maintained at a constant value of 873 K. The membrane is set as a fixed wall with a coupled thermal boundary condition. In terms of flow dynamics, feed and sweep mass flow rates at the inlets of the MR. To ensure an accurate representation of boundary layer effects, fine meshing is applied near the membrane wall, as shown in **Figure 12.b.** 

The pressure at the outlets is set equal to the inlet pressure for both the membrane tube and reformer shell sides. The CFD Ansys Fluent 2023 model setup is as follows: 

- A second-order upwind scheme is used for discretization 

- The SIMPLE algorithm is used for pressure−velocity coupling 

- A transient pressure-based solver is applied 

- The residual for conservation is set to 1 × 10<sup>−6</sup> 

- The laminar flow condition is applied due to the low Reynolds number. 

57 



<!-- Start of picture text -->
| gi<br>® Membrane wall<br><!-- End of picture text -->

**Figure 12: a) Schematic diagram of the MR mesh on the x-y-z axis, b) Mesh front view on the x-z axis.** 

The feed S/C with a ratio of 3 enters a membrane reactor with 6.8 × 10<sup>-5</sup> kg/s (10000 

GHSV), at 10 bar pressure and 873 K. Meanwhile, the reformer side remains unchanged from the previous SMR case, with steam flowing on the membrane side as a sweeping flow at atmospheric pressure at 873 K and 6.8 × 10<sup>-5</sup> kg/s. The membrane tube diameter is 8.5 mm, the pitch size between the centers of two adjacent tubes is 22 mm, and the MR length is 500 mm. Comparing the conversion in the case of MR-1 (where hydrogen continuously permeates to the membrane side) with the previous SMR results reveals a significant improvement in the methane conversion at the feed outlet, with an increase of up to 70%.In this case, the H2 mole fraction dropped on the retentate zone from 0.286 to 0.198, as shown in **Table 8** . Furthermore, the sweep flow enhances the hydrogen flux to the tube side, 

58 

thereby driving the reaction forward in the reformer. In the case of two membrane reactors, methane conversion decreases as the feed flow rate increases in MR-2. 

**Table 8: Performance comparison between steam methane reformer and membrane reactor.** 

||In|put||Output||
|---|---|---|---|---|---|
||Feed flow|Sweep flow|CH4|H2mole f|raction|
|Model|rate (kg/s)|rate (kg/s)|conversion|Reformer<br>side|Tube<br>side|
|SMR|8.6 e-5|-|0.39|0.286|-|
|MR-1|8.6 e-5|8.6 E-5|0.73|0.198|3.5 E-4|
|MR-2|8.6 e-4|8.6 E-4|0.666|0.18|6.6 E-5|



This study investigates the effect of steam flow rates as sweep flow on the permeate side, maintaining a constant pressure of 1 atm, while varying pressures on the reformer side (5, 10, and 15 bar) in co-current flow directions. In this study, the permeate side pressure was maintained at 1 atm. Subsequently, the effect of varying the feed flow rate on hydrogen production was analyzed under constant temperature and pressure conditions (873 K and 10 bar on the reformer side, 1 atm and 873 K on the permeate side). Additionally, the performance of membrane reactors with different tube geometries and reformer volumes was investigated. 

Methane conversion, hydrogen recovery, and hydrogen selectivity (kg hydrogen/kg carbon) over carbon (carbon dioxide and carbon monoxide) are used to evaluate the 

59 

performers of the MR under different parameters. These quantities are defined at the MR outlet as follows: 



The main objective of MR is to maximize hydrogen recovery from a membrane reactor during methane conversion. To optimize the system's efficiency, the effect of membrane tube diameter is studied, while keeping the feed and steam flow rates constant at various operating pressures. Three MR geometries are examined, with tube diameters of 8 mm, 10 mm, and 12 mm, and corresponding pitch sizes of 17.5 mm, 20 mm, and 22.3 mm respectively, all having a length of 500 mm lengths, as shown in **Figure 13** . The reformer volume is adjusted to maintain a constant membrane surface area-to-reformer volume ratio of 98 m⁻¹ across all configurations. The mesh sizes for the three configurations are 133,000, 162,000, and 173,000 element cells, respectively. Additionally, the impact of shell volume on the MR performance was tested with a fixed membrane tube diameter at 12 mm diameter (modified Tube-12 mm). 

60 



**Figure 13: Geometries of membrane reactor (tube and shell) numerical domain.** 

Methane and steam are Fed to the reformer with a 12 mm membrane tube diameter. The steam-to-carbon (S/C) ratio is set at 3, under feed pressure of 5,10, and 15 bar. The feed temperature is maintained at 873 K, with a feed flow rate of 0.0001 kg/s. Steam enters the tube as sweep flow at 1 atm, 873 K, and 0.0001 kg/s. 

Despite the reformer-side outlet pressure being held constant and equal to the feed pressure in every case, a slight pressure increase is observed near the reformer inlet for every feed pressure, as shown in **Figure 14** . This pressure increase occurs as the flow passes through the porous zone on the reformer side [63]. Since the pressure rise near the reformer inlet is negligible, the overall pressure change has an insignificant effect on the hydrogen flux rate 

change along the membrane length. 

61 



<!-- Start of picture text -->
)<br>0 0.1 02. | 0.3 0.4 05<br>axial distance (m)<br>es<br>nn<br>0 0.1 02. . 0.3 04 05<br>axial distance (m)<br>‘)<br>° ot OZ2 ial distance (ny 3 0.4. 0.5°<br><!-- End of picture text -->

**Figure 14: The pressure profile along the reformer at (a) 5 bar, (b) 10 bar, and (c) 15 bar feed pressure.** 

The temperature profile along the membrane tube film is represented in **Figure 15** . Given 

that the temperature is constant along the axial distance, the temperature does not influence 

the hydrogen flux rate change along the length. 



<!-- Start of picture text -->
Temperature (K) 860 861 862 863 864 865 866 867 868 869 870 871 872 873<br>0 04 02 03 04 05<br>axial distance (m)<br><!-- End of picture text -->

**Figure 15: The temperature profile along the reformer.** 

Changes in the kinetic reaction rates influence the mole fractions of species within the 

reformer. At high feed pressure, the reaction equilibrium shifts backward leading to a 

62 

reduction in methane conversion. This trend is reflected in the species mole fractions at the different feed pressures. **Figure 16, Figure 17,** and **Figure 18** represent the changes in the reactant and product mole fractions. At the lower feed pressure of 5 bar, the reaction occurs at a higher kinetic compared to the cases with feed pressure of 10 and 15 bar. This higher reaction rate leads to faster methane reforming, causing a rapid decrease in the methane mole fraction immediately after entering the reformer. The CO2 mole fraction increases as CO, produced from the reaction (1) at the reformer inlet, reacts with steam in the water shaft reaction (2) to produce CO2, which is also produced from reaction (3). 



<!-- Start of picture text -->
1.0<br>09 —co<br>0.8 CO2<br>§ 07 —— CH4<br>2 —— H20.<br>& 06<br>rf0S re<br>£<br>FA 0.4<br>Z<br>o 0.3<br>0.2<br>ss lll—l—=—===<br>0.0 01 0.2 03 04 OS<br>Membrane length (m)<br><!-- End of picture text -->

**Figure 16: Species mole fraction on reformer side for Tube-12 mm MR at feed rate 1 × 10**<sup>**-4**</sup> **kg/s of 3 S/C, 873 K, and 5 bar feed pressure.** 

63 



<!-- Start of picture text -->
1.0<br>09 ——2<br>—— CH,<br>08 —— co<br>507 —— CO.:<br>gs ——H,0<br>8 06<br>no<br>SOSvo<br>£<br>y 04<br>203<br>0.2<br>oo<br>00 oa 02 03 04 os<br>Membrane length (m)<br><!-- End of picture text -->

**Figure 17: Species mole fraction on reformer side for Tube-12 mm MR at feed rate 1 × 10**<sup>**-4**</sup> **kg/s, 3 S/C, 873 K,** 

**and 10 bar feed pressure.** 

64 



<!-- Start of picture text -->
1.0<br>——H,0<br>09 CH,<br>08 ——He<br>§ —— co.<br>g 07 —— co °<br>8 06<br>=<br>S05vo<br>£<br>4g 04<br>2<br>203<br>0.2 —————————————————————————<br>oo<br>0.0 0.1 0.2 0.3 04 Os<br>Membrane length (m)<br><!-- End of picture text -->

**Figure 18: Species mole fraction on reformer side for Tube-12 mm MR at feed rate 1 × 10**<sup>**-4**</sup> **kg/s, 3 S/C,  873 K, and 15 bar feed pressure.** 

Since there are insufficient changes in pressure or temperature along the length of the MR, the hydrogen partial pressure is the only factor influencing the hydrogen flux rate through the membrane tube. **Figure 19** , illustrates the hydrogen flux rates through the membrane at feed pressures of 5, 10, and 15 bar. The hydrogen flux rate is directly proportional to the hydrogen mole fraction on the reformer side. According to Sievert’s Law, the highest hydrogen flux rate occurs at a feed pressure of 15 bar, where the difference in hydrogen partial pressure between the two sides of the membrane is maximized. 

65 



<!-- Start of picture text -->
3E-4<br>r__ 5bar<br>2.8E-4. —— 15 bar<br>S 268-4 —— 10 bar<br>iS<br>S<br>@ 248-4<br>x<br>= 226-4<br>a<br>as<br>€ 26-4<br><o<br>Da<br>2 188-4<br>me}><br>x=<br>1.66-4<br>0.0 01 02 03 04 05<br>Membrane length (m)<br><!-- End of picture text -->

**Figure 19: Hydrogen flux rate along the membrane length for Tube-12 mm MR at feed rate 1 × 10**<sup>**-4**</sup> **kg/s, 3 S/C, and 873 K. Under 5,10, and 15 bar feed pressure.** 

## **5.1 Effect of sweep flow rate** 

**Figure 20** shows the impact of sweep flow and rate on methane conversion at different reformer pressures on Tube-12 mm under a range of feed pressure, 873 K, and feed flow rate of 0.0001 kg/s. The analysis begins with a no-sweep condition and progressively increases the sweep flow rates to 1.0, 2.0, and 4.0 times the feed flow rates. Introducing sweep flow on the permeate side in a co-current direction with the reformer-side feed flow set at 0.0001 kg/s, increases methane conversion. However, further increases in the sweep flow rate beyond 0.0001 kg/s had a slight increase in methane conversion. This indicates 

that a sweep flow rate equal to the feed flow rate is sufficient to enhance methane conversion by continually eliminating hydrogen from the reformer side. 

66 



<!-- Start of picture text -->
0.60<br>O55 —#—5 bar<br>—* 10 bar<br>0.50 —4— 15 bar<br>0.45<br>6<br>B 040<br>$ 0.35<br>Fa<br>8 030<br>2<br>§ 0.25<br>3gss 0.20<br>0.15<br>0.10<br>0.05<br>0.00<br>0 1 2 a 4<br>Sweep flow rate/feed flow rate<br><!-- End of picture text -->

**Figure 20: Effect of sweep flow rate on methane conversion on Tube-12 mm at different reformer pressures, 3** 

**S/C ratio, and 873 K.** 

Hydrogen recovery improves with the sweep flow rate, as shown in **Figure 21** . The sweep flow rate exhibits a consistent effect on hydrogen recovery across all pressure values. The higher sweep flow rate helps maintain a lower hydrogen partial pressure on the tube side, which enhances the hydrogen flux rate from the reformer side. Hydrogen selectivity over carbon follows the same pattern as the hydrogen recovery with increasing the sweep ratio, **Figure 22** . As a result, the mass flow rates of hydrogen rise at the permeate outlet **Figure** 

**23** while declining at the retentate outlet **Figure 24** . 

67 



<!-- Start of picture text -->
0.25<br>—*—5 bar<br>—®— 10 bar<br>20 = 15 bar<br>ra]<br>voS<br>8 015<br>2<br>=<br>©<br>a2 0.10<br>3<br>zr<br>0.05<br>0.00<br>0 1 2. 3 4<br>Sweep flow rate/feed flow rate<br><!-- End of picture text -->

**Figure 21: Effect of sweep flow rate on hydrogen recovery on Tube-12 mm at different reformer pressures, 3** 

**S/C, and 873 K.** 

68 



<!-- Start of picture text -->
0.20<br>—#—5 bar<br>—*— 10 bar<br>—+— 15 bar<br>ry<br>2o<br>x<br>&<br>< 0.15<br>ovaQ<br>ne}><br>ade<br>0.10<br>0 1 2 3 4 5<br>Sweep flow rate/feed flow rate<br><!-- End of picture text -->

**Figure 22: Effect of sweep flow rate on hydrogen selectivity on Tube-12 mm at different reformer pressures, 3** 

**S/C ratio, and 873 K.** 

69 



<!-- Start of picture text -->
__ 1E-6 —*—5 bar<br>xg —*— 10 bar<br>Qe-7 —4— 15 bar<br>2<br>© 8E-7<br>2ES<br>= 7E-7<br>B<br>s<br>=<br>© 6E-7<br>5<br>i}<br>S<br>& 5E-7<br>2<br>me}><br>=<br>4E-7<br>0 1 2. 3 4<br>Sweep flow rate/feed flow rate<br><!-- End of picture text -->

**Figure 23: Mass flow rate of hydrogen at retentate outlet of Tube-12 mm for 0.0001 kg/s feed flow rate, 873 K** 

**operating temperature, and different reformer pressure.** 

70 



<!-- Start of picture text -->
1.40E-07<br>—*—5 bar<br>x= —*— 10 bar<br>B 1208-07 ‘tba<br>2g<br>© 1.00£-07<br>2Es<br>“tp 8.00E-08<br>B<br>cy<br>—<br>+3 6.00E-08<br>5<br>io}<br>& 4.00E-08<br>vo<br>S<br>B 2.00E-08<br>><br>rz<br>0.00E+00<br>0 1 2 a 4<br>Sweep flow rate/feed flow rate<br><!-- End of picture text -->

**Figure 24: Mass flow rate of hydrogen at permeate outlet of Tube-12 mm for 0.0001 kg/s feed flow rate, 873 K operating temperature, and 10 bar reformer pressure.** 

## **5.2 Effect of Feed Pressure** 

**Figure 25** depicts the performance of the Tube-12 mm membrane reactor operating at 873 K, S/C of 3, and an equal feed and sweep flow rate of 0.0001 kg/s. The feed side pressure varies between 5 and 15 bar. The performance indicators include methane conversion, 

hydrogen recovery, and hydrogen selectivity over carbons. Methane conversion decreases as the feed side pressure rises. At a feed-side pressure of 5 bar, methane conversion is about 0.42. However, as the pressure increases to 15 bar, the conversion decreases to around 0.29. Higher feed-side pressure negatively impacts methane conversion, likely due to equilibrium limitations. Increased pressure shifts the reaction equilibrium backward, 

reducing the reaction rate and subsequently lowering methane conversion. As the feed side pressure rises, the hydrogen recovery rate increases. This indicates that higher feed-side 

71 

pressure increases selective hydrogen penetration through the membrane, leading to improved hydrogen recovery. Additionally, Hydrogen selectivity over carbon increases with increasing pressure. This suggests that the membrane reactor becomes more efficient as hydrogen permeability increases at higher pressures, increased hydrogen permeability shifts the chemical equilibrium, favoring hydrogen production over carbon. 



<!-- Start of picture text -->
0.45<br>—#— Methane conversion<br>2Fo40 —®— Hydrogen recovery<br>2 —4— Hydrogen selectivity<br>2 035<br>ray3<br>8© 0.30<br>=<br>g 0.25<br>fe}<br>2<br>£ 0.20<br>e<br>2<br>£0.15<br>5Sos2 aio o—_—________w—_*ae<br>0.05<br>4 6 8 10 12 14 16<br>Feed pressure (bar)<br><!-- End of picture text -->

**Figure 25: Effect of feed pressure on the performance of Tube-12 mm MR. Feed flow rate 1*E-4 kg/s, 3 S/C, and 873 K.** 

As pressure rises, methane conversion declines, while hydrogen recovery and selectivity improve. This is most likely due to pressure-driven hydrogen permeation, which increases recovery but alters the chemical equilibrium, resulting in methane conversion reduction. An ideal pressure balance may be determined by process goals: Higher pressures (around 

15 bar) promote hydrogen recovery, whilst lower pressures (5 bar) improve methane 

72 

conversion. Hydrogen permeation through membranes, especially palladium-based ones, is driven by the hydrogen partial pressure differences between the feed and permeate sides, with greater pressures improving hydrogen recovery and selectivity. 

The hydrogen mole fraction along both sides of the MR at various feed pressures is represented in **Figure 26** . At a lower pressure of 5 bar the hydrogen on the reformer side is distributed uniformly along the reactor. This low pressure reduces the hydrogen partial pressure, resulting in a lower flow rate through the membrane. At a feed pressure of 10 bar the hydrogen distribution becomes clearer, with a larger contrast between bulk hydrogen and hydrogen near the membrane. The rising pressure increases hydrogen flux through the membrane, resulting in a more concentrated hydrogen zone on the retentate side. At the highest pressure of 15 bar represented in, the polarization of the hydrogen mole fraction expands as the difference in hydrogen partial pressure grows. 

73 



<!-- Start of picture text -->
SEE 0 0.025 0.05 0.075 0.1 0.125 0.15 0.175 0.2 0.225 0.25 0.275 0.3<br><!-- End of picture text -->





<!-- Start of picture text -->
5 bar<br>10 bar<br>15 bar<br><!-- End of picture text -->



<!-- Start of picture text -->
S 0 S0.1 0.2 e0.3 0.4Se0.5 |<br>Membrane length (m)<br><!-- End of picture text -->

**Figure 26: Hydrogen mole fraction on Tube-12 mm MR at feed rate 1 × 10**<sup>**-4**</sup> **kg/s, 873 K, 3 S/C, and different feed pressures.** 

From the outlet mass flow rate of hydrogen **Figure 27** , we observe that pressure variations 

result in only minor changes in the mass flow rate. The positive effect of pressure on hydrogen flux rate counterbalances its negative impact on methane conversion. 

74 



<!-- Start of picture text -->
—#— Retentate outlet<br>aS —®— Permeate outlet<br>x<br>££<br>= 1E-6<br>fe}<br>2= =<br>a<br>8<br>S<br>iS<br>2ss<br>5a 1E-7<br>c<br>vo<br>aD<br>2<br>me}><br>=<br>1E-8<br>4 6 8 10 12 14 16<br>Feed pressure (bar)<br><!-- End of picture text -->

**Figure 27: Mass flow rate of hydrogen at the Tube-12 mm outlets for 0.0001 kg/s feed flow rate, 873 K operating temperature, and different feed pressure.** 

## **5.3 Effect of Steam to Carbon Ratio** 

The steam-to-methane (S/C) ratio is a crucial indicator of the performance of a membrane reformer. The S/C ratio affects methane conversion to hydrogen and other product gases. **Figure 28** shows the effect of the S/C ratio on Tube-12 mm at 873 K, 10 bar feed pressure, and feed and sweep flow rates of 0.0001 kg/s. 

As the S/C ratio rises, the methane conversion rate also rises. This implies that increased steam availability boosts methane conversion, especially when the S/C ratio is 5, where methane conversion peaks at 0.42. Higher S/C increases the reaction rates by delivering more steam for reactions, resulting in greater methane conversion. Hydrogen recovery is 

highest at low S/C ratios but decreases as S/C increases. This shows that increasing the 

75 

steam ratio reduces the hydrogen partial pressure on the reformer side, reducing the driving power for hydrogen penetration across the membrane. As the S/C ratio increases, the higher steam content in the system shifts the reaction equilibrium towards more hydrogen production. While higher S/C ratios provide more steam, which drives methane reforming and hydrogen production, excess steam also dilutes hydrogen and other components in the system. This dilution effect reduces the hydrogen mole fraction, which lowers its partial pressure at the reformer outlet, leading to a decrease in flux rate. As a result, the hydrogen mass flow rate at the permeate outlet decreases with an increasing S/C ratio, **Figure 29** . Higher S/C ratios (about 4-5) are preferable for operations aiming to maximize methane conversion. However, if hydrogen recovery is the first concern, a S/C ratio of about 1-2 appears to be ideal. 



<!-- Start of picture text -->
—=— Methane conversion<br>og<br>£ : —®— Hydrogen recovery<br>€ —4— Hydrogen selectivity<br>205<br>o<br>n<br>me]<br>& 04<br>Fa}<br>vo<br>6 03<br>iS}<br>aov<br>§¢ 02<br>2 CSS<br>g —S<br>fe}<br>U<br>5"0.0| SS<br>1 2 3 4 5<br>Steam to carbon ratio<br><!-- End of picture text -->

**Figure 28: Effect of steam to methane ratio on Tube-12 mm MR performance at 873 K, 10 bar feed pressure.** 

76 



<!-- Start of picture text -->
—#— Retentate outlet<br>=S —®— Permeate outlet<br>a<br>22 ies<br>=<br>2&<br>=<br>a<br>8<br>cs<br>SI<br>c<br>®<br>9 16-7<br>3<br>><br>=<br>z<br>=]5<br>°o<br>1E-8<br>1 2 3 4 5<br>Steam to carbon ratio<br><!-- End of picture text -->

**Figure 29: Mass flow rate of hydrogen at the Tube-12 mm outlets for 0.0001 kg/s feed flow rate, 873 K operating temperature, and different steam-to-carbon ratios.** 

## **5.4 Effect of Feed Flow Rates** 

The feed flow rate is essential in determining the overall efficiency of hydrogen production in methane reforming. It has a direct effect on the gases' residence time in the reformer. To improve system efficiency, the influence of feed flow rate on hydrogen production is tested at 1.00 × 10<sup>−5</sup> , 1.00 × 10<sup>−4</sup> , 1.00 × 1 0<sup>3</sup> , and 1.00 × 10<sup>−2</sup> kg/s rates on the Tube-12 mm MR configuration. **Figure 30** shows the effect of feed flow rate on MR performance under the following conditions: S/C of 3, a temperature of 873 K, and a pressure of 10 bar. 

Methane conversion drops with an increasing feed flow rate. At low feed flow rates (1×10<sup>−5</sup> kg/s), the conversion is relatively high, about 0.57. Beyond this point, conversion gradually decreases, reaching roughly 0.06 at higher feed flow rates. At a low flow rate, methane 

77 

remains in the reactor for a longer time, allowing for more conversion. As the flow rate rises, the residence time falls, resulting in conversion reduction due to insufficient time for the reaction to achieve equilibrium. When the feed flow rate increases, hydrogen recovery falls greatly. Initially, at low flow rates, hydrogen recovery is strong, exceeding 0.31, but rapidly reduces at increasing flow rates to 0.01 at a flow rate of 0.01 kg/s. Higher hydrogen recovery at lower feed flow rates indicates that more hydrogen passes through the membrane since the process has more time to create and separate hydrogen. As the feed flow rate increases, less hydrogen is recovered because the residence time decreases, limiting the amount of hydrogen that can permeate through the membrane. The selectivity for hydrogen production over carbon monoxide and carbon dioxide decreases with higher feed flow rates. This occurs because carbon species are produced from the slower reaction kinetics of reactions 2 and 3. 

78 



<!-- Start of picture text -->
—#— Methane conversion<br>£ 06: —®— Hydrogen recovery<br>€ —4— Hydrogen selectivity<br>205<br>o<br>n<br>=§ 04<br>ral<br>vo<br>8 03<br>iS}<br>ov<br>a<br>fa<br>3°PN<br>=01<br>fe}<br>U<br>$ —0.0<br>1E-5 1E-4 0.001 0.01<br>Feed flow rate (kg/s)<br><!-- End of picture text -->

**Figure 30: Effect of feed flow rate on Tube-12 mm MR performance, 3 S/C, 873 K, and 10 bar.** 

The hydrogen mole fraction on the MR changes with the feed flow rate **Figure 31** . The hydrogen contour plots indicate that the lowest hydrogen mole fraction in the reformer is located near the inlet. This low-hydrogen zone (dark blue) extends axially as the feed flow rate increases due to the shorter residence time of reactants. At lower feed flow rates, more hydrogen is observed on the tube side, leading to higher hydrogen recovery. Additionally, the hydrogen flux at the reactor outlet increases with the rising feed flow rate, as the hydrogen amount is proportional to the inlet feed flux, **Figure 32** . 

79 







<!-- Start of picture text -->
0.01 kg/s<br>0.001 kg/s<br>0.0001 kg/s<br>0.00001 kg/s<br><!-- End of picture text -->



<!-- Start of picture text -->
4<br>(e) 0.1 0.2 0.3 0.4 0.5<br>Membrane length (m)<br><!-- End of picture text -->

**Figure 31: Hydrogen mole fraction distribution on Tube-12 mm at different feed flow rates, under 10 bar feed pressure, 873 K, and 3 S/C.** 

80 



<!-- Start of picture text -->
—#— Retentate outlet<br>_S —®— Permeate outlet<br>< 1E-4<br>2<br>fd<br>E<br>2 16-5<br>Es<br>a<br>Bs<br>iS<br>© 1E-6<br>5<br>io}<br>c<br>De-7<br>2 1E-<br>me}><br>=<br>1E-8<br>1E-6 1E-5 1E-4 0.001 0.01 01<br>Feed flow rate (kg/s)<br><!-- End of picture text -->

**Figure 32: Mass flow rate of hydrogen at the Tube-12 mm outlets at 873 K operating temperature, 10 bar reformer pressure, and different feed flow rates.** 

The hydrogen flux rate has its highest value at the highest feed flow rate (0.01 kg/s) **Figure 33** , this is the effectiveness of the sweep gas to keep the hydrogen partial pressure low on the tube side. 

81 



<!-- Start of picture text -->
5E-4<br>4SE-4 —— 0.1 kg/s<br>a AE-4 —— 0.001 kg/s<br>¥ —— 0.0001 kg/s<br>S 35E-4 —— 0.0000 kg/s<br>£<br>Sy 3E-4<br>Zz5> 2.5E-4 AL | TT<br>=<br>&£ 26-4 f-—_<br>ov<br>* /<br>no}><br>=<br>Dna1E-4PT<br>0.0 0.1 0.2 03 0.4 0.5<br>Membrane length (m)<br><!-- End of picture text -->

**Figure 33: Hydrogen flux rate along the membrane length for Tube-12 mm membrane reactor at different feed flow rates, at 10 bar feed pressure, 3 S/C, and 873 K.** 

## **5.5 Effect of Flow Configuration** 

The performance of the MR for counter-current and co-current direction of feed and sweep flows, in terms of methane conversion, is represented in **Figure 34** . At 873 K, 3 S/C, and 0.0001 kg/s sweep and feed flow rates on Tube-12 mm at different feed pressures. At a feed pressure of 5 bar, co-current flow exhibits higher methane conversion compared to counter-current flow. However, as the pressure increases to 10 bar, the conversion rates for both configurations become nearly identical. Further increasing the pressure to 15 bar results in counter-current flow achieving higher methane conversion than co-current flow. 

This trend can be attributed to the differing driving forces for hydrogen permeation in each configuration. In co-current flow, the driving force is substantial at the reactor's entrance 

82 

but diminishes along its length, leading to decreased methane conversion at higher pressures. Conversely, counter-current flow maintains a more uniform driving force throughout the reactor, enhancing methane conversion as pressure increases. The highest hydrogen recovery and hydrogen selectivity recodes for the counter-current flow configure at 15 bar feed pressure, **Figure 35** and **Figure 36** . 



<!-- Start of picture text -->
0.50<br>—*— Counter current<br>0.45 —e—Co-Co-current<br>& 0.40<br>ra<br>g<br>2 0.35<br>°°<br>iS)<br>2 030<br>S<br>$s<br>=uv 0.25<br>0.20<br>0.15<br>4 6 8 10 12 14 16<br>Feed pressure (bar)<br><!-- End of picture text -->

**Figure 34: Methane conversion on Tube-12 mm at 873 K, feed flow rate 1*10**<sup>**-4**</sup> **kg/s, and 3 S/C, for co-current and counter-current flow configurations.** 

83 



<!-- Start of picture text -->
04<br>—*— Counter-current<br>—*— Co-current<br>03<br>a<br>vo$<br>fe)<br>5<br>2<br>c 02<br>G<br>a<br>ig<br>3<br>ES<br>x= oO<br>01<br>0.0<br>4 6 8 10 12 14 16<br>Feed pressure (bar)<br><!-- End of picture text -->

**Figure 35: Hydrogen recovery on Tube-12 mm at 873 K, feed flow rate 1*10**<sup>**-4**</sup> **kg/s, and 3 S/C, for co-current and** 

**counter-current flow configurations.** 

84 



<!-- Start of picture text -->
0.20<br>—#— Counter-current<br>—®*— Co-current<br>0.18<br>2<br>2<br>=)5<br>©<br>© 0.16<br>a<br><o<br>Da<br>Qo2<br>=<br>0.12<br>4 6 8 10 12 14 16<br>Feed pressure (bar)<br><!-- End of picture text -->

**Figure 36: Hydrogen selectivity on Tube-12 mm at 873 K, feed flow rate 1*10**<sup>**-4**</sup> **kg/s, and 3 S/C, for co-current and counter-current flow configurations.** 

**Figure 37** shows the hydrogen flux rate across the membrane for both flow configurations at different feed pressures, highlighting the impact of flow direction. In the counter-current configuration, the sweep gas enters at 0.5 m axial length, resulting in a permeation rate that 

peaks at the retentate outlet of the MR. In the co-current configuration, the hydrogen flux rate exhibits it is peak near the reformer inlet. 

85 



<!-- Start of picture text -->
SE-4<br>Asa: —+— Counter-currentCounter-current 510barbar<br>aE-4 —*— Counter-current 15 bar<br>@ 35-4 —*—Co-current 5 bar<br>E —— Co-current 10 bar<br>5E 3-4 —*— Co-current 15 bar<br>:5 |<br>2{<br>g<br>5<br>0.0 0.1 0.2 0.3 04 0.5<br>Membrane length (m)<br><!-- End of picture text -->

**Figure 37: Co-current and counter-current flow configurations hydrogen flux rate along the membrane length for Tube-12 mm MR at feed rate 1 × 10**<sup>**-4**</sup> **kg/s, 3 S/C, and 873 K.** 

**Figure 38** illustrates that the hydrogen mole fraction is consistently higher on the permeate side in the counter-current configuration across all pressure values. Consequently, the counter-current configuration achieves the highest hydrogen mass flow rate at the permeate outlet for all pressure conditions, as shown in **Figure 39** . 

86 



<!-- Start of picture text -->
—*— CC retentate outlet<br>=S —*— CO retentate outlet<br>= —4— CC permeate outlet<br>4 —y¥— CO permeate outlet<br>= 1E-6<br>6<br>= ——_<br>a -+-_ "3<br>a&<br>e<br>ca© 1E-7 ee ne<br>me}><br>=<br>z<br>=<br>5<br>fo}<br>1E-8<br>4 6 8 10 12 14 16<br>Feed pressuer (bar)<br><!-- End of picture text -->

**Figure 38: Co-current and counter-current flow configurations mass flow rate of hydrogen at Tube-12 mm** 

**outlets for 0.0001 kg/s feed flow rate, 873 K operating temperature, and different pressure.** 

87 



<!-- Start of picture text -->
QO 0.025 0.05 0.075 0.1 0.125 0.15 0.175 0.2 0.225 0.25 0.275 0.3<br><!-- End of picture text -->





<!-- Start of picture text -->
Co-current 5 bar<br>Counter-current 5 bar<br>Co-current 10 bar<br>Counter-current 10 bar<br>Co-current 15 bar<br>Counter-current 15 bar<br><!-- End of picture text -->

**Figure 39: Hydrogen mole fraction distribution on Tube-12 mm for co-current and counter-current flow directions under 10 bar feed pressure, 873 K, and 3 S/C.** 

88 

## **5.6 Effect of Membrane Tube Configuration** 

The methane conversion, hydrogen recovery, and hydrogen selectivity for the three tubes configures at 5 bar, 10 bar, and 15 bar reformer side pressure, are summarized in **Figure** 

**40** , **Figure 41** , and **Figure 42** , respectively. 

Across all operating pressures (5, 10, and 15 bar) at 873 K, 3 S/C, and equal flow rates for feed and sweep at 0.0001 kg/s, methane conversion slightly increases as the tube diameter increases. Tube-12 mm initially shows a methane conversion of about 0.42 at 5 bar, decreasing to around 0.29 at 15 bar, for Tube-10 mm starts around 0.41 at 5 bar and decreases to approximately 0.26 at 15 bar, and for Tube-8 mm the methane conversion drops from about 0.39 at 5 bar to 0.25 at 15 bar. Methane conversion declines with increasing pressure, this is likely due to reaction kinetics and equilibrium limitations at higher pressure. Tube-12 mm remains the most efficient for methane conversion. 

89 



<!-- Start of picture text -->
0.44<br>0.42 —#— Tube-8 mm<br>—®—Tube-10 mm<br>0.40 —+—Tube-12 mm<br>5 038<br>a<br>5 0.36<br>e<br>© 0.34<br>S<br>2 0.32<br>S<br>s© 0.30<br>=<br>0.28<br>0.26<br>0.24<br>4 6 8 10 12 14 16<br>Feed pressure (bar)<br><!-- End of picture text -->

**Figure 40:  Methane conversion for the three MR configures. Reformer feed pressure of 5, 10, and 15 bar, temperature at 873 K, and 3 S/C.** 

Hydrogen recovery increases with pressure but varies with tube diameter. Tube-8 mm consistently shows the highest hydrogen recovery across all pressures. At 5 bar feed pressure, hydrogen recovery is moderate for all tubes, but it is notably higher for Tube-8 mm. At higher pressures (10 and 15 bar), hydrogen recovery improves significantly due to the hydrogen partial pressure increase, which enhances the driving force for hydrogen permeation. The gap between Tube-12 mm and Tube-10 mm is relatively small, but the gap between Tube-8 mm and the other tubes is wide, especially for higher pressure. This suggests that Tube-8 mm may be the best suitable for efficient hydrogen recovery at higher pressures compared to the others. Hydrogen selectivity, which indicates the selectivity to produce hydrogen over other carbon, shows a similar trend to hydrogen recovery. Tube-8 

90 

mm demonstrates the highest selectivity across all pressures, that’s justified the higher 

hydrogen recovery for Tube-8 mm. 



<!-- Start of picture text -->
0.28<br>—#—Tube-8 mm<br>0.26 —®—Tube-10 mm<br>0.24 —*— Tube-12 mm.<br>ry<br>@ 0.22<br>ce}<br>5<br>© 0.20<br>&D018<br>2<br>me}0.16><br>0.14<br>0.12<br>0.10<br>4 6 8 10 12 14 16<br>Feed pressure (bar)<br><!-- End of picture text -->

**Figure 41:  Hydrogen recovery for the three MR configures. Reformer feed pressure of 5, 10, and 15 bar,** 

**temperature at 873 K, and 3 S/C.** 

91 



<!-- Start of picture text -->
0.190<br>aes —=— Tube-8Tube-  mm<br>—®—Tube-10 mm<br>0.180 —4—Tube-12 mm<br>0.175<br>2<br>= 0.170<br>& 0.165<br>& 0.160<br>&0155<br>5 0.150<br>><br>TP o.145<br>0.140<br>0.135<br>0.130<br>4 6 8 10 12 14 16<br>Feed pressure (bar)<br><!-- End of picture text -->

**Figure 42: Hydrogen selectivity for the three MR configures. Reformer feed pressure of 5, 10, and 15 bar, temperature at 873 K, and 3 S/C.** 

**Figure 43** illustrates the hydrogen flux rate across three membrane tubes of varying diameters. The membrane reactor with the lowest tube diameter achieves the highest hydrogen flux along the membrane length. This results in the best performance in terms of methane conversion and hydrogen separation. 

92 



<!-- Start of picture text -->
2.4E-4 ——Tube-8 mm<br>——Tube-10 mm.<br>aay 2:3E-4 — Tube-127 mm.<br>=<br>By 2.2E-4<br>=<br>x<br>a 2.1E-4 =—<br>=<br>a<br>a<br>S€ 2€-4<br>c<br>o<br>D2 1.9-4<br>3<br>ES<br>x=<br>1.8E-4<br>0.0 01 0.2 03 04 0.5<br>Membrane length (m)<br><!-- End of picture text -->

**Figure 43: Hydrogen flux rate along the membrane length for three MR configures at feed rate 1 × 10**<sup>**-4**</sup> **kg/s, 3** 

**S/C, and 873 K.** 

Better radial hydrogen distribution along the membrane tube improves hydrogen flux through the membrane. **Figure 44** illustrates the hydrogen mole fraction contours for various MR configurations. In the Tube-8 mm, hydrogen permeation extends into the bulk on the reformer side **.** This justifies the higher hydrogen flux rate at Tube-8 mm. 

93 



<!-- Start of picture text -->
0 0.025 0.05 0.075 0.1 0.125 0.15 0.175 0.2 0.225 0.25<br><!-- End of picture text -->





<!-- Start of picture text -->
Tube-8 mm<br>Tube-10 mm<br>Tube-12 mm<br>Tube-12 mm modified<br><!-- End of picture text -->



<!-- Start of picture text -->
0es0.1 0.2 0.3 0.4cs0.5 J<br>Membrane length (m)<br><!-- End of picture text -->

**Figure 44: Hydrogen mole fraction distribution for different MR configures under 10 bar feed pressure, 873 K, and 3 S/C.** 

## **5.7 Effect of Shell Volume** 

Tube-12 mm has a variance in hydrogen mole fraction on the shell side **Figure 44** , 

minimizing the shell volume is expected to suppress the hydrogen on the bulk towards the 

94 

membrane film and lead to increased hydrogen permeation through the membrane film. A membrane tube with a 12 mm diameter and 20 mm pitch size (Tube-12 mm modified) with membrane surface areas to reformer volume ratio at 131 m⁻¹ tested for 0.0001 kg/s, 3 S/C, and 10 bar feed pressure. The methane conversion dropped to 0.26 compared to 0.30 for Tube-12 mm **Figure 45** . The hydrogen recovery drops to 0.08 from 0.12 on Tube-12 mm. Hydrogen selectivity raised slightly on Tube-12 mm modified. This result confirms (Bian and Xia) work [64]. In steam methane reforming within a membrane separation reactor, a smaller shell volume leads to reduced overall hydrogen production due to the elevated hydrogen partial pressure, which inhibits further hydrogen generation. Similarly, the conversion rate decreases in smaller shell volumes for the same reason. The total hydrogen recovery through the membrane tube is lower in the modified configurations with a smaller shell volume, **Figure 46** . Moreover, the modified Tube-12 mm configuration exhibits a higher hydrogen flux rate in the uniform region along the membrane length, attributed to the increased hydrogen partial pressure, **Figure 47** . 

95 



<!-- Start of picture text -->
HE Methane conversion<br>204 [EM Hydrogen recovery<br>F [Hydrogen selectivity<br>2o<br>&<br>me]=<br>5<br>S<br>ov2<br>8 02<br>2<br>¢<br>2¥<br>$<br>Fa<br>0fe}<br>0.0<br>Tube-12 mm modified Tube-12 mm<br><!-- End of picture text -->

**Figure 45: Methane conversion, Hydrogen recovery, and selectivity on Tube-10 mm, Tube-12 mm, and modified Tube-12 mm, at 0.0001 kg/s feed flow rate, 873 K, 10 bar, and 3 S/C.** 

Hydrogen mole fraction contours on the modified Tube-12 mm **Figure 44** . Hydrogen permeation is limited to the narrow region on the tube side. The Tube-12 mm with a 12 mm diameter and 22.3 mm pitch size is optimal for hydrogen recovery over the modified Tube-12 mm with lower shell volume. 

96 



<!-- Start of picture text -->
_ [EE Permeate outlet<br>LQ 1e-5 (0 Retentate outlet<br>Zz<br>1-6<br>STE<br>ES6<br>= 1E-7<br>vgg<br>E<br>S 1E-8<br>BU<br>=<br>3<br>(1E-9<br>c<br>oS<br>% 1E-10<br>><br>zr<br>1E-11<br>Tube-12 mm modified Tube-12 mm.<br><!-- End of picture text -->

**Figure 46: Mass flow rate of hydrogen at the Tube-12 mm and Tube-12 mm modified outlets for 0.0001 kg/s feed** 

**flow rate, 873 K operating temperature, and different steam-to-carbon ratios.** 

97 



<!-- Start of picture text -->
——Tube-12 mm<br>ry 228-4 —— Tube-12 mm modified<br>Res<br>A<br><<br>£<br>]<br>oD |<br>J<br>ro i a<br>=<br>> 216-42E-4 :<br>%<br>oO<br>&<br>c<br>& 1,9E-4<br>ot<br>ne}><br>x=<br>1.8E-4<br>0.0 0.1 0.2 0.3 04 0.5<br>Membrane length (m)<br><!-- End of picture text -->

**Figure 47: Hydrogen flux rate along the membrane length for Tube-12 mm and Tube-12 mm modified MR** 

**configures at feed rate 1 × 10**<sup>**-4**</sup> **kg/s, 3 S/C, and 873 K.** 

98 

# **CHAPTER 6** 

# **CONCLUSIONS, RECOMMENDATIONS, AND** 

# **LIMITATIONS** 

The potential for scaling up membrane reactors for industrial hydrogen production emphasizes the need for optimal reactor design and operational conditions. By optimizing the membrane reactor, methane leakage can be minimized, reducing greenhouse gas emissions, and enhancing the environmental profit of blue hydrogen as a green fuel. These conclusions provide a comprehensive realization of the critical factors that impact the efficiency of steam methane reforming on MR, paving the way for more effective and environmentally friendly hydrogen production technologies. 

- While high pressures are necessary for effective hydrogen separation in membrane reactors, they tend to reduce the methane conversion efficiency. This inverse relationship suggests a need for careful pressure optimization to balance methane conversion and hydrogen recovery. 

- Increasing the steam to carbon ratio improves methane conversion and negatively impacts hydrogen recovery. 

- Higher pressures enhance hydrogen recovery for all tubes, but the smaller tube performs the best. The trend indicates that increasing pressure favors higher hydrogen recovery across all tube types. 

- The feed flow rate is a critical parameter in methane reforming processes, as it directly affects methane conversion, hydrogen recovery, and hydrogen permeation. Lower feed 

99 

flow rates favor higher methane conversion and higher hydrogen recovery, due to longer reactants’ residence time. 

- Larger membrane tube diameter shows the best methane conversion. And the smaller tube diameter configure shows best the hydrogen recovery, and selectivity across all pressure levels. These results suggest that the choice of tube has a significant impact on hydrogen recovery and optimizing pressure conditions could further enhance recovery. 

- The larger shell side volume enhances methane conversion and hydrogen recovery. 

- The selection of MR dimensions should be based on target methane conversion, hydrogen recovery, and hydrogen selectivity for the specific process requirements. 

- Further investigating the membrane reformer dimensions of the tube and pitch size is recommended under higher feed pressure, to underline the tube and pitch size for best methane conversion and hydrogen recovery. Additionally, studying the effect of the membrane length on the hydrogen recovery. 

The computational tools and approaches used in my thesis research are the main source of its limitations. Although ANSYS Fluent provides strong simulation and visualization platforms, the analysis's coverage may be limited by their built-in limitations, which include predefined modeling capabilities and numerical approximations. Furthermore, the study's results rely on the accuracy of the assumptions, boundary conditions, and input data used, all of which might fail to accurately reflect the complexity of the real world. The investigation of a wider range of cases and characteristics was also constrained by time restrictions and the processing demands of high-High-precision modeling. 

100 

# **Appendix [A]: Reaction Rate Code** 

```
/**********************************************************
************/
```

```
/* The reaction rate were taken from this paper
```

```
"1989 Methane Steam Reforming, Methanation and Water-Gas
Shift: 1. Intrinsic Kinetics" */
```

```
#include "udf.h"
```

```
DEFINE_VR_RATE(myrate,c,t,r,wk,yk,rate,rr_t)
```

```
{
```

```
/*If more than one reaction is defined, it is necessary to
distinguish
```

```
between these using the names of the reactions. */
```

```
float p[6];            /* partial pressure for each specie
*/
float g[5];            /* adsorption rate from Arrhenius
equation */
float w[3];            /* Reaction rate from Arrhenius
equation */
float s[3];            /* ?????????????????????????????? */
real xc[ND_ND];        /* for any dimension geometry  */
float y[6];            /* Molar weight for each specie */
```

```
//int ds=1870;
```

```
//float b=exp(30.42-27106/C_T(c,t));
```

```
//float d=exp(-3.798+4160/C_T(c,t));
//float o=exp(34.218-31266/C_T(c,t));///original
//float o=exp(37-31266/C_T(c,t)); //changed
```

101 

```
float b=pow(10,(13.076-11650/C_T(c,t)));  /* equilibrium
constant for rate 0    ?? */
```

```
float d=pow(10,(-1.764+1910/C_T(c,t)));   /* equilibrium
constant for rate 1    ?? */
```

```
float o=pow(10,(11.312-9740/C_T(c,t)));   /* equilibrium
constant for rate 2    ?? */
```

```
/* For calculating the Molar fraction for each specie */
```

```
float
```

```
bb=((C_YI(c,t,0)/16)+(C_YI(c,t,1)/18)+(C_YI(c,t,2)/28)+(C_Y
I(c,t,3)/2)+(C_YI(c,t,4)/44)+ (C_YI(c,t,5)/28));
```

```
int cc[6]={16,18,28,2,44,28};   /* Molecular  weight for
each specie === CH4 , H2O , CO , H2 , CO2 , N2 */
```

```
float q; /* For calculating the demenator of each rate */
```

```
/* The pre_exponential coeff. (m[i]) of adsorption and
delta H f[5] for each specie were taken from paper:
```

```
 Methane Steam Reforming, Methanation and Water-Gas Shift:
```

```
1. Intrinsic Kinetics, 1989*/
```

```
float m[5]={6.65/(10000), 1.77*100000, 8.23/(100000),
6.12/(1000000000), 2}; /* pre-exponential co-effiients for
each specie adsorption*/
```

```
int f[5]={-38280, 88680, -70650, -82900, 2};  /*
delta H for each specie at respective refernce
temeprature*/
```

```
/* The pre_exponential coeff. (n[i]) and activation energy
j[i] for each reaction were taken from paper:
```

```
 Methane Steam Reforming, Methanation and Water-Gas Shift:
1. Intrinsic Kinetics, 1989*/
```

```
float n[3]={(4.225*1000000000000000), (1.955*1000000),
(1.020*1000000000000000)};  /* pre-exponential co-effiients
for each reaction*/
```

102 

```
int j[3]={240100, 67130, 243900};
```

```
/*activation energy for each reaction*/
```

```
int i=0;
```

```
/*Message("Cell number: %f\n",UNIVERSAL_GAS_CONSTANT);*/
```

- `/* For calculating the partial pressure of species */` 

```
C_CENTROID(xc,c,t);
```

```
/*Message("pressure : %f\n", C_P(c,t));*/
```

- `/* Molar fraction for each specie */` 

- `/*  where CyI is the mass fraction of specie, b.b is the mixture, and c.c is the Molecular weight */` 

```
i=0;
```

```
for(i = 0; i < 6; i++)
```

```
{
```

```
y[i]=C_YI(c,t,i)/(bb*cc[i]);      /* Molar fraction for
each specie where CyI is the mass fraction of specie */
```

```
}
```

- `/* then calculate the partial pressure for each specie */` 

```
p[0] = ((C_P(c,t))/101325)*y[0];    /* partial pressure of
CH4 */
```

```
p[1] = ((C_P(c,t))/101325)*y[1];    /* partial pressure of
H2O */
```

```
p[2] = ((C_P(c,t))/101325)*y[2];    /* partial pressure of
CO */
```

- `p[3] = (((C_P(c,t))/101325)*y[3]);  /* partial pressure of H2 */` 

- `p[4] = ((C_P(c,t))/101325)*y[4];    /* partial pressure of CO2 */` 

```
p[5] = ((C_P(c,t))/101325)*y[5];    /* partial pressure of
N2 */
```

103 

```
/* for calculating the adsorption rate g(i)for each specie
*/
```

```
i=0;
for(i = 0; i < 5; i++)
{
```

```
g[i]=m[i]*exp((-f[i]/(8.314*C_T(c,t))));        /*
adsorption rate from Arrhenius equation */
```

```
//Message("pp : %f\n", p[i]);
```

```
}
```

```
//Message("pt : %f\n", (C_P(c,t))/101325);
```

```
//Message("den : %f\n", C_R(c,t));
```

- `/* for calculating the reaction rate w(i)for each reaction */` 

```
i=0;
```

```
for(i = 0; i < 3; i++)
{
```

```
w[i]=n[i]*exp((-j[i]/(8.314*C_T(c,t))));      /* Reaction
rate from Arrhenius equation */
```

```
}
```

- `/* For calculating the demenator of each rate */` 

```
q=1+g[2]*p[2]+g[3]*p[3]+g[0]*p[0]+g[1]*p[1]/p[3];
```

```
if (!strcmp(r->name, "reaction-1"))
```

```
{
```

```
/* Reaction 1 */
```

```
*rate = 1*((w[0]/pow(p[3],2.5))*(p[0]*p[1]-
pow(p[3],3)*p[2]/b)/pow(q,2));
```

```
*rr_t = *rate;
```

104 

```
/* No "return..;" value. */
/*Message("reaction 1");*/
//Message("r1 : %f\n", *rr_t);
//Message("t1 : %f\n", .5194);
//Message("t2 : %f\n", (w[0]/pow(p[3],2.5)));
//Message("t3 : %f\n", (p[0]*p[1]-pow(p[3],3)*p[2]/b));
//Message("t4 : %f\n", pow(q,2));
//Message("T : %f\n", C_T(c,t));
//Message("P : %f\n", C_P(c,t));
}
else if (!strcmp(r->name, "reaction-2"))
{
/* Reaction 2 */
*rate = 1*((w[1]/pow(p[3],1))*(p[1]*p[2]-
pow(p[3],1)*p[4]/d)/pow(q,2));
*rr_t = *rate;
/* No "return..;" value. */
/*Message("reaction 2");*/
//Message("r2 : %f\n", *rr_t);
}
else if (!strcmp(r->name, "reaction-3"))
{
/* Reaction 3 */
```

```
*rate = 1*((w[2]/pow(p[3],3.5))*(p[0]*pow(p[1],2)-
pow(p[3],4)*p[4]/o)/pow(q,2));
*rr_t = *rate;
```

105 

```
/* No "return..;" value. */
/*Message("reaction 3");*/
//Message("r3 : %f\n", *rr_t);
}
else
{
Message("UDF is not read");
/* Message("Unknown Reaction\n"); */
Message("UDF is not read");
}
/* Message("Actual Reaction: %s\n",r->name); */
}
```

106 

# **Appendix [B]: Hydrogen Permeation Code** 

```
/* UDF for hydrogen permation through pd membranes */
#include "udf.h"
#define WALLSIDE1 8
#define WALLSIDE2 17
#define P_0 101325
#define UDM_NEIGHBOUR_C    0
#define UDM_NEIGHBOUR_TC   1
#define UDM_MASS_SOURCE    2
#define UDM_flux           3
#define UDM_fluxperarea    4 /* Number of memories should
be 5 */
#define TOLERANCE 1E-10
#define SPECIES_NUMBER 0
DEFINE_INIT(init_functionright,d)
{
  Thread *tc1, *tc2;
  Thread *tf1, *tf2;
  cell_t c1, c2;
  face_t f1, f2;
  real   f_c1[3], f_c2[3];
  thread_loop_c(tc1,d)
  {
    begin_c_loop(c1,tc1)
    {
```

107 

```
      C_UDMI(c1,tc1,UDM_NEIGHBOUR_C)    = 0.0;
      C_UDMI(c1,tc1,UDM_NEIGHBOUR_TC)   = 0.0;
      C_UDMI(c1,tc1,UDM_MASS_SOURCE)    = 0.0;
    }
    end_c_loop(c1,tc1)
  }
  tf1 = Lookup_Thread(d,WALLSIDE1);
  tf2 = Lookup_Thread(d,WALLSIDE2);
  begin_f_loop(f1,tf1)
  {
    F_CENTROID(f_c1,f1,tf1);
    c1 = F_C0(f1,tf1);
    tc1 = THREAD_T0(tf1);
    begin_f_loop(f2,tf2)
    {
      F_CENTROID(f_c2,f2,tf2);
      if (fabs(f_c1[0]-f_c2[0]) <= TOLERANCE &&
          fabs(f_c1[1]-f_c2[1]) <= TOLERANCE &&
          fabs(f_c1[2]-f_c2[2]) <= TOLERANCE )
      {
        c2 = F_C0(f2,tf2);
       tc2 = THREAD_T0(tf2);
        C_UDMI(c1,tc1,UDM_NEIGHBOUR_C) = c2 + 0.1;
        C_UDMI(c2,tc2,UDM_NEIGHBOUR_C) = c1 + 0.1;
        C_UDMI(c1,tc1,UDM_NEIGHBOUR_TC) = THREAD_ID(tc2) +
0.1;
```

108 

```
        C_UDMI(c2,tc2,UDM_NEIGHBOUR_TC) = THREAD_ID(tc1) +
0.1;
      }
    end_f_loop(f2,tf2)
  }
  end_f_loop(f1,tf1)
```

```
Message("\n Membrane initialisation completed.\n");
}
DEFINE_SOURCE(source_massright,c,t,ds,eqn)
{
  ds[eqn] = 0.0;
  return C_UDMI(c,t,UDM_MASS_SOURCE);
}
DEFINE_ADJUST(adjust_sourcesright, d)
{
  Thread *tc1, *tc2;
  Thread *tf1;
  cell_t c1, c2;
  face_t f1;
  real mass_flux, face_area, face_area_vector[3];
  real
massfrac1_CH4,massfrac1_H2O,massfrac1_CO,massfrac1_H2,massf
rac1_CO2,massfrac1_N2,cell_volume1;
```

```
  real
```

```
massfrac2_CH4,massfrac2_H2O,massfrac2_CO,massfrac2_H2,massf
rac2_CO2,massfrac2_N2,cell_volume2;
```

```
  real molefrac1_H2,molefrac2_H2;
```

109 

```
  real CH4_mwt,H2O_mwt,CO_mwt,H2_mwt,CO2_mwt,N2_mwt;
  real P1,P2,PP1,PP2, Ah;
CH4_mwt=16;
H2O_mwt=18;
CO_mwt=28;
H2_mwt=2;
CO2_mwt=44;
N2_mwt=14;
Ah=0.4/1000*H2_mwt;
  tf1 = Lookup_Thread(d,WALLSIDE1);
  begin_f_loop(f1,tf1)
  {
```

```
    F_AREA(face_area_vector,f1,tf1);
    face_area = NV_MAG(face_area_vector);
    c1 = F_C0(f1,tf1);
    tc1 = THREAD_T0(tf1);
    cell_volume1 = C_VOLUME(c1,tc1);
    c2  = (int)C_UDMI(c1,tc1,UDM_NEIGHBOUR_C);
    tc2 = Lookup_Thread(d,
(int)C_UDMI(c1,tc1,UDM_NEIGHBOUR_TC));
    cell_volume2 = C_VOLUME(c2,tc2);
    massfrac1_CH4 = C_YI(c1,tc1,0);
    massfrac2_CH4 = C_YI(c2,tc2,0);
    massfrac1_H2O = C_YI(c1,tc1,1);
    massfrac2_H2O = C_YI(c2,tc2,1);
    massfrac1_CO = C_YI(c1,tc1,2);
```

110 

```
    massfrac2_CO = C_YI(c2,tc2,2);
```

```
    massfrac1_H2 = C_YI(c1,tc1,3);
```

```
    massfrac2_H2 = C_YI(c2,tc2,3);
```

```
    massfrac1_CO2 = C_YI(c1,tc1,4);
```

```
    massfrac2_CO2 = C_YI(c2,tc2,4);
```

```
massfrac1_N2 = C_YI(c1,tc1,5);
```

```
    massfrac2_N2 = C_YI(c2,tc2,5);
```

```
molefrac1_H2=(massfrac1_H2/H2_mwt)/((massfrac1_CH4/CH4_mwt)
+(massfrac1_H2O/H2O_mwt)+(massfrac1_CO/CO_mwt)+(massfrac1_H
2/H2_mwt)+(massfrac1_CO2/CO2_mwt)+(massfrac1_N2/N2_mwt));
```

```
molefrac2_H2=(massfrac2_H2/H2_mwt)/((massfrac2_CH4/CH4_mwt)
+(massfrac2_H2O/H2O_mwt)+(massfrac2_CO/CO_mwt)+(massfrac2_H
2/H2_mwt)+(massfrac2_CO2/CO2_mwt)+(massfrac2_N2/N2_mwt));
```

```
P1 = molefrac1_H2*(C_P(c1,tc1)+P_0);
```

```
P2 = molefrac2_H2*(C_P(c2,tc2)+P_0);
```

```
     PP1=P1/P_0;
```

```
         PP2=P2/P_0;
```

```
  mass_flux = face_area * Ah * exp(-
10700/(8.314*C_T(c2,tc2)))*(pow(PP1,0.5)-pow(PP2,0.5));
```

```
    C_UDMI(c1,tc1,UDM_MASS_SOURCE) = -mass_flux /
cell_volume1;
```

```
    C_UDMI(c2,tc2,UDM_MASS_SOURCE) = +mass_flux /
cell_volume2;
```

```
    C_UDMI(c2,tc2,UDM_flux) = mass_flux;
```

```
C_UDMI(c2,tc2,UDM_fluxperarea) = mass_flux   }
```

```
  end_f_loop(f1,tf1)
```

```
}
```

111 

# **References** 

- [1] R. Soltani, M. A. Rosen, and I. Dincer, “Assessment of CO2 capture options from various points in steam methane reforming for hydrogen production,” _Int J Hydrogen Energy_ , vol. 39, no. 35, pp. 20266–20275, Dec. 2014, doi: 10.1016/j.ijhydene.2014.09.161. 

- [2] M. Boscherini, A. Storione, M. Minelli, F. Miccio, and F. Doghieri, “New Perspectives on Catalytic Hydrogen Production by the Reforming, Partial Oxidation and Decomposition of Methane and Biogas,” Sep. 01, 2023, _Multidisciplinary Digital Publishing Institute (MDPI)_ . doi: 10.3390/en16176375. 

- [3] S. E. Hosseini and M. A. Wahid, “Hydrogen production from renewable and sustainable energy resources: Promising green energy carrier for clean development,” May 01, 2016, _Elsevier Ltd_ . doi: 10.1016/j.rser.2015.12.112. 

- [4] M. K. Sarmah, T. P. Singh, P. Kalita, and A. Dewan, “Sustainable hydrogen generation and storage - a review,” Aug. 23, 2023, _Royal Society of Chemistry_ . doi: 10.1039/d3ra04148d. 

- [5] T. da Silva Veras, T. S. Mozer, D. da Costa Rubim Messeder dos Santos, and A. da Silva César, “Hydrogen: Trends, production and characterization of the main process worldwide,” Jan. 26, 2017, _Elsevier Ltd_ . doi: 10.1016/j.ijhydene.2016.08.219. 

- [6] P. A. Le, V. D. Trung, P. L. Nguyen, T. V. Bac Phung, J. Natsuki, and T. Natsuki, “The current status of hydrogen energy: an overview,” Sep. 25, 2023, _Royal Society of Chemistry_ . doi: 10.1039/d3ra05158g. 

- [7] T. L. Levalley, A. R. Richard, and M. Fan, “The progress in water gas shift and steam reforming hydrogen production technologies - A review,” Oct. 13, 2014, _Elsevier Ltd_ . doi: 10.1016/j.ijhydene.2014.08.041. 

- [8] S. Masoudi Soltani, A. Lahiri, H. Bahzad, P. Clough, M. Gorbounov, and Y. Yan, “Sorption-enhanced Steam Methane Reforming for Combined CO2 Capture and Hydrogen Production: A State-of-the-Art Review,” Dec. 01, 2021, _Elsevier Ltd_ . doi: 10.1016/j.ccst.2021.100003. 

- [9] M. A. Nemitallah, “Characteristics of hydrogen separation and methane steam reforming in a Pd-based membrane reactor of shell and tube design,” _Case Studies in Thermal Engineering_ , vol. 45, May 2023, doi: 10.1016/j.csite.2023.102939. 

112 

- [10] O. O. Yolcan, “World energy outlook and state of renewable energy: 10-Year evaluation,” _Innovation and Green Development_ , vol. 2, no. 4, p. 100070, Dec. 2023, doi: 10.1016/J.IGD.2023.100070. 

- [11] I. Mezghani and H. Ben Haddad, “Energy consumption and economic growth: An empirical study of the electricity consumption in Saudi Arabia,” _Renewable and Sustainable Energy Reviews_ , vol. 75, pp. 145–156, 2017, doi: 10.1016/j.rser.2016.10.058. 

- [12] T. da Silva Veras, T. S. Mozer, D. da Costa Rubim Messeder dos Santos, and A. da Silva César, “Hydrogen: Trends, production and characterization of the main process worldwide,” _Int J Hydrogen Energy_ , vol. 42, no. 4, pp. 2018–2033, Jan. 2017, doi: 10.1016/J.IJHYDENE.2016.08.219. 

- [13] J. Nowotny and T. N. Veziroglu, “Impact of hydrogen on the environment,” _Int J Hydrogen Energy_ , vol. 36, no. 20, pp. 13218–13224, Oct. 2011, doi: 10.1016/J.IJHYDENE.2011.07.071. 

- [14] F. Frieden and J. Leker, “Future costs of hydrogen: a quantitative review,” Mar. 25, 2024, _Royal Society of Chemistry_ . doi: 10.1039/d4se00137k. 

- [15] A. Pal, S. Kakran, A. Kumar, A. Ben Youssef, U. P. Singh, and A. Sidhu, “Powering squarely into the future: A strategic analysis of hydrogen energy in QUAD nations,” Jan. 02, 2024, _Elsevier Ltd_ . doi: 10.1016/j.ijhydene.2023.06.169. 

- [16] F. Suleman, I. Dincer, and M. Agelin-Chaab, “Environmental impact assessment and comparison of some hydrogen production options,” _Int J Hydrogen Energy_ , vol. 40, no. 21, pp. 6976–6987, Jun. 2015, doi: 10.1016/J.IJHYDENE.2015.03.123. 

- [17] P. K. Pathak, A. K. Yadav, and S. Padmanaban, “Transition toward emission-free energy systems by 2050: Potential role of hydrogen,” _Int J Hydrogen Energy_ , vol. 48, no. 26, pp. 9921–9927, Mar. 2023, doi: 10.1016/J.IJHYDENE.2022.12.058. 

- [18] Q. Hassan, A. Z. Sameen, H. M. Salman, M. Jaszczur, M. Al-Hitmi, and M. Alghoul, “Energy futures and green hydrogen production: Is Saudi Arabia trend?,” _Results in Engineering_ , vol. 18, p. 101165, Jun. 2023, doi: 10.1016/J.RINENG.2023.101165. 

- [19] M. I. Khan and S. G. Al-Ghamdi, “Hydrogen economy for sustainable development in GCC countries: A SWOT analysis considering current situation, challenges, and prospects,” _Int J Hydrogen Energy_ , vol. 48, no. 28, pp. 10315– 10344, Apr. 2023, doi: 10.1016/J.IJHYDENE.2022.12.033. 

113 

- [20] B. Su, Y. Wang, Z. Xu, W. Han, H. Jin, and H. Wang, “Novel ways for hydrogen production based on methane steam and dry reforming integrated with carbon capture,” _Energy Convers Manag_ , vol. 270, Oct. 2022, doi: 10.1016/j.enconman.2022.116199. 

- [21] M. Sinaei Nobandegani, M. R. Sardashti Birjandi, T. Darbandi, M. M. Khalilipour, F. Shahraki, and D. Mohebbi-Kalhori, “An industrial Steam Methane Reformer optimization using response surface methodology,” _J Nat Gas Sci Eng_ , vol. 36, pp. 540–549, Nov. 2016, doi: 10.1016/j.jngse.2016.10.031. 

- [22] X. Peng and Q. Jin, “Molecular simulation of methane steam reforming reaction for hydrogen production,” _Int J Hydrogen Energy_ , vol. 47, no. 12, pp. 7569–7585, Feb. 2022, doi: 10.1016/j.ijhydene.2021.12.105. 

- [23] A. L. García-Lario, G. S. Grasa, and R. Murillo, “Performance of a combined CaO-based sorbent and catalyst on H2 production, via sorption enhanced methane steam reforming,” _Chemical Engineering Journal_ , vol. 264, pp. 697–705, Mar. 2015, doi: 10.1016/j.cej.2014.11.116. 

- [24] A. Neni, Y. Benguerba, M. Balsamo, A. Erto, B. Ernst, and D. Benachour, “Numerical study of sorption-enhanced methane steam reforming over Ni/Al2O3 catalyst in a fixed-bed reactor,” _Int J Heat Mass Transf_ , vol. 165, Feb. 2021, doi: 10.1016/j.ijheatmasstransfer.2020.120635. 

- [25] L. Lao, A. Aguirre, A. Tran, Z. Wu, H. Durand, and P. D. Christofides, “CFD modeling and control of a steam methane reforming reactor,” _Chem Eng Sci_ , vol. 148, pp. 78–92, Jul. 2016, doi: 10.1016/j.ces.2016.03.038. 

- [26] I. Aloisi, N. Jand, S. Stendardo, and P. U. Foscolo, “Hydrogen by sorption enhanced methane reforming: A grain model to study the behavior of bi-functional sorbent-catalyst particles,” Jul. 31, 2016, _Elsevier Ltd_ . doi: 10.1016/j.ces.2016.03.042. 

- [27] J. Xu, G.F. Froment, Methane steam reforming, methanation and water-gas shift: I. Intrinsic kinetics, AIChE J. 35 (1989) 88–96. 

- [28] S. Z. Abbas, V. Dupont, and T. Mahmud, “Kinetics study and modelling of steam methane reforming process over a NiO/Al2O3 catalyst in an adiabatic packed bed reactor,” _Int J Hydrogen Energy_ , vol. 42, no. 5, pp. 2889–2903, Feb. 2017, doi: 10.1016/j.ijhydene.2016.11.093. 

- [29] J. Easa, C. Yan, W. F. Schneider, and C. P. O’Brien, “CO and C3H6 poisoning of hydrogen permeation across Pd77Ag23 alloy membranes: A comparative study 

114 

with pure palladium,” _Chemical Engineering Journal_ , vol. 430, p. 133080, Feb. 2022, doi: 10.1016/J.CEJ.2021.133080. 

- [30] J. Wallis _et al._ , “Structural and electrical properties of BaZr0.7Ce0.2Y0.1O3−δ proton conducting ceramic fabricated by spark plasma sintering,” _Solid State Ion_ , vol. 345, p. 115118, Feb. 2020, doi: 10.1016/J.SSI.2019.115118. 

- [31] G. M. Jaid, A. A. AbdulRazak, H. Meskher, S. Al-Saadi, and Q. F. Alsalhy, “Metal-organic frameworks (MOFs), covalent organic frameworks (COFs), and hydrogen-bonded organic frameworks (HOFs) in mixed matrix membranes,” _Materials Today Sustainability_ , vol. 25, p. 100672, Mar. 2024, doi: 10.1016/J.MTSUST.2024.100672. 

- [32] R. B. Merlet, M. A. Pizzoccaro-Zilamy, A. Nijmeijer, and L. Winnubst, “Hybrid ceramic membranes for organic solvent nanofiltration: State-of-the-art and challenges,” _J Memb Sci_ , vol. 599, p. 117839, Apr. 2020, doi: 10.1016/J.MEMSCI.2020.117839. 

- [33] S. K. Ryi, J. S. Park, S. H. Kim, S. H. Cho, D. W. Kim, and K. Y. Um, “Characterization of Pd–Cu–Ni ternary alloy membrane prepared by magnetron sputtering and Cu-reflow on porous nickel support for hydrogen separation,” _Sep Purif Technol_ , vol. 50, no. 1, pp. 82–91, Jun. 2006, doi: 10.1016/J.SEPPUR.2005.11.024. 

- [34] S. Li _et al._ , “Recent Advances in Polymer-Inorganic Mixed Matrix Membranes for CO2 Separation,” _Polymers 2021, Vol. 13, Page 2539_ , vol. 13, no. 15, p. 2539, Jul. 2021, doi: 10.3390/POLYM13152539. 

- [35] R. Ben-Mansour _et al._ , “Comprehensive parametric investigation of methane reforming and hydrogen separation using a CFD model,” _Energy Convers Manag_ , vol. 249, Dec. 2021, doi: 10.1016/j.enconman.2021.114838. 

- [36] M. Upadhyay, H. Lee, A. Kim, S. hun Lee, and H. Lim, “CFD simulation of methane steam reforming in a membrane reactor: Performance characteristics over range of operating window,” _Int J Hydrogen Energy_ , vol. 46, no. 59, pp. 30402– 30411, Aug. 2021, doi: 10.1016/j.ijhydene.2021.06.178. 

- [37] A. Basile _et al._ , “Methane steam reforming in a Pd-Ag membrane reformer: An experimental study on reaction pressure influence at middle temperature,” _Int J Hydrogen Energy_ , vol. 36, no. 2, pp. 1531–1539, Jan. 2011, doi: 10.1016/j.ijhydene.2010.10.101. 

115 

- [38] Y. Chen, Y. Wang, H. Xu, and G. Xiong, “Efficient production of hydrogen from natural gas steam reforming in palladium membrane reactor,” _Appl Catal B_ , vol. 81, no. 3–4, pp. 283–294, Jun. 2008, doi: 10.1016/j.apcatb.2007.10.024. 

- [39] M. De Falco, G. Iaquaniello, and A. Salladini, “Experimental tests on steam reforming of natural gas in a reformer and membrane modules (RMM) plant,” _J Memb Sci_ , vol. 368, no. 1–2, pp. 264–274, Feb. 2011, doi: 10.1016/j.memsci.2010.11.050. 

- [40] A. Iulianelli _et al._ , “H2 production by low pressure methane steam reforming in a Pd-Ag membrane reactor over a Ni-based catalyst: Experimental and modeling,” _Int J Hydrogen Energy_ , vol. 35, no. 20, pp. 11514–11524, Oct. 2010, doi: 10.1016/j.ijhydene.2010.06.049. 

- [41] M. Sarić, Y. C. Van Delft, R. Sumbharaju, D. F. Meyer, and A. De Groot, “Steam reforming of methane in a bench-scale membrane reactor at realistic working conditions,” in _Catalysis Today_ , Oct. 2012, pp. 74–80. doi: 10.1016/j.cattod.2012.04.009. 

- [42] Y. M. Lin, S. L. Liu, C. H. Chuang, and Y. T. Chu, “Effect of incipient removal of hydrogen through palladium membrane on the conversion of methane steam reforming: Experimental and modeling,” in _Catalysis Today_ , Jul. 2003, pp. 127– 139. doi: 10.1016/S0920-5861(03)00212-8. 

- [43] T. Chompupun, S. Limtrakul, T. Vatanatham, C. Kanhari, and P. A. Ramachandran, “Experiments, modeling and scaling-up of membrane reactors for hydrogen production via steam methane reforming,” _Chemical Engineering and Processing - Process Intensification_ , vol. 134, pp. 124–140, Dec. 2018, doi: 10.1016/j.cep.2018.10.007. 

- [44] C.-H. Kim, J.-Y. Han, H. Lim, D.-W. Kim, and S.-K. Ryi, “Methane steam reforming in a membrane reactor using high-permeable and low-selective Pd-Ru membrane,” _Korean Journal of Chemical Engineering_ , vol. 34, no. 4, pp. 1260– 1265, 2017, doi: 10.1007/s11814-016-0359-0. 

- [45] B. Anzelmo, J. Wilcox, and S. Liguori, “Hydrogen production via natural gas steam reforming in a Pd-Au membrane reactor. Comparison between methane and natural gas steam reforming reactions,” _J Memb Sci_ , vol. 568, pp. 113–120, Dec. 2018, doi: 10.1016/j.memsci.2018.09.054. 

- [46] A. A. Albasry _et al._ , “Membrane reformer technology for sustainable hydrogen production from hydrocarbon feedstocks,” _Int J Hydrogen Energy_ , 2024, doi: 10.1016/j.ijhydene.2024.10.257. 

116 

- [47] H. W. Abu El Hawa, S. T. B. Lundin, N. S. Patki, and J. Douglas Way, “Steam methane reforming in a Pd-Au membrane reactor: Long-term assessment,” _Int J Hydrogen Energy_ , vol. 41, no. 24, pp. 10193–10201, Jun. 2016, doi: 10.1016/j.ijhydene.2016.04.244. 

- [48] R. Ben-Mansour _et al._ , “Comprehensive parametric investigation of methane reforming and hydrogen separation using a CFD model,” _Energy Convers Manag_ , vol. 249, Dec. 2021, doi: 10.1016/j.enconman.2021.114838. 

- [49] R. Y. Chein, Y. C. Chen, Y. P. Chyou, and J. N. Chung, “Three-dimensional numerical modeling on high pressure membrane reactors for high temperature water-gas shift reaction,” _Int J Hydrogen Energy_ , vol. 39, no. 28, pp. 15517– 15529, Sep. 2014, doi: 10.1016/j.ijhydene.2014.07.113. 

- [50] T. Chompupun, S. Limtrakul, T. Vatanatham, C. Kanhari, and P. A. Ramachandran, “Experiments, modeling and scaling-up of membrane reactors for hydrogen production via steam methane reforming,” _Chemical Engineering and Processing - Process Intensification_ , vol. 134, pp. 124–140, Dec. 2018, doi: 10.1016/j.cep.2018.10.007. 

- [51] G. Ji, M. Zhao, and G. Wang, “Computational fluid dynamic simulation of a sorption-enhanced palladium membrane reactor for enhancing hydrogen production from methane steam reforming,” _Energy_ , vol. 147, pp. 884–895, Mar. 2018, doi: 10.1016/j.energy.2018.01.092. 

- [52] S. A. M. Said _et al._ , “Computational fluid dynamics study of hydrogen generation by low temperature methane reforming in a membrane reactor,” _Int J Hydrogen Energy_ , vol. 40, no. 8, pp. 3158–3169, Mar. 2015, doi: 10.1016/j.ijhydene.2015.01.024. 

- [53] M. Upadhyay, H. Lee, A. Kim, S. hun Lee, and H. Lim, “CFD simulation of methane steam reforming in a membrane reactor: Performance characteristics over range of operating window,” _Int J Hydrogen Energy_ , vol. 46, no. 59, pp. 30402– 30411, Aug. 2021, doi: 10.1016/j.ijhydene.2021.06.178. 

- [54] S. Kim _et al._ , “Steam reforming of methanol for ultra-pure H2 production in a membrane reactor: Techno-economic analysis,” _Int J Hydrogen Energy_ , pp. 2330– 2339, Jan. 2019, doi: 10.1016/j.ijhydene.2018.08.087. 

- [55] Y. Yan, V. Manovic, E. J. Anthony, and P. T. Clough, “Techno-economic analysis of low-carbon hydrogen production by sorption enhanced steam methane reforming (SE-SMR) processes,” _Energy Convers Manag_ , vol. 226, Dec. 2020, doi: 10.1016/j.enconman.2020.113530. 

117 

- [56] C. Joo, J. Lee, Y. Kim, H. Cho, B. Gu, and J. Kim, “A novel on-site SMR process integrated with a hollow fiber membrane module for efficient blue hydrogen production: Modeling, validation, and techno-economic analysis,” _Appl Energy_ , vol. 354, Jan. 2024, doi: 10.1016/j.apenergy.2023.122227. 

- [57] D. M. Sweeney, V. Alves, S. Sakhai, S. Dinh, and F. V. Lima, “Techno-economic Analysis and Optimization of Intensified, Large-Scale Hydrogen Production with Membrane Reactors,” _Ind Eng Chem Res_ , vol. 62, no. 46, pp. 19740–19751, Nov. 2023, doi: 10.1021/acs.iecr.3c02045. 

- [58] A. Giaconia, G. Iaquaniello, B. Morico, A. Salladini, and E. Palo, “Technoeconomic assessment of solar steam reforming of methane in a membrane reactor using molten salts as heat transfer fluid,” _Int J Hydrogen Energy_ , vol. 46, no. 71, pp. 35172–35188, Oct. 2021, doi: 10.1016/j.ijhydene.2021.08.096. 

- [59] D. Pashchenko, “Effect of the geometric dimensionality of computational domain on the results of CFD-modeling of steam methane reforming,” _Int J Hydrogen Energy_ , vol. 43, no. 18, pp. 8662–8673, May 2018, doi: 10.1016/j.ijhydene.2018.03.183. 

- [60] Ansys Fluent Theory Guide, “Ansys Fluent Theory Guide,” _ANSYS Inc., USA_ , vol. 15317, no. November, 2021. 

- [61] D. L. Hoang, S. H. Chan, and O. L. Ding, “Kinetic and modelling study of methane steam reforming over sulfide nickel catalyst on a gamma alumina support,” _Chemical Engineering Journal_ , vol. 112, no. 1–3, pp. 1–11, Sep. 2005, doi: 10.1016/j.cej.2005.06.004. 

- [62] A. Iulianelli, S. Liguori, J. Wilcox, and A. Basile, “Advances on methane steam reforming to produce hydrogen through membrane reactors technology: A review,” _Catal Rev Sci Eng_ , vol. 58, no. 1, pp. 1–35, Jan. 2016, doi: 10.1080/01614940.2015.1099882. 

- [63] S. ’Ghulam, M. I. ’Abdus, “9 - Fundamentals of fluid flow through porous media,” _Reservoir Engineering_ . 

- [64] Z. Bian _et al._ , “A CFD study on H2-permeable membrane reactor for methane CO2 reforming: Effect of catalyst bed volume,” _Int J Hydrogen Energy_ , vol. 46, no. 77, pp. 38336–38350, Nov. 2021, doi: 10.1016/j.ijhydene.2021.09.098. 

118 

# **Vitae** 

|**Name**|: Minas Mohammad Al-Rashdan|
|---|---|
|**Nationality**|: Jordanian|
|**Date of Birth**|: 07/24/1990|
|**Email**|: minasalrshdan@gmail.com|
|**Addres**s|: Irbid, Jordan|



**Academic Background** : 

- **Master of Science (MSc) in Chemical Engineering** , 2024 

King Fahd University of Petroleum and Minerals (KFUPM), Saudi Arabia 

- **Bachelor of Science (BSc) in Chemical Engineering** , 2013 

Jordan University of Science and Technology (JUST), Jordan 

**Research Interests** : 

- Hydrogen production and separation processes 

- Process simulation and optimization 

**Submitted Paper** : 

- Minas M. Alrshdana, Medhat A. Nemitallah, and Usama Ahmed, Process 

   - Intensification of Hydrogen Production via Steam Methane Reforming with Palladium Membrane Technology 

119 

• Minas M. Alrshdana, Medhat A. Nemitallah, and Usama Ahmed, Features of steam methane reforming and hydrogen separation in a shell-and-tube-designed Palladium-based membrane reactor for blue hydrogen production, ESCAPE 35 - European Symposium on Computer Aided Process Engineering 

#### **Technical Skills & Software Proficiency** : 

- Process Simulation: ASPEN HYSYS, ANSYS Fluent 

- Data Analysis: MATLAB, Tecplot 

120 

