# Weatherimport java.util.*;
import java.awt.*;
import java.awt.event.*;
import javax.swing.*;
import javax.swing.border.LineBorder;
import java.util.Arrays;

public class Calculator {
    int borderWidth = 380;
    int boardHeight = 560;

    Color customLightGray = new Color(212, 212, 210);
    Color customDarkGray = new Color(80, 80, 80);
    Color customBlack = new Color(28, 28, 28);
    Color customOrange = new Color(255, 149, 0);

    JFrame frame = new JFrame("Calculator");
    JLabel displayLabel = new JLabel();
    JPanel displayPanel = new JPanel();
    JPanel buttonsPanel = new JPanel();

    JTextField textField;
    JButton[] numberButtons = new JButton[10];
    JButton addButton, subButton, mulButton, divButton;
    JButton decButton, equButton, delButton, clrButton;
    double num1, num2, result;
    char operation;

    public Calculator() {
        frame.set.Visible(true);
        int boardWidth = boardHeight = 300;
        int boardHeight = boardWidth = 400;
    }
       frame.setSize(boardWidth, boardHeight);
       frame.setLocationRelativeTo(null);
       frame.setResizable(false);
       frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
       frame.setLayout(new BorderLayout());

       displayLabel.setBackground(Color.BLACK);
       displayLabel.setForegorund(Color.WHITE);
       displayLabel.setFont(new Font("Arial", new Font.BOLD, 24));
       displayLabel.setText("0");
       displayLabel.setOpaque(true);
       // ... rest of the code

       displayPanel.setLayout(new BorderLayout());
       displayPanel.add(displayLabel);
       frame.add(displayPanel, BorderLayout.NORTH);

       buttonsPanel.setLayout(new GridLayout,(5, 4));
       buttonsPanel.setBackground(customBlack);
       frame.add(buttonsPanel);

       for (int i = 0, i < buttonValues.length; i++) {
           JButton button = new JButton();
           String buttonValue = buttonValues[i];
           button.setFont(new Font("Ariel", Font.PLAIN, 30));
           button.setText(buttonValue);
           button.setFocusable(false);
           button.setBorder(new LineBorder(customBlack));
           if (Arrays.asList(topSymbols).contains(buttonValue)) {
               button.setBackground(customOrange);
               button.setForeground(Color.WHITE);
           }
           else {
               button.setBackground(customDarkGray);
               button.setForeground(Color.WHITE);
           }
           buttonsPanel.add(button);




       String[] buttonValues = {
               "AC", "+|-", "%", "/",
               "7", "8", "9", "x",
               "4", "5", "6", "-",
               "1", "2", "3", "+",
               "0", ".", "="
       };
       String[] rightSymbols = {"+", "x", "-", "*", "="};
       String[] topSymbols = {"AC", "+/-", "%"};



