# Cash Register Lab

A Python `CashRegister` class that models the core functions of a real
cash register: adding items, applying a percentage discount, and voiding
the most recent transaction. Built as part of the OOP Part 2 lab.

## Description

This project implements a `CashRegister` class with the following behavior:

- **`add_item(item, price, quantity=1)`** — adds an item (or multiple units
  of it) to the register, updating the running total, the list of items,
  and a log of past transactions.
- **`apply_discount()`** — applies the register's discount percentage to
  the current total, if a discount greater than 0 was set and at least
  one item has been added. Prints a message with the new total, or a
  message saying there's no discount to apply.
- **`void_last_transaction()`** — reverses the most recent `add_item` call,
  subtracting its price from the total and removing the corresponding
  item(s) from the items list.

## Installation

Clone the repo and install dependencies with pipenv:

```bash
git clone [email protected]:JeffKibet/oop-p2-cash-register-lab.git
cd oop-p2-cash-register-lab
pipenv install
pipenv shell
```

## Usage

```python
from cash_register import CashRegister

register = CashRegister(20)  # 20% discount
register.add_item("macbook air", 1000)
register.apply_discount()
# After the discount, the total comes to $800.
```

## Running Tests

This project uses `pytest`. From the project root:

```bash
pytest
```

All 14 tests in `lib/testing/cash_register_test.py` should pass:

![Passing tests](./screenshot-tests-passing.png)

## Author

Built by [Jeff Kibet](https://github.com/JeffKibet) as part of a
software engineering bootcamp assignment.

## License

See [LICENSE.md](./LICENSE.md).