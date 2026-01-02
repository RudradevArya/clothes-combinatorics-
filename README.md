# Wardrobe Optimizer

A minimalist tool to calculate the mathematically perfect "Capsule Wardrobe." It helps users determine the minimum number of clothing items required to generate a unique outfit for every day of a specific time range (e.g., a year).

## Main Goal
To answer the question: **"How can I maximize unique outfits while buying the minimum number of items?"**

Most people think 10 shirts and 10 pants = 20 outfits (Addition).
This tool proves that 10 shirts and 10 pants = 100 outfits (Multiplication/Combinatorics).

## Features & Enhancements

1.  **Optimized Calculation:** Finds the ideal balance of items (e.g., 19 shirts × 20 pants) to cover a target date range with the lowest total item count.
2.  **Comparative Analysis:** Compares the "Optimized" strategy against the "Exact" strategy (Prime Factorization) to show why flexibility saves money.
3.  **Smart User Interface:**
    * Responsive Sidebar explaining the math.
    * Preset ranges (Month, Year, Lifetime) + Custom input.
    * Automatic labeling of categories (Shirts, Pants, Socks, etc.).
4.  **Visual Feedback:** Green (Winner) vs. Orange (Expensive) cards to highlight efficiency.

## The Math Behind It

### 1. The Optimization Strategy (The "Cube Root" Method)
To minimize the sum of factors while maximizing their product, the factors should be as close to each other as possible (Squares are better than thin Rectangles).
* **Formula:** Base Item Count = $\lfloor \sqrt[Categories]{Days} \rfloor$
* **Algorithm:** We start with the base count (e.g., $[19, 19]$) and add 1 item to the smallest pile until the product $\ge$ Target Days.

### 2. The "Exact" Strategy (Prime Factorization)
This method forces the outfits to equal the target exactly.
* **Example (365 Days):** Factors are $73 \times 5$.
* **Result:** You need 73 Shirts and 5 Pants.
* **Total Items:** $73 + 5 = 78$.
* **Vs Optimized:** 19 Shirts + 20 Pants = 39 Items. Optimization wins!

### 3. The "Cicada" Strategy
Inspired by Reddit user `BeardedBaldMan`, this concept relies on **Coprime numbers**. If you have 7 Shirts and 3 Pants (7 and 3 share no factors), the combination "Shirt A + Pant B" won't repeat for $7 \times 3 = 21$ days.

## Resources & References
* **Spreadsheet:** `clothing_combos.xlsx` (Matt Parker/Stand-up Maths).
* **Video:** Stand-up Maths video on Wardrobe Combinatorics.
* **Reddit Inspiration:** User `BeardedBaldMan` explaining the 7 Shirts / 3 Pants rotation strategy to avoid the "Tuesday Outfit" problem.

## Learning Journey Questions
* *Why is $3 \times 3$ better than 6 items in one pile?* (Multiplication vs Addition)
* *Why does the calculator jump from 366 to 392?* Because aiming for exactly 366 (factors 61, 3, 2) requires 66 items, but aiming for 392 (factors 8, 7, 7) only requires 22 items.
* *What is the binary method?* Using "Wearing vs Not Wearing" an item to generate $2^N$ combinations.

---
*Built with HTML, CSS, and vanilla JavaScript.*