# Laminate Calculator

Works out how many packs of laminate flooring you need for a room and what they will cost. Enter the price per m², the coverage of one pack and the floor area, and it rounds up to whole packs and gives you the total price.

I built it from my time managing a flooring shop, where quickly working out packs and prices for a customer's room was an everyday job. It was my first finished Python program (August 2022), and I later rebuilt it as a desktop app with a Tkinter interface.

## Features

- Rounds up to whole packs, since you can't buy part of one
- Command-line version: `LaminateCal.py`
- Desktop version with a simple form and input checks: `LaminateCalGui.py`

## Built with

- Python 3
- Tkinter (desktop version)

## Running it

You need Python 3. No extra packages are required.

```
python3 LaminateCal.py       # command-line version
python3 LaminateCalGui.py    # desktop version
```

## Example

```
How much does the laminate cost per m2? >18.99
What is the pack size of the laminate in m2? >2.13
What is the area to be covered in m2? >14.5

You will need 7 packs of laminate
The area that will be covered is 14.91 m2
The total cost of your laminate will be £283.14
```

## What I learned

- Taking user input and converting it to numbers
- Using the `math` module to round up
- Building a basic GUI with Tkinter and showing error messages with `messagebox`

## Ideas for improvement

- Add an allowance for wastage and cuts (usually 5–10%)
- Show the total m² being bought in the desktop version, as the command-line version does
- Stop the desktop version from calculating when an input is invalid

## Bug fix (November 2026)

The original version multiplied the number of packs by the price per m², so it left out the pack size and under-quoted. It now works out the total m² in whole packs first, then multiplies that by the price per m².