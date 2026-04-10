# ================================
# PAYROLL MANAGEMENT SYSTEM
# ================================

# Function to calculate salary
def calculate_salary(hours_worked, hourly_wage, overtime_hours, tax_rate):
    regular_salary = hours_worked * hourly_wage
    overtime_salary = overtime_hours * (hourly_wage * 1.5)
    gross_salary = regular_salary + overtime_salary
    tax_deduction = (tax_rate / 100) * gross_salary
    net_salary = gross_salary - tax_deduction
    return regular_salary, overtime_salary, gross_salary, tax_deduction, net_salary



def display_details(name, emp_id, regular_salary, overtime_salary, gross_salary, tax_deduction, net_salary):
    print("\n====== PAYROLL DETAILS ======")
    print("Employee Name :", name)
    print("Employee ID   :", emp_id)
    print("Regular Salary:", regular_salary)
    print("Overtime Pay  :", overtime_salary)
    print("Gross Salary  :", gross_salary)
    print("Tax Deduction :", tax_deduction)
    print("Net Salary    :", net_salary)
    print("=============================")


# Main function (Exception Handling + Input)
def main():
    try:
        name = input("Enter Employee Name: ")

        emp_id = input("Enter Employee ID (numbers only): ")
        
        
        if not emp_id.isdigit():
            raise ValueError("Employee ID must contain only numbers!")

        hours_worked = float(input("Enter total working hours: "))
        hourly_wage = float(input("Enter hourly wage: "))
        overtime_hours = float(input("Enter overtime hours: "))
        tax_rate = float(input("Enter tax rate (%): "))

        
        results = calculate_salary(hours_worked, hourly_wage, overtime_hours, tax_rate)

        
        display_details(name, emp_id, *results)

        
        with open("payroll.txt", "a") as file:
            file.write(f"{name}, {emp_id}, {results[-1]}\n")

    except ValueError as e:
        print("Error:", e)


# Run program
main()shu, 123, 45900.0
