Oláh, Tarcsay & Brunner 2021 at KOKI
------------------------------------------------------------
CONCEPT:
This model was used to simulate a modified 1U modelcell connected to an amplifier 
(MultiClamp700B) for investigation the properties of the compensatory mechanisms 
present in CC mode



Model cell circuit:

								|---R2(R_cell)----|
								|				  |
				|----R1(R_pip)---				  |--|
				|				|				  |	 |
 CC_input-------|				|---C2(C_cell)----|  |-----GRND
				|									 |					
				|-------------------C1(C_pip)--------|
				

We systematically varied cellular capacitance (C2), and recorded the voltage signals 
with and without optimal bridge balance (BB) and capacitance compensation (CPN) 
in the actual tests. 
The other modelcell parameters (R1=10 MOhm, C1=2.8 pF, R2=500 MOhm) were held constant.

This simulation shows some of the recorded data together with the responses of the 
optimalized model.



DESCRIPTION OF FILES:
start.hoc			-initiates the simulation. It also creates a GUI for the simulation.

filter_settings.hoc	-set the parameters of the implemented 4-pole Bessel filter.
						set_filter($01,$02) needs to be called to modify the filter characteristics
							arg1=cutoff frequency of the output voltage
							arg2=cutoff frequency of the current command					
							
custominit.hoc		-modified model initiation that allows for the model variables to reach their 
						steady-state before actual simulation starts   

BB_CPN.ses			-session file that contains the amplifier representation (a LinearCircuit), 
						the RunControl and some of the graphs

files with .dat extension contain experimental data 						