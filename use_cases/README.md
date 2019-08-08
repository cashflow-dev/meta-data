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
2. A list of the current month upcomming incomes and expenses are listet.

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