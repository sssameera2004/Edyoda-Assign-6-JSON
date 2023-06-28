import json
class Employee:
    def __init__(self,name,dob,height,city,state):
        self.name = name
        self.dob = dob
        self.height = height
        self.city = city
        self.state = state
        
# with open(r"C:\Users\Hp\OneDrive\Desktop\Edyoda Practice\Edyoda Python Assignment 6\employee.json") as file:
#     data = json.load(file)
file = open(r"C:\Users\Hp\OneDrive\Desktop\Edyoda Practice\Edyoda Python Assignment 6\employee.json")
data = json.load(file)
employees = []
for i in data["employees"]:
    name = i["name"]
    dob = i["DOB"]
    height = i["Height"]
    city = i["city"]
    state = i["state"]

    employee = Employee(name,dob,height,city,state)
    employees.append(employee)

for i in employees:
    print("Name : ",i.name)
    print("DOB : ",i.dob)
    print("Height : ",i.height)
    print("City : ",i.city)
    print("State : ",i.state)
    print()


EMPLOYEE JSON FILE

{"employees" : [{"name": "Ram","DOB":"01/01/1997","Height":"5.8","city":"Noida","state":"Uttar Pradesh"},
{"name": "Raj","DOB":"10/05/1996","Height":"5.1","city":"Bhatinda","state":"Punjab"},
{"name": "Rahul","DOB":"12/01/1998","Height":"6.2","city":"Gurgaon","state":"Haryana"},
{"name": "Rohan","DOB":"01/04/1995","Height":"5.9","city":"Pune","state":"Maharashtra"},
{"name": "Rehan","DOB":"11/01/1999","Height":"6.0","city":"Shimla","state":"Himachal Pradesh"}]}

OUTPUT IN VSCODE
Name :  Ram
DOB :  01/01/1997     
Height :  5.8
City :  Noida
State :  Uttar Pradesh

Name :  Raj
DOB :  10/05/1996     
Height :  5.1
City :  Bhatinda      
State :  Punjab       

Name :  Rahul
DOB :  12/01/1998     
Height :  6.2
City :  Gurgaon
State :  Haryana

Name :  Rohan
DOB :  01/04/1995
Height :  5.9
City :  Pune
State :  Maharashtra

Name :  Rehan
DOB :  11/01/1999
Height :  6.0
City :  Shimla
State :  Himachal Pradesh

PS C:\Users\Hp\OneDrive\Desktop\Edyoda Practice>
