# Tabelas — Forecast

> Categoria extraída da planilha `Tables-Database.xlsx`. Total de tabelas: **1**.

## `C_FORECAST_ASS`

- **Tipo:** Transactional
- **Categoria:** Forecast
- **Campos:** 50
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `DOC_NUM` | Document Number | NUMBER | 22 | 9 | N |
| 4 | `DOC_LINE_NUM` | Document Line Number | NUMBER | 22 | 4 | N |
| 5 | `DOC_LOC_LINE_NUM` | Document Location Line Number | NUMBER | 22 | 4 | N |
| 6 | `DOC_TP_FLAG` | Doc_Tpessorial Flag | VARCHAR2 | 1 |  | N |
| 7 | `FORECAST_TP_CODE` | Forecast_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 8 | `FORECAST_ASS_ID` | Forecast_Assessorial Id | VARCHAR2 | 100 |  | N |
| 9 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 10 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 11 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | Y |
| 12 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | Y |
| 13 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | Y |
| 14 | `LOAD_TP_CODE` | Load Type Code | VARCHAR2 | 4 |  | Y |
| 15 | `DOC_CARRY_UNIT_NUM` | Doc_Carry_Unitessorial Num | VARCHAR2 | 20 |  | Y |
| 16 | `DOC_VES` | Docessorial Ves | VARCHAR2 | 20 |  | Y |
| 17 | `DOC_VOY` | Docessorial Voy | VARCHAR2 | 20 |  | Y |
| 18 | `CON_SHIP_CODE` | Consignee Ship Code | VARCHAR2 | 10 |  | Y |
| 19 | `CON_SHIP_NAME` | Con_Shipessorial Name | VARCHAR2 | 30 |  | Y |
| 20 | `CON_SHIP_MAST_CODE` | Con_Ship_Mastessorial Code | VARCHAR2 | 10 |  | Y |
| 21 | `FORECAST_DOC_FIRST_LAST_FLAG` | Forecast_Doc_First_Lastessorial Flag | VARCHAR2 | 1 |  | Y |
| 22 | `FORECAST_QTY` | Forecastessorial Qty | NUMBER | 22 | 9 | N |
| 23 | `FORECAST_WGT` | Forecastessorial Wgt | NUMBER | 22 | 16 | N |
| 24 | `FORECAST_WGT_NET` | Forecast_Wgtessorial Net | NUMBER | 22 | 16 | N |
| 25 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | N |
| 26 | `FORECAST_CUBE` | Forecastessorial Cube | NUMBER | 22 | 16 | N |
| 27 | `LINEAR_MEAS_CODE` | Linear Measurement Code | VARCHAR2 | 4 |  | N |
| 28 | `FORECAST_ASN_FLAG` | Forecast_Asnessorial Flag | VARCHAR2 | 1 |  | N |
| 29 | `FORECAST_SPC_COND_REF` | Forecast_Spc_Condessorial Ref | VARCHAR2 | 20 |  | Y |
| 30 | `FORECAST_WRAP_REQ_FLAG` | Forecast_Wrap_Reqessorial Flag | VARCHAR2 | 1 |  | Y |
| 31 | `CART_ID` | Cart ID | VARCHAR2 | 40 |  | Y |
| 32 | `WHSE_CODE_FROM` | Whse_Codeessorial From | VARCHAR2 | 4 |  | Y |
| 33 | `LOC_CODE_FROM` | Loc_Codeessorial From | VARCHAR2 | 12 |  | Y |
| 34 | `WHSE_CODE_TO` | Warehouse Code To | VARCHAR2 | 4 |  | Y |
| 35 | `LOC_CODE_TO` | Loc_Codeessorial To | VARCHAR2 | 12 |  | Y |
| 36 | `LOC_SEQ_NUM` | Loc_Seqessorial Num | NUMBER | 22 | 3 | Y |
| 37 | `WHSE_ACT_TP_NUM` | Whse_Act_Tpessorial Num | NUMBER | 22 | 2 | Y |
| 38 | `BLDG_CODE` | Building Code | VARCHAR2 | 4 |  | Y |
| 39 | `DOOR_CODE` | Door Code | VARCHAR2 | 4 |  | Y |
| 40 | `LOAD_NUM` | Load Number | NUMBER | 22 | 6 | Y |
| 41 | `STOP_NUM` | Stop Number | NUMBER | 22 | 2 | Y |
| 42 | `CON_CODE_LOAD` | Con_Codeessorial Load | VARCHAR2 | 10 |  | Y |
| 43 | `AUDIT_NUM` | Audit Number | NUMBER | 22 | 6 | Y |
| 44 | `FORECAST_AUDIT_DATE` | Forecast_Auditessorial Date | DATE | 7 |  | Y |
| 45 | `FORECAST_ASS_EST_TIME` | Forecast_Ass_Estessorial Time | NUMBER | 22 | 9 | Y |
| 46 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 47 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 48 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 49 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 50 | `VERSION` | Version | NUMBER | 22 | 9 | N |

