import java.util.Scanner;

public class RomanArabianCalculator {
    public static void Main {
        System.out.println("Укажите операцию");
        System.out.println("1. Сложение");
        System.out.println("2. Вычетание");
        System.out.println("3. Умножение");
        System.out.println("4. Деление");
        Scanner scanner = new Scanner(System.in);
        int operation = Scanner.nextInt();
        System.out.println("Первое число");
        int a = Scanner.nextInt();
        System.out.println("Второе число");
        int b = Scanner.nextInt();
        int result;
        if (operation == 1) {
            result = a + b;
        } else if (operation == 2) {
                result = a - b;
        } else if (operation == 3) {
            result = a * b;
        } else if (operation == 4) {
            result = a / b;
            }
        System.out.println("Результат = " + result);

        }
    }
}

    private static String convertNumToRoman (int numArabian) {
        String[] roman = {"O", "I", "II", "III", "IV", "V", "VI", "VII", "VIII", "IX", "X"
        };
        final String s = roman[numArabian];
        return s;
    }


    private static int romanToNumber (String roman) {
        try {
            switch (roman) {
                case "I":
                    return 1;
                case "II":
                    return 2;
                case "III":
                    return 3;
                case "IV":
                    return 4;
                case "V":
                    return 5;
                case "VI":
                    return 6;
                case "VII":
                    return 7;
                case "VIII":
                    return 8;
                case "IX":
                    return 9;
                case "X":
                    return 10;
                default:
                    throw new IllegalStateException("Unexpected value: " + roman);
            }
        } catch (InputMismatchException e) {
            throw new InputMismatchException("Неверный формат данных");
        }
        return -1;
    }
