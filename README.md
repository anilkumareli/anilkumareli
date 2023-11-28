
function displayMenu() {
  console.log("ATM Machine");
  console.log("1. Check Balance");
  console.log("2. Withdraw Money");
  console.log("3. Deposit Money");
  console.log("4. Exit");
}

function checkBalance() {
  console.log("Your balance is $" + balance);
}

function withdrawMoney(amount) {
  if (amount > 0 && amount <= balance) {
    balance -= amount;
    console.log("You have successfully withdrawn $" + amount);
  } else {
    console.log("Invalid amount or insufficient funds");
  }
}

function depositMoney(amount) {
  if (amount > 0) {
    balance += amount;
    console.log("You have successfully deposited $" + amount);
  } else {
    console.log("Invalid amount");
  }
}

function startATM() {
  var choice;
  do {
    displayMenu();
    choice = prompt("Enter your choice (1-4):");
    switch (choice) {
      case "1":
        checkBalance();
        break;
      case "2":
        var withdrawAmount = parseFloat(prompt("Enter the amount to withdraw:"));
        withdrawMoney(withdrawAmount);
        break;
      case "3":
        var depositAmount = parseFloat(prompt("Enter the amount to deposit:"));
        depositMoney(depositAmount);
        break;
      case "4":
        console.log("Thank you for using the ATM. Goodbye!");
        break;
      default:
        console.log("Invalid choice. Please enter a number between 1 and 4.");
    }
  } while (choice !== "4");
}
console.read 
