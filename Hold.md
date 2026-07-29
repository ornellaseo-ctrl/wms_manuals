# Tabelas — Hold

> Categoria extraída da planilha `Tables-Database.xlsx`. Total de tabelas: **8**.

## `C_HOLD_ACCESS`

- **Tipo:** Transactional
- **Categoria:** Hold
- **Campos:** 2
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `HOLD_ACCESS` | Holdessorial Access | VARCHAR2 | 4 |  | N |

## `C_HOLD_TRANS`

- **Tipo:** Transactional
- **Categoria:** Hold
- **Campos:** 14
- **Campos-chave prováveis:** HOLD_CODE, LOC_CODE, COMP_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | N |
| 2 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | N |
| 3 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 4 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | N |
| 5 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 6 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 7 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 8 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | N |
| 9 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | N |
| 10 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | N |
| 11 | `INVT_LEV5` | Inventory Level 5 | VARCHAR2 | 40 |  | Y |
| 12 | `HOLD_TRANS_DATE` | Hold_Transessorial Date | DATE | 7 |  | N |
| 13 | `HOLD_TRANS_QTY` | Hold_Transessorial Qty | NUMBER | 22 | 9 | N |
| 14 | `HOLD_CNVC_QTY` | Hold_Cnvcessorial Qty | NUMBER | 22 | 6 | Y |

## `M_HOLD`

- **Tipo:** Master
- **Categoria:** Hold
- **Campos:** 24
- **Campos-chave prováveis:** COMP_CODE, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | N |
| 4 | `HOLD_DES` | Holdessorial Des | VARCHAR2 | 30 |  | N |
| 5 | `HOLD_STAT` | Holdessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `HOLD_SHIP_FLAG` | Hold_Shipessorial Flag | VARCHAR2 | 1 |  | N |
| 7 | `HOLD_RENW_FLAG` | Hold_Renwessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `HOLD_AUTO_TAKEOFF_FLAG` | Hold_Auto_Takeoffessorial Flag | VARCHAR2 | 1 |  | N |
| 9 | `NUM_DAY` | Numessorial Day | NUMBER | 22 | 3 | Y |
| 10 | `NUM_HOUR` | Numessorial Hour | NUMBER | 22 | 4 | Y |
| 11 | `HOLD_BOND_FLAG` | Hold_Bondessorial Flag | VARCHAR2 | 1 |  | N |
| 12 | `HOLD_QLTY_FLAG` | Hold_Qltyessorial Flag | VARCHAR2 | 1 |  | Y |
| 13 | `HOLD_DAM_FLAG` | Hold_Damessorial Flag | VARCHAR2 | 1 |  | Y |
| 14 | `HOLD_AUTO_TAKEOFF_DATE` | Hold_Auto_Takeoffessorial Date | DATE | 7 |  | Y |
| 15 | `HOLD_BREAK_HIGH_SKU_ADJ_FLAG` | Hold_Break_High_Sku_Adjessorial Flag | VARCHAR2 | 1 |  | N |
| 16 | `PICK_PROF_CODE` | Pick_Professorial Code | VARCHAR2 | 4 |  | Y |
| 17 | `HOLD_RES_FLAG` | Hold_Resessorial Flag | VARCHAR2 | 1 |  | Y |
| 18 | `HOLD_DSBL_EDI_ADJ_SEND_FLAG` | Hold_Dsbl_Edi_Adj_Sendessorial Flag | VARCHAR2 | 1 |  | Y |
| 19 | `HOLD_EVISTA_FLAG` | Hold_Evistaessorial Flag | VARCHAR2 | 1 |  | Y |
| 20 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 21 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 22 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 23 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 24 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_HOLD_ACTN`

- **Tipo:** Master
- **Categoria:** Hold
- **Campos:** 5
- **Campos-chave prováveis:** COMP_CODE, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | N |
| 3 | `ACTN_CODE` | Actnessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `ACTN_DES` | Actnessorial Des | VARCHAR2 | 30 |  | N |
| 5 | `ACTN_STAT` | Actnessorial Stat | VARCHAR2 | 1 |  | N |

## `M_HOLD_COMP_CUST_EDI`

- **Tipo:** Master
- **Categoria:** Hold
- **Campos:** 13
- **Campos-chave prováveis:** COMP_CODE, HOLD_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | N |
| 4 | `COMP_CODE_ACTUAL` | Comp_Codeessorial Actual | VARCHAR2 | 2 |  | N |
| 5 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 6 | `HOLD_CODE_INB_EDI_CODE` | Hold_Code_Inb_Ediessorial Code | VARCHAR2 | 20 |  | Y |
| 7 | `HOLD_CODE_OUTB_EDI_CODE` | Hold_Code_Outb_Ediessorial Code | VARCHAR2 | 20 |  | Y |
| 8 | `HOLD_CODE_INB_BASE_FLAG` | Hold_Code_Inb_Baseessorial Flag | VARCHAR2 | 1 |  | Y |
| 9 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 10 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 12 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 13 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_HOLD_SHIP_SEQ_PROF_D`

- **Tipo:** Master
- **Categoria:** Hold
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `HOLD_SHIP_SEQ_PROF_CODE` | Hold_Ship_Seq_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `HOLD_SHIP_SEQ_NUM` | Hold_Ship_Seqessorial Num | NUMBER | 22 | 2 | N |
| 5 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_HOLD_SHIP_SEQ_PROF_H`

- **Tipo:** Master
- **Categoria:** Hold
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `HOLD_SHIP_SEQ_PROF_CODE` | Hold_Ship_Seq_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `HOLD_SHIP_SEQ_PROF_DES` | Hold_Ship_Seq_Professorial Des | VARCHAR2 | 30 |  | N |
| 5 | `HOLD_SHIP_SEQ_PROF_STAT` | Hold_Ship_Seq_Professorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_INCUB_HOLD_PROF`

- **Tipo:** Master
- **Categoria:** Hold
- **Campos:** 14
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `INCUB_HOLD_PROF_CODE` | Incub_Hold_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `INCUB_HOLD_PROF_DES` | Incub_Hold_Professorial Des | VARCHAR2 | 30 |  | N |
| 5 | `INCUB_HOLD_PROF_STAT` | Incub_Hold_Professorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `ITEM_INCUB_HOLD_CODE` | Item_Incub_Holdessorial Code | VARCHAR2 | 4 |  | N |
| 7 | `ITEM_INCUB_HOLD_NUM_DAYS` | Item_Incub_Hold_Numessorial Days | NUMBER | 22 | 6 | N |
| 8 | `ITEM_INCUB_HOLD_DATE_FORUL` | Item_Incub_Hold_Dateessorial Forul | VARCHAR2 | 255 |  | N |
| 9 | `ITEM_INCUB_HOLD_DATE_FORUL_FMT` | Item_Incub_Hold_Date_Forulessorial Fmt | VARCHAR2 | 20 |  | N |
| 10 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 11 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 13 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 14 | `VERSION` | Version | NUMBER | 22 | 9 | N |

