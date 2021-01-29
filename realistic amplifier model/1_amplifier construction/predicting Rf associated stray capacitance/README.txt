Oláh, Tarcsay & Brunner 2021 at KOKI
------------------------------------------------------------
CONCEPT:
This model was used to simulate the situation in which a simple load resistance
was connected to the amplifier ((MultiClamp700B). We used this arrangement to predict 
the stray capacitance (Cstray) associated with the Rf.
Rf is part of the current generator circuitry in CC mode.      


Model circuit:

 CC_input-----------R_load---------------------GRND	
												
parasitic capacitances of load resistance were also implemented
 
We varied the load resistance in the actual tests (20, 50 and 100 MOhm). 
Cstray acts as capacitance neutralization element:
with 20 and 50 MOhm Rload it actually overcompensates the amplifier's intrinsic 
capacitance.
The model was able to replicate this behavior when significant Cstray (0.3-0.5 pF) was applied.

This simulation shows the recorded data together with the model responses.



DESCRIPTION OF FILES:
start.hoc			-initiates the simulation. It also creates a GUI for the simulation.

filter_settings.hoc	-set the parameters of the implemented 4-pole Bessel filter.
						set_filter($01,$02) needs to be called to modify the filter characteristics
							arg1=cutoff frequency of the output voltage
							arg2=cutoff frequency of the current command					
							
custominit.hoc		-modified model initiation that allows for the model variables to reach their 
						steady-state before actual simulation starts   

Co_Rf.ses			-session file that contains the amplifier representation (a LinearCircuit), 
						the RunControl and some of the graphs

files with .dat extension contain experimental data 


