# CPS2231-Hospital_Management_System

Final project for **CPS 2231 Computer Programming** at Wenzhou-Kean University (Instructor: Prof. Wu).

A command-line hospital management system in Java, built around object-oriented design and binary serialization for persistent storage.

![UML diagram](HMS-UML.jpg)

## Features
- Doctor registration and login
- Patient consultation records entered by the attending doctor
- Billing for consultations through a `Tradable` interface
- Persistent storage of admin, doctor, and patient objects via `ObjectOutputStream` / `ObjectInputStream`

## Project structure
```
src/edu/wku/hospital/management/
├── frame/       HospitalManagementSystem (entry point and menus)
├── model/       Person, Doctor, Patient, Hospital, Tradable
├── service/     IOManager (serialization helpers)
└── exception/   NotFoundException, TransactionFailedException
tmp/             serialized data and system log, read at startup
```

## Running
```bash
javac -d out $(find src -name "*.java")
java -cp out edu.wku.hospital.management.frame.HospitalManagementSystem
```
Run from the repository root so the program can find `./tmp/`.

The slides used for the final presentation are in `Hospital Management System.pptx`.
