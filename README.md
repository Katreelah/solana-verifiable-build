# Solana Verifiable Build 🛠️🔐  
**CLI tool for deterministic builds and on-chain verification of Solana programs and buffer accounts.**  
Built by [Ellipsis Labs](https://github.com/Ellipsis-Labs) — maintained by `maintainers@ellipsislabs.xyz`  
L## Table of Contents  
- [Overview](#overview)  
- [Installation](#installation)  
- [Usage](#usage)  
- [Build Verification Flow](#build-verification-flow)  
- [Examples](#examples)  
- [Docker Support](#docker-support)  
- [Troubleshooting](#troubleshooting)  
- [Contributing](#contributing)  
- [License](#license)
-  ## Build Verification Flow  
1. ✅ Build your Solana program locally using `solana-verifiable-build`  
2. 📦 Upload build metadata to chain (program or buffer account)  
3. 🔍 Trigger remote verification job  
4. 📄 Compare local build hash vs on-chain hash  
5. 🧾 Confirm deterministic match or log mismatch
6.  ## Examples  
Run the Hello World demo:  
```bash
cargo run --example hello_world

---

Would you like me to generate a full README draft with overlays and captions next? Or do you want to start with a visual checklist for the verification flow?





## Quick Start

1. Install prerequisites:

   - Docker
   - Cargo
   - Solana Verify CLI (`cargo install solana-verify`)

2. Build your program:

```bash
solana-verify build
```

3. Deploy and verify:

```bash
# Deploy
solana program deploy -u $NETWORK_URL target/deploy/$PROGRAM_LIB_NAME.so --program-id $PROGRAM_ID

# Verify against repository -> upload your build data on chain
solana-verify verify-from-repo -u $NETWORK_URL --program-id $PROGRAM_ID https://github.com/$REPO_PATH

# Trigger a remote job
solana-verify remote submit-job --program-id $PROGRAM_ID --uploader $THE_PUBKEY_THAT_UPLOADED_YOUR_BUILD_DATA
```

## Documentation

For detailed instructions and best practices, please refer to the [official Solana documentation on verified builds](https://solana.com/developers/guides/advanced/verified-builds).

## Security Considerations

While verified builds enhance transparency, they should not be considered a complete security solution. Always:

- Review the source code
- Use trusted build environments
- Consider using governance solutions for program upgrades

For responsible disclosure of bugs related to verified builds CLI, please email maintainers@ellipsislabs.xyz with a detailed description of the attack vector.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.
