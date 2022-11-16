# P1-17-Code Produkt
#include <stdlib.h>
#include <stdio.h>

double yearly_wage_to_hourly_wage();

int main() {
double train_ticket, plane_ticket, hourly_salary, yearly_salary = 120000;
char method;

    printf("Continue calculations based on hourly [h] or yearly [y] - salary?\n");
    scanf(" %c", &method);


    while ((method == 'y') || (method == 'h')) {

        if (method == 'h') {
            printf("vi er i løkken");
            break;
        } else if (method == 'y') {
            hourly_salary = yearly_wage_to_hourly_wage(yearly_salary);
            printf("\n%f\n", hourly_salary);
            break;
        } else {
            printf("faulty print, enter 'h' for hourly or 'y' for yearly");
            scanf("%c", &method);
        }


    }
    printf("Enter price of train ticket [int]");
    scanf("%d", &train_ticket);

    printf("Enter price of plane ticket [int]");
    scanf("%d", &plane_ticket);


    return 0;
}


double yearly_wage_to_hourly_wage(double yearly_sallery) {
double hourly_wage = 0, avarege_work_week = 52, averege_workhours_pr_week = 42.5, weekly_wage = 0;
weekly_wage = yearly_sallery / avarege_work_week;
hourly_wage = weekly_wage / averege_workhours_pr_week;
return hourly_wage;
}

void labour_hours_for_ticket(double hourly_wage, double plane_ticket_price, double train_ticket_price,
double *labour_hours_for_train_ticket, double *labour_hours_for_plane_ticket) {
*labour_hours_for_plane_ticket = plane_ticket_price /hourly_wage;
*labour_hours_for_train_ticket=train_ticket_price/hourly_wage;
}
