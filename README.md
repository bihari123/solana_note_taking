# solana_note_taking

# Compressed Notes

## Overview

Compressed Notes is a Solana program that demonstrates the use of generalized state compression. This project implements a basic note-taking application where notes are stored in a compressed format using a Merkle tree structure. The program showcases efficient on-chain storage and management of data using the SPL Account Compression program.

## Features

- Create a new Merkle tree for storing compressed notes
- Add new notes to the Merkle tree
- Update existing notes
- Efficient on-chain storage using state compression techniques

## Prerequisites

- Rust and Cargo
- Solana CLI
- Node.js and npm
- Anchor Framework

## Installation

1. Clone the repository:
   ```
   git clone https://github.com/your-username/compressed-notes.git
   cd compressed-notes
   ```

2. Install dependencies:
   ```
   npm install
   ```

3. Build the program:
   ```
   anchor build
   ```

## Usage

1. Start a local Solana validator:
   ```
   solana-test-validator
   ```

2. Run the tests:
   ```
   anchor test
   ```

## Program Structure

- `lib.rs`: Contains the main program logic, including instruction handlers for creating a note tree, appending notes, and updating notes.
- `utils.ts`: Utility functions for client-side operations, including hash generation and note log retrieval.

## Key Components

- `NoteLog`: Struct representing a note in the system, including the leaf node hash, owner's public key, and the note content.
- `NoteAccounts`: Struct defining the accounts required for note operations.
- `create_note_tree`: Instruction to initialize a new Merkle tree for storing notes.
- `append_note`: Instruction to add a new note to the Merkle tree.
- `update_note`: Instruction to update an existing note in the Merkle tree.

## Testing

The project includes several tests to verify the functionality of the program:

1. Creating a new note tree
2. Adding a note to the Merkle tree
3. Adding a maximum-size note to the Merkle tree
4. Updating an existing note in the Merkle tree

Run the tests using `anchor test`.

## Resources

- [Solana Developers Course: State Compression](https://solana.com/developers/courses/state-compression/generalized-state-compression)
- [SPL Account Compression Program](https://spl.solana.com/account-compression)

## License

[MIT License](LICENSE)

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.
