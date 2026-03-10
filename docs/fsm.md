# Finite State Machine Definition

## States

1. NS_GREEN
2. NS_YELLOW
3. ALL_RED_1
4. EW_GREEN
5. EW_YELLOW
6. ALL_RED_2

## State Description

### NS_GREEN
North-South traffic is allowed to move.

### NS_YELLOW
North-South traffic prepares to stop.

### ALL_RED_1
Both directions stopped for safety buffer.

### EW_GREEN
East-West traffic allowed to move.

### EW_YELLOW
East-West traffic prepares to stop.

### ALL_RED_2
Safety buffer before returning to NS_GREEN.

## State Transitions

NS_GREEN → NS_YELLOW  
NS_YELLOW → ALL_RED_1  
ALL_RED_1 → EW_GREEN  
EW_GREEN → EW_YELLOW  
EW_YELLOW → ALL_RED_2  
ALL_RED_2 → NS_GREEN