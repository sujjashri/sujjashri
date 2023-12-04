#include <stdio.h>

double basicSalary() 
{
  double basic_salary;
  printf("Enter basic salary: ");
  scanf("%lf", &basic_salary);
  return basic_salary;
}

double EPF(double basic_salary) 
{
//printf("\nEPF decuction: ");
  return 0.11 * basic_salary;
}

double calculateBonus(double basic_salary) 
{
  return 0.5 * basic_salary;
} 

void displayTotalPay(double basic_salary, double epf, double bonus) 
{
  //printf("\nYour total pay is: ");
  double net_salary = basic_salary - epf;
  double total_pay = net_salary + bonus;
  printf("\nBasic Salary: %.2f", basic_salary);
  printf("\nEPF decuction: %.2f", epf);
  printf("\nNet Salary: %.2f", net_salary);
  printf("\nBonus: %.2f", bonus);
  printf("\nYour Total Pay is : %.2f", total_pay);
}

int main() 
{
  double basic_salary = basicSalary();
  double epf = EPF(basic_salary);
  double bonus = calculateBonus(basic_salary);
  displayTotalPay(basic_salary, epf, bonus);
  return 0;
}
