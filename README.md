//PROGRAM FOR ATM SERVICE CENTRE

#include<stdio.h>

int pin_no,count,option;

long int Deposit,WithDraw,Transfer,Balance_Amount=1000;

char Name[1000];

char Transaction='Y',dep='Y';

int main()

{

printf(">>>>>>>>>>>>>>WELCOME TO ATM<<<<<<<<<<<<<<\n\n");

printf("ENTER YOUR NAME :");

scanf("%s",Name);

 printf("HI %s....",Name);
 
 printf("\n");
 
 while(pin_no!=1234)    /*ASSUME THE PASSWORD AS 1234..*/
 
 {
     
      printf("ENTER YOUR SECRET PIN NUMBER : ");
      
      scanf("%d",&pin_no);
      
      if(pin_no!=1234)
      
      {
          
           printf("PLEASE ENTER VALID PASSWORD\n");
           
      }
      
 }
 
      do
      
      {
          
           printf("***************ATM MAIN MENU****************\n");
           
            printf("Enter[1] To Balance Enquiry\n");
            
             printf("Enter[2] To WithDraw Cash\n");
             
              printf("Enter[3] To  Deposit Cash\n");
              
               printf("Enter[4] To Transfer Fund\n");
               
                printf("Enter[5] To Exit \n");
                
                 printf("*******************************************\n\n");
                 
                  printf("PLEASE CHOOSE THE OPTION AND PRESS ENTER KEY");
                  
                  scanf("%d",&option);
                  
                  switch(option)
                  
                  {
                      
                      case 1:
                      
                      {
                          
                       printf("\nYOUR BALANCE IN Rs:%ld",Balance_Amount);
                       
                       break;
                       
                      }
                      
                       case 2:
                       
                       {
                           
                       printf("\nENTER TE AMOUNT TO WITHDRAW:");
                       
                       scanf("%ld",&WithDraw);
                       
                       if(WithDraw ==0)
                       
                       {
                           
                           printf("PLEASE ENTER THE AMOUNT TO WITHDRAW\n");
                           
                           }
                           
                       else if(WithDraw > (Balance_Amount-500))
                       
                       {
                           
                           printf("\nINSUFFICIENT BALANCE");
                           
                       }
                       
                       else
                       
                       
                       {
                           Balance_Amount=Balance_Amount-WithDraw;
                           
                           printf("\n\n PLEASE COLLECT THE CASH\n");
                           
                           printf("\n YOUR CURRENT BALANCE IS %ld",Balance_Amount);
                           
                       }
                       
                       break;
                       
                       }
                       
                        case 3:
                        
                        {
                            
                       printf("\nENTER THE AMOUNT TO DEPOSIT");
                       
                       scanf("%ld",&Deposit);
                       
                       Balance_Amount=Balance_Amount+Deposit;
                       
                     
                       printf(" YOUR BALANCE IS %ld",Balance_Amount);
                       
                       break;
                       
                        }
                        
                        case 4:
                        
                        {
                            
                       printf("\nYOUR BALANCE IN Rs:%ld",Balance_Amount);
                       
                       printf("\nENTER THE AMOUNT TO TRANSFER:");
                       
                       scanf("%ld",&Transfer);
                       
                       Balance_Amount=Balance_Amount-Transfer;
                       
                       printf(" YOUR BALANCE IS %ld",Balance_Amount);
                       
                       break;
                       
                        }
                        
                        case 5:
                        
                        {
                            
                       printf("\n ARE YOU WANT TO EXIT..?");
                       
                       break;
                       
                        }
                        
                        default:
                        
                        {
                            
                            printf("\n INVALID CHOICE");
                            
                        }
                        
                  }
                     printf("\n\n\n DO YOU WISH TO HAVE ANOTHER TRANSACTION ? (yes/no): \n");
                     
                     fflush(stdin);
                     
                     scanf("%c",&Transaction);
                     
                     if(Transaction=='N' || Transaction=='n')
                     
                     {
                         
                         count=1;
                         
                     }
                     
       }while(count!=1);
       
                      printf("\n\n THANK YOU FOR USING ATM SERVICE");
return 0;

}
