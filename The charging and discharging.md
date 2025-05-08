Time Constant:
$$  
\tau = RC
$$
We  know for RC charging equation is:
$$
V(t) = V_{cc} *(1-e^{-(t/\tau)})\\
$$
**Note:**(The threshold and trigger voltage is taken as final and initial voltage of capacitor.
Through the Diode and with initial voltage of 0.5*control voltage.)
$$
V(t) = (V_{cc}-V_D) - (V_{cc}-V_D-V_{initial})e^{-(t/\tau)})\\
$$
let V(t) = V-final
thus:
$$
t = -\tau * \ln (\frac {V_{cc}-V_D -V_{final}} { V_{cc}-V_D-V_{initial}})
$$
for charging
$$
V_{cc} = 12V, V_D = 0.7V\\
V_{final} = V_{CV} , V_{initial} = 0.5*V_{CV}
$$
***Note***: (V-initial is 0.5 times V-final is because of 555 timer design. The final voltage is equal to Control pin Voltage of 555 timer.)
$$
t = -\tau * \ln( \frac { 12-0.7-V_{CV} } {12-0.7-0.5*V_{CV} })
$$
$$
t = -\tau * \ln (\frac{11.3-V_{CV}} { 11.3-0.5*V_{CV} })
$$

| **Control Voltage(V)** | **Charging time** |
| ------- | ------- |
| 10 | 1.58 Time Constant
| 9 | 1.1 Time Constant
| 8 | 0.8 Time Constant
| 7 | 0.6 Time Constant
| 6 | 0.45 Time Constant
| 5 | 0.33 Time Constant
| 4 | 0.24 Time Constant

----------------------------------------------
----------------------------------------------
we know the discharging equation is:
$$
V(t) = V_{0} *(e^{-(t/\tau)})\\
$$
In the Discharge path Diode is revers biased.
thus:
$$
V_{final} = V_{initial}*e^{-(t/\tau)}
$$
thus the time will be:
$$
t = -\tau * \ln( \frac {V_{final}} {V_{initial}})
$$
For discharging:
$$
V_{inital} = V_{CV} ,
V_{final} = 0.5*V_{CV}
$$

$$t = -\tau \ln(\frac{0.5*V_{CV}} {V_{CV}})$$
$$t = -\tau *\ln (0.5)$$
$$t = \tau *0.693$$

thus shows that the discharging time is independent of the Control Voltage and is only depended on the RC Time Constant.




