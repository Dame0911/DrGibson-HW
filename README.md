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
     
  public double getFreeThrowPercent(){
     double percentage = 0;
     if(freeThrowsAttempted == 0){
        return percentage;
        }
     else{
        percentage =  100 *freeThrowsMade / freeThrowsAttempted;
        return percentage;
     }
     }
     
   public void shootFreeThrow(boolean isMade){
         if(isMade){
         freeThrowsMade++ ;
         }
         freeThrowsAttempted++ ;
     
  }
  

      public static void main(String[] args) {
		testShootFreeThrows();
//		testShootTwoPointers();
//		testShootThreePointers();
//		testGetTotalPoints_OnlyFreeThrows();
//		testGetTotalPoints_OnlyTwoPointers();
//		testGetTotalPoints_OnlyThreePointers();
//		testGetTotalPoints();
//		testToString();
	}
	
	private static void testShootFreeThrows() {
		System.out.println("-->testShootFreeThrows()");
		BasketballPlayer p = new BasketballPlayer("Paul");
		p.shootFreeThrow(true);
		p.shootFreeThrow(true);
		p.shootFreeThrow(false);
		p.shootFreeThrow(true);
		p.shootFreeThrow(false);
		int numMade = p.getFreeThrowsMade();
		int numAtt = p.getFreeThrowsAttempted();
		double percent = p.getFreeThrowPercent();
		String msgExpected = String.format("Expected: made=%d, attempted=%d, percent=%.1f%%", 3, 5, 60.0);
		String msgActual =   String.format("  Actual: made=%d, attempted=%d, percent=%.1f%%", numMade, numAtt, percent);
		System.out.println(msgExpected);
		System.out.println(msgActual);
	}

            /*                    
           BasketballPlayer baller = new BasketballPlayer("Kobe");
           baller.shootFreeThrows(true);
           baller.shootFreeThrows(true);
           baller.shootFreeThrows(false);
           System.out.println(baller);                                         // Test Code "Free throws Attempted: ", "Free Throws made: ", 
           System.out.println(baller.getFreeThrowPercentage());
           System.out.println(baller.getFreeThrowsAttempted());
           System.out.print(baller.getFreeThrowsMade());
           */               
}

     //




   
