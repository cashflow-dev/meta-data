# Use Cases

## UC1 - View accounts

### CLI

1. User performs command  `cf account --list` (should also work wiht alias `cf account -l`)
2. A list of all the accounts is shown, containing, account name, amount and shortId

## UC2 - Create Account

### CLI

1. User performs the command `cf account --create`
2. The User is asked to provide an account name (required) and amount (optional - defaults to 0)

## UC3 - View Account Actions

### CLI

1. User performs UC1
2. User selects one of the accounts listed.
3. A list of actions is listed

## UC4 - Delete Account

### CLI

1. User performs UC3.
2. In the list of actions the user selects delete
3. The user is asked if he is sure, and confirms with either `N` (no) or `Y` (yes)

## UC5 - Edit account

### CLI

1. User performs UC3.
2. In the list of actions the user selects edit
3. A list of the account fields is shown, the user slects the fields he wishes to edit (ex. amount, name etc)
4. The user enters the new value
5. The user is asked if he wants to save, and confirms with either `N` (no) or `Y` (yes)

## UC6 - Overview

## CLI

1. User performs the command `cf overview`
2. A list of the current month upcomming incomes and expenses are listet. Also show the total amount of the month savings, expenses, incomes and whats left (incomes - expenses), also shows the amount of money on the primarly bank account

## UC7 - Income/Expense Actions

### CLI

1. The user performs UC6.
2. The user slects an income/expense
3. A list of actions is shown

## UC8 - Mark Income/Expense as "Paid"

### CLI

1. User performs UC7.
2. User selects "Paid".

## UC9 - Delete Income/Expense

### CLI

1. User performs UC7.
2. User selects Delete.

## UC10 - Postpone Income/Expense

### CLI

1. User performs UC7.
2. User selects "Postpone".
3. User enters a new date

## UC11 - Fulfill part of Income/Expense

### CLI

1. User performs UC7.
2. User selects "Partly Paid".
3. User enters the paid amount

## UC12 - List savings

### CLI

1. User performs the command `cf savings --list`
2. A list over the different savings are shown. Showing, name, saved amount and goal amount

## UC13 - Create new saving

### CLI

1. User performs the command `cf savings --create`
2. User gets asked to enter a savings name, savings goal and due date, an savings category and which savings account the saving is associated with

## UC14 - Create account

### CLI

1. User performs the command `cf signup`
2. User enters email and password.

## UC15 - Login

### CLI

1. User performs the command `cf signin`
2. User enters email and password

## UC16 - Not logged in

### CLI

1. User performs any command (beside UC15) and is not logged
2. A message is printed, informing the user to first login.

## UC17 - User is out of money on his primary account.

### CLI

1. User performs UC8 but has no money.
2. User gets to pick an savings account to take money from.
3. A transaction is created from savings account to primary banking account.
4. A loan is created (owed to savings) due date for next month
5. A lending is created (money savings is expected to get back)
6. A transaction is created (the money the user whishes to pay)

## UC18 - User creates income

### CLI

1. User performs the command `cf income --create`
2. User is asked to enter an amount, a name, if it is a recurrent or one-time income

## UC19 - User creates an expense

### CLI 

1. User performs the command `cf expense --create`
2. User is asked to enter an amount, a name, if it is a recurrent or one-time expense and if its a fixed or dynamic cost.
3. If its a cost that ocurrs more oftan than yearly and less than monthly the user gets the option to use savings.