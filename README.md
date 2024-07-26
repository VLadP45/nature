# nature# Rainbow Text Printer

def print_rainbow(text):
    """
    Print the given text in rainbow colors.
    """
    # ANSI escape codes for rainbow colors
    colors = [
        '\033[91m',  # Red
        '\033[93m',  # Yellow
        '\033[92m',  # Green
        '\033[96m',  # Cyan
        '\033[94m',  # Blue
        '\033[95m',  # Magenta
        '\033[0m'    # Reset to default
    ]

    for i, char in enumerate(text):
        color = colors[i % len(colors)]
        print(f"{color}{char}", end="")
    print("\033[0m")  # Reset to default color at the end

def main():
    """
    Main function to run the rainbow text printer.
    """
    text = "This is a rainbow text!"
    print_rainbow(text)

if __name__ == "__main__":
    main()
