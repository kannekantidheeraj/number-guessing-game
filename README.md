# number-guessing-game#include <stdio.h>
#include <stdlib.h>  
#include <time.h>    

int main() {
    srand(time(0));
    int random_value = (rand() % 100) + 1;
    int gussed;
    int no_of_gusses = 0;
    printf("the computer has a number try to guess the number correctly it is in between 1 to 100\n");
    do{
        printf("enter the correct number =  ");
        scanf("%d",&gussed);
      no_of_gusses++;
        if(gussed<random_value){
            printf("higher number please\n");
        }
        else if(gussed>random_value){
            printf("lower number please\n");
        }
        else{
            printf("Congrats! you have guessed the correct number\n" );
        }
    }while(gussed!=random_value);
    printf("you  took %d attempts to guess the number",no_of_gusses);

    return 0;
}
