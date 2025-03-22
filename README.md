# COP2664-1-Lesson-6-Programming-Assignment-2
This repository is a submission link for COP2664-1: Lesson 6 Programming Assignment 2

// This program is designed to calculate the bonus that will be given to employees based on their years of service and their salary amount.

import Foundation

func calculateBonus(name: String?, salary: Double, yearsOfService: Int) {
    guard let name = name, !name.isEmpty, salary > 0, yearsOfService >= 0 else {
      // If the name is empty, the salary is not positive, or the years of service is not positive, the program will print an error message and return.
        print("Invalid input! salary and/or years of service must be official: \(name ?? "Unknown"), \(salary), \(yearsOfService)")
        return
    }
    var bonusPercentage: Double = 0.0
    if yearsOfService >= 5 {
        bonusPercentage = 0.2
    } else if yearsOfService >= 3 {
        bonusPercentage = 0.1
    } else if yearsOfService >= 1 {
        bonusPercentage = 0.05
    } else if yearsOfService == 0 {
        bonusPercentage = 0.0
    }
  // If the years of service is greater than or equal to 5, the bonus percentage is 20%. If the years of service is greater than or equal to 3, the bonus percentage is 10%. If the years of service is greater than or equal to 1, the bonus percentage is 5%. If the years of service is 0, the bonus percentage is 0%.
    let bonusAmount = salary * bonusPercentage
    print("Employee: \(name)")
    print("Salary: $\(salary)")
    print("Years of Service: \(yearsOfService)")
    print("Bonus Percentage: \(bonusPercentage * 100)%")
    print("Bonus Amount: $\(bonusAmount)")
}
// This function takes the name, salary, and years of service as input and calculates the bonus percentage and amount based on the years of service.
calculateBonus(name: "Caleb Danielson", salary: 60000.0, yearsOfService: 2)
calculateBonus(name: "Jane Smith", salary: 50000.0, yearsOfService: 7)
calculateBonus(name: "Bob Johnson", salary: 80000.0, yearsOfService: 0)
calculateBonus(name: "Alice Brown", salary: 55000.0, yearsOfService: -1)
calculateBonus(name: "Michael Lee", salary: -4000.0, yearsOfService: 8)
