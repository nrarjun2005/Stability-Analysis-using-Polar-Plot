# Stability-Analysis-using-Polar-Plot
## Aim:
To analyse the stability of the system having open loop transfer function, G(S)=10/(S(1+0.5S)(1+0.2S)) using polar plot and verify it using MATLAB. 
## Apparatus Required:
Computer with MATLAB software

## Theory:
![WhatsApp Image 2025-11-27 at 23 37 23_d2e7ca80](https://github.com/user-attachments/assets/8234da5b-db19-4bbc-a47d-30a68c0f06d8)
![WhatsApp Image 2025-11-27 at 23 37 24_710f9fb8](https://github.com/user-attachments/assets/bcdd699e-29c3-46d4-864c-4ca3414d3da3)
![WhatsApp Image 2025-11-27 at 23 37 23_86fbd7c8](https://github.com/user-attachments/assets/98a9b302-2e9c-4451-800e-4037d731f376)
![WhatsApp Image 2025-11-27 at 23 37 23_c9301326](https://github.com/user-attachments/assets/6efa1636-95ab-4aba-b36a-0e988456134a)






## Procedure:
	Open MATLAB software
	Open a new script file.
	Type the program.
	Save and Execute the program.
	Determine the gain crossover frequency, phase cross over frequency, gain margin and phase margin.
	Also determine the stability.

## Program: 
num=[10]<br>
den=[0.1 0.7 1 0]<br>
sys=tf(num,den)<br>
[mag,phase,W] =bode(sys)<br>
mag=squeeze(mag)<br>
phase=squeeze(phase)<br>
phase1=deg2rad(phase)<br>
polarplot(phase1,mag,'linewidth',1.5)<br>
grid on<br>
[Gm Pm Wpc Wgc ]=margin(sys)<br>
if(Wpc>Wgc)<br>
    disp('stable,)<br>
elseif(Wpc == Wgc)<br>
    disp('marginally stable')<br>
else<br>
    disp('unsatble')<br>
end
## Output:
<img width="713" height="640" alt="image" src="https://github.com/user-attachments/assets/a1e2dc05-3608-4ad6-8314-44430e9bd608" />


## Result:
Thus the polar plot for the given transfer function was drawn and verified using MATLAB. <br>
Gain margin = 0.7 <br>
Phase Margin = -8.8865 <br>
Gain crossover frequency = 3.7565 <br>
Phase crossover frequency = 3.1623 <br>
The system is unstable
