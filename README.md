# Assignment A1
#LIST
l=["Leto","Max","Anton"]
print("Original List:",l)

l.append("Lewellyn ")
print("After Adding:",l)

l[1]="Karl"
print("Updated list:",l)

#TUPLE
t=("Leto","Max","Anton")
print("Original Tuple:",t)

print("First Student",t[0])
print("Max count:",t.count("Max"))

#DICTIONARY
d={1:"Leto",2:"Max",3:"Anton"}
print("Origial dictionary:",d)

d[4]="Lewellyn"
print("Added dictionary:",d)

d[2]="Cole"
print("Updated dictionary:",d)



# Assignment A2

a = int(input("Enter 1st number: "))
b = int(input("Enter 2nd number: "))
c = int(input("Enter 3rd number: "))

if a == b == c:
    print("All three numbers are equal")

elif a == b and a > c:
    print("a and b are equal and greater than c")

elif a == c and a > b:
    print("a and c are equal and greater than b")

elif b == c and b > a:
    print("b and c are equal and greater than a")

elif a > b and a > c:
    print("a is greatest")

elif b > a and b > c:
    print("b is greatest")

else:
    print("c is greatest")



# Assignment A3

a=float(input("enter length of 1st side: "))
b=float(input("enter length of 2nd side: "))
c=float(input("enter length of 3rd side: "))

def check_triangle(s1,s2,s3):
    if s1*2 + s22==s32 or s22 + s32==s12 or s32 + s12==s2*2:
        print("it is a right angled triangle")
        if s1==s2 or s2==s3 or s3==s1:
            print("it is a right angled isoceles triangle")
    elif s1==s2 or s2==s3 or s3==s1:
        print("it is an isoceles triangle")
    else:
        print("it is a scalene triangle")
        
    

check_triangle(a,b,c)


# Assignment A4

#ADDITION OF 2 MATRICES USING NUMPY

import numpy as np
m1=np.array([[1,2,3],[3,4,5],[6,7,8]])
m2=np.array([[2,3,4],[5,6,7],[8,9,10]])
m3=m1+m2
print("Matrix 1:")
print(m1)

print("Matrix 2:")
print(m2)

print("Addition of two matrices:")
print(m3)


# Assignment A5

import re 
def check_chr(s): 
    return bool(re.fullmatch(r'[A-Za-z0-9]+', s)) 
text = input("Enter a string: ") 
if check_chr(text): 
    print("The string contains only a-z, A-Z, and 0-9.") 
else: 
    print("The string contains other characters.")


# Assignment A6

import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

df = pd.read_csv("data.csv")
print(df)

#LINE PLOT
plt.plot(df["Name"], df["Marks"])
plt.xlabel("Name")
plt.ylabel("Marks")
plt.title("Line Plot")
plt.show()

#BAR PLOT
plt.bar(df["Name"], df["Marks"])
plt.xlabel("Name")
plt.ylabel("Marks")
plt.title("Bar Plot")
plt.show()

#SCATTER PLOT
plt.scatter(df["Age"], df["Marks"])
plt.xlabel("Age")
plt.ylabel("Marks")
plt.title("Scatter Plot")
plt.show()

#HEATMAP
plt.figure(figsize=(6, 4))
sns.heatmap(df.select_dtypes("number").corr(),
            annot=True, cmap="coolwarm")
plt.title("Correlation Heatmap")
plt.show()


# Assignment A7

import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

df = pd.read_csv("data.csv")
print(df)

#LINE PLOT
plt.plot(df["Name"], df["Marks"])
plt.xlabel("Name")
plt.ylabel("Marks")
plt.title("Line Plot")
plt.show()

#BAR PLOT
plt.bar(df["Name"], df["Marks"])
plt.xlabel("Name")
plt.ylabel("Marks")
plt.title("Bar Plot")
plt.show()

#SCATTER PLOT
plt.scatter(df["Age"], df["Marks"])
plt.xlabel("Age")
plt.ylabel("Marks")
plt.title("Scatter Plot")
plt.show()

#HEATMAP
plt.figure(figsize=(6, 4))
sns.heatmap(df.select_dtypes("number").corr(),
            annot=True, cmap="coolwarm")
plt.title("Correlation Heatmap")
plt.show()

