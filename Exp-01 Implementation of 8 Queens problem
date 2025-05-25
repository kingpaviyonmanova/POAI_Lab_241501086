def is_safe(board, row, col, N):
    for i in range(row):
        if board[i] == col or abs(board[i] - col) == abs(i - row):
            return False
    return True

def solve_n_queens(N, row, board):
    if row == N:
        return board  # Return the first valid solution found
    
    for col in range(N):
        if is_safe(board, row, col, N):
            board[row] = col
            result = solve_n_queens(N, row + 1, board)
            if result:  # If a solution is found, return it
                return result
    return None

def print_board(board):
    N = len(board)
    for row in range(N):
        line = ["." for _ in range(N)]
        line[board[row]] = "Q"
        print(" ".join(line))

# Define board size
N = 8  # Change this value for different board sizes
solution = solve_n_queens(N, 0, [-1] * N)

# Print the board
if solution:
    print_board(solution)
else:
    print("No solution found.")
