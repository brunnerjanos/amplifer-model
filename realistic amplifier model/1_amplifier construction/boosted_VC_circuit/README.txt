Oláh, Tarcsay & Brunner 2021 at KOKI
------------------------------------------------------------
CONCEPT:
This model was used to simulate open circuit amplifier (MultiClamp700B) responses in VC mode.
We used this arrangement to predict size of the injector capacitor of the amplifier and to adjust 
the frequency profile of the current responses.

Using the amplifier's CC mode, we characterized the amount of Cstray associated with the Rf.
Rf associated Cstray slows down the amplifier responses in VC mode.
To restore the speed of the responses, we implemented a high frequency boost unit.  

This simulation shows the recorded open circuit amplifier response (to -5 mV voltage step) 
together with the model responses with- or without the boosting unit.



DESCRIPTION OF FILES:
start.hoc			-initiates the simulation. 

filter_settings.hoc	-set the parameters of the implemented 4-pole Bessel filter.
						set_filter($01) needs to be called to modify the filter characteristics
							note that VC filter implementation has single argument, as we applied
							filter only for the output current
							arg1=cutoff frequency of the output current
					

VC_boost.ses			-session file that contains the VC amplifier representation (a LinearCircuit), 
						the RunControl

recorded_data.dat		-experimental data 





note that VC simulations needs high temporal resolution!
