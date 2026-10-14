wins = 0
losses = 0
ties = 0
seed = 0
play_again = "y"

print("ROCK PAPER SCISSORS")

while play_again == "y":
    print("1 = ROCK, 2 = PAPER, 3 = SCISSORS")
    print("CHOICE")

    # Read the player's choice; non-numbers count as invalid
    try:
        player = int(input())
    except ValueError:
        player = 0

    if player < 1 or player > 3:
        print("INVALID CHOICE, ENTER 1, 2 OR 3")
    else:
        # Computer picks: seed jumps to a new value, then maps to 1..3
        seed = (seed * 7 + 5) % 11
        computer = seed % 3 + 1

        # Turn the computer's number into a name
        if computer == 1:
            comp_name = "Rock"
        elif computer == 2:
            comp_name = "Paper"
        else:
            comp_name = "Scissors"

        print("Computer chose: " + comp_name)

        # Decide the winner
        if player == computer:
            print("It's a tie")
            ties += 1
        elif ((player == 1 and computer == 3) or
              (player == 2 and computer == 1) or
              (player == 3 and computer == 2)):
            print("You won this round!")
            wins += 1
        else:
            print("You lose")
            losses += 1

        print(f"Score - Wins: {wins}  Losses: {losses}  Ties: {ties}")

    print("Play again? (y/n)")
    play_again = input().strip().lower()
