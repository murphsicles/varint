# varint — Variable-length integer encoding for Zeta

**Namespace:** `@serde/varint`

Unsigned LEB128 variable-length integer encoding and decoding.

## Usage

```zeta
use serde::varint::{encode, decode};

// Encode a u64 into a varint byte buffer
let buf: [i64; 10] = [0; 10];
let count: i64 = encode_u64(300, buf);

// Decode a varint from a byte buffer  
let (value, consumed): (i64, i64) = decode_u64(buf, 0);
```

## API

- `encode_u64(value, buf)` — encode a u64, returns bytes written
- `decode_u64(buf, index)` — decode a u64, returns (value, bytes consumed)

## Implementation

Transpiled from `unsigned-varint` v0.8.0 via dark-factory Rust-to-Zeta transpiler.

## License

MIT — The Zeta Foundation
