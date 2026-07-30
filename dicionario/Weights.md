# Tabelas — Weights

> Categoria extraída da planilha `Tables-Database.xlsx`. Total de tabelas: **5**.

## `C_TARE_WGT_ENTRY`

- **Tipo:** Transactional
- **Categoria:** Weights
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | Y |
| 4 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | Y |
| 5 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | Y |
| 6 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | Y |
| 7 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | Y |
| 8 | `GROSS_WGT` | Grossessorial Wgt | NUMBER | 22 | 14 | Y |
| 9 | `TARE_WGT` | Tareessorial Wgt | NUMBER | 22 | 14 | Y |
| 10 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 11 | `TARE_WGT_ENTRY_DATE` | Tare_Wgt_Entryessorial Date | DATE | 7 |  | N |

## `C_WGT_SCALE`

- **Tipo:** Transactional
- **Categoria:** Weights
- **Campos:** 6

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `WGT_SCALE_CODE` | Wgt_Scaleessorial Code | VARCHAR2 | 4 |  | N |
| 2 | `WGT_SCALE_WGT` | Wgt_Scaleessorial Wgt | NUMBER | 22 | 16 | Y |
| 3 | `ERR_TEXT` | Error Text | VARCHAR2 | 1500 |  | Y |
| 4 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 5 | `CREATE_DATE` | Create Date | DATE | 7 |  | N |
| 6 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |

## `M_WGT_SCALE`

- **Tipo:** Master
- **Categoria:** Weights
- **Campos:** 11

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `WGT_SCALE_CODE` | Wgt_Scaleessorial Code | VARCHAR2 | 4 |  | N |
| 3 | `WGT_SCALE_DES` | Wgt_Scaleessorial Des | VARCHAR2 | 30 |  | N |
| 4 | `WGT_SCALE_STAT` | Wgt_Scaleessorial Stat | VARCHAR2 | 1 |  | N |
| 5 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | N |
| 6 | `WGT_SCALE_COMM_REF` | Wgt_Scale_Commessorial Ref | VARCHAR2 | 80 |  | N |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_WGT_TLR_PROF`

- **Tipo:** Master
- **Categoria:** Weights
- **Campos:** 18
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `WGT_TLR_PROF_CODE` | Wgt_Tlr_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `WGT_TLR_PROF_DES` | Wgt_Tlr_Professorial Des | VARCHAR2 | 30 |  | N |
| 5 | `WGT_TLR_PROF_STAT` | Wgt_Tlr_Professorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `WGT_TLR_PROF_OUTB_UN_PCENT` | Wgt_Tlr_Prof_Outb_Unessorial Pcent | NUMBER | 22 | 7 | Y |
| 7 | `WGT_TLR_PROF_OUTB_OV_PCENT` | Wgt_Tlr_Prof_Outb_Ovessorial Pcent | NUMBER | 22 | 7 | Y |
| 8 | `WGT_TLR_PROF_OUTB_UN_WGT` | Wgt_Tlr_Prof_Outb_Unessorial Wgt | NUMBER | 22 | 16 | Y |
| 9 | `WGT_TLR_PROF_OUTB_OV_WGT` | Wgt_Tlr_Prof_Outb_Ovessorial Wgt | NUMBER | 22 | 16 | Y |
| 10 | `WGT_TLR_PROF_INB_UN_PCENT` | Wgt_Tlr_Prof_Inb_Unessorial Pcent | NUMBER | 22 | 7 | Y |
| 11 | `WGT_TLR_PROF_INB_OV_PCENT` | Wgt_Tlr_Prof_Inb_Ovessorial Pcent | NUMBER | 22 | 7 | Y |
| 12 | `WGT_TLR_PROF_INB_UN_WGT` | Wgt_Tlr_Prof_Inb_Unessorial Wgt | NUMBER | 22 | 16 | Y |
| 13 | `WGT_TLR_PROF_INB_OV_WGT` | Wgt_Tlr_Prof_Inb_Ovessorial Wgt | NUMBER | 22 | 16 | Y |
| 14 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 15 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 16 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 17 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 18 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `S_WGT_MEAS_FACT`

- **Tipo:** System Setup Related
- **Categoria:** Weights
- **Campos:** 4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | N |
| 2 | `WGT_MEAS_DES` | Wgt_Measessorial Des | VARCHAR2 | 30 |  | N |
| 3 | `WGT_MEAS_FACT` | Wgt_Measessorial Fact | NUMBER | 22 | 8 | N |
| 4 | `WGT_MEAS_FORMAT` | Wgt_Measessorial Format | VARCHAR2 | 20 |  | N |

