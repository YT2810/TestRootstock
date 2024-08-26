## Foundry

**Foundry is a blazing fast, portable and modular toolkit for Ethereum application development written in Rust.**

Foundry consists of:

-   **Forge**: Ethereum testing framework (like Truffle, Hardhat and DappTools).
-   **Cast**: Swiss army knife for interacting with EVM smart contracts, sending transactions and getting chain data.
-   **Anvil**: Local Ethereum node, akin to Ganache, Hardhat Network.
-   **Chisel**: Fast, utilitarian, and verbose solidity REPL.

## Documentation

https://book.getfoundry.sh/

## Prerrequisitos

Para trabajar con este proyecto, asegúrate de tener las siguientes herramientas instaladas:

- **Rust y Cargo**: Necesarios para la compilación de contratos inteligentes con Foundry.
    - Para instalar Rust y Cargo, ejecuta el siguiente comando en tu terminal:

    ```bash
    curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
    ```

    - Verifica la instalación ejecutando:

    ```bash
    rustc --version
    cargo --version
    ```

## Configuración del Entorno

1. **Crear el Archivo `.env`**

   Crea un archivo `.env` en la raíz del proyecto y añade las siguientes variables:

   ```plaintext
   ROOTSTOCK_RPC_URL=https://rpc.testnet.rootstock.io/{YOUR_APIKEY}
   PRIVATE_KEY=0x...
   Reemplaza {YOUR_APIKEY} con tu API key de Rootstock Testnet y 0x... con tu clave privada.

Obtener Fondos de Prueba

Para obtener fondos de prueba (tRBTC), configura MetaMask para Rootstock Testnet y utiliza el faucet de Rootstock Testnet.

## Usage

### Build

```shell
$ forge build
```

### Test

```shell
$ forge test
```

### Format

```shell
$ forge fmt
```

### Gas Snapshots

```shell
$ forge snapshot
```

### Anvil

```shell
$ anvil
```

### Deploy

```shell
$ forge script script/Counter.s.sol:CounterScript --rpc-url <your_rpc_url> --private-key <your_private_key>
```

### Cast

```shell
$ cast <subcommand>
```

### Help

```shell
$ forge --help
$ anvil --help
$ cast --help
```
