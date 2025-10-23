# KipuBank

## Descripción
KipuBank es un contrato inteligente que permite a los usuarios depositar y retirar ETH de manera segura, siguiendo límites globales y por transacción. Además, mantiene historial completo de depósitos y retiros.

## Características
- Depósitos de ETH con límite global (`bankCap`).
- Retiros con límite por transacción (`perTxWithdrawLimit`).
- Historial de depósitos y retiros por usuario.
- Funciones de consulta (`view`) para estadísticas y saldos.
- Función privada para obtener movimientos internos.
- Función externa solo para el dueño para consultar todos los movimientos de un usuario.
- Seguridad: reentrancy guard, errores personalizados, checks-effects-interactions.

## Despliegue
1. Configurar Remix con Solidity ^0.8.0.
2. Desplegar el contrato en la testnet (Sepolia) con los parámetros:
   - `_bankCap`: Límite total de depósitos.
   - `_perTxWithdrawLimit`: Límite de retiro por transacción.
3. Verificar el contrato en el explorador de la testnet.

## Interacción
- **Depositar ETH:** llamar a `deposit()` enviando ETH.
- **Retirar ETH:** llamar a `withdraw(uint256 amount)`.
- **Consultar saldo:** `getUserBalance(address user)`.
- **Consultar estadísticas del banco:** `getBankStats()`.
- **Consultar historial:** `getDepositHistory(address user)` o `getWithdrawHistory(address user)`.
- **Dueño:** `getUserMovements(address user)` para historial completo.

## Dirección del contrato anterior
0x9Ae2004220931735B7b67013E39Ac1E6D34758F5
## Dirección del contrato corregido
0xce1041e3905b0308A9d2Fc41e6601e4DB49F14F1
