# DrGibson-HW
All HW FOR DR GIBSON

public class BasketballPlayer{
   private int freeThrowsAttempted;
   private int freeThrowsMade;
   private int threePointersAttempted;
   private int threePointersMade;
   private int twoPointersAttempted;
   private int twoPointersMade;
   private String name;
   
      public BasketballPlayer(String name) {
         this.name = name;
         freeThrowsAttempted = 0;
         freeThrowsMade = 0;
           }
         
      public String toString() {
         String str = "name=" + name;
         return name + ", Free throws attempted: " + freeThrowsAttempted + " ,Free Throw percentage: " + "%";
         }
         
      public int getFreeThrowsAttempted(){                               
         return freeThrowsAttempted;
         }
         
         
      public int getFreeThrowsMade(){
         return freeThrowsMade;
         }
         
      public double getFreeThrowPercentage(){
         double percentage = 0;
         if(freeThrowsAttempted == 0){
            return percentage;
            }
         else{
            percentage = 100.0 * freeThrowsAttempted / freeThrowsMade;
            return percentage;
         }
         
         
         
         
         
         
      }
      
                                                                            
            public static void main(String[] args) {                               
               BasketballPlayer baller = new BasketballPlayer("Kobe");
               
               System.out.println(baller);                                         // Test Code
               System.out.print(baller.getFreeThrowPercentage());
               
      
   }
   
}                                                                            //




   
