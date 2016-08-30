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


#----------------------------------
#----------------------------------
#设置首字母大小写
l = ['adam','LISA','bsrT']

def name(x):
    
    return x[0].upper() + x[1:].lower()

print map(name,l)


#--------------------------------------
#--------------------------------------
#使用reduce函数循环求一个数列的积
L = [1,2,3,4,5]

def prod(y,z):
    
    y = y*z 
     
    return y 

print reduce(prod, L)

#======================================
#--coding:utf-8 --
#create a mew file.
def createfile():
    import os
    
    ls = os.linesep
    
    #get filename 
    
    
    
    
    
    while True:
         
        fname = raw_input('create your file name>')
        #输入创建的文件名并赋值给左边变量
         
        #判断文件名称是否存在，档文件名存在就一直循环下去
        if os.path.exists(fname):
             
            print "ERROR:'%s' already exists" % fname
             
             
        else:
             
            break
    
    #get file content (text) line
    all = []
    
    print "\n Enter lines ('.' by itself to quit).\n"
    
    #loop until user terminates input 
    
    while True:
        
        entry = raw_input('>')
        
        if entry == '.':
            
            break
        
        else:
            
            all.append(entry)
    
    #write  lines to file with proper line-ending
    fobj = open(fname,'w')
    #打开文件准备进行写操作
    
    fobj.writelines('%s%s' % (x,ls) for x in all)
    #'%s%s'为每行添加行结束符，（x,ls)表示每一行及其结束符。
    fobj.close()
    
    print 'DONE!'

def openfile():
    fname = raw_input('Enter filename:')
    
    print '\n'
    
    #attempt to open file reading 
    
    try:
        
        fobj = open(fname,'r')
        
    except IOError,e:
        
        print "*** file open error:",e 
        
    else:
        
        #display contents to the screen 
        
        for eachLine in fobj:
            
            print eachLine,
            
        fobj.close()  


def start():
    
    file_choose = raw_input('make your choose>')
    
    if int(file_choose) == 1:
        
        print "create a new file"
        
        createfile()
        
    elif int(file_choose) == 2:
        
        print "Open a file!"
        
        openfile()
        
    else:
        
        print "Please enter the number 1 or 2!"
        
        start()


print "What do you want to do?"
    
print "If you want to create a new file,please enter number:1"
    
print "If you want to open a file,please enter number:2"

start()

    
    


