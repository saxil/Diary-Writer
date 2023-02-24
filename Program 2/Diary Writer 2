from tkinter import *
from tkinter import messagebox
from datetime import date
today=date.today()
##print(today)

root=Tk()
root.geometry("300x200")
root.title("Diary Writer")

Diary_Label=Label(root,text=f"It's an Diary writer for you all\nso use it that way!!,\nToday\'s  date is :{today}").pack()



Diary_format="Dear Diary,\n"
DiaryEntry=Entry(root,width=20,relief=FLAT)
DiaryEntry.insert(0,"Write your text:")
DiaryEntry.pack()

Diary_Info_Writer=Label(root,text="You can remove \'Write your text:\' and write your things there",relief=FLAT).pack()

def Save():
    answer = messagebox.askyesno(title='save',
                    message='Are you sure that you want to save?')
    if answer:
            with open(f"diary_{today}.txt","w+") as Diary:
                Diary_Mat=DiaryEntry.get()
                Diary.write(f"Today {today}\n")
                if "Write your text:" in Diary_Mat:
                    Diary_Rewrite=messagebox.showinfo("Re-write?","You don\'t  wanna write anything?\nIf you want to you can write it now!!")
                else:
                    Diary.write(Diary_format)
                    Diary.write(Diary_Mat)
                Diary.close()

Diary_Save=Button(root,text="Save now",command=Save,relief= FLAT,cursor="arrow").pack()

def Destroy():
    Answer=messagebox.askyesno(title="Diary Writer",message='are you sure about ending  the program?')
    if Answer:
        root.destroy()
Diary_End=Button(root,text="Finish?",command=Destroy,relief=FLAT).pack()

root.mainloop()
