> **If your platform is Windows**
- Double
1. Open the **_double_** directory and edit the make file *MakefileWin*, with the correct path for the compiler and Boost library. Then, execute the make command.	
2. After this, make sure that your have an HH_BBT2017_doubleP.exe file
3. For simulations with 100% neurons Excitatorys with vInh = 70 mV and dt = 0.01 type the following line code:

> HH_BBT2017_doubleP.exe -pExcN 1.0 -vInh 70 <
Then, it will make four files inside the results directory, are they:
	 - HH_BBT_rk4_dt0100_100,0,vI70,t=8s_double_IappDES,Epis.txt
	 - HH_BBT_rk4_dt0100_100,0,vI70,t=8s_double_IappDES,Iapp.txt
	 - HH_BBT_rk4_dt0100_100,0,vI70,t=8s_double_IappDES.txt
	 - HH_BBT_rk4_dt0100_100_0_vI_70_t8s_double_IappDES_Spikes.m

4. For simulations with 80/20% Excitatory/Inhibitory with vInh = 70 mV and dt = 0.01 type the following line code:
> HH_BBT2017_doubleP.exe -pExcN 0.8 -vInh 70
Then, it will make four files inside the results directory, are they:
	 - HH_BBT_rk4_dt0100_100,20,vI70,t=8s_double_IappDES,Epis.txt
	 - HH_BBT_rk4_dt0100_100,20,vI70,t=8s_double_IappDES,Iapp.txt
	 - HH_BBT_rk4_dt0100_100,20,vI70,t=8s_double_IappDES.txt
	 - HH_BBT_rk4_dt0100_100_20_vI_70_t8s_double_IappDES_Spikes.m
