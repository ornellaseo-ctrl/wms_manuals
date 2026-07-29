# Tabelas — Pallet

> Categoria extraída da planilha `Tables-Database.xlsx`. Total de tabelas: **3**.

## `M_PALL`

- **Tipo:** Master
- **Categoria:** Pallet
- **Campos:** 18
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `PALL_CODE` | Pallessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `PALL_DES` | Pallessorial Des | VARCHAR2 | 30 |  | N |
| 5 | `PALL_STAT` | Pallessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `LINEAR_MEAS_CODE` | Linear Measurement Code | VARCHAR2 | 4 |  | N |
| 7 | `PALL_LEN` | Pallessorial Len | NUMBER | 22 | 7 | Y |
| 8 | `PALL_WID` | Pallessorial Wid | NUMBER | 22 | 7 | Y |
| 9 | `PALL_HGT` | Pallessorial Hgt | NUMBER | 22 | 7 | Y |
| 10 | `PALL_CUBE` | Pallessorial Cube | NUMBER | 22 | 10 | Y |
| 11 | `PALL_TP_CODE` | Pall_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 12 | `PALL_WGT` | Pallessorial Wgt | NUMBER | 22 | 16 | Y |
| 13 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | Y |
| 14 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 15 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 16 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 17 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 18 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `T_PALL_CNT`

- **Tipo:** Temporary
- **Categoria:** Pallet
- **Campos:** 6
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `COMP_CODE_ACTUAL` | Comp_Codeessorial Actual | VARCHAR2 | 2 |  | N |
| 3 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | N |
| 4 | `LOAD_NUM` | Load Number | NUMBER | 22 | 6 | N |
| 5 | `PALL_TP` | Pallessorial Tp | VARCHAR2 | 1 |  | N |
| 6 | `PALL_ID` | Pallessorial Id | VARCHAR2 | 250 |  | N |

## `T_PLT_CONSL`

- **Tipo:** Temporary
- **Categoria:** Pallet
- **Campos:** 22
- **Campos-chave prováveis:** COMP_CODE, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `PLT_CONSL_NUM` | Plt_Conslessorial Num | NUMBER | 22 | 9 | N |
| 2 | `PLT_CONSL_LINE_NUM` | Plt_Consl_Lineessorial Num | NUMBER | 22 | 9 | N |
| 3 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 4 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 5 | `CREATE_DATE` | Create Date | DATE | 7 |  | N |
| 6 | `PROS_FLAG` | Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 7 | `PROS_DATE` | Prosessorial Date | DATE | 7 |  | Y |
| 8 | `OP_CODE_PROS` | Op_Codeessorial Pros | VARCHAR2 | 20 |  | Y |
| 9 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 10 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | N |
| 11 | `PLT_CONSL_QTY` | Plt_Conslessorial Qty | NUMBER | 22 | 9 | N |
| 12 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | N |
| 13 | `WHSE_CODE_FROM` | Whse_Codeessorial From | VARCHAR2 | 4 |  | N |
| 14 | `LOC_CODE_FROM` | Loc_Codeessorial From | VARCHAR2 | 12 |  | N |
| 15 | `WHSE_CODE_TO` | Warehouse Code To | VARCHAR2 | 4 |  | Y |
| 16 | `LOC_CODE_TO` | Loc_Codeessorial To | VARCHAR2 | 12 |  | Y |
| 17 | `PLT_CONSL_MAX_HGT` | Plt_Consl_Maxessorial Hgt | NUMBER | 22 | 7 | Y |
| 18 | `LINEAR_MEAS_CODE` | Linear Measurement Code | VARCHAR2 | 4 |  | Y |
| 19 | `ITEM_QTY_BKD_NUM_LAY` | Item_Qty_Bkd_Numessorial Lay | NUMBER | 22 | 3 | Y |
| 20 | `ASS_NUM` | Assessorial Num | NUMBER | 22 | 9 | Y |
| 21 | `ASS_NUM_SEQ` | Ass_Numessorial Seq | NUMBER | 22 | 9 | Y |
| 22 | `PLT_CONSL_GRP_STR` | Plt_Consl_Grpessorial Str | VARCHAR2 | 2000 |  | Y |

