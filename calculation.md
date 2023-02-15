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

calculation is as follows: - 

PaLM training time = 1200 hrs on 6144 TPU v4 chips + 336 hrs on 3072 TPU V4 chips 

Utilization = 45% (varies between 45 - 57% )

the compute cost = 2.56 e^24 Flops

In case want to compute in dollars, the pricing is not mentioned on website, however we take the value of V3 TPU mentioned on the website.

The cost per flop for V3 TPU = 110.7 Pflops per $ (for TPU V3 we changed the utilisation to 50%)

cost = 2.56 e^24 / 110.7 e^15 = $ 23.1 M (it is important to note that these are based on teh commercial prices. The price incurred by Google wil be much lesser). 


Calculating the cost on Nvidia A100 (with 50% utilisation )- the cost comes out to be = $ 9 M. 

This is close to the value stated in the blog = $ 6.7 M.
