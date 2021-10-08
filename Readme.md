# **总结**
## **电路中的理想元件**
**电阻**：一般使用 R 进行表示，将电能转化为内能

**电容**：一般使用 C 来表示，将电能转化为磁场能

**电感**：使用 L 表示，将电能转化为磁场能

## 元件的特性方程
元件的特性方程是用来描述通过元件的电流与电压的对应关系的方程。
## 电阻特性方程
$$u(t)=Ri(t)$$
同时根据 $R$ 与时间是否有关划分时变与时不变，与 $i$ 是否有关划分线性与非线性。
## 电容特性方程
$$q(t)=Cu(t)$$
式中$q$表示通过导线横截面的面积，并导出
$$i(t)=\frac{dq}{dt}=C\frac{du}{dt}$$
*在直流情况下，电容两端的电压为常量,此时电流 i 恒为 0，符合开路的特征*

## 电感特性方程
$$\psi(t)=Li(t)$$
式中 $\psi$ 表示通过元件的磁通量，并进一步推得
$$u(t)=\frac{d\psi}{dt}=L\frac{di}{dt}$$
*在直流情况下，通过电感的电流为常量，此时两端电压恒为 0 ，可将电感视为导线*

# 电流、电压的相量表示
在正弦交流电路中，通常会将电流和电压通过虚数表示
$$i=\sqrt{2}Isin(\omega t+\varphi_i)
=\sqrt{2} Im [Ie^{j(\omega t+\varphi_i)}]
=\sqrt{2} Im [e^{j\omega t} \cdot Ie^{j\varphi_i}]$$
$$u=\sqrt{2}Usin(\omega t+\varphi_u)
=\sqrt{2} Im [Ue^{j(\omega t+\varphi_u)}]
=\sqrt{2} Im [e^{j\omega t} \cdot Ue^{j\varphi_u}]$$

## 阻抗定义
$$\mathring{I}=Ie^{j\varphi_i}$$
$$\mathring{U}=Ue^{j\varphi_u}$$
称为**相量**，相量是同时反映电压或电流幅值以及相位的量。

同时定义$Z=\frac{\mathring{U}}{\mathring{I}}$，称为**阻抗**。

## 电阻电路
<img src="https://raw.githubusercontent.com/whwh13/smms/master/%E5%9B%BE%E7%89%871.png" width="50%">



电阻的特性方程 $u(t)=Ri(t)$ ,将 $i=\sqrt{2}Isin(\omega t+\varphi_i) 和 u=\sqrt{2}Usin(\omega t+\varphi_u)$ 代入，有
$$Usin(\omega t+\varphi_u)=RIsin(\omega t+\varphi_i)$$
进一步导出
$$\begin{array}{l}
U=RI\\
\varphi_u=\varphi_i
\end{array}$$
利用阻抗的定义，$Z=\frac{\mathring{U}}{\mathring{I}}=\frac{Ue^{j\varphi_u}}{Ie^{j\varphi_i}}=R$
## 电容电路
<img src="https://raw.githubusercontent.com/whwh13/smms/master/%E5%9B%BE%E7%89%872.png" width="50%">

电容的特性方程 $q(t)=Cu(t)$ 即 $i(t)=C\frac{du(t)}{dt}$ ，将电阻与电流代入，可以得到
$$Isin(\omega t+\varphi_i)=C\omega u(t)cos(\omega t+\varphi_u)$$
进一步导出
$$\begin{array}{l}
I=C\omega U\\
\varphi_i=\varphi_u+\frac{\pi}{2}
\end{array}$$
通过阻抗的定义得出, $Z=-\frac{j}{C\omega}$

**当 $\omega$ 较大时，阻抗较小，即通高频，阻低频**
## 电感电路
<img src="https://raw.githubusercontent.com/whwh13/smms/master/111.png" width="50%">

电感的特性方程是 $u(t)=L\frac{di(t)}{dt}$ ,电流电压带入
$$Usin(\omega t+\varphi_u)=IL\omega COS(\omega t+\varphi_i)$$
$$\begin{array}{l}
U=IL\omega\\
\varphi_u=\varphi_i+\frac{\pi}{2}
\end{array}$$
得出阻抗为$Z=\frac{\mathring{U}}{\mathring{I}}=jL\omega$

**当 $\omega$ 较小时，阻抗较大，即通低频，阻高频**
# 举例
## 串联电路
$$\mathring{U}=\mathring{U_1}+\mathring{U_2}$$
$$\mathring{I}=\mathring{I_1}=\mathring{I_2}$$
因此 $Z=Z_1+Z_2$
## 并联电路
$$\mathring{I}=\mathring{I_1}+\mathring{I_2}$$
$$\mathring{U}=\mathring{U_1}=\mathring{U_2}$$
因此 $Z=\frac{1}{\frac{1}{Z_1}+\frac{1}{Z_2}}$
## 复合电路
<img src="https://raw.githubusercontent.com/whwh13/smms/master/10_8_1.jpg"/>

对于如图电路，支路1阻抗$Z_1=R+j\omega L$

支路2阻抗$Z=-\frac{j}{\omega C}$

对整体
$$Z=\frac{1}{\frac{1}{Z_1}+\frac{1}{Z_2}}=\frac{jR-\omega L}{j-\omega CR-j\omega^2 L}$$