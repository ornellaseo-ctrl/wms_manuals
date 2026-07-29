# Tabelas — Equipment

> Categoria extraída da planilha `Tables-Database.xlsx`. Total de tabelas: **8**.

## `C_MHE_INTFACE_LOG`

- **Tipo:** Transactional
- **Categoria:** Equipment
- **Campos:** 14
- **Campos-chave prováveis:** COMP_CODE, LOC_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `INTFACE_SEQ_NUM` | Intface_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `CREATE_DATE` | Create Date | DATE | 7 |  | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 5 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 6 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 7 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | N |
| 8 | `MODE_CODE` | Modeessorial Code | VARCHAR2 | 20 |  | N |
| 9 | `ZONE_CODE` | Zone Code | VARCHAR2 | 4 |  | Y |
| 10 | `ZONE_COMM_REF` | Zarehouse Comm Ref | VARCHAR2 | 20 |  | Y |
| 11 | `MSG_SENT` | Msgessorial Sent | VARCHAR2 | 250 |  | Y |
| 12 | `MSG_FEEDBACK` | Msgessorial Feedback | VARCHAR2 | 250 |  | Y |
| 13 | `ERR_NUM` | Erressorial Num | NUMBER | 22 | 9 | Y |
| 14 | `ERR_TEXT` | Error Text | VARCHAR2 | 250 |  | Y |

## `E_PROS_MHE`

- **Tipo:** Transactional
- **Categoria:** Equipment
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `MHE_CODE` | Mheessorial Code | VARCHAR2 | 10 |  | N |
| 3 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 4 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |

## `M_EQP_OWN`

- **Tipo:** Master
- **Categoria:** Equipment
- **Campos:** 17
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `EQP_OWN_CODE` | Eqp_Ownessorial Code | VARCHAR2 | 10 |  | N |
| 4 | `EQP_OWN_NAME` | Eqp_Ownessorial Name | VARCHAR2 | 30 |  | N |
| 5 | `EQP_OWN_STAT` | Eqp_Ownessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `EQP_OWN_ADD1` | Eqp_Ownessorial Add1 | VARCHAR2 | 30 |  | N |
| 7 | `EQP_OWN_ADD2` | Eqp_Ownessorial Add2 | VARCHAR2 | 30 |  | Y |
| 8 | `EQP_OWN_ADD3` | Eqp_Ownessorial Add3 | VARCHAR2 | 30 |  | Y |
| 9 | `ZIP_CODE` | Zip Code | VARCHAR2 | 10 |  | N |
| 10 | `EQP_OWN_ADD4` | Eqp_Ownessorial Add4 | VARCHAR2 | 30 |  | Y |
| 11 | `COUNTRY_CODE` | Country Code | VARCHAR2 | 4 |  | N |
| 12 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 13 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 14 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 15 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 16 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 17 | `ZIP_ID` | Zip ID | RAW | 32 |  | N |

## `M_EQP_TP`

- **Tipo:** Master
- **Categoria:** Equipment
- **Campos:** 9
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `EQP_TP_CODE` | Eqp_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 3 | `EQP_TP_DES` | Eqp_Tpessorial Des | VARCHAR2 | 30 |  | N |
| 4 | `EQP_TP_STAT` | Eqp_Tpessorial Stat | VARCHAR2 | 1 |  | N |
| 5 | `BAS_EQP_TP_CODE` | Bas_Eqp_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 6 | `EQP_TP_LIC_REQ_FLAG` | Eqp_Tp_Lic_Reqessorial Flag | VARCHAR2 | 1 |  | N |
| 7 | `EQP_TP_CAPC_REQ_FLAG` | Eqp_Tp_Capc_Reqessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `EQP_TP_DIM_REQ_FLAG` | Eqp_Tp_Dim_Reqessorial Flag | VARCHAR2 | 1 |  | N |
| 9 | `EQP_TP_OP_LIC_REQ_FLAG` | Eqp_Tp_Op_Lic_Reqessorial Flag | VARCHAR2 | 1 |  | N |

## `M_MHE`

- **Tipo:** Master
- **Categoria:** Equipment
- **Campos:** 14
- **Campos-chave prováveis:** COMP_CODE, LOC_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `MHE_CODE` | Mheessorial Code | VARCHAR2 | 10 |  | N |
| 4 | `MHE_DES` | Mheessorial Des | VARCHAR2 | 30 |  | N |
| 5 | `MHE_STAT` | Mheessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `MHE_TP_CODE` | Mhe_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 7 | `MHE_HOUR_COST` | Mhe_Houressorial Cost | NUMBER | 22 | 6 | N |
| 8 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 9 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | Y |
| 10 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 11 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 13 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 14 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_MHE_TP_D`

- **Tipo:** Master
- **Categoria:** Equipment
- **Campos:** 8

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `MHE_TP_CODE` | Mhe_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 3 | `LOC_VERT_HGT_FACT_CODE` | Loc_Vert_Hgt_Factessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 5 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 6 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 7 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_MHE_TP_H`

- **Tipo:** Master
- **Categoria:** Equipment
- **Campos:** 15

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `MHE_TP_CODE` | Mhe_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 3 | `MHE_TP_DES` | Mhe_Tpessorial Des | VARCHAR2 | 30 |  | Y |
| 4 | `MHE_TP_HOUR_COST` | Mhe_Tp_Houressorial Cost | NUMBER | 22 | 6 | N |
| 5 | `MHE_TP_STAT` | Mhe_Tpessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `MHE_TP_LAB_STD_MODY_NUM` | Mhe_Tp_Lab_Std_Modyessorial Num | NUMBER | 22 | 4 | Y |
| 7 | `MHE_TP_UNIT_PACK_FLAG` | Mhe_Tp_Unit_Packessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `MHE_TP_LOC_REQ_FLAG` | Mhe_Tp_Loc_Reqessorial Flag | VARCHAR2 | 1 |  | N |
| 9 | `MHE_TP_OUT_PACK_FLAG` | Mhe_Tp_Out_Packessorial Flag | VARCHAR2 | 1 |  | N |
| 10 | `SYS_TP_CODE` | Sys_Tpessorial Code | VARCHAR2 | 20 |  | N |
| 11 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 12 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 13 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 14 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 15 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_MHE_TP_WHSE_ACT_TP_NUM`

- **Tipo:** Master
- **Categoria:** Equipment
- **Campos:** 8

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `MHE_TP_CODE_EXCL` | Mhe_Tp_Codeessorial Excl | VARCHAR2 | 4 |  | N |
| 3 | `WHSE_ACT_TP_NUM` | Whse_Act_Tpessorial Num | NUMBER | 22 | 2 | N |
| 4 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 5 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 6 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 7 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `VERSION` | Version | NUMBER | 22 | 9 | N |

