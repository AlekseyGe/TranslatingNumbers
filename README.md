# TranslatingNumbers
What is that? In that world there are a lot of `number systems`. For for example decimal, binary, octal and hexadecimal. That programm can convert numbers from one system to another

## How to use it
You enter your number systems and the programm will convert it into another systems

## The code
```
import static javax.swing.JOptionPane.*;

int binaryToDecimal(String num) {
    return Integer.parseInt(num, 2);
}
String binaryToOctal(String num) {
    int decimal = binaryToDecimal(num);
    return Integer.toOctalString(decimal);
}
String binaryToHexadecimal(String num) {
    int decimal = binaryToDecimal(num);
    return Integer.toHexString(decimal).toUpperCase();
}

String decimalToBinary(int num) {
    return Integer.toBinaryString(num);
}
String decimalToOctal(int num) {
    return Integer.toOctalString(num);
}
String decimalToHexadecimal(int num) {
    return Integer.toHexString(num).toUpperCase();
}

int octalToDecimal(String num) {
    return Integer.parseInt(num, 8);
}
String octalToBinary(String num) {
    int decimalValue = octalToDecimal(num);
    return Integer.toBinaryString(decimalValue);
}
String octalToHexadecimal(String num) {
    int decimalValue = octalToDecimal(num);
    return Integer.toHexString(decimalValue).toUpperCase();
}

int hexToDecimal(String num) {
    return Integer.parseInt(num, 16);
}
String hexToBinary(String num) {
    int decimalValue = hexToDecimal(num);
    return Integer.toBinaryString(decimalValue);
}
String hexToOctal(String num) {
    int decimalValue = hexToDecimal(num);
    return Integer.toOctalString(decimalValue);
}

void setup() {
    int num = parseInt(showInputDialog(null, "Enter your number:"));
    String num2 = Integer.toString(num);

    String[] options = {"Decimal", "Binary", "Octal", "Hexadecimal"};
    String selectedOption = (String) showInputDialog(null, "Select the number system of your input:", "System Selection", QUESTION_MESSAGE, null, options, options[0]);

    if (selectedOption.equals("Binary")) {
        showMessageDialog(null, "Decimal: " + binaryToDecimal(num2) + "\nOctal: " + binaryToOctal(num2) + "\nHexadecimal: " + binaryToHexadecimal(num2));
    } else if (selectedOption.equals("Decimal")) {
        showMessageDialog(null, "Binary: " + decimalToBinary(num) + "\nOctal: " + decimalToOctal(num) + "\nHexadecimal: " + decimalToHexadecimal(num));
    } else if (selectedOption.equals("Octal")) {
        showMessageDialog(null, "Decimal: " + octalToDecimal(num2) + "\nBinary: " + octalToBinary(num2) + "\nHexadecimal: " + octalToHexadecimal(num2));
    } else {
        showMessageDialog(null, "Decimal: " + hexToDecimal(num2) + "\nBinary: " + hexToBinary(num2) + "\nOctal: " + hexToOctal(num2));
    }
}

```
