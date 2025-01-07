# Solana Ultra-Fast New Token Sniper on Raydium and Pump.fun in Rust 🚀

## Overview

Introducing the **Solana Ultra-Fast New Token Sniper** written in **Rust** 🦀, designed to detect newly launched tokens on both **Raydium** and **Pump.fun** and execute buys at lightning speed ⚡. With Rust's memory safety features and performance optimizations, our sniper ensures a secure and ultra-fast experience, giving you the edge in the competitive world of DeFi trading.

### Key Features:

- **Speed and Efficiency**: Harness the power of Rust, known for its exceptional performance, enabling you to snipe new tokens almost instantly. No more delays—be the first to act! 🏎️💨
  
- **Safety First**: Rust's safety guarantees minimize bugs and vulnerabilities, ensuring your trading activities remain secure. Trade with peace of mind! 🔒

- **Multiple gRPC Connections**: Seamlessly connect to leading Solana data providers like **Helius** and **Yellowstone** through various gRPC connections, ensuring you receive real-time updates and insights for making informed trading decisions 📈.

- **User-Friendly Interface**: The sniper comes with an intuitive interface, making it accessible for both novice and experienced traders alike. Get up and running quickly! 👩‍💻👨‍💻

- **High-Level Customization**: Tailor your trading strategy with custom settings, including buy limits and token filters, optimizing your chances of securing those coveted early buys. 🎯

## Directory Structure

```
src/
├── core/
│   ├── token.rs        # Token definitions and handling
│   └── tx.rs        # Transaction handling
| 
├── engine/
│   ├── swap.rs        # Token swap(buy/sell) functionalities in some dex
│   └── monitor.rs        # New token monitoring in some dex
|
├── dex/
│   ├── pump_fun.rs        # Pump.fun dex
│   └── raydium.rs        # Raydium dex
│
├── services/
│   └── jito.rs        # Jito service provides ultra-fast transaction confirmation
|
├── common/
│   ├── logger.rs        # Logs to be clean and convenient to monitor.
│   └── utils.rs        # Utility functions used across the project
│
├── lib.rs
└── main.rs
```

## Support

For support and further inquiries, please connect via Telegram: [jwest951227](https://t.me/jwest951227).
