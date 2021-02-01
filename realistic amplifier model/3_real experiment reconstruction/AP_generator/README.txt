Oláh, Tarcsay & Brunner 2021 at KOKI
------------------------------------------------------------
CONCEPT:
This model contains the realistic CC amplifier together with the realistic pipette representation 
and a biphysically realistic reconstructed mossy fiber. We used this model arrangement to reconstruct
the recorded AP waveforms and to predict native AP parameters.    

This simulation shows some of the recorded data together with their optimalized model representation.


DESCRIPTION OF FILES:
start.hoc			-initiates the simulation. It also creates a GUI for the simulation.

filter_settings.hoc	-set the parameters of the implemented 4-pole Bessel filter.
						set_filter($01,$02) needs to be called to modify the filter characteristics
							arg1=cutoff frequency of the output voltage
							arg2=cutoff frequency of the current command					
							
custominit.hoc		-modified model initiation that allows for the model variables to reach their 
						steady-state before actual simulation starts   

CC.ses				-session file that contains the amplifier and pipette representation (a LinearCircuit), 
						the RunControl and some of the graphs

bjd1375.hoc			-reconstructed axonal morphology 

real data folder 	-experimental data 						

settrace.hoc		-function that reads the experimental data


hh_bj.mod			-modified HH mechanism
holding_current.mod	-point process mechanism to set the holding current at the recording site



mechanisms need to be compiled before launching the simulations
