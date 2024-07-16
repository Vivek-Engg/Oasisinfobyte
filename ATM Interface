import java.util.Scanner;

class BankAccount {
    private double balance;

    public BankAccount(double balance) {
        this.balance += balance;
    }

    public double getBalance() {
        return balance;
    }

    public void deposit(double amount) {
        balance = amount;
    }

    public boolean withdraw(double amount){
        if(amount <= balance) {
            balance -= amount;
            return true;
        }else{
            return false;
        }
    }
}

public class atmsystem {
    private BankAccount bankAccount;
    private Scanner scanner;


    public atmsystem(BankAccount bankAccount) {
        this.bankAccount = bankAccount;
        this.scanner = new Scanner(System.in);
    }
     public void displayOption() {
        System.out.println("WELCOME TO BANK OF BARODA ATM!");
        System.out.println("1. Deposit");
        System.out.println("                               2.Withdraw ");
        System.out.println("3.Check Balance");
        System.out.println("                                4.Exit ");
     }

     public void Withdraw() {
        System.out.print("Enter amount to withdrawn: ");
        double amount = scanner.nextDouble();
        if (bankAccount.withdraw(amount)) {
            System.out.println("Withdrawl successful. Remaining balance: " + bankAccount.getBalance());
        } else {
            System.out.println("Insufficient balance.");
        }
     }

     public void deposite() {
        System.out.print("Enter amount to deposite: ");
        double amount = scanner.nextDouble();
        bankAccount.deposit(amount);
        System.out.println("Deposit successful. New balance:" + bankAccount.getBalance());

     }

     public void checkBalance() {
        System.out.println("Your current balance is: "+ bankAccount.getBalance());
     }


     public static void main(String[] args) {
        BankAccount bankAccount = new BankAccount(1000);
        atmsystem atm = new atmsystem(bankAccount);
        Scanner scanner = new Scanner(System.in);


        while (true) {
            
        
            atm.displayOption();
            System.out.print("Enter your choice: ");
            int choice = scanner.nextInt();

            switch (choice) {
                case 1:
                  atm.Withdraw();
                  break;
                case 2:

                  atm.deposite();
                  break;
                case 3:
                  atm.checkBalance();
                  break;
                case 4:
                  System.out.println("Thank you for using the ATM!");
                  scanner.close();
                  return;
                default:
                  System.out.println("Invaild choice. Please try again.");

            }
        }
     }
}
 
