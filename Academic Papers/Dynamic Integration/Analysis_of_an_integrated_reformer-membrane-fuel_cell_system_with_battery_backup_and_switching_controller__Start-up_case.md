**2019 Fifth Indian Control Conference (ICC) IIT Delhi, India, January 9-11, 2019** 

# **Analysis of an integrated reformer-membrane-fuel cell system with battery backup and switching controller : Start-up case** 

Pravin P.S.<sup>1</sup> Sharad Bhartiya<sup>2</sup> Ravindra D. Gudi<sup>3</sup><sup>_∗_</sup> 

**_Abstract_ — Due to several stringent challenges and constraints faced in direct on-board storage of hydrogen in fuel cell vehicles, appreciable efforts are in progress to prevent direct storage of hydrogen. Directly storing hydrocarbons rich in hydrogen and suitably reforming them in-situ using available reforming techniques could be a possible option to overcome this challenge. A detailed overview of the mathematical modeling and analysis of the integrated reformer membrane fuel cell system was already discussed in an earlier paper. It was shown that at start-up of the plant and during frequent fluctuations in the power demand, requirement of an auxiliary power source like battery/super-capacitor is crucial for a delay free response to the power demand. In this study, an equivalent circuit model of a battery backup system is analyzed along with a switching controller that switches between battery and fuel cell based on some energy management policy. The mathematical model of the system is simulated, considering case study of start-up of the integrated system powering a fuel cell vehicle with battery backup, assuming an idealized driving power profile.** 

**_Index Terms_ — Auto thermal reformer, Palladium membrane hydrogen separation,PEM fuel cell, Multiloop control, Battery, Switching controller.** 

## I. INTRODUCTION 

Reducing the amount of pollutants and greenhouse gas emissions during power generation is one of the main challenging tasks faced by automobile manufacturers. Fuel cell has been increasingly accepted as a potential candidate for energy storage and conversion in portable, stationary and automotive power applications. This is due to its ability to convert chemical energy stored in fuel directly into electricity without undergoing any intermediate conversion steps. Fuel cells incorporate the advantages of high fuel efficiency and low emissions which qualifies them for transportation applications. However, stringent requirements are imposed on the transient behavior of the fuel cell power system especially in automotive applications. Transient response is a crucial characteristic feature of any power generation system when used in applications involving uncertain fast load power demand fluctuations. The response of fuel cells to varying load power demand is comparatively sluggish than other power sources due to its complex dynamics. Hydrogen, the most abundant chemical substance in the universe, is the fuel used in majority of the fuel 

1 _,_ 2 _,_ 3Department of Chemical Engineering, Indian Institute of Technology Bombay, Mumbai-400076, India.<sup>1</sup> pravin ~~p~~ s@iitb.ac.in, 2bhartiya@che.iitb.ac.in, 3<sup>_∗_</sup> ravigudi@iitb.ac.in 

cells available in the current market. The contemporary method to deliver hydrogen to fuel cells is by directly storing the fuel in appropriately designed tanks. Tanks that are capable of withstanding high pressures of the order of 350 to 700 bars are required for gaseous hydrogen storage. For on-board storage of hydrogen in fuel cell vehicles, large volume and high pressure composite vessels are needed due to its low volumetric energy density [1].This requirement might not have larger effect on heavy duty vehicles, but can be a challenging issue for light duty compact vehicles. 

Moreover, hydrogen when exposed to air can easily catch fire and can further lead to explosion, thereby emphasizing the high risk of direct hydrogen storage on-board fuel cell vehicles. One option to circumvent the issues associated with direct hydrogen storage is to incorporate an integrated fuel processing system that utilizes hydrogen rich hydrocarbons to generate necessary hydrogen in situ on an “as needed” basis [2] [3]. As there is an already existing infrastructure for natural gas supply, reforming it to produce hydrogen seems to be a viable option in fuel cell powered automobiles. However, the response time of the integrated system is expected to be slow compared to the frequency of power demand fluctuations by the electric motor due to acceleration and unexpected traffic conditions. This can lead to a significant lag between the power requested by the electric motor and the power delivered by the fuel cell. Hence, the need for an auxiliary power source is inevitable in order to ensure satisfactory and delay free performance of the fuel cell vehicle. 

In an earlier paper [4], the basic components of the integrated system namely the fuel processing subsystem, fuel purification subsystem and the power generation subsystem were discussed along with a preliminary design of the control system. An auxiliary power source like battery or super capacitor to improve the system performance was outside the scope and was not discussed in the previous work. In this work, we attempt to explore the overall startup dynamic behavior of an integrated reformer membrane fuel cell system equipped with a battery backup. Battery takes care of the load power demand during the time duration which the fuel cell takes to generate the requisite power. A logic based switching controller that switches between the battery backup and fuel cell is designed for generating a delay free response to the load power demand. 

An auto thermal reformer is preferred as the hydrogen 

**978-1-5386-6246-5/19/$31.00 ©2019 IEEE** 

**225** 

Authorized licensed use limited to: ASTON UNIVERSITY. Downloaded on September 01,2026 at 20:40:00 UTC from IEEE Xplore.  Restrictions apply. 



<!-- Start of picture text -->
Pressure Setpoint Power Set point<br>cH Conialler(Pc) 4 @) cova<br>Air Heat<br>HoCpBwerSA  PRRCOM! preheater BatMixer Autothermal W SYH— Heat  Raga membraneNaykyLinepack ControtXCon exchanger ar<br>PC —Pressure controller Leftover H ¥ 1 [eter<br>PC ~ Power controller o[_coototer >) ((oaay<br>PT ~ Pressure transmitter i A ;<br>PT ~Power transmitter 4 4<br><!-- End of picture text -->

Fig. 1. Block diagram showing the integrated reformer membrane fuel cell system with battery back-up 

fuel synthesis system as it does not require supply or dissipation of heat continuously to or from the system except during start of the reaction. Dense palladium membrane has been considered for _H_ 2 gas purification in the present study. High hydrogen permeability, fast hydrogen absorption and transport kinetics as well as excellent thermal stability of the palladium membrane qualifies it to be used as the gas purification sub system for fuel cell applications [5] [6]. Polymer electrolyte membrane fuel cell (PEMFC), an electrochemical device that produces water, electricity and heat by combining hydrogen and oxygen is favored for automotive applications due to its low operating temperature (around 80<sup>_o_</sup> C) which helps in fast start-up. 

The rest of the paper is organized as follows. An overview of the design analysis of the integrated system is discussed in the next section. The subsequent three sections briefly examine the fuel processing subsystem, fuel purification subsystem and power generation subsystem. An equivalent circuit model of a battery backup system is analyzed along with a switching controller that switches between battery and fuel cell to provide a delay free delivery of power. A case study on the start-up of the integrated system with battery back-up and switching controller is presented followed by results and discussions. Conclusion are presented in the last section. 

## II. SYSTEM DESIGN ANALYSIS 

This section discusses the main components of the integrated system that can be engaged as a single unit to produce hydrogen rich stream for power generation. The major components of the integrated system are (1) fuel processing subsystem (2) fuel purification subsystem and (3) power generation subsystem. The schematic showing a block diagram of the integrated reformer membrane fuel cell system with battery backup and switching controller is shown in Figure 1. During start of the reaction, appropriate amount of methane, air and steam, thoroughly mixed and preheated to reforming temperatures, are fed as input to the auto thermal reformer. As the auto thermal 

reformer requires external heat only during start of the reaction, the pre-heater can be disconnected from the loop once the reaction initiates. As can be seen from Figure 1, two heat exchangers, one at the reformer outlet and other at the fuel cell anode inlet side, are installed to maintain the gas temperatures at appropriate values. Pure hydrogen gas is extracted from the gas mixture exiting the reformer by utilizing the palladium based membrane separation unit. It is to be noted that during start-up of the plant, the line pack is assumed to be already filled with some hydrogen gas in order to maintain a line pack pressure of 1 atm. A non-return valve (NRV) is installed after the membrane separation unit. The pure hydrogen gas separated from the gaseous effluents of reformer by the palladium membrane is then fed to the fuel cell for power generation. The line pack is assumed to have a volume of 0.5 liters which is negligibly small compared to the actual storage tank volumes in conventional fuel cell vehicles where hydrogen gas is stored directly. A line pack is considered in order to make sure that a requisite small amount of hydrogen is always available during fast load transitions and sudden peak demands. Depending on the load requirement, the quantity of hydrogen gas available and the percentage of battery charge, the switching controller switches among battery and fuel cell to feed power to the vehicle and charge the battery. 

A multi loop control strategy is designed wherein two controllers, one at the fuel cell anode inlet side for hydrogen flow and other at the reformer inlet side for methane flow are implemented to achieve effective control of the integrated system. Fluctuations in power demand forces the controller 2 (Proportional controller) to manipulate the hydrogen flow rate using control valve 2 to feed the required amount of hydrogen to the fuel cell to generate power. In response to the control valve 2 opening, the hydrogen pressure in the line pack gets disturbed. By sensing the pressure variation in the line pack, controller 1 (PID controller) brings back the line 

**226** 

Authorized licensed use limited to: ASTON UNIVERSITY. Downloaded on September 01,2026 at 20:40:00 UTC from IEEE Xplore.  Restrictions apply. 

pack pressure to its set point value by manipulating the control valve 1, thereby feeding the requisite amount of methane to the reformer inlet. The switching controller takes care of selecting between the battery and fuel cell based on a list of energy management policies which will be discussed in the future section. More details on the integrated reformer membrane fuel cell system can be obtained from the earlier paper [4]. 

## III. FUEL PROCESSING SUBSYSTEM: Auto thermal reformer 

An auto thermal reformer that utilizes methane as the fuel to generate hydrogen is used as the fuel processing subsystem. The upstream part of the reactor is dominated by the highly exothermic oxidation reaction while the endothermic steam reforming reactions dominates the downstream part. For the simulation studies, a steam to carbon molar ratio of 1:1 and oxygen to carbon molar ratio of 0.45:1 is considered. Out of many reactions expected to arise, only the dominant set of reactions are considered in this study [4]. 

In order to perform the dynamic studies of the auto thermal reformer, a one-dimensional dynamic model is selected from [7]. The reformer comprises of a cylindrical reactor of 0.2m in length and with Nickel as the catalyst having a density of 1870 _kg/m_<sup>3</sup> . Both the gas feed as well as catalyst temperature is maintained at a value of 542<sup>_o_</sup> C. The reformer operating pressure is chosen to be 1.5 atm with a Gas Hourly Space Velocity (GHSV) of 3071 _h_<sup>_−_1</sup> implying a residence time of 1.17s and a gas mass flow velocity of 0.15 _kg/m_<sup>2</sup> _s_ . In an earlier paper, mathematical model equations of the auto thermal reformer were already discussed and the reader is directed to refer [4] for better understanding of the model. 

## IV. FUEL PURIFICATION SUBSYSTEM: Palladium based membrane separation 

Availability of pure hydrogen gas at the anode inlet is a critical requirement for the efficient operation of a PEMFC. Presence of impurities in the feed can cause deterioration in the efficiency and lifetime of the fuel cell due to poisoning of the catalyst. Palladium alloy based membrane separation is adopted as the method for hydrogen gas purification from mixture of other gases [8]. Palladium membrane is reported to have low permeability for other gases compared to hydrogen gas which fits them good enough for either portable or stationary applications. In this particular study, palladium membrane is assumed to be free of defects as well as without any physical porous support. For the current study, the membrane permeability is assumed to be zero for all the other gas species except hydrogen. For more information on the model equations related to the molar flow rate of hydrogen permeating through the membrane and the membrane permeability, the reader is directed to refer to the earlier paper [4]. 

## V. POWER GENERATION SUBSYSTEM : PEMFC and Battery 

## _A. PEMFC_ 

Low temperature PEMFC that utilizes pure hydrogen gas at the anode side and oxygen/air at the cathode side can be effectively employed as the power generation subsystem for either portable or stationary applications. As soon as the reactants reach the active catalyst sites through the fuel cell electrodes, electrochemical reactions initiate which further lead to electric power generation. A single cell typically has an open circuit voltage of around 1 V and under load, it drops down to around 0.6 to 0.7 V. Real world applications demand electricity of the order of several tens or hundreds of volts. In order to achieve these high voltage values, individual fuel cells are stacked in series so that the aggregate voltage fits any specified voltage requirement. For better conductivity, the polymer membrane needs to be hydrated with water which constraints the fuel cell operation at temperatures below 90<sup>_o_</sup> C. More details on the maximum power rating of the designed fuel cell system, model equations governing consumption of each species, temperature variation of the membrane and the voltage obtained from the cell can be obtained by referring to an earlier paper [4]. 

## _B. Battery_ 

Battery modeling is one of the major considerations in the area of electric vehicles as well as hybrid electric vehicles. State-of-charge ( _SOC_ ) is the most important parameter of a battery which is defined as the ratio of the used capacity to the total capacity [9]. Change in _SOC_ of a battery for a time interval ∆ _T_ can be expressed as follows. 





Total capacity is the rated _Ah_ capacity of the battery. Ideally, it can be interpreted that _SOC_ of a battery will be one when the battery is fully charged and zero when discharged to a critical voltage. It is a usual practice to maintain the _SOC_ at a value between 0.5 and 0.7 [10]. 

A mathematical model of battery was presented in the ADVISOR HEV model [10] wherein battery was considered as a pure resistance source. The authors in [10] used the battery open circuit voltage _Voc_ and internal resistance _R_ , for each specific _SOC_ to calculate the battery terminal voltage _Vterminal_ and output current _I_ . However, they reported that this approach of model development is not practically viable as the values of _Voc_ and _R_ are not readily available from the battery specifications and also because the data on _Voc_ and _R_ are difficult to obtain in practice [10]. Using the experimental data obtained, a plot for the battery capacity curve was developed in [10] showing the relation between _Ah_ and _I_ 

**227** 

Authorized licensed use limited to: ASTON UNIVERSITY. Downloaded on September 01,2026 at 20:40:00 UTC from IEEE Xplore.  Restrictions apply. 

TABLE I 

Energy management policy of switching controller 

|Logic|Condition|Status|
|---|---|---|
|_L_1|_P_1 _<_= 1_._3_∗P_2 & _SOCbat < SOClow_|Battery OFF<br>Fuel cell OFF|
|_L_2|_P_1 _<_= 1_._3_∗P_2 & _SOCbat > SOClow_ & _abs_(_PF C −PD_)_>_0_._015|Battery ON<br>Fuel cell OFF|
|_L_3|_P_1 _>_1_._3_∗P_2 & _SOCbat < SOChigh_ & _abs_(_PF C −PD_)_<_0_._015|Battery CHARGING<br>Fuel cell ON|
|_L_4|_P_1 _>_1_._3_∗P_2 & _SOCbat < SOClow_ & _abs_(_PF C −PD_)_>_0_._015|Battery IDLE<br>Fuel cell ON|
|_L_5|_P_1 _>_1_._3_∗P_2 & _SOCbat > SOClow_ & _abs_(_PF C −PD_)_>_0_._015|Battery ON<br>Fuel cell ON|
|_L_6|_P_1 _>_1_._3_∗P_2 & _SOCbat >_=_SOChigh_ & _abs_(_PF C −PD_)_<_0_._015|Battery CHARGE FULL<br>Fuel cell ON|



and the results were compared with the manufacturer’s specifications. Using linear curve fitting, plot of _Vterminal_ versus _I_ corresponding to a given _SOC_ were generated and an empirical relation between the parameters were developed as follows. In this work, we have adopted this empirical relationship for the battery model. 



Specifically, 

a = -0.18, b = 172, c = 40 for _SOC <_ 0 _._ 4 a = -0.20, b = 186.94, c = 4 for 1 _> SOC >_ = 0 _._ 4 

Expression for power demanded from the battery is given by 



Substituting the expression for _Vterminal_ from eq.(3) in eq.(4), we obtain the expression to calculate current _I_ given by 



For a given _SOC_ of the battery and power demanded from the battery, battery charge/discharge current _I_ can be calculated. _I_ is assumed to be positive while discharging and negative while charging. 

## VI. SWITCHING CONTROLLER 

The switching controller is a logic based controller in order to switch between the fuel cell and battery to achieve a delay free response to the power demand. There is always a time lag associated with the power demanded by the electric load and the power delivered by the fuel cell. One reason for this can be due to the sluggish response of the complex fuel processing subsystem and other can be due to the delay associated with the control valve 2 dynamics based on the command from the controller 2. The switching controller operates on an energy management policy as documented in Table I. _P_ 1 denotes the hydrogen pressure in the line pack, _P_ 2 denotes the fuel cell pressure (1 atm), _SOCbat_ indicates 

the State of Charge of the battery at a given time instant, _SOClow_ and _SOChigh_ denotes the SOC lower and upper limits of the battery respectively. During the plant startup, _SOClow_ and _SOChigh_ values are set equal to 0.2 and 0.8 respectively. _PF C_ and _PD_ denotes the power delivered by the fuel cell and power demanded by the electric load in kW respectively. 

## VII. CASE STUDY : Start-up of the integrated system with battery back-up and switching controller 

During cold start of the plant, it takes considerable amount of time for the fuel processing subsystem to produce hydrogen to be fed to the fuel cell to generate power. The rate of hydrogen production at the reformer depends on the percentage opening of the control valve 1 which is maintained at a position of 90% during the plant start-up. The non-return valve (NRV) restricts the flow of hydrogen from the reformer exit until the upstream pressure (reformer exit pressure) exceeds the downstream pressure (line pack pressure). The line pack is assumed to be initially filled with some amount of hydrogen so as to maintain a line pack pressure of 1 atm. However, this does not satisfy the condition for the control valve 2 to open and supply hydrogen to fuel cell because of the operating policy _L_ 2. Opening of control valve 2 is permitted only when the upstream line pack pressure ( _P_ 1) becomes 1.3 times greater than the downstream fuel cell pressure ( _P_ 2). At start, the logic _L_ 2 holds true for a time period of 215s during which battery supplies power to the load and fuel cell remains OFF. At 215s, the logic _L_ 2 fails and _L_ 5 becomes active wherein both battery and fuel cell jointly supplies power to the load. This is because fuel cell alone is unable to generate the target load power. At 225s, fuel cell becomes capable enough to serve the power demanded by the load. Thus, the difference between _PF C_ and _PD_ becomes less than an acceptable offset value of 0.015 kW. Due to this, logic _L_ 5 fails and _L_ 3 becomes active and the battery goes to charging mode and fuel cell starts charging the battery as well as supplying power to the external load. Once the battery gets fully charged, logic _L_ 3 fails and the logic _L_ 6 becomes active. This condition 

**228** 

Authorized licensed use limited to: ASTON UNIVERSITY. Downloaded on September 01,2026 at 20:40:00 UTC from IEEE Xplore.  Restrictions apply. 



<!-- Start of picture text -->
25<br>20<br>15<br>10<br>5<br>0<br>0 200 400 600 800 1000<br>Time [s]<br>3Molar conc. of H at reformer output [mol/m]2<br><!-- End of picture text -->

Fig. 2. Molar concentration of _H_ 2 at reformer output 



<!-- Start of picture text -->
21.5<br>21 Desired H2 conc. in the line pack<br>20.5 Actual H2 conc. in the line pack<br>20<br>19.5<br>19<br>18.5 Non-return valve opens at 158s<br>18<br>0 200 400 600 800 1000<br>Time [s]<br>3Molar conc. of H in the line pack [mol/m]2<br><!-- End of picture text -->

Fig. 3. Molar concentration of _H_ 2 in the line pack 

occurs at around 400s in the present case study, after which the fuel cell lowers the extra power generated for charging the battery. During the plant operation, there can be a possibility of quantity of hydrogen becoming lower than required and the battery _SOC_ becoming lower than the lower bound _SOClow_ . This condition satisfies the logic _L_ 1 thereby switching OFF both the power sources. This gives an indication or alert signal of low fuel and low battery charge to the vehicle driver. 

The dynamic profile of the molar concentration of hydrogen at the reformer exit is as shown in Figure 2. It can be noticed that the molar concentration starts increasing and settles to a steady state value of around 21 _mol/m_<sup>3</sup> . Figure 3 compares the profiles for the desired and actual molar concentration of hydrogen in the line pack. The flow of hydrogen through the NRV is restricted due to low upstream pressure in comparison to the high downstream pressure until 158s beyond which flow starts and the line pack pressure starts building up. After the NRV opens at 158s, the controller 1 regulates the _H_ 2 concentration in the line pack to the desired concentration by manipulating the flow of methane using control valve 1. The molar flow rate of hydrogen through the palladium membrane depicted in Figure 4 is found to be increasing as soon as the NRV opens at 158s. 

It can be seen that the flow rate starts dropping at around 180s due to pressure buildup in the line pack and hence a reduced pressure difference. A sudden increase in the flow rate can be observed at around 215s when the control valve 2 opens. It can also be noticed that at around 225s, fuel cell becomes capable of delivering the full power 



<!-- Start of picture text -->
4.5 × 10 -5<br>4 Flow rate starts dropping at 180s due to<br>      pressure buildup in the line pack<br>3.5<br>3 Battery starts charging at 225s<br>2.5 Control valve 2 opens at 215s<br>2 Battery gets fully charged at 400s<br>1.5<br>Non-return valve opens at 158s<br>1<br>0.5<br>0<br>0 100 200 300 400 500 600 700 800 900 1000<br>Time [s]<br>Molar flow rate of H 2 through palladium<br>2.5 × 10 -5<br>Battery gets fully charged at 400s<br>2<br>1.5<br>Battery starts charging at 225s<br>1<br>0.5<br>Control valve 2 opens at 215s<br>0<br>0 200 400 600 800 1000<br>Time [s]<br>Molar flowrate of H through 2 palladium membrane [mol/s]<br>Molar flowrate of H through 2<br>control valve 2 to fuel cell [mol/s]<br><!-- End of picture text -->

Fig. 4. Molar flow rate of _H_ 2 through palladium membrane 

Fig. 5. Molar flow rate of _H_ 2 through control valve 2 to fuel cell 

demanded by the electric load and thus the battery starts charging from the extra power delivered by the fuel cell. At 400s, the battery gets fully charged thus the extra power delivered by the fuel cell for charging the battery is no longer needed. The molar flow rate of hydrogen to the fuel cell through the control valve 2 based on its opening is shown in Figure 5. Based on the energy management policy already discussed, the switching controller takes actions as illustrated in Figure 6 to switch between the battery and fuel cell for a delay-free delivery of power to the external load. The percentage opening of the control valve 1 and control valve 2 manipulated by their respective controllers can be seen from Figure 7 and Figure 8 respectively. The profile for change in state of charge of the battery is depicted in Figure 9. It can be noticed that during plant start-up, the SOC starts from _SOChigh_ value and decreases during battery discharging and increases during battery charging. 

## VIII. Conclusions 

In an earlier work, the mathematical model of an integrated reformer membrane fuel cell system was developed, wherein the necessity for an auxiliary power source like battery or super-capacitor was highlighted. This is due to the difference in dynamics associated with the sluggish behavior of the reformer compared to the fuel cell system. The integrated system was simulated with a multi loop control strategy choosing power demanded by the electric load and molar concentration of hydrogen in the line pack as the controlled variables. A battery model was adopted which gives the relation between the state of charge and 

**229** 

Authorized licensed use limited to: ASTON UNIVERSITY. Downloaded on September 01,2026 at 20:40:00 UTC from IEEE Xplore.  Restrictions apply. 



<!-- Start of picture text -->
25<br>Electric load power demand<br>20 Extra power P Battery<br>for charging PFuelcell<br>15 the battery<br>10<br>5<br>0<br>  Battery ON   Battery CHARGING   Battery CHARGE FULL<br>-5 Fuel cell OFF         Fuel cell ON           Fuel cell ON<br>-10   Battery ON<br> Fuel cell ON<br>-15<br>-20<br>0 100 200 300 400 500 600 700 800 900 1000<br>Time [s]<br>Power [kW]<br><!-- End of picture text -->

Fig. 6. Profile of the power delivered to the external load 



<!-- Start of picture text -->
100<br>Control valve 2 opens at 215s<br>90<br>80<br>70<br>60<br>50<br>Battery gets fully charged at 400s<br>40<br>0 200 400 600 800 1000<br>Time [s]<br>Control valve 1 opening [%]<br><!-- End of picture text -->

Fig. 7. Percentage opening of control valve 1 



<!-- Start of picture text -->
100<br>90<br>80<br>Battery gets fully charged at 400s<br>70<br>60<br>50<br>40<br>30<br>20<br>Control valve 2 opens at 215s<br>10<br>0<br>0 200 400 600 800 1000<br>Time [s]<br>Control valve 2 opening [%]<br><!-- End of picture text -->

Fig. 8. Percentage opening of control valve 2 



<!-- Start of picture text -->
85<br> Battery Discharging<br>     Fuel cell OFF<br>80<br> Battery Discharging<br>75       Fuel cell ON<br>70<br>   Battery Charging<br>      Fuel cell ON<br>65<br>   Battery Charge FULL<br>60       Fuel cell ON<br>55<br>0 200 400 600 800 1000<br>Time [s]<br>State of charge of battery [%]<br><!-- End of picture text -->

power demanded from the battery. A switching controller operating on an energy management policy is designed to switch between the battery and fuel cell to offer a delay free response during start-up of the plant and during frequent load demand variations. The simulation results demonstrate a delay free delivery of power to the external load with negligible offset justifying the effectiveness of the fuel cell battery system 

## References 

- [1] Integrated fuel processors for fuel cell application: A review, Fuel Processing Technology 88 (1) (2007) 3 – 22. 

- [2] M. D. Falco, Pd-based membrane steam reformers: A simulation study of reactor performance, International Journal of Hydrogen Energy 33 (12) (2008) 3036 – 3040. 

- [3] B. J. Bowers, J. L. Zhao, M. Ruffo, R. Khan, D. Dattatraya, N. Dushman, J.-C. Beziat, F. Boudjemaa, Onboard fuel processor for pem fuel cell vehicles, International Journal of Hydrogen Energy 32 (10) (2007) 1437 – 1442. 

- [4] P. Pravin, R. D. Gudi, S. Bhartiya, Dynamic modeling of an integrated reformer membrane fuel cell system, IFACPapersOnLine 50 (1) (2017) 10790 – 10795, 20th IFAC World Congress. 

- [5] I. J. Iwuchukwu, A. Sheth, Mathematical modeling of high temperature and high-pressure dense membrane separation of hydrogen from gasification, Chemical Engineering and Processing: Process Intensification 47 (8) (2008) 1292 – 1304. 

- [6] J. Okazaki, T. Ikeda, D. A. P. Tanaka, K. Sato, T. M. Suzuki, F. Mizukami, An investigation of thermal stability of thin palladiumâĂŞsilver alloy membranes for high temperature hydrogen separation, Journal of Membrane Science 366 (1) (2011) 212 – 219. 

- [7] M. Halabi, M. de Croon, J. van der Schaaf, P. Cobden, J. Schouten, Modeling and analysis of autothermal reforming of methane to hydrogen in a fixed bed reformer, Chemical Engineering Journal 137 (3) (2008) 568 – 578. 

- [8] P. Pinacci, F. Drago, Influence of the support on permeation of palladium composite membranes in presence of sweep gas, Catalysis Today 193 (1) (2012) 186 – 193, proceedings of the 10th International Conference on Catalysis in Membrane Reactors. 

- [9] X. He, J. W. Hodgson, Modeling and simulation for hybrid electric vehicles. i. modeling, IEEE Transactions on Intelligent Transportation Systems 3 (4) (2002) 235–243. 

- [10] P. Kolavennu, J. Telotte, S. Palanki, Analysis of battery backup and switching controller for a fuel-cell powered automobile 34. 

Fig. 9. State of charge of the battery 

**230** 

Authorized licensed use limited to: ASTON UNIVERSITY. Downloaded on September 01,2026 at 20:40:00 UTC from IEEE Xplore.  Restrictions apply. 

