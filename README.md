# PowerQuarry-BLE-Handler
The LiFePO4 batteries manufactured by Shentec can be monitored using the "Power Quarry" Bluetooth app, available for both Android and iOS. The app provides detailed battery information, including individual cell voltages, battery current, battery temperature, charge/discharge status, cycle count, and the current state of charge (SoC).

This project demonstrates how the same information can be accessed directly from ESPHome via Bluetooth Low Energy (BLE). The BLE communication protocol used by the battery was reverse-engineered from the Power Quarry app and implemented natively in ESPHome.

Since the battery only supports a single BLE connection at a time, the ESP establishes a connection, reads the required data, and then disconnects again. This allows the official Power Quarry app to be used in parallel without interference. If desired, the ESP can also maintain a permanent connection to the battery.

The implementation provides access to battery voltage, current, power, state of charge (SoC), individual cell voltages, temperatures, operating status, cycle count, and other diagnostic information, making it easy to integrate the battery into Home Assistant via ESPHome.
