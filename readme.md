***After set the environment with the _C++ compile_ and the _Boost library_***
**For more informations about the code equations, check the _JCN_2019_Eqs_Parameters_**
**How to compile**
> **If your platform is Windows**
- Double
1. Open the **_double_** directory and edit the make file *MakefileWin*, with the correct path for the compiler and Boost library. Then, execute the make command.	
2. After this, make sure that your have an HH_BBT2017_doubleP.exe file
3. For simulations with 100% neurons Excitatorys with vInh = 70 mV and dt = 0.01 type the following line code:
```HH_BBT2017_doubleP.exe -pExcN 1.0 -vInh 70```
- Then, It will create four files inside the results directory:
	- HH_BBT_rk4_dt0100_100,0,vI70,t=8s_double_IappDES,Epis.txt
	- HH_BBT_rk4_dt0100_100,0,vI70,t=8s_double_IappDES,Iapp.txt
	- HH_BBT_rk4_dt0100_100,0,vI70,t=8s_double_IappDES.txt
	- HH_BBT_rk4_dt0100_100_0_vI_70_t8s_double_IappDES_Spikes.m

4. For simulations with 80/20% Excitatory/Inhibitory with vInh = 70 mV and dt = 0.01 type the following line code:
```HH_BBT2017_doubleP.exe -pExcN 0.8 -vInh 70```
- Then, It will create four files inside the results directory:
	- HH_BBT_rk4_dt0100_100,20,vI70,t=8s_double_IappDES,Epis.txt
	- HH_BBT_rk4_dt0100_100,20,vI70,t=8s_double_IappDES,Iapp.txt
	- HH_BBT_rk4_dt0100_100,20,vI70,t=8s_double_IappDES.txt
	- HH_BBT_rk4_dt0100_100_20_vI_70_t8s_double_IappDES_Spikes.m

5. ***For dt = 0.05, change the line 33 in HH_BBT2017_doubleP.cpp by 'const double dt = 0.05;' . The generated files will be renamed with dt050, for example: _HH_BBT_rk4_dt050_100,0,vI70,t=8s_double_IappDES,Epis.txt_***
