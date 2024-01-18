
import random
class SuperComputer:
    def __init__(self):
        self.dice = [1, 2, 3, 4, 5, 6]
        self.thesaurus = {
            "happy": ["joyful", "delighted", "content"],
            "sad": ["unhappy", "depressed", "gloomy"],
            # Add more words and synonyms as needed
        }
        self.songs = []
        self.poems = []
        self.dictionary = {}
    
    def roll_dice(self):
        return random.choice(self.dice)
    
    def make_palindrome(self, word):
        return word + word[::-1]
    
    def calculate(self, expression):
        try:
            return eval(expression)
        except:
            return "Invalid expression"
    
    def generate_song(self):
        # Generate a song using AI logic
        song = "This is a generated song."
        self.songs.append(song)
        return song
    
    def generate_poem(self):
        # Generate a poem using AI logic
        poem = "This is a generated poem."
        self.poems.append(poem)
        return poem
    
    def add_word_to_dictionary(self, word, definition):
        self.dictionary[word] = definition
    
    def get_synonyms(self, word):
        if word in self.thesaurus:
            return self.thesaurus[word]
        else:
            return "No synonyms found for the given word."
    
    def run(self):
        while True:
            print("1. Roll Dice")
            print("2. Make Palindrome")
            print("3. Calculate")
            print("4. Generate Song")
            print("5. Generate Poem")
            print("6. Add Word to Dictionary")
            print("7. Get Synonyms")
            print("8. Exit")
            
            choice = input("Enter your choice: ")
            
            if choice == "1":
                print("Dice rolled:", self.roll_dice())
            elif choice == "2":
                word = input("Enter a word: ")
                print("Palindrome:", self.make_palindrome(word))
            elif choice == "3":
                expression = input("Enter an expression: ")
                print("Result:", self.calculate(expression))
            elif choice == "4":
                print("Generated Song:", self.generate_song())
            elif choice == "5":
                print("Generated Poem:", self.generate_poem())
            elif choice == "6":
                word = input("Enter a word: ")
                definition = input("Enter the definition: ")
                self.add_word_to_dictionary(word, definition)
                print("Word added to dictionary.")
            elif choice == "7":
                word = input("Enter a word: ")
                print("Synonyms:", self.get_synonyms(word))
            elif choice == "8":
                print("Exiting...")
                break
            else:
                print("Invalid choice. Please try again.")

# Create an instance of the SuperComputer class
computer = SuperComputer()

# Run the program
computer.run()
