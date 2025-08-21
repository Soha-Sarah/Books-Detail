#  Library Management System (Python OOP)  
This is a simple Object-Oriented Programming (OOP) project in Python that demonstrates how a library system can manage books.  
It features classes for Book and Library, allowing users to add, issue, return, and display books.  

# Features  

- Add books to the library  
- Display all books with details (title, author, ISBN, availability)  
- Issue books by ISBN (updates availability)  
- Return books by ISBN
- 
## Handles cases where:

- Book is already issued  
- Book is not found  
- Book is not yet issued  

# Classes  

### Book:  

- Represents a single book  

• Attributes:

- Title  
- Author  
- ISBN  
- Available (boolean)  

#### Methods:  

- Display() → shows book details  
- Available() → checks availability  
- SetAvailability(status) → updates availability  
- GetIsbn() → returns the book’s ISBN  

### Library  

- Represents a collection of books  

• Attributes:

- books (list of Book objects)
  
#### Methods:

- AddBook(book) → adds a book  
- IssueBook(isbn) → issues a book  
- ReturnBook(isbn) → returns a book  
- DisplayBooks() → lists all books

# Example Usage:
```python
# Create books  
b1 = Book("1984", "George Orwell", "12345", True)  
b2 = Book("To Kill a Mockingbird", "Harper Lee", "54321", True)  

# Create library  
lib = Library()  

# Add books  
lib.AddBook(b1)  
lib.AddBook(b2)  

# Show all books  
lib.DisplayBooks()  

# Issue and return  
lib.IssueBook("12345")  
lib.DisplayBooks()  
lib.ReturnBook("12345")  
lib.DisplayBooks()  
```
## Output  
```python
Book added to the library
Book added to the library
The title of the book:  1984
The author of the book:  George Orwell
The ISBN of the book:  12345
Is the book available :  Yes
The title of the book:  To Kill a Mockingbird
The author of the book:  Harper Lee
The ISBN of the book:  54321
Is the book available :  Yes

Book issued successfully.
...
Book returned successfully.
```
