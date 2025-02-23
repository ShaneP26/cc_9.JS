
class Employee {constructor(name, id, department, salary) {
    this.name = name;
    this.id = id;
    this.department = department;
    this.salary = salary;
  }
  getDetails() {
    return `Employee: ${this.name}, ID: ${this.id}, Department: ${this.department}, Salary: $${this.salary}`;
  }
calculateAnnualSalary() {
    return this.salary * 12;
  }
}
const emp1 = new Employee("Alice Johnson", 101, "Sales", 5000);

class Employee {
  constructor(name, id, department, salary) {
    this.name = name;
    this.id = id;
    this.department = department;
    this.salary = salary;
  }

  getDetails() {
    return `Employee: ${this.name}, ID: ${this.id}, Department: ${this.department}, Salary: $${this.salary}`;
  }

  calculateAnnualSalary() {
    return this.salary * 12;
  }
}class Manager extends Employee {
  constructor(name, id, department, salary, teamSize) {
    // Call the parent class constructor
    super(name, id, department, salary);
    this.teamSize = teamSize;
  }
  getDetails() {
    return `Manager: ${this.name}, ID: ${this.id}, Department: ${this.department}, Salary: $${this.salary}, Team Size: ${this.teamSize}`;
  }
calculateBonus() {
    return this.calculateAnnualSalary() * 0.1;  // 10% of the annual salary
  }
}
const mgr1 = new Manager("John Smith", 201, "IT", 8000, 5);
