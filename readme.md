# Student Management Application (Java Swing)

This is a Java Swing desktop application for managing student records.

## Main Files (4 classes)

1. `src/bt_nhom5/GUI.java`
- Entry point of the program.
- Creates a `StudentManager` object and opens the main window (`MainFrame`).

2. `src/bt_nhom5/MainFrame.java`
- The main UI (`JFrame`) of the application.
- Displays student data in a table.
- Provides actions: Add, Edit, Delete, Search, Save, Open, Exit.
- Uses `StudentManager` for all data operations.

3. `src/bt_nhom5/Student.java`
- Data model class for a student.
- Fields: `ID`, `fullName`, `date`, `gender`, `GPA`.
- Includes getters/setters and `toString()` for display.

4. `src/bt_nhom5/StudentManager.java`
- Handles student list operations and file persistence.
- Loads default data from `students.txt` when initialized.
- Saves automatically after add/remove operations.
- Supports loading/saving from custom `.txt` files.

## Data Format

Student records are saved in text format as one line per student:

`ID,FullName,dd/MM/yyyy,Gender,GPA`

Example:

`SV001,Nguyen Van A,15/09/2004,Male,3.45`

## How To Run

### Option 1: NetBeans

1. Open the project folder in NetBeans.
2. Run the project.
3. The app starts from `bt_nhom5.GUI`.

### Option 2: Command Line

From project root:

```bash
javac -d out src/bt_nhom5/*.java
java -cp out bt_nhom5.GUI
```

## Notes

- Date format must be `dd/MM/yyyy`.
- GPA must be a valid number.
- Default storage file is `students.txt` (in the working directory).
- The table is sorted by GPA descending.
