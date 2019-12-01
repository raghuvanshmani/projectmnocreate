# projectmnocreate
from tkinter import *
import pymongo
root =Tk()
def create():
    uri = "mongodb://127.0.0.1:27017"
    connection = pymongo.MongoClient(uri)
    database = connection['Ragistration']
    collection = database['student']
    data = {"age":23}
    collection.insert_one(data)
def insert():
    uri = "mongodb://127.0.0.1:27017"
    connection = pymongo.MongoClient(uri)
    database = connection['Ragistration']
    collection = database['student']
    data = [
        {
            
        }
    ]
    collection.insert_one(data)


cr = Button(root,text="create",font=10,activebackground="yellow",
activeforeground="red",command=create)
cr.grid(row=7,column=0)
ins = Button(root,text="insert",font=10,activebackground="yellow",
activeforeground="red",command=insert)
ins.grid(row=7,column=2)

root.title("Ragitrationform")
name = Label(root ,text="Name",bg="white",font = 20,bd=4,fg="green")
name.grid(row = 0,column= 0)
namee=Entry(root,font=10,bg="white")
namee.grid(row=0,column=3)
addr = Label(root ,text="Address",bg="white",font = 20,bd=4,fg="green")
addr.grid(row = 1,column= 0)
addre = Entry(root,font=20,bg="white")
addre.grid(row=1,column=3)
quali = Label(root ,text="Qualification",bg="white",font = 20,bd=4,fg="red")
quali.grid(row = 2,column= 0)
qualie = Entry(root,font=20,bg="white")
qualie.grid(row=2,column=3)
number = Label(root ,text="Mobile Number",bg="white",font = 20,bd=4,fg="red")
number.grid(row = 3,column= 0)
numbere = Entry(root,font=20,bg="white")
numbere.grid(row=3,column=3)
gender = Label(root ,text="gender",bg="white",font = 20,bd=4,fg="red")
gender.grid(row = 4,column= 0)
gendere = Entry(root,font=20,bg="white")
gendere.grid(row=4,column=3)
root.geometry('600x600')
root.mainloop()
