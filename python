import os
import platform
import mysql.connector
import datetime
global z
mydb = mysql.connector.connect(user='root',
password='Twinkle11',host='localhost',database='hotel
')
mycursor=mydb.cursor()
def registercust():
L=[]
name=input("enter name:")
L.append(name)
addr=input("enter address:")
L.append(addr)
indate=input("enter check in date:")
L.append(indate)
outdate=input("enter check out date:")
L.append(outdate)
cust=(L)
sql="insert into custdata values(%s,%s,%s,%s)"
mycursor.execute(sql,cust)
mydb.commit()
def roomrent():
global s
print ("We have the following rooms for you:-")
print ("1. type A---->rs 1000 PN\-")
print ("2. type B---->rs 2000 PN\-")
print ("3. type C---->rs 3000 PN\-")
print ("4. type D---->rs 4000 PN\-")
x=int(input("Enter Your Choice Please->"))
n=int(input("For How Many Nights Did You Stay:"))
if(x==1):
print ("you have opted room type A")
s=1000*n
elif (x==2):
print ("you have opted room type B")
s=2000*n

elif (x==3):
print ("you have opted room type C")
s=3000*n
elif (x==4):
print ("you have opted room type D")
s=4000*n
else:
print ("please choose a room")
print ("your room rent is =",s,"\n")

def orderitem():
global b
print("Do you want to see menu available : ")
ch=int(input("Enter 1 for yes :"))
if ch==1:
sql="select * from restaurent"
mycursor.execute(sql)
rows=mycursor.fetchall()
for x in rows:
print(x)
d=int(input("enter your choice:"))
if(d==1):
print("you have ordered tea")
a=int(input("enter quantity"))
b=10*a
print("your amount for tea is :",b,"\n")
elif (d==2):
print("you have ordered coffee")
a=int(input("enter quantity"))
b=10*a
print("your amount for coffee is :",b,"\n")
elif(d==3):
print("you have ordered colddrink")
a=int(input("enter quantity"))
b=20*a
print("your amount for colddrink is :",b,"\n")
elif(d==4):
print("you have ordered samosa")
a=int(input("enter quantity"))
b=10*a
print("your amount fopr samosa is :",b,"\n")
elif(d==5):

print("you have ordered sandwich")
a=int(input("enter quantity"))
b=50*a
print("your amount fopr sandwich is :",b,"\n")
elif(d==6):
print("you have ordered dhokla")
a=int(input("enter quantity"))
b=30*a
print("your amount for dhokla is :",b,"\n")
elif(d==7):
print("you have ordered kachori")
a=int(input("enter quantity"))
b=10*a
print("your amount for kachori is :",b,"\n")
elif(d==8):
print("you have ordered milk")
a=int(input("enter quantity"))
b=20*a
print("your amount for kachori is :",b,"\n")
elif(d==9):
print("you have ordered noodles")
a=int(input("enter quantity"))
b=50*a
print("your amount for noodles is :",b,"\n")
elif(d==10):
print("you have ordered pasta")
a=int(input("enter quantity"))
b=50*a
print("your amount for pasta is :",b,"\n")
else:
print("please enter your choice from the menu")
def laundrybill():
global z
print("Do you want to see rate for laundry")
ch=int(input("enter 1 for yes:"))
if ch==1:
sql="select * from laundary"
mycursor.execute(sql)
rows=mycursor.fetchall()
for x in rows:
print(x)
y=int(input("Enter Your Choice->"))
if(y==1):

print('you can carry your pant to the laundry
room')
z=10
elif(y==2):
print('you can carry your shirt to the laundry
room')
z=10
elif(y==3):
print('you can carry your suit to the laundry
room')
z=10
elif(y==4):
print('you can carry your pant to the laundry
room')
z=10
else:
print("Please enter a correct choice")
print("your laundry bill:",z,"\n")
return z
def lb():
print(z)
def res():
print(b)
def ren():
print(s)
def viewbill():
a=input("enter customer name:")
print("customer name :",a,"\n")
print("laundry bill:")
lb()
print("restaurant bill:")
res()
print("room bill:")
ren()

def Menuset():
print("enter 1 : To enter customer data")
print("enter 2 : for calculating room bill")
print("enter 3 : for restaurant bill")
print("enter 4 : for laundry bill")
print("enter 5 : for complete bill")
print("enter 6 : for exit:")

userinput=int(input("enter your choice"))
if(userinput==1):
registercust()
elif(userinput==2):
roomrent()
elif(userinput==3):
orderitem()
elif(userinput==4):
laundrybill()
elif(userinput==5):
viewbill()
elif(userinput==6):
quit()
else:
print("enter correct choice")
Menuset()
def runagain():
runagn=input("\n want to run again y/n:")
while(runagn.lower()=='y'):
if(platform.system()=="windows"):
print(os.system('cls'))
else:
print(os.system('clear'))
Menuset()
runagn=input("\n want to run again y/n:")
runagain()
