# SCL Go SDK (SCL:V1)

This repository contains the **official Go SDK** for SCL:V1.

The SDK provides:
- Canonical parser
- Canonical validator
- Canonical runtime engine
- Canonical JSON serialization
- Deterministic golden-hash computation
- Guaranteed bit-for-bit parity with the Python and JavaScript SDKs

The Go implementation is the **reference implementation** used during protocol freezing and parity validation.

## Repository Structure

scl-go/
  src/        # SDK implementation (main.go placeholder)
  tests/      # Conformance and parity tests
  README.md
  LICENSE
  CHANGELOG.md

## Installation

Go module installation (public after launch):

go get github.com/scl-protocol/scl-go

Local development:

go build ./...
go test ./...

## Guarantees

The Go SDK must:
1. Parse exactly according to PARSER_CONTRACT_V1.md
2. Validate exactly according to VALIDATION_CONTRACT_V1.md
3. Execute runtime behavior exactly as defined in RUNTIME_CONTRACT_V1.md
4. Serialize AST and runtime output exactly as in CANONICAL_JSON_V1.md
5. Compute golden hashes exactly as in ENGINE_V1_CONTRACT.md
6. Match Python and JS outputs with zero divergence

Any deviation is a protocol violation.

## Contributing

The SCL:V1 specification is frozen.  
See the main spec repository for the contribution rules.

## License

See LICENSE for usage terms.
