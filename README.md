# Softshell
SoftShell OS, A streamlined minimized OS written in Rust


## Building Binary

Custom Target:
`
cargo build --target thumbv7em-none-eabihf
`

For Operating System:
`
# Linux
cargo rustc -- -C link-arg=-nostartfiles
# Windows
cargo rustc -- -C link-args="/ENTRY:_start /SUBSYSTEM:console"
# macOS
cargo rustc -- -C link-args="-e __start -static -nostartfiles"
`

## Switching to Nighly for features
`
rustup override set nightly  
cargo build --target x86_64-softshell.json      
`