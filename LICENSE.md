# --coding:utf-8 --
#定义一个函数计算一元二次方程
import math 
def quadratic(a,b,c):
    
    if a == 0:
        
        x = -c / b 
        return x 
    elif b == 0:
        
        x = math.sqrt(-c/a)
        
        return x 
        
    elif b*b - 4*a*c >=0:
        
        x1 = (-b + math.sqrt(b*b -4*a*c)) / 2*a 
        
        x2 = (-b - math.sqrt(b*b -4*a*c)) / 2*a 
        
        return x1,x2  
     
    else:
        
        print "not answer!"
print quadratic(1, 0, -4)

print quadratic(1, 4, 2)
