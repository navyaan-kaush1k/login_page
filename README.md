# login_page


from tkinter import*
from PIL import Image, ImageTk
from tkinter import messagebox
from tkinter import ttk
from tkcalendar import DateEntry

root=Tk()
root.geometry("650x400")
root.configure(bg="white")
root.maxsize(width="750", height="1000")
root.minsize(width="750",height="1000")
root.title("hellish.jpg")

def sign_in():
    USERNAME= e1.get()
    PASSWORD=e.get()

    if  e1.get()=="admin123" and e.get()=="123456789":
        messagebox.showinfo("loggedin","you are successfully logged in")

    else:
        messagebox.showinfo("loggedin","unsuccessfull in logging you in")

img= Image.open("hellish.jpg")
render=ImageTk.PhotoImage(img)
lbl_1=Label(image=render).grid(row=0,column=0)


img1= Image.open("welcome.png")
render1=ImageTk.PhotoImage(img1)

def forgotten():
    top1=Toplevel(root,bg="black")
    top1.geometry("650x400")
    top1.configure(bg="")
    top1.maxsize(width="750", height="1000")
    top1.minsize(width="750",height="1000")
    top1.title("Forgotten Your Password!")

    imga=Image.open("hellish.jpg")
    rende=ImageTk.PhotoImage(imga)


    
    Label(top1, image=rende, bg="white", fg="red",padx=10,pady=10,border=5, borderwidth=5).place(x=0, y=0)
    me=LabelFrame(top1,text="Forget Your Password",fg='white', bg="red",font=("new times roman",8,("bold","italic")), labelanchor=NW, width=385, height=130, border=10, borderwidth=15).place(x=215, y=275)

    me2=Entry(top1, text="Username", bg="white", fg="black", border=5, borderwidth=10,cursor="", width=35).place(x=350,y=291)
    me3=Entry(top1, text="Email Address", fg="black", bg="white", border=5, borderwidth=10,cursor="", width=35).place(x=350,y=341)


    Label(top1,text="Username" , bg="white", fg="red",border=5, font=("new times roman",8,("bold","italic")),borderwidth=5).place(x=232, y=291)
    Label(top1,text="Email Address" , bg="white", fg="red",border=5, font=("new times roman",8,("bold","italic")),borderwidth=5).place(x=232, y=341)
    
    Frame(top1, background="black",border=5, borderwidth=10).place(x=350,y=430)
    Button(top1, text=("Submit"),pady=6, fg="white",font=("new times roman",8,("bold","italic")), background="black",width=50, border=5, borderwidth=10).place(x=220, y=440)

    top1.mainloop()


def sign_up():
    top=Toplevel(root,bg="black")
    top.geometry("650x400")
    top.configure(bg="black")
    top.maxsize(width="750", height="1000")
    top.minsize(width="750",height="1000")
    top.title("SIGH UP WINDOW")


    Label(top, image=render1, bg="white", fg="red",padx=10,pady=10,border=5, borderwidth=5).place(x=220, y=20)

    imagge=Image.open("hellish.jpg")
    ima=ImageTk.PhotoImage(imagge)


    me=LabelFrame(top,text="SIGN UP",fg='white', bg="black",font=("new times roman",8,("bold","italic")), labelanchor=NW, width=385, height=450, border=10, borderwidth=15).place(x=215, y=175)
    me0=Entry(top, text="E.mail", bg="white", fg="black", border=5, borderwidth=10,cursor="" ,width=35)
    me0.place(x=350,y=182)
    me1=DateEntry(top,width=35)
    me1.place(x=350,y=240)
    me2=Entry(top, text="confirm your password", bg="white", fg="black", border=5, borderwidth=10,cursor="", width=35)
    me2.place(x=350,y=282)
    me3=Entry(top, text="password", fg="black", bg="white", border=5, borderwidth=10,cursor="", width=35)
    me3.place(x=350,y=332)
    me4=Entry(top, text="usrname", fg="black", bg="white", border=5, borderwidth=10,cursor="", width=35)
    me4.place(x=350,y=382)
    me5=Entry(top, text="number", fg="black", bg="white", border=5, borderwidth=10,cursor="", width=35)
    me5.place(x=350,y=432)
    me6=Entry(top, text="name", fg="black", bg="white", border=5, borderwidth=10,cursor="", width=35)
    me6.place(x=350,y=482)

    Label(top, text='Name', bg="white", fg="red",border=5,font=("new times roman",8,("bold","italic")), borderwidth=5).place(x=232, y=190)
    Label(top,text="Date of Birth" , bg="white", fg="red",border=5, font=("new times roman",8,("bold","italic")),borderwidth=5).place(x=232, y=240)
    Label(top, text='Phone No.', bg="white", fg="red",border=5,font=("new times roman",8,("bold","italic")), borderwidth=5).place(x=232, y=290)
    Label(top,text="Email Address" , bg="white", fg="red",border=5, font=("new times roman",8,("bold","italic")),borderwidth=5).place(x=232, y=340)
    Label(top,text="Username" , bg="white", fg="red",border=5, font=("new times roman",8,("bold","italic")),borderwidth=5).place(x=232, y=390)
    Label(top, text="Password", bg="white", fg="red",border=5,font=("new times roman",8,("bold","italic")), borderwidth=5).place(x=232, y=440)
    Label(top, text="Confirm Password", bg="white", fg="red",border=5,font=("new times roman",8,("bold","italic")), borderwidth=5).place(x=232, y=490)

    c1=Checkbutton(top, text=" Yes, I Accept The Terms And Conditions", bg="black",fg="red").place(x=280,y=540)
    c2=Checkbutton(top, text=" No, I  Don't Accept The Terms And Conditions", bg="black",fg="red").place(x=280,y=580)

    
    top.mainloop()
    

heading=Label(root, image=render1, bg="white", fg="red",padx=10, pady=10,border=5, borderwidth=5).place(x=220, y=50)
button_frame=Frame(root, bg="black",  width=375, height=260, border=10, borderwidth=15).place(x=220, y=200)


e1=Entry(root, text="", bg="red", fg="white", border=5, borderwidth=10,cursor="", width=50)
e1.place(x=245,y=240)
e1.insert(0,"Username:")

e=Entry(root, bg="red", fg="white", border=5, borderwidth=10,cursor="", width=50)
e.place(x=245,y=290)

e.insert(0, "Password:")

Button(button_frame, text="SIGN IN", fg="white",padx=0,pady=8,font=("new times roman",8,("bold","italic")),command=lambda:sign_in(),background="black", border=15,width=50, borderwidth=10).place(x=220, y=350)

Button(button_frame, text="FORGET PASSWORD?",padx=0,pady=8,command=lambda:forgotten(), fg="white",font=("new times roman",8,("bold","italic")), background="black", border=10, width=50).place(x=220, y=400)

checkbutton_frame=Frame(root, bg="black", width=375, height=140, border=10, borderwidth=15).place(x=220, y=462)

Button(checkbutton_frame, text=("I don't have an account! SIGN UP!"),padx=0,pady=8, fg="white",font=("new times roman",8,("bold","italic")), background="black", command=lambda:sign_up(),width=50, border=15, borderwidth=10).place(x=220, y=475)

def display():
    pass

check1=Checkbutton(checkbutton_frame,onvalue=1,offvalue=0,command=display(), text=" Yes, I Accept The Terms And Conditions", bg="black",fg="white").place(x=280,y=542)
check2=Checkbutton(checkbutton_frame,onvalue=0,command=display(), text=" No, I don't Accept Terms And Conditions", bg='black', fg="white").place(x=280,y=567)

root.mainloop()
