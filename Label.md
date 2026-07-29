# Tabelas — Label

> Categoria extraída da planilha `Tables-Database.xlsx`. Total de tabelas: **9**.

## `BAK_S_LABEL_ML`

- **Tipo:** Misc
- **Categoria:** Label
- **Campos:** 7

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `APP_CODE` | Application Code | VARCHAR2 | 10 |  | N |
| 2 | `ENTITY_CODE` | Entityessorial Code | VARCHAR2 | 40 |  | N |
| 3 | `LABEL_CODE` | Labelessorial Code | VARCHAR2 | 50 |  | N |
| 4 | `LABEL_SUB_CODE` | Label_Subessorial Code | VARCHAR2 | 20 |  | N |
| 5 | `LABEL_TEXT` | Labelessorial Text | VARCHAR2 | 512 |  | N |
| 6 | `LABEL_TEXT_HINT` | Label_Textessorial Hint | VARCHAR2 | 80 |  | Y |
| 7 | `LABEL_ID` | Labelessorial Id | NUMBER | 22 | 4 | Y |

## `C_A1SCH_INTFACE_APPO`

- **Tipo:** Transactional
- **Categoria:** Label
- **Campos:** 26
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `INTFACE_SEQ_NUM` | Intface_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `APPO_A1SCH_ID` | Appo_A1Schessorial Id | VARCHAR2 | 100 |  | N |
| 3 | `APPO_A1SCH_NUM` | Appo_A1Schessorial Num | VARCHAR2 | 100 |  | N |
| 4 | `APPO_A1SCH_MODY_DATE` | Appo_A1Sch_Modyessorial Date | DATE | 7 |  | N |
| 5 | `APPO_A1SCH_STAT` | Appo_A1Schessorial Stat | VARCHAR2 | 100 |  | Y |
| 6 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 7 | `BLDG_CODE` | Building Code | VARCHAR2 | 4 |  | N |
| 8 | `DOOR_CODE` | Door Code | VARCHAR2 | 4 |  | Y |
| 9 | `APPO_INB_OUTB_FLAG` | Appo_Inb_Outbessorial Flag | VARCHAR2 | 1 |  | N |
| 10 | `APPO_REF_NUM` | Appo_Refessorial Num | VARCHAR2 | 20 |  | Y |
| 11 | `APPO_DATE` | Appointment Date | DATE | 7 |  | Y |
| 12 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | Y |
| 13 | `CON_CODE` | Consignee Code | VARCHAR2 | 10 |  | Y |
| 14 | `SHIP_CODE` | Shipper Code | VARCHAR2 | 10 |  | Y |
| 15 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | Y |
| 16 | `APPO_START_DATE` | Appo_Startessorial Date | DATE | 7 |  | Y |
| 17 | `APPO_LAPSE_TIME` | Appo_Lapseessorial Time | NUMBER | 22 | 5 | Y |
| 18 | `APPO_END_DATE` | Appo_Endessorial Date | DATE | 7 |  | Y |
| 19 | `APPO_DES` | Appoessorial Des | VARCHAR2 | 30 |  | Y |
| 20 | `APPO_REM` | Appoessorial Rem | VARCHAR2 | 1000 |  | Y |
| 21 | `CREATE_DATE` | Create Date | DATE | 7 |  | N |
| 22 | `PROS_DATE` | Prosessorial Date | DATE | 7 |  | Y |
| 23 | `PROS_FLAG` | Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 24 | `ERR_MES` | Erressorial Mes | VARCHAR2 | 250 |  | Y |
| 25 | `CONTAINER_ID` | Containeressorial Id | VARCHAR2 | 50 |  | Y |
| 26 | `CONTAINER_SEAL_ID` | Container_Sealessorial Id | VARCHAR2 | 50 |  | Y |

## `EV_M_LABEL_ML`

- **Tipo:** Misc
- **Categoria:** Label
- **Campos:** 7

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `APP_CODE` | Application Code | VARCHAR2 | 10 |  | N |
| 2 | `ENTITY_CODE` | Entityessorial Code | VARCHAR2 | 40 |  | N |
| 3 | `LABEL_CODE` | Labelessorial Code | VARCHAR2 | 50 |  | N |
| 4 | `LABEL_SUB_CODE` | Label_Subessorial Code | VARCHAR2 | 20 |  | N |
| 5 | `LANG_CODE` | Language Code | VARCHAR2 | 4 |  | N |
| 6 | `LABEL_TEXT` | Labelessorial Text | VARCHAR2 | 512 |  | Y |
| 7 | `LABEL_TEXT_HINT` | Label_Textessorial Hint | VARCHAR2 | 80 |  | Y |

## `EV_S_LABEL_ML`

- **Tipo:** Misc
- **Categoria:** Label
- **Campos:** 6

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `APP_CODE` | Application Code | VARCHAR2 | 10 |  | N |
| 2 | `ENTITY_CODE` | Entityessorial Code | VARCHAR2 | 40 |  | N |
| 3 | `LABEL_CODE` | Labelessorial Code | VARCHAR2 | 50 |  | N |
| 4 | `LABEL_SUB_CODE` | Label_Subessorial Code | VARCHAR2 | 20 |  | N |
| 5 | `LABEL_TEXT` | Labelessorial Text | VARCHAR2 | 512 |  | N |
| 6 | `LABEL_TEXT_HINT` | Label_Textessorial Hint | VARCHAR2 | 80 |  | Y |

## `M_LABEL`

- **Tipo:** Master
- **Categoria:** Label
- **Campos:** 7

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COL_NAME` | Column Name | VARCHAR2 | 30 |  | N |
| 2 | `LANG_CODE` | Language Code | VARCHAR2 | 4 |  | N |
| 3 | `VERT_CODE` | Vertessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `CLASS_NAME` | Class Name | VARCHAR2 | 80 |  | N |
| 5 | `TEXT_SHORT` | Textessorial Short | VARCHAR2 | 8 |  | Y |
| 6 | `TEXT_MED` | Textessorial Med | VARCHAR2 | 40 |  | N |
| 7 | `TEXT_LONG` | Textessorial Long | VARCHAR2 | 160 |  | Y |

## `M_LABEL_ML`

- **Tipo:** Master
- **Categoria:** Label
- **Campos:** 13

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `APP_CODE` | Application Code | VARCHAR2 | 10 |  | N |
| 3 | `ENTITY_CODE` | Entityessorial Code | VARCHAR2 | 40 |  | N |
| 4 | `LABEL_CODE` | Labelessorial Code | VARCHAR2 | 50 |  | N |
| 5 | `LABEL_SUB_CODE` | Label_Subessorial Code | VARCHAR2 | 20 |  | N |
| 6 | `LANG_CODE` | Language Code | VARCHAR2 | 4 |  | N |
| 7 | `LABEL_TEXT` | Labelessorial Text | VARCHAR2 | 512 |  | Y |
| 8 | `LABEL_TEXT_HINT` | Label_Textessorial Hint | VARCHAR2 | 80 |  | Y |
| 9 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 10 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 12 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 13 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `S_LABEL`

- **Tipo:** System Setup Related
- **Categoria:** Label
- **Campos:** 7

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COL_NAME` | Column Name | VARCHAR2 | 30 |  | N |
| 2 | `LANG_CODE` | Language Code | VARCHAR2 | 4 |  | N |
| 3 | `VERT_CODE` | Vertessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `CLASS_NAME` | Class Name | VARCHAR2 | 80 |  | N |
| 5 | `TEXT_SHORT` | Textessorial Short | VARCHAR2 | 8 |  | Y |
| 6 | `TEXT_MED` | Textessorial Med | VARCHAR2 | 40 |  | N |
| 7 | `TEXT_LONG` | Textessorial Long | VARCHAR2 | 160 |  | Y |

## `S_LABEL_ML`

- **Tipo:** System Setup Related
- **Categoria:** Label
- **Campos:** 13

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `APP_CODE` | Application Code | VARCHAR2 | 10 |  | N |
| 3 | `ENTITY_CODE` | Entityessorial Code | VARCHAR2 | 40 |  | N |
| 4 | `LABEL_CODE` | Labelessorial Code | VARCHAR2 | 50 |  | N |
| 5 | `LABEL_SUB_CODE` | Label_Subessorial Code | VARCHAR2 | 20 |  | N |
| 6 | `LABEL_TEXT` | Labelessorial Text | VARCHAR2 | 512 |  | N |
| 7 | `LABEL_TEXT_HINT` | Label_Textessorial Hint | VARCHAR2 | 80 |  | Y |
| 8 | `LABEL_ID` | Labelessorial Id | NUMBER | 22 | 4 | Y |
| 9 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 10 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 12 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 13 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `T_LABEL_DS`

- **Tipo:** Temporary
- **Categoria:** Label
- **Campos:** 86
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `DOC_NUM` | Document Number | NUMBER | 22 | 9 | N |
| 5 | `DOC_LINE_NUM` | Document Line Number | NUMBER | 22 | 4 | Y |
| 6 | `DOC_CODE` | Document Code | VARCHAR2 | 4 |  | N |
| 7 | `LABEL_DS_DOC_TP` | Label_Ds_Docessorial Tp | VARCHAR2 | 1 |  | N |
| 8 | `LABEL_CNT` | Labelessorial Cnt | NUMBER | 22 | 9 | Y |
| 9 | `LABEL_CNT_TOT` | Label_Cntessorial Tot | NUMBER | 22 | 9 | Y |
| 10 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | Y |
| 11 | `CUST_NAME` | Customer Name | VARCHAR2 | 30 |  | Y |
| 12 | `CUST_ADD1` | Custessorial Add1 | VARCHAR2 | 30 |  | Y |
| 13 | `CUST_ADD2` | Custessorial Add2 | VARCHAR2 | 30 |  | Y |
| 14 | `CUST_ADD3` | Custessorial Add3 | VARCHAR2 | 30 |  | Y |
| 15 | `CUST_ADD4` | Custessorial Add4 | VARCHAR2 | 30 |  | Y |
| 16 | `CUST_CITY` | Custessorial City | VARCHAR2 | 30 |  | Y |
| 17 | `CUST_ZIP` | Custessorial Zip | VARCHAR2 | 10 |  | Y |
| 18 | `CUST_STATE` | Custessorial State | VARCHAR2 | 4 |  | Y |
| 19 | `CUST_COUNTRY` | Custessorial Country | VARCHAR2 | 4 |  | Y |
| 20 | `DOC_REF1` | Docessorial Ref1 | VARCHAR2 | 20 |  | Y |
| 21 | `DOC_REF2` | Docessorial Ref2 | VARCHAR2 | 20 |  | Y |
| 22 | `DOC_REF3` | Docessorial Ref3 | VARCHAR2 | 20 |  | Y |
| 23 | `DOC_REF4` | Docessorial Ref4 | VARCHAR2 | 20 |  | Y |
| 24 | `CON_SHIP_CODE` | Consignee Ship Code | VARCHAR2 | 10 |  | Y |
| 25 | `CON_SHIP_NAME` | Con_Shipessorial Name | VARCHAR2 | 30 |  | Y |
| 26 | `CON_SHIP_ADD1` | Con_Shipessorial Add1 | VARCHAR2 | 30 |  | Y |
| 27 | `CON_SHIP_ADD2` | Con_Shipessorial Add2 | VARCHAR2 | 30 |  | Y |
| 28 | `CON_SHIP_ADD3` | Con_Shipessorial Add3 | VARCHAR2 | 30 |  | Y |
| 29 | `CON_SHIP_ADD4` | Con_Shipessorial Add4 | VARCHAR2 | 30 |  | Y |
| 30 | `CON_SHIP_CITY` | Con_Shipessorial City | VARCHAR2 | 30 |  | Y |
| 31 | `CON_SHIP_ZIP` | Con_Shipessorial Zip | VARCHAR2 | 10 |  | Y |
| 32 | `CON_SHIP_STATE` | Con_Shipessorial State | VARCHAR2 | 4 |  | Y |
| 33 | `CON_SHIP_COUNTRY` | Con_Shipessorial Country | VARCHAR2 | 4 |  | Y |
| 34 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 35 | `WHSE_NAME` | Warehouse Name | VARCHAR2 | 30 |  | Y |
| 36 | `WHSE_ADD1` | Whseessorial Add1 | VARCHAR2 | 30 |  | Y |
| 37 | `WHSE_ADD2` | Whseessorial Add2 | VARCHAR2 | 30 |  | Y |
| 38 | `WHSE_ADD3` | Whseessorial Add3 | VARCHAR2 | 30 |  | Y |
| 39 | `WHSE_ADD4` | Whseessorial Add4 | VARCHAR2 | 30 |  | Y |
| 40 | `WHSE_CITY` | Whseessorial City | VARCHAR2 | 30 |  | Y |
| 41 | `WHSE_ZIP` | Warehouse Zip | VARCHAR2 | 10 |  | Y |
| 42 | `WHSE_STATE` | Warehouse State | VARCHAR2 | 4 |  | Y |
| 43 | `WHSE_COUNTRY` | Warehouse Country | VARCHAR2 | 4 |  | Y |
| 44 | `LOAD_TP_CODE` | Load Type Code | VARCHAR2 | 4 |  | Y |
| 45 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | Y |
| 46 | `CARR_NAME` | Carrier Name | VARCHAR2 | 30 |  | Y |
| 47 | `CARR_SCAC` | Carressorial Scac | VARCHAR2 | 4 |  | Y |
| 48 | `DOC_DATE` | Docessorial Date | DATE | 7 |  | Y |
| 49 | `DOC_SHIP_DATE` | Doc_Shipessorial Date | DATE | 7 |  | Y |
| 50 | `DOC_ARR_DATE` | Doc_Arressorial Date | DATE | 7 |  | Y |
| 51 | `DOC_DATE_STR` | Doc_Dateessorial Str | VARCHAR2 | 8 |  | Y |
| 52 | `DOC_SHIP_DATE_STR` | Doc_Ship_Dateessorial Str | VARCHAR2 | 8 |  | Y |
| 53 | `DOC_ARR_DATE_STR` | Doc_Arr_Dateessorial Str | VARCHAR2 | 8 |  | Y |
| 54 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | Y |
| 55 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | Y |
| 56 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | Y |
| 57 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | Y |
| 58 | `INVT_EXPY_DATE` | Invt_Expyessorial Date | DATE | 7 |  | Y |
| 59 | `INVT_EXPY_DATE_STR` | Invt_Expy_Dateessorial Str | VARCHAR2 | 8 |  | Y |
| 60 | `ITEM_GTIN_CODE` | Item_Gtinessorial Code | VARCHAR2 | 20 |  | Y |
| 61 | `ITEM_DES1` | Item Code Description 1 | VARCHAR2 | 40 |  | Y |
| 62 | `ITEM_DES2` | Item Code Description 2 | VARCHAR2 | 60 |  | Y |
| 63 | `CART_ID` | Cart ID | VARCHAR2 | 40 |  | Y |
| 64 | `CART_UCC128_NUM` | Cart_Ucc128essorial Num | VARCHAR2 | 40 |  | Y |
| 65 | `CART_CARR_TRACK_NUM` | Cart_Carr_Trackessorial Num | VARCHAR2 | 40 |  | Y |
| 66 | `CART_IND_NUM` | Cart_Indessorial Num | NUMBER | 22 | 9 | Y |
| 67 | `CART_IND_MAX` | Cart_Indessorial Max | NUMBER | 22 | 9 | Y |
| 68 | `CART_SIZE_CODE` | Cart_Sizeessorial Code | VARCHAR2 | 4 |  | Y |
| 69 | `PALL_CODE` | Pallessorial Code | VARCHAR2 | 4 |  | Y |
| 70 | `LABEL_DS_QTY` | Label_Dsessorial Qty | NUMBER | 22 | 9 | Y |
| 71 | `LABEL_DS_WGT` | Label_Dsessorial Wgt | NUMBER | 22 | 16 | Y |
| 72 | `CART_SIZE_WGT` | Cart_Sizeessorial Wgt | NUMBER | 22 | 16 | Y |
| 73 | `PALL_TP_WGT` | Pall_Tpessorial Wgt | NUMBER | 22 | 16 | Y |
| 74 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | Y |
| 75 | `LABEL_DS_VAR_WGT_FLAG` | Label_Ds_Var_Wgtessorial Flag | VARCHAR2 | 1 |  | Y |
| 76 | `LABEL_DS_PACK_TP` | Label_Ds_Packessorial Tp | VARCHAR2 | 4 |  | Y |
| 77 | `LABEL_DS_MISC_FIELD1` | Label_Ds_Miscessorial Field1 | VARCHAR2 | 80 |  | Y |
| 78 | `LABEL_DS_MISC_FIELD2` | Label_Ds_Miscessorial Field2 | VARCHAR2 | 80 |  | Y |
| 79 | `LABEL_DS_MISC_FIELD3` | Label_Ds_Miscessorial Field3 | VARCHAR2 | 80 |  | Y |
| 80 | `LABEL_DS_MISC_FIELD4` | Label_Ds_Miscessorial Field4 | VARCHAR2 | 80 |  | Y |
| 81 | `LABEL_DS_MISC_FIELD5` | Label_Ds_Miscessorial Field5 | VARCHAR2 | 80 |  | Y |
| 82 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 83 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 84 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 85 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 86 | `VERSION` | Version | NUMBER | 22 | 9 | N |

