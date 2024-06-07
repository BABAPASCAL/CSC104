class Account:
    def __init__(self, account_number, initial_balance=0):
        self._account_number = account_number
        self._balance = initial_balance

    def deposit(self, amount):
        if amount <= 50000:
            self._balance += amount
        else:
            print("Deposit limit exceeded. Maximum deposit allowed is 50,000")

    def withdraw(self, amount):
        if amount >= 2000 and amount <= self._balance:
            self._balance -= amount
        elif amount < 2000:
            print("Withdrawal amount must be at least 2,000")
        else:
            print("Insufficient funds")

    def check_balance(self):
        return self._balance

    def get_account_number(self):
        return self._account_number
