# Discord Token Onliner

This Python script brings Discord tokens online using WebSocket connections and keeps them alive to appear online on Discord. It validates tokens, maintains WebSocket sessions, and uses multi-threading to handle multiple tokens simultaneously.

## Features

- **Token Validation**: Ensures that each token is valid before attempting to bring it online.
- **WebSocket Connection**: Uses Discord’s WebSocket gateway to keep tokens online.
- **Multi-threading**: Handles multiple tokens concurrently to keep them all online.
- **Console Output**: Displays a real-time console output with color-coded statuses for each token.

## Requirements

- Python 3.x
- Required Libraries:
  - `colorama` for colored console output
  - `websocket-client` for WebSocket connections
  - `pystyle` for styled printing in the terminal

## How to Use

1. **Install Dependencies**:
   - If the script detects that `colorama` or `websocket-client` is missing, it will automatically install them. You can also manually install the required packages by running:
     ```bash
     pip install colorama websocket-client pystyle
     ```

2. **Prepare Your Tokens**:
   - Place your tokens in a `tokens.txt` file, with each token on a new line.

3. **Run the Script**:
   - Simply run the Python script:
     ```bash
     python main.py
     ```

4. **Watch It Go**:
   - The script will output the status of each token as it comes online, showing whether the token is valid or if any errors occur.

## How It Works

- **Token Validation**: The script first checks if each token is valid using a simple API request to Discord.
- **WebSocket Connection**: If valid, the token is connected to Discord’s WebSocket server, and a keep-alive message is sent at regular intervals to maintain the online status.
- **Logging**: All token activities are printed to the console in real-time, with different color codes indicating the status.

## Notes

- Make sure your `tokens.txt` file is correctly formatted with valid Discord tokens.
- The script handles multiple tokens at once, allowing you to bring several accounts online simultaneously.
