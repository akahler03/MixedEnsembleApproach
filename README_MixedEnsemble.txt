This contains the code developed for the thesis		
Tailoring hydrologic models for improved water resources decision support: A mixed ensemble approach		
12-May-23		
		
Primary variables to change		
test		     the number of iterations to run the mixed ensemble
ensemble_size	     the number of models in the initial ensemble
metropolis_rounds    the number of perturbations
Pnum		     the number of parameter sets in Parameter Space
		
Variables to change for further exploration and analysis		
x_obs	     distance to monitoring well	
x_pred	     distance to point of compliance	
t_end	     total time of observations	
t_end_pred   total time of prediction	
		
U_th	  stakeholder utility threshold	
C_0	  concentration values above this level have zero utility for stakeholder	
C_1	  concentration values below this level have full utility for stakeholder	
		
Sequence of operations in main block		
cell #1	        outside loop to create Parameter Space, designate truth model, calculate maximum concentration	
cell #85	inner loop to select metropolis models	
cell #157	return to main loop, create MOC ensemble	
cell #174	terminate run if there are insufficient MOCs	
cell #212	inner loop to select metropolis models for MOC ensemble	
cell #286	return to main loop to create mixed ensemble	
cell #359	plot cumulative likelihood-utility for truth MOC, for truth not_MOC	
cell #410	creating truth matrix of results	
