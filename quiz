import random

def generate_question():
    """Generate a random math question."""
    operations = ['+', '-', '*', '/']
    num1 = random.randint(1, 100)
    num2 = random.randint(1, 100)
    operation = random.choice(operations)

    # Ensure division results in a whole number
    if operation == '/':
        num1 = num1 * num2

    question = f"{num1} {operation} {num2}"
    answer = eval(question)  # Use eval for simple operations (safe here as inputs are controlled)
    return question, answer

def math_quiz():
    """Run the math quiz game."""
    print("Welcome to the 6th Grade Math Quiz!")
    print("You will be given 5 questions to solve. Try your best!")

    score = 0
    total_questions = 5

    for i in range(total_questions):
        question, correct_answer = generate_question()

        # Ask the question
        print(f"Question {i + 1}: What is {question}?")
        
        # Get user's answer
        while True:
            try:
                user_answer = float(input("Your answer: "))
                break
            except ValueError:
                print("Please enter a valid number.")

        # Check the answer
        if abs(user_answer - correct_answer) < 0.01:  # Allow small margin of error for division
            print("Correct! Great job!")
            score += 1
        else:
            print(f"Oops! The correct answer was {correct_answer}.")

    # Display the final score
    print("\nQuiz complete!")
    print(f"Your final score is {score} out of {total_questions}.")

    if score == total_questions:
        print("Amazing! You're a math genius!")
    elif score >= total_questions // 2:
        print("Good job! Keep practicing to improve even more.")
    else:
        print("Don't worry, practice makes perfect!")

if __name__ == "__main__":
    math_quiz()
