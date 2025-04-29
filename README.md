# 🎲DICE -with-graphics-interface-by-python-#

import tkinter as tk
import random

root = tk.Tk()
root.title("Dice Roller")
root.geometry("300x200")

dice_label = tk.Label(root, text="\u2680", font=("Helvetica", 100))
dice_label.pack(pady=20)

def roll_dice():
    dice_faces = ['\u2680', '\u2681', '\u2682', '\u2683', '\u2684', '\u2685']
    dice_label.config(text=random.choice(dice_faces))

roll_button = tk.Button(root, text="Roll Dice", command=roll_dice, font=("Helvetica", 14))
roll_button.pack()

root.mainloop()
