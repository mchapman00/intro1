# Humans vs. Zombies part III

### PARTNER SWAP
* If you both finished (or very close to finished) your labs:
  - Get a copy of the working lab from your partner. They should email it to you.

* If you BOTH don't have a working lab, work on your own labs and help each other! I will walk around too. AFTER it works, then email your code to each other and do today's lab.

* Think about using the patch-ahead command. Look it up!


**FOR THIS LAB YOU ARE EDITING YOUR PARTNERS CODE! NOT YOURS!!!**

also: use (blue + 3) instead of blue.

## Instructions
1. Setup should make 2 safe havens for humans:
* Setup must make:
 - an 11x11 square of blue patches on the left side of the screen.
 - an  11x11 square of white patches on the right side of the screen.
 - These should be randomly positioned, but should not wrap around the world to the other side.
    hint: Pick the center of the square such that it is not close to a border and not close to the middle of the screen.

2. Zombie behavior modification:
* Zombies cannot step on the white/blue patches.
* Zombie Vision does not detect humans when they are in either safe haven (blue or white patch)
* When zombies kill a human, they should just change the breed of the human to zombie, and change the color to a zombie color.

3. Final Human Behavior: (try to get to a specific safe haven)
* Humans get a new variable "safeColor" which is set to blue or white randomly when they are created.
* When they are on a blue or white square that matches their safeColor, they will stay in that color, and not step on black patches anymore.
* When they are not on their proper safeColor, the humans will still wiggle normally.
* Set the human label to "B" or "W" based on their safeColor.

4. Add some chaos!
Make a button to make 10% of the humans chosen randomly, to change their safe color.
This will make the humans wiggle around to try to find the other safe haven.

5. Make a line graph to track:
* Number of zombies
* Number of humans
* Number of humans in their preferred safe haven color
