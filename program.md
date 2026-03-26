
Program :

import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
from faker import Faker

fake=Faker()

data={"Student_ID":np.random.randint(0,10,250),
"Name":[fake.name() for _ in range(250)],
"Gender":np.random.choice(["Male","Female"],250),
"Department":np.random.choice(["CSE","IT","ECE"],250),
"Year":np.random.choice([1,2,3,4],250),
"Maths":np.random.randint(40,100,250),
"Science":np.random.randint(40,100,250),
"English":np.random.randint(40,100,250),
"Attendance":np.random.randint(50,100,250),
"Internal_Marks":np.random.randint(0,25,250),
"External_Marks":np.random.randint(25,75,250)}

df=pd.DataFrame(data)

print(df.head())

df["Total"]=df["Internal_Marks"]+df["External_Marks"]
df["Average"]=df["Total"]/2

def grade(marks):
    if marks>=90:return"A"
    elif marks>=75:return"B"
    elif marks>=50:return"C"
    else:return"Fail"

df["Grade"]=df["Average"].apply(grade)

print("Mean:",df["Average"].mean())
print("Median:",df["Average"].median())
print("Mode:",df["Average"].mode()[0])
print("Standard Deviation:",df["Average"].std())

top_students=df[df["Average"]>=90]
fail_students=df[df["Grade"]=="Fail"]

print(top_students)
print(fail_students)

print(df.groupby("Department")["Average"].mean())
print(df.groupby("Gender")["Average"].mean())
print(df.groupby("Year")["Average"].mean())

print(df[["Attendance","Average"]].corr())

df.groupby("Department")["Average"].mean().plot(kind='bar')
plt.show()

df["Gender"].value_counts().plot(kind='bar')
plt.show()

plt.hist(df["Average"])
plt.show()
