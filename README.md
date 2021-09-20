tic-tac- player vs player VERY beginner code




 board = np.array(["*","*","*","*","*","*","*","*","*"]) 
 win_commbinations = np.array([[0, 1, 2], [3, 4, 5], [6, 7, 8], [0, 3, 6], [1, 4, 7], [2, 5, 8], [0, 4, 8], [2, 4, 6]])

  for z in board:
    print("player 1 choose where to place a cross, to place your move choose a number in between 1-9 ")
    print(board[:3])
    print(board[3:6])
    print(board[6:])
    move = input()
    move = int(move) - 1
    if board[move] == "*":
        board[move] = "x"
    else :
        print("Invalid move, place is taken choose another number")
        move = input()
        move = int(move) - 1
        board[move] = "x"
        
    print("player 1 choose where to place a nought, to place your move choose a number in between 1-9 ")
    print(board[:3])
    print(board[3:6])
    print(board[6:])
    move = input()
    move = int(move) - 1
    if board[move] == "*":
        board[move] = "o"
    else :
        print("Invalid move, place is taken choose another number")
        move = input()
        move = int(move) - 1
        board[move] = "o"
        
    for a in win_commbinations:
    
        if board[a[0]] == board[a[1]] == board[a[2]] == "x":
            print("Player 1 Wins!")
            print("Congratulations!")
            break
        if board[a[0]] == board[a[1]] == board[a[2]] == "o":
            print("Player 2 Wins!")
            print("Congratulations!")
            break
