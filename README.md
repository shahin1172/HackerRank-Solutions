# HackerRank-Solutions
"This repository contains Python solutions to HackerRank challenges on algorithms, data structures, and problem-solving.
def minion_game(string):
    """
    This function determines the winner of the Minion Game based on a given string.

    Args:
        string: The string to be used for the game.

    Returns:
        None (prints the winner or a draw message to the console).
    """

    vowels = "AEIOU"

    kevin_score = 0
    stuart_score = 0

    for i in range(len(string)):
        if string[i].upper() in vowels:
            # Kevin gets points for the remaining characters in the string
            kevin_score += len(string) - i
        else:
            # Stuart gets points for the remaining characters in the string
            stuart_score += len(string) - i

    if kevin_score > stuart_score:
        print(f"Kevin {kevin_score}")
    elif stuart_score > kevin_score:
        print(f"Stuart {stuart_score}")
    else:
        print("Draw")
