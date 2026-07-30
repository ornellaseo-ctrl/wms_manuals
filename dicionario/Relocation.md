# Tabelas — Relocation

> Categoria extraída da planilha `Tables-Database.xlsx`. Total de tabelas: **2**.

## `C_RELO_PICK`

- **Tipo:** Transactional
- **Categoria:** Relocation
- **Campos:** 35
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4, ORD_NUM, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 5 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | N |
| 6 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | N |
| 7 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | N |
| 8 | `INVT_LEV5` | Inventory Level 5 | VARCHAR2 | 40 |  | Y |
| 9 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 10 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |
| 11 | `ORD_LOC_LINE_NUM` | Ord_Loc_Lineessorial Num | NUMBER | 22 | 4 | N |
| 12 | `WHSE_CODE_FROM` | Whse_Codeessorial From | VARCHAR2 | 4 |  | N |
| 13 | `LOC_CODE_FROM` | Loc_Codeessorial From | VARCHAR2 | 12 |  | N |
| 14 | `WHSE_CODE_TO` | Warehouse Code To | VARCHAR2 | 4 |  | N |
| 15 | `LOC_CODE_TO` | Loc_Codeessorial To | VARCHAR2 | 12 |  | N |
| 16 | `RELO_QTY` | Reloessorial Qty | NUMBER | 22 | 9 | N |
| 17 | `RELO_WGT` | Reloessorial Wgt | NUMBER | 22 | 11 | N |
| 18 | `RELO_CUBE` | Reloessorial Cube | NUMBER | 22 | 12 | N |
| 19 | `RELO_DATE` | Reloessorial Date | DATE | 7 |  | N |
| 20 | `RELO_AUDIT_NUM` | Relo_Auditessorial Num | NUMBER | 22 | 6 | Y |
| 21 | `WHSE_CODE_FLT` | Whse_Codeessorial Flt | VARCHAR2 | 4 |  | Y |
| 22 | `LOC_CODE_FLT` | Loc_Codeessorial Flt | VARCHAR2 | 12 |  | Y |
| 23 | `WHSE_CODE_MOVE` | Whse_Codeessorial Move | VARCHAR2 | 4 |  | Y |
| 24 | `LOC_CODE_MOVE` | Loc_Codeessorial Move | VARCHAR2 | 12 |  | Y |
| 25 | `EMP_TASK_SEQ_NUM_FROM` | Emp_Task_Seq_Numessorial From | NUMBER | 22 | 9 | Y |
| 26 | `EMP_TASK_SEQ_NUM_TO` | Emp_Task_Seq_Numessorial To | NUMBER | 22 | 9 | Y |
| 27 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |
| 28 | `RELO_SEQ_NUM` | Relo_Seqessorial Num | NUMBER | 22 | 9 | Y |
| 29 | `INVT_ACCESS_TO` | Invt_Accessessorial To | VARCHAR2 | 5 |  | Y |
| 30 | `RELO_PICK_MES_TEXT` | Relo_Pick_Mesessorial Text | VARCHAR2 | 30 |  | Y |
| 31 | `WHSE_CODE_FROM_ORG` | Whse_Code_Fromessorial Org | VARCHAR2 | 4 |  | Y |
| 32 | `LOC_CODE_FROM_ORG` | Loc_Code_Fromessorial Org | VARCHAR2 | 12 |  | Y |
| 33 | `ADJ_NUM` | Adjustment Number | NUMBER | 22 | 6 | Y |
| 34 | `ADJ_LINE_NUM` | Adjustment Line Number | NUMBER | 22 | 4 | Y |
| 35 | `PRTY_NUM_OVRR` | Prty_Numessorial Ovrr | NUMBER | 22 | 9 | Y |

## `H_RELO_PICK`

- **Tipo:** Historical
- **Categoria:** Relocation
- **Campos:** 37
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4, ORD_NUM, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `INSERT_TO_H_RELO_PICK_DATE` | Insert_To_H_Relo_Pickessorial Date | DATE | 7 |  | N |
| 2 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 5 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 6 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | N |
| 7 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | N |
| 8 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | N |
| 9 | `INVT_LEV5` | Inventory Level 5 | VARCHAR2 | 40 |  | Y |
| 10 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 11 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |
| 12 | `ORD_LOC_LINE_NUM` | Ord_Loc_Lineessorial Num | NUMBER | 22 | 4 | N |
| 13 | `WHSE_CODE_FROM` | Whse_Codeessorial From | VARCHAR2 | 4 |  | N |
| 14 | `LOC_CODE_FROM` | Loc_Codeessorial From | VARCHAR2 | 12 |  | N |
| 15 | `WHSE_CODE_TO` | Warehouse Code To | VARCHAR2 | 4 |  | N |
| 16 | `LOC_CODE_TO` | Loc_Codeessorial To | VARCHAR2 | 12 |  | N |
| 17 | `RELO_QTY` | Reloessorial Qty | NUMBER | 22 | 9 | N |
| 18 | `RELO_WGT` | Reloessorial Wgt | NUMBER | 22 | 11 | N |
| 19 | `RELO_CUBE` | Reloessorial Cube | NUMBER | 22 | 12 | N |
| 20 | `RELO_DATE` | Reloessorial Date | DATE | 7 |  | N |
| 21 | `RELO_AUDIT_NUM` | Relo_Auditessorial Num | NUMBER | 22 | 6 | Y |
| 22 | `WHSE_CODE_FLT` | Whse_Codeessorial Flt | VARCHAR2 | 4 |  | Y |
| 23 | `LOC_CODE_FLT` | Loc_Codeessorial Flt | VARCHAR2 | 12 |  | Y |
| 24 | `WHSE_CODE_MOVE` | Whse_Codeessorial Move | VARCHAR2 | 4 |  | Y |
| 25 | `LOC_CODE_MOVE` | Loc_Codeessorial Move | VARCHAR2 | 12 |  | Y |
| 26 | `EMP_TASK_SEQ_NUM_FROM` | Emp_Task_Seq_Numessorial From | NUMBER | 22 | 9 | Y |
| 27 | `EMP_TASK_SEQ_NUM_TO` | Emp_Task_Seq_Numessorial To | NUMBER | 22 | 9 | Y |
| 28 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |
| 29 | `RELO_SEQ_NUM` | Relo_Seqessorial Num | NUMBER | 22 | 9 | Y |
| 30 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | Y |
| 31 | `INVT_ACCESS_TO` | Invt_Accessessorial To | VARCHAR2 | 5 |  | Y |
| 32 | `RELO_PICK_MES_TEXT` | Relo_Pick_Mesessorial Text | VARCHAR2 | 30 |  | Y |
| 33 | `WHSE_CODE_FROM_ORG` | Whse_Code_Fromessorial Org | VARCHAR2 | 4 |  | Y |
| 34 | `LOC_CODE_FROM_ORG` | Loc_Code_Fromessorial Org | VARCHAR2 | 12 |  | Y |
| 35 | `ADJ_NUM` | Adjustment Number | NUMBER | 22 | 6 | Y |
| 36 | `ADJ_LINE_NUM` | Adjustment Line Number | NUMBER | 22 | 4 | Y |
| 37 | `PRTY_NUM_OVRR` | Prty_Numessorial Ovrr | NUMBER | 22 | 9 | Y |

