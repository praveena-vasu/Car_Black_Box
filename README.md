# 🚗 Car Black Box

📜 Description

The Car Black Box is an Embedded C application designed to monitor, display, and store important vehicle-related events such as time, speed, gear/event status, and system activity.

This project works similar to a real vehicle black box, where important event data is recorded in memory for future analysis. The system displays real-time information on a CLCD, stores event logs in EEPROM, uses RTC for accurate time tracking, and supports log viewing, downloading, clearing, and time setting through a menu-based interface.

This project mainly focuses on real-time embedded system design, EEPROM-based data logging, RTC interfacing, ADC reading, keypad navigation, UART communication, and state-machine implementation.


🔷 Features

        * Real-Time Dashboard Display
        * Event Logging in EEPROM
        * View Stored Logs on CLCD
        * Download Logs through UART
        * Clear Stored Logs
        * Set Time using Matrix Keypad
        * ADC-Based Speed Reading
        * RTC-Based Real-Time Tracking
        * Menu-Driven User Interface
        * State-Machine Based Implementation


⚙️ Technologies Used

      * Embedded C
      * PIC Microcontroller
      * MPLAB X IDE
      * XC8 Compiler
      * CLCD Interfacing
      * Matrix Keypad
      * ADC
      * I2C Protocol
      * DS1307 RTC
      * EEPROM
      * UART Communication
      * Tera Term / Serial Terminal
      * Interrupt / Switch Handling


📍 Validation

    * Validates keypad inputs before changing events or menu options.
    * Ensures proper event logging only when event status changes.
    * Maintains accurate time using RTC before storing logs.
    * Stores logs safely in EEPROM for non-volatile memory backup.
    * Handles maximum log storage with rollover mechanism.
    * Displays proper messages when no logs are available.
    * Ensures stable dashboard updates without affecting menu operations.



▶️ How to Run

      1. Compile the Embedded C project using **MPLAB X IDE** with **XC8 Compiler**.
      2. Flash the code into the **PIC microcontroller**.
      3. Connect the required peripherals:
      
         * CLCD
         * Matrix Keypad
         * DS1307 RTC
         * EEPROM
         * ADC input
         * UART serial terminal
      4. Power ON the system.
      5. Monitor real-time dashboard data on CLCD.
      6. Use keypad switches to:
      
         * Change event/gear status
         * Open main menu
         * View logs
         * Download logs
         * Clear logs
         * Set time


🔶 Displayed Parameters

    ```text
    Time   : 12:30:45
    Event  : GN
    Speed  : 45 km/h
    ```



📂 Stored Log Format

    ```text
    LOG   TIME      EV  SP
    0     12:30:45  GN  45
    1     12:31:10  G1  52
    2     12:32:20  GR  20
    ```

Each log stores:

    * Time
    * Event/Gear Status
    * Speed



🔁 Project Workflow

    ```text
    System Power ON
            ↓
    Initialize CLCD, Keypad, ADC, RTC, EEPROM and UART
            ↓
    Display Dashboard
            ↓
    Read Time from RTC
            ↓
    Read Speed from ADC
            ↓
    Read Event Input from Keypad
            ↓
    If Event Changes, Store Log in EEPROM
            ↓
    If Menu Key Pressed, Open Main Menu
            ↓
    View Log / Download Log / Clear Log / Set Time
            ↓
    Return to Dashboard
```

🧠  State Machine Used


    The project is implemented using a state-machine approach.
    
    ```c
    e_dashboard
    e_main_menu
    e_view_log
    e_download_log
    e_clear_log
    e_set_time
    ```

    Using a state machine makes the project easier to organize, because each operation is handled as a separate state.


🔶 Events Used


    ```text
    ON  - System ON
    GN  - Gear Neutral
    G1  - Gear 1
    G2  - Gear 2
    G3  - Gear 3
    G4  - Gear 4
    G5  - Gear 5
    GR  - Gear Reverse
    C_  - Collision/Event Alert
    ```

📌 Applications


    * Vehicle event monitoring system
    * Accident/event analysis support
    * Driver activity tracking
    * Embedded data logging application
    * EEPROM and RTC-based monitoring system
    * Automotive embedded system learning project


📚 Key Learnings


    * Interfacing CLCD with PIC microcontroller
    * Reading analog speed input using ADC
    * Interfacing RTC using I2C protocol
    * Storing and retrieving logs from EEPROM
    * UART-based log downloading
    * Matrix keypad-based menu navigation
    * State-machine based embedded application design
    * Handling limited memory in embedded systems



 👩‍💻 Author

**Praveena**
