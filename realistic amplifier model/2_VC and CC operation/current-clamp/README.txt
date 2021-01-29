Oláh, Tarcsay & Brunner 2021 at KOKI
------------------------------------------------------------
CONCEPT:
This simulation demonstrate how the final CC model operates.
The model consists of the CC amplifier together with idealized pipette- and cell representation.  


DESCRIPTION OF FILES:
start.hoc			-initiates the simulation. It also creates a GUI for the simulation.

filter_settings.hoc	-set the parameters of the implemented 4-pole Bessel filter.
						set_filter($01,$02) needs to be called to modify the filter characteristics
							arg1=cutoff frequency of the output voltage
							arg2=cutoff frequency of the current command					
							
custominit.hoc		-modified model initiation that allows for the model variables to reach their 
						steady-state before actual simulation starts   

CC.ses			-session file that contains the amplifier representation (a LinearCircuit), 
						the RunControl and some of the graphs
