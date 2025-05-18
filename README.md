# Circom Multiply Project

This project demonstrates a simple circuit written in [Circom](https://docs.circom.io/) for multiplying two numbers.

## Files

- `multiply.circom`: The main Circom circuit file that defines the multiplication logic.
- `README.md`: This file. Project overview and usage instructions.

## Prerequisites

- [Node.js](https://nodejs.org/)
- [Circom](https://docs.circom.io/getting-started/installation/)
- [SnarkJS](https://github.com/iden3/snarkjs)

## Usage

1. **Compile the circuit:**
   ```sh
   circom multiply.circom --r1cs --wasm --sym
   ```
2. **Generate witness:**
   ```sh
   node multiply_js/generate_witness.js multiply_js/multiply.wasm input.json witness.wtns
   ```
3. **Generate proof and verify:**
   Follow the [Circom documentation](https://docs.circom.io/) for proof generation and verification steps using SnarkJS.

## Example `input.json`
```json
{
  "a": 3,
  "b": 11
}
```

## License

MIT License
