# EXP. NO: 03

# DATE: 


# <p align = "center"> Correlation and Regression for Data Analysis </p>
# Aim : 

To analyse given data using  coeffificient of correlation and regression line.
![image](https://user-images.githubusercontent.com/104613195/168224136-d6b64e64-7d3d-4775-9337-c8f96fe41f2d.png)


# Software required :  

Python

# Theory:

Correlation describes the strength of an association between two variables, and is completely symmetrical, the correlation between A and B is the same as the correlation between B and A. However, if the two variables are related it means that when one changes by a certain amount the other changes on an average by a certain amount.  

If y represents the dependent variable and x the independent variable, this relationship is described as the regression of y on x. The relationship can be represented by a simple equation called the regression equation. The regression equation representing how much y changes with any given change of x can be used to construct a regression line on a scatter diagram, and in the simplest case this is assumed to be a straight line.

# <br><br><br><br>Procedure :

![image](https://user-images.githubusercontent.com/104613195/168225866-ac8f6610-bdc3-4ac2-a24e-2b24ba08e189.png)

# Program
```python
Developed By:Kumaran.B
Register Number:212220230026
import math
import numpy as np
import matplotlib.pyplot as plt
x=[25,28,35,32,31,36,29,38,34,32]
y=[43,46,49,41,36,32,31,30,33,39]
tx=0
ty=0
txy=0
tx2=0
ty2=0
n=10
for i in range(0,10):
    tx=tx+x[i]
    ty=ty+y[i]
    txy=txy+(x[i]*y[i])
    tx2=tx2+x[i]**2
    ty2=ty2+y[i]**2
crc = (n*txy-tx*ty)/(math.sqrt(n*tx2-tx**2)*math.sqrt(n*ty2-ty**2))
rc=((n*txy)-(tx*ty))/((n*tx2)-(tx)**2)
rc 
mean_x=tx/10
mean_y=ty/10
plt.scatter(x,y,c='red')
def reg(x):
    return mean_y+rc*(x-mean_x)
x=np.linspace(20,40,51)
y1=reg(x)
print("The Correlation Coefficient is %.3f"%crc)
print("The regression line y on x is::: Y=%0.3f %0.3f(x-%0.3f)"%(mean_y,rc,mean_x))
plt.plot(x,y1,'g')
plt.xlabel("x-data")
plt.ylabel("y_data")
plt.legend(["Regression line","Datapoints"])
plt.show()
```

# Output : 
![Screenshot (242)](https://user-images.githubusercontent.com/75243072/170187517-3d7b87fa-1cf6-4a7a-93ee-46be7aa06cb6.png)

# Result:
Thus,we implemented a coeffificient of correlation and regression line on given data.
