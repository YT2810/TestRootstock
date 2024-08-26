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

Cargar las Variables de entorno

```shell
$ source .env
```

```shell
$ forge script script/Counter.s.sol:CounterScript --rpc-url $ROOTSTOCK_RPC_URL --broadcast --legacy
```
Nota: El flag --legacy es necesario para Rootstock porque no soporta EIP-1559.

Verificar el Despliegue:

Puedes verificar el contrato desplegado en Rootstock Testnet Explorer.


### Contrato Desplegado
Dirección del Contrato: 0x603CB2Ea788542f48990A4e393025045428bFaB9
Hash Transacción de Despliegue: 0xc0fcbf4ffc4d618fd9c632f4f0dc215094faaa0e7115adcb9ab1c63818838e2f

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

### Interactuar con el Contrato Desplegado

```shell
$ cast send --rpc-url $ROOTSTOCK_RPC_URL --private-key $PRIVATE_KEY <contract_address> "functionName(<params>)"
```

Reemplaza <contract_address> con la dirección del contrato desplegado y functionName con el nombre de la función que deseas llamar.


