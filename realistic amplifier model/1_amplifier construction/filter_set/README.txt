Oláh, Tarcsay & Brunner 2021 at KOKI
------------------------------------------------------------
CONCEPT:
This simulations show the filtering capabilities of the 4-pole low-pass Bessel filter implemented in the model.
For the filter implementation, we applied real filter parameters obtained with: https://tools.analog.com/en/filterwizard/


DESCRIPTION OF FILES:
start.hoc			-initiates the simulation. 

filter_settings.hoc	-set the parameters of the implemented 4-pole Bessel filter.
						set_filter($01) needs to be called to modify the filter characteristics
							note that VC filter implementation has single argument, as we applied
							filter only for the output current
							arg1=cutoff frequency of the output current
					

VC_boost.ses			-session file that contains the VC amplifier representation (a LinearCircuit), 
						the RunControl

modelcell and test_1 folders contain experimental data 
