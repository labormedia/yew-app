# Make sure to match the os requirements
sudo apt install libssl-dev
cargo install wasm-pack
wasm-pack build --target web --out-name wasm --out-dir ./static

# Check the web file on a server
cargo install miniserve
miniserve ./static --index index.html