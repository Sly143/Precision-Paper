# neural-numerical-replicability
This project aims to provide tools to analyse the influence of numerical imprecision under different platforms in the context of neural computational replicability, taking as a case study a small neural network composed of Hodgkin-Huxley-type neurons. The simulated models and their parameters are described in JCN_2019_Eqs_Parameters.pdf file. The project was implemented using C/C++ program language. The Ordinary Differential Equations (ODEs) were solved using Runge–Kutta fourth-order method (RK4), implemented by Boost C++ library, specifically Boost.Numeric.Odeint module.

# Software requirements:
- C/C++ compiler (ex: gcc)
- Make builder
- Boost C++ libraries (http://www.boost.org)
    ODEint module, to solving ordinary differential equations, is include in the distribution 

The source code includes the following files:<br>
Project Tree
  - Double precision
    - HH_BBT2017_doubleP.cpp
    - iappDist_doubleP.cpp
    - iappDist_doubleP.h
    - SpikeTrain_doubleP.cpp
    - SpikeTrain_doubleP.h
    - MakefileMacLinux
    - MakefileWin
    - ./results
  
  - Long Double precision
    - HH_BBT2017_LongDouble.cpp
    - iappDist_LongDouble.cpp
    - iappDist_LongDouble.h
    - SpikeTrain_LongDouble.cpp
    - SpikeTrain_LongDouble.h
    - MakefileMacLinux
    - MakefileWin
    - ./results
    
  - Boost Double precision
    - HH_BBT2017_Boost.cpp
    - iappDist_Boost.cpp
    - iappDist_Boost.h
    - SpikeTrain_Boost.cpp
    - SpikeTrain_Boost.h
    - MakefileMacLinux
    - MakefileWin
    - ./results
  
  - Figures
    - Fig1_as.m
    - Fig2_as.m
    - Fig3_as.m
    - Fig2_rp.m
    - Fig3_rp.m
    - Figure1.png
    - Figure1_dt005.png
    - Figure2.png
    - Figure2_dt005.png
    - Figure3.png
    - Figure3_dt005.png
    
***After set the environment with the _C++ compile_ and the _Boost library_***
**For more informations about the code equations, check the _JCN_2019_Eqs_Parameters_**
**How to compile**
> **If your platform is Windows**
- Double
1. Open the **_double_** directory and edit the make file *MakefileWin*, with the correct path for the compiler and Boost library. Then, execute the make command.	
2. After this, make sure that your have an HH_BBT2017_doubleP.exe file
3. For simulations with 100% neurons Excitatorys with vInh = 70 mV and dt = 0.01 type the following line code:
> HH_BBT2017_doubleP.exe -pExcN 1.0 -vInh 70


- Then, It will create four files inside the results directory:
	- HH_BBT_rk4_dt0100_100,0,vI70,t=8s_double_IappDES,Epis.txt
	- HH_BBT_rk4_dt0100_100,0,vI70,t=8s_double_IappDES,Iapp.txt
	- HH_BBT_rk4_dt0100_100,0,vI70,t=8s_double_IappDES.txt
	- HH_BBT_rk4_dt0100_100_0_vI_70_t8s_double_IappDES_Spikes.m

4. For simulations with 80/20% Excitatory/Inhibitory with vInh = 70 mV and dt = 0.01 type the following line code:
> HH_BBT2017_doubleP.exe -pExcN 0.8 -vInh 70


- Then, It will create four files inside the results directory:
	- HH_BBT_rk4_dt0100_100,20,vI70,t=8s_double_IappDES,Epis.txt
	- HH_BBT_rk4_dt0100_100,20,vI70,t=8s_double_IappDES,Iapp.txt
	- HH_BBT_rk4_dt0100_100,20,vI70,t=8s_double_IappDES.txt
	- HH_BBT_rk4_dt0100_100_20_vI_70_t8s_double_IappDES_Spikes.m

5. ***For dt = 0.05, change the line 33 in HH_BBT2017_doubleP.cpp by 'const double dt = 0.05;' . The generated files will be renamed with dt050, for example: _HH_BBT_rk4_dt0050_100,0,vI70,t=8s_double_IappDES,Epis.txt_***
