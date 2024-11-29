


Here is how to use the **`colorama`** library to include color-coded debug messages in Python.

### Installation:
First, install the `colorama` library:
```bash
pip install colorama
```

### Usage:
The `colorama` library provides a simple way to add colors to text in the console. Here’s how you can use it:

```python
from colorama import Fore, Back, Style, init

# Initialize colorama (to ensure it works on all platforms)
init(autoreset=True)

# Example usage
print(Fore.RED + "This is an error message!")  # Red text
print(Fore.GREEN + "This is a success message!")  # Green text
print(Fore.YELLOW + "This is a warning message!")  # Yellow text
print(Fore.CYAN + "This is an informational message!")  # Cyan text
print(Back.MAGENTA + "This has a magenta background!")  # Magenta background
print(Style.BRIGHT + "This is bright text!")  # Bright text
```

### Explanation of `colorama` Components:
- **`Fore`**: Sets the text color.
  - Options: `RED`, `GREEN`, `YELLOW`, `CYAN`, `MAGENTA`, etc.
- **`Back`**: Sets the background color.
  - Options: `BLACK`, `RED`, `GREEN`, `YELLOW`, `BLUE`, `MAGENTA`, etc.
- **`Style`**: Adjusts text style.
  - Options: `BRIGHT`, `DIM`, `NORMAL`.

### Adding `colorama` to Your Code:
Here’s how the provided code uses `colorama` for color-coded debugging:

```python
from colorama import Fore, Style, init

# Initialize colorama
init(autoreset=True)

def fetch_and_filter_data():
    try:
        print(Fore.CYAN + "DEBUG: Starting database connection...")
        # Simulate a database connection
        print(Fore.GREEN + "DEBUG: Successfully connected to the database.")

        # Simulating fetching data
        print(Fore.CYAN + "DEBUG: Fetching data from the database...")
        # Assume data fetched here
        print(Fore.GREEN + "DEBUG: Data fetched successfully.")

        # Simulating filtering data
        print(Fore.CYAN + "DEBUG: Filtering rows...")
        # Assume filtering is done
        print(Fore.YELLOW + "DEBUG: Rows remaining after filtering: 100")

        # Simulating success in saving to Excel
        print(Fore.GREEN + "DEBUG: Data successfully saved to Excel.")
        
    except Exception as e:
        print(Fore.RED + "ERROR: An unexpected error occurred!")
        print(Fore.RED + f"DETAILS: {e}")

# Run the function
fetch_and_filter_data()
```

### Output:
```
DEBUG: Starting database connection... (CYAN)
DEBUG: Successfully connected to the database. (GREEN)
DEBUG: Fetching data from the database... (CYAN)
DEBUG: Data fetched successfully. (GREEN)
DEBUG: Filtering rows... (CYAN)
DEBUG: Rows remaining after filtering: 100 (YELLOW)
DEBUG: Data successfully saved to Excel. (GREEN)
```

This makes your script more **readable** and helps in **debugging** effectively by categorizing messages with colors.


