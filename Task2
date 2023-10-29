#Codsoft project-2
import tkinter as tk
# Calculation Fucntion
def calculate(operation):
    num1 = float(entry_num1.get())
    num2 = float(entry_num2.get())

    if operation == "+":
        result.set(f"Result: {num1 + num2:.2f}")
    elif operation == "-":
        result.set(f"Result: {num1 - num2:.2f}")
    elif operation == "*":
        result.set(f"Result: {num1 * num2:.2f}")
    elif operation == "/":
        if num2 == 0:
            result.set("Error: Division by zero")
        else:
            result.set(f"Result: {num1 / num2:.2f}")
#Clear function
def clear_entries():
    entry_num1.delete(0, tk.END)
    entry_num2.delete(0, tk.END)
    result.set("")
# Main window
root = tk.Tk()
root.title("Calculator")
root.geometry("300x300")
root.configure(bg="purple")
# Entry fields for user input
label_num1 = tk.Label(root, text="Enter a number:")
label_num1.pack()
entry_num1 = tk.Entry(root)
entry_num1.pack()

label_num2 = tk.Label(root, text="Enter another number:")
label_num2.pack()
entry_num2 = tk.Entry(root)
entry_num2.pack()
#Frame for the operation buttons
operation_frame = tk.Frame(root,bg="green")
operation_frame.pack()
#Buttons for operations
add_button = tk.Button(operation_frame, text="+", command=lambda: calculate("+"))
subtract_button = tk.Button(operation_frame, text="-", command=lambda: calculate("-"))
multiply_button = tk.Button(operation_frame, text="", command=lambda: calculate("*"))
divide_button = tk.Button(operation_frame, text="/", command=lambda: calculate("/"))

add_button.pack(side="left",padx=5,pady=5)
subtract_button.pack(side="left",padx=5,pady=5)
multiply_button.pack(side="left",padx=7,pady=7)
divide_button.pack(side="left",padx=5,pady=5)
#Clear Button
clear_button = tk.Button(root,text="Clear",command=clear_entries)
clear_button.pack()
#Label to display the result
result = tk.StringVar()
result_label = tk.Label(root, textvariable=result, font=("Helvetica", 14),bg="yellow")
result_label.pack()
root.mainloop()
