Bubblecurtain V1

The bubble curtain class is a package that works with the SILENCE model.

It requires the dependencies stated in Requirements.txt

It also requires the SILENCE model to operate
---------------------
	INPUT
---------------------

path = folder where SILENCE software is situated
r = Distance of the bubblecurtain
smin = minimum width of the bubble curtain
smax = maximum width of the bubble curtain
airflow = airflow
mu = input parameters of the lognormal distribution, default = -6.7
sigma = input parameters of the lognormal distribution, default = 0.67


--------------------------------------
Methods for effective source reduction
--------------------------------------

mesh_r_fluid 				-> get mesh in the fluid
frequency_domain 			-> Get the frequency domain solution of the free field simulation
transmission_coeff(self,thickness) 	-> Calculate transmission coefficient for a certain thickness
reflection_coeff(self,thickness) 	-> Calculate reflection coefficient for a certain thickness
curtain_thickness(self) 		-> Calculate thickness based on height
plot_coeff_vs_f(self) 			-> Plot frequency dependant coefficients
plot_coeff_2D(self) 			-> Plot coefficient matrices
BBC(self) 				-> Make bubblecurtain for all heights
format_data(self, quantity='PRESSURE') 	-> Format all pressures (or Velocities)

--------------------------------
Methods for work of Bohne et al.
--------------------------------
bubble_size_distribution(self) 	-> Returns bubble size distribution
mean_bubble_volume(self) 	-> Returns mean bubble volume
bubble_solver(self)		-> Returns q vector, z vector and b vector q = [ulmz0, egm0    z= depth, b = half width
										ulmz1, egm1
										.	.		
										ulmzn, egmn]
eps_g(self)			-> returns volume fraction
N_bubbles(self) 		-> returns total number of bubbles

The functions in "Methods for work of bohne et al." are inherited in N_bubbles()
So the command N_bubbles runs the entire script.						