Oláh, Tarcsay & Brunner 2021 at KOKI
------------------------------------------------------------
CONCEPT:
This simulation demonstrate how the final VC model operates.
The model consists of the VC amplifier together with idealized pipette- and cell representation.  


DESCRIPTION OF FILES:
start.hoc			-initiates the simulation. It also creates a GUI for the simulation.

filter_settings.hoc	-set the parameters of the implemented 4-pole Bessel filter.
						set_filter($01) needs to be called to modify the filter characteristics
							note that VC filter implementation has single argument, as we applied
							filter only for the output current
							arg1=cutoff frequency of the output current

VC.ses			-session file that contains the amplifier representation (a LinearCircuit), 
						the RunControl and some of the graphs
