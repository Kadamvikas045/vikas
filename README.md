import java.util.Scanner;

class TemperatureConverter {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        System.out.println("🌡️ Temperature Conversion Program");

        System.out.print("Enter temperature value: ");
        double temp = sc.nextDouble();

        System.out.print("Enter unit (C for Celsius, F for Fahrenheit, K for Kelvin): ");
        char unit = sc.next().toUpperCase().charAt(0);

        if (unit == 'C') {
            double fahrenheit = (temp * 9/5) + 32;
            double kelvin = temp + 273.15;
            System.out.printf("\n%.2f°C = %.2f°F\n", temp, fahrenheit);
            System.out.printf("%.2f°C = %.2fK\n", temp, kelvin);

        } else if (unit == 'F') {
            double celsius = (temp - 32) * 5/9;
            double kelvin = celsius + 273.15;
            System.out.printf("\n%.2f°F = %.2f°C\n", temp, celsius);
            System.out.printf("%.2f°F = %.2fK\n", temp, kelvin);

        } else if (unit == 'K') {
            double celsius = temp - 273.15;
            double fahrenheit = (celsius * 9/5) + 32;
            System.out.printf("\n%.2fK = %.2f°C\n", temp, celsius);
            System.out.printf("%.2fK = %.2f°F\n", temp, fahrenheit);

        } else {
            System.out.println("❌ Invalid unit! Please enter C, F, or K.");
        }

        sc.close();
    }
}
