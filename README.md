# Python-customtkinter-
Small applications that I have made at the beginner level with custom tkinter. These applications can be modified and brought to intermediate or higher levels.
With CustomTkinter you can create modern looking user interfaces in python with tkinter. CustomTkinter is a tkinter extension which provides extra ui-elements like the CTkButton, which can be used like a normal tkinter.Button, but can be customized with a border and round edges.
To use CustomTkinter, just place the /customtkinter folder from this repository next to your program, and then you can do import customtkinter.
If you dont specify any colors, customtkinter uses the standard blue color in the light theme. You can change the color theme to dark by calling customtkinter.set_appearance_mode("Dark"). If you specify custom colors for CustomTkinter elements, the you can either use a tuple in the form: (light_color, dark_color). Or you can set a single color which will be used in light and dark theme.
It's also possible to put an image on a CTkButton. You just have to pass a PhotoImage object to the CTkButton with the argument image. You can find an example program ( /simple_test_images.py ), where I created two buttons with a bell and a settings image on them:

CTkButton
Examle Code:

def button_event():
    print("button pressed")

button = customtkinter.CTkButton(master=root_tk,
                                 text="CTkButton",
                                 command=button_event,
                                 width=120,
                                 height=32,
                                 border_width=0,
                                 corner_radius=8)
button.place(relx=0.5, rely=0.5, anchor=tkinter.CENTER)
Show all arguments:

CTkLabel
Example Code:

label = customtkinter.CTkLabel(master=root_tk,
                               text="CTkLabel",
                               width=120,
                               height=25,
                               corner_radius=8)
label.place(relx=0.5, rely=0.5, anchor=tkinter.CENTER)
Show all arguments:

CTkEntry
Example Code:

entry = customtkinter.CTkEntry(master=root_tk,
                               width=120,
                               height=25,
                               corner_radius=10)
entry.place(relx=0.5, rely=0.5, anchor=tkinter.CENTER)

text = entry.get()
Show all arguments:

CTkSlider
Example Code:

def slider_event(value):
    print(value)

slider = customtkinter.CTkSlider(master=root_tk,
                                 width=160,
                                 height=16,
                                 border_width=5.5,
                                 command=slider_event)
slider.place(relx=0.5, rely=0.5, anchor=tkinter.CENTER)
Show all arguments:

CTkProgressBar
Example Code:

progressbar = customtkinter.CTkProgressBar(master=root_tk,
                                           width=160,
                                           height=20,
                                           border_width=5)
progressbar.place(relx=0.5, rely=0.5, anchor=tkinter.CENTER)

progressbar.set(value)
Show all arguments:

CTkFrame
Example Code:

frame = customtkinter.CTkFrame(master=root_tk,
                               width=200,
                               height=200,
                               corner_radius=10)
frame.place(relx=0.5, rely=0.5, anchor=tkinter.CENTER)
