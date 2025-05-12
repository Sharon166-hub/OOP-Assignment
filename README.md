# OOP-Assignment
# Parent class: Book
class Book:
    def __init__(self, title, author, pages):
        self.title = title
        self.author = author
        self.pages = pages

    def read(self):
        return f"Reading {self.title} by {self.author}."

    def get_description(self):
        return f"{self.title} is a book written by {self.author} with {self.pages} pages."

class Ebook(Book):
    def __init__(self, title, author, pages, file_size):
        super().__init__(title, author, pages)  
        self.file_size = file_size  

    def download(self):
        return f"Downloading {self.title} ({self.file_size} MB)..."

    def get_description(self):
        return f"{self.title} is an Ebook by {self.author}, with {self.pages} pages and a file size of {self.file_size} MB."

book = Book("1998", "George Orwell", 328)
ebook = Ebook("Digital Fortress", "Dan Brown", 400, 2.5)


print(book.get_description())  
print(book.read()) 

print(ebook.get_description())  
print(ebook.download())  
