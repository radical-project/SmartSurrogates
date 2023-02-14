This file is to show the calculations for various models.


a) To start with Alphafold calculation: -


The method adopted uses the formula for calculation: -

= Training Time * num_cores * peakflops/ sec * utilization rate

For Alphafold following assumtions were made: -

1. utilization rate = 50%
2. Training Time = initial training time + fine tuning = 1 week + 4 days = 11 days
3. num_cores = 128 for each TPU V3 * num_chips


=> 11 * 128 * 123 Tflops/ sec * 86400 sec * 50%

= 7.5 * 10^21

5 models trained with different seeds => 5 * 7.5 e^21 = 3.75 e^22 flops * num_chips

Info about num_chips not provided in any literature.


b) calculate the cost of PaLM 

- The paper describes the usage of TPU v4 chips. However, we try to calculate using the A100 as well as the v4 chips. This is mainly to compare the prices.
