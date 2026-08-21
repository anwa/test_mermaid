# test_mermaid

graph TD;
    A[THREE-PHASE AC SOURCE] -->|L1| B[R4875G1 Module 1]
    A -->|L2| C[R4875G1 Module 2]
    A -->|L3| D[R4875G1 Module 3]
    
    B -->|CAN-H / CAN-L| E[PARALLEL]
    C -->|CAN-H / CAN-L| E
    D -->|CAN-H / CAN-L| E
    
    E -->|DC +| F[48–58 V BATTERY / DC BUS]
    
    F -->|CAN| G[3.3 V CAN transceiver]
    
    G --> H[ESP32-S3-WROOM N16R8]
    H -->|ESPHome| I[ESPHome]
    H -->|Rotary encoder| J[Rotary encoder]
    H -->|ILI9488 TFT| K[ILI9488 TFT]
    H -->|Home Assistant API| L[Home Assistant API]
    H -->|MQTT| M[MQTT]
    H -->|ESPHome Web UI| N[ESPHome Web UI]
