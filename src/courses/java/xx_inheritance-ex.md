# Bank Accounts

1. Declare a class called `Account`.

- Declare the instance variables `funds` & `interestRate`.
  - `interestRate` will be set to `0`.
- Declare a protected constructor that instanciates the variables.
- Declare a method called `withdrawal` which will return the amount withdrawn and modify the `funds` variable.
  - If the account doesn't have enough funds, return the amount which is withdrawable.
- Declare a method called `deposit` which will add to our funds.
- Declare a method called `applyInterest` which will apply the current `ìnterestRate` to the current `funds`.
- Declare a method called `transferTo` which accepts a first parameter of Account and a second being the amount to transfer.

2. Declare a class called `Savings` which extends `Account`.

- This variation of `Account` will have a higher `interestRate`.
  - `interestRate` will be set to `6%`.
- `interestRate` is fixed and not changeable via the constructor of `Savings`.
- `Savings` cannot use `withdrawal`. If a `withdrawal` is attempted, throw a new `Exception`.

3. Declare a class called `Checking` which extends `Account`.

- `interestRate` will be set to `2%`.
- This variation of `Account` will have a `withdrawalLimit`.

```java
class Account{
  int funds;
  int interestRate;

  public Account(int funds, int interestRate){
    this.funds = funds;
    this.interestRate = interestRate;
  }

  public int withdrawal(int amount){
    if(funds < amount){
      int tmp = funds;
      funds = 0;
      return tmp;
    }
    funds -= amount;
    return amount;
  }

  public void deposit(int amount){
    funds += amount;
  }

  public void applyIntrest(){
    // TODO
  }

  public void TransferTo(Accout acc, int amount){
    int actualAmount = this.withDrawal(amount);
    acc.deposit(actualAmount);
  }
}

class Savings extends Account {

}

class Checking extends Account {

}

```
