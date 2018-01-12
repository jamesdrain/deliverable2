import java.util.Scanner;

public class DiffDates {
	public static void main(String[] args) {
		Scanner scnr = new Scanner(System.in);
		int firstYear   = 0;
		int firstMonth  = 0;
		int firstDay    = 0;
		int secondYear  = 0;
		int secondMonth = 0;
		int secondDay   = 0;
		int sumOfDays1  = 0;
		int sumOfDays2  = 0;
		int diffDays    = 0;

		// Get dates

		System.out.println("Let's compare two dates. \nFirst, give me a year: ");
		firstYear = scnr.nextInt();
		System.out.println("Now the month (1-12): ");
		firstMonth = scnr.nextInt();
		System.out.println("And the day: ");
		firstDay = scnr.nextInt();
		System.out.println("Ok, " + firstMonth + "/" + firstDay + "/" + firstYear + "\nNow for the second date. \nWhat year: ");
		secondYear = scnr.nextInt();
		System.out.println("And the month: ");
		secondMonth = scnr.nextInt();
		System.out.println("The day: ");
		secondDay = scnr.nextInt();
		System.out.println("    " + secondMonth + "/" + secondDay + "/" + secondYear);

		// Calculate difference

		sumOfDays1 = (firstYear * 365) + (firstMonth * 30) + (firstDay);
		sumOfDays2 = (secondYear * 365) + (secondMonth * 30) + (secondDay);
		if (sumOfDays1 >= sumOfDays2) {
			diffDays = sumOfDays1 - sumOfDays2;
		} else {
			diffDays = sumOfDays2 - sumOfDays1;
		}
		int finalYear = diffDays / 365;
		int monthCalc = diffDays % 365;
		int finalMonth = monthCalc / 30;
		int finalDays = monthCalc % 30;
		
		System.out.println("Those dates are " + finalYear + " years " + finalMonth + " months and " + finalDays + " days apart.");
 
		scnr.close();
	}
	

}

