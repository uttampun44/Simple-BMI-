# Simple-BMI-
This project made in Java. It show your weight and guide fitness.

  import java.util.Scanner;
  class First{
        public void first(){
            try {
                /////////////Showing display value for user choice
                System.out.println("*****");
                System.out.println(" *** ");
                System.out.println("Welcome to BMI Converter");
                System.out.println("First select the Number");
                System.out.println("Enter the value of your body in:");
                  

                Scanner s = new Scanner(System.in);
         for(int i = 1; i <= 2; i++){
                   switch(i){
                     case 1:
                     System.out.println("1.Kg");
                     break;
                     case 2:
                     System.out.println("2.Pound");
                     break;
                 }
           }
                 ///user input
                 
                 int num = s.nextInt();
                
                 //////////First OPTION KG to pound
             if(num == 1){
                  
                 System.out.println("You have select the KG value");
                 }else if(num == 2){
                   
                     System.out.println("You have select the Pound");
                    // int m = rs.nextInt();
                      } else {
                              Scanner sc = new Scanner(System.in);
                              System.out.println("You have select the wrong input");
                              sc.close();
                                       }
                 //s.close();
                              }   
           
              catch (Exception e) {
               
               System.out.println(e);
           }
          
        }
   }     
   //////////Inheritance the class

    class Second extends First{
       public void second(){
             
             try{
                Scanner ns = new Scanner(System.in);
                System.out.println("Pick you measure value in");

                //////using loop  to show the switch case
             for(int j = 3; j <= 4; j++){
                
                switch(j){
                  case 3:
                  System.out.println("3.Kg");
                  break;

                  case 4:
                  System.out.println("4.Pound");
                  break;
        
              }
        }
             
                int values = ns.nextInt();

                ///////user input values
              if( values== 3){
              
                   Scanner v = new Scanner(System.in);
                  double pounds = v.nextDouble();
                  double Kilograms = pounds * 0.4535;
                  System.out.println("Your total weight in kilogram is " + Kilograms);
               // v.close();
               
           } else if(values == 4){

            Scanner l = new Scanner(System.in);
            double kilo = l.nextDouble();
            double pounds = kilo * 2.402;
            System.out.println("Your total weight in pound is " + pounds);
            //l.close();
             
           }
          // ns.close();

               Scanner f = new Scanner(System.in);
              System.out.println("Enter Your Height Also.");
               float height = f.nextFloat();
              
                System.out.println("Your height is "+ height);

                float weight = 60;
                if((weight >55 && weight<80)&&(height >= 5.4 && height<=6.0)){
                   System.out.println("You are fit! ");
                   System.out.println("According to your height and weight");
                }else{
                  System.out.println("You are unhealthy");
                }
                //f.close();
        }
        catch(Exception IO){
                System.out.println(IO);
        }
    }
}
public class BMI {
    public static void main(String[] args){
       Second s = new Second();
       s.first();
       s.second();
       
    }
}

