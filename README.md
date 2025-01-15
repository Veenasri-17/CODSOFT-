import random
import string

def generate_password(length):
    if length < 1:
        return "Password length must be at least 1."
    
    # Define character pools
    characters = string.ascii_letters + string.digits + string.punctuation

    # Generate random password
    password = ''.join(random.choice(characters) for _ in range(length))
    return password

def main():
    try:
        # User input for password length
        length = int(input("Enter the desired length of the password: "))
        
        # Generate and display password
        password = generate_password(length)
        print(f"Generated Password: {password}")
    except ValueError:
        print("Invalid input! Please enter a valid number.")

if __name__ == "__main__":
    main()
