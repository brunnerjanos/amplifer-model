Oláh, Tarcsay & Brunner 2021 at KOKI
------------------------------------------------------------
CONCEPT:
This model contains the realistic CC amplifier together with the realistic pipette representation and a biphysically realistic reconstruction of a somatically labelled, well preserved mossy fiber. We used this model arrangement to explore the relative contribution of observer and filtering effects to the overall measurement error. We ran simulated experiments with the same instrumental parameters but from different axonal segments. 
This model will show measured/local/native AP waveforms "recorded" from biophysically diverse axonal compartments.      


DESCRIPTION OF FILES:
start.hoc			-initiates the simulation. It also creates a GUI for the simulation.

filter_settings.hoc	-set the parameters of the implemented 4-pole Bessel filter.
						set_filter($01,$02) needs to be called to modify the filter characteristics
							arg1=cutoff frequency of the output voltage
							arg2=cutoff frequency of the current command					
							
custominit.hoc		-modified model initiation that allows for the model variables to reach their 
						steady-state before actual simulation starts   

CC.ses				-session file that contains the amplifier and pipette representation (a LinearCircuit)

bjd1218.hoc			-reconstructed GC with well preserved mossy fiber 


hh_bj.mod			-modified HH mechanism





mechanism needs to be compiled before launching the simulations
