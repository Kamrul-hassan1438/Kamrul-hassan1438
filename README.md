- 👋 Hi, I’m @Kamrul-hassan1438
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
Kamrul-hassan1438/Kamrul-hassan1438 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
#include<stdio.h>


void main()
{
    int a,b,c,q,n=0,i;
    int count=0;
    char op;
    float average=0, sum=0;
    //64 cities
    // n how many city we want to track.
    const int N[64]= {};
    printf("======= BD Covid Case Tracking System =========\n");
    printf("1.Enter a to take the number of COVID patients\n");
    printf("2.Enter b to find the average number of patients of all the cities\n");
    printf("3.Enter c display which city have above average COVID patients\n");
    printf("4.Enter q to exit the menu system\n");


    //If user input 'q' the program will be exit.

    while(op!='q')
    {

        printf("\nEnter your choice ");
        scanf(" %c",&op);
        switch (op)
            //Enter �a�, to take the number of COVID patients of all cities into �patients� array of size N.
            //Enter �b�, to find the average number of patients of all the cities.

            //Enter �c�, to count and display the # of cities which have above average COVID patients.

            //Enter �q�, to quit/exit the menu system.

            //For any other input, display Invalid Input.
        {
        case'a':{
            printf("How many City you want to track the number of COVID patients ");
            scanf("%d",&n);
            if(64>=n){
            for(i=0; i<n; i++)
            {
                printf("city%d COVID patients ",i+1);
                scanf("%d",&N[i]);
                sum+=N[i];
                average=sum/(float)n;


            }
            }
            break;
        }
    case 'b':
        {
            if(n!=0)
            {

                printf("\nAverage number of patients of all the cities %.2f ",average);
            }

            else
            {
                printf("No patients information is found");
            }

            break;


        }
    case 'c':
        {

            if(n!=0)
            {
                for(i=0; i<n; i++)
                {
                    if (N[i]>average)
                    {
                        printf(" city %d have above average COVID patients \n",i+1);
                        //count how many cities have above average  Covid patients
                        count++;
                    }
                }
                printf(" \n %d cities have above average COVID patients",count);
            }
            else
            {
                printf("No patients information is found");
            }

            break;

        }
    case 'q':
        {
            break;
        }


    default:
        printf("Invalid Input");

    }

}

}

