# Project Setup

## Setup

- Create new folder
- rustup default nightly
- cargo init .
- cargo add rocket     
- cargo isntall cargo-watch
- cargo add rocket_contrib
- cargo add serde
- cargo add serde_json

## Make some changes to cargo.toml

### Before

```toml
rocket = "0.4.11"
rocket_contrib = "0.4.11"
rusqlite = "0.27.0"
serde = "1.0.137"
serde_json = "1.0.82"
```

### After

```toml
rocket = "0.4.11"
rocket_contrib = {version="0.4.11", features=["json"]}
rusqlite = {version= "0.27.0", features= ["bundled"]}
serde = {version="1.0.137", features=["derive"]}
serde_json = "1.0.82"
```




## Runing The Server
```bash
cargo watch -x run 
```
