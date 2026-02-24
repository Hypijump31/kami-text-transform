# kami-text-transform

[![KAMI Plugin](https://img.shields.io/badge/KAMI-plugin-8A2BE2)](https://github.com/Hypijump31/KAMI)
[![Signed](https://img.shields.io/badge/Ed25519-signed-green)](https://github.com/Hypijump31/kami-registry)

Transform text: case conversion, slugify, truncate, word count, and more.

## Install

```bash
kami install Hypijump31/kami-text-transform@v0.1.0
```

## Usage

```bash
# Uppercase
kami exec dev.kami.text-transform '{"action": "uppercase", "text": "hello world"}'

# Slugify
kami exec dev.kami.text-transform '{"action": "slugify", "text": "Hello World! How are you?"}'

# Word count
kami exec dev.kami.text-transform '{"action": "word_count", "text": "The quick brown fox"}'

# Truncate
kami exec dev.kami.text-transform '{"action": "truncate", "text": "Long text here", "max_length": 8}'
```

## Actions

`uppercase` | `lowercase` | `titlecase` | `snake_case` | `camel_case` | `pascal_case` | `kebab_case` | `slugify` | `truncate` | `trim` | `reverse` | `word_count`

## Arguments

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `action` | string | yes | Transformation to apply (see above) |
| `text` | string | yes | Text to transform |
| `max_length` | number | no | Maximum length (required for `truncate`) |

## Build from source

```bash
git clone https://github.com/Hypijump31/kami-text-transform
cd kami-text-transform
cargo build --target wasm32-wasip2 --release
```

## Security

- Filesystem: none
- Network: none
- Max memory: 16 MB
- Max execution: 1000 ms

## License

MIT
