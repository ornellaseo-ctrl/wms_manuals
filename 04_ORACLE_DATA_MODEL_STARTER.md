# Oracle Data Model — Starter Körber / AccellosOne 3PL

> Camada inicial para conectar documentação funcional, tabelas Oracle e troubleshooting. Edite este arquivo com joins reais, regras locais e queries validadas.

## Recebimento

| Tabela | Existe na planilha | Categoria | Tipo | Campos documentados | Campos-chave encontrados |
|---|:---:|---|---|---:|---|
| `E_RCPT_H` | Sim | Receipts | Transactional | 68 | COMP_CODE, RCPT_NUM, CUST_CODE |
| `E_RCPT_D5` | Sim | Receipts | Transactional | 79 | COMP_CODE, RCPT_NUM, SKU_CODE, HOLD_CODE |
| `VA_OP_RCPT` | Não | - | - | 0 | - |
| `C_INVT` | Sim | Billing | Transactional | 49 | COMP_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4 |
| `C_MVT_H` | Sim | Move | Transactional | 59 | MVT_TRANS_TP, COMP_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4, HOLD_CODE, LOC_CODE |

## Pedidos / Expedição

| Tabela | Existe na planilha | Categoria | Tipo | Campos documentados | Campos-chave encontrados |
|---|:---:|---|---|---:|---|
| `E_ORD_H` | Sim | Orders | Transactional | 91 | COMP_CODE, ORD_NUM, CUST_CODE |
| `E_ORD_D5` | Sim | Orders | Transactional | 73 | COMP_CODE, ORD_NUM, CUST_CODE, SKU_CODE, HOLD_CODE |
| `E_ORD_D5D1` | Sim | Orders | Transactional | 37 | COMP_CODE, ORD_NUM, CUST_CODE, INVT_LEV1, LOC_CODE, HOLD_CODE |
| `VA_OP_ORD` | Não | - | - | 0 | - |
| `C_INVT` | Sim | Billing | Transactional | 49 | COMP_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4 |
| `C_MVT_H` | Sim | Move | Transactional | 59 | MVT_TRANS_TP, COMP_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4, HOLD_CODE, LOC_CODE |

## Inventário

| Tabela | Existe na planilha | Categoria | Tipo | Campos documentados | Campos-chave encontrados |
|---|:---:|---|---|---:|---|
| `C_INVT` | Sim | Billing | Transactional | 49 | COMP_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4 |
| `C_LOC` | Sim | Locations | Transactional | 46 | LOC_CODE, HOLD_CODE, COMP_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4 |
| `C_MVT_H` | Sim | Move | Transactional | 59 | MVT_TRANS_TP, COMP_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4, HOLD_CODE, LOC_CODE |
| `VA_INVT_HIST` | Não | - | - | 0 | - |

## Cadastro Cliente/Item

| Tabela | Existe na planilha | Categoria | Tipo | Campos documentados | Campos-chave encontrados |
|---|:---:|---|---|---:|---|
| `M_CUST_H` | Sim | Customer | Master | 67 | COMP_CODE, CUST_CODE |
| `M_ITEM_H` | Sim | Item | Master | 83 | COMP_CODE, CUST_CODE, ITEM_CODE, SKU_CODE |
| `M_ITEM_D3` | Sim | Item | Master | 11 | COMP_CODE, CUST_CODE, ITEM_CODE |
| `M_ALT_INVT_REP_D` | Sim | Billing | Master | 13 | COMP_CODE |

## Billing

| Tabela | Existe na planilha | Categoria | Tipo | Campos documentados | Campos-chave encontrados |
|---|:---:|---|---|---:|---|
| `E_ACCSS_H` | Sim | Billing | Transactional | 90 | COMP_CODE, CUST_CODE, CHG_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4 |
| `M_CHG` | Sim | Billing | Master | 25 | COMP_CODE, CHG_CODE |
| `M_ITEM_BILL_PROF` | Sim | Item | Master | 29 | COMP_CODE |
| `M_DATE_PROF_D` | Sim | Date | Master | 9 | COMP_CODE |

## Cargas / Loads

| Tabela | Existe na planilha | Categoria | Tipo | Campos documentados | Campos-chave encontrados |
|---|:---:|---|---|---:|---|
| `E_LOAD_H` | Não | - | - | 0 | - |
| `E_LOAD_D` | Não | - | - | 0 | - |
| `VA_OP_LOAD` | Não | - | - | 0 | - |

## Observação

As relações acima são ponto de partida. Valide os joins no ambiente Oracle antes de usar em produção.
