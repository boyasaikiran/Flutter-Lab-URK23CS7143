# Flutter Experiments - Complete Laboratory Suite

A collection of nine standalone Flutter experiments covering core widgets and
layouts, responsive interfaces, interactive input, form validation, navigation,
and data persistence with SQLite and Google Cloud Firestore.

Each experiment is an independent Flutter project. Open its project directory
in **VS Code** or **Android Studio**, or run it from the Flutter CLI. The
repository root is not itself a Flutter project.

---

## Table of Experiments

| # | Experiment | Key Concepts | Project |
|---|---|---|---|
| 01 | [Building Applications Using Flutter](#experiment-1-building-applications-using-flutter) | Reusable widgets, layouts, asset images | [Project](./Experiment1/Building-Applications-using-Flutter/) |
| 02 | [Adaptive and Responsive UI Design](#experiment-2-adaptive-and-responsive-ui-design) | `LayoutBuilder`, responsive `GridView`, breakpoints | [Project](./Experiment2/Adaptive-and-Responsive-UI-Design/) |
| 03 | [Add Interactivity to App Input and Forms](#experiment-3-add-interactivity-to-app-input-and-forms) | `TextField`, `TextEditingController`, live filtering | [Project](./Experiment3/Add-Interactivity-to-App-Input-and-Forms/) |
| 04 | [Form Validation Using Stateful Widgets](#experiment-4-form-validation-using-stateful-widgets) | `Form`, `TextFormField`, validation, state | [Project](./Experiment4/Form-Validation-using-Stateful-Widgets/) |
| 05 | [Implementation of Navigation and Routing](#experiment-5-implementation-of-navigation-and-routing) | Named routes, screen navigation, student results | [Project](./Experiment5/Implementation-of-Navigation-and-Routing/) |
| 06 | [Data Persistence Using SQLite](#experiment-6-data-persistence-using-sqlite) | SQLite, local records, asynchronous database access | [Project](./Experiment6/Data-Persistence-using-SQLite/) |
| 07 | [Data Persistence Using Google Cloud Firestore](#experiment-7-data-persistence-using-google-cloud-firestore) | Firebase, Firestore writes, student records | [Project](./Experiment7/Data-Persistence-Using-Google-Cloud-Firestore/) |
| 08 | [Searching Information in Google Firestore Database](#experiment-8-searching-information-in-google-firestore-database) | Firestore queries, record search | [Project](./Experiment8/Searching-Information-in-Google-Firestore-Database/) |
| 09 | [Update Information in Google Firestore Database](#experiment-9-update-information-in-google-firestore-database) | Firestore document lookup and update | [Project](./Experiment9/Update-Information-in-Google-Firestore-Database/) |

---

## Experiment Details

### Experiment 1: Building Applications Using Flutter

Build a fruit-market list that introduces Flutter's widget tree and common
layout widgets.

- Displays fruit names, descriptions, prices, and local images.
- Uses a reusable `FruitItem` widget for each fruit card.
- Demonstrates `ListView`, `Card`, `Row`, `Column`, and image assets.
- **Primary files:** `lib/main.dart`, `assets/images/`, `pubspec.yaml`
- **[Project README](./Experiment1/Building-Applications-using-Flutter/README.md)**

### Experiment 2: Adaptive and Responsive UI Design

Create a product catalog whose grid adapts its number of columns to the
available screen width.

- Uses `LayoutBuilder` to determine the available width.
- Displays two columns on compact layouts, three on medium layouts, and four
  on wider layouts.
- Uses a reusable `ProductCard` and sample product data.
- The **Add to Cart** button is a visual placeholder.
- **Primary file:** `lib/main.dart`
- **[Project README](./Experiment2/Adaptive-and-Responsive-UI-Design/README.md)**

### Experiment 3: Add Interactivity to App Input and Forms

Build a simple product search screen that filters a built-in fruit list as the
user types.

- Uses a `TextEditingController` to observe search input.
- Filters results without regard to letter case.
- Provides a clear-search button and a no-results message.
- **Primary file:** `lib/main.dart`
- **[Project README](./Experiment3/Add-Interactivity-to-App-Input-and-Forms/README.md)**

### Experiment 4: Form Validation Using Stateful Widgets

Create a car mileage calculator with validated distance and fuel inputs.

- Uses a `Form`, `GlobalKey<FormState>`, and `TextFormField` validators.
- Requires positive numeric values for distance and fuel.
- Calculates mileage in kilometers per liter and shows an efficiency rating.
- **Primary file:** `lib/main.dart`
- **[Project README](./Experiment4/Form-Validation-using-Stateful-Widgets/README.md)**

### Experiment 5: Implementation of Navigation and Routing

Collect student details on one screen and display calculated results on
another using named routes.

- Separates the entry form, results screen, and student data model.
- Passes student details between screens and displays performance results.
- **Primary files:** `lib/main.dart`, `lib/home_screen.dart`,
  `lib/second_screen.dart`, `lib/user_data_model.dart`
- **[Project README](./Experiment5/Implementation-of-Navigation-and-Routing/README.md)**

### Experiment 6: Data Persistence Using SQLite

Save and display student records in a local SQLite database.

- Validates student details and marks before saving.
- Stores records with a unique registration number.
- Loads saved records from SQLite; the project also includes a web SQLite
  implementation.
- **Primary file:** `lib/main.dart`
- **[Project README](./Experiment6/Data-Persistence-using-SQLite/README.md)**

### Experiment 7: Data Persistence Using Google Cloud Firestore

Connect a Flutter app to Firestore to create and display student records.

- Saves records to the `students` collection using the uppercased registration
  number as the document ID.
- Displays Firestore-backed records and reports read/write errors.
- Requires a Firebase project and local app configuration.
- **Primary files:** `lib/main.dart`, `lib/firebase_options.dart`,
  `firebase_config.example.json`
- **[Project README](./Experiment7/Data-Persistence-Using-Google-Cloud-Firestore/README.md)**

### Experiment 8: Searching Information in Google Firestore Database

Find student records in Firestore by student name or registration number.

- Queries the `students` collection for exact name and registration-number
  matches.
- Shows loading, no-result, and error states.
- Requires Firebase configuration and student records in Firestore.
- **Primary files:** `lib/main.dart`, `lib/firebase_options.dart`,
  `firebase_config.example.json`
- **[Project README](./Experiment8/Searching-Information-in-Google-Firestore-Database/README.md)**

### Experiment 9: Update Information in Google Firestore Database

Load an existing student record and update its editable fields in Firestore.

- Looks up a record by registration number.
- Allows updating the student's name, department, and marks.
- Validates updates and reports missing records or Firestore errors.
- **Primary files:** `lib/main.dart`, `lib/firebase_options.dart`,
  `firebase_config.example.json`
- **[Project README](./Experiment9/Update-Information-in-Google-Firestore-Database/README.md)**

---

## Getting Started

### Prerequisites

- Flutter SDK installed and configured. Run `flutter doctor` to check your
  setup.
- A device, emulator, browser, or other target supported by the selected
  project.
- Firebase project configuration for Experiments 7, 8, and 9.

Check each experiment's README for its specific SDK and platform requirements.

### Run an Individual Experiment

Change to that experiment's Flutter project directory before running Flutter
commands. For example, in PowerShell:

```powershell
Set-Location .\Experiment1\Building-Applications-using-Flutter
flutter pub get
flutter devices
flutter run
```

Use the project links in the table above to find the correct directory for
another experiment. To run its tests and static analysis, from that same
directory use:

```powershell
flutter test
flutter analyze
```

Some projects have extra setup steps; follow the linked project README.

### Open in VS Code or Android Studio

Open an individual experiment project directory (the directory containing
`pubspec.yaml`) for the best IDE support, including Dart analysis, debugging,
and hot reload. You can also open the repository root and work with each
experiment in its own terminal.

---

## Repository Structure

```text
Flutter Lab/
├── README.md
├── Experiment1/
│   └── Building-Applications-using-Flutter/
│       ├── assets/images/
│       ├── lib/main.dart
│       └── pubspec.yaml
├── Experiment2/
│   └── Adaptive-and-Responsive-UI-Design/
│       ├── lib/main.dart
│       └── pubspec.yaml
├── Experiment3/
│   └── Add-Interactivity-to-App-Input-and-Forms/
│       ├── lib/main.dart
│       └── pubspec.yaml
├── Experiment4/
│   └── Form-Validation-using-Stateful-Widgets/
│       ├── lib/main.dart
│       └── pubspec.yaml
├── Experiment5/
│   └── Implementation-of-Navigation-and-Routing/
│       ├── lib/
│       └── pubspec.yaml
├── Experiment6/
│   └── Data-Persistence-using-SQLite/
│       ├── lib/main.dart
│       └── pubspec.yaml
├── Experiment7/
│   └── Data-Persistence-Using-Google-Cloud-Firestore/
│       ├── firebase_config.example.json
│       ├── lib/
│       └── pubspec.yaml
├── Experiment8/
│   └── Searching-Information-in-Google-Firestore-Database/
│       ├── firebase_config.example.json
│       ├── lib/
│       └── pubspec.yaml
└── Experiment9/
    └── Update-Information-in-Google-Firestore-Database/
        ├── firebase_config.example.json
        ├── lib/
        └── pubspec.yaml
```

Each experiment is maintained as a separate Flutter app, with its own
dependencies, source, and (where provided) tests and platform folders.

---

## Firebase Configuration and Data Safety

Experiments 7–9 use Firebase Cloud Firestore. Each project includes a
`firebase_config.example.json` template and instructions for configuring a
Firebase app. Follow the individual README for setup and run commands.

The apps do not implement user authentication. Do not use unrestricted
Firestore rules with student data. Configure authentication and appropriate
Firestore security rules before using real data. Firebase client configuration
is not a substitute for security rules; never add service-account credentials
or other server secrets to a Flutter app.
