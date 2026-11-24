# Assignment Project: Bicycle Rental and Mushroom Identifier

This is my Java Swing project, made in NetBeans. It starts with a welcome page where you pick one of two small programs:

1. **Bicycle rental**: works out how much you pay to rent a bicycle between two hours of the day.
2. **Mushroom identifier**: guesses which of six mushrooms you are thinking of from your yes/no answers.

I first wrote both programs for the console, then turned them into windows with buttons, text fields and radio buttons.

## What you need

- Java JDK 8 or newer
- NetBeans

## Files

The project is called `asssignmentproject` and everything is in the default package:

- `Welcome.java` is the welcome page. Run this one.
- `Bicycle_rental.java` is the bicycle rental page.
- `Mushroom_type.java` is the mushroom page.
- `Asssignmentproject.java` is the main class NetBeans created with the project.

## How to run it

1. Open the project in NetBeans.
2. Right-click `Welcome.java` in the Projects panel.
3. Click **Run File** (or press Shift+F6).

## The welcome page

- **Bicycle_rental** opens the bicycle page.
- **Mushroom_name** opens the mushroom page.
- **Exit** closes the program.

The **Cancel** button on both of the other pages brings you back to the welcome page.

## Bicycle rental

You type the starting hour and the ending hour (24-hour clock, so 14 means 2 PM) and press **Calculate**. The total shows up in the Total box in RWF.

Every hour is charged at its own rate:

| Hours | Price per hour |
|---|---|
| 0 to 6 | 500 RWF |
| 7 to 13 | 1000 RWF |
| 14 to 18 | 1500 RWF |
| 19 to 20 | 1000 RWF |
| 21 to 23 | 500 RWF |

For example, starting at 13 and ending at 15 gives 1000 + 1500 = 2500 RWF.

A message saying "Invalid rental hours!" pops up if:

- a box is empty or has anything other than a whole number
- the start hour is less than 0 or more than 23
- the end hour is less than 1 or more than 24
- the start hour is the same as or bigger than the end hour

## Mushroom identifier

You think of one of the six mushrooms and answer the questions with yes or no. The program only needs three questions at most:

1. Does it grow in the forest?
2. Does it have a convex cup?
3. Does it have a ring? (only matters if it grows in the forest and has a convex cup)
4. Does it have gills? (only matters if it grows in the forest and has no convex cup)

This is how the answers lead to a mushroom:

| Forest | Convex cup | Last question | Mushroom |
|---|---|---|---|
| No | Yes | none | Agaric jaunissant |
| No | No | none | Coprin chevelu |
| Yes | Yes | Ring: yes | Amanite tue-mouche |
| Yes | Yes | Ring: no | Pied bleu |
| Yes | No | Gills: yes | Girolle |
| Yes | No | Gills: no | Cepe de Bordeaux |

"Invalid selection!" appears if:

- question 1 or question 2 is not answered
- the last question you need (ring or gills) is not answered
- you answer more than three questions

## Names I used in the code

Bicycle page: `txtstart`, `txtend`, `txttotal`, `btncalculate`, `btncancle`

Mushroom page: `forestyes`, `forestno`, `convexyes`, `convexno`, `ringyes`, `ringno`, `gillsyes`, `gillsno`, `results`, `btnidentify`, `btncancle`

Welcome page: `btnbicycle`, `btnmushroom`, `btnexit`
