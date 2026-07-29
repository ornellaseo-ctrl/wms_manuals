# Tabelas — Hazard

> Categoria extraída da planilha `Tables-Database.xlsx`. Total de tabelas: **5**.

## `C_HAZ_TIER_II_REP`

- **Tipo:** Transactional
- **Categoria:** Hazard
- **Campos:** 18
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE, SKU_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `HAZ_TIER_II_REP_EFF_DATE` | Haz_Tier_Ii_Rep_Effessorial Date | DATE | 7 |  | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 5 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 6 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | N |
| 7 | `ITEM_HAZ_EXT_REF_CODE` | Item_Haz_Ext_Refessorial Code | VARCHAR2 | 20 |  | N |
| 8 | `ON_HAND_WGT_NET` | On_Hand_Wgtessorial Net | NUMBER | 22 | 16 | N |
| 9 | `ITEM_HAZ_PHYS_MATTER_TP` | Item_Haz_Phys_Matteressorial Tp | VARCHAR2 | 4 |  | Y |
| 10 | `SKU_CODE` | SKU Code | VARCHAR2 | 4 |  | Y |
| 11 | `ITEM_HAZ_TECH_NAME` | Item_Haz_Techessorial Name | VARCHAR2 | 255 |  | Y |
| 12 | `ISOL_CODE` | ISOL Code | VARCHAR2 | 4 |  | Y |
| 13 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 14 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 15 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 16 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 17 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 18 | `ITEM_HAZ_MULTIPLIER` | Item_Hazessorial Multiplier | NUMBER | 22 | 5 | Y |

## `C_HAZ_VIOLATION`

- **Tipo:** Transactional
- **Categoria:** Hazard
- **Campos:** 26
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4, LOC_CODE, HOLD_CODE, MVT_TRANS_TP

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 4 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | N |
| 5 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | N |
| 6 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | N |
| 7 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 8 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | N |
| 9 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | N |
| 10 | `TRANS_UNIT` | Transessorial Unit | VARCHAR2 | 20 |  | N |
| 11 | `MVT_UNIT` | Mvtessorial Unit | NUMBER | 22 | 9 | N |
| 12 | `TRANS_DATE` | Transaction Date | DATE | 7 |  | N |
| 13 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 14 | `MVT_TRANS_TP` | Mvt_Transessorial Tp | VARCHAR2 | 2 |  | N |
| 15 | `DOC_NUM` | Document Number | NUMBER | 22 | 9 | N |
| 16 | `DOC_LINE_NUM` | Document Line Number | NUMBER | 22 | 4 | N |
| 17 | `DOC_LOC_LINE_NUM` | Document Location Line Number | NUMBER | 22 | 4 | N |
| 18 | `REP_AUDIT_NUM` | Rep_Auditessorial Num | NUMBER | 22 | 9 | Y |
| 19 | `REP_AUDIT_DATE` | Rep_Auditessorial Date | DATE | 7 |  | Y |
| 20 | `ISOL_CODE` | ISOL Code | VARCHAR2 | 4 |  | N |
| 21 | `ITEM_HAZ_CLASS_CODE` | Item_Haz_Classessorial Code | VARCHAR2 | 10 |  | N |
| 22 | `ITEM_HAZ_SUB_CLASS_PRIMARY` | Item_Haz_Sub_Classessorial Primary | VARCHAR2 | 10 |  | Y |
| 23 | `ITEM_HAZ_SUB_CLASS_SECONDARY` | Item_Haz_Sub_Classessorial Secondary | VARCHAR2 | 10 |  | Y |
| 24 | `ITEM_HAZ_SUB_CLASS_TERTIARY` | Item_Haz_Sub_Classessorial Tertiary | VARCHAR2 | 10 |  | Y |
| 25 | `ITEM_HAZ_LINE_NUM` | Item_Haz_Lineessorial Num | NUMBER | 22 | 4 | N |
| 26 | `ITEM_HAZ_COMPN_LINE_NUM` | Item_Haz_Compn_Lineessorial Num | NUMBER | 22 | 4 | N |

## `M_HAZ_D`

- **Tipo:** Master
- **Categoria:** Hazard
- **Campos:** 7
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `HAZ_CODE` | Hazessorial Code | VARCHAR2 | 6 |  | N |
| 4 | `HAZ_LINE_NUM` | Haz_Lineessorial Num | NUMBER | 22 | 5 | N |
| 5 | `HAZ_LINE_CONN_NUM` | Haz_Line_Connessorial Num | NUMBER | 22 | 5 | N |
| 6 | `HAZ_LINE_ROOT_FLAG` | Haz_Line_Rootessorial Flag | VARCHAR2 | 1 |  | Y |
| 7 | `HAZ_LINE_TEXT` | Haz_Lineessorial Text | VARCHAR2 | 45 |  | Y |

## `M_HAZ_H`

- **Tipo:** Master
- **Categoria:** Hazard
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `HAZ_CODE` | Hazessorial Code | VARCHAR2 | 6 |  | N |
| 4 | `HAZ_DES` | Hazessorial Des | VARCHAR2 | 30 |  | N |
| 5 | `HAZ_STAT` | Hazessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `HAZ_TEXT` | Hazessorial Text | VARCHAR2 | 2000 |  | Y |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_ISOL_HAZ_REST`

- **Tipo:** Master
- **Categoria:** Hazard
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ISOL_CODE` | ISOL Code | VARCHAR2 | 4 |  | N |
| 4 | `ITEM_HAZ_PRIMARY_CLASS` | Item_Haz_Primaryessorial Class | VARCHAR2 | 10 |  | N |
| 5 | `ITEM_HAZ_SECD_CLASS` | Item_Haz_Secdessorial Class | VARCHAR2 | 10 |  | Y |
| 6 | `ITEM_HAZ_TERTIARY_CLASS` | Item_Haz_Tertiaryessorial Class | VARCHAR2 | 10 |  | Y |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

