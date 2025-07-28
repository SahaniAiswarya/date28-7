#normal method // instance method
class student:
    def __init__(s,name,marks):
        s.name=name
        s.marks=marks
    def display(self):
        print(f"student name:{s.name}")
        print(f"student marks:{s.marks}")
name=str(input("enter the name:"))
marks=int(input("enter the marks:"))
s=student(name,marks)
s.display()


#classmethod
class student:
    def __init__(self,name,marks):
        self.name=name
        self.marks=marks
    @classmethod
    def input(cls):
        name=str(input("enter the name:"))
        marks=int(input("enter the marks:"))
        return cls(name,marks)
    def display(self):
        print(f"student name:{s.name}")
        print(f"student marks:{s.marks}")
s=student.input()
s.display()



class product:
    tax_rate=0.18   #choice
    def __init__(self,name,price):
        self.name=name
        self.price=price
    def finalprice(self):
        total=self.price*(1+product.tax_rate)
        print(f"final price of {self.name} is Rs.{total:.2f}")
    @classmethod
    def settax(cls,rate):
        cls.tax_rate=rate/100
name=str(input("enter the product name:"))
price=float(input("enter the base price:"))
rate=int(input("enter tax_rate in %:"))
product.settax(rate)
item=product(name,price)
item.finalprice()



#basic math operation using@classmethod
class calculator:
    def __init__(s,a,b,):
        s.a=a
        s.b=b
    @classmethod
    def input(cls):
        a=int(input("enter a value:"))
        b=int(input("enter b value:"))
        return cls(a,b)
    def add(s):
        return s.a+s.b
c=calculator.input()
print("addition result:",c.add())



class calculator:
    def __init__(s,a,b,):
        s.a=a
        s.b=b
    @classmethod
    def input(cls):
        a=int(input("enter a value:"))
        b=int(input("enter b value:"))
        return cls(a,b)
    def op(s):
        print("Addition result:",s.a+s.b)
        print("subtraction result:",s.a-s.b)
        print("multiplication result:",s.a*s.b)
        print("division result:",s.a/s.b)
c=calculator.input()
c.op()



#static method @staticmethod
class student:
    gender="Female"
    def __init__(s,name):
        s.name=name
    def display(s):
        print(f"name:{s.name}")
    @classmethod
    def getname(cls):
        return cls.gender
    @staticmethod
    def resident(type_of_resident):
        if type_of_resident.lower()=='indian':
            return "the person is indian"
        else:
            return "non-resident indian"
name=str(input("enter your name:"))
type=input("enter resident or non-resident:")
s=student(name)
s.display()
print("student gender:",student.getname())
print(s.resident(type))   



class op:
    @staticmethod
    def add(a,b):
        return a+b
x=int(input("enter x value:"))
y=int(input("enter y value:"))
print("sum:",op.add(x,y))






