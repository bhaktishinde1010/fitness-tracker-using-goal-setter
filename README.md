# fitness-tracker-using-goal-setter
import tkinter as tk
from tkinter import messagebox

def open_registration_window():
    registration_window = tk.Toplevel(root)
    registration_window.title("User Registration")
    registration_window.geometry("300x300")

    # Create labels and entries for user registration
    tk.Label(registration_window, text="UserID:").grid(row=0, column=0, padx=5, pady=5)
    user_id_entry = tk.Entry(registration_window)
    user_id_entry.grid(row=0, column=1, padx=5, pady=5)

    tk.Label(registration_window, text="Name:").grid(row=1, column=0, padx=5, pady=5)
    name_entry = tk.Entry(registration_window)
    name_entry.grid(row=1, column=1, padx=5, pady=5)

    tk.Label(registration_window, text="Age:").grid(row=2, column=0, padx=5, pady=5)
    age_entry = tk.Entry(registration_window)
    age_entry.grid(row=2, column=1, padx=5, pady=5)

    tk.Label(registration_window, text="Gender:").grid(row=3, column=0, padx=5, pady=5)
    gender_entry = tk.Entry(registration_window)
    gender_entry.grid(row=3, column=1, padx=5, pady=5)

    tk.Label(registration_window, text="Height:").grid(row=4, column=0, padx=5, pady=5)
    height_entry = tk.Entry(registration_window)
    height_entry.grid(row=4, column=1, padx=5, pady=5)

    tk.Label(registration_window, text="Weight:").grid(row=5, column=0, padx=5, pady=5)
    weight_entry = tk.Entry(registration_window)
    weight_entry.grid(row=5, column=1, padx=5, pady=5)

    tk.Label(registration_window, text="Email:").grid(row=6, column=0, padx=5, pady=5)
    email_entry = tk.Entry(registration_window)
    email_entry.grid(row=6, column=1, padx=5, pady=5)

    # Button to submit registration
    submit_button = tk.Button(registration_window, text="Submit Registration", command=lambda: register_user(registration_window))
    submit_button.grid(row=7, columnspan=2, padx=5, pady=5)

def register_user(window):
    # Perform registration tasks here
    # For demonstration purposes, let's assume the registration is successful
    messagebox.showinfo("Success", "User registered successfully!")
    window.destroy()

   # Function to open the weight gain recipe page
def open_weight_gain_recipes():
    weight_gain_recipes_window = tk.Toplevel(root)
    weight_gain_recipes_window.title("Weight Gain Recipes")
    
    # Sample weight gain recipes
    recipe1 = "1. Peanut Butter Banana Smoothie:\nIngredients:\n- 1 ripe banana\n- 2 tablespoons peanut butter\n- 1 cup whole milk\n- 1/2 cup Greek yogurt\n- 1 tablespoon honey (optional)\n\nInstructions:\n1. Combine all ingredients in a blender.\n2. Blend until smooth and creamy.\n3. Pour into a glass and enjoy!"

    recipe2 = "2. Avocado Toast with Eggs:\nIngredients:\n- 2 slices whole-grain bread\n- 1 ripe avocado\n- 2 eggs\n- Salt and pepper to taste\n\nInstructions:\n1. Toast the bread until golden brown.\n2. Mash the ripe avocado and spread it evenly on the toast.\n3. Cook eggs to your preference (fried, scrambled, poached).\n4. Place cooked eggs on top of the avocado toast.\n5. Season with salt and pepper."

    recipe3 = "3. Loaded Baked Potato:\nIngredients:\n- 1 large russet potato\n- 1/4 cup shredded cheddar cheese\n- 2 tablespoons sour cream\n- 2 slices cooked bacon, crumbled\n- Chopped chives for garnish\n\nInstructions:\n1. Preheat oven to 400°F (200°C).\n2. Pierce potato with a fork and bake for 45-60 minutes, until tender.\n3. Slice potato open and fluff the insides with a fork.\n4. Top with shredded cheddar cheese, sour cream, crumbled bacon, and chopped chives."

    # Create labels to display recipes
    tk.Label(weight_gain_recipes_window, text=recipe1, justify="left", padx=10, pady=10).pack(anchor="w")
    tk.Label(weight_gain_recipes_window, text=recipe2, justify="left", padx=10, pady=10).pack(anchor="w")
    tk.Label(weight_gain_recipes_window, text=recipe3, justify="left", padx=10, pady=10).pack(anchor="w")


# Function to open the weight loss recipe page
def open_weight_loss_recipes():
    weight_loss_recipes_window = tk.Toplevel(root)
    weight_loss_recipes_window.title("Weight Loss Recipes")
    
    # Sample weight loss recipes
    recipe1 = "1. Grilled Chicken Salad:\nIngredients:\n- Grilled chicken breast\n- Mixed greens\n- Cherry tomatoes\n- Cucumber\n- Bell peppers\n- Olive oil and vinegar dressing\n\nInstructions:\n1. Grill the chicken breast until cooked thoroughly.\n2. Chop the mixed greens, cherry tomatoes, cucumber, and bell peppers.\n3. Toss all ingredients together in a bowl.\n4. Drizzle olive oil and vinegar dressing over the salad."

    recipe2 = "2. Vegetable Stir-Fry:\nIngredients:\n- Mixed vegetables (broccoli, carrots, bell peppers, snap peas)\n- Tofu or lean protein of choice\n- Soy sauce\n- Garlic\n- Ginger\n- Brown rice\n\nInstructions:\n1. Cut tofu into cubes and marinate with soy sauce, garlic, and ginger.\n2. Stir-fry mixed vegetables in a pan until tender-crisp.\n3. Add marinated tofu and cook until heated through.\n4. Serve over cooked brown rice."

    recipe3 = "3. Quinoa and Black Bean Salad:\nIngredients:\n- Quinoa\n- Black beans\n- Corn\n- Red onion\n- Bell peppers\n- Cilantro\n- Lime juice\n- Olive oil\n- Salt and pepper\n\nInstructions:\n1. Cook quinoa according to package instructions.\n2. In a bowl, combine cooked quinoa, black beans, corn, diced red onion, diced bell peppers, and chopped cilantro.\n3. Drizzle with lime juice and olive oil.\n4. Season with salt and pepper to taste."

    # Create labels to display recipes
    tk.Label(weight_loss_recipes_window, text=recipe1, justify="left", padx=10, pady=10).pack(anchor="w")
    tk.Label(weight_loss_recipes_window, text=recipe2, justify="left", padx=10, pady=10).pack(anchor="w")
    tk.Label(weight_loss_recipes_window, text=recipe3, justify="left", padx=10, pady=10).pack(anchor="w")

    
    # Add labels and information about weight loss recipes here
def open_bmi_calculator():
    bmi_window = tk.Toplevel(root)
    bmi_window.title("BMI Calculator")
    bmi_window.geometry("300x200")

    # Create labels and entries for BMI calculation
    tk.Label(bmi_window, text="Enter Height (m):").grid(row=0, column=0, padx=5, pady=5)
    height_entry_bmi = tk.Entry(bmi_window)
    height_entry_bmi.grid(row=0, column=1, padx=5, pady=5)

    tk.Label(bmi_window, text="Enter Weight (kg):").grid(row=1, column=0, padx=5, pady=5)
    weight_entry_bmi = tk.Entry(bmi_window)
    weight_entry_bmi.grid(row=1, column=1, padx=5, pady=5)

    # Button to calculate BMI
    calculate_bmi_button = tk.Button(bmi_window, text="Calculate BMI", command=lambda: calculate_bmi(bmi_window, height_entry_bmi, weight_entry_bmi))
    calculate_bmi_button.grid(row=2, columnspan=2, padx=5, pady=5)

    # Label to display BMI result
    global bmi_label_bmi
    bmi_label_bmi = tk.Label(bmi_window, text="")
    bmi_label_bmi.grid(row=3, columnspan=2, padx=5, pady=5)

    # Label to display BMI category
    global category_label
    category_label = tk.Label(bmi_window, text="")
    category_label.grid(row=4, columnspan=2, padx=5, pady=5)

def calculate_bmi(window, height_entry, weight_entry):
    try:
        height = float(height_entry.get())
        weight = float(weight_entry.get())
        bmi = weight / (height ** 2)

        bmi_label_bmi.config(text=f"BMI: {bmi:.2f}")

        if bmi < 18.5 or bmi >= 25:
            open_weight_management_window(bmi)
        else:
            category_label.config(text="Category: Normal")
    except ValueError:
        error_label = tk.Label(window, text="Please enter valid height and weight values.")
        error_label.grid(row=3, columnspan=2, padx=5, pady=5)

def open_weight_management_window(bmi):
    weight_management_window = tk.Toplevel(root)
    weight_management_window.title("Weight Management")

    if bmi < 18.5:
        tk.Label(weight_management_window, text="You are underweight. Choose an option to gain weight:").pack(pady=10)
        tk.Button(weight_management_window, text="Weight Gain Plan", command=open_weight_gain_plan).pack(pady=5)
    else:
        tk.Label(weight_management_window, text="You are overweight. Choose an option to lose weight:").pack(pady=10)
        tk.Button(weight_management_window, text="Weight Loss Plan", command=open_weight_loss_plan).pack(pady=5)
 
 # Define global variables
steps_goal_entry = None
calories_goal_entry = None
minutes_goal_entry = None
water_goal_entry = None
sleep_goal_entry = None
steps_taken_entry = None
calories_burned_entry = None
minutes_active_entry = None
water_intake_entry = None
sleep_duration_entry = None

def open_weight_gain_plan():
    global steps_goal_entry, calories_goal_entry, minutes_goal_entry, water_goal_entry, sleep_goal_entry, steps_taken_entry, calories_burned_entry, minutes_active_entry, water_intake_entry, sleep_duration_entry
    
    weight_gain_window = tk.Toplevel(root)
    weight_gain_window.title("Weight Gain Plan")

    # Create labels and entries for user input
    tk.Label(weight_gain_window, text="Enter Daily Steps Goal:").grid(row=0, column=0, padx=5, pady=5)
    steps_goal_entry = tk.Entry(weight_gain_window)
    steps_goal_entry.grid(row=0, column=1, padx=5, pady=5)

    tk.Label(weight_gain_window, text="Enter Daily Calories Goal:").grid(row=1, column=0, padx=5, pady=5)
    calories_goal_entry = tk.Entry(weight_gain_window)
    calories_goal_entry.grid(row=1, column=1, padx=5, pady=5)

    tk.Label(weight_gain_window, text="Enter Daily Active Minutes Goal:").grid(row=2, column=0, padx=5, pady=5)
    minutes_goal_entry = tk.Entry(weight_gain_window)
    minutes_goal_entry.grid(row=2, column=1, padx=5, pady=5)

    tk.Label(weight_gain_window, text="Enter Daily Water Intake Goal (in liters):").grid(row=3, column=0, padx=5, pady=5)
    water_goal_entry = tk.Entry(weight_gain_window)
    water_goal_entry.grid(row=3, column=1, padx=5, pady=5)

    tk.Label(weight_gain_window, text="Enter Daily Sleep Duration Goal (in hours):").grid(row=4, column=0, padx=5, pady=5)
    sleep_goal_entry = tk.Entry(weight_gain_window)
    sleep_goal_entry.grid(row=4, column=1, padx=5, pady=5)

    tk.Label(weight_gain_window, text="Enter Steps Taken:").grid(row=5, column=0, padx=5, pady=5)
    steps_taken_entry = tk.Entry(weight_gain_window)
    steps_taken_entry.grid(row=5, column=1, padx=5, pady=5)

    tk.Label(weight_gain_window, text="Enter Calories Burned:").grid(row=6, column=0, padx=5, pady=5)
    calories_burned_entry = tk.Entry(weight_gain_window)
    calories_burned_entry.grid(row=6, column=1, padx=5, pady=5)

    tk.Label(weight_gain_window, text="Enter Minutes Active:").grid(row=7, column=0, padx=5, pady=5)
    minutes_active_entry = tk.Entry(weight_gain_window)
    minutes_active_entry.grid(row=7, column=1, padx=5, pady=5)

    tk.Label(weight_gain_window, text="Enter Water Intake (in liters):").grid(row=8, column=0, padx=5, pady=5)
    water_intake_entry = tk.Entry(weight_gain_window)
    water_intake_entry.grid(row=8, column=1, padx=5, pady=5)

    tk.Label(weight_gain_window, text="Enter Sleep Duration (in hours):").grid(row=9, column=0, padx=5, pady=5)
    sleep_duration_entry = tk.Entry(weight_gain_window)
    sleep_duration_entry.grid(row=9, column=1, padx=5, pady=5)

    # Create buttons for actions
    calculate_button = tk.Button(weight_gain_window, text="Calculate Progress", command=calculate_progress)
    calculate_button.grid(row=10, columnspan=2, padx=5, pady=5)

    clear_button = tk.Button(weight_gain_window, text="Clear Data", command=clear_data)
    clear_button.grid(row=11, columnspan=2, padx=5, pady=5)

    set_goals_button = tk.Button(weight_gain_window, text="Set Goals", command=set_goals)
    set_goals_button.grid(row=11, column=0, padx=5, pady=5)

    set_default_goals_button = tk.Button(weight_gain_window, text="Set Default Goals", command=set_default_goals)
    set_default_goals_button.grid(row=11, column=1, padx=5, pady=5)

    tk.Label(weight_gain_window, text="Weight Gain Exercises:").grid(row=12, column=0, columnspan=2, pady=10)
    tk.Label(weight_gain_window, text="1. Squats").grid(row=13, column=0, columnspan=2, pady=10)
    tk.Label(weight_gain_window, text="2. Deadlifts").grid(row=14, column=0, columnspan=2, pady=10)
    tk.Label(weight_gain_window, text="3. Bench Press").grid(row=15, column=0, columnspan=2, pady=10)

def open_weight_loss_plan():
    global steps_goal_entry, calories_goal_entry, minutes_goal_entry, water_goal_entry, sleep_goal_entry, steps_taken_entry, calories_burned_entry, minutes_active_entry, water_intake_entry, sleep_duration_entry
    
    weight_loss_window = tk.Toplevel(root)
    weight_loss_window.title("Weight Loss Plan")

    # Create labels and entries for user input
    tk.Label(weight_loss_window, text="Enter Daily Steps Goal:").grid(row=0, column=0, padx=5, pady=5)
    steps_goal_entry = tk.Entry(weight_loss_window)
    steps_goal_entry.grid(row=0, column=1, padx=5, pady=5)

    tk.Label(weight_loss_window, text="Enter Daily Calories Goal:").grid(row=1, column=0, padx=5, pady=5)
    calories_goal_entry = tk.Entry(weight_loss_window)
    calories_goal_entry.grid(row=1, column=1, padx=5, pady=5)

    tk.Label(weight_loss_window, text="Enter Daily Active Minutes Goal:").grid(row=2, column=0, padx=5, pady=5)
    minutes_goal_entry = tk.Entry(weight_loss_window)
    minutes_goal_entry.grid(row=2, column=1, padx=5, pady=5)

    tk.Label(weight_loss_window, text="Enter Daily Water Intake Goal (in liters):").grid(row=3, column=0, padx=5, pady=5)
    water_goal_entry = tk.Entry(weight_loss_window)
    water_goal_entry.grid(row=3, column=1, padx=5, pady=5)

    tk.Label(weight_loss_window, text="Enter Daily Sleep Duration Goal (in hours):").grid(row=4, column=0, padx=5, pady=5)
    sleep_goal_entry = tk.Entry(weight_loss_window)
    sleep_goal_entry.grid(row=4, column=1, padx=5, pady=5)

    tk.Label(weight_loss_window, text="Enter Steps Taken:").grid(row=5, column=0, padx=5, pady=5)
    steps_taken_entry = tk.Entry(weight_loss_window)
    steps_taken_entry.grid(row=5, column=1, padx=5, pady=5)

    tk.Label(weight_loss_window, text="Enter Calories Burned:").grid(row=6, column=0, padx=5, pady=5)
    calories_burned_entry = tk.Entry(weight_loss_window)
    calories_burned_entry.grid(row=6, column=1, padx=5, pady=5)

    tk.Label(weight_loss_window, text="Enter Minutes Active:").grid(row=7, column=0, padx=5, pady=5)
    minutes_active_entry = tk.Entry(weight_loss_window)
    minutes_active_entry.grid(row=7, column=1, padx=5, pady=5)

    tk.Label(weight_loss_window, text="Enter Water Intake (in liters):").grid(row=8, column=0, padx=5, pady=5)
    water_intake_entry = tk.Entry(weight_loss_window)
    water_intake_entry.grid(row=8, column=1, padx=5, pady=5)

    tk.Label(weight_loss_window, text="Enter Sleep Duration (in hours):").grid(row=9, column=0, padx=5, pady=5)
    sleep_duration_entry = tk.Entry(weight_loss_window)
    sleep_duration_entry.grid(row=9, column=1, padx=5, pady=5)

    # Create buttons for actions
    calculate_button = tk.Button(weight_loss_window, text="Calculate Progress", command=calculate_progress)
    calculate_button.grid(row=10, columnspan=2, padx=5, pady=5)

    clear_button = tk.Button(weight_loss_window, text="Clear Data", command=clear_data)
    clear_button.grid(row=11, columnspan=2, padx=5, pady=5)

    set_goals_button = tk.Button(weight_loss_window, text="Set Goals", command=set_goals)
    set_goals_button.grid(row=11, column=0, padx=5, pady=5)

    set_default_goals_button = tk.Button(weight_loss_window, text="Set Default Goals", command=set_default_goals)
    set_default_goals_button.grid(row=11, column=1, padx=5, pady=5)

    # Create labels for weight loss exercises using grid
    tk.Label(weight_loss_window, text="Weight Loss Exercises:").grid(row=12, column=0, columnspan=2, pady=10)
    tk.Label(weight_loss_window, text="1. Cardio (Running, Cycling)").grid(row=13, column=0, columnspan=2)
    tk.Label(weight_loss_window, text="2. HIIT Workouts").grid(row=14, column=0, columnspan=2)
    tk.Label(weight_loss_window, text="3. Circuit Training").grid(row=15, column=0, columnspan=2)

def calculate_progress():
    global steps_goal_entry, calories_goal_entry, minutes_goal_entry, water_goal_entry, sleep_goal_entry
    try:
        steps_goal = int(steps_goal_entry.get())
        calories_goal = int(calories_goal_entry.get())
        minutes_goal = int(minutes_goal_entry.get())
        water_goal = int(water_goal_entry.get())
        sleep_goal = int(sleep_goal_entry.get())

        steps_taken = int(steps_taken_entry.get())
        calories_burned = int(calories_burned_entry.get())
        minutes_active = int(minutes_active_entry.get())
        water_intake = int(water_intake_entry.get())
        sleep_duration = int(sleep_duration_entry.get())

        steps_progress = (steps_taken / steps_goal) * 100
        calories_progress = (calories_burned / calories_goal) * 100
        minutes_progress = (minutes_active / minutes_goal) * 100
        water_progress = (water_intake / water_goal) * 100
        sleep_progress = (sleep_duration / sleep_goal) * 100

        steps_message = get_motivational_message(steps_progress)
        calories_message = get_motivational_message(calories_progress)
        minutes_message = get_motivational_message(minutes_progress)
        water_message = get_motivational_message(water_progress)
        sleep_message = get_motivational_message(sleep_progress)

        messagebox.showinfo("Progress Report",
                            f"Steps Progress: {steps_progress:.2f}%\n{steps_message}\n\n"
                            f"Calories Progress: {calories_progress:.2f}%\n{calories_message}\n\n"
                            f"Minutes Active Progress: {minutes_progress:.2f}%\n{minutes_message}\n\n"
                            f"Water Intake Progress: {water_progress:.2f}%\n{water_message}\n\n"
                            f"Sleep Duration Progress: {sleep_progress:.2f}%\n{sleep_message}")

    except ValueError:
        messagebox.showerror("Error", "Please enter valid numerical values.")

def get_motivational_message(progress):
    if progress < 25:
        return "You've got this! Keep pushing forward."
    elif progress < 50:
        return "You're making progress! Keep up the good work."
    elif progress < 75:
        return "Great job! You're getting closer to your goal."
    elif progress < 100:
        return "Almost there! Stay focused and keep going."
    else:
        return "Congratulations! You've reached your goal. Time to set new ones!"

def clear_data():
    steps_goal_entry.delete(0, tk.END)
    calories_goal_entry.delete(0, tk.END)
    minutes_goal_entry.delete(0, tk.END)
    water_goal_entry.delete(0, tk.END)
    sleep_goal_entry.delete(0, tk.END)
    steps_taken_entry.delete(0, tk.END)
    calories_burned_entry.delete(0, tk.END)
    minutes_active_entry.delete(0, tk.END)
    water_intake_entry.delete(0, tk.END)
    sleep_duration_entry.delete(0, tk.END)

def set_goals():
    clear_data()
    set_default_goals()

def set_default_goals():
    steps_goal_entry.insert(0, "10000")
    calories_goal_entry.insert(0, "2000")
    minutes_goal_entry.insert(0, "30")
    water_goal_entry.insert(0, "8")
    sleep_goal_entry.insert(0, "8")

# Create the main window
root = tk.Tk()
root.title("Fitness Tracker and Goal Setter")
root.geometry("400x400")
root.configure(bg="#f0f0f0")

watermark_label = tk.Label(root, text="FITNESS TRACKER", fg="#4682B4", font=("Arial", 30, "bold italic"))
watermark_label.place(relx=0.5, rely=0.1, anchor="center")

# Button to open user registration window
registration_button = tk.Button(root, text="User Registration", command=open_registration_window)
registration_button.place(relx=0.5, rely=0.3, anchor="center")

# Button to open BMI calculator window
bmi_calculator_button = tk.Button(root, text="BMI Calculator", command=open_bmi_calculator)
bmi_calculator_button.place(relx=0.5, rely=0.4, anchor="center")

# Button to open weight gain recipe page
weight_gain_recipes_button = tk.Button(root, text="Weight Gain Recipes", command=open_weight_gain_recipes)
weight_gain_recipes_button.place(relx=0.5, rely=0.5, anchor="center")

# Button to open weight loss recipe page
weight_loss_recipes_button = tk.Button(root, text="Weight Loss Recipes", command=open_weight_loss_recipes)
weight_loss_recipes_button.place(relx=0.5, rely=0.6, anchor="center")
# Run the main event loop
root.mainloop()
