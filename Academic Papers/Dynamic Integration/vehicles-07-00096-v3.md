

_Article_ 

# **Dynamic Load Optimization of PEMFC Stacks for FCEVs: A Data-Driven Modelling and Digital Twin Approach Using NSGA-II** 

**Balasubramanian Sriram**<sup>**1**</sup> **, Saeed Shirazi**<sup>**2**</sup> **, Christos Kalyvas**<sup>**1**</sup> **, Majid Ghassemi**<sup>**2**</sup> **and Mahmoud Chizari**<sup>**1,**</sup> ***** 

- 1 School of Physics, Engineering and Computer Science, College Lane Campus, University of Hertfordshire, Hatfield AL10 9AB, UK 

- 2 School of Mechanical Engineering, KN Toosi University of Technology, Tehran 19697-64499, Iran 

- Correspondence: m.chizari@herts.ac.uk 

### **Abstract** 

Academic Editor: Weixiang Shen Received: 13 July 2025 Revised: 2 September 2025 Accepted: 4 September 2025 Published: 7 September 2025 

**Citation:** Sriram, B.; Shirazi, S.; Kalyvas, C.; Ghassemi, M.; Chizari, M. Dynamic Load Optimization of PEMFC Stacks for FCEVs: A Data-Driven Modelling and Digital Twin Approach Using NSGA-II. _Vehicles_ **2025** , _7_ , 96. https://doi.org/ 10.3390/vehicles7030096 

**Copyright:** © 2025 by the authors. Licensee MDPI, Basel, Switzerland. This article is an open access article distributed under the terms and conditions of the Creative Commons Attribution (CC BY) license (https://creativecommons.org/ licenses/by/4.0/). 

This study presents a machine learning-enhanced optimization framework for proton exchange membrane fuel cell (PEMFC), designed to address critical challenges in dynamic load adaptation and thermal management for automotive applications. A high-fidelity model of a 65-cell stack (45 V, 133.5 A, 6 kW) is developed in MATLAB/Simulink, integrating four core subsystems: PID-controlled fuel delivery, humidity-regulated air supply, an electrochemical-thermal stack model (incorporating Nernst voltage and activation, ohmic, and concentration losses), and a 97.2–efficient SiC MOSFET-based DC/DC boost converter. The framework employs the NSGA-II algorithm to optimize key operational parameters—membrane hydration (λ = 12–14), cathode stoichiometry (λO2 = 1.5–3.0), and cooling flow rate (0.5–2.0 L/min)—to balance efficiency, voltage stability, and dynamic performance. The optimized model achieves a 38% reduction in model-data discrepancies (RMSE < 5.3%) compared to experimental data from the Toyota Mirai, and demonstrates a 22% improvement in dynamic response, recovering from 0 to 100% load steps within 50 ms with a voltage deviation of less than 0.15 V. Peak performance includes 77.5% oxygen utilization at 250 L/min air flow (1.1236 V/cell) and 99.89% hydrogen utilization at a nominal voltage of 48.3 V, yielding a peak power of 8112 W at 55% stack efficiency. Furthermore, fuzzy-PID control of fuel ramping (50–85 L/min in 3.5 s) and thermal management (∆T < 1.5<sup>_◦_</sup> C via 1.0–1.5 L/min cooling) reduces computational overhead by 29% in the resulting digital twin platform. The framework demonstrates compliance with ISO 14687-2 and SAE J2574 standards, offering a scalable and efficient solution for next-generation fuel cell electric vehicle (FCEV) aligned with global decarbonization targets, including the EU’s 2035 CO2 neutrality mandate. 

**Keywords:** PEMFC; dynamic load response; NSGA-II optimization; Nernst voltage; stoichiometry; digital twin; SiC MOSFET; FCEV; thermal management 

## **1. Introduction** 

Data-driven optimization of fuel cell systems plays a pivotal role in advancing nextgeneration electrified powertrains, offering significant improvements in efficiency, performance, and sustainability. FCEV represent a promising pathway toward sustainable transportation; however, their widespread adoption hinges on overcoming both technical and policy-related challenges [1]. The transportation sector accounts for nearly 25% of global CO2 emissions as reported by International Energy Agency (https://www.iea.org, 

_Vehicles_ **2025** , _7_ , 96 

https://doi.org/10.3390/vehicles7030096 

_Vehicles_ **2025** , _7_ , 96 

2 of 22 

accessed on 12 July 2025), placing it at the centre of global climate change mitigation efforts. With stringent regulations such as the EU’s 2035 CO2 neutrality mandate and the U.S. Clean Air Act, automakers are under increasing pressure to decarbonize vehicle powertrains. 

While battery electric vehicles (BEVs) currently dominate the market, they face limitations including limited driving range, long charging times, and vulnerabilities in the lithium supply chain. These constraints highlight the need for complementary electrification strategies. Among them, FCEV powered by PEMFC stand out as a transformative alternative, offering over 500 km of range, refuelling times of 3–5 min, and zero tailpipe emissions [2]. 

Despite these advantages, PEMFCs encounter critical challenges related to dynamic load response—an essential requirement for automotive applications. Sudden power demands during acceleration, hill climbing, or regenerative braking can lead to issues such as fuel starvation, water flooding, or thermal instability, which degrade system efficiency and longevity [3]. The model-based optimization of cooling system parameters reinforces the value of advanced thermal management strategies [4], and the introduction of optimal temperature-tracking methods by researchers [5] helps reduce parasitic losses while sustaining stable PEMFC operation. However, recent automotive stack experiments confirm that highly dynamic load steps continue to pose one of the most significant challenges for PEMFC integration [3]. Addressing these challenges necessitates high-fidelity models that accurately simulate real-world conditions, along with adaptive optimization frameworks capable of balancing competing objectives such as efficiency, durability, and cost-effectiveness. Traditional modelling approaches, such as the Motapon et al. (2012) [6] framework, often prioritize simplicity at the expense of capturing complex transient behaviours crucial for automotive integration. These oversimplified representations may fail to adequately model the dynamic phenomena required for effective vehicle-level deployment. Although the experimental studies have shown that repeated load cycling accelerates efficiency decay and validates the importance of high-fidelity models for transient prediction [7]. 

This study introduces a novel machine learning-aided parametric optimization pipeline specifically tailored for PEMFC applications in the automotive industry. Although, recent studies have demonstrated the integration of artificial intelligence with fuel cell modelling, such as the work of [8], who applied AI to enhance the performance prediction of micro solid oxide fuel cells. By integrating genetic algorithms and surrogate modelling techniques, we systematically calibrate key operational parameters—including membrane hydration, oxygen stoichiometry, and thermal gradients—against experimental datasets. This approach achieves a 38% improvement in predictive accuracy compared to conventional methods. The scalability of the proposed framework is demonstrated through a case study involving a fuel cell-powered electric golf cart, a practical platform for validating control strategies under variable load profiles. Our findings enhance the dynamic responsiveness of PEMFC models and establish a digital twin foundation for optimizing vehicle-level energy management systems (EMS). At the supervisory level, fuzzy logic has been used in health-aware EMS for fuel cell hybrid vehicles, resulting in reduced hydrogen consumption and extended stack life [9]. Although, digital twin–enhanced control has been applied to fuel cell–battery hybrids, leading to improved system-wide efficiency and adaptability [10]. Similar data-driven digital twin frameworks for fuel cells, including solid oxide fuel cells (SOFCs), confirm the value of machine-learning regressors for real-time prediction [11]. 

The methodology bridges the critical gap between component-level fuel cell modelling and system-level vehicle integration, providing actionable insights for automakers aiming to develop ISO 26262-compliant (https://www.iso.org/standard/68388.html, accessed on 12 July 2025) control systems and deploy FCEVs in a cost-effective manner. ISO 26262, an 

_Vehicles_ **2025** , _7_ , 96 

3 of 22 

international standard for functional safety in road vehicles, ensures that electronic and electrical systems—such as those used in fuel cell control—are designed and operated to prevent hazards arising from system malfunctions. Adherence to this standard is vital for ensuring the safe and reliable operation of advanced technologies like FCEVs. 

While this study focuses on automotive fuel cell applications, broader research—such as that conducted by [12] —confirms the versatility of fuel cell technology across both stationary and mobile energy systems. Recent literature also underscores the growing importance of system-level modelling and control strategies in fuel cell applications. Mitra et al. (2021) [13] present a comprehensive review of fuel cell technologies, emphasizing their adaptability across diverse energy platforms and reinforcing the need for advanced control strategies to enhance performance in dynamic environments. 

Transitioning toward hydrogen-based mobility involves more than technological innovation—it also requires addressing behavioural and infrastructural factors. Insights into consumer adoption patterns, as highlighted by Hardman et al. (2017) [14], can guide strategic investments in hydrogen refuelling infrastructure and public incentives. 

The potential of FCEVs to complement BEVs in achieving global decarbonization targets has gained widespread recognition. As noted by Hassan et al. (2023) [15], overcoming current technological and logistical barriers will require coordinated efforts across research, industry, and policy-making sectors. 

Moreover, efficient hydrogen utilization depends not only on electrochemical performance but also on robust storage and delivery infrastructure. Dafedar et al. (2021) [16] emphasize that hydrogen storage technologies must evolve to meet the demands of real-world FCEV operation, particularly with respect to weight, volume, and refuelling convenience. 

The proposed optimization framework benefits a wide range of stakeholders across the automotive and energy sectors. Automakers can leverage it to design more efficient and durable FCEVs with reduced development costs. Energy planners may apply it to model large-scale hydrogen mobility scenarios, while policymakers can use its insights to craft regulations aligned with international climate goals, including the EU’s 2035 CO2 neutrality mandate and the U.S. Clean Air Act. 

While the base model provides a solid foundation, it does not address dynamic load adaptation, multi-objective optimization, or digital twin integration—key requirements for modern FCEVs. This study bridges that gap by introducing an enhanced framework that combines NSGA-II optimization, fuzzy-PID control, and a real-time digital twin platform, significantly improving dynamic performance and system efficiency. 

## **2. Methodology** 

This research presents a data-driven parametric optimization framework for PEMFC systems, developed using MATLAB/Simulink 2024a (MathWorks, n.d.) to enable highfidelity simulations of automotive powertrains. The modelling framework is built upon a foundational PEMFC model adapted from Motapon et al. (2012) [6], which represents a 65-cell stack with a nominal voltage of 45 V, a current of 133.5 A, and a power output of 6 kW. This configuration is representative of mid-power fuel cell systems used in light-duty FCEV and serves as the baseline for dynamic performance evaluation. 

To ensure the model’s relevance to real-world applications, all simulations are conducted under operating conditions compliant with the ISO 14687 standard (https: //www.iso.org/standard/82660.html, accessed on 12 July 2025). Specifically, the fuel (H2) is supplied at a pressure of 1.5 bar, with a tolerance of _±_ 0.05 bar, while the air pressure is maintained at 1 bar ( _±_ 0.03 bar). The stack temperature is controlled at 65<sup>_◦_</sup> C with a stability of _±_ 1<sup>_◦_</sup> C, reflecting typical thermal management strategies in commercial FCEVs. 

_Vehicles_ **2025** , _7_ , 96 

4 of 22 

Reactant purity is set to 99.95% for hydrogen and 21% for oxygen in air, in accordance with hydrogen quality standards for automotive fuel cells. 

These operating parameters were selected to align with SAE J2574 (https://www.sae. org/standards/content/j2574_201109/, accessed on 12 July 2025), a widely recognized standard developed by the Society of Automotive Engineers for fuel cell system testing and performance evaluation. Adherence to these standards ensures that the model’s behaviour is consistent with real-world FCEV platforms, such as the Toyota Mirai, and supports its use in system-level integration studies, control system design, and digital twin development. 

The overall architecture of the PEMFC model comprises four core subsystems: the Fuel Flow Regulator (FFR), Air Supply System (ASS), Fuel Cell Stack (FCS), and DC/DC Boost Converter (DBC), as illustrated in Figure 1. Each subsystem is parameterized and validated to replicate transient behaviour under dynamic automotive load profiles, enabling a comprehensive analysis of efficiency, stability, and responsiveness. 



<!-- Start of picture text -->
Input: Output:<br>1. Air flow rate 1. Voltage<br>2. Fuel flow rate 2. Current<br>I/P<br>-100v<br>Bus current &<br>Fuel cell stack DC/DC conventor RC circuit<br>Bus voltage<br><!-- End of picture text -->

**Figure 1.** Integrated workflow of the PEMFC model, included with the core subsystems: Fuel Flow Regulator, Air Supply System, Fuel Cell Stack, and DC/DC Boost Converter. 

### _2.1. Model Architecture and Dynamic Subsystems_ 

The proposed PEMFC model is structured into four interconnected subsystems to accurately capture dynamic behaviour under real-world driving conditions. The FFR employs a PID-controlled mass flow controller to adjust hydrogen supply based on stack demand. To prevent pressure shocks during startup, a ramp function ensures a linear transition from 50 to 85 L/min over 3.5 s. The fuzzy-PID controllers have already been demonstrated to improve voltage tracking in hydrogen vehicle power systems [17]. The control logic integrates fuzzy-PID feedback to dynamically adjust the flow rate in response to variations in stack current (133.5 A _±_ 5%), enhancing system responsiveness and fuel efficiency. 

The ASS maintains optimal oxygen stoichiometry (λO2 = 2.0–2.5) through a variablespeed compressor, while a proportional-integral (PI) controller sustains membrane hydration at λ = 13.5 (95% RH). This dual-control strategy ensures robustness against rapid load fluctuations, including step changes from 0% to 100% within 50 milliseconds. 

The FCS comprises 65 cells in series, modelled using multiphysics equations that couple Nernst voltage with activation, ohmic, and concentration losses. Thermal dynamics are captured using a lumped capacitance method, with cooling flow adjustments (1.0–1.5 L/min) mitigating temperature spikes (∆T < 1.5<sup>_◦_</sup> C) and preserving membrane integrity. 

Finally, the DBC features a 97.2% efficient SiC MOSFET and a sliding mode controller (SMC) to regulate output voltage. It interfaces with the Controller Area Network (CAN bus) and supports regenerative braking by managing bidirectional power flow, making it suitable for automotive applications. Although, SiC MOSFETs have demonstrated 

_Vehicles_ **2025** , _7_ , 96 

5 of 22 

superior efficiency and lower switching losses compared to Si IGBTs in EV traction inverters, supporting their use in high-efficiency converters [18]. 

Although researchers Alpaslan et al. (2023) [19] introduced a control method for a hybrid system comprising a fuel cell, battery, and supercapacitor, this study employs a Model Predictive Controller (MPC). The MPC dynamically adjusts the FFR and ASS to maintain voltage deviations below 0.2V and keep O2 stoichiometry within the range of λO2 = 2.0–2.5. This approach ensures robustness against rapid load fluctuations, including step changes from 0% to 100% within 50 milliseconds. The use of supercapacitors alongside fuel cells has been shown to improve regenerative braking efficiency and load-following capability [10]. In their study, Armenta-Déu and Arenas (2023) [20] evaluated a fuel cellsupercapacitor hybrid system and reported enhanced transient response and reduced fuel consumption. 

The air supplied to the cathode is pre-humidified to 95% relative humidity (RH) to ensure rapid and uniform membrane hydration. A PI controller adjusts the humidification level in real time to maintain optimal water balance across varying load conditions. 

The hydrogen flow rate is controlled to maintain an anode stoichiometry (λH2) of 1.2–1.5, ensuring high fuel utilization while preventing fuel starvation under dynamic loads. 

### _2.2. Parametric Optimization Pipeline_ 

The Non-dominated Sorting Genetic Algorithm II (NSGA-II) is a widely adopted multiobjective evolutionary algorithm, renowned for its ability to generate a well-distributed Pareto front while maintaining computational efficiency. Meta-heuristic algorithms such as Genetic Algorithm (GA) and Particle Swarm Optimization (PSO) have been successfully applied to calibrate PEMFC model parameters for higher predictive accuracy [21]. It has been extensively applied in the optimization of fuel cell systems, where multiple conflicting objectives—such as maximizing efficiency and minimizing dynamic response time—must be balanced. Changizian et al. (2020) [22] demonstrated its effectiveness in enhancing the performance of hybrid hydrogen fuel cell-electric vehicles under real-world driving conditions, showing that careful tuning of operational parameters can significantly improve both system efficiency and dynamic responsiveness. 

In this study, NSGA-II is employed to simultaneously optimize two key performance metrics: system efficiency and voltage stability under dynamic load conditions. The primary objective is to maximize system efficiency, defined as the ratio of electrical power output to the chemical energy input from hydrogen: 



where _m_ . _H_ 2 represents the mass flow rate of hydrogen (kg/s), and _LHV H_ 2 is the lower heating value of hydrogen, taken as approximately 120 MJ/kg. The secondary objective is to minimize voltage ripple (∆V) during transient load changes, particularly under the New European Driving Cycle (NEDC), which simulates real-world acceleration, cruising, and deceleration events. 

The optimization process considers three key decision variables: membrane water content (λ = 12–14), cathode stoichiometry (λO2 = 1.5–3.0), and cooling flow rate (Q = 0.5–2.0 L/min). 

Although the simplified stoichiometry–voltage models further highlight the sensitivity of cell voltage to air over-stoichiometry, underscoring the importance of λO2 tuning [23]. These parameters are critical in determining the electrochemical performance, water management, and thermal stability of the PEMFC stack. The algorithm was configured with a population size of 100, evolved over 200 generations, to ensure adequate exploration 

_Vehicles_ **2025** , _7_ , 96 

6 of 22 

of the solution space. A crossover probability of 0.9 and a mutation rate of 1/n (where n is the number of decision variables) were used to maintain genetic diversity and prevent premature convergence. Parent selection was performed using tournament selection with crowding distance, ensuring both elitism and solution diversity. 

The optimization workflow, illustrated in Figure 2, begins with the initialization of a random population of candidate solutions, followed by fitness evaluation based on the two objective functions. Subsequent steps include non-dominated sorting, crowding distance assignment, selection, crossover, and mutation to generate offspring. The combined parent and offspring populations are then truncated to form the next generation, and the process repeats until the maximum number of generations is reached. 



<!-- Start of picture text -->
Initialize Population Output Pareto<br>(Random solutions) +  Front<br>Evaluate Fitness (η, ΔV)<br>Yes<br>Selection<br>Non-dominated<br>(Tournament) + Create Offspring +  Offspring Pop.<br>Sorting & Crowding<br>Crossover +  Combine Parents  Reached?<br>Distance Assignment<br>Mutation<br><!-- End of picture text -->

**Figure 2.** Flowchart of the NSGA-II optimization process, illustrating the iterative evolution of solutions to balance system efficiency and voltage stability under dynamic load conditions. 

To ensure the validity and practical relevance of the optimized parameters, the resulting solutions were validated against experimental data from the Toyota Mirai’s PEMFC system and the National Renewable Energy Laboratory’s (NREL) H2FAST database [24]. The model achieved a RMSE of less than 5.3%, confirming its high predictive accuracy and suitability for real-world automotive applications. 

### _2.3. Model Specifications_ 

The PEMFC model integrates three core subsystems (Figure 3) to simulate electrochemicalthermal dynamics under automotive load profiles. Each component is parameterized using ISO 14687-2 standards and validated against experimental data from Toyota Mirai’s operational data [25]. The simulations comply with ISO 14687-2 standards for operating parameters like humidity, pressure, and temperature. Hydrogen purity, regulated by both ISO 14687-2 and SAE J2574 guidelines, plays a critical role in determining PEMFC performance. Arul Murugan and Brown (2015) [26] offer an in-depth review of analytical techniques for hydrogen quality assurance, highlighting the significance of contamination management in automotive contexts. 

The PEMFC stack model is based on the 65-cell, 6 kW, 45 Vdc stack developed by Motapon et al. (2012) [6], available in MATLAB/Simulink [27–33]. While this study is simulation-based, the model is validated against real-world operational data from the Toyota Mirai and adheres to ISO 14687-2 and SAE J2574 standards for automotive fuel cell systems. 

The nominal operating point of 45 V, 133.5 A, and 6 kW is used as a reference condition for model validation and parametric analysis. It does not imply constant operation, but rather a representative state under balanced load conditions. Transient behaviour and voltage stability are analysed in Section 3.3. 

The parameter space explored during NSGA-II optimization is summarized in Table 1, which lists the ranges, step sizes, and final optimal values for key operational variables. 

_Vehicles_ **2025** , _7_ , 96 

7 of 22 



<!-- Start of picture text -->
featovron fo)<br>Wl<i<isizaiencrnsrosen09 [O2(volom)onl Arion,H2Magental> Festiagnmp |<br>Stack E1 rey (%P s 1<br>— o<br>Supe<br>Fuel flow rate (Ipm) =<br>CZF mn Ramp Fi = 7<br>+m =o = sre . on<br>Fe_roain Fr.s00.ou _—" DC bus current<br>Flow rate selector [=] a { .|<br><!-- End of picture text -->



<!-- Start of picture text -->
Bes vate<br>Fuel Cell Stack 100Véc Boost<br>OCIDC Converter 3<br>{average valve) 5<br>Tora an<br><!-- End of picture text -->

**Figure 3.** Simplified Simscape/Simulink model of the PEMFC system based on Motapon et al. (2012) [6]. The model integrates three core subsystems: (1) FFR, (2) ASS, and (3) FCS. Key parameters are optimized using NSGA-II, with real-time validation against Toyota Mirai operational data. 

**Table 1.** NSGA-II optimization parameter space and optimal solutions. 

|**Parameter**|**Range (Min–Max)**|**Step Size**|**Optimal Value**|**Impact on Performance**|
|---|---|---|---|---|
|Membrane Hydration (λ)|12–14|0.1|13.2|Maximizes proton conductivity; prevents<br>drying/flooding|
|Cathode Stoichiometry<br>(λO2)|1.5–3.0|0.1|2.1|Balances O2 supply and parasitic load from<br>air compressor|
|Anode Stoichiometry<br>(λH2)|1.1–1.8|0.05|1.4|Prevents fuel starvation; minimizes<br>purge frequency|
|Cooling Flow Rate (Q)|0.5–2.0 L/min|0.1|1.3 L/min|Maintains∆T < 1.5 <sup>_◦_</sup>C; prevents thermal stress|
|Target Efficiency (η)|50–60%|—|55%|Achieved at 8112 W peak power output|
|Voltage Ripple (∆V)|—|—|<0.15 V|Achieved via fuzzy-PID control under<br>NEDC cycles|



Note: The NSGA-II algorithm evaluated over 20,000 parameter combinations across 200 generations. The optimal values represent solutions on the Pareto front that balance efficiency, stability, and dynamic response. 

### 2.3.1. Flow Control System: Adaptive Reactant Management 

The Adaptive Reactant Management subsystem is designed to maintain optimal stoichiometric balance between hydrogen and oxygen during dynamic load conditions, thereby mitigating critical operational risks such as fuel starvation and water flooding. This is achieved through coordinated control of fuel and air delivery systems, ensuring stable and efficient PEMFC operation across transient driving scenarios. 

The fuel flow regulation is managed through a FFR input system, which operates within an adjustable range of 50 to 85 L/min, using high-purity hydrogen (99.95%). To prevent pressure shocks during startup or rapid load changes, a ramp function is implemented to enable a smooth, linear transition over 3.5 s. The control logic integrates a fuzzy PID feedback mechanism that dynamically adjusts the hydrogen flow rate based on real-time stack current, which is maintained at a nominal value of 133.5 A with a _±_ 5% tolerance. This adaptive approach enhances system responsiveness while minimizing overshoot and oscillations. 

_Vehicles_ **2025** , _7_ , 96 

8 of 22 

On the cathode side, the Air Flow Regulator (AFR) employs a variable-speed compressor to maintain oxygen stoichiometry (λO2) within the optimal range of 2.0 to 2.5, ensuring sufficient oxidant supply without excessive parasitic power consumption. Humidity control is achieved through a proportional-integral (PI) controller that sustains membrane hydration at λ = 13.5, corresponding to 95% relative humidity. This level of hydration is critical for maintaining high proton conductivity and preventing membrane drying under high-current operation. 

The integration of a ramp-based transition with advanced PID/PI control strategies forms the core of the system’s design rationale. Simulation results under the NEDC demonstrate that this approach reduces transient voltage dips by 22% compared to conventional stepwise adjustments, significantly improving voltage stability and overall system performance. 

### 2.3.2. Fuel Cell Stack: Electrochemical-Thermal Coupling 

The integration of fuel cells with auxiliary energy storage systems is grounded in established principles from hybrid vehicle research. As demonstrated by Aslam et al. (2023) [34], optimal system sizing and effective hydrogen management are critical to achieving balanced performance and efficiency, particularly in small-scale fuel cell vehicles. Building on this foundation, the present study employs a 65-cell PEMFC stack connected in series, modelled using multiphysics equations to capture both electrochemical voltage losses and thermal dynamics under transient load conditions. 

The model is driven by two primary inputs: a hydrogen flow rate of 50.06 L/min, compliant with ISO 14687-2 standards, and an oxygen flow rate adjusted to maintain a cathode stoichiometry (λO2) between 2.0 and 2.5, ensuring stable electrochemical reactions while minimizing parasitic losses. The cell voltage is computed as the difference between the theoretical open-circuit voltage (Nernst potential) and three major sources of voltage loss: 



The Nernst voltage ( _ENernst_ ) is calculated based on reactant partial pressures: 



where _R_ is the gas constant (8.314 J/mol _·_ K), _T_ is the operating temperature in Kelvin, _F_ is Faraday’s constant (96485 C/mol), and _PH_ 2, _PO_ 2, and _PH_ 2 _O_ are the partial pressures of hydrogen, oxygen, and water vapor, respectively. 

Activation losses (ηactivation) arise from sluggish electrochemical kinetics and are modelled as 



where _i_ is the current density (A/cm<sup>2</sup> ), _io_ is the exchange current density, and _A_ is the Tafel slope. Ohmic losses (ηohmic) account for resistance in the membrane and interconnects: 



with _Rm_ representing membrane resistance (Ω _·_ cm<sup>2</sup> ). Concentration losses ( _ηconcentration_ ) become significant at high current densities and are expressed as 



where _iL_ is limiting current density. 

_Vehicles_ **2025** , _7_ , 96 

9 of 22 

The total power output of the stack is calculated as 



where Vstack = Ncells _×_ Vcell, yielding a nominal power of 6 kW at 45 V and 133.5 A. System efficiency ( _η_ ) is defined based on the lower heating value (LHV) of hydrogen: 



where _m_ . _H_ 2 is the mass flow rate of hydrogen (kg/s) and _LHV H_ 2 is approximately 120 MJ/kg. 

Thermal behaviour is modelled using a lumped capacitance approach, which predicts a temperature rise of 2–5<sup>_◦_</sup> C during pulsed load transients (0–100% in 50 ms). To maintain thermal stability, the cooling flow rate is optimized via the NSGA-II algorithm to keep the stack temperature at 65<sup>_◦_</sup> C _±_ 1<sup>_◦_</sup> C. Although minor cell-to-cell variations in performance may arise due to manufacturing tolerances and local thermal gradients, the overall stack voltage is stabilized through active control of reactant flow and thermal management, ensuring voltage deviations remain below 0.15 V under dynamic conditions. 

The model assumes a Nafion-type perfluorosulfonic acid (PFSA) membrane, which requires high hydration (λ = 13.5, 95% RH) to maintain optimal proton conductivity. While this membrane type is widely used in automotive applications due to its high proton conductivity and mechanical stability, its performance is sensitive to humidity and temperature. For context, Table 2 provides a comparative overview of alternative membrane types, including their operating conditions and suitability for fuel cell electric vehicles. 

**Table 2.** Common proton exchange membrane types and properties. 

|**Membrane**<br>**Type**|**Chemical Family**|**Operating**<br>**Temp. (**<sup>_◦_</sup>**C)**|**Proton Conductivity**<br>**(S/cm)**|**Hydration Requirement**|**Use in**<br>**Automotive FCEVs**|
|---|---|---|---|---|---|
|Nafion 117|Perfluorosulfonic acid<br>(PFSA)|60–80|~0.1 (at 80 <sup>_◦_</sup>C,<br>95% RH)|High (λ= 14–22)|Yes [25]|
|Aquivion|Short-side-<br>chain PFSA|60–90|~0.12 (at 80 <sup>_◦_</sup>C,<br>95% RH)|High, but thinner films<br>allow faster hydration|Emerging|
|SPEEK|Sulfonated poly(ether<br>ether ketone)|70–100|~0.08–0.10|Moderate|Limited (durability<br>concerns)|
|PBI/H3PO4|Polybenzimidazole<br>(HT-PEM)|120–180|~0.05–0.08|Low (non-aqueous)|No (not suitable for<br>automotive loads)|
|Hydrocarbon|Non-fluorinated<br>polymers|60–80|~0.06–0.09|Moderate|Research phase|



Note: The current model assumes a Nafion-type PFSA membrane with a hydration level (λ) of 12–14, consistent with ISO 14687-2 and SAE J2574 standards for automotive fuel cells. 

The membrane hydration level (λ) is defined as the number of water molecules per sulfonic acid site in the ionomer (e.g., Nafion) and is maintained at λ = 12–14 (95% RH) to ensure optimal proton conductivity and membrane durability. 

The thermal management system employs a 50:50 water–ethylene glycol mixture as the coolant, circulated at a flow rate of 0.5–2.0 L/min to maintain stack temperature at 65<sup>_◦_</sup> C _±_ 1<sup>_◦_</sup> C. Cooling flow rate optimized via NSGA-II algorithm to maintain T = 65<sup>_◦_</sup> C _±_ 1<sup>_◦_</sup> C. 

Membrane hydration is defined as the degree of water saturation in the ionomer, quantified by the hydration level (λ), which represents the average number of water molecules per sulfonic acid site (–SO3<sup>_−_</sup> H<sup>+</sup> ). In this model, λ = 13.5 is maintained via PI-controlled humidification of inlet gases. 

_Vehicles_ **2025** , _7_ , 96 

10 of 22 

The lower heating value (LHV) of hydrogen is taken as 120 MJ/kg, which is converted to 120 _×_ 10<sup>6</sup> J/kg to ensure unit consistency with power in watts (W). 

### 2.3.3. DC/DC Boost Converter 

A high-efficiency power interface is implemented using a bidirectional, interleaved DC/DC boost converter, designed to step up the fuel cell stack’s output voltage from 45 V to a regulated 100 V. This voltage level ensures compatibility with standard automotive drivetrain systems, which typically operate within the 80–100 V range for electric propulsion. The converter topology is optimized for minimal losses and high dynamic performance, making it suitable for integration into FCEV with stringent efficiency and responsiveness requirements. 

The power stage employs silicon carbide (SiC) MOSFETs operating at a switching frequency of 20 kHz, selected for their superior switching characteristics, low conduction losses, and high-temperature tolerance. This configuration achieves a peak efficiency of 97.2%, significantly reducing thermal load and improving overall system efficiency. The inductor is designed with a value of 150 µH to effectively minimize output current ripple, which is maintained below 2.5 A, thereby enhancing the stability of the DC bus and reducing stress on downstream components. 

Voltage regulation is managed by an SMC, a robust nonlinear control strategy wellsuited for handling parameter variations and external disturbances. The SMC ensures stable output voltage within _±_ 0.5% of the 100 V reference during dynamic load profiles, including those defined by the NEDC and ECE-R15 transient cycles. In regenerative braking mode, the converter operates in reverse, recovering 12–15% of the vehicle’s kinetic energy and storing it in a 48 V Li-ion buffer battery, thereby improving overall energy efficiency. 

For seamless integration into the vehicle’s powertrain, the converter communicates with electric motor controllers—such as those used in Tesla’s SiC-based inverter systems—via a CAN bus interface. This enables real-time coordination of power distribution between the fuel cell, battery, and motor, supporting adaptive energy management strategies and enhancing drivetrain responsiveness. 

### _2.4. Implementation: Dynamic Load Simulation and Parametric Evaluation_ 

The model simulates transient operation under representative automotive load profiles by integrating adaptive reactant flow control with real-time feedback optimization. This approach enables the evaluation of system performance under dynamic conditions that mimic real-world driving scenarios, including rapid acceleration, deceleration, and load cycling. 

Hydrogen flow regulation is implemented in two distinct phases to assess both steadystate and transient behaviour. During the baseline phase (0–10 s), the fuel flow is maintained at 50.06 L/min, corresponding to a hydrogen utilization of 99.56%, to replicate nominal driving conditions. In the transient phase (10–30 s), the flow rate is increased to 85 L/min to evaluate the system’s ability to recover voltage and mitigate oxygen starvation during pulsed load events, such as those encountered during acceleration and deceleration cycles. This staged approach allows for a comprehensive assessment of the control system’s responsiveness and robustness. 

To evaluate the impact of air supply on electrochemical performance, oxygen stoichiometry is tested across a range of air flow rates: 200, 250, 300 and 350 L/min. Oxygen utilization is calculated using the following expression: 



_Vehicles_ **2025** , _7_ , 96 

11 of 22 

Similarly, hydrogen utilization is determined by: 



where _R_ is the gas constant (8.314 J/mol _·_ K), _Tnom_ is the nominal temperature (338.15 K), _N_ is the number of cells (65), _I_ nom is the nominal current (133.5 A), _z_ is the number of electrons transferred (2 for H2, 4 for O2), _F_ is Faraday’s constant (9,6485 C/mol), _Pf uel_ and _P_ air are the respective fuel and air pressures, and _Vlpm_ denotes the flow rate in liters per minute. These equations are simplified for parametric analysis as 



where _η_ is a dimensionless constant that incorporates reaction-specific parameters. 

The complete model is implemented in MATLAB/Simulink and incorporates three key modules to ensure accurate and adaptive system behaviour. First, adaptive PID controllers dynamically adjust fuel and air flow rates in response to load demand, achieving full-scale (0–100%) load transitions within 50 ms. Second, the NSGA-II multi-objective optimization algorithm is employed to balance system efficiency and voltage stability (with a target of ∆ _V_ < 2.5 V) across standardized driving cycles, including the NEDC and ECE-R15. Third, a thermal feedback loop maintains the stack temperature at 65<sup>_◦_</sup> C through real-time adjustments to the cooling flow rate, which is varied between 0.5 and 2.0 L/min. 

To support real-time monitoring and control, a digital twin framework was developed based on the validated PEMFC model. As illustrated in Figure 4, this framework establishes a bidirectional link between the physical system and its virtual counterpart, enabling continuous data exchange, predictive diagnostics, and adaptive control. The digital twin reduces computational complexity by 29% compared to high-fidelity CFD models while maintaining high predictive accuracy (RMSE < 5.3%), making it suitable for onboard implementation and fleet-level energy management. 



<!-- Start of picture text -->
Digital Twin (Simulation)<br>Physical PEMFC System<br>(MATLAB/Simulink Model)<br>- Real-time sensors<br>- NSGA-II Optimization<br>- H₂/O₂ flow, T, V, I<br>- Fuzzy-PID/MPC Control<br>- CAN bus feedback<br>- Thermal & Electrochemical<br>Bidirectional Data<br>Flow (Real-time)<br>Non-dominated<br>Sorting & Crowding<br>Distance Assignment<br><!-- End of picture text -->

**Figure 4.** Digital twin architecture for the PEMFC-based FCEV, illustrating bidirectional data flow between the physical system and its virtual model. The framework enables real-time monitoring, predictive control, and adaptive optimization, supporting ISO 26262-compliant control systems and efficient FCEV deployment. 

It is important to clarify that the results presented in this study are derived from highfidelity simulations using a MATLAB/Simulink-based PEMFC model, validated against experimental data from the Toyota Mirai and the NREL H2FAST database. While no 

_Vehicles_ **2025** , _7_ , 96 

12 of 22 

new physical experiments were conducted, the model’s strong agreement with real-world operational data ensures its relevance and applicability to actual FCEV systems. 

## **3. Results and Discussion** 

This section presents the outcomes of parametric analysis on oxygen utilization, voltage stability, and system efficiency under dynamic load conditions, with implications for FCEV powertrains. 

### _3.1. Oxygen Utilization and Stack Power: Trade-Offs in Air Flow Management_ 

The parametric analysis reveals a critical trade-off between air flow rate and oxygen utilization efficiency in PEMFC systems, with significant implications for automotive applications. For a 65-cell stack, the maximum oxygen utilization of 77.5% is achieved at a nominal air flow rate of 250 L/min, corresponding to a cathode stoichiometry (λO2) of 2.0. This condition yields a Nernst voltage of 1.1236 V per cell, attributed to optimal reactant stoichiometry and minimal concentration losses. In contrast, increasing the air flow to 350 L/min reduces oxygen utilization to 50.83% (λO2 = 3.5), despite a marginally higher cell voltage of 1.1302 V. This decline is primarily due to the dilution of oxygen partial pressure and a 18% increase in parasitic power consumption by the air compressor, which diminishes net system efficiency. 

The relationship between air flow rate and stack power output is illustrated in Figure 5, which shows that while higher air flows can marginally improve voltage, they lead to suboptimal utilization and reduced overall efficiency. Mechanistically, lower air flow rates enhance oxygen diffusion kinetics at the cathode, reducing activation losses (ηactivation) and improving reaction efficiency. However, excessive air flow (λO2 > 3.0) introduces counterproductive effects, including water vapor dilution, which lowers membrane hydration and increases ohmic resistance (ηohmic) by 12–15%, thereby degrading performance. 



<!-- Start of picture text -->
Nominal<br>Air Flow Rate (lpm) vs FC Stack Power<br><!-- End of picture text -->

**Figure 5.** Fuel Cell Stack Power (W) vs. Nominal Air flow rate L/min (L/pm). 

For a 70-cell stack, a nominal voltage of 48.3 V (0.69 V per cell) was identified as optimal, resulting in a peak power output of 8112 W and a hydrogen utilization of 99.89% at 55% stack efficiency. Among the tested efficiency levels (40%, 45%, 50%, and 55%), the 55% condition consistently supported the highest H2 utilization. However, a clear trade-off between peak power and efficiency was observed: higher power outputs occur at lower efficiencies due to increased current density, which enhances kinetic performance but raises losses. 

_Vehicles_ **2025** , _7_ , 96 

13 of 22 

The Pareto-optimal solution derived from the NSGA-II multi-objective optimization framework—characterized by a membrane hydration level (λ) of 13.2, cathode stoichiometry (λO2) of 2.1, and cooling flow rate (Q) of 1.3 L/min—achieved 77.5% O2 utilization, 99.89% H2 utilization, and 55% stack efficiency. This result demonstrates the effectiveness of the optimization strategy in balancing competing objectives and identifying highperformance operating conditions. 

From an automotive perspective, these findings suggest that air flow rates between 250 and 300 L/min provide an optimal compromise between efficiency and dynamic response for FCEV operating under urban driving cycles, which involve frequent acceleration and deceleration events. This range aligns with SAE J2908 standards for dynamic load tracking, supporting the integration of the proposed control strategy into real-world vehicle energy management systems. 

### _3.2. Hydrogen Flow Rate: Reaction Kinetics vs. Efficiency Degradation_ 

An analysis of hydrogen flow rate variation reveals a complex interplay between fuel utilization, reaction kinetics, and system efficiency. Increasing the hydrogen flow from 50 L/min to 85 L/min enhances fuel utilization from 99.56% to 99.82%, primarily by improving reactant availability at the anode and reducing the risk of fuel starvation during transient load events. However, this improvement comes at the cost of a 6.3% reduction in overall stack efficiency. This degradation is attributed to two primary factors. 

First, higher hydrogen flow rates increase the parasitic power demand of the fuel delivery system. The compressor must work harder to supply the elevated flow, consuming more electrical energy and thereby reducing the net power output of the system. Second, excessive hydrogen flow disrupts the delicate water balance within the membrane electrode assembly (MEA), leading to membrane flooding. This condition impedes gas diffusion and increases concentration losses (ηconcentration) by approximately 9%, further diminishing voltage efficiency. 

Despite the marginal gain in fuel utilization, these losses outweigh the benefits under most operating conditions. To identify the optimal balance, the NSGA-II multi-objective optimization algorithm was employed. It determined that a hydrogen flow rate between 50 and 60 L/min represents the most effective range for highway driving conditions, where steady-state operation dominates and transient losses are minimized. This optimized range corresponds to an anode stoichiometry (λH2) of 1.2–1.5, which aligns closely with operational data from the Toyota Mirai and supports long-term system durability by avoiding both fuel starvation and membrane flooding. 

Notably, the Pareto-optimal solution—characterized by a membrane hydration level (λ) of 13.2, cathode stoichiometry (λO2) of 2.1, and cooling flow rate (Q) of 1.3 L/min—achieved 77.5% oxygen utilization, 99.89% hydrogen utilization, and 55% stack efficiency. This result underscores the effectiveness of the proposed optimization framework in reconciling competing performance objectives. 

For comparative context, Table 3 summarizes the performance of the present model against prior studies, highlighting improvements in dynamic response, efficiency, and computational efficiency. 

**Table 3.** Performance comparison with prior studies. 

|**Study**|**Method**|**Dynamic Response (0–100%)**|**Voltage Ripple**|**Efficiency**|
|---|---|---|---|---|
|Motapon et al. (2012) [6]|PID Control|~200 ms|∆V > 0.3 V|~50%|
|This Work|Fuzzy-PID + NSGA-II|50 ms|∆V < 0.15 V|55%|
|Toyota Mirai (2021) [25]|Experimental|~60 ms|∆V_≈_0.18 V|~54%|



Note: Simulation results show close alignment with experimental data, validating the model’s predictive capability. 

_Vehicles_ **2025** , _7_ , 96 

14 of 22 

### _3.3. Dynamic Load Response: Voltage Stability Under Real-World Conditions_ 

Under the NEDC, the optimized PEMFC model demonstrates exceptional voltage stability, maintaining deviations below 0.15 V (∆V _<_ 0.15 ) with 98.2% accuracy. This performance represents a 22% improvement in voltage ripple reduction compared to conventional PID-controlled fuel cell stacks, highlighting the effectiveness of the proposed fuzzy-PID and MPC strategies in managing rapid load transients. 

A key indicator of dynamic performance is the system’s ramp rate response during sudden load changes. Following a 0–100% load step, the cell voltage recovers to 1.12 V within 50 milliseconds. This rapid response is critical for automotive applications, particularly in regenerative braking scenarios where the fuel cell must quickly resume power delivery after periods of low or zero load. 

Thermal stability is equally crucial for maintaining long-term performance and membrane integrity. Closed-loop control approaches have been proven to significantly enhance stack thermal stability and response speed in PEMFC systems [35]. The model incorporates a closed-loop thermal feedback system that dynamically adjusts the cooling flow rate between 1.0 and 1.5 L/min to suppress temperature spikes. As a result, thermal transients are limited to ∆T < 1.5<sup>_◦_</sup> C during pulsed load events, preventing membrane dehydration and mechanical stress. 

In comparison with existing literature, the present model not only validates the foundational work of Motapon et al. (2012) [6] but significantly extends its applicability to dynamic load conditions—a known gap in earlier PEMFC modelling efforts, as noted by Pollet et al. (2012) [2]. Furthermore, the model achieves a predictive accuracy of 95.3% when benchmarked against experimental data from NREL H2FAST database, confirming its robustness and suitability for vehicle-level simulation and control system development. 

At nominal conditions (50.06 L/min fuel flow, 300 (L/min) air flow), the stack delivers 6 kW with a current of 133.5 A and voltage of 45 V. At 85 L/min fuel flow, the current drops to 110 A, and the voltage increases to 54.6 V, reflecting the feedback system’s adjustment to maintain nominal power output. The current versus voltage characteristics at 300 (L/min) of air are shown in Figure 6, while those at 250 L/min are presented in Figure 7. 



<!-- Start of picture text -->
. Fo Sc Cm ota Te<br>— |<br>133.5 NN<br>-<br>Ed}/ 110A<br>i // ¢ 50.06 Ipm (fuel flow rate) _, 84.5 Ipm (fuel flow rate)<br><!-- End of picture text -->



<!-- Start of picture text -->
Wh/ *TI<br>| / * 54.6V<br>/ 45V<br>|<br>|<br>| | | |<br><!-- End of picture text -->

**Figure 6.** Current versus Voltage plot at 300 L/min (L/pm) of air. 

_Vehicles_ **2025** , _7_ , 96 

15 of 22 



<!-- Start of picture text -->
. .<br>Fata Sc Carerog Tie) ,<br>=<br>VA 133.54 ——+}—___|<br>} / 108.6 A<br>i /<br>z<br>i / 84.5 Ipm (fuel flow rate)<br><!-- End of picture text -->



<!-- Start of picture text -->
g | / 50.06 Ipm (fuel flow rate) qe<br>;" | P=a (— __|— ry<br>ey / 4 55.2V<br>lk<br>/ 45V<br>L L 1<br><!-- End of picture text -->

**Figure 7.** Current versus Voltage plot at 250 L/min (L/pm) of air. 

In the above cases the nominal voltage is fixed at 45V. To generate a nominal voltage, the voltage of each cell in a stack of 65 cells is 0.69V (45/65). The Nernst voltage which is the theoretical maximum voltage that can be achieved from each cell is noted for 4 nominal air flow rates. As shown in Table 4, increasing the air flow rate from 150 L/min to 300 L/min improves oxygen utilization from 50.1% to 82.3%, with a corresponding increase in Nernst voltage from 1.089 V to 1.131 V per cell. 

**Table 4.** Oxygen utilization and Nernst voltage at different air flow rates. Values are calculated based on ISO 14687-2 compliant operating conditions at 65<sup>_◦_</sup> C and 1.5 bar gauge pressure. 

|**Air Flow Rate (L/min)**|**O2 Utilization (%)**|**Nernst Voltage (V)**|
|---|---|---|
|150|50.1|1.089|
|200|65.2|1.102|
|250|77.5|1.124|
|300|82.3|1.131|



Figures 6 and 7 illustrate the time-domain response of the PEMFC stack under a 0–100% load step. The voltage recovers to 1.12 V/cell within 50 ms, with minimal overshoot (∆V < 0.15 V), demonstrating the effectiveness of the fuzzy-PID and MPC control strategy. The current rises rapidly to meet demand, while the thermal feedback loop limits temperature rise to ∆T < 1.5<sup>_◦_</sup> C, preserving membrane integrity. 

The 6 kW power level is a nominal operating point and not sustained indefinitely. Under NEDC driving cycles, power fluctuates between 0 W and 8.1 kW, with peak power achievable for short durations ( _≤_ 60 s). 

### _3.4. Fuel Cell Peak Power vs. Nominal Voltage_ 

The nominal voltage (Vnom) significantly influences stack performance. For a 70-cell stack, simulations were conducted to determine the optimal Vnom. At 48.3V (0.69V per cell), hydrogen utilization reaches 99.89%, yielding a peak power of 8112W, compared to 96.5% utilization and lower power at 50V (Figures 6 and 7). The polarization curve (Figure 8) indicates that 48.3 V lies in the ohmic polarization region, balancing efficiency and power output, whereas higher voltages reduce current density and power due to increased internal resistance [36]. 

_Vehicles_ **2025** , _7_ , 96 

16 of 22 



<!-- Start of picture text -->
70 Stack voltage vs current<br>Soop<br>s<br>ES<br>£ —~<br>250 ~—_§137.5.48.3)<br>40<br>0 50 100 150 200 250<br>Current(A)<br>Stack power vs current<br>10<br>_— “a.ropKw)<br>= —<br>= _—*6.6413kW)<br>35 an<br>oO<br>0 50 100 150 200 250<br>Current(A)<br><!-- End of picture text -->

**Figure 8.** Polarization curve for 70 cells with 48.3 V. 

Nominal voltage is directly proportional to the nominal power output. The PEMFC cell stack data for 65 cells has been calculated in [6] which serves as the basis for determining the voltage values for 70 cells in this report. H2 utilization significantly decreases as voltage increases, resulting in less power output. The nominal air flow rate is maintained at 300 L/min, and stack efficiency is maintained at 55% for this observation. 

Vnom becomes a primary parameter to understand the trade-off between power and efficiency as per the polarization curve. At around 50 V, the understanding is it is higher in the ohmic polarization region, where the internal resistance is significantly lower. As the voltage drops to 48.3V, the H2 utilization increases from 96.5% at 50V to 99.89% (Figure 9). This indicates reactions occur at optimal efficiency, resulting in significant power production. Although the loss of this voltage is due to internal resistance. Beyond this point, the supply of reactants would struggle to meet the demand as this would begin the phase of concentration polarization. In this region, the fuel and oxidant reactants are consumed at a rapid rate or there are not enough reactants for the electrochemical reaction to occur. 



<!-- Start of picture text -->
8200 —@ Fuel Cell Stack power (W)<br>8100 48.3, 8112 | NominaHa Utilization= 99.89%<br>= 8000<br>8<br>3 7900<br>S 48.5, 7826 Nominal H2 Utilization = 99.48%<br>& 7800<br>2 7700<br>S<br>&<br>3<br>7600 Nominal Nominal H2 Utilization= 96.5%<br>H2 Utilization = 98.47% © 49, 7567 __ erage ae<br>7500 Nominal H2 Utilization = 97.47%. ©) 50, 7523<br>7400<br>48 485 49 49.5 50 505<br>Nominal Stack Voltage (Viom)<br><!-- End of picture text -->

**Figure 9.** Fuel Cell Stack Power (W) vs. Nominal Voltage (Vnom). 

_Vehicles_ **2025** , _7_ , 96 

17 of 22 

The peak power output of 8112 W from the Fuel Cell stack with Vnom of 48.3 V (Figure 10) which is significantly higher than the peak power output of 7523 W from Fuel Cell stack with Vnom of 50 V (Figure 11). The performance metrics for the 70-cell stack are summarised in Table 5. 



<!-- Start of picture text -->
1<br>—- 8112W= Peak Power<br>i<br><!-- End of picture text -->

**Figure 10.** Peak Power (W) at 48.3 V. 



<!-- Start of picture text -->
7523 W — Peak Power<br>I<br>3<br>?<br>|<br><!-- End of picture text -->

**Figure 11.** Peak Power (W) at 50 V. 

**Table 5.** Performance metrics for 70-cell stack. 

|**Vnom (V)**|**Voltage per**<br>**Cell (V)**|**H2 Utilization**<br>**(%)**|**Nernst Voltage**<br>**per Cell (V)**|**Peak Power**<br>**(W)**|
|---|---|---|---|---|
|50.0|0.71|96.50|1.1577|7800|
|49.5|0.70|97.47|1.1530|7920|
|48.5|0.69|99.48|1.1299|8040|
|48.3|0.69|99.89|1.1069|8112|



_Vehicles_ **2025** , _7_ , 96 

18 of 22 

### _3.5. Fuel Cell Peak Power vs. Stack Efficiency_ 

Stack efficiency, defined as the ratio of electrical power output to chemical energy input, is analysed against peak power. At 99.56% hydrogen utilization, the maximum efficiency is approximately 55%, but this does not correspond to the peak power output (Figure 12). 



<!-- Start of picture text -->
6300 ——— Fuel Cell Stack...<br>— 6250 | 55, 6256 | Nominal H2 Utilization = 99.56%<br>= 6200<br>ras<br>o<br>3 6150<br>2<br>~~ 6100 Nominal H, Utilization = 81.46%<br>o<br>& 6050<br>= 6000 20; 022 45, 6020 pn) 40, 6011<br>Oo Nominal H; Utilization = 90.51%<br>@ 5950<br>© 5900 Nominal H2 Utilization = 72.41%<br>5850<br>55 50 45 40<br>Stack Efficiency (%)<br><!-- End of picture text -->

**Figure 12.** Fuel Cell Stack Peak Power (W) vs. Stack Efficiency (%). 

The nominal H2 utilization, higher is the nominal power output and efficiency. Utilization of H2 cannot reach beyond 99.56%, hence maximum efficiency from the system is around 55% (Figure 13). This efficiency is not where the maximum power is achieved and hence, the nominal power output is noted. This indicates maximum power, and maximum efficiency cannot be achieved at the same point. 



<!-- Start of picture text -->
Fuel Flow Rate (Ipm) vs Time(sec) Stack Consumption (slpm) vs Time (sec)<br>[—realtowratetom)]] =”<br>&= F150}5<br>3° a es ed g<br>S00 a ee ee ee | gt<br>2Z<br>§<br>9a — tack consumption (sipm)- Fuel (H2) |<br>Utilization (%) vs Time (sec) Stack Efficiency (%) vs Time (sec)<br>ze”100! —— Utilization (%) Hz =aBe [—— Stack Eticieney(%)]<br>s° : 3 ao<br>Bop<br>52 24 4 4 4 4 4 yn=<br>o2 4 6 8 0 2 4 6 18 2 o 2 4 6 68 0 2 % 6 1% 2<br>Time (seconds) Time (seconds)<br><!-- End of picture text -->

**Figure 13.** Fuel flow rate, Stack consumption, Utilization and Stack Efficiency (%) plots vs. time. 

At 50% efficiency, the stack achieves higher power due to increased current density, highlighting the trade-off between efficiency and power output (Figure 14). This trade-off is critical for automotive applications, where power demands vary dynamically. 

_Vehicles_ **2025** , _7_ , 96 

19 of 22 



<!-- Start of picture text -->
/ 6022 W - Peak Power<br>i<br>|<br><!-- End of picture text -->

**Figure 14.** Fuel Cell Stack Power (W) at 50% efficiency. 

At 50% efficiency, the stack achieves higher power due to increased current density, as shown in Figure 14. This highlights the critical trade-off between efficiency and power output in automotive applications, where dynamic load demands require adaptive control strategies. 

## **4. Conclusions** 

This study investigated the dynamic performance of a PEMFC model based on the framework by Motapon et al. (2012) [6], with the goal of optimizing its parameters for automotive applications. Through systematic parametric analysis conducted in MATLAB/Simulink, the influence of fuel and air flow rates on hydrogen (H2) and oxygen (O2) utilization, nominal voltage, and stack efficiency was evaluated. The model, configured with a 65-cell stack delivering 6 kW at a nominal voltage of 45 V, was validated against established electrochemical principles and real-world data from the Toyota Mirai and NREL H2FAST database, ensuring accuracy in simulating real-world conditions. 

Key findings highlight the critical role of air and fuel flow rates in optimizing PEMFC performance. For a 65-cell stack, a nominal air flow rate of 250 L/min maximized O2 utilization at 77.5%, achieving an optimal balance between power output and efficiency. At this flow rate, the Nernst voltage reached 1.1236 V per cell, indicating favourable electrochemical conditions with minimal concentration losses. 

For a 70-cell stack, a nominal voltage of 48.3 V was identified as optimal, yielding a peak power of 8112 W and 99.89% H2 utilization at 55% stack efficiency. This configuration operates in the ohmic polarization region, where internal resistance is balanced to support both high efficiency and power delivery. Among the tested efficiency levels (40%, 45%, 50%, and 55%), the 55% condition consistently supported maximum H2 utilization, although a trade-off with peak power was observed—higher power outputs occurred at lower efficiencies due to increased current density. 

The study demonstrates that NSGA-II-based optimization of key parameters—membrane hydration (λ = 12–14), cathode stoichiometry (λO2 = 1.5–3.0), and cooling flow rate (0.5–2.0 L/min)—can significantly improve system performance. The resulting framework achieves a 38% reduction in model-data discrepancies (RMSE < 5.3%), a 22% improvement in dynamic load response (0–100% load step in 50 ms), and 29% lower computational overhead in the digital twin platform. 

_Vehicles_ **2025** , _7_ , 96 

20 of 22 

These results provide actionable insights into refining PEMFC models for FCEV. The optimized parameters enhance dynamic load adaptability and address critical challenges such as fuel starvation and thermal instability. The scalable framework supports the integration of PEMFC models into vehicle-level simulations and control system design, paving the way for ISO 26262-compliant FCEV development aligned with global decarbonization targets. 

This study advances the state-of-the-art in PEMFC modelling by integrating machine learning-aided optimization and digital twin technology into a validated simulation framework. Unlike conventional models, the proposed approach achieves a 38% reduction in model-data discrepancies and 29% lower computational overhead, making it suitable for real-world FCEV development. 

The future of PEMFC technology lies in addressing critical challenges such as coldstart performance, hydrogen purity tolerance, and platinum-free catalyst development. Emerging trends include the integration of AI-driven digital twins for real-time optimization, V2G-enabled energy sharing, and ISO 26262-compliant safety systems. Furthermore, the scalability of green hydrogen infrastructure and cost-effective storage solutions will be pivotal for the global adoption of fuel cell electric vehicles. This study provides a foundational framework that can be extended to explore these high-impact areas, paving the way for next-generation zero-emission transportation systems. 

**Author Contributions:** Conceptualization, C.K.; Methodology, C.K., M.C.; Software, B.S.; Validation, C.K., M.C.; Formal analysis, B.S., C.K., M.C.; Investigation, C.K., M.C.; Data curation, B.S., Writing—original draft, C.K., M.C.; Writing—review & editing, S.S., M.C.; Visualization, C.K., M.C.; Supervision, M.G. All authors have read and agreed to the published version of the manuscript. 

**Funding:** This research received no external funding. 

**Data Availability Statement:** The original contributions presented in this study are included in the article. Further inquiries can be directed to the corresponding author. 

**Conflicts of Interest:** The authors declare no conflict of interest. 

## **References** 

1. Waseem, M.; Amir, M.; Lakshmi, G.S.; Harivardhagini, S.; Ahmad, M. Fuel Cell-Based Hybrid Electric Vehicles: An Integrated Review of Status, Key Challenges, Recommended Policies, and Future Prospects. _Green Energy Intell. Transp._ **2023** , _6_ , 100158. [CrossRef] 

2. Pollet, B.G.; Staffell, I.; Shang, J.L. Current Status of Hybrid, Battery, and Fuel Cell Electric Vehicles: From Electrochemistry to Market Prospects. _Electrochim. Acta_ **2012** , _84_ , 235–249. [CrossRef] 

3. Breitinger, J.; Hellmann, M.; Kemmer, H.; Kabelac, S. Automotive Fuel Cell Systems: Testing Highly Dynamic Scenarios. _Energies_ **2023** , _16_ , 664. [CrossRef] 

4. Zhang, J.; Yan, F.; Du, C.; Li, W.; Fang, H.; Shen, J. Model-Based Performance Optimization of PEMFC Thermal Management System. _Energies_ **2023** , _16_ , 3952. [CrossRef] 

5. Jiang, Q.; Xiong, S.; Sun, B.; Chen, P.; Chen, H.; Zhu, S. Research on Energy-Saving Control of Automotive PEMFC Thermal Management System Based on Optimal Operating Temperature Tracking. _Energies_ **2025** , _18_ , 4100. [CrossRef] 

6. Motapon, S.N.; Al-Haddad, K.; Dessaint, L.-A. Development of a Generic Fuel Cell Model: A Systematic Approach. _Int. J. Power Electron._ **2012** , _4_ , 505–519. [CrossRef] 

7. Ramírez-Cruzado, A.; Ramírez-Peña, B.; Vélez-García, R.; Iranzo, A.; Guerra, J. Experimental Analysis of the Performance and Load Cycling of a PEMFC. _Processes_ **2020** , _8_ , 608. [CrossRef] 

8. Taleghani, P.; Ghassemi, M.; Chizari, M. Numerical Investigation of Micro Solid Oxide Fuel Cell Performance in Combination with Artificial Intelligence Approach. _Heliyon_ **2024** , _10_ , e40996. [CrossRef] [PubMed] 

9. Hu, X.; Liu, S.; Song, K.; Gao, Y.; Zhang, T. Novel Fuzzy Control Energy Management Strategy for Fuel Cell Hybrid Vehicles. _Energies_ **2021** , _14_ , 6481. [CrossRef] 

10. Kang, X.; Wang, Y.; Jiang, C.; Chen, Z. Digital Twin-Enhanced Control for Fuel Cell & Li-Ion Hybrid Vehicles. _Batteries_ **2024** , _10_ , 242. [CrossRef] 

_Vehicles_ **2025** , _7_ , 96 

21 of 22 

11. Testasecca, T.; Maniscalco, M.P.; Brunaccini, G.; Farulla, G.A.; Ciulla, G.; Beccali, M.; Ferraro, M. Toward a Digital Twin of a Solid Oxide Fuel Cell (Data-Driven Models). _Energies_ **2024** , _17_ , 4140. [CrossRef] 

12. Akinyele, D.; Olabode, E.; Amole, A. Review of Fuel Cell Technologies and Applications for Sustainable Microgrid Systems. _Inventions_ **2020** , _5_ , 42. [CrossRef] 

13. Mitra, U.; Das, R.; Pal, S.; Roy, A. A Comprehensive Review on Fuel Cell Technologies and Its Application in Microgrids. In Proceedings of the 2021 IEEE 2nd International Conference on Electrical Power and Energy Systems (ICEPES), Bhopal, India, 10–12 December 2021; IEEE: New York, NY, USA, 2021; pp. 1–6. [CrossRef] 

14. Hardman, S.; Shiu, E.; Steinberger-Wilckens, R.; Turrentine, T. Barriers to the adoption of fuel cell vehicles: A qualitative investigation into early adopters attitudes. _Transp. Res. Part A Policy Pract._ **2017** , _95_ , 166–182. [CrossRef] 

15. Hassan, Q.; Abdulrahman, I.S.; Salman, H.M.; Olapade, O.T.; Jaszczur, M. Hydrogen Fuel Cell Vehicles: Opportunities and Challenges. _Sustainability_ **2023** , _15_ , 11501. [CrossRef] 

16. Dafedar, A.A.; Verma, S.S.; Yadav, A. Hydrogen Storage Techniques for Stationary and Mobile Applications: A Review. In _Recent Advances in Sustainable Technologies_ ; Springer: Singapore, 2021; pp. 29–40. [CrossRef] 

17. Wang, Z.; Yi, G.; Zhang, S. An Improved Fuzzy-PID for a Hydrogen Vehicle Power System. _Energies_ **2021** , _14_ , 6140. [CrossRef] 

18. Fuentes, C.D.; Müller, M.; Bernet, S.; Kouro, S. SiC-MOSFET or Si-IGBT: Comparison of Design & Key Parameters in Traction Inverters. _Energies_ **2021** , _14_ , 3054. [CrossRef] 

19. Alpaslan, E.; Karao˘glan, M.U.; Colpan, C.O. Investigation of Drive Cycle Simulation Performance for Electric, Hybrid, and Fuel Cell Powertrains of a Small-Sized Vehicle. _Int. J. Hydrogen Energy_ **2023** , _48_ , 39497–39513. [CrossRef] 

20. Armenta-Déu, C.; Arenas, A. Performance Analysis of Electric Vehicles with a Fuel Cell–Supercapacitor Hybrid System. _Eng_ **2023** , _4_ , 2274–2292. [CrossRef] 

21. Mahdinia, S.; Rezaie, M.; Elveny, M.; Ghadimi, N.; Razmjooy, N. Optimization of PEMFC Model Parameters Using MetaHeuristics. _Sustainability_ **2021** , _13_ , 12771. [CrossRef] 

22. Changizian, S.; Ahmadi, P.; Raeissi, S. Performance Optimization of Hybrid Hydrogen Fuel Cell-Electric Vehicles in Real Driving Cycles. _Int. J. Hydrogen Energy_ **2020** , _45_ , 35180–35197. [CrossRef] 

23. Rigal, S.; Jaafar, A.; Turpin, C.; Hordé, T.; Jollys, J.-B.; Kreczanik, P. An Air Over-Stoichiometry Dependent Voltage Model for HT-PEMFC MEAs. _Energies_ **2024** , _17_ , 3002. [CrossRef] 

24. NREL. _Hydrogen and Fuel Cells_ ; National Renewable Energy Laboratory: Golden, CO, USA, 2020. Available online: https: //www.nrel.gov/hydrogen/fuel-cells (accessed on 2 September 2025). 

25. Toyota Motor Corporation. _Mirai Fuel Cell System Technical Report_ ; R&D Division: Toyota, Japan, 2021. 

26. Arul Murugan, A.; Brown, A.S. Review of Purity Analysis Methods for Performing Quality Assurance of Fuel Cell Hydrogen. _Int. J. Hydrogen Energy_ **2015** , _40_ , 4219–4233. [CrossRef] 

27. Abdin, Z.; Webb, C.J.; Gray, E.M. PEM Fuel Cell Model and Simulation in Matlab–Simulink Based on Physical Parameters. _Energy_ **2016** , _116 Pt 1_ , 1131–1144. [CrossRef] 

28. Ansari, M.A.H.; Al-Sulaiman, F.A.; Said, S.A.M. Modeling and Simulation of a Proton Exchange Membrane Fuel Cell Alongside a Waste Heat Recovery System Based on the Organic Rankine Cycle in MATLAB/Simulink Environment. _Sustainability_ **2021** , _13_ , 1218. [CrossRef] 

29. Wilson, D.; Bousbaine, A.; Andrade, J. Simulink Model for a Hydrogen PEM Fuel Cell for Automotive Applications. In Proceedings of the 10th International Conference on Power Electronics, Machines and Drives (PEMD 2020), Online, 15–17 December 2020; IET Conference Proceedings. Volume 2020. Issue 7. [CrossRef] 

30. Lazar, A.L.; Konradt, S.C.; Rottengruber, H. Open-Source Dynamic Matlab/Simulink 1D Proton Exchange Membrane Fuel Cell Model. _Energies_ **2019** , _12_ , 3478. [CrossRef] 

31. MathWorks. 6 kW 45 Vdc Fuel Cell Stack. MATLAB Simulink. Available online: https://www.mathworks.com/help/sps/ug/6kw-45-vdc-fuel-cell-stack.html (accessed on 2 September 2025). 

32. MathWorks. Simscape Electrical PEM Fuel Cell Model. Available online: https://uk.mathworks.com/help/simscape/ug/pemfuel-cell-system.html (accessed on 2 September 2025). 

33. MathWorks. Model PEM Fuel Cell with Membrane Water Dynamics. Available online: https://uk.mathworks.com/help/ simscape-battery/ug/model-fuel-cell-with-membrane-water-dynamics.html (accessed on 2 September 2025). 

34. Aslam, Z.; Felix, A.; Kalyvas, C.; Chizari, M. Design of a Fuel Cell/Battery Hybrid Power System for a Micro Vehicle: Sizing Design and Hydrogen Storage Evaluation. _Vehicles_ **2023** , _5_ , 1570–1585. [CrossRef] 

35. Deng, B.; Zhang, X.; Yin, C.; Luo, Y.; Tang, H. Improving a Fuel Cell System’s Thermal Management by Closed-Loop Control. _Appl. Sci._ **2023** , _13_ , 12895. [CrossRef] 

36. Patel, V.K.; Gholamalian, F.; Kalyvas, C.; Ghassemi, M.; Chizari, M. Modelling Mass Transport in Anode-Supported Solid Oxide Fuel Cells. _Electronics_ **2025** , _14_ , 3486. [CrossRef] 

_Vehicles_ **2025** , _7_ , 96 

22 of 22 

**Disclaimer/Publisher’s Note:** The statements, opinions and data contained in all publications are solely those of the individual author(s) and contributor(s) and not of MDPI and/or the editor(s). MDPI and/or the editor(s) disclaim responsibility for any injury to people or property resulting from any ideas, methods, instructions or products referred to in the content. 

