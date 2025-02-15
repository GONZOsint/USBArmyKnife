# Example - Payload Selector

This script provides a user interface for selecting and executing one of several payloads. It displays an image, a menu of payload options, and allows you to cycle through them using button presses.

## Features

- **Startup Sequence:** Displays an image and initializes the UI.
- **Payload Menu:** Lists available payloads with a count and allows selection.
- **Button Interaction:**
  - **Short Press:** Cycles through the payload options (LED flashes green).
  - **Long Press:** Executes the selected payload (LED turns red during execution).
- **LED Feedback:** Uses different LED colors to indicate the current state (blue for idle, green for cycling, red for execution).

## How to Use

1. **Load the Script:** Upload the script to your device.
2. **Cycle Payloads:** Use a short button press to navigate through the payload list.
3. **Run Payload:** Hold the button (long press) to execute the selected payload.
4. **Restart:** The script automatically restarts the payload selection after execution.

## Adding More Payload Files

To add additional payload files to the UI, follow these steps:

1. **Define the Payload:**
   - Add a new `DEFINE` statement at the top of the script. For example:
     ```plaintext
     DEFINE #PAYLOAD_8 new_payload.ds
     ```
2. **Update the Loop Condition:**
   - Increase the number in the `WHILE` loop condition to reflect the new total (e.g., change `< 7` to `< 8`).
3. **Display Section:**
   - Add a new `ELSE IF` block to display the new payload in the menu.
4. **Execution Section:**
   - Add a new `ELSE IF` block to execute the new payload when selected.
5. **Update UI Text:**
   - Ensure that the payload count and display texts are updated accordingly.

