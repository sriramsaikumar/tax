# tax
import java.util.Scanner;
class Source {
    
    public static void main(String args[]) {
         Scanner scan = new Scanner(System.in);
        // Enter annual income
        double income = scan.nextDouble();
        // Enter age
        int age = scan.nextInt();
        
        double tax = 0.0;
        if(income<=250000){
            tax=0.0;
        }
        else if(income>=250001&&income<=300000){
            if(age>0&&age<60){
                tax=0.1*(income-250000);
            }
            else if(age>=60&&age<80){
                tax=0.0;
            }
            else{
                tax=0.0;
                }
        }
        else if(income>=300001&&income<=500000){
            if(age>0&&age<60){
                tax=0.1*(income-250000);
            }
            else if(age>=60&&age<80){
                tax=0.1*(income-250000);
                }
                else{
                    tax=0.0;
                }
        }
         else if(income>=500001&&income<=1000000){
                    if(age>0&&age<60){
                        tax=25000+0.2*(income-500000);
                    }
                    else if(age>=60&&age<80){
                        tax=25000+0.2*(income-500000);
                    }
                    else{
                        tax=25000+0.2*(income-500000);
                    }
         }
         else if(income>1000000){
             if(age>0&&age<60){
                 tax=1025000+0.3*(income-1000000);
                }
                else if(age>=60&&age<80){
                    tax=1025000+0.3*(income-1000000);
                }
                else{
                    tax=1025000+0.3*(income-1000000);
                }
         }
         else{
             System.out.println("invalid");
         }
         
        // Write your logic here
        
        System.out.print(tax);
        scan.close();
    }
}
