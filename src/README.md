# Project 1 Socket

## High-level Approach

The client employs a guessing strategy that begins with selecting a random word from a list of possible words. After each guess, the client refines its choices based on the feedback received from the server, limiting subsequent guesses to words containing letters that received a 1 or 2 mark (letters exist in correct answer).

## Challenges Faced

One of the challenges encountered during development was distinguishing between different port options and formulating a robust loop structure to continuously make guesses until receiving a "bye" message from the server.

## Code Structure

The code is organized into modular functions that handle specific tasks, such as sending messages, receiving responses, and processing guesses. The script utilizes command-line arguments to specify the server hostname, username, and optional parameters like the TCP port and TLS encryption.

## Testing

To ensure the client's functionality and robustness, various testing scenarios were considered. These tests included connecting to the sockets using all combinations of the different flags as well as manually providing the ports. I also made sure that different impossible values or errors are handled so the code doesn't crash!

## Usage

To run the script, use the following command:

```bash
./client [-p <port>] [-s] <hostname> <username> 
