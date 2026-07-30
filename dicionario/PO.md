# Tabelas — PO

> Categoria extraída da planilha `Tables-Database.xlsx`. Total de tabelas: **7**.

## `E_PO_D1`

- **Tipo:** Transactional
- **Categoria:** PO
- **Campos:** 5
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `PO_NUM` | PO Number | NUMBER | 22 | 9 | N |
| 3 | `PO_LINE_NUM` | Po_Lineessorial Num | NUMBER | 22 | 4 | N |
| 4 | `PO_REM_LINE_NUM` | Po_Rem_Lineessorial Num | NUMBER | 22 | 3 | N |
| 5 | `PO_REM_LINE_TEXT` | Po_Rem_Lineessorial Text | VARCHAR2 | 45 |  | Y |

## `E_PO_D2`

- **Tipo:** Transactional
- **Categoria:** PO
- **Campos:** 35
- **Campos-chave prováveis:** COMP_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4, HOLD_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `PO_NUM` | PO Number | NUMBER | 22 | 9 | N |
| 3 | `PO_LINE_NUM` | Po_Lineessorial Num | NUMBER | 22 | 4 | N |
| 4 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 5 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | Y |
| 6 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | Y |
| 7 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | Y |
| 8 | `PO_LINE_REF_NUM` | Po_Line_Refessorial Num | VARCHAR2 | 20 |  | Y |
| 9 | `PO_ORD_QTY` | Po_Ordessorial Qty | NUMBER | 22 | 9 | N |
| 10 | `PO_ON_RCPT_QTY` | Po_On_Rcptessorial Qty | NUMBER | 22 | 9 | N |
| 11 | `PO_RECD_QTY` | Po_Recdessorial Qty | NUMBER | 22 | 9 | N |
| 12 | `PO_TLR_OVER` | Po_Tlressorial Over | NUMBER | 22 | 9 | Y |
| 13 | `PO_TLR_SHORT` | Po_Tlressorial Short | NUMBER | 22 | 9 | Y |
| 14 | `PO_TLR_TP_FLAG` | Po_Tlr_Tpessorial Flag | VARCHAR2 | 1 |  | Y |
| 15 | `PO_LINE_EDI_INFO_FLAG` | Po_Line_Edi_Infoessorial Flag | VARCHAR2 | 1 |  | N |
| 16 | `PO_LINE_EXPT_DATE` | Po_Line_Exptessorial Date | DATE | 7 |  | Y |
| 17 | `PO_LINE_PRICE` | Po_Lineessorial Price | NUMBER | 22 | 12 | Y |
| 18 | `PO_LINE_COST` | Po_Lineessorial Cost | NUMBER | 22 | 12 | Y |
| 19 | `PO_LINE_REM_FLAG` | Po_Line_Remessorial Flag | VARCHAR2 | 1 |  | N |
| 20 | `PO_LINE_DISC_PRICE` | Po_Line_Discessorial Price | NUMBER | 22 | 12 | Y |
| 21 | `SKU_CODE_FACT` | Sku_Codeessorial Fact | VARCHAR2 | 20 |  | Y |
| 22 | `INVT_QTY_BKD_FACT` | Invt_Qty_Bkdessorial Fact | VARCHAR2 | 30 |  | Y |
| 23 | `DIST_TP_CODE` | Dist_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 24 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |
| 25 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | Y |
| 26 | `PO_LINE_EXT_ID` | Po_Line_Extessorial Id | VARCHAR2 | 40 |  | Y |
| 27 | `INVT_LEV2_DES` | Invt_Lev2essorial Des | VARCHAR2 | 40 |  | Y |
| 28 | `INVT_LEV3_DES` | Invt_Lev3essorial Des | VARCHAR2 | 40 |  | Y |
| 29 | `INVT_LEV4_DES` | Invt_Lev4essorial Des | VARCHAR2 | 40 |  | Y |
| 30 | `PO_ORD_WGT` | Po_Ordessorial Wgt | NUMBER | 22 | 16 | Y |
| 31 | `PO_ORD_WGT_NET` | Po_Ord_Wgtessorial Net | NUMBER | 22 | 16 | Y |
| 32 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | Y |
| 33 | `PO_ORD_VALUE_ORG` | Po_Ord_Valueessorial Org | NUMBER | 22 | 16 | Y |
| 34 | `PO_ORD_VALUE_FACT` | Po_Ord_Valueessorial Fact | NUMBER | 22 | 16 | Y |
| 35 | `PO_ORD_UOM` | Po_Ordessorial Uom | VARCHAR2 | 20 |  | Y |

## `E_PO_D2D1`

- **Tipo:** Transactional
- **Categoria:** PO
- **Campos:** 5
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `PO_NUM` | PO Number | NUMBER | 22 | 9 | N |
| 3 | `PO_LINE_NUM` | Po_Lineessorial Num | NUMBER | 22 | 4 | N |
| 4 | `CON_CODE` | Consignee Code | VARCHAR2 | 10 |  | N |
| 5 | `PO_CON_QTY` | Po_Conessorial Qty | NUMBER | 22 | 9 | N |

## `E_PO_D2D2`

- **Tipo:** Transactional
- **Categoria:** PO
- **Campos:** 5
- **Campos-chave prováveis:** COMP_CODE, RCPT_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `PO_NUM` | PO Number | NUMBER | 22 | 9 | N |
| 3 | `PO_LINE_NUM` | Po_Lineessorial Num | NUMBER | 22 | 4 | N |
| 4 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | N |
| 5 | `RCPT_LINE_NUM` | Receipt Line Number | NUMBER | 22 | 4 | N |

## `E_PO_D3`

- **Tipo:** Transactional
- **Categoria:** PO
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `PO_NUM` | PO Number | NUMBER | 22 | 9 | N |
| 3 | `PO_START_DATE` | Po_Startessorial Date | DATE | 7 |  | N |
| 4 | `PO_END_DATE` | Po_Endessorial Date | DATE | 7 |  | N |

## `E_PO_D4`

- **Tipo:** Transactional
- **Categoria:** PO
- **Campos:** 14
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `PO_NUM` | PO Number | NUMBER | 22 | 9 | N |
| 3 | `PO_LINE_NUM` | Po_Lineessorial Num | NUMBER | 22 | 4 | N |
| 4 | `EDI_PROF_CODE` | Edi_Professorial Code | VARCHAR2 | 4 |  | N |
| 5 | `EDI_TRANS_SET_CODE` | Edi_Trans_Setessorial Code | VARCHAR2 | 4 |  | N |
| 6 | `EDI_DATA_ID_CODE` | Edi_Data_Idessorial Code | VARCHAR2 | 20 |  | N |
| 7 | `EDI_DATA_ID_DES` | Edi_Data_Idessorial Des | VARCHAR2 | 30 |  | N |
| 8 | `EDI_DATA_ID_SEND_FLAG` | Edi_Data_Id_Sendessorial Flag | VARCHAR2 | 1 |  | N |
| 9 | `EDI_DATA_ID_ENTRY_TP_FLAG` | Edi_Data_Id_Entry_Tpessorial Flag | VARCHAR2 | 1 |  | N |
| 10 | `EDI_DATA_ID_LINE_ENTRY_FLAG` | Edi_Data_Id_Line_Entryessorial Flag | VARCHAR2 | 1 |  | N |
| 11 | `EDI_DATA_ID_MAND_FLAG` | Edi_Data_Id_Mandessorial Flag | VARCHAR2 | 1 |  | N |
| 12 | `EDI_DATA_ID_LEN` | Edi_Data_Idessorial Len | VARCHAR2 | 6 |  | N |
| 13 | `COL_TP_CODE` | Col_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 14 | `EDI_DATA_ID_VALUE` | Edi_Data_Idessorial Value | VARCHAR2 | 250 |  | Y |

## `E_PO_H`

- **Tipo:** Transactional
- **Categoria:** PO
- **Campos:** 21
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `PO_NUM` | PO Number | NUMBER | 22 | 9 | N |
| 3 | `PO_STAT` | Poessorial Stat | VARCHAR2 | 1 |  | N |
| 4 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 5 | `PO_DATE` | Poessorial Date | DATE | 7 |  | N |
| 6 | `SHIP_CODE` | Shipper Code | VARCHAR2 | 10 |  | N |
| 7 | `CON_CODE` | Consignee Code | VARCHAR2 | 10 |  | Y |
| 8 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 9 | `PO_CONF_FLAG` | Po_Confessorial Flag | VARCHAR2 | 1 |  | N |
| 10 | `PO_REM_FLAG` | Po_Remessorial Flag | VARCHAR2 | 1 |  | N |
| 11 | `PO_REF1` | Poessorial Ref1 | VARCHAR2 | 20 |  | Y |
| 12 | `PO_REF2` | Poessorial Ref2 | VARCHAR2 | 20 |  | Y |
| 13 | `PO_REF3` | Poessorial Ref3 | VARCHAR2 | 20 |  | Y |
| 14 | `PO_REF4` | Poessorial Ref4 | VARCHAR2 | 20 |  | Y |
| 15 | `PO_DEP_NUM` | Po_Depessorial Num | VARCHAR2 | 10 |  | Y |
| 16 | `EDI_INFO_FLAG` | Edi_Infoessorial Flag | VARCHAR2 | 1 |  | N |
| 17 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 18 | `DIST_TP_CODE` | Dist_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 19 | `PO_ASN_NUM` | Po_Asnessorial Num | NUMBER | 22 | 3 | Y |
| 20 | `PO_ALLOW_ENTRY_LEV_NUM` | Po_Allow_Entry_Levessorial Num | NUMBER | 22 | 1 | Y |
| 21 | `TRANS_TP_CODE` | Trans_Tpessorial Code | VARCHAR2 | 4 |  | Y |

