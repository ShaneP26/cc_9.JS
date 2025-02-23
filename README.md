
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
    super(name, id, department, salary);
    this.teamSize = teamSize;
  }

  getDetails() {
    return `Manager: ${this.name}, ID: ${this.id}, Department: ${this.department}, Salary: $${this.salary}, Team Size: ${this.teamSize}`;
  }

  calculateBonus() {
    return this.calculateAnnualSalary() * 0.1;
  }
}

// Company class definition
class Company {
  constructor(name) {
    this.name = name;
    this.employees = []; // Array to store employee objects
  }
  addEmployee(employee) {
    this.employees.push(employee);
  }
 listEmployees() {
    this.employees.forEach(employee => {
      console.log(employee.getDetails());
    });
  }
}
const company = new Company("TechCorp");

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
}
class Manager extends Employee {
  constructor(name, id, department, salary, teamSize) {
    super(name, id, department, salary);
    this.teamSize = teamSize;
  }

  getDetails() {
    return `Manager: ${this.name}, ID: ${this.id}, Department: ${this.department}, Salary: $${this.salary}, Team Size: ${this.teamSize}`;
  }
calculateAnnualSalary() {
    const baseAnnualSalary = super.calculateAnnualSalary(); // Calculate base salary (salary * 12)
    const bonus = this.calculateBonus(); // Calculate bonus
    return baseAnnualSalary + bonus;
  }
 calculateBonus() {
    return this.salary * 12 * 0.1; // 10% of the annual salary
  }
}
class Company {
  constructor(name) {
    this.name = name;
    this.employees = []; // Array to store employee objects
  }
 addEmployee(employee) {
    this.employees.push(employee);
  } listEmployees() {
    this.employees.forEach(employee => {
      console.log(employee.getDetails());
    });
  }
calculateTotalPayroll() {
    return this.employees.reduce((total, employee) => total + employee.calculateAnnualSalary(), 0);
  }
}
const company = new Company("TechCorp");

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
}

// Manager class definition (from Task 2)
class Manager extends Employee {
  constructor(name, id, department, salary, teamSize) {
    super(name, id, department, salary);
    this.teamSize = teamSize;
  }
getDetails() {
    return `Manager: ${this.name}, ID: ${this.id}, Department: ${this.department}, Salary: $${this.salary}, Team Size: ${this.teamSize}`;
  }

  calculateAnnualSalary() {
    const baseAnnualSalary = super.calculateAnnualSalary();
    const bonus = this.calculateBonus();
    return baseAnnualSalary + bonus;
  }

  calculateBonus() {
    return this.salary * 12 * 0.1;
  }
}class Company {
  constructor(name) {
    this.name = name;
    this.employees = []; // Array to store employee objects
  }

  addEmployee(employee) {
    this.employees.push(employee);
  }

  listEmployees() {
    this.employees.forEach(employee => {
      console.log(employee.getDetails());
    });
  }

  calculateTotalPayroll() {
    return this.employees.reduce((total, employee) => total + employee.calculateAnnualSalary(), 0);
  }
promoteToManager(employee, teamSize) {
    if (employee instanceof Employee && !(employee instanceof Manager)) {
