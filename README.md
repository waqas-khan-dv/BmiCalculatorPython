# BmiCalculatorPython
a simple BMI cCalculator simulation in python to practice my coding skills
## Description

This is a simple BMI (Body Mass Index) Calculator simulation written in Python. It allows users to input their weight and height, and then calculates their BMI and categorizes it into different weight categories.

## Usage

To use the BMI Calculator, run the `main` function. You will be prompted to enter your weight in kilograms and your height in meters. The program will then calculate your BMI and display the corresponding weight category.

## Code

```python
def calculate_bmi(weight, height):
    try:
        bmi = weight / (height ** 2)
        return bmi
    except ZeroDivisionError:
        return "Height cannot be zero."

def bmi_category(bmi):
    if bmi < 18.5:
        return "Underweight"
    elif 18.5 <= bmi < 24.9:
        return "Normal weight"
    elif 25 <= bmi < 29.9:
        return "Overweight"
    else:
        return "Obesity"

def main():
    try:
        weight = float(input("Enter your weight in kilograms: "))
        height = float(input("Enter your height in meters: "))
        bmi = calculate_bmi(weight, height)
        if isinstance(bmi, str):
            print(bmi)
        else:
            category = bmi_category(bmi)
            print(f"Your BMI is {bmi:.2f}. You are classified as: {category}")
    except ValueError:
        print("Please enter valid numbers for weight and height.")

if __name__ == "__main__":
    main()
```

## Requirements

- Python 3.x

## How to Run

1. Clone the repository.
2. Navigate to the directory containing the script.
3. Run the script using Python.

```sh
python bmi_calculator.py
```

## License

This project is licensed under the MIT License.