# WaterDispenser

import java.util.Scanner;

public class P50_WaterDispenser {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        int volumeCup = Integer.parseInt(scanner.nextLine());
        int volumeWater = 0;
        int count = 0;

        while (volumeCup > volumeWater) {
            String button = scanner.nextLine();
            switch (button) {
                case "Easy":
                    volumeWater += 50;
                    break;
                case "Medium":
                    volumeWater += 100;
                    break;
                case "Hard":
                    volumeWater += 200;
                    break;
            }
            count++;
        }
        if (volumeCup == volumeWater) {
            System.out.printf("The dispenser has been tapped %d times.", count);
        } else {
            System.out.printf("%dml has been spilled.", volumeWater - volumeCup);
        }
    }
}
