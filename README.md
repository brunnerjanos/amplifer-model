# amplifer-model

Uploaded models relate to the manuscript entitled:
"Small size of recorded neuronal structures confine the accuracy in direct axonal voltage measurements"
	Viktor János Oláh, Gergely Tarcsay and János Brunner
								2021			
----------------------------------------------------------------------------------------------------------
Simulations have been tested using NEURON 7.4-7.6 under Windows10 	

Folder description:

1_amplifier construction --- contains three model session to illustrate the tuning of the amplifier model
					predicting Rf associated stray capacitance
					compensations in CC mode
					boosted_VC_circuit
					
2_VC and CC operation --- contains two model session in which we show how the model amplifier operates by
						  simulating idelaized expereimental conditions  
					current-clamp
					voltage-clamp

3_real experiment reconstruction --- it is a single model session which shows the model representation of a 
									 direct axonal voltage recording used for the prediction of native AP 
									 shape and underliing conductances 
					AP_generator
					
					
Any feedbacks, questions or bug reports can be sent to: 
brunner.janos at koki.hu
