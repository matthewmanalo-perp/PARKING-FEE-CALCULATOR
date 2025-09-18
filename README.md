import java.util.Scanner;
public class PARKING-FEE-CALCULATOR
{
	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		
		System.out.print("How many hours parked: ");
		int hours = sc.nextInt();
		
		System.out.print("Day Type (weekend/weekday): ");
		String dayType = sc.nextLine();
		 dayType = sc.nextLine();
		
		double fee = 0.0;
		
		double discount = 0.10; 
		if(hours <= 2){
		  fee = hours * 3.0; 
		}else if(hours >= 3 && hours <= 5 ){
		    fee = hours * 2.50;
		}else if(hours > 5){
		    fee = hours * 2.0;
		}if(dayType.equalsIgnoreCase("weekend")){
		    fee = fee - (fee * 0.10);
		}else if(fee > 20){
		    fee = 20.0;
		}
		 System.out.println("=======YOUR PARKING FEE====== ");
		 System.out.println("Hours parked: " + hours);
		 System.out.println("Day Type: " + dayType);
		 System.out.println("Fee: " + fee);
		
		}
	}
