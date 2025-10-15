import tkinter as tk
import random

choices = ["Rock", "Paper", "Scissors"]
icons = {"Rock": "✊", "Paper": "✋", "Scissors": "✌️"}

def play(user_choice, user_label, comp_label, result_label):
    computer_choice = random.choice(choices)

    user_label.config(text=icons[user_choice], font=("Arial", 40))
    comp_label.config(text=icons[computer_choice], font=("Arial", 40))

    if user_choice == computer_choice:
        result = "It's a Tie!"
    elif (user_choice == "Rock" and computer_choice == "Scissors") or \
         (user_choice == "Paper" and computer_choice == "Rock") or \
         (user_choice == "Scissors" and computer_choice == "Paper"):
        result = "You Win!"
    else:
        result = "You Lose!"

    result_label.config(text=result, font=("Arial", 16, "bold"), fg="blue")

def game_window(start_screen):
    start_screen.destroy()

    game_root = tk.Tk()
    game_root.title("Rock Paper Scissors Game 🎮")
    game_root.geometry("500x500")

    tk.Label(game_root, text="Rock ✊ Paper ✋ Scissors ✌️", font=("Arial", 14)).pack(pady=10)

    frame = tk.Frame(game_root)
    frame.pack(pady=20)

    user_label = tk.Label(frame, text="❔", font=("Arial", 40))
    user_label.grid(row=0, column=0, padx=40)

    vs_label = tk.Label(frame, text="VS", font=("Arial", 20))
    vs_label.grid(row=0, column=1)

    comp_label = tk.Label(frame, text="❔", font=("Arial", 40))
    comp_label.grid(row=0, column=2, padx=40)

    result_label = tk.Label(game_root, text="", font=("Arial", 14))
    result_label.pack(pady=20)

    tk.Button(game_root, text="Rock ✊", width=15, height=2,
              command=lambda: play("Rock", user_label, comp_label, result_label)).pack(pady=5)
    tk.Button(game_root, text="Paper ✋", width=15, height=2,
              command=lambda: play("Paper", user_label, comp_label, result_label)).pack(pady=5)
    tk.Button(game_root, text="Scissors ✌️", width=15, height=2,
              command=lambda: play("Scissors", user_label, comp_label, result_label)).pack(pady=5)

    game_root.mainloop()

def launch_screen():
    start_screen = tk.Tk()
    start_screen.title("Rock Paper Scissors - Start")
    start_screen.geometry("300x200")

    tk.Label(start_screen, text="Welcome to Rock Paper Scissors 🎮", font=("Arial", 12)).pack(pady=20)
    tk.Button(start_screen, text="Play Game", width=20, height=2, command=lambda: game_window(start_screen)).pack(pady=10)
    tk.Button(start_screen, text="Quit", width=20, height=2, command=start_screen.destroy).pack()

    start_screen.mainloop()

launch_screen()
