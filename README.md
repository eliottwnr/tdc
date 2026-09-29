# Trou du cul (TDC)

A digital implementation of the traditional card game **Trou du cul** (also known internationally as **President**, **Scum**, or **Asshole**), developed with [Godot Engine 4](https://godotengine.org/).

---

## What is "Trou du cul"?

**Trou du cul** is a popular shedding card game for 4 or more players played with a standard 52-card deck. The goal is to get rid of all your cards as fast as possible. Finishing position determines each player's social rank and privileges for the following round.

### Objective
- Be the first player to empty your hand to become the **President**.
- Avoid being the last player with cards, who becomes the **Trou du cul** (Asshole).

---

## Hierarchy & Social Roles

At the end of each round, players earn ranks according to the order in which they shed all their cards:

| Rank | French Title | English Title | Description & Privilege |
| :--- | :--- | :--- | :--- |
| **1st** | **Président** | President | Wins the round. Receives the best 2 cards from the Trou du cul and gives away 2 cards of choice. Leads first in the next round. |
| **2nd** | **Vice-Président** | Vice-President | Receives the best 1 card from the Vice-Trou du cul and gives away 1 card of choice. |
| **Middle** | **Citoyens / Neutres** | Citizens / Neutrals | No card exchanges; they stay neutral. |
| **2nd to last** | **Vice-Trou du cul** | Vice-Asshole | Must give their highest card to the Vice-President and receives 1 card in return. |
| **Last** | **Trou du cul** | Asshole | Cleans/deals cards, must give their 2 highest cards to the President, and receives 2 cards in return. |

*(Note: In a 4-player game, there are no Citizens—only President, Vice-President, Vice-Trou du cul, and Trou du cul).*

---

## Card Values & Combinations

### Card Ranking (Lowest to Highest)
In standard Trou du cul, the card order is inverted compared to standard games:
$$\text{3} < \text{4} < \text{5} < \text{6} < \text{7} < \text{8} < \text{9} < \text{10} < \text{J} < \text{Q} < \text{K} < \text{A} < \text{2}$$
- **3** is the lowest card.
- **2** is the highest card.

### Valid Combinations
Players can play combinations of matching rank:
- **Singles** (e.g., 5)
- **Pairs** (e.g., 7-7)
- **Three of a kind** (e.g., J-J-J)
- **Four of a kind** (e.g., K-K-K-K)

---

## 📜 How to Play

1. **Card Exchange**: Before play begins, the President/Vice-President and Trou du cul/Vice-Trou du cul exchange cards according to their rank.
2. **Opening Lead**: The President (or the player with the 3 of Clubs in the very first round) plays an opening combination (single, pair, etc.).
3. **Following Turns**:
   - The next player must play the **exact same number of cards** with a **strictly higher value** (or equal, depending on variant rules).
   - Alternatively, a player may **Pass**. Passing does not eliminate a player from future turns in the same trick unless playing strict pass rules.
4. **Clearing the Trick**:
   - When all other players pass in succession, the trick ends and the pile is cleared.
   - The last player who played leads the next trick with any combination.
   - A **2** (or a four-of-a-kind in many variants) instantly cuts/clears the trick.
5. **Next Round**: As players discard their final card, they exit and claim the next available rank. The game continues until only one player remains with cards.

---

## Common Variant Rules

- **Revolution**: Playing four cards of the same rank reverses card values for the rest of the round (3 becomes highest, 2 becomes lowest).
- **Two Cuts**: Playing a 2 immediately ends the trick, and that player leads the next round.
- **Equal Skip / Pass**: Playing an identical card value skips the next player.

---

## Getting Started

### Prerequisites
- [Godot Engine 4.x](https://godotengine.org/download) (Compatible with Godot 4.7+)

### Running the Project
1. Clone the repository:
   ```bash
   git clone https://github.com/eliottwnr/tdc.git
   ```
   or 
   ```bash
   git clone https://gitlab.com/eliott.wnr/tdc.git
   ```
2. Open **Godot Engine**.
3. Click **Import** and select `project.godot` inside the project folder.
4. Press **Run Project** (`F5`) or edit the scenes.
