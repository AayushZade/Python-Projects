import random

# Function to calculate the score
def calculate_score(cards):
    score = sum(cards)
    # If there's an Ace (11) and the score is over 21, convert the Ace to 1
    if 11 in cards and score > 21:
        cards.remove(11)
        cards.append(1)
        score = sum(cards)
    return score

# Function to display results
def display_results(user_cards, computer_cards):
    print(f"Your Final Hand: {user_cards}, final score: {calculate_score(user_cards)}")
    print(f"Computer's Final Hand: {computer_cards}, final score: {calculate_score(computer_cards)}")

# Main game loop
def play_blackjack():
    User_Input = input("Do you want to play the game of Blackjack? Type 'y' or 'n': ").lower()

    if User_Input == 'y':
        # Create deck of cards and initialize hands
        cards = [11, 2, 3, 4, 5, 6, 7, 8, 9, 10, 10, 10, 10]
        user_cards = [random.choice(cards) for _ in range(2)]
        computer_cards = [random.choice(cards) for _ in range(2)]

        # Show the user's cards and the computer's first card
        print(f"Your cards: {user_cards}, current score: {calculate_score(user_cards)}")
        print(f"Computer's first card: {computer_cards[0]}")

        # User's turn to draw cards
        another_card = input("Type 'y' to get another card, type 'n' to pass: ").lower()
        while another_card == 'y':
            user_cards.append(random.choice(cards))
            print(f"Your cards: {user_cards}, current score: {calculate_score(user_cards)}")
            print(f"Computer's first card: {computer_cards[0]}")
            
            # Check if the user's score exceeds 21
            if calculate_score(user_cards) > 21:
                display_results(user_cards, computer_cards)
                print("You went over 21. You Lost 😢")
                return
            
            # Ask again if the user wants another card
            another_card = input("Type 'y' to get another card, type 'n' to pass: ").lower()

        # Computer's turn to draw cards until the score reaches at least 17
        while calculate_score(computer_cards) < 17:
            computer_cards.append(random.choice(cards))

        # Show final hands and scores
        display_results(user_cards, computer_cards)

        # Determine the winner
        user_score = calculate_score(user_cards)
        computer_score = calculate_score(computer_cards)

        if computer_score > 21 or user_score > computer_score:
            print("You Win 😎")
        elif user_score == computer_score:
            print("It's a Draw 🤷‍♂️")
        else:
            print("You Lost 😢")

    else:
        print("Maybe next time!")

# Run the game
play_blackjack()
