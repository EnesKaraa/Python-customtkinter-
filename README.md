# Python-customtkinter-
made in the beginning  applications are very suitable for development.

import customtkinter
from time import strftime

customtkinter.set_appearance_mode("dark")
customtkinter.set_default_color_theme("dark-blue")

root = customtkinter.CTk()
root.title("Saat")

#text_color = violet, grey, black, silver, yellow ...
#font = Times, Helvetica ...
label = customtkinter.CTkLabel(root, text='%d.%h.%y - %H:%M:%S %p', text_color="beige", font=('ds-digital', 35))

def Clock():
    vakit = strftime('%d.%h.%y - %H:%M:%S %p')
    label.configure(text = vakit)
    label.after(1000, Clock)

label.pack(anchor = 'center')
Clock()

root.mainloop()
