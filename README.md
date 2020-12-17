# hMLMC
Multilevel Monte Carlo on Heterogeneous Computer Architectures

## Summary:
Calculate the optimal sample allocation for the Monte Carlo (MC) [1], Multilevel Monte Carlo (MLMC) [1], and Multilevel Monte Carlo on Hetergeneous Computer Architectures (hMLMC) [2] methods.

## Details: 
The MC methods (MC, MLMC, and hMLMC) are used to estimate the mean of a quantity of interest (estimator) for problems with stochastic inputs. This mean is estimated by sampling from the stochastic inputs and solving the problem for these inputs; each of these evaluations is called a sample. For MC we have a single type of processor and model. For MLMC we have a single type of processor and multiple models (called levels.) The levels have increasing cost and accuracy. For example, for a stochastic partial differential equation, these levels can be created by refining the mesh or the physics. For hMLMC we have two types of processors (such as CPUs and GPUs) and multiple levels. This code determines how many samples to run on each level and processor type to meet a desired variance with the smallest wall-clock time-to-solution (cost). The user must supply estimates of the cost and variance of running a sample on each level. 

The user can then run the number of samples on each level and processor type specified by MC, MLMC, or hMLMC and calculate the mean and variance of their quantity of interest using the MC, MLMC, or hMLMC method, respectively. MLMC aims to calculate the estimator at lower cost than MC when multiple levels are available. hMLMC aims to calculate the estimator at lower cost than MC or MLMC when multiple levels and processor types are available.

## References:
[1] M.B. Giles, 2018, Multilevel Monte Carlo methods, Acta Numerica, https://people.maths.ox.ac.uk/gilesm/files/acta15.pdf

[2] C. Adcock, L. Jofre, G. Iaccarino, 2020, Multilevel Monte Carlo Sampling on Heterogenous Computer Architectures, International Journal for Uncertainty Quantification, http://www.dl.begellhouse.com.stanford.idm.oclc.org/journals/52034eb04b657aea,3673619972b2eee6,2dc1fd2d0ec3d1c0.html
