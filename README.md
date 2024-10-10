# DependencyPractice

This repository demonstrates **Dependency Injection** (DI) in ASP.NET Core 8 using simple class-based examples. The project showcases how to implement DI through **Constructor Injection**, enabling loose coupling between classes.

## Project Structure

The project consists of the following main components:

### 1. **IOgretmen Interface**

The `IOgretmen` interface defines the contract for the `Teacher` class. It includes:
- `FirstName`: The teacher's first name.
- `LastName`: The teacher's last name.
- `GetInfo()`: A method that returns the teacher's full name.

### 2. **Teacher Class**

The `Teacher` class implements the `IOgretmen` interface and provides the following:
- `FirstName`: Stores the teacher's first name.
- `LastName`: Stores the teacher's last name.
- `GetInfo()`: Returns the teacher’s full name as a string.

### 3. **ClassRoom Class**

The `ClassRoom` class depends on the `IOgretmen` interface and retrieves teacher information through DI:
- Constructor injection of a `Teacher` object.
- `GetTeacherInfo()`: Calls the `GetInfo()` method of the injected `Teacher` instance to return teacher details.

