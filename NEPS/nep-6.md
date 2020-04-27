# NEP-6:URI Scheme

| Item | Description |
|:-|:-|
| NEP | 6 |
| Title | URI Scheme |
| Author | [Newbie D.](https://github.com/newbie-demo) , [Xuefeng Wei](mailto:xf@demo.com), [Alex Xr](mailto:alex.xr@demo.com)|
| Discussions to | URL |
| Status | WIP |
| Type | Standard |
| Category | Technical |
| Created |  |
| Updated |  |
<!--  -->
## Simple Summary

This NEP proposes a URI scheme for making NEW payments/transfers.

## Abstract

The purpose of this URI scheme is to enable users to easily make payments/transfers by simply clicking links on webpages or scanning QR Codes.

## Motivation

It is essential to have a standard for URI scheme to the Newton Community. For developers to create services/applications that compatible with each other. Also to make it compatible outside Newton Community. E.g. app/wallet supports multiple blockchains like Bitcoin and Newton.

## Specification

### Simpler Syntax

[ foo ] means optional, < bar > are placeholders

`<coin>:<address>[?code=<code>][?amount=<amount>][?unit=<unit>][?label=<label>][?msg=<notes>][?msg_param=<param>]`

Items with TBD means this field needs To Be Determined in future versions. Should not be used in current production.

### Parameters

| Parameters           | Description       |
| -------------- | ----------------- |
| coin           | Coin. E.g. newton, bitcoin etc. |
| address        | Address to receiver. E.g. NEW182.....1234, JIs...i2x etc. |
| code           | Symbol Code, Optional. E.g. NEW, BTC etc. |
| amount         | Amount to send. Optional. E.g. 12345678.12345678 |
| unit           | Unit to the Amount. Optional. E.g. NEW, CNY, USD etc. |
| label          | Label Message. Optional. E.g. Vending Machine No.123 |
| msg            | Notes in transaction. Optional. |
| msg_param      | Parameters for notes. values: lock, hidden.   |

## Examples

### Just the address

`NEW182cJEKxVB5dX4K2g5qcC1Zb6o64V17NNZCa`

### Prefix and the address

`newton:NEW182cJEKxVB5dX4K2g5qcC1Zb6o64V17NNZCa`

`bitcoin:1J1CwuZHrhYS4nB1g3osdKZtSrGWYFaT3E`

### Address with name

`newton:NEW182cJEKxVB5dX4K2g5qcC1Zb6o64V17NNZCa?label=Sir-Newton`

### Request 123,456.12345678 NEW to "Someone Newton"

`newton:NEW182cJEKxVB5dX4K2g5qcC1Zb6o64V17NNZCa?amount=123456.12345678&label="Someone Newton"`

### Request equivalence amount of 100 CNY to NEW Address

`newton:NEW182cJEKxVB5dX4K2g5qcC1Zb6o64V17NNZCa?amount=100&unit=CNY`

### Request 123,456.12345678 NEW with Message

`newton:NEW182cJEKxVB5dX4K2g5qcC1Zb6o64V17NNZCa?amount=123456.12345678&msg=thisIsMyMessage`

### Request 123,456.12345678 NEW with Label and Message

`newton:NEW182cJEKxVB5dX4K2g5qcC1Zb6o64V17NNZCa?amount=123456.12345678&label="New Vending Machine"&msg=thisIsMyMessage`

### Request 123,456.12345678 NEW with Message not editable by user

`newton:NEW182cJEKxVB5dX4K2g5qcC1Zb6o64V17NNZCa?amount=123456.12345678&msg=thisIsMyMessage&msg_param=-l`



## Copyright
Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).
