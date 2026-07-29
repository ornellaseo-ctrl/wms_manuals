# Tabelas — Receipts

> Categoria extraída da planilha `Tables-Database.xlsx`. Total de tabelas: **93**.

## `A3PL_ORG_RCT_NUM`

- **Tipo:** Misc
- **Categoria:** Receipts
- **Campos:** 7
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 4 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | N |
| 5 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | N |
| 6 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | N |
| 7 | `ORG_RCPT_NUM` | Org_Rcptessorial Num | VARCHAR2 | 9 |  | Y |

## `C_CREATE_RCPT_D`

- **Tipo:** Transactional
- **Categoria:** Receipts
- **Campos:** 9
- **Campos-chave prováveis:** INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `RCPT_SEQ_NUM` | Rcpt_Seqessorial Num | NUMBER | 22 | 6 | Y |
| 2 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | Y |
| 3 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | Y |
| 4 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | Y |
| 5 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | Y |
| 6 | `INVT_LEV5` | Inventory Level 5 | VARCHAR2 | 40 |  | Y |
| 7 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 8 | `RCPT_RECD_QTY` | Rcpt_Recdessorial Qty | NUMBER | 22 | 9 | Y |
| 9 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |

## `C_CREATE_RCPT_H`

- **Tipo:** Transactional
- **Categoria:** Receipts
- **Campos:** 18
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `RCPT_SEQ_NUM` | Rcpt_Seqessorial Num | NUMBER | 22 | 6 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | Y |
| 3 | `RCPT_TP` | Rcptessorial Tp | VARCHAR2 | 1 |  | Y |
| 4 | `RCPT_PRTY_NUM` | Rcpt_Prtyessorial Num | NUMBER | 22 | 1 | Y |
| 5 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | Y |
| 6 | `SHIP_CODE` | Shipper Code | VARCHAR2 | 10 |  | Y |
| 7 | `SHIP_NAME` | Shipessorial Name | VARCHAR2 | 30 |  | Y |
| 8 | `CUST_CODE_BILL_TO` | Cust_Code_Billessorial To | VARCHAR2 | 10 |  | Y |
| 9 | `RCPT_DATE` | Rcptessorial Date | DATE | 7 |  | Y |
| 10 | `RCPT_PRO_BILL_NUM` | Rcpt_Pro_Billessorial Num | VARCHAR2 | 20 |  | Y |
| 11 | `RCPT_REF_NUM` | Rcpt_Refessorial Num | VARCHAR2 | 20 |  | Y |
| 12 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | Y |
| 13 | `CARR_NAME` | Carrier Name | VARCHAR2 | 30 |  | Y |
| 14 | `LOAD_TP_CODE` | Load Type Code | VARCHAR2 | 4 |  | Y |
| 15 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | Y |
| 16 | `RCPT_ALT_REF1` | Rcpt_Altessorial Ref1 | VARCHAR2 | 20 |  | Y |
| 17 | `RCPT_ALT_REF2` | Rcpt_Altessorial Ref2 | VARCHAR2 | 20 |  | Y |
| 18 | `LOAD_NUM` | Load Number | NUMBER | 22 | 6 | Y |

## `C_CREATE_RCPT_TRIG`

- **Tipo:** Transactional
- **Categoria:** Receipts
- **Campos:** 2

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `RCPT_SEQ_NUM` | Rcpt_Seqessorial Num | NUMBER | 22 | 6 | N |
| 2 | `COMP_ID` | Compessorial Id | VARCHAR2 | 10 |  | Y |

## `C_RCPT_PEND`

- **Tipo:** Transactional
- **Categoria:** Receipts
- **Campos:** 14
- **Campos-chave prováveis:** COMP_CODE, RCPT_NUM, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | N |
| 3 | `RCPT_LINE_NUM` | Receipt Line Number | NUMBER | 22 | 4 | N |
| 4 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 5 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 6 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | N |
| 7 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | N |
| 8 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | N |
| 9 | `INVT_LEV5` | Inventory Level 5 | VARCHAR2 | 40 |  | Y |
| 10 | `RCPT_PEND_QTY` | Rcpt_Pendessorial Qty | NUMBER | 22 | 9 | N |
| 11 | `RCPT_PEND_WGT` | Rcpt_Pendessorial Wgt | NUMBER | 22 | 16 | N |
| 12 | `RCPT_PEND_CUBE` | Rcpt_Pendessorial Cube | NUMBER | 22 | 16 | N |
| 13 | `RCPT_TP` | Rcptessorial Tp | VARCHAR2 | 1 |  | N |
| 14 | `RCPT_DATE` | Rcptessorial Date | DATE | 7 |  | N |

## `C_RCPT_STAT`

- **Tipo:** Transactional
- **Categoria:** Receipts
- **Campos:** 9
- **Campos-chave prováveis:** COMP_CODE, RCPT_NUM, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | N |
| 3 | `RCPT_LINE_NUM` | Receipt Line Number | NUMBER | 22 | 4 | N |
| 4 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 5 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 6 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | Y |
| 7 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | Y |
| 8 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | Y |
| 9 | `INVT_LEV5` | Inventory Level 5 | VARCHAR2 | 40 |  | Y |

## `C_SHIP_CART`

- **Tipo:** Transactional
- **Categoria:** Receipts
- **Campos:** 2
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `SHIP_CART_ID` | Ship_Cartessorial Id | VARCHAR2 | 20 |  | N |

## `C_SHIP_SORT`

- **Tipo:** Transactional
- **Categoria:** Receipts
- **Campos:** 14
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `SHIP_SORT_SEQ_NUM` | Ship_Sort_Seqessorial Num | NUMBER | 22 | 9 | N |
| 3 | `SHIP_SORT_ROUTE_ID` | Ship_Sort_Routeessorial Id | VARCHAR2 | 10 |  | N |
| 4 | `SHIP_SORT_LANE_ID` | Ship_Sort_Laneessorial Id | VARCHAR2 | 10 |  | N |
| 5 | `CON_CODE` | Consignee Code | VARCHAR2 | 10 |  | N |
| 6 | `SHIP_SORT_CART_ID` | Ship_Sort_Cartessorial Id | VARCHAR2 | 20 |  | N |
| 7 | `SHIP_SORT_CART_DATE` | Ship_Sort_Cartessorial Date | DATE | 7 |  | N |
| 8 | `SHIP_SORT_CART_WGT` | Ship_Sort_Cartessorial Wgt | NUMBER | 22 | 16 | N |
| 9 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | N |
| 10 | `SHIP_SORT_CART_CUBE` | Ship_Sort_Cartessorial Cube | NUMBER | 22 | 16 | N |
| 11 | `LINEAR_MEAS_CODE` | Linear Measurement Code | VARCHAR2 | 4 |  | N |
| 12 | `SHIP_SORT_CART_HGT` | Ship_Sort_Cartessorial Hgt | NUMBER | 22 | 7 | Y |
| 13 | `SHIP_SORT_CART_WID` | Ship_Sort_Cartessorial Wid | NUMBER | 22 | 7 | Y |
| 14 | `SHIP_SORT_CART_LEN` | Ship_Sort_Cartessorial Len | NUMBER | 22 | 7 | Y |

## `EVCORIN`

- **Tipo:** Misc
- **Categoria:** Receipts
- **Campos:** 24

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `BOXID` | Boxidessorial Boxid | VARCHAR2 | 20 |  | N |
| 2 | `ORDERID` | Orderidessorial Orderid | VARCHAR2 | 20 |  | N |
| 3 | `PONO` | Ponoessorial Pono | NUMBER | 22 | 10 | Y |
| 4 | `CUST` | Custessorial Cust | VARCHAR2 | 30 |  | Y |
| 5 | `CONTACT` | Contactessorial Contact | VARCHAR2 | 20 |  | Y |
| 6 | `COMPANYNAME` | Companynameessorial Companyname | VARCHAR2 | 30 |  | Y |
| 7 | `ADDRESS1` | Addressessorial Address1 | VARCHAR2 | 30 |  | Y |
| 8 | `ADDRESS2` | Addressessorial Address2 | VARCHAR2 | 30 |  | Y |
| 9 | `CITY` | Cityessorial City | VARCHAR2 | 30 |  | Y |
| 10 | `STATE` | Stateessorial State | VARCHAR2 | 2 |  | Y |
| 11 | `POSTALCODE` | Postalcodeessorial Postalcode | VARCHAR2 | 15 |  | Y |
| 12 | `PHONE` | Phoneessorial Phone | VARCHAR2 | 15 |  | Y |
| 13 | `SHIPVIA` | Shipviaessorial Shipvia | VARCHAR2 | 10 |  | Y |
| 14 | `FREIGHTERM` | Freightermessorial Freighterm | VARCHAR2 | 10 |  | Y |
| 15 | `INSURANCEAMOUNT` | Insuranceamountessorial Insuranceamount | NUMBER | 22 | 10 | Y |
| 16 | `CODAMOUNT` | Codamountessorial Codamount | NUMBER | 22 | 10 | Y |
| 17 | `BILLTOACCOUNT_NO` | Billtoaccountessorial No | VARCHAR2 | 20 |  | Y |
| 18 | `BILLTONAME` | Billtonameessorial Billtoname | VARCHAR2 | 30 |  | Y |
| 19 | `BILLTOADDRESS1` | Billtoaddressessorial Billtoaddress1 | VARCHAR2 | 30 |  | Y |
| 20 | `BILLTOCITY` | Billtocityessorial Billtocity | VARCHAR2 | 30 |  | Y |
| 21 | `BILLTOSTATE` | Billtostateessorial Billtostate | VARCHAR2 | 2 |  | Y |
| 22 | `BILLTOPOSTALCODE` | Billtopostalcodeessorial Billtopostalcode | VARCHAR2 | 15 |  | Y |
| 23 | `STATUS` | Statusessorial Status | VARCHAR2 | 30 |  | Y |
| 24 | `CUSTORDNUM` | Custordnumessorial Custordnum | VARCHAR2 | 20 |  | Y |

## `E_INB_LOAD_MAN_D`

- **Tipo:** Transactional
- **Categoria:** Receipts
- **Campos:** 5
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `LOAD_NUM` | Load Number | NUMBER | 22 | 6 | N |
| 3 | `PO_NUM` | PO Number | NUMBER | 22 | 9 | N |
| 4 | `PO_REF1` | Poessorial Ref1 | VARCHAR2 | 20 |  | Y |
| 5 | `PO_REF2` | Poessorial Ref2 | VARCHAR2 | 20 |  | Y |

## `E_INB_LOAD_MAN_DD`

- **Tipo:** Transactional
- **Categoria:** Receipts
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE, RCPT_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `LOAD_NUM` | Load Number | NUMBER | 22 | 6 | N |
| 3 | `PO_NUM` | PO Number | NUMBER | 22 | 9 | N |
| 4 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | N |

## `E_INB_LOAD_MAN_H`

- **Tipo:** Transactional
- **Categoria:** Receipts
- **Campos:** 24
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `LOAD_NUM` | Load Number | NUMBER | 22 | 6 | N |
| 3 | `INB_LOAD_CREATE_DATE` | Inb_Load_Createessorial Date | DATE | 7 |  | Y |
| 4 | `INB_LOAD_RCPT_DATE` | Inb_Load_Rcptessorial Date | DATE | 7 |  | N |
| 5 | `DRV_CODE` | Driver Code | VARCHAR2 | 4 |  | Y |
| 6 | `INB_LOAD_CARRY_UNIT_NUM` | Inb_Load_Carry_Unitessorial Num | VARCHAR2 | 20 |  | Y |
| 7 | `INB_LOAD_POW_UNIT_NUM` | Inb_Load_Pow_Unitessorial Num | VARCHAR2 | 20 |  | Y |
| 8 | `INB_LOAD_VES` | Inb_Loadessorial Ves | VARCHAR2 | 20 |  | Y |
| 9 | `INB_LOAD_VOY` | Inb_Loadessorial Voy | VARCHAR2 | 20 |  | Y |
| 10 | `INB_LOAD_SEAL1` | Inb_Loadessorial Seal1 | VARCHAR2 | 20 |  | Y |
| 11 | `INB_LOAD_SEAL2` | Inb_Loadessorial Seal2 | VARCHAR2 | 20 |  | Y |
| 12 | `INB_LOAD_TEMP_FRONT` | Inb_Load_Tempessorial Front | VARCHAR2 | 10 |  | Y |
| 13 | `INB_LOAD_TEMP_MID` | Inb_Load_Tempessorial Mid | VARCHAR2 | 10 |  | Y |
| 14 | `INB_LOAD_TEMP_BACK` | Inb_Load_Tempessorial Back | VARCHAR2 | 10 |  | Y |
| 15 | `INB_LOAD_TEMP_SET` | Inb_Load_Tempessorial Set | VARCHAR2 | 10 |  | Y |
| 16 | `DRV_NAME_MAN` | Drv_Nameessorial Man | VARCHAR2 | 30 |  | Y |
| 17 | `INB_LOAD_GEN_TP` | Inb_Load_Genessorial Tp | VARCHAR2 | 1 |  | N |
| 18 | `INB_LOAD_STAT` | Inb_Loadessorial Stat | VARCHAR2 | 1 |  | N |
| 19 | `INB_LOAD_RCPT_FLAG` | Inb_Load_Rcptessorial Flag | VARCHAR2 | 1 |  | Y |
| 20 | `INB_LOAD_REF1` | Inb_Loadessorial Ref1 | VARCHAR2 | 20 |  | Y |
| 21 | `INB_LOAD_REF2` | Inb_Loadessorial Ref2 | VARCHAR2 | 20 |  | Y |
| 22 | `INB_LOAD_REF3` | Inb_Loadessorial Ref3 | VARCHAR2 | 20 |  | Y |
| 23 | `INB_LOAD_REF4` | Inb_Loadessorial Ref4 | VARCHAR2 | 20 |  | Y |
| 24 | `LOAD_TP_CODE` | Load Type Code | VARCHAR2 | 4 |  | Y |

## `E_PROS_RCPT`

- **Tipo:** Transactional
- **Categoria:** Receipts
- **Campos:** 9
- **Campos-chave prováveis:** COMP_CODE, RCPT_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | N |
| 3 | `RCPT_PROS_FLAG` | Rcpt_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 4 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 5 | `RCPT_PRTY_NUM` | Rcpt_Prtyessorial Num | NUMBER | 22 | 1 | N |
| 6 | `RCPT_PROS_DATE` | Rcpt_Prosessorial Date | DATE | 7 |  | Y |
| 7 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | Y |
| 8 | `RCPT_PROS_SEQ_NUM` | Rcpt_Pros_Seqessorial Num | NUMBER | 22 | 4 | Y |
| 9 | `RCPT_SORT_CODE` | Rcpt_Sortessorial Code | VARCHAR2 | 20 |  | Y |

## `E_PROS_RCPT_LINE`

- **Tipo:** Transactional
- **Categoria:** Receipts
- **Campos:** 8
- **Campos-chave prováveis:** COMP_CODE, RCPT_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | N |
| 3 | `RCPT_LINE_NUM` | Receipt Line Number | NUMBER | 22 | 4 | N |
| 4 | `RCPT_PROS_FLAG` | Rcpt_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 6 | `RCPT_PRTY_NUM` | Rcpt_Prtyessorial Num | NUMBER | 22 | 1 | N |
| 7 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | Y |
| 8 | `RCPT_SORT_CODE` | Rcpt_Sortessorial Code | VARCHAR2 | 20 |  | Y |

## `E_RCPT_D1`

- **Tipo:** Transactional
- **Categoria:** Receipts
- **Campos:** 14
- **Campos-chave prováveis:** COMP_CODE, RCPT_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | N |
| 4 | `RCPT_LINE_NUM` | Receipt Line Number | NUMBER | 22 | 4 | N |
| 5 | `CUST_CODE_CHG` | Cust_Codeessorial Chg | VARCHAR2 | 10 |  | Y |
| 6 | `CHG_CODE` | Charge Code | VARCHAR2 | 6 |  | Y |
| 7 | `CHG_DATE` | Charge Date | DATE | 7 |  | Y |
| 8 | `RCPT_REM_LINE_NUM` | Rcpt_Rem_Lineessorial Num | NUMBER | 22 | 3 | N |
| 9 | `RCPT_REM_LINE_TEXT` | Rcpt_Rem_Lineessorial Text | VARCHAR2 | 45 |  | Y |
| 10 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 11 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 13 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 14 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `E_RCPT_D10`

- **Tipo:** Transactional
- **Categoria:** Receipts
- **Campos:** 20
- **Campos-chave prováveis:** COMP_CODE, RCPT_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | N |
| 4 | `RCPT_LINE_NUM` | Receipt Line Number | NUMBER | 22 | 4 | N |
| 5 | `EDI_PROF_CODE` | Edi_Professorial Code | VARCHAR2 | 4 |  | N |
| 6 | `EDI_TRANS_SET_CODE` | Edi_Trans_Setessorial Code | VARCHAR2 | 4 |  | N |
| 7 | `EDI_DATA_ID_CODE` | Edi_Data_Idessorial Code | VARCHAR2 | 20 |  | N |
| 8 | `EDI_DATA_ID_DES` | Edi_Data_Idessorial Des | VARCHAR2 | 30 |  | N |
| 9 | `EDI_DATA_ID_SEND_FLAG` | Edi_Data_Id_Sendessorial Flag | VARCHAR2 | 1 |  | N |
| 10 | `EDI_DATA_ID_ENTRY_TP_FLAG` | Edi_Data_Id_Entry_Tpessorial Flag | VARCHAR2 | 1 |  | N |
| 11 | `EDI_DATA_ID_LINE_ENTRY_FLAG` | Edi_Data_Id_Line_Entryessorial Flag | VARCHAR2 | 1 |  | N |
| 12 | `EDI_DATA_ID_MAND_FLAG` | Edi_Data_Id_Mandessorial Flag | VARCHAR2 | 1 |  | N |
| 13 | `EDI_DATA_ID_LEN` | Edi_Data_Idessorial Len | VARCHAR2 | 6 |  | N |
| 14 | `COL_TP_CODE` | Col_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 15 | `EDI_DATA_ID_VALUE` | Edi_Data_Idessorial Value | VARCHAR2 | 250 |  | Y |
| 16 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 17 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 18 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 19 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 20 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `E_RCPT_D12`

- **Tipo:** Transactional
- **Categoria:** Receipts
- **Campos:** 17
- **Campos-chave prováveis:** COMP_CODE, RCPT_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `RCPT_REM_SEQ_NUM` | Rcpt_Rem_Seqessorial Num | NUMBER | 22 | 9 | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | N |
| 5 | `RCPT_LINE_NUM` | Receipt Line Number | NUMBER | 22 | 4 | N |
| 6 | `RCPT_REM_CUST_FLAG` | Rcpt_Rem_Custessorial Flag | VARCHAR2 | 1 |  | N |
| 7 | `RCPT_REM_SHIP_FLAG` | Rcpt_Rem_Shipessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `RCPT_REM_CARR_FLAG` | Rcpt_Rem_Carressorial Flag | VARCHAR2 | 1 |  | N |
| 9 | `RCPT_REM_RF_FLAG` | Rcpt_Rem_Rfessorial Flag | VARCHAR2 | 1 |  | N |
| 10 | `RCPT_DOC_CODE_REST` | Rcpt_Doc_Codeessorial Rest | VARCHAR2 | 4 |  | Y |
| 11 | `RCPT_REM_MES_CODE` | Rcpt_Rem_Mesessorial Code | VARCHAR2 | 4 |  | Y |
| 12 | `RCPT_REM_TEXT` | Rcpt_Remessorial Text | VARCHAR2 | 2000 |  | Y |
| 13 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 14 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 15 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 16 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 17 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `E_RCPT_D2`

- **Tipo:** Transactional
- **Categoria:** Receipts
- **Campos:** 24
- **Campos-chave prováveis:** COMP_CODE, RCPT_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | N |
| 4 | `RCPT_LINE_NUM` | Receipt Line Number | NUMBER | 22 | 4 | N |
| 5 | `PROF_TP_CODE` | Prof_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 6 | `EXTRA_CHG_PROF_CODE` | Extra_Chg_Professorial Code | VARCHAR2 | 4 |  | N |
| 7 | `EXTRA_CHG_PROF_SEQ_NUM` | Extra_Chg_Prof_Seqessorial Num | NUMBER | 22 | 2 | N |
| 8 | `CHG_CODE` | Charge Code | VARCHAR2 | 6 |  | N |
| 9 | `GRP_CODE` | Grpessorial Code | VARCHAR2 | 4 |  | N |
| 10 | `EXTRA_CHG_PROF_ACTN_FLAG` | Extra_Chg_Prof_Actnessorial Flag | VARCHAR2 | 1 |  | N |
| 11 | `EXTRA_CHG_PROF_ENTRY_TP_FLAG` | Extra_Chg_Prof_Entry_Tpessorial Flag | VARCHAR2 | 1 |  | N |
| 12 | `EXTRA_CHG_PROF_OVRR_QTY_FLAG` | Extra_Chg_Prof_Ovrr_Qtyessorial Flag | VARCHAR2 | 1 |  | N |
| 13 | `EXTRA_CHG_PROF_TREAT_FLAG` | Extra_Chg_Prof_Treatessorial Flag | VARCHAR2 | 1 |  | N |
| 14 | `BILL_TO_TP_CODE` | Bill_To_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 15 | `RCPT_EXTRA_CHG_QTY` | Rcpt_Extra_Chgessorial Qty | NUMBER | 22 | 16 | Y |
| 16 | `RCPT_EXTRA_CHG_PROS_FLAG` | Rcpt_Extra_Chg_Prosessorial Flag | VARCHAR2 | 1 |  | Y |
| 17 | `RCPT_EXTRA_CHG_ACCEPT_FLAG` | Rcpt_Extra_Chg_Acceptessorial Flag | VARCHAR2 | 1 |  | Y |
| 18 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | Y |
| 19 | `RCPT_EXTRA_CHG_LAST_DATE` | Rcpt_Extra_Chg_Lastessorial Date | DATE | 7 |  | Y |
| 20 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 21 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 22 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 23 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 24 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `E_RCPT_D3`

- **Tipo:** Transactional
- **Categoria:** Receipts
- **Campos:** 25
- **Campos-chave prováveis:** COMP_CODE, RCPT_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | N |
| 4 | `DRV_CODE` | Driver Code | VARCHAR2 | 4 |  | Y |
| 5 | `RCPT_POW_UNIT_NUM` | Rcpt_Pow_Unitessorial Num | VARCHAR2 | 20 |  | Y |
| 6 | `RCPT_CARRY_UNIT_NUM` | Rcpt_Carry_Unitessorial Num | VARCHAR2 | 20 |  | Y |
| 7 | `RCPT_VES` | Rcptessorial Ves | VARCHAR2 | 20 |  | Y |
| 8 | `RCPT_VOY` | Rcptessorial Voy | VARCHAR2 | 20 |  | Y |
| 9 | `RCPT_SEAL1` | Rcptessorial Seal1 | VARCHAR2 | 20 |  | Y |
| 10 | `RCPT_SEAL2` | Rcptessorial Seal2 | VARCHAR2 | 20 |  | Y |
| 11 | `RCPT_TEMP_FRONT` | Rcpt_Tempessorial Front | VARCHAR2 | 10 |  | Y |
| 12 | `RCPT_TEMP_MID` | Rcpt_Tempessorial Mid | VARCHAR2 | 10 |  | Y |
| 13 | `RCPT_TEMP_BACK` | Rcpt_Tempessorial Back | VARCHAR2 | 10 |  | Y |
| 14 | `DRV_NAME_MAN` | Drv_Nameessorial Man | VARCHAR2 | 30 |  | Y |
| 15 | `RCPT_SEAL1_INTACT` | Rcpt_Seal1essorial Intact | VARCHAR2 | 1 |  | Y |
| 16 | `RCPT_TEMP_SET` | Rcpt_Tempessorial Set | VARCHAR2 | 10 |  | Y |
| 17 | `RCPT_TEMP_AMB` | Rcpt_Tempessorial Amb | VARCHAR2 | 10 |  | Y |
| 18 | `RCPT_PALL_QTY_IN` | Rcpt_Pall_Qtyessorial In | NUMBER | 22 | 4 | Y |
| 19 | `RCPT_PALL_QTY_OUT` | Rcpt_Pall_Qtyessorial Out | NUMBER | 22 | 4 | Y |
| 20 | `RCPT_TEMP_6` | Rcpt_Tempessorial 6 | VARCHAR2 | 10 |  | Y |
| 21 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 22 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 23 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 24 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 25 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `E_RCPT_D4`

- **Tipo:** Transactional
- **Categoria:** Receipts
- **Campos:** 14
- **Campos-chave prováveis:** COMP_CODE, RCPT_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | N |
| 4 | `PALL_ACC_CODE` | Pall_Accessorial Code | VARCHAR2 | 10 |  | N |
| 5 | `PALL_ACC_TP` | Pall_Accessorial Tp | VARCHAR2 | 4 |  | N |
| 6 | `PALL_TRANS_TP` | Pall_Transessorial Tp | VARCHAR2 | 1 |  | N |
| 7 | `PALL_CODE` | Pallessorial Code | VARCHAR2 | 4 |  | N |
| 8 | `PALL_QTY` | Pallessorial Qty | NUMBER | 22 | 4 | N |
| 9 | `PALL_REF_DES` | Pall_Refessorial Des | VARCHAR2 | 60 |  | Y |
| 10 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 11 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 13 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 14 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `E_RCPT_D5`

- **Tipo:** Transactional
- **Categoria:** Receipts
- **Campos:** 79
- **Campos-chave prováveis:** COMP_CODE, RCPT_NUM, SKU_CODE, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | N |
| 4 | `RCPT_LINE_NUM` | Receipt Line Number | NUMBER | 22 | 4 | N |
| 5 | `RCPT_LINE_TP` | Rcpt_Lineessorial Tp | VARCHAR2 | 1 |  | N |
| 6 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | N |
| 7 | `RCPT_EXPT_ENT_QTY` | Rcpt_Expt_Entessorial Qty | VARCHAR2 | 20 |  | N |
| 8 | `RCPT_RECD_ENT_QTY` | Rcpt_Recd_Entessorial Qty | VARCHAR2 | 20 |  | N |
| 9 | `RCPT_RECD_QTY` | Rcpt_Recdessorial Qty | NUMBER | 22 | 9 | N |
| 10 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | N |
| 11 | `RCPT_UNIT_WGT` | Rcpt_Unitessorial Wgt | NUMBER | 22 | 16 | N |
| 12 | `SKU_CODE` | SKU Code | VARCHAR2 | 4 |  | N |
| 13 | `RCPT_TOT_WGT` | Rcpt_Totessorial Wgt | NUMBER | 22 | 16 | N |
| 14 | `RCPT_TOT_WGT_NET` | Rcpt_Tot_Wgtessorial Net | NUMBER | 22 | 16 | N |
| 15 | `LINEAR_MEAS_CODE` | Linear Measurement Code | VARCHAR2 | 4 |  | N |
| 16 | `RCPT_TOT_CUBE` | Rcpt_Totessorial Cube | NUMBER | 22 | 16 | N |
| 17 | `RCPT_LINE_REM_FLAG` | Rcpt_Line_Remessorial Flag | VARCHAR2 | 1 |  | N |
| 18 | `RCPT_LINE_EXTRA_CHG_FLAG` | Rcpt_Line_Extra_Chgessorial Flag | VARCHAR2 | 1 |  | N |
| 19 | `RCPT_LINE_ALTER_FLAG` | Rcpt_Line_Alteressorial Flag | VARCHAR2 | 1 |  | N |
| 20 | `RCPT_LINE_LOC_BAL_FLAG` | Rcpt_Line_Loc_Balessorial Flag | VARCHAR2 | 1 |  | N |
| 21 | `RCPT_LINE_LOC_GEN_FLAG` | Rcpt_Line_Loc_Genessorial Flag | VARCHAR2 | 1 |  | N |
| 22 | `RCPT_LINE_CONF_FLAG` | Rcpt_Line_Confessorial Flag | VARCHAR2 | 1 |  | N |
| 23 | `RCPT_LINE_RATE_FLAG` | Rcpt_Line_Rateessorial Flag | VARCHAR2 | 1 |  | N |
| 24 | `RCPT_LINE_EDI_INFO_FLAG` | Rcpt_Line_Edi_Infoessorial Flag | VARCHAR2 | 1 |  | N |
| 25 | `RCPT_LINE_ITEM_PROS_FLAG` | Rcpt_Line_Item_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 26 | `RCPT_LEV1` | Rcptessorial Lev1 | VARCHAR2 | 40 |  | Y |
| 27 | `RCPT_SEQ_QTY_LEV1` | Rcpt_Seq_Qtyessorial Lev1 | NUMBER | 22 | 4 | Y |
| 28 | `RCPT_LEV2` | Rcptessorial Lev2 | VARCHAR2 | 40 |  | Y |
| 29 | `RCPT_SEQ_QTY_LEV2` | Rcpt_Seq_Qtyessorial Lev2 | NUMBER | 22 | 4 | Y |
| 30 | `RCPT_LEV3` | Rcptessorial Lev3 | VARCHAR2 | 40 |  | Y |
| 31 | `RCPT_SEQ_QTY_LEV3` | Rcpt_Seq_Qtyessorial Lev3 | NUMBER | 22 | 4 | Y |
| 32 | `RCPT_LEV4` | Rcptessorial Lev4 | VARCHAR2 | 40 |  | Y |
| 33 | `RCPT_SEQ_QTY_LEV4` | Rcpt_Seq_Qtyessorial Lev4 | NUMBER | 22 | 4 | Y |
| 34 | `RCPT_LEV5` | Rcptessorial Lev5 | VARCHAR2 | 40 |  | Y |
| 35 | `RCPT_SEQ_QTY_LEV5` | Rcpt_Seq_Qtyessorial Lev5 | NUMBER | 22 | 4 | Y |
| 36 | `RCPT_CLS_DATE` | Rcpt_Clsessorial Date | DATE | 7 |  | Y |
| 37 | `RCPT_EXPY_DATE` | Rcpt_Expyessorial Date | DATE | 7 |  | Y |
| 38 | `RCPT_LINE_CONF_DATE` | Rcpt_Line_Confessorial Date | DATE | 7 |  | Y |
| 39 | `RCPT_LINE_LEN` | Rcpt_Lineessorial Len | NUMBER | 22 | 16 | Y |
| 40 | `RCPT_LINE_WID` | Rcpt_Lineessorial Wid | NUMBER | 22 | 16 | Y |
| 41 | `RCPT_LINE_HGT` | Rcpt_Lineessorial Hgt | NUMBER | 22 | 16 | Y |
| 42 | `RCPT_LINE_TEMP` | Rcpt_Lineessorial Temp | NUMBER | 22 | 5 | Y |
| 43 | `CRS_DOCK_PROF_CODE` | Crs_Dock_Professorial Code | VARCHAR2 | 4 |  | Y |
| 44 | `RCPT_LEV_DES1` | Rcpt_Levessorial Des1 | VARCHAR2 | 40 |  | Y |
| 45 | `RCPT_LEV_DES2` | Rcpt_Levessorial Des2 | VARCHAR2 | 40 |  | Y |
| 46 | `RCPT_LEV_DES3` | Rcpt_Levessorial Des3 | VARCHAR2 | 40 |  | Y |
| 47 | `RCPT_LEV_DES4` | Rcpt_Levessorial Des4 | VARCHAR2 | 40 |  | Y |
| 48 | `RCPT_LEV_DES5` | Rcpt_Levessorial Des5 | VARCHAR2 | 40 |  | Y |
| 49 | `INVT_QTY_BKD_FACT` | Invt_Qty_Bkdessorial Fact | VARCHAR2 | 30 |  | Y |
| 50 | `REAS_CODE` | Reasessorial Code | VARCHAR2 | 4 |  | Y |
| 51 | `RCPT_DIST_ORD_NUM` | Rcpt_Dist_Ordessorial Num | NUMBER | 22 | 9 | Y |
| 52 | `RCPT_DIST_ORD_LINE_NUM` | Rcpt_Dist_Ord_Lineessorial Num | NUMBER | 22 | 4 | Y |
| 53 | `BOND_NUM` | Bond Number | VARCHAR2 | 20 |  | Y |
| 54 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |
| 55 | `RCPT_LINE_SRCE_LINE` | Rcpt_Line_Srceessorial Line | NUMBER | 22 | 4 | Y |
| 56 | `RCPT_EXT_INV_NUM` | Rcpt_Ext_Invessorial Num | NUMBER | 22 | 16 | Y |
| 57 | `RCPT_EXT_INV_PREX` | Rcpt_Ext_Invessorial Prex | VARCHAR2 | 4 |  | Y |
| 58 | `RCPT_EXT_INV_DATE` | Rcpt_Ext_Invessorial Date | DATE | 7 |  | Y |
| 59 | `WHSE_CODE_REST` | Whse_Codeessorial Rest | VARCHAR2 | 4 |  | Y |
| 60 | `PO_LINE_NUM` | Po_Lineessorial Num | NUMBER | 22 | 4 | Y |
| 61 | `PO_NUM` | PO Number | NUMBER | 22 | 9 | Y |
| 62 | `RCPT_LINE_NUM_UPDOWNSTREAM` | Rcpt_Line_Numessorial Updownstream | NUMBER | 22 | 4 | Y |
| 63 | `RCPT_LINE_SKIP_PUTAWAY_FLAG` | Rcpt_Line_Skip_Putawayessorial Flag | VARCHAR2 | 1 |  | Y |
| 64 | `RCPT_LINE_EXT_ID` | Rcpt_Line_Extessorial Id | VARCHAR2 | 40 |  | Y |
| 65 | `WHSE_CODE_SUG` | Whse_Codeessorial Sug | VARCHAR2 | 4 |  | Y |
| 66 | `LOC_CODE_SUG` | Loc_Codeessorial Sug | VARCHAR2 | 12 |  | Y |
| 67 | `RCPT_LINE_EDI_CREATE_FLAG` | Rcpt_Line_Edi_Createessorial Flag | VARCHAR2 | 1 |  | Y |
| 68 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 69 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 70 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 71 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 72 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 73 | `RCPT_LINE_MIN_MAX_DATE_OVER` | Rcpt_Line_Min_Max_Dateessorial Over | VARCHAR2 | 1 |  | Y |
| 74 | `ITEM_LOC_PROF_CODE` | Item_Loc_Professorial Code | VARCHAR2 | 4 |  | Y |
| 75 | `RCPT_LINE_SKIP_PROS_VALI_TP` | Rcpt_Line_Skip_Pros_Valiessorial Tp | VARCHAR2 | 1 |  | Y |
| 76 | `RCPT_LINE_NUM_LAY` | Rcpt_Line_Numessorial Lay | NUMBER | 22 | 3 | Y |
| 77 | `RCPT_LINE_QTY_LAY` | Rcpt_Line_Qtyessorial Lay | NUMBER | 22 | 3 | Y |
| 78 | `RCPT_LINE_QTY_ODD_LAY` | Rcpt_Line_Qty_Oddessorial Lay | NUMBER | 22 | 3 | Y |
| 79 | `RCPT_LINE_THL_VARI_PASS_FLAG` | Rcpt_Line_Thl_Vari_Passessorial Flag | VARCHAR2 | 1 |  | Y |

## `E_RCPT_D5D1`

- **Tipo:** Transactional
- **Categoria:** Receipts
- **Campos:** 34
- **Campos-chave prováveis:** COMP_CODE, RCPT_NUM, CUST_CODE, INVT_LEV1, LOC_CODE, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | N |
| 4 | `RCPT_LINE_NUM` | Receipt Line Number | NUMBER | 22 | 4 | N |
| 5 | `RCPT_LOC_LINE_NUM` | Rcpt_Loc_Lineessorial Num | NUMBER | 22 | 4 | N |
| 6 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 7 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 8 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | N |
| 9 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 10 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | Y |
| 11 | `RCPT_LOC_ENT_QTY` | Rcpt_Loc_Entessorial Qty | VARCHAR2 | 20 |  | N |
| 12 | `RCPT_LOC_QTY` | Rcpt_Locessorial Qty | NUMBER | 22 | 9 | N |
| 13 | `RCPT_LOC_CNVC_QTY` | Rcpt_Loc_Cnvcessorial Qty | NUMBER | 22 | 6 | Y |
| 14 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | N |
| 15 | `RCPT_LOC_PROS_FLAG` | Rcpt_Loc_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 16 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |
| 17 | `HOLD_SHIP_FLAG` | Hold_Shipessorial Flag | VARCHAR2 | 1 |  | Y |
| 18 | `HOLD_RENW_FLAG` | Hold_Renwessorial Flag | VARCHAR2 | 1 |  | Y |
| 19 | `WHSE_CODE_ORG` | Whse_Codeessorial Org | VARCHAR2 | 4 |  | Y |
| 20 | `LOC_CODE_ORG` | Loc_Codeessorial Org | VARCHAR2 | 12 |  | Y |
| 21 | `LOC_SIZE_CODE` | Loc_Sizeessorial Code | VARCHAR2 | 4 |  | Y |
| 22 | `WHSE_CODE_STATIC` | Whse_Codeessorial Static | VARCHAR2 | 4 |  | Y |
| 23 | `LOC_CODE_STATIC` | Loc_Codeessorial Static | VARCHAR2 | 12 |  | Y |
| 24 | `WHSE_CODE_MOVE` | Whse_Codeessorial Move | VARCHAR2 | 4 |  | Y |
| 25 | `LOC_CODE_MOVE` | Loc_Codeessorial Move | VARCHAR2 | 12 |  | Y |
| 26 | `RCPT_LOC_EXPT_QTY` | Rcpt_Loc_Exptessorial Qty | NUMBER | 22 | 9 | Y |
| 27 | `LOOSE_WHSE_CODE_STATIC` | Loose_Whse_Codeessorial Static | VARCHAR2 | 4 |  | Y |
| 28 | `LOOSE_LOC_CODE_STATIC` | Loose_Loc_Codeessorial Static | VARCHAR2 | 12 |  | Y |
| 29 | `WHSE_ACT_TP_NUM` | Whse_Act_Tpessorial Num | NUMBER | 22 | 2 | Y |
| 30 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 31 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 32 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 33 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 34 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `E_RCPT_D5D2`

- **Tipo:** Transactional
- **Categoria:** Receipts
- **Campos:** 22
- **Campos-chave prováveis:** COMP_CODE, RCPT_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | N |
| 4 | `RCPT_LINE_NUM` | Receipt Line Number | NUMBER | 22 | 4 | N |
| 5 | `PROS_CODE` | Prosessorial Code | VARCHAR2 | 4 |  | N |
| 6 | `PROS_LINE_NUM` | Pros_Lineessorial Num | NUMBER | 22 | 6 | N |
| 7 | `PROS_DES` | Prosessorial Des | VARCHAR2 | 30 |  | N |
| 8 | `PROS_TP_CODE` | Pros_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 9 | `PROS_LEN` | Prosessorial Len | VARCHAR2 | 6 |  | N |
| 10 | `COL_TP_CODE` | Col_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 11 | `SKU_CLASS_NUM` | Sku_Classessorial Num | NUMBER | 22 | 1 | N |
| 12 | `PROS_VALUE` | Prosessorial Value | VARCHAR2 | 250 |  | Y |
| 13 | `RCPT_LOC_LINE_NUM` | Rcpt_Loc_Lineessorial Num | NUMBER | 22 | 4 | Y |
| 14 | `RCPT_PROS_PRT_FLAG` | Rcpt_Pros_Prtessorial Flag | VARCHAR2 | 1 |  | Y |
| 15 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | Y |
| 16 | `PROS_REF` | Prosessorial Ref | VARCHAR2 | 250 |  | Y |
| 17 | `RCPT_PROS_VALID_FLAG` | Rcpt_Pros_Validessorial Flag | VARCHAR2 | 1 |  | Y |
| 18 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 19 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 20 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 21 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 22 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `E_RCPT_D5D3`

- **Tipo:** Transactional
- **Categoria:** Receipts
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE, RCPT_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | N |
| 4 | `RCPT_LINE_NUM` | Receipt Line Number | NUMBER | 22 | 4 | N |
| 5 | `DOC_CODE` | Document Code | VARCHAR2 | 4 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `E_RCPT_D5D4`

- **Tipo:** Transactional
- **Categoria:** Receipts
- **Campos:** 15
- **Campos-chave prováveis:** COMP_CODE, RCPT_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | N |
| 4 | `RCPT_LINE_NUM` | Receipt Line Number | NUMBER | 22 | 4 | N |
| 5 | `INVT_ATTR_PROF_CODE` | Invt_Attr_Professorial Code | VARCHAR2 | 4 |  | N |
| 6 | `INVT_ATTR_NAME` | Invt_Attressorial Name | VARCHAR2 | 20 |  | N |
| 7 | `INVT_ATTR_VAL` | Invt_Attressorial Val | VARCHAR2 | 40 |  | Y |
| 8 | `INVT_ATTR_VAL_ORG` | Invt_Attr_Valessorial Org | VARCHAR2 | 40 |  | Y |
| 9 | `INVT_ATTR_RCPT_EXCL_FLAG` | Invt_Attr_Rcpt_Exclessorial Flag | VARCHAR2 | 1 |  | Y |
| 10 | `INVT_ATTR_ALLOW_OVER_NAME` | Invt_Attr_Allow_Overessorial Name | VARCHAR2 | 1 |  | Y |
| 11 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 12 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 13 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 14 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 15 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `E_RCPT_D5D5`

- **Tipo:** Transactional
- **Categoria:** Receipts
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE, RCPT_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | N |
| 4 | `RCPT_LINE_NUM` | Receipt Line Number | NUMBER | 22 | 4 | N |
| 5 | `RCPT_REF_VAL` | Rcpt_Refessorial Val | VARCHAR2 | 40 |  | N |
| 6 | `RCPT_REF_QUAL_CODE` | Rcpt_Ref_Qualessorial Code | VARCHAR2 | 4 |  | Y |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `E_RCPT_D6`

- **Tipo:** Transactional
- **Categoria:** Receipts
- **Campos:** 23
- **Campos-chave prováveis:** COMP_CODE, RCPT_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | N |
| 4 | `INFO_FLOW_SEQ_NUM` | Info_Flow_Seqessorial Num | NUMBER | 22 | 2 | N |
| 5 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | N |
| 6 | `INFO_FLOW_MAND_FLAG` | Info_Flow_Mandessorial Flag | VARCHAR2 | 1 |  | N |
| 7 | `INFO_FLOW_DOC_SEQ_NUM` | Info_Flow_Doc_Seqessorial Num | NUMBER | 22 | 2 | N |
| 8 | `DOC_CODE` | Document Code | VARCHAR2 | 4 |  | Y |
| 9 | `FORM_CODE` | Form Code | VARCHAR2 | 4 |  | Y |
| 10 | `DOC_PRT_TP_FLAG` | Doc_Prt_Tpessorial Flag | VARCHAR2 | 1 |  | Y |
| 11 | `RCPT_DOC_PRT_STAT` | Rcpt_Doc_Prtessorial Stat | VARCHAR2 | 1 |  | Y |
| 12 | `RCPT_DOC_REPRT_CNT` | Rcpt_Doc_Reprtessorial Cnt | NUMBER | 22 | 4 | Y |
| 13 | `INFO_FLOW_ASS_LOC_FLAG` | Info_Flow_Ass_Locessorial Flag | VARCHAR2 | 1 |  | N |
| 14 | `INFO_FLOW_DEALLOC_FLAG` | Info_Flow_Deallocessorial Flag | VARCHAR2 | 1 |  | N |
| 15 | `LAB_STD_NUM_PROF_CODE` | Lab_Std_Num_Professorial Code | VARCHAR2 | 4 |  | Y |
| 16 | `LAB_STD_UOM` | Lab_Stdessorial Uom | VARCHAR2 | 4 |  | Y |
| 17 | `LAB_STD_MODY_PROF_CODE` | Lab_Std_Mody_Professorial Code | VARCHAR2 | 4 |  | Y |
| 18 | `INFO_FLOW_CREATE_DRMS_FLAG` | Info_Flow_Create_Drmsessorial Flag | VARCHAR2 | 1 |  | Y |
| 19 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 20 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 21 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 22 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 23 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `E_RCPT_D7`

- **Tipo:** Transactional
- **Categoria:** Receipts
- **Campos:** 45
- **Campos-chave prováveis:** COMP_CODE, RCPT_NUM, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | N |
| 4 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 5 | `CUST_INVT_PROF_CODE` | Cust_Invt_Professorial Code | VARCHAR2 | 4 |  | N |
| 6 | `RCPT_ITEM_LEV` | Rcpt_Itemessorial Lev | VARCHAR2 | 9 |  | N |
| 7 | `RCPT_ITEM_LEV_DES` | Rcpt_Item_Levessorial Des | VARCHAR2 | 13 |  | N |
| 8 | `RCPT_CHG_LEV_NUM` | Rcpt_Chg_Levessorial Num | NUMBER | 22 | 1 | N |
| 9 | `RCPT_INVT_TERMGY_CODE_LEV1` | Rcpt_Invt_Termgy_Codeessorial Lev1 | VARCHAR2 | 4 |  | N |
| 10 | `RCPT_LEV_NUM_LEV1` | Rcpt_Lev_Numessorial Lev1 | NUMBER | 22 | 1 | N |
| 11 | `RCPT_INVT_LEV1` | Rcpt_Invtessorial Lev1 | VARCHAR2 | 9 |  | N |
| 12 | `RCPT_ASS_FLAG_LEV1` | Rcpt_Ass_Flagessorial Lev1 | VARCHAR2 | 1 |  | N |
| 13 | `RCPT_SEQ_NUM_FLAG_LEV1` | Rcpt_Seq_Num_Flagessorial Lev1 | VARCHAR2 | 1 |  | N |
| 14 | `CUST_INVT_ASS_PROF_CODE_LEV1` | Cust_Invt_Ass_Prof_Codeessorial Lev1 | VARCHAR2 | 4 |  | Y |
| 15 | `RCPT_INVT_TERMGY_CODE_LEV2` | Rcpt_Invt_Termgy_Codeessorial Lev2 | VARCHAR2 | 4 |  | Y |
| 16 | `RCPT_LEV_NUM_LEV2` | Rcpt_Lev_Numessorial Lev2 | NUMBER | 22 | 1 | Y |
| 17 | `RCPT_INVT_LEV2` | Rcpt_Invtessorial Lev2 | VARCHAR2 | 9 |  | Y |
| 18 | `RCPT_ASS_FLAG_LEV2` | Rcpt_Ass_Flagessorial Lev2 | VARCHAR2 | 1 |  | Y |
| 19 | `RCPT_SEQ_NUM_FLAG_LEV2` | Rcpt_Seq_Num_Flagessorial Lev2 | VARCHAR2 | 1 |  | Y |
| 20 | `CUST_INVT_ASS_PROF_CODE_LEV2` | Cust_Invt_Ass_Prof_Codeessorial Lev2 | VARCHAR2 | 4 |  | Y |
| 21 | `RCPT_INVT_TERMGY_CODE_LEV3` | Rcpt_Invt_Termgy_Codeessorial Lev3 | VARCHAR2 | 4 |  | Y |
| 22 | `RCPT_LEV_NUM_LEV3` | Rcpt_Lev_Numessorial Lev3 | NUMBER | 22 | 1 | Y |
| 23 | `RCPT_INVT_LEV3` | Rcpt_Invtessorial Lev3 | VARCHAR2 | 9 |  | Y |
| 24 | `RCPT_ASS_FLAG_LEV3` | Rcpt_Ass_Flagessorial Lev3 | VARCHAR2 | 1 |  | Y |
| 25 | `RCPT_SEQ_NUM_FLAG_LEV3` | Rcpt_Seq_Num_Flagessorial Lev3 | VARCHAR2 | 1 |  | Y |
| 26 | `CUST_INVT_ASS_PROF_CODE_LEV3` | Cust_Invt_Ass_Prof_Codeessorial Lev3 | VARCHAR2 | 4 |  | Y |
| 27 | `RCPT_INVT_TERMGY_CODE_LEV4` | Rcpt_Invt_Termgy_Codeessorial Lev4 | VARCHAR2 | 4 |  | Y |
| 28 | `RCPT_LEV_NUM_LEV4` | Rcpt_Lev_Numessorial Lev4 | NUMBER | 22 | 1 | Y |
| 29 | `RCPT_INVT_LEV4` | Rcpt_Invtessorial Lev4 | VARCHAR2 | 9 |  | Y |
| 30 | `RCPT_ASS_FLAG_LEV4` | Rcpt_Ass_Flagessorial Lev4 | VARCHAR2 | 1 |  | Y |
| 31 | `RCPT_SEQ_NUM_FLAG_LEV4` | Rcpt_Seq_Num_Flagessorial Lev4 | VARCHAR2 | 1 |  | Y |
| 32 | `CUST_INVT_ASS_PROF_CODE_LEV4` | Cust_Invt_Ass_Prof_Codeessorial Lev4 | VARCHAR2 | 4 |  | Y |
| 33 | `RCPT_INVT_TERMGY_CODE_LEV5` | Rcpt_Invt_Termgy_Codeessorial Lev5 | VARCHAR2 | 4 |  | Y |
| 34 | `RCPT_LEV_NUM_LEV5` | Rcpt_Lev_Numessorial Lev5 | NUMBER | 22 | 1 | Y |
| 35 | `RCPT_INVT_LEV5` | Rcpt_Invtessorial Lev5 | VARCHAR2 | 9 |  | Y |
| 36 | `RCPT_ASS_FLAG_LEV5` | Rcpt_Ass_Flagessorial Lev5 | VARCHAR2 | 1 |  | Y |
| 37 | `RCPT_SEQ_NUM_FLAG_LEV5` | Rcpt_Seq_Num_Flagessorial Lev5 | VARCHAR2 | 1 |  | Y |
| 38 | `CUST_INVT_ASS_PROF_CODE_LEV5` | Cust_Invt_Ass_Prof_Codeessorial Lev5 | VARCHAR2 | 4 |  | Y |
| 39 | `CHG_CODE` | Charge Code | VARCHAR2 | 6 |  | Y |
| 40 | `RCPT_INVT_LEV_DES` | Rcpt_Invt_Levessorial Des | VARCHAR2 | 13 |  | Y |
| 41 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 42 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 43 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 44 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 45 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `E_RCPT_DRAFT`

- **Tipo:** Transactional
- **Categoria:** Receipts
- **Campos:** 24
- **Campos-chave prováveis:** RCPT_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `RCPT_DRAFT_STAT_ID` | Rcpt_Draft_Statessorial Id | RAW | 32 |  | Y |
| 3 | `COMP_ID` | Compessorial Id | RAW | 32 |  | Y |
| 4 | `CUST_ID` | Customer ID | RAW | 32 |  | Y |
| 5 | `RCPT_DRAFT_RCPT_TP_ID` | Rcpt_Draft_Rcpt_Tpessorial Id | RAW | 32 |  | Y |
| 6 | `RCPT_DRAFT_PRTY_NUM_ID` | Rcpt_Draft_Prty_Numessorial Id | RAW | 32 |  | Y |
| 7 | `RCPT_DRAFT_REF_NUM` | Rcpt_Draft_Refessorial Num | VARCHAR2 | 20 |  | Y |
| 8 | `RCPT_DRAFT_PRO_BILL_NUM` | Rcpt_Draft_Pro_Billessorial Num | VARCHAR2 | 20 |  | Y |
| 9 | `RCPT_DRAFT_RCPT_ALT_REF1` | Rcpt_Draft_Rcpt_Altessorial Ref1 | VARCHAR2 | 20 |  | Y |
| 10 | `RCPT_DRAFT_RCPT_ALT_REF2` | Rcpt_Draft_Rcpt_Altessorial Ref2 | VARCHAR2 | 20 |  | Y |
| 11 | `RCPT_DRAFT_RCPT_DATE_GMT` | Rcpt_Draft_Rcpt_Dateessorial Gmt | DATE | 7 |  | Y |
| 12 | `RCPT_DRAFT_RCPT_EXPT_DATE_GMT` | Rcpt_Draft_Rcpt_Expt_Dateessorial Gmt | DATE | 7 |  | Y |
| 13 | `WHSE_CODE_ID` | Whse_Codeessorial Id | RAW | 32 |  | Y |
| 14 | `RCPT_DRAFT_PROS_FLAG` | Rcpt_Draft_Prosessorial Flag | VARCHAR2 | 1 |  | Y |
| 15 | `RCPT_ID` | Rcptessorial Id | RAW | 32 |  | Y |
| 16 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 17 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 18 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 19 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 20 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 21 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | Y |
| 22 | `RCPT_DRAFT_CARR_FLAG` | Rcpt_Draft_Carressorial Flag | VARCHAR2 | 1 |  | Y |
| 23 | `RCPT_DRAFT_PALL_FLAG` | Rcpt_Draft_Pallessorial Flag | VARCHAR2 | 1 |  | Y |
| 24 | `LOCK_OP_CODE` | Lock_Opessorial Code | VARCHAR2 | 100 |  | Y |

## `E_RCPT_DRAFT_ADDR`

- **Tipo:** Transactional
- **Categoria:** Receipts
- **Campos:** 18

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `RCPT_DRAFT_ID` | Rcpt_Draftessorial Id | RAW | 32 |  | Y |
| 3 | `RCPT_DRAFT_ADDR_TP_ID` | Rcpt_Draft_Addr_Tpessorial Id | RAW | 32 |  | Y |
| 4 | `RCPT_DRAFT_ADDR_CODE_ID` | Rcpt_Draft_Addr_Codeessorial Id | RAW | 32 |  | Y |
| 5 | `RCPT_DRAFT_ADDR_NAME` | Rcpt_Draft_Addressorial Name | VARCHAR2 | 30 |  | Y |
| 6 | `RCPT_DRAFT_ADDR_ADD1` | Rcpt_Draft_Addressorial Add1 | VARCHAR2 | 30 |  | Y |
| 7 | `RCPT_DRAFT_ADDR_ADD2` | Rcpt_Draft_Addressorial Add2 | VARCHAR2 | 30 |  | Y |
| 8 | `RCPT_DRAFT_ADDR_ADD3` | Rcpt_Draft_Addressorial Add3 | VARCHAR2 | 30 |  | Y |
| 9 | `RCPT_DRAFT_ADDR_ADD4` | Rcpt_Draft_Addressorial Add4 | VARCHAR2 | 30 |  | Y |
| 10 | `RCPT_DRAFT_ADDR_CITY` | Rcpt_Draft_Addressorial City | VARCHAR2 | 30 |  | Y |
| 11 | `RCPT_DRAFT_ADDR_ZIP` | Rcpt_Draft_Addressorial Zip | VARCHAR2 | 10 |  | Y |
| 12 | `RCPT_DRAFT_ADDR_STATE` | Rcpt_Draft_Addressorial State | VARCHAR2 | 4 |  | Y |
| 13 | `RCPT_DRAFT_ADDR_COUNTRY` | Rcpt_Draft_Addressorial Country | VARCHAR2 | 4 |  | Y |
| 14 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 15 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 16 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 17 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 18 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `E_RCPT_DRAFT_CARR_DET`

- **Tipo:** Transactional
- **Categoria:** Receipts
- **Campos:** 24

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `RCPT_DRAFT_ID` | Rcpt_Draftessorial Id | RAW | 32 |  | Y |
| 3 | `DRV_ID` | Drvessorial Id | RAW | 32 |  | Y |
| 4 | `DRV_NAME` | Drvessorial Name | VARCHAR2 | 30 |  | Y |
| 5 | `RCPT_DRAFT_POW_UNIT_NUM` | Rcpt_Draft_Pow_Unitessorial Num | VARCHAR2 | 20 |  | Y |
| 6 | `RCPT_DRAFT_CARRY_UNIT_NUM` | Rcpt_Draft_Carry_Unitessorial Num | VARCHAR2 | 20 |  | Y |
| 7 | `RCPT_DRAFT_VES` | Rcpt_Draftessorial Ves | VARCHAR2 | 20 |  | Y |
| 8 | `RCPT_DRAFT_VOY` | Rcpt_Draftessorial Voy | VARCHAR2 | 20 |  | Y |
| 9 | `RCPT_DRAFT_SEAL1` | Rcpt_Draftessorial Seal1 | VARCHAR2 | 20 |  | Y |
| 10 | `RCPT_DRAFT_SEAL2` | Rcpt_Draftessorial Seal2 | VARCHAR2 | 20 |  | Y |
| 11 | `RCPT_DRAFT_TEMP_FRONT` | Rcpt_Draft_Tempessorial Front | VARCHAR2 | 10 |  | Y |
| 12 | `RCPT_DRAFT_TEMP_MID` | Rcpt_Draft_Tempessorial Mid | VARCHAR2 | 10 |  | Y |
| 13 | `RCPT_DRAFT_TEMP_BACK` | Rcpt_Draft_Tempessorial Back | VARCHAR2 | 10 |  | Y |
| 14 | `RCPT_DRAFT_TEMP_SET` | Rcpt_Draft_Tempessorial Set | VARCHAR2 | 10 |  | Y |
| 15 | `RCPT_DRAFT_TEMP_AMB` | Rcpt_Draft_Tempessorial Amb | VARCHAR2 | 10 |  | Y |
| 16 | `RCPT_DRAFT_TEMP6` | Rcpt_Draftessorial Temp6 | VARCHAR2 | 10 |  | Y |
| 17 | `RCPT_DRAFT_SEAL1_INTACT` | Rcpt_Draft_Seal1essorial Intact | VARCHAR2 | 1 |  | Y |
| 18 | `RCPT_DRAFT_PALL_QTY_IN` | Rcpt_Draft_Pall_Qtyessorial In | NUMBER | 22 | 4 | Y |
| 19 | `RCPT_DRAFT_PALL_QTY_OUT` | Rcpt_Draft_Pall_Qtyessorial Out | NUMBER | 22 | 4 | Y |
| 20 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 21 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 22 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 23 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 24 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `E_RCPT_DRAFT_EDI`

- **Tipo:** Transactional
- **Categoria:** Receipts
- **Campos:** 10

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `RCPT_DRAFT_ID` | Rcpt_Draftessorial Id | RAW | 32 |  | Y |
| 3 | `RCPT_DRAFT_LINE_ID` | Rcpt_Draft_Lineessorial Id | RAW | 32 |  | Y |
| 4 | `EDI_DATA_ID_ID` | Edi_Data_Idessorial Id | RAW | 32 |  | Y |
| 5 | `EDI_DATA_ID_VALUE` | Edi_Data_Idessorial Value | VARCHAR2 | 250 |  | Y |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `E_RCPT_DRAFT_LINE`

- **Tipo:** Transactional
- **Categoria:** Receipts
- **Campos:** 23
- **Campos-chave prováveis:** INVT_LEV2, INVT_LEV3, INVT_LEV4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `RCPT_DRAFT_ID` | Rcpt_Draftessorial Id | RAW | 32 |  | Y |
| 3 | `RCPT_DRAFT_LINE_TP_ID` | Rcpt_Draft_Line_Tpessorial Id | RAW | 32 |  | Y |
| 4 | `CUST_ID` | Customer ID | RAW | 32 |  | Y |
| 5 | `ITEM_ID` | Itemessorial Id | RAW | 32 |  | Y |
| 6 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | Y |
| 7 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | Y |
| 8 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | Y |
| 9 | `WHSE_ID` | Warehouse Id | RAW | 32 |  | Y |
| 10 | `RCPT_DRAFT_LINE_EXPT_QTY` | Rcpt_Draft_Line_Exptessorial Qty | NUMBER | 22 | 9 | Y |
| 11 | `RCPT_DRAFT_LINE_EXPT_ENT_QTY` | Rcpt_Draft_Line_Expt_Entessorial Qty | VARCHAR2 | 20 |  | Y |
| 12 | `RCPT_DRAFT_LINE_RECD_QTY` | Rcpt_Draft_Line_Recdessorial Qty | NUMBER | 22 | 9 | Y |
| 13 | `RCPT_DRAFT_LINE_RECD_ENT_QTY` | Rcpt_Draft_Line_Recd_Entessorial Qty | VARCHAR2 | 20 |  | Y |
| 14 | `RCPT_DRAFT_LINE_UNIT_WGT` | Rcpt_Draft_Line_Unitessorial Wgt | NUMBER | 22 | 16 | Y |
| 15 | `SKU_ID` | Skuessorial Id | RAW | 32 |  | Y |
| 16 | `RCPT_DRAFT_LINE_WGT` | Rcpt_Draft_Lineessorial Wgt | NUMBER | 22 | 16 | Y |
| 17 | `RCPT_DRAFT_LINE_WGT_NET` | Rcpt_Draft_Line_Wgtessorial Net | NUMBER | 22 | 16 | Y |
| 18 | `WGT_MEAS_ID` | Wgt_Measessorial Id | RAW | 32 |  | Y |
| 19 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 20 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 21 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 22 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 23 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `E_RCPT_DRAFT_LINE_PROS`

- **Tipo:** Transactional
- **Categoria:** Receipts
- **Campos:** 11

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `RCPT_DRAFT_ID` | Rcpt_Draftessorial Id | RAW | 32 |  | Y |
| 3 | `RCPT_DRAFT_LINE_ID` | Rcpt_Draft_Lineessorial Id | RAW | 32 |  | Y |
| 4 | `RCPT_DRAFT_LOC_LINE_ID` | Rcpt_Draft_Loc_Lineessorial Id | RAW | 32 |  | Y |
| 5 | `PROS_ID` | Prosessorial Id | RAW | 32 |  | Y |
| 6 | `PROS_VALUE` | Prosessorial Value | VARCHAR2 | 250 |  | Y |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `E_RCPT_DRAFT_MISC`

- **Tipo:** Transactional
- **Categoria:** Receipts
- **Campos:** 11

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `RCPT_DRAFT_ID` | Rcpt_Draftessorial Id | RAW | 32 |  | Y |
| 3 | `LOAD_TP_ID` | Load_Tpessorial Id | RAW | 32 |  | Y |
| 4 | `MES_ID` | Mesessorial Id | RAW | 32 |  | Y |
| 5 | `RCPT_DRAFT_GRP_VAL` | Rcpt_Draft_Grpessorial Val | VARCHAR2 | 30 |  | Y |
| 6 | `DIST_TP_ID` | Dist_Tpessorial Id | RAW | 32 |  | Y |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `E_RCPT_DRAFT_PALL_DET`

- **Tipo:** Transactional
- **Categoria:** Receipts
- **Campos:** 13

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `RCPT_DRAFT_ID` | Rcpt_Draftessorial Id | RAW | 32 |  | Y |
| 3 | `PALL_ACC_ID` | Pall_Accessorial Id | RAW | 32 |  | Y |
| 4 | `PALL_ACC_TP` | Pall_Accessorial Tp | VARCHAR2 | 4 |  | Y |
| 5 | `PALL_TRANS_TP_ID` | Pall_Trans_Tpessorial Id | RAW | 32 |  | Y |
| 6 | `PALL_ID` | Pallessorial Id | RAW | 32 |  | Y |
| 7 | `PALL_QTY` | Pallessorial Qty | NUMBER | 22 | 4 | Y |
| 8 | `PALL_REF_DES` | Pall_Refessorial Des | VARCHAR2 | 60 |  | Y |
| 9 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 10 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 12 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 13 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `E_RCPT_DRAFT_PROS`

- **Tipo:** Transactional
- **Categoria:** Receipts
- **Campos:** 8

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `RCPT_ID` | Rcptessorial Id | RAW | 32 |  | Y |
| 3 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | Y |
| 4 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 5 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 6 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 7 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `E_RCPT_DRAFT_REM`

- **Tipo:** Transactional
- **Categoria:** Receipts
- **Campos:** 15

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `RCPT_DRAFT_ID` | Rcpt_Draftessorial Id | RAW | 32 |  | Y |
| 3 | `RCPT_DRAFT_LINE_ID` | Rcpt_Draft_Lineessorial Id | RAW | 32 |  | Y |
| 4 | `RCPT_DRAFT_REM_CUST_FLAG` | Rcpt_Draft_Rem_Custessorial Flag | VARCHAR2 | 1 |  | Y |
| 5 | `RCPT_DRAFT_REM_CON_FLAG` | Rcpt_Draft_Rem_Conessorial Flag | VARCHAR2 | 1 |  | Y |
| 6 | `RCPT_DRAFT_REM_CARR_FLAG` | Rcpt_Draft_Rem_Carressorial Flag | VARCHAR2 | 1 |  | Y |
| 7 | `RCPT_DRAFT_REM_RF_FLAG` | Rcpt_Draft_Rem_Rfessorial Flag | VARCHAR2 | 1 |  | Y |
| 8 | `DOC_ID_REST` | Doc_Idessorial Rest | RAW | 32 |  | Y |
| 9 | `MES_ID` | Mesessorial Id | RAW | 32 |  | Y |
| 10 | `RCPT_DRAFT_REM_TEXT` | Rcpt_Draft_Remessorial Text | VARCHAR2 | 2000 |  | Y |
| 11 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 12 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 13 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 14 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 15 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `E_RCPT_H`

- **Tipo:** Transactional
- **Categoria:** Receipts
- **Campos:** 68
- **Campos-chave prováveis:** COMP_CODE, RCPT_NUM, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | N |
| 4 | `RCPT_PREX` | Rcptessorial Prex | VARCHAR2 | 4 |  | N |
| 5 | `RCPT_SUFX` | Rcptessorial Sufx | VARCHAR2 | 4 |  | Y |
| 6 | `RCPT_STAT` | Rcptessorial Stat | VARCHAR2 | 1 |  | N |
| 7 | `RCPT_TP` | Rcptessorial Tp | VARCHAR2 | 1 |  | N |
| 8 | `RCPT_PRTY_NUM` | Rcpt_Prtyessorial Num | NUMBER | 22 | 1 | N |
| 9 | `RCPT_INV_DATE` | Rcpt_Invessorial Date | DATE | 7 |  | Y |
| 10 | `RCPT_INV_REG_NUM` | Rcpt_Inv_Regessorial Num | NUMBER | 22 | 9 | Y |
| 11 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 12 | `SHIP_CODE` | Shipper Code | VARCHAR2 | 10 |  | N |
| 13 | `CUST_CODE_BILL_TO` | Cust_Code_Billessorial To | VARCHAR2 | 10 |  | N |
| 14 | `RCPT_DATE` | Rcptessorial Date | DATE | 7 |  | N |
| 15 | `RCPT_PRO_BILL_NUM` | Rcpt_Pro_Billessorial Num | VARCHAR2 | 20 |  | Y |
| 16 | `RCPT_REF_NUM` | Rcpt_Refessorial Num | VARCHAR2 | 20 |  | Y |
| 17 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | N |
| 18 | `LOAD_TP_CODE` | Load Type Code | VARCHAR2 | 4 |  | N |
| 19 | `RCPT_TOT_UNIT` | Rcpt_Totessorial Unit | NUMBER | 22 | 9 | N |
| 20 | `RCPT_REM_FLAG` | Rcpt_Remessorial Flag | VARCHAR2 | 1 |  | N |
| 21 | `RCPT_CARR_FLAG` | Rcpt_Carressorial Flag | VARCHAR2 | 1 |  | N |
| 22 | `RCPT_PALL_FLAG` | Rcpt_Pallessorial Flag | VARCHAR2 | 1 |  | N |
| 23 | `RCPT_BILL_FLAG` | Rcpt_Billessorial Flag | VARCHAR2 | 1 |  | N |
| 24 | `RCPT_EXTRA_CHG_FLAG` | Rcpt_Extra_Chgessorial Flag | VARCHAR2 | 1 |  | N |
| 25 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 26 | `RCPT_ENTRY_DATE` | Rcpt_Entryessorial Date | DATE | 7 |  | N |
| 27 | `RCPT_ALTER_FLAG` | Rcpt_Alteressorial Flag | VARCHAR2 | 1 |  | N |
| 28 | `RCPT_CONF_FLAG` | Rcpt_Confessorial Flag | VARCHAR2 | 1 |  | N |
| 29 | `RCPT_RATE_FLAG` | Rcpt_Rateessorial Flag | VARCHAR2 | 1 |  | N |
| 30 | `RCPT_LOC_GEN_FLAG` | Rcpt_Loc_Genessorial Flag | VARCHAR2 | 1 |  | N |
| 31 | `RCPT_LOC_STAT` | Rcpt_Locessorial Stat | VARCHAR2 | 1 |  | N |
| 32 | `RCPT_DAY_ACT_REP_PROS_FLAG` | Rcpt_Day_Act_Rep_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 33 | `INFO_FLOW_PROF_CODE` | Information Flow Profile Code | VARCHAR2 | 4 |  | N |
| 34 | `INFO_FLOW_SEQ_NUM` | Info_Flow_Seqessorial Num | NUMBER | 22 | 2 | N |
| 35 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | N |
| 36 | `RCPT_TRANS_ORD_NUM` | Rcpt_Trans_Ordessorial Num | NUMBER | 22 | 9 | Y |
| 37 | `RCPT_TRANS_ORD_PREX` | Rcpt_Trans_Ordessorial Prex | VARCHAR2 | 4 |  | Y |
| 38 | `RCPT_TRANS_ORD_SUFX` | Rcpt_Trans_Ordessorial Sufx | VARCHAR2 | 4 |  | Y |
| 39 | `RCPT_EDI_CREATE_FLAG` | Rcpt_Edi_Createessorial Flag | VARCHAR2 | 1 |  | N |
| 40 | `RCPT_CONF_DATE` | Rcpt_Confessorial Date | DATE | 7 |  | Y |
| 41 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 42 | `EDI_INFO_FLAG` | Edi_Infoessorial Flag | VARCHAR2 | 1 |  | N |
| 43 | `RCPT_APPO_DATE` | Rcpt_Appoessorial Date | DATE | 7 |  | Y |
| 44 | `DAY_ACT_REG_NUM` | Day_Act_Regessorial Num | NUMBER | 22 | 6 | Y |
| 45 | `RCPT_EDI_GRP_VAL` | Rcpt_Edi_Grpessorial Val | VARCHAR2 | 30 |  | Y |
| 46 | `RCPT_ALT_REF1` | Rcpt_Altessorial Ref1 | VARCHAR2 | 20 |  | Y |
| 47 | `RCPT_ALT_REF2` | Rcpt_Altessorial Ref2 | VARCHAR2 | 20 |  | Y |
| 48 | `RCPT_OS_NUM` | Rcpt_Osessorial Num | NUMBER | 22 | 6 | Y |
| 49 | `RCPT_OS_FLAG` | Rcpt_Osessorial Flag | VARCHAR2 | 1 |  | Y |
| 50 | `RCPT_SRCE_RCPT_NUM` | Rcpt_Srce_Rcptessorial Num | NUMBER | 22 | 9 | Y |
| 51 | `BAT_NUM` | Batch Number | NUMBER | 22 | 9 | Y |
| 52 | `MHE_TP_CODE` | Mhe_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 53 | `DIST_TP_CODE` | Dist_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 54 | `PO_NUM` | PO Number | NUMBER | 22 | 9 | Y |
| 55 | `FINAL_DEST_CODE` | Final_Destessorial Code | VARCHAR2 | 10 |  | Y |
| 56 | `COMP_CODE_UPDOWNSTREAM` | Comp_Codeessorial Updownstream | VARCHAR2 | 2 |  | Y |
| 57 | `RCPT_NUM_UPDOWNSTREAM` | Rcpt_Numessorial Updownstream | NUMBER | 22 | 9 | Y |
| 58 | `RCPT_EXPT_DATE` | Rcpt_Exptessorial Date | DATE | 7 |  | Y |
| 59 | `LOAD_NUM` | Load Number | NUMBER | 22 | 6 | Y |
| 60 | `RCPT_A1INSPECTION_STAT_MES` | Rcpt_A1Inspection_Statessorial Mes | VARCHAR2 | 100 |  | Y |
| 61 | `BLDG_CODE_UNLOAD` | Bldg_Codeessorial Unload | VARCHAR2 | 4 |  | Y |
| 62 | `DOOR_CODE_UNLOAD` | Door_Codeessorial Unload | VARCHAR2 | 4 |  | Y |
| 63 | `RCPT_PUTAWAY_MODE` | Rcpt_Putawayessorial Mode | VARCHAR2 | 4 |  | Y |
| 64 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 65 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 66 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 67 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 68 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `E_RCPT_PACK_D`

- **Tipo:** Transactional
- **Categoria:** Receipts
- **Campos:** 22
- **Campos-chave prováveis:** COMP_CODE, RCPT_NUM, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | N |
| 4 | `RCPT_LINE_NUM` | Receipt Line Number | NUMBER | 22 | 4 | N |
| 5 | `RCPT_LOC_LINE_NUM` | Rcpt_Loc_Lineessorial Num | NUMBER | 22 | 4 | N |
| 6 | `RCPT_PACK_NUM` | Rcpt_Packessorial Num | NUMBER | 22 | 9 | N |
| 7 | `RCPT_PACK_REF_NUM1` | Rcpt_Pack_Refessorial Num1 | VARCHAR2 | 20 |  | Y |
| 8 | `RCPT_PACK_REF_NUM2` | Rcpt_Pack_Refessorial Num2 | VARCHAR2 | 20 |  | Y |
| 9 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | Y |
| 10 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | Y |
| 11 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | Y |
| 12 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | Y |
| 13 | `INVT_LEV5` | Inventory Level 5 | VARCHAR2 | 40 |  | Y |
| 14 | `RCPT_PACK_UNIT` | Rcpt_Packessorial Unit | NUMBER | 22 | 9 | Y |
| 15 | `RCPT_PACK_ENT_UNIT` | Rcpt_Pack_Entessorial Unit | VARCHAR2 | 20 |  | Y |
| 16 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | Y |
| 17 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |
| 18 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 19 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 20 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 21 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 22 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `E_RCPT_PACK_H`

- **Tipo:** Transactional
- **Categoria:** Receipts
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE, RCPT_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | N |
| 4 | `RCPT_PACK_NUM` | Rcpt_Packessorial Num | NUMBER | 22 | 6 | N |
| 5 | `RCPT_PACK_REF_NUM1` | Rcpt_Pack_Refessorial Num1 | VARCHAR2 | 20 |  | Y |
| 6 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | Y |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `E_RCPT_VIRT_D`

- **Tipo:** Transactional
- **Categoria:** Receipts
- **Campos:** 6
- **Campos-chave prováveis:** COMP_CODE, RCPT_NUM, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | N |
| 3 | `RCPT_VIRT_LINE_NUM` | Rcpt_Virt_Lineessorial Num | NUMBER | 22 | 4 | N |
| 4 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 5 | `RCPT_VIRT_CUST_QTY` | Rcpt_Virt_Custessorial Qty | NUMBER | 22 | 9 | N |
| 6 | `RCPT_VIRT_CUST_ENT_QTY` | Rcpt_Virt_Cust_Entessorial Qty | VARCHAR2 | 20 |  | N |

## `E_RCPT_VIRT_H`

- **Tipo:** Transactional
- **Categoria:** Receipts
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE, RCPT_NUM, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4, LOC_CODE, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | N |
| 3 | `RCPT_VIRT_LINE_NUM` | Rcpt_Virt_Lineessorial Num | NUMBER | 22 | 4 | N |
| 4 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | Y |
| 5 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | Y |
| 6 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | Y |
| 7 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | Y |
| 8 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 9 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | N |
| 10 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |
| 11 | `RCPT_VIRT_QTY` | Rcpt_Virtessorial Qty | NUMBER | 22 | 9 | N |
| 12 | `RCPT_VIRT_ENT_QTY` | Rcpt_Virt_Entessorial Qty | VARCHAR2 | 20 |  | N |

## `E_SAND_RCPT_D`

- **Tipo:** Transactional
- **Categoria:** Receipts
- **Campos:** 13
- **Campos-chave prováveis:** INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4, LOC_CODE, HOLD_CODE, SKU_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SAND_RCPT_SEQ_NUM` | Sand_Rcpt_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `SAND_RCPT_LINE_NUM` | Sand_Rcpt_Lineessorial Num | NUMBER | 22 | 4 | N |
| 3 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | Y |
| 4 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | Y |
| 5 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | Y |
| 6 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | Y |
| 7 | `SAND_RCPT_QTY` | Sand_Rcptessorial Qty | NUMBER | 22 | 9 | Y |
| 8 | `SAND_RCPT_UNIT` | Sand_Rcptessorial Unit | NUMBER | 22 | 9 | Y |
| 9 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 10 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | Y |
| 11 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |
| 12 | `SKU_CODE` | SKU Code | VARCHAR2 | 4 |  | Y |
| 13 | `SAND_REM_TEXT` | Sand_Remessorial Text | VARCHAR2 | 2000 |  | Y |

## `E_SAND_RCPT_H`

- **Tipo:** Transactional
- **Categoria:** Receipts
- **Campos:** 29
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SAND_RCPT_SEQ_NUM` | Sand_Rcpt_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `SHIP_CODE` | Shipper Code | VARCHAR2 | 10 |  | Y |
| 5 | `SHIP_NAME` | Shipessorial Name | VARCHAR2 | 30 |  | Y |
| 6 | `SHIP_ADD1_MAN` | Ship_Add1essorial Man | VARCHAR2 | 30 |  | Y |
| 7 | `SHIP_ADD2_MAN` | Ship_Add2essorial Man | VARCHAR2 | 30 |  | Y |
| 8 | `SHIP_ADD3_MAN` | Ship_Add3essorial Man | VARCHAR2 | 30 |  | Y |
| 9 | `SHIP_ZIP_CODE_MAN` | Ship_Zip_Codeessorial Man | VARCHAR2 | 10 |  | Y |
| 10 | `SHIP_ZIP_CITY_MAN` | Ship_Zip_Cityessorial Man | VARCHAR2 | 30 |  | Y |
| 11 | `SHIP_STATE_CODE_MAN` | Ship_State_Codeessorial Man | VARCHAR2 | 4 |  | Y |
| 12 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | Y |
| 13 | `CARR_NAME` | Carrier Name | VARCHAR2 | 30 |  | Y |
| 14 | `SAND_RCPT_REF_NUM` | Sand_Rcpt_Refessorial Num | VARCHAR2 | 20 |  | N |
| 15 | `SAND_RCPT_DATE` | Sand_Rcptessorial Date | DATE | 7 |  | N |
| 16 | `SAND_RCPT_LINE_CNT` | Sand_Rcpt_Lineessorial Cnt | NUMBER | 22 | 3 | N |
| 17 | `WHSE_CODE_DEF` | Whse_Codeessorial Def | VARCHAR2 | 4 |  | Y |
| 18 | `LOC_CODE_DEF` | Loc_Codeessorial Def | VARCHAR2 | 12 |  | Y |
| 19 | `SKU_CODE_DEF` | Sku_Codeessorial Def | VARCHAR2 | 4 |  | Y |
| 20 | `INVT_LEV1_DEF` | Invt_Lev1essorial Def | VARCHAR2 | 40 |  | Y |
| 21 | `INVT_LEV2_DEF` | Invt_Lev2essorial Def | VARCHAR2 | 40 |  | Y |
| 22 | `INVT_LEV3_DEF` | Invt_Lev3essorial Def | VARCHAR2 | 40 |  | Y |
| 23 | `INVT_LEV4_DEF` | Invt_Lev4essorial Def | VARCHAR2 | 40 |  | Y |
| 24 | `SAND_RCPT_TOT_UNIT` | Sand_Rcpt_Totessorial Unit | NUMBER | 22 | 9 | Y |
| 25 | `SAND_REM_TEXT` | Sand_Remessorial Text | VARCHAR2 | 2000 |  | Y |
| 26 | `SAND_RCPT_PRTY_NUM` | Sand_Rcpt_Prtyessorial Num | NUMBER | 22 | 1 | Y |
| 27 | `SAND_RCPT_PRO_BILL_NUM` | Sand_Rcpt_Pro_Billessorial Num | VARCHAR2 | 20 |  | Y |
| 28 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 29 | `SAND_RCPT_ALT_REF2` | Sand_Rcpt_Altessorial Ref2 | VARCHAR2 | 20 |  | Y |

## `E_SHIP_D`

- **Tipo:** Transactional
- **Categoria:** Receipts
- **Campos:** 15
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `SHIP_NUM` | Shipessorial Num | NUMBER | 22 | 9 | N |
| 3 | `CON_CODE` | Consignee Code | VARCHAR2 | 10 |  | N |
| 4 | `SHIP_SORT_CART_ID` | Ship_Sort_Cartessorial Id | VARCHAR2 | 20 |  | N |
| 5 | `SHIP_SORT_CART_DATE` | Ship_Sort_Cartessorial Date | DATE | 7 |  | N |
| 6 | `SHIP_SORT_CART_WGT` | Ship_Sort_Cartessorial Wgt | NUMBER | 22 | 16 | N |
| 7 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | N |
| 8 | `SHIP_SORT_CART_CUBE` | Ship_Sort_Cartessorial Cube | NUMBER | 22 | 16 | N |
| 9 | `LINEAR_MEAS_CODE` | Linear Measurement Code | VARCHAR2 | 4 |  | N |
| 10 | `SHIP_SORT_CART_HGT` | Ship_Sort_Cartessorial Hgt | NUMBER | 22 | 7 | Y |
| 11 | `SHIP_SORT_CART_WID` | Ship_Sort_Cartessorial Wid | NUMBER | 22 | 7 | Y |
| 12 | `SHIP_SORT_CART_LEN` | Ship_Sort_Cartessorial Len | NUMBER | 22 | 7 | Y |
| 13 | `SHIP_CON_PRT_DATE` | Ship_Con_Prtessorial Date | DATE | 7 |  | Y |
| 14 | `SHIP_CON_PRT_CNT` | Ship_Con_Prtessorial Cnt | NUMBER | 22 | 4 | Y |
| 15 | `SHIP_NUM_CON` | Ship_Numessorial Con | NUMBER | 22 | 6 | Y |

## `E_SHIP_H`

- **Tipo:** Transactional
- **Categoria:** Receipts
- **Campos:** 19
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `SHIP_NUM` | Shipessorial Num | NUMBER | 22 | 9 | N |
| 3 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | N |
| 4 | `SHIP_ROUTE_ID` | Ship_Routeessorial Id | VARCHAR2 | 10 |  | N |
| 5 | `SHIP_LANE_ID` | Ship_Laneessorial Id | VARCHAR2 | 10 |  | N |
| 6 | `SHIP_TRUCK_NUM` | Ship_Truckessorial Num | VARCHAR2 | 20 |  | Y |
| 7 | `SHIP_EQP_NUM` | Ship_Eqpessorial Num | VARCHAR2 | 20 |  | Y |
| 8 | `SHIP_DRV_NUM` | Ship_Drvessorial Num | VARCHAR2 | 10 |  | Y |
| 9 | `SHIP_DRV_NAME` | Ship_Drvessorial Name | VARCHAR2 | 30 |  | Y |
| 10 | `SHIP_START_DATE` | Ship_Startessorial Date | DATE | 7 |  | N |
| 11 | `SHIP_END_DATE` | Ship_Endessorial Date | DATE | 7 |  | Y |
| 12 | `SHIP_TOT_CART` | Ship_Totessorial Cart | NUMBER | 22 | 9 | Y |
| 13 | `SHIP_PRT_DATE` | Ship_Prtessorial Date | DATE | 7 |  | Y |
| 14 | `SHIP_PRT_CNT` | Ship_Prtessorial Cnt | NUMBER | 22 | 4 | Y |
| 15 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 16 | `SHIP_EDI_PRT_DATE` | Ship_Edi_Prtessorial Date | DATE | 7 |  | Y |
| 17 | `SHIP_EDI_PRT_CNT` | Ship_Edi_Prtessorial Cnt | NUMBER | 22 | 4 | Y |
| 18 | `SHIP_NUM_BOL_NUM` | Ship_Num_Bolessorial Num | NUMBER | 22 | 6 | Y |
| 19 | `CON_CODE` | Consignee Code | VARCHAR2 | 10 |  | Y |

## `E_SHIP_VICS_D1`

- **Tipo:** Transactional
- **Categoria:** Receipts
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `SHIP_VICS_SEQ_NUM` | Ship_Vics_Seqessorial Num | NUMBER | 22 | 9 | N |
| 3 | `SHIP_VICS_REM_LINE_NUM` | Ship_Vics_Rem_Lineessorial Num | NUMBER | 22 | 3 | N |
| 4 | `SHIP_VICS_REM_LINE_TEXT` | Ship_Vics_Rem_Lineessorial Text | VARCHAR2 | 45 |  | Y |

## `E_SHIP_VICS_D2`

- **Tipo:** Transactional
- **Categoria:** Receipts
- **Campos:** 6
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `SHIP_VICS_SEQ_NUM` | Ship_Vics_Seqessorial Num | NUMBER | 22 | 9 | N |
| 3 | `SHIP_VICS_COMD_LINE_NUM` | Ship_Vics_Comd_Lineessorial Num | NUMBER | 22 | 2 | N |
| 4 | `SHIP_VICS_COMD_DES` | Ship_Vics_Comdessorial Des | VARCHAR2 | 45 |  | Y |
| 5 | `SHIP_VICS_NMFC` | Ship_Vicsessorial Nmfc | VARCHAR2 | 20 |  | Y |
| 6 | `SHIP_VICS_CLASS` | Ship_Vicsessorial Class | VARCHAR2 | 20 |  | Y |

## `E_SHIP_VICS_D3`

- **Tipo:** Transactional
- **Categoria:** Receipts
- **Campos:** 5
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `SHIP_VICS_SEQ_NUM` | Ship_Vics_Seqessorial Num | NUMBER | 22 | 9 | N |
| 3 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 4 | `ORD_REF_TP` | Ord_Refessorial Tp | VARCHAR2 | 1 |  | Y |
| 5 | `ORD_REF_NUM` | Ord_Refessorial Num | NUMBER | 22 | 9 | Y |

## `E_SHIP_VICS_H`

- **Tipo:** Transactional
- **Categoria:** Receipts
- **Campos:** 41
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `SHIP_VICS_SEQ_NUM` | Ship_Vics_Seqessorial Num | NUMBER | 22 | 9 | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `SHIP_VICS_CHK_DIGIT` | Ship_Vics_Chkessorial Digit | NUMBER | 22 | 1 | N |
| 5 | `SHIP_VICS_EAN_PREX` | Ship_Vics_Eanessorial Prex | VARCHAR2 | 20 |  | N |
| 6 | `SHIP_VICS_BOL_NUM` | Ship_Vics_Bolessorial Num | VARCHAR2 | 20 |  | N |
| 7 | `SHIP_VICS_STAT` | Ship_Vicsessorial Stat | VARCHAR2 | 1 |  | N |
| 8 | `SHIP_VICS_CREATE_DATE` | Ship_Vics_Createessorial Date | DATE | 7 |  | N |
| 9 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 10 | `SHIP_VICS_TO_ARR_DATE` | Ship_Vics_To_Arressorial Date | DATE | 7 |  | Y |
| 11 | `SHIP_VICS_CLOSE_DATE` | Ship_Vics_Closeessorial Date | DATE | 7 |  | Y |
| 12 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | N |
| 13 | `SHIP_VICS_SID_REF` | Ship_Vics_Sidessorial Ref | VARCHAR2 | 30 |  | Y |
| 14 | `SHIP_VICS_CID_REF` | Ship_Vics_Cidessorial Ref | VARCHAR2 | 30 |  | Y |
| 15 | `SHIP_VICS_REF1` | Ship_Vicsessorial Ref1 | VARCHAR2 | 30 |  | Y |
| 16 | `SHIP_VICS_REF2` | Ship_Vicsessorial Ref2 | VARCHAR2 | 30 |  | Y |
| 17 | `SHIP_VICS_FOB_FLAG` | Ship_Vics_Fobessorial Flag | VARCHAR2 | 1 |  | N |
| 18 | `SHIP_VICS_PRE_FLAG` | Ship_Vics_Preessorial Flag | VARCHAR2 | 1 |  | N |
| 19 | `SHIP_VICS_COL_FLAG` | Ship_Vics_Colessorial Flag | VARCHAR2 | 1 |  | N |
| 20 | `SHIP_VICS_THIRD_FLAG` | Ship_Vics_Thirdessorial Flag | VARCHAR2 | 1 |  | N |
| 21 | `SHIP_VICS_TRAILER` | Ship_Vicsessorial Trailer | VARCHAR2 | 20 |  | Y |
| 22 | `SHIP_VICS_SEAL` | Ship_Vicsessorial Seal | VARCHAR2 | 20 |  | Y |
| 23 | `SHIP_VICS_PRO_NUM` | Ship_Vics_Proessorial Num | VARCHAR2 | 20 |  | Y |
| 24 | `SHIP_VICS_REM_FLAG` | Ship_Vics_Remessorial Flag | VARCHAR2 | 1 |  | N |
| 25 | `SHIP_VICS_COMD_FLAG` | Ship_Vics_Comdessorial Flag | VARCHAR2 | 1 |  | N |
| 26 | `SHIP_VICS_PRT_DATE` | Ship_Vics_Prtessorial Date | DATE | 7 |  | Y |
| 27 | `SHIP_VICS_PRT_CNT` | Ship_Vics_Prtessorial Cnt | NUMBER | 22 | 4 | Y |
| 28 | `OP_CODE_PRT` | Op_Codeessorial Prt | VARCHAR2 | 20 |  | Y |
| 29 | `SHIP_VICS_PRT_ERR` | Ship_Vics_Prtessorial Err | VARCHAR2 | 250 |  | Y |
| 30 | `SHIP_VICS_THIRD_PARTY_NAME` | Ship_Vics_Third_Partyessorial Name | VARCHAR2 | 30 |  | Y |
| 31 | `SHIP_VICS_THIRD_PARTY_ADD1` | Ship_Vics_Third_Partyessorial Add1 | VARCHAR2 | 30 |  | Y |
| 32 | `SHIP_VICS_THIRD_PARTY_ADD2` | Ship_Vics_Third_Partyessorial Add2 | VARCHAR2 | 30 |  | Y |
| 33 | `SHIP_VICS_THIRD_PARTY_ADD3` | Ship_Vics_Third_Partyessorial Add3 | VARCHAR2 | 30 |  | Y |
| 34 | `SHIP_VICS_THIRD_PARTY_ADD4` | Ship_Vics_Third_Partyessorial Add4 | VARCHAR2 | 30 |  | Y |
| 35 | `SHIP_VICS_THIRD_PARTY_CITY` | Ship_Vics_Third_Partyessorial City | VARCHAR2 | 30 |  | Y |
| 36 | `SHIP_VICS_THIRD_PARTY_STATE` | Ship_Vics_Third_Partyessorial State | VARCHAR2 | 4 |  | Y |
| 37 | `SHIP_VICS_THIRD_PARTY_ZIP` | Ship_Vics_Third_Partyessorial Zip | VARCHAR2 | 10 |  | Y |
| 38 | `SHIP_VICS_THIRD_PARTY_COUNTRY` | Ship_Vics_Third_Partyessorial Country | VARCHAR2 | 4 |  | Y |
| 39 | `CON_CODE` | Consignee Code | VARCHAR2 | 10 |  | N |
| 40 | `CON_NAME` | Consignee Name | VARCHAR2 | 30 |  | Y |
| 41 | `SHIP_VICS_PALL_SLIP_FLAG` | Ship_Vics_Pall_Slipessorial Flag | VARCHAR2 | 1 |  | Y |

## `E_SYVOX_ASSEM`

- **Tipo:** Transactional
- **Categoria:** Receipts
- **Campos:** 9
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 3 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | Y |
| 4 | `ORD_LOC_LINE_NUM` | Ord_Loc_Lineessorial Num | NUMBER | 22 | 4 | Y |
| 5 | `SYVOX_PROS_ORD_SEQ` | Syvox_Pros_Ordessorial Seq | NUMBER | 22 | 6 | N |
| 6 | `SYVOX_ASSEM_INOUT_FLAG` | Syvox_Assem_Inoutessorial Flag | VARCHAR2 | 1 |  | N |
| 7 | `SYVOX_ASSEM_MESS_ID` | Syvox_Assem_Messessorial Id | VARCHAR2 | 12 |  | Y |
| 8 | `SYVOX_ASSEM_TEXT` | Syvox_Assemessorial Text | VARCHAR2 | 2000 |  | Y |
| 9 | `SYVOX_ASSEM_DATE` | Syvox_Assemessorial Date | DATE | 7 |  | Y |

## `E_SYVOX_MESS`

- **Tipo:** Transactional
- **Categoria:** Receipts
- **Campos:** 5

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `MESS_ID` | Messessorial Id | NUMBER | 22 | 6 | N |
| 2 | `MESS_ID_DES` | Mess_Idessorial Des | VARCHAR2 | 40 |  | N |
| 3 | `RESP_MESS_ID` | Resp_Messessorial Id | NUMBER | 22 | 6 | Y |
| 4 | `RESP_MESS_ID_DES` | Resp_Mess_Idessorial Des | VARCHAR2 | 40 |  | Y |
| 5 | `CHANNEL_MODE_FLAG` | Channel_Modeessorial Flag | VARCHAR2 | 1 |  | N |

## `E_SYVOX_PROS`

- **Tipo:** Transactional
- **Categoria:** Receipts
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 3 | `SYVOX_PROS_ORD_SEQ` | Syvox_Pros_Ordessorial Seq | NUMBER | 22 | 6 | N |
| 4 | `SYVOX_PROS_FLAG` | Syvox_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `SYVOX_PROS_START_DATE` | Syvox_Pros_Startessorial Date | DATE | 7 |  | N |
| 6 | `SYVOX_PROS_INOUT_FLAG` | Syvox_Pros_Inoutessorial Flag | VARCHAR2 | 1 |  | N |
| 7 | `SYVOX_PROS_OUT_ACK_STAT` | Syvox_Pros_Out_Ackessorial Stat | VARCHAR2 | 40 |  | Y |
| 8 | `SYVOX_PROS_OUT_ACK_DATE` | Syvox_Pros_Out_Ackessorial Date | DATE | 7 |  | Y |
| 9 | `SYVOX_PROS_IN_ACK_STAT` | Syvox_Pros_In_Ackessorial Stat | VARCHAR2 | 40 |  | Y |
| 10 | `SYVOX_PROS_IN_ACK_DATE` | Syvox_Pros_In_Ackessorial Date | DATE | 7 |  | Y |
| 11 | `SYVOX_PROS_END_DATE` | Syvox_Pros_Endessorial Date | DATE | 7 |  | Y |

## `E_TAKE_AR_INV_D`

- **Tipo:** Transactional
- **Categoria:** Receipts
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `INV_NUM` | Invoice Number | NUMBER | 22 | 9 | N |
| 3 | `INV_REM_LINE_NUM` | Inv_Rem_Lineessorial Num | NUMBER | 22 | 3 | N |
| 4 | `INV_REM_LINE_TEXT` | Inv_Rem_Lineessorial Text | VARCHAR2 | 45 |  | Y |

## `E_TAKE_AR_INV_H`

- **Tipo:** Transactional
- **Categoria:** Receipts
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `BAT_NUM` | Batch Number | NUMBER | 22 | 9 | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `INV_NUM` | Invoice Number | NUMBER | 22 | 9 | N |
| 5 | `INV_PREX` | Invoice Prefix | VARCHAR2 | 4 |  | N |
| 6 | `INV_SUFX` | Invoice Suffix | VARCHAR2 | 4 |  | Y |
| 7 | `INV_DATE` | Invessorial Date | DATE | 7 |  | N |
| 8 | `INV_AMT` | Invoice Amount | NUMBER | 22 | 15 | N |
| 9 | `TERM_CODE` | Termessorial Code | VARCHAR2 | 4 |  | N |
| 10 | `CUR_CODE` | Currency Code | VARCHAR2 | 4 |  | N |
| 11 | `INV_REM_FLAG` | Inv_Remessorial Flag | VARCHAR2 | 1 |  | N |

## `E_TEMP_SYVOX_ORD`

- **Tipo:** Transactional
- **Categoria:** Receipts
- **Campos:** 5
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 5 | `SYVOX_PROS_ERR_MESS` | Syvox_Pros_Erressorial Mess | VARCHAR2 | 40 |  | Y |

## `E_TEXT_MES`

- **Tipo:** Transactional
- **Categoria:** Receipts
- **Campos:** 7
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `CREATE_DATE` | Create Date | DATE | 7 |  | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `TEXT_NUM` | Textessorial Num | NUMBER | 22 | 9 | N |
| 5 | `OP_CODE_FROM` | Op_Codeessorial From | VARCHAR2 | 20 |  | N |
| 6 | `OP_CODE_TO` | Op_Codeessorial To | VARCHAR2 | 20 |  | N |
| 7 | `TEXT_MES` | Textessorial Mes | VARCHAR2 | 250 |  | N |

## `E_TRF_ORD`

- **Tipo:** Transactional
- **Categoria:** Receipts
- **Campos:** 6
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM, RCPT_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 3 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | Y |
| 4 | `ORD_PROS_DATE` | Ord_Prosessorial Date | DATE | 7 |  | N |
| 5 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | Y |
| 6 | `FUNC_CODE` | Funcessorial Code | VARCHAR2 | 4 |  | Y |

## `E_VES`

- **Tipo:** Transactional
- **Categoria:** Receipts
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `VES_SEQ_NUM` | Ves_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `VES_CREATE_DATE` | Ves_Createessorial Date | DATE | 7 |  | N |
| 3 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 4 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 5 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | N |
| 6 | `VES_VOY` | Vesessorial Voy | VARCHAR2 | 20 |  | N |
| 7 | `VES_EXPT_DATE` | Ves_Exptessorial Date | DATE | 7 |  | N |
| 8 | `VES_RECD_DATE` | Ves_Recdessorial Date | DATE | 7 |  | Y |
| 9 | `CARR_CODE_PIER` | Carr_Codeessorial Pier | VARCHAR2 | 10 |  | N |
| 10 | `VES_COMPL_FLAG` | Ves_Complessorial Flag | VARCHAR2 | 1 |  | N |

## `E_VES_CONTAIN_DD`

- **Tipo:** Transactional
- **Categoria:** Receipts
- **Campos:** 17
- **Campos-chave prováveis:** COMP_CODE, SKU_CODE, RCPT_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `VES_CONTAIN_SEQ_NUM` | Ves_Contain_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `VES_CONTAIN_HEALTH_CERT_SEQNUM` | Ves_Contain_Health_Certessorial Seqnum | NUMBER | 22 | 9 | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `HEALTH_CERT_LINE_NUM` | Health_Cert_Lineessorial Num | NUMBER | 22 | 4 | N |
| 5 | `HEALTH_CERT_ITEM_CODE` | Health_Cert_Itemessorial Code | VARCHAR2 | 20 |  | Y |
| 6 | `HEALTH_CERT_ITEM_DES1` | Health_Cert_Itemessorial Des1 | VARCHAR2 | 40 |  | Y |
| 7 | `HEALTH_CERT_LOT` | Health_Certessorial Lot | VARCHAR2 | 40 |  | Y |
| 8 | `HEALTH_CERT_SHIP_MARK` | Health_Cert_Shipessorial Mark | VARCHAR2 | 40 |  | Y |
| 9 | `HEALTH_CERT_QTY` | Health_Certessorial Qty | NUMBER | 22 | 9 | Y |
| 10 | `SKU_CODE` | SKU Code | VARCHAR2 | 4 |  | Y |
| 11 | `HEALTH_CERT_WGT_NET` | Health_Cert_Wgtessorial Net | NUMBER | 22 | 16 | Y |
| 12 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | Y |
| 13 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | Y |
| 14 | `RCPT_LINE_NUM` | Receipt Line Number | NUMBER | 22 | 4 | Y |
| 15 | `HEALTH_CERT_CUST_SHIP_MARK` | Health_Cert_Cust_Shipessorial Mark | VARCHAR2 | 40 |  | Y |
| 16 | `HEALTH_CERT_CUST_QTY` | Health_Cert_Custessorial Qty | NUMBER | 22 | 9 | Y |
| 17 | `HEALTH_CERT_CUST_WGT_NET` | Health_Cert_Cust_Wgtessorial Net | NUMBER | 22 | 16 | Y |

## `E_VES_CONTAIN_H`

- **Tipo:** Transactional
- **Categoria:** Receipts
- **Campos:** 28
- **Campos-chave prováveis:** COMP_CODE, RCPT_NUM, ORD_NUM, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `VES_CONTAIN_SEQ_NUM` | Ves_Contain_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `VES_CONTAIN_CREATE_DATE` | Ves_Contain_Createessorial Date | DATE | 7 |  | N |
| 3 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 4 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 5 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | Y |
| 6 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | Y |
| 7 | `CONTAIN_NUM` | Containessorial Num | VARCHAR2 | 20 |  | N |
| 8 | `VES_SEQ_NUM` | Ves_Seqessorial Num | NUMBER | 22 | 9 | N |
| 9 | `LOAD_TP_CODE` | Load Type Code | VARCHAR2 | 4 |  | N |
| 10 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 11 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 12 | `CARR_CODE_SHIP_LINE` | Carr_Code_Shipessorial Line | VARCHAR2 | 10 |  | N |
| 13 | `VES_CONTAIN_PERMIT_REQ_FLAG` | Ves_Contain_Permit_Reqessorial Flag | VARCHAR2 | 1 |  | Y |
| 14 | `VES_CONTAIN_PERMIT_DATE` | Ves_Contain_Permitessorial Date | DATE | 7 |  | Y |
| 15 | `VES_CONTAIN_PERMIT_EXPT_DATE` | Ves_Contain_Permit_Exptessorial Date | DATE | 7 |  | Y |
| 16 | `VES_CONTAIN_PERMIT_REF` | Ves_Contain_Permitessorial Ref | VARCHAR2 | 20 |  | Y |
| 17 | `VES_CONTAIN_PICKUP_LAST_DATE` | Ves_Contain_Pickup_Lastessorial Date | DATE | 7 |  | Y |
| 18 | `VES_CONTAIN_RETURN_LAST_DATE` | Ves_Contain_Return_Lastessorial Date | DATE | 7 |  | Y |
| 19 | `VES_CONTAIN_LAB_HOUR_RATE` | Ves_Contain_Lab_Houressorial Rate | NUMBER | 22 | 6 | Y |
| 20 | `VES_CONTAIN_RUSH_OP_CODE` | Ves_Contain_Rush_Opessorial Code | VARCHAR2 | 20 |  | Y |
| 21 | `VES_CONTAIN_RUSH_UPD_STAT` | Ves_Contain_Rush_Updessorial Stat | VARCHAR2 | 1 |  | N |
| 22 | `VES_CONTAIN_RUSH_PRTY_TP` | Ves_Contain_Rush_Prtyessorial Tp | VARCHAR2 | 1 |  | Y |
| 23 | `VES_CONTAIN_RUSH_DATE` | Ves_Contain_Rushessorial Date | DATE | 7 |  | Y |
| 24 | `VES_CONTAIN_INTERMODALS` | Ves_Containessorial Intermodals | VARCHAR2 | 80 |  | Y |
| 25 | `VES_CONTAIN_DEST` | Ves_Containessorial Dest | VARCHAR2 | 80 |  | Y |
| 26 | `VES_CONTAIN_SHIP_DATE` | Ves_Contain_Shipessorial Date | DATE | 7 |  | Y |
| 27 | `VES_CONTAIN_COMPL_FLAG` | Ves_Contain_Complessorial Flag | VARCHAR2 | 1 |  | N |
| 28 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | Y |

## `H_RCPT_D1`

- **Tipo:** Historical
- **Categoria:** Receipts
- **Campos:** 15
- **Campos-chave prováveis:** COMP_CODE, RCPT_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | N |
| 5 | `RCPT_LINE_NUM` | Receipt Line Number | NUMBER | 22 | 4 | N |
| 6 | `CUST_CODE_CHG` | Cust_Codeessorial Chg | VARCHAR2 | 10 |  | Y |
| 7 | `CHG_CODE` | Charge Code | VARCHAR2 | 6 |  | Y |
| 8 | `CHG_DATE` | Charge Date | DATE | 7 |  | Y |
| 9 | `RCPT_REM_LINE_NUM` | Rcpt_Rem_Lineessorial Num | NUMBER | 22 | 3 | N |
| 10 | `RCPT_REM_LINE_TEXT` | Rcpt_Rem_Lineessorial Text | VARCHAR2 | 45 |  | Y |
| 11 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 12 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 13 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 14 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 15 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `H_RCPT_D10`

- **Tipo:** Historical
- **Categoria:** Receipts
- **Campos:** 21
- **Campos-chave prováveis:** COMP_CODE, RCPT_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | N |
| 5 | `RCPT_LINE_NUM` | Receipt Line Number | NUMBER | 22 | 4 | N |
| 6 | `EDI_PROF_CODE` | Edi_Professorial Code | VARCHAR2 | 4 |  | N |
| 7 | `EDI_TRANS_SET_CODE` | Edi_Trans_Setessorial Code | VARCHAR2 | 4 |  | N |
| 8 | `EDI_DATA_ID_CODE` | Edi_Data_Idessorial Code | VARCHAR2 | 20 |  | N |
| 9 | `EDI_DATA_ID_DES` | Edi_Data_Idessorial Des | VARCHAR2 | 30 |  | N |
| 10 | `EDI_DATA_ID_SEND_FLAG` | Edi_Data_Id_Sendessorial Flag | VARCHAR2 | 1 |  | N |
| 11 | `EDI_DATA_ID_ENTRY_TP_FLAG` | Edi_Data_Id_Entry_Tpessorial Flag | VARCHAR2 | 1 |  | N |
| 12 | `EDI_DATA_ID_LINE_ENTRY_FLAG` | Edi_Data_Id_Line_Entryessorial Flag | VARCHAR2 | 1 |  | N |
| 13 | `EDI_DATA_ID_MAND_FLAG` | Edi_Data_Id_Mandessorial Flag | VARCHAR2 | 1 |  | N |
| 14 | `EDI_DATA_ID_LEN` | Edi_Data_Idessorial Len | VARCHAR2 | 6 |  | N |
| 15 | `COL_TP_CODE` | Col_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 16 | `EDI_DATA_ID_VALUE` | Edi_Data_Idessorial Value | VARCHAR2 | 250 |  | Y |
| 17 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 18 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 19 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 20 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 21 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `H_RCPT_D12`

- **Tipo:** Historical
- **Categoria:** Receipts
- **Campos:** 18
- **Campos-chave prováveis:** COMP_CODE, RCPT_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | N |
| 3 | `RCPT_REM_SEQ_NUM` | Rcpt_Rem_Seqessorial Num | NUMBER | 22 | 9 | N |
| 4 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 5 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | N |
| 6 | `RCPT_LINE_NUM` | Receipt Line Number | NUMBER | 22 | 4 | N |
| 7 | `RCPT_REM_CUST_FLAG` | Rcpt_Rem_Custessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `RCPT_REM_SHIP_FLAG` | Rcpt_Rem_Shipessorial Flag | VARCHAR2 | 1 |  | N |
| 9 | `RCPT_REM_CARR_FLAG` | Rcpt_Rem_Carressorial Flag | VARCHAR2 | 1 |  | N |
| 10 | `RCPT_REM_RF_FLAG` | Rcpt_Rem_Rfessorial Flag | VARCHAR2 | 1 |  | N |
| 11 | `RCPT_DOC_CODE_REST` | Rcpt_Doc_Codeessorial Rest | VARCHAR2 | 4 |  | Y |
| 12 | `RCPT_REM_MES_CODE` | Rcpt_Rem_Mesessorial Code | VARCHAR2 | 4 |  | Y |
| 13 | `RCPT_REM_TEXT` | Rcpt_Remessorial Text | VARCHAR2 | 2000 |  | Y |
| 14 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 15 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 16 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 17 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 18 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `H_RCPT_D2`

- **Tipo:** Historical
- **Categoria:** Receipts
- **Campos:** 25
- **Campos-chave prováveis:** COMP_CODE, RCPT_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | N |
| 5 | `RCPT_LINE_NUM` | Receipt Line Number | NUMBER | 22 | 4 | N |
| 6 | `PROF_TP_CODE` | Prof_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 7 | `EXTRA_CHG_PROF_CODE` | Extra_Chg_Professorial Code | VARCHAR2 | 4 |  | N |
| 8 | `EXTRA_CHG_PROF_SEQ_NUM` | Extra_Chg_Prof_Seqessorial Num | NUMBER | 22 | 2 | N |
| 9 | `CHG_CODE` | Charge Code | VARCHAR2 | 6 |  | N |
| 10 | `GRP_CODE` | Grpessorial Code | VARCHAR2 | 4 |  | N |
| 11 | `EXTRA_CHG_PROF_ACTN_FLAG` | Extra_Chg_Prof_Actnessorial Flag | VARCHAR2 | 1 |  | N |
| 12 | `EXTRA_CHG_PROF_ENTRY_TP_FLAG` | Extra_Chg_Prof_Entry_Tpessorial Flag | VARCHAR2 | 1 |  | N |
| 13 | `EXTRA_CHG_PROF_OVRR_QTY_FLAG` | Extra_Chg_Prof_Ovrr_Qtyessorial Flag | VARCHAR2 | 1 |  | N |
| 14 | `EXTRA_CHG_PROF_TREAT_FLAG` | Extra_Chg_Prof_Treatessorial Flag | VARCHAR2 | 1 |  | N |
| 15 | `BILL_TO_TP_CODE` | Bill_To_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 16 | `RCPT_EXTRA_CHG_QTY` | Rcpt_Extra_Chgessorial Qty | NUMBER | 22 | 16 | Y |
| 17 | `RCPT_EXTRA_CHG_PROS_FLAG` | Rcpt_Extra_Chg_Prosessorial Flag | VARCHAR2 | 1 |  | Y |
| 18 | `RCPT_EXTRA_CHG_ACCEPT_FLAG` | Rcpt_Extra_Chg_Acceptessorial Flag | VARCHAR2 | 1 |  | Y |
| 19 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | Y |
| 20 | `RCPT_EXTRA_CHG_LAST_DATE` | Rcpt_Extra_Chg_Lastessorial Date | DATE | 7 |  | Y |
| 21 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 22 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 23 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 24 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 25 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `H_RCPT_D3`

- **Tipo:** Historical
- **Categoria:** Receipts
- **Campos:** 26
- **Campos-chave prováveis:** COMP_CODE, RCPT_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | N |
| 5 | `DRV_CODE` | Driver Code | VARCHAR2 | 4 |  | Y |
| 6 | `RCPT_POW_UNIT_NUM` | Rcpt_Pow_Unitessorial Num | VARCHAR2 | 20 |  | Y |
| 7 | `RCPT_CARRY_UNIT_NUM` | Rcpt_Carry_Unitessorial Num | VARCHAR2 | 20 |  | Y |
| 8 | `RCPT_VES` | Rcptessorial Ves | VARCHAR2 | 20 |  | Y |
| 9 | `RCPT_VOY` | Rcptessorial Voy | VARCHAR2 | 20 |  | Y |
| 10 | `RCPT_SEAL1` | Rcptessorial Seal1 | VARCHAR2 | 20 |  | Y |
| 11 | `RCPT_SEAL2` | Rcptessorial Seal2 | VARCHAR2 | 20 |  | Y |
| 12 | `RCPT_TEMP_FRONT` | Rcpt_Tempessorial Front | VARCHAR2 | 10 |  | Y |
| 13 | `RCPT_TEMP_MID` | Rcpt_Tempessorial Mid | VARCHAR2 | 10 |  | Y |
| 14 | `RCPT_TEMP_BACK` | Rcpt_Tempessorial Back | VARCHAR2 | 10 |  | Y |
| 15 | `DRV_NAME_MAN` | Drv_Nameessorial Man | VARCHAR2 | 30 |  | Y |
| 16 | `RCPT_SEAL1_INTACT` | Rcpt_Seal1essorial Intact | VARCHAR2 | 1 |  | Y |
| 17 | `RCPT_TEMP_SET` | Rcpt_Tempessorial Set | VARCHAR2 | 10 |  | Y |
| 18 | `RCPT_TEMP_AMB` | Rcpt_Tempessorial Amb | VARCHAR2 | 10 |  | Y |
| 19 | `RCPT_PALL_QTY_IN` | Rcpt_Pall_Qtyessorial In | NUMBER | 22 | 4 | Y |
| 20 | `RCPT_PALL_QTY_OUT` | Rcpt_Pall_Qtyessorial Out | NUMBER | 22 | 4 | Y |
| 21 | `RCPT_TEMP_6` | Rcpt_Tempessorial 6 | VARCHAR2 | 10 |  | Y |
| 22 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 23 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 24 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 25 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 26 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `H_RCPT_D4`

- **Tipo:** Historical
- **Categoria:** Receipts
- **Campos:** 15
- **Campos-chave prováveis:** COMP_CODE, RCPT_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | N |
| 5 | `PALL_ACC_CODE` | Pall_Accessorial Code | VARCHAR2 | 10 |  | N |
| 6 | `PALL_ACC_TP` | Pall_Accessorial Tp | VARCHAR2 | 4 |  | N |
| 7 | `PALL_TRANS_TP` | Pall_Transessorial Tp | VARCHAR2 | 1 |  | N |
| 8 | `PALL_CODE` | Pallessorial Code | VARCHAR2 | 4 |  | N |
| 9 | `PALL_QTY` | Pallessorial Qty | NUMBER | 22 | 4 | N |
| 10 | `PALL_REF_DES` | Pall_Refessorial Des | VARCHAR2 | 60 |  | Y |
| 11 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 12 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 13 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 14 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 15 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `H_RCPT_D5`

- **Tipo:** Historical
- **Categoria:** Receipts
- **Campos:** 80
- **Campos-chave prováveis:** COMP_CODE, RCPT_NUM, SKU_CODE, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | N |
| 5 | `RCPT_LINE_NUM` | Receipt Line Number | NUMBER | 22 | 4 | N |
| 6 | `RCPT_LINE_TP` | Rcpt_Lineessorial Tp | VARCHAR2 | 1 |  | N |
| 7 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | N |
| 8 | `RCPT_EXPT_ENT_QTY` | Rcpt_Expt_Entessorial Qty | VARCHAR2 | 20 |  | N |
| 9 | `RCPT_RECD_ENT_QTY` | Rcpt_Recd_Entessorial Qty | VARCHAR2 | 20 |  | N |
| 10 | `RCPT_RECD_QTY` | Rcpt_Recdessorial Qty | NUMBER | 22 | 9 | N |
| 11 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | N |
| 12 | `RCPT_UNIT_WGT` | Rcpt_Unitessorial Wgt | NUMBER | 22 | 16 | N |
| 13 | `SKU_CODE` | SKU Code | VARCHAR2 | 4 |  | N |
| 14 | `RCPT_TOT_WGT` | Rcpt_Totessorial Wgt | NUMBER | 22 | 16 | N |
| 15 | `RCPT_TOT_WGT_NET` | Rcpt_Tot_Wgtessorial Net | NUMBER | 22 | 16 | N |
| 16 | `LINEAR_MEAS_CODE` | Linear Measurement Code | VARCHAR2 | 4 |  | N |
| 17 | `RCPT_TOT_CUBE` | Rcpt_Totessorial Cube | NUMBER | 22 | 16 | N |
| 18 | `RCPT_LINE_REM_FLAG` | Rcpt_Line_Remessorial Flag | VARCHAR2 | 1 |  | N |
| 19 | `RCPT_LINE_EXTRA_CHG_FLAG` | Rcpt_Line_Extra_Chgessorial Flag | VARCHAR2 | 1 |  | N |
| 20 | `RCPT_LINE_ALTER_FLAG` | Rcpt_Line_Alteressorial Flag | VARCHAR2 | 1 |  | N |
| 21 | `RCPT_LINE_LOC_BAL_FLAG` | Rcpt_Line_Loc_Balessorial Flag | VARCHAR2 | 1 |  | N |
| 22 | `RCPT_LINE_LOC_GEN_FLAG` | Rcpt_Line_Loc_Genessorial Flag | VARCHAR2 | 1 |  | N |
| 23 | `RCPT_LINE_CONF_FLAG` | Rcpt_Line_Confessorial Flag | VARCHAR2 | 1 |  | N |
| 24 | `RCPT_LINE_RATE_FLAG` | Rcpt_Line_Rateessorial Flag | VARCHAR2 | 1 |  | N |
| 25 | `RCPT_LINE_EDI_INFO_FLAG` | Rcpt_Line_Edi_Infoessorial Flag | VARCHAR2 | 1 |  | N |
| 26 | `RCPT_LINE_ITEM_PROS_FLAG` | Rcpt_Line_Item_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 27 | `RCPT_LEV1` | Rcptessorial Lev1 | VARCHAR2 | 40 |  | Y |
| 28 | `RCPT_SEQ_QTY_LEV1` | Rcpt_Seq_Qtyessorial Lev1 | NUMBER | 22 | 4 | Y |
| 29 | `RCPT_LEV2` | Rcptessorial Lev2 | VARCHAR2 | 40 |  | Y |
| 30 | `RCPT_SEQ_QTY_LEV2` | Rcpt_Seq_Qtyessorial Lev2 | NUMBER | 22 | 4 | Y |
| 31 | `RCPT_LEV3` | Rcptessorial Lev3 | VARCHAR2 | 40 |  | Y |
| 32 | `RCPT_SEQ_QTY_LEV3` | Rcpt_Seq_Qtyessorial Lev3 | NUMBER | 22 | 4 | Y |
| 33 | `RCPT_LEV4` | Rcptessorial Lev4 | VARCHAR2 | 40 |  | Y |
| 34 | `RCPT_SEQ_QTY_LEV4` | Rcpt_Seq_Qtyessorial Lev4 | NUMBER | 22 | 4 | Y |
| 35 | `RCPT_LEV5` | Rcptessorial Lev5 | VARCHAR2 | 40 |  | Y |
| 36 | `RCPT_SEQ_QTY_LEV5` | Rcpt_Seq_Qtyessorial Lev5 | NUMBER | 22 | 4 | Y |
| 37 | `RCPT_CLS_DATE` | Rcpt_Clsessorial Date | DATE | 7 |  | Y |
| 38 | `RCPT_EXPY_DATE` | Rcpt_Expyessorial Date | DATE | 7 |  | Y |
| 39 | `RCPT_LINE_CONF_DATE` | Rcpt_Line_Confessorial Date | DATE | 7 |  | Y |
| 40 | `RCPT_LINE_LEN` | Rcpt_Lineessorial Len | NUMBER | 22 | 16 | Y |
| 41 | `RCPT_LINE_WID` | Rcpt_Lineessorial Wid | NUMBER | 22 | 16 | Y |
| 42 | `RCPT_LINE_HGT` | Rcpt_Lineessorial Hgt | NUMBER | 22 | 16 | Y |
| 43 | `RCPT_LINE_TEMP` | Rcpt_Lineessorial Temp | NUMBER | 22 | 5 | Y |
| 44 | `CRS_DOCK_PROF_CODE` | Crs_Dock_Professorial Code | VARCHAR2 | 4 |  | Y |
| 45 | `RCPT_LEV_DES1` | Rcpt_Levessorial Des1 | VARCHAR2 | 40 |  | Y |
| 46 | `RCPT_LEV_DES2` | Rcpt_Levessorial Des2 | VARCHAR2 | 40 |  | Y |
| 47 | `RCPT_LEV_DES3` | Rcpt_Levessorial Des3 | VARCHAR2 | 40 |  | Y |
| 48 | `RCPT_LEV_DES4` | Rcpt_Levessorial Des4 | VARCHAR2 | 40 |  | Y |
| 49 | `RCPT_LEV_DES5` | Rcpt_Levessorial Des5 | VARCHAR2 | 40 |  | Y |
| 50 | `INVT_QTY_BKD_FACT` | Invt_Qty_Bkdessorial Fact | VARCHAR2 | 30 |  | Y |
| 51 | `REAS_CODE` | Reasessorial Code | VARCHAR2 | 4 |  | Y |
| 52 | `RCPT_DIST_ORD_NUM` | Rcpt_Dist_Ordessorial Num | NUMBER | 22 | 9 | Y |
| 53 | `RCPT_DIST_ORD_LINE_NUM` | Rcpt_Dist_Ord_Lineessorial Num | NUMBER | 22 | 4 | Y |
| 54 | `BOND_NUM` | Bond Number | VARCHAR2 | 20 |  | Y |
| 55 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |
| 56 | `RCPT_LINE_SRCE_LINE` | Rcpt_Line_Srceessorial Line | NUMBER | 22 | 4 | Y |
| 57 | `RCPT_EXT_INV_NUM` | Rcpt_Ext_Invessorial Num | NUMBER | 22 | 16 | Y |
| 58 | `RCPT_EXT_INV_PREX` | Rcpt_Ext_Invessorial Prex | VARCHAR2 | 4 |  | Y |
| 59 | `RCPT_EXT_INV_DATE` | Rcpt_Ext_Invessorial Date | DATE | 7 |  | Y |
| 60 | `WHSE_CODE_REST` | Whse_Codeessorial Rest | VARCHAR2 | 4 |  | Y |
| 61 | `PO_LINE_NUM` | Po_Lineessorial Num | NUMBER | 22 | 4 | Y |
| 62 | `PO_NUM` | PO Number | NUMBER | 22 | 9 | Y |
| 63 | `RCPT_LINE_NUM_UPDOWNSTREAM` | Rcpt_Line_Numessorial Updownstream | NUMBER | 22 | 4 | Y |
| 64 | `RCPT_LINE_SKIP_PUTAWAY_FLAG` | Rcpt_Line_Skip_Putawayessorial Flag | VARCHAR2 | 1 |  | Y |
| 65 | `RCPT_LINE_EXT_ID` | Rcpt_Line_Extessorial Id | VARCHAR2 | 40 |  | Y |
| 66 | `WHSE_CODE_SUG` | Whse_Codeessorial Sug | VARCHAR2 | 4 |  | Y |
| 67 | `LOC_CODE_SUG` | Loc_Codeessorial Sug | VARCHAR2 | 12 |  | Y |
| 68 | `RCPT_LINE_EDI_CREATE_FLAG` | Rcpt_Line_Edi_Createessorial Flag | VARCHAR2 | 1 |  | Y |
| 69 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 70 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 71 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 72 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 73 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 74 | `RCPT_LINE_MIN_MAX_DATE_OVER` | Rcpt_Line_Min_Max_Dateessorial Over | VARCHAR2 | 1 |  | Y |
| 75 | `ITEM_LOC_PROF_CODE` | Item_Loc_Professorial Code | VARCHAR2 | 4 |  | Y |
| 76 | `RCPT_LINE_SKIP_PROS_VALI_TP` | Rcpt_Line_Skip_Pros_Valiessorial Tp | VARCHAR2 | 1 |  | Y |
| 77 | `RCPT_LINE_NUM_LAY` | Rcpt_Line_Numessorial Lay | NUMBER | 22 | 3 | Y |
| 78 | `RCPT_LINE_QTY_LAY` | Rcpt_Line_Qtyessorial Lay | NUMBER | 22 | 3 | Y |
| 79 | `RCPT_LINE_QTY_ODD_LAY` | Rcpt_Line_Qty_Oddessorial Lay | NUMBER | 22 | 3 | Y |
| 80 | `RCPT_LINE_THL_VARI_PASS_FLAG` | Rcpt_Line_Thl_Vari_Passessorial Flag | VARCHAR2 | 1 |  | Y |

## `H_RCPT_D5D1`

- **Tipo:** Historical
- **Categoria:** Receipts
- **Campos:** 35
- **Campos-chave prováveis:** COMP_CODE, RCPT_NUM, CUST_CODE, INVT_LEV1, LOC_CODE, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | N |
| 5 | `RCPT_LINE_NUM` | Receipt Line Number | NUMBER | 22 | 4 | N |
| 6 | `RCPT_LOC_LINE_NUM` | Rcpt_Loc_Lineessorial Num | NUMBER | 22 | 4 | N |
| 7 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 8 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 9 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | N |
| 10 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 11 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | Y |
| 12 | `RCPT_LOC_ENT_QTY` | Rcpt_Loc_Entessorial Qty | VARCHAR2 | 20 |  | N |
| 13 | `RCPT_LOC_QTY` | Rcpt_Locessorial Qty | NUMBER | 22 | 9 | N |
| 14 | `RCPT_LOC_CNVC_QTY` | Rcpt_Loc_Cnvcessorial Qty | NUMBER | 22 | 6 | Y |
| 15 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | N |
| 16 | `RCPT_LOC_PROS_FLAG` | Rcpt_Loc_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 17 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |
| 18 | `HOLD_SHIP_FLAG` | Hold_Shipessorial Flag | VARCHAR2 | 1 |  | Y |
| 19 | `HOLD_RENW_FLAG` | Hold_Renwessorial Flag | VARCHAR2 | 1 |  | Y |
| 20 | `WHSE_CODE_ORG` | Whse_Codeessorial Org | VARCHAR2 | 4 |  | Y |
| 21 | `LOC_CODE_ORG` | Loc_Codeessorial Org | VARCHAR2 | 12 |  | Y |
| 22 | `LOC_SIZE_CODE` | Loc_Sizeessorial Code | VARCHAR2 | 4 |  | Y |
| 23 | `WHSE_CODE_STATIC` | Whse_Codeessorial Static | VARCHAR2 | 4 |  | Y |
| 24 | `LOC_CODE_STATIC` | Loc_Codeessorial Static | VARCHAR2 | 12 |  | Y |
| 25 | `WHSE_CODE_MOVE` | Whse_Codeessorial Move | VARCHAR2 | 4 |  | Y |
| 26 | `LOC_CODE_MOVE` | Loc_Codeessorial Move | VARCHAR2 | 12 |  | Y |
| 27 | `RCPT_LOC_EXPT_QTY` | Rcpt_Loc_Exptessorial Qty | NUMBER | 22 | 9 | Y |
| 28 | `LOOSE_WHSE_CODE_STATIC` | Loose_Whse_Codeessorial Static | VARCHAR2 | 4 |  | Y |
| 29 | `LOOSE_LOC_CODE_STATIC` | Loose_Loc_Codeessorial Static | VARCHAR2 | 12 |  | Y |
| 30 | `WHSE_ACT_TP_NUM` | Whse_Act_Tpessorial Num | NUMBER | 22 | 2 | Y |
| 31 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 32 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 33 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 34 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 35 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `H_RCPT_D5D2`

- **Tipo:** Historical
- **Categoria:** Receipts
- **Campos:** 23
- **Campos-chave prováveis:** COMP_CODE, RCPT_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | N |
| 5 | `RCPT_LINE_NUM` | Receipt Line Number | NUMBER | 22 | 4 | N |
| 6 | `PROS_CODE` | Prosessorial Code | VARCHAR2 | 4 |  | N |
| 7 | `PROS_LINE_NUM` | Pros_Lineessorial Num | NUMBER | 22 | 6 | N |
| 8 | `PROS_DES` | Prosessorial Des | VARCHAR2 | 30 |  | N |
| 9 | `PROS_TP_CODE` | Pros_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 10 | `PROS_LEN` | Prosessorial Len | VARCHAR2 | 6 |  | N |
| 11 | `COL_TP_CODE` | Col_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 12 | `SKU_CLASS_NUM` | Sku_Classessorial Num | NUMBER | 22 | 1 | N |
| 13 | `PROS_VALUE` | Prosessorial Value | VARCHAR2 | 250 |  | Y |
| 14 | `RCPT_LOC_LINE_NUM` | Rcpt_Loc_Lineessorial Num | NUMBER | 22 | 4 | Y |
| 15 | `RCPT_PROS_PRT_FLAG` | Rcpt_Pros_Prtessorial Flag | VARCHAR2 | 1 |  | Y |
| 16 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | Y |
| 17 | `PROS_REF` | Prosessorial Ref | VARCHAR2 | 250 |  | Y |
| 18 | `RCPT_PROS_VALID_FLAG` | Rcpt_Pros_Validessorial Flag | VARCHAR2 | 1 |  | Y |
| 19 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 20 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 21 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 22 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 23 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `H_RCPT_D5D3`

- **Tipo:** Historical
- **Categoria:** Receipts
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE, RCPT_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | N |
| 5 | `RCPT_LINE_NUM` | Receipt Line Number | NUMBER | 22 | 4 | N |
| 6 | `DOC_CODE` | Document Code | VARCHAR2 | 4 |  | N |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `H_RCPT_D5D4`

- **Tipo:** Historical
- **Categoria:** Receipts
- **Campos:** 16
- **Campos-chave prováveis:** COMP_CODE, RCPT_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | N |
| 5 | `RCPT_LINE_NUM` | Receipt Line Number | NUMBER | 22 | 4 | N |
| 6 | `INVT_ATTR_PROF_CODE` | Invt_Attr_Professorial Code | VARCHAR2 | 4 |  | N |
| 7 | `INVT_ATTR_NAME` | Invt_Attressorial Name | VARCHAR2 | 20 |  | N |
| 8 | `INVT_ATTR_VAL` | Invt_Attressorial Val | VARCHAR2 | 40 |  | Y |
| 9 | `INVT_ATTR_VAL_ORG` | Invt_Attr_Valessorial Org | VARCHAR2 | 40 |  | Y |
| 10 | `INVT_ATTR_RCPT_EXCL_FLAG` | Invt_Attr_Rcpt_Exclessorial Flag | VARCHAR2 | 1 |  | Y |
| 11 | `INVT_ATTR_ALLOW_OVER_NAME` | Invt_Attr_Allow_Overessorial Name | VARCHAR2 | 1 |  | Y |
| 12 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 13 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 14 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 15 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 16 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `H_RCPT_D5D5`

- **Tipo:** Historical
- **Categoria:** Receipts
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE, RCPT_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | N |
| 5 | `RCPT_LINE_NUM` | Receipt Line Number | NUMBER | 22 | 4 | N |
| 6 | `RCPT_REF_VAL` | Rcpt_Refessorial Val | VARCHAR2 | 40 |  | N |
| 7 | `RCPT_REF_QUAL_CODE` | Rcpt_Ref_Qualessorial Code | VARCHAR2 | 4 |  | Y |
| 8 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 9 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 11 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `H_RCPT_D6`

- **Tipo:** Historical
- **Categoria:** Receipts
- **Campos:** 24
- **Campos-chave prováveis:** COMP_CODE, RCPT_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | N |
| 5 | `INFO_FLOW_SEQ_NUM` | Info_Flow_Seqessorial Num | NUMBER | 22 | 2 | N |
| 6 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | N |
| 7 | `INFO_FLOW_MAND_FLAG` | Info_Flow_Mandessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `INFO_FLOW_DOC_SEQ_NUM` | Info_Flow_Doc_Seqessorial Num | NUMBER | 22 | 2 | N |
| 9 | `DOC_CODE` | Document Code | VARCHAR2 | 4 |  | Y |
| 10 | `FORM_CODE` | Form Code | VARCHAR2 | 4 |  | Y |
| 11 | `DOC_PRT_TP_FLAG` | Doc_Prt_Tpessorial Flag | VARCHAR2 | 1 |  | Y |
| 12 | `RCPT_DOC_PRT_STAT` | Rcpt_Doc_Prtessorial Stat | VARCHAR2 | 1 |  | Y |
| 13 | `RCPT_DOC_REPRT_CNT` | Rcpt_Doc_Reprtessorial Cnt | NUMBER | 22 | 4 | Y |
| 14 | `INFO_FLOW_ASS_LOC_FLAG` | Info_Flow_Ass_Locessorial Flag | VARCHAR2 | 1 |  | N |
| 15 | `INFO_FLOW_DEALLOC_FLAG` | Info_Flow_Deallocessorial Flag | VARCHAR2 | 1 |  | N |
| 16 | `LAB_STD_NUM_PROF_CODE` | Lab_Std_Num_Professorial Code | VARCHAR2 | 4 |  | Y |
| 17 | `LAB_STD_UOM` | Lab_Stdessorial Uom | VARCHAR2 | 4 |  | Y |
| 18 | `LAB_STD_MODY_PROF_CODE` | Lab_Std_Mody_Professorial Code | VARCHAR2 | 4 |  | Y |
| 19 | `INFO_FLOW_CREATE_DRMS_FLAG` | Info_Flow_Create_Drmsessorial Flag | VARCHAR2 | 1 |  | Y |
| 20 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 21 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 22 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 23 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 24 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `H_RCPT_D7`

- **Tipo:** Historical
- **Categoria:** Receipts
- **Campos:** 46
- **Campos-chave prováveis:** COMP_CODE, RCPT_NUM, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | N |
| 5 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 6 | `CUST_INVT_PROF_CODE` | Cust_Invt_Professorial Code | VARCHAR2 | 4 |  | N |
| 7 | `RCPT_ITEM_LEV` | Rcpt_Itemessorial Lev | VARCHAR2 | 9 |  | N |
| 8 | `RCPT_ITEM_LEV_DES` | Rcpt_Item_Levessorial Des | VARCHAR2 | 13 |  | N |
| 9 | `RCPT_CHG_LEV_NUM` | Rcpt_Chg_Levessorial Num | NUMBER | 22 | 1 | N |
| 10 | `RCPT_INVT_TERMGY_CODE_LEV1` | Rcpt_Invt_Termgy_Codeessorial Lev1 | VARCHAR2 | 4 |  | N |
| 11 | `RCPT_LEV_NUM_LEV1` | Rcpt_Lev_Numessorial Lev1 | NUMBER | 22 | 1 | N |
| 12 | `RCPT_INVT_LEV1` | Rcpt_Invtessorial Lev1 | VARCHAR2 | 9 |  | N |
| 13 | `RCPT_ASS_FLAG_LEV1` | Rcpt_Ass_Flagessorial Lev1 | VARCHAR2 | 1 |  | N |
| 14 | `RCPT_SEQ_NUM_FLAG_LEV1` | Rcpt_Seq_Num_Flagessorial Lev1 | VARCHAR2 | 1 |  | N |
| 15 | `CUST_INVT_ASS_PROF_CODE_LEV1` | Cust_Invt_Ass_Prof_Codeessorial Lev1 | VARCHAR2 | 4 |  | Y |
| 16 | `RCPT_INVT_TERMGY_CODE_LEV2` | Rcpt_Invt_Termgy_Codeessorial Lev2 | VARCHAR2 | 4 |  | Y |
| 17 | `RCPT_LEV_NUM_LEV2` | Rcpt_Lev_Numessorial Lev2 | NUMBER | 22 | 1 | Y |
| 18 | `RCPT_INVT_LEV2` | Rcpt_Invtessorial Lev2 | VARCHAR2 | 9 |  | Y |
| 19 | `RCPT_ASS_FLAG_LEV2` | Rcpt_Ass_Flagessorial Lev2 | VARCHAR2 | 1 |  | Y |
| 20 | `RCPT_SEQ_NUM_FLAG_LEV2` | Rcpt_Seq_Num_Flagessorial Lev2 | VARCHAR2 | 1 |  | Y |
| 21 | `CUST_INVT_ASS_PROF_CODE_LEV2` | Cust_Invt_Ass_Prof_Codeessorial Lev2 | VARCHAR2 | 4 |  | Y |
| 22 | `RCPT_INVT_TERMGY_CODE_LEV3` | Rcpt_Invt_Termgy_Codeessorial Lev3 | VARCHAR2 | 4 |  | Y |
| 23 | `RCPT_LEV_NUM_LEV3` | Rcpt_Lev_Numessorial Lev3 | NUMBER | 22 | 1 | Y |
| 24 | `RCPT_INVT_LEV3` | Rcpt_Invtessorial Lev3 | VARCHAR2 | 9 |  | Y |
| 25 | `RCPT_ASS_FLAG_LEV3` | Rcpt_Ass_Flagessorial Lev3 | VARCHAR2 | 1 |  | Y |
| 26 | `RCPT_SEQ_NUM_FLAG_LEV3` | Rcpt_Seq_Num_Flagessorial Lev3 | VARCHAR2 | 1 |  | Y |
| 27 | `CUST_INVT_ASS_PROF_CODE_LEV3` | Cust_Invt_Ass_Prof_Codeessorial Lev3 | VARCHAR2 | 4 |  | Y |
| 28 | `RCPT_INVT_TERMGY_CODE_LEV4` | Rcpt_Invt_Termgy_Codeessorial Lev4 | VARCHAR2 | 4 |  | Y |
| 29 | `RCPT_LEV_NUM_LEV4` | Rcpt_Lev_Numessorial Lev4 | NUMBER | 22 | 1 | Y |
| 30 | `RCPT_INVT_LEV4` | Rcpt_Invtessorial Lev4 | VARCHAR2 | 9 |  | Y |
| 31 | `RCPT_ASS_FLAG_LEV4` | Rcpt_Ass_Flagessorial Lev4 | VARCHAR2 | 1 |  | Y |
| 32 | `RCPT_SEQ_NUM_FLAG_LEV4` | Rcpt_Seq_Num_Flagessorial Lev4 | VARCHAR2 | 1 |  | Y |
| 33 | `CUST_INVT_ASS_PROF_CODE_LEV4` | Cust_Invt_Ass_Prof_Codeessorial Lev4 | VARCHAR2 | 4 |  | Y |
| 34 | `RCPT_INVT_TERMGY_CODE_LEV5` | Rcpt_Invt_Termgy_Codeessorial Lev5 | VARCHAR2 | 4 |  | Y |
| 35 | `RCPT_LEV_NUM_LEV5` | Rcpt_Lev_Numessorial Lev5 | NUMBER | 22 | 1 | Y |
| 36 | `RCPT_INVT_LEV5` | Rcpt_Invtessorial Lev5 | VARCHAR2 | 9 |  | Y |
| 37 | `RCPT_ASS_FLAG_LEV5` | Rcpt_Ass_Flagessorial Lev5 | VARCHAR2 | 1 |  | Y |
| 38 | `RCPT_SEQ_NUM_FLAG_LEV5` | Rcpt_Seq_Num_Flagessorial Lev5 | VARCHAR2 | 1 |  | Y |
| 39 | `CUST_INVT_ASS_PROF_CODE_LEV5` | Cust_Invt_Ass_Prof_Codeessorial Lev5 | VARCHAR2 | 4 |  | Y |
| 40 | `CHG_CODE` | Charge Code | VARCHAR2 | 6 |  | Y |
| 41 | `RCPT_INVT_LEV_DES` | Rcpt_Invt_Levessorial Des | VARCHAR2 | 13 |  | Y |
| 42 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 43 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 44 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 45 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 46 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `H_RCPT_H`

- **Tipo:** Historical
- **Categoria:** Receipts
- **Campos:** 69
- **Campos-chave prováveis:** COMP_CODE, RCPT_NUM, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | N |
| 5 | `RCPT_PREX` | Rcptessorial Prex | VARCHAR2 | 4 |  | N |
| 6 | `RCPT_SUFX` | Rcptessorial Sufx | VARCHAR2 | 4 |  | Y |
| 7 | `RCPT_STAT` | Rcptessorial Stat | VARCHAR2 | 1 |  | N |
| 8 | `RCPT_TP` | Rcptessorial Tp | VARCHAR2 | 1 |  | N |
| 9 | `RCPT_PRTY_NUM` | Rcpt_Prtyessorial Num | NUMBER | 22 | 1 | N |
| 10 | `RCPT_INV_DATE` | Rcpt_Invessorial Date | DATE | 7 |  | Y |
| 11 | `RCPT_INV_REG_NUM` | Rcpt_Inv_Regessorial Num | NUMBER | 22 | 9 | Y |
| 12 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 13 | `SHIP_CODE` | Shipper Code | VARCHAR2 | 10 |  | N |
| 14 | `CUST_CODE_BILL_TO` | Cust_Code_Billessorial To | VARCHAR2 | 10 |  | N |
| 15 | `RCPT_DATE` | Rcptessorial Date | DATE | 7 |  | N |
| 16 | `RCPT_PRO_BILL_NUM` | Rcpt_Pro_Billessorial Num | VARCHAR2 | 20 |  | Y |
| 17 | `RCPT_REF_NUM` | Rcpt_Refessorial Num | VARCHAR2 | 20 |  | Y |
| 18 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | N |
| 19 | `LOAD_TP_CODE` | Load Type Code | VARCHAR2 | 4 |  | N |
| 20 | `RCPT_TOT_UNIT` | Rcpt_Totessorial Unit | NUMBER | 22 | 9 | N |
| 21 | `RCPT_REM_FLAG` | Rcpt_Remessorial Flag | VARCHAR2 | 1 |  | N |
| 22 | `RCPT_CARR_FLAG` | Rcpt_Carressorial Flag | VARCHAR2 | 1 |  | N |
| 23 | `RCPT_PALL_FLAG` | Rcpt_Pallessorial Flag | VARCHAR2 | 1 |  | N |
| 24 | `RCPT_BILL_FLAG` | Rcpt_Billessorial Flag | VARCHAR2 | 1 |  | N |
| 25 | `RCPT_EXTRA_CHG_FLAG` | Rcpt_Extra_Chgessorial Flag | VARCHAR2 | 1 |  | N |
| 26 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 27 | `RCPT_ENTRY_DATE` | Rcpt_Entryessorial Date | DATE | 7 |  | N |
| 28 | `RCPT_ALTER_FLAG` | Rcpt_Alteressorial Flag | VARCHAR2 | 1 |  | N |
| 29 | `RCPT_CONF_FLAG` | Rcpt_Confessorial Flag | VARCHAR2 | 1 |  | N |
| 30 | `RCPT_RATE_FLAG` | Rcpt_Rateessorial Flag | VARCHAR2 | 1 |  | N |
| 31 | `RCPT_LOC_GEN_FLAG` | Rcpt_Loc_Genessorial Flag | VARCHAR2 | 1 |  | N |
| 32 | `RCPT_LOC_STAT` | Rcpt_Locessorial Stat | VARCHAR2 | 1 |  | N |
| 33 | `RCPT_DAY_ACT_REP_PROS_FLAG` | Rcpt_Day_Act_Rep_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 34 | `INFO_FLOW_PROF_CODE` | Information Flow Profile Code | VARCHAR2 | 4 |  | N |
| 35 | `INFO_FLOW_SEQ_NUM` | Info_Flow_Seqessorial Num | NUMBER | 22 | 2 | N |
| 36 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | N |
| 37 | `RCPT_TRANS_ORD_NUM` | Rcpt_Trans_Ordessorial Num | NUMBER | 22 | 9 | Y |
| 38 | `RCPT_TRANS_ORD_PREX` | Rcpt_Trans_Ordessorial Prex | VARCHAR2 | 4 |  | Y |
| 39 | `RCPT_TRANS_ORD_SUFX` | Rcpt_Trans_Ordessorial Sufx | VARCHAR2 | 4 |  | Y |
| 40 | `RCPT_EDI_CREATE_FLAG` | Rcpt_Edi_Createessorial Flag | VARCHAR2 | 1 |  | N |
| 41 | `RCPT_CONF_DATE` | Rcpt_Confessorial Date | DATE | 7 |  | Y |
| 42 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 43 | `EDI_INFO_FLAG` | Edi_Infoessorial Flag | VARCHAR2 | 1 |  | N |
| 44 | `RCPT_APPO_DATE` | Rcpt_Appoessorial Date | DATE | 7 |  | Y |
| 45 | `DAY_ACT_REG_NUM` | Day_Act_Regessorial Num | NUMBER | 22 | 6 | Y |
| 46 | `RCPT_EDI_GRP_VAL` | Rcpt_Edi_Grpessorial Val | VARCHAR2 | 30 |  | Y |
| 47 | `RCPT_ALT_REF1` | Rcpt_Altessorial Ref1 | VARCHAR2 | 20 |  | Y |
| 48 | `RCPT_ALT_REF2` | Rcpt_Altessorial Ref2 | VARCHAR2 | 20 |  | Y |
| 49 | `RCPT_OS_NUM` | Rcpt_Osessorial Num | NUMBER | 22 | 6 | Y |
| 50 | `RCPT_OS_FLAG` | Rcpt_Osessorial Flag | VARCHAR2 | 1 |  | Y |
| 51 | `RCPT_SRCE_RCPT_NUM` | Rcpt_Srce_Rcptessorial Num | NUMBER | 22 | 9 | Y |
| 52 | `BAT_NUM` | Batch Number | NUMBER | 22 | 9 | Y |
| 53 | `MHE_TP_CODE` | Mhe_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 54 | `DIST_TP_CODE` | Dist_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 55 | `PO_NUM` | PO Number | NUMBER | 22 | 9 | Y |
| 56 | `FINAL_DEST_CODE` | Final_Destessorial Code | VARCHAR2 | 10 |  | Y |
| 57 | `COMP_CODE_UPDOWNSTREAM` | Comp_Codeessorial Updownstream | VARCHAR2 | 2 |  | Y |
| 58 | `RCPT_NUM_UPDOWNSTREAM` | Rcpt_Numessorial Updownstream | NUMBER | 22 | 9 | Y |
| 59 | `RCPT_EXPT_DATE` | Rcpt_Exptessorial Date | DATE | 7 |  | Y |
| 60 | `LOAD_NUM` | Load Number | NUMBER | 22 | 6 | Y |
| 61 | `RCPT_A1INSPECTION_STAT_MES` | Rcpt_A1Inspection_Statessorial Mes | VARCHAR2 | 100 |  | Y |
| 62 | `BLDG_CODE_UNLOAD` | Bldg_Codeessorial Unload | VARCHAR2 | 4 |  | Y |
| 63 | `DOOR_CODE_UNLOAD` | Door_Codeessorial Unload | VARCHAR2 | 4 |  | Y |
| 64 | `RCPT_PUTAWAY_MODE` | Rcpt_Putawayessorial Mode | VARCHAR2 | 4 |  | Y |
| 65 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 66 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 67 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 68 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 69 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `L_SN_RCPT_D`

- **Tipo:** Custom
- **Categoria:** Receipts
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE, RCPT_NUM, LOC_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | N |
| 3 | `RCPT_LEV1` | Rcptessorial Lev1 | VARCHAR2 | 40 |  | Y |
| 4 | `RCPT_LEV2` | Rcptessorial Lev2 | VARCHAR2 | 40 |  | N |
| 5 | `PO_LINE_NUM` | Po_Lineessorial Num | NUMBER | 22 | 4 | Y |
| 6 | `UNIT_TOTE` | Unitessorial Tote | NUMBER | 22 | 6 | N |
| 7 | `UNIT_PACK` | Unitessorial Pack | NUMBER | 22 | 6 | Y |
| 8 | `RECD_QTY` | Recdessorial Qty | NUMBER | 22 | 9 | N |
| 9 | `PROS_TP_CODE` | Pros_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 10 | `PRE_TICK_CODE` | Pre_Tickessorial Code | VARCHAR2 | 1 |  | N |
| 11 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 12 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | N |

## `L_SN_RCPT_DD1`

- **Tipo:** Custom
- **Categoria:** Receipts
- **Campos:** 8
- **Campos-chave prováveis:** COMP_CODE, RCPT_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | N |
| 3 | `RCPT_LEV1` | Rcptessorial Lev1 | VARCHAR2 | 40 |  | N |
| 4 | `RCPT_LEV2` | Rcptessorial Lev2 | VARCHAR2 | 40 |  | N |
| 5 | `PO_LINE_NUM` | Po_Lineessorial Num | NUMBER | 22 | 4 | Y |
| 6 | `UNIT_PACK` | Unitessorial Pack | NUMBER | 22 | 6 | N |
| 7 | `TOT_PACK_QTY` | Tot_Packessorial Qty | NUMBER | 22 | 9 | N |
| 8 | `PACK_QTY` | Packessorial Qty | NUMBER | 22 | 9 | N |

## `L_SN_RECD`

- **Tipo:** Custom
- **Categoria:** Receipts
- **Campos:** 16
- **Campos-chave prováveis:** COMP_CODE, RCPT_NUM, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4, LOC_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | N |
| 3 | `PO_NUM` | PO Number | NUMBER | 22 | 9 | N |
| 4 | `PO_LINE_NUM` | Po_Lineessorial Num | NUMBER | 22 | 4 | N |
| 5 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 6 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | Y |
| 7 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | Y |
| 8 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | Y |
| 9 | `PO_ORD_QTY` | Po_Ordessorial Qty | NUMBER | 22 | 9 | N |
| 10 | `RECD_QTY` | Recdessorial Qty | NUMBER | 22 | 9 | N |
| 11 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 12 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | Y |
| 13 | `RCPT_PRICE` | Rcptessorial Price | NUMBER | 22 | 12 | Y |
| 14 | `CUR_CODE` | Currency Code | VARCHAR2 | 4 |  | Y |
| 15 | `PROS_FLAG` | Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 16 | `PO_AVAIL_QTY` | Po_Availessorial Qty | NUMBER | 22 | 9 | N |

## `M_CST_BROK`

- **Tipo:** Master
- **Categoria:** Receipts
- **Campos:** 17
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CST_BROK_CODE` | Cst_Brokessorial Code | VARCHAR2 | 10 |  | N |
| 4 | `CST_BROK_NAME` | Cst_Brokessorial Name | VARCHAR2 | 30 |  | N |
| 5 | `CST_BROK_STAT` | Cst_Brokessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `CST_BROK_ADD1` | Cst_Brokessorial Add1 | VARCHAR2 | 30 |  | N |
| 7 | `CST_BROK_ADD2` | Cst_Brokessorial Add2 | VARCHAR2 | 30 |  | Y |
| 8 | `CST_BROK_ADD3` | Cst_Brokessorial Add3 | VARCHAR2 | 30 |  | Y |
| 9 | `CST_BROK_ADD4` | Cst_Brokessorial Add4 | VARCHAR2 | 30 |  | Y |
| 10 | `ZIP_CODE` | Zip Code | VARCHAR2 | 10 |  | N |
| 11 | `COUNTRY_CODE` | Country Code | VARCHAR2 | 4 |  | N |
| 12 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 13 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 14 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 15 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 16 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 17 | `ZIP_ID` | Zip ID | RAW | 32 |  | N |

## `M_RCPT_PRTY`

- **Tipo:** Master
- **Categoria:** Receipts
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `RCPT_PRTY_NUM` | Rcpt_Prtyessorial Num | NUMBER | 22 | 1 | N |
| 4 | `RCPT_PRTY_DES` | Rcpt_Prtyessorial Des | VARCHAR2 | 30 |  | N |
| 5 | `RCPT_PRTY_STAT` | Rcpt_Prtyessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `RCPT_PRTY_AUTO_ALLOC_FLAG` | Rcpt_Prty_Auto_Allocessorial Flag | VARCHAR2 | 1 |  | N |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_SHIP`

- **Tipo:** Master
- **Categoria:** Receipts
- **Campos:** 36
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `SHIP_CODE` | Shipper Code | VARCHAR2 | 10 |  | N |
| 4 | `SHIP_NAME` | Shipessorial Name | VARCHAR2 | 30 |  | N |
| 5 | `SHIP_STAT` | Shipessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `SHIP_ADD1` | Shipessorial Add1 | VARCHAR2 | 30 |  | N |
| 7 | `SHIP_ADD2` | Shipessorial Add2 | VARCHAR2 | 30 |  | Y |
| 8 | `SHIP_ADD3` | Shipessorial Add3 | VARCHAR2 | 30 |  | Y |
| 9 | `ZIP_CODE` | Zip Code | VARCHAR2 | 10 |  | N |
| 10 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | N |
| 11 | `SHIP_LAST_ACT_DATE` | Ship_Last_Actessorial Date | DATE | 7 |  | Y |
| 12 | `LOAD_ANAL_CODE` | Load_Analessorial Code | VARCHAR2 | 4 |  | N |
| 13 | `FRT_DEST_CODE` | Frt_Destessorial Code | VARCHAR2 | 10 |  | Y |
| 14 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 15 | `INFO_FLOW_PROF_CODE` | Information Flow Profile Code | VARCHAR2 | 4 |  | Y |
| 16 | `SHIP_LAB_STD_MODY_NUM` | Ship_Lab_Std_Modyessorial Num | NUMBER | 22 | 4 | Y |
| 17 | `EXTRA_CHG_PROF_CODE` | Extra_Chg_Professorial Code | VARCHAR2 | 4 |  | Y |
| 18 | `SHIP_ADD4` | Shipessorial Add4 | VARCHAR2 | 30 |  | Y |
| 19 | `COUNTRY_CODE` | Country Code | VARCHAR2 | 4 |  | N |
| 20 | `EXT_REF_NUM1` | Ext_Refessorial Num1 | VARCHAR2 | 20 |  | Y |
| 21 | `EDI_PROF_CODE` | Edi_Professorial Code | VARCHAR2 | 4 |  | Y |
| 22 | `SHIP_TP_CODE` | Ship_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 23 | `ITEM_LOC_PROF_CODE` | Item_Loc_Professorial Code | VARCHAR2 | 4 |  | Y |
| 24 | `VEND_CODE` | Vendessorial Code | VARCHAR2 | 10 |  | Y |
| 25 | `SHIP_ESTAB_NUM` | Ship_Estabessorial Num | VARCHAR2 | 20 |  | Y |
| 26 | `SHIP_COUNTRY_ORIGIN` | Ship_Countryessorial Origin | VARCHAR2 | 4 |  | Y |
| 27 | `SHIP_CODE_MAST` | Ship_Codeessorial Mast | VARCHAR2 | 10 |  | Y |
| 28 | `SHIP_CODE_MAST_FLAG` | Ship_Code_Mastessorial Flag | VARCHAR2 | 1 |  | Y |
| 29 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 30 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 31 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 32 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 33 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 34 | `SHIP_DATA_SERVICE_ID` | Ship_Data_Serviceessorial Id | VARCHAR2 | 100 |  | Y |
| 35 | `SHIP_EMP_ID_NUM` | Ship_Emp_Idessorial Num | VARCHAR2 | 20 |  | Y |
| 36 | `ZIP_ID` | Zip ID | RAW | 32 |  | N |

## `M_SHIP_CON_RELATE`

- **Tipo:** Master
- **Categoria:** Receipts
- **Campos:** 7
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `SHIP_CODE` | Shipper Code | VARCHAR2 | 10 |  | N |
| 3 | `CON_CODE` | Consignee Code | VARCHAR2 | 10 |  | N |
| 4 | `RF_INPUT_PROF_CODE` | Rf_Input_Professorial Code | VARCHAR2 | 4 |  | N |
| 5 | `RF_INPUT_PROF_EFF_DATE` | Rf_Input_Prof_Effessorial Date | DATE | 7 |  | N |
| 6 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | Y |
| 7 | `SHIP_CON_RELATE_STAT` | Ship_Con_Relateessorial Stat | VARCHAR2 | 1 |  | N |

## `M_SHIP_CON_RELATE_ENTRY`

- **Tipo:** Master
- **Categoria:** Receipts
- **Campos:** 8
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `SHIP_CODE` | Shipper Code | VARCHAR2 | 10 |  | N |
| 3 | `CON_CODE` | Consignee Code | VARCHAR2 | 10 |  | N |
| 4 | `RF_INPUT_PROF_CODE` | Rf_Input_Professorial Code | VARCHAR2 | 4 |  | N |
| 5 | `RF_INPUT_PROF_EFF_DATE` | Rf_Input_Prof_Effessorial Date | DATE | 7 |  | N |
| 6 | `RF_INPUT_PROF_STEP_NUM` | Rf_Input_Prof_Stepessorial Num | NUMBER | 22 | 2 | N |
| 7 | `CART_ID` | Cart ID | VARCHAR2 | 40 |  | N |
| 8 | `RF_INPUT_PROF_ENTRY_VAL` | Rf_Input_Prof_Entryessorial Val | VARCHAR2 | 40 |  | N |

## `M_SHIP_LANE`

- **Tipo:** Master
- **Categoria:** Receipts
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE, LOC_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `SHIP_LANE_CODE` | Ship_Laneessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `SHIP_LANE_DES` | Ship_Laneessorial Des | VARCHAR2 | 30 |  | N |
| 5 | `SHIP_LANE_STAT` | Ship_Laneessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 7 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | N |
| 8 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 9 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 11 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_SHIP_LANE_ASS`

- **Tipo:** Master
- **Categoria:** Receipts
- **Campos:** 9
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `SHIP_LANE_CODE` | Ship_Laneessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `CON_CODE` | Consignee Code | VARCHAR2 | 10 |  | N |
| 5 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 6 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 7 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 8 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `TE_RCPT_D1`

- **Tipo:** Misc
- **Categoria:** Receipts
- **Campos:** 8
- **Campos-chave prováveis:** COMP_CODE, RCPT_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 6 | N |
| 3 | `RCPT_LINE_NUM` | Receipt Line Number | NUMBER | 22 | 4 | N |
| 4 | `CUST_CODE_CHG` | Cust_Codeessorial Chg | VARCHAR2 | 10 |  | Y |
| 5 | `CHG_CODE` | Charge Code | VARCHAR2 | 6 |  | Y |
| 6 | `CHG_DATE` | Charge Date | DATE | 7 |  | Y |
| 7 | `RCPT_REM_LINE_NUM` | Rcpt_Rem_Lineessorial Num | NUMBER | 22 | 3 | N |
| 8 | `RCPT_REM_LINE_TEXT` | Rcpt_Rem_Lineessorial Text | VARCHAR2 | 45 |  | Y |

## `TE_RCPT_D5`

- **Tipo:** Misc
- **Categoria:** Receipts
- **Campos:** 54
- **Campos-chave prováveis:** COMP_CODE, RCPT_NUM, SKU_CODE, LOC_CODE, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 6 | N |
| 3 | `RCPT_LINE_NUM` | Receipt Line Number | NUMBER | 22 | 4 | N |
| 4 | `RCPT_LINE_STAT` | Rcpt_Lineessorial Stat | VARCHAR2 | 1 |  | N |
| 5 | `RCPT_LINE_MVT_CNT` | Rcpt_Line_Mvtessorial Cnt | NUMBER | 22 | 6 | N |
| 6 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | Y |
| 7 | `RCPT_LEV1` | Rcptessorial Lev1 | VARCHAR2 | 20 |  | N |
| 8 | `RCPT_LEV1_DES` | Rcpt_Lev1essorial Des | VARCHAR2 | 40 |  | Y |
| 9 | `RCPT_SEQ_QTY_LEV1` | Rcpt_Seq_Qtyessorial Lev1 | NUMBER | 22 | 4 | Y |
| 10 | `RCPT_LEV2` | Rcptessorial Lev2 | VARCHAR2 | 20 |  | Y |
| 11 | `RCPT_LEV2_DES` | Rcpt_Lev2essorial Des | VARCHAR2 | 40 |  | Y |
| 12 | `RCPT_SEQ_QTY_LEV2` | Rcpt_Seq_Qtyessorial Lev2 | NUMBER | 22 | 4 | Y |
| 13 | `RCPT_LEV3` | Rcptessorial Lev3 | VARCHAR2 | 20 |  | Y |
| 14 | `RCPT_LEV3_DES` | Rcpt_Lev3essorial Des | VARCHAR2 | 40 |  | Y |
| 15 | `RCPT_SEQ_QTY_LEV3` | Rcpt_Seq_Qtyessorial Lev3 | NUMBER | 22 | 4 | Y |
| 16 | `SKU_CODE` | SKU Code | VARCHAR2 | 4 |  | N |
| 17 | `SKU_CODE_ORG` | Sku_Codeessorial Org | VARCHAR2 | 4 |  | Y |
| 18 | `RCPT_EXPT_QTY` | Rcpt_Exptessorial Qty | NUMBER | 22 | 9 | N |
| 19 | `RCPT_RECD_QTY` | Rcpt_Recdessorial Qty | NUMBER | 22 | 9 | N |
| 20 | `RCPT_RECD_QTY_ORG` | Rcpt_Recd_Qtyessorial Org | NUMBER | 22 | 9 | Y |
| 21 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | N |
| 22 | `WGT_MEAS_CODE_ORG` | Wgt_Meas_Codeessorial Org | VARCHAR2 | 4 |  | Y |
| 23 | `RCPT_UNIT_WGT` | Rcpt_Unitessorial Wgt | NUMBER | 22 | 9 | Y |
| 24 | `RCPT_UNIT_WGT_ORG` | Rcpt_Unit_Wgtessorial Org | NUMBER | 22 | 9 | Y |
| 25 | `RCPT_TOT_WGT` | Rcpt_Totessorial Wgt | NUMBER | 22 | 11 | Y |
| 26 | `RCPT_TOT_WGT_ORG` | Rcpt_Tot_Wgtessorial Org | NUMBER | 22 | 11 | Y |
| 27 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 28 | `WHSE_CODE_ORG` | Whse_Codeessorial Org | VARCHAR2 | 4 |  | Y |
| 29 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | Y |
| 30 | `LOC_CODE_ORG` | Loc_Codeessorial Org | VARCHAR2 | 12 |  | Y |
| 31 | `LOC_DESIG_CODE` | Loc_Desigessorial Code | VARCHAR2 | 4 |  | Y |
| 32 | `RCPT_HOLD_QTY` | Rcpt_Holdessorial Qty | NUMBER | 22 | 9 | Y |
| 33 | `RCPT_HOLD_QTY_ORG` | Rcpt_Hold_Qtyessorial Org | NUMBER | 22 | 9 | Y |
| 34 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |
| 35 | `HOLD_CODE_ORG` | Hold_Codeessorial Org | VARCHAR2 | 4 |  | Y |
| 36 | `HOLD_SHIP_FLAG` | Hold_Shipessorial Flag | VARCHAR2 | 1 |  | Y |
| 37 | `HOLD_SHIP_FLAG_ORG` | Hold_Ship_Flagessorial Org | VARCHAR2 | 1 |  | Y |
| 38 | `RCPT_EXPY_DATE` | Rcpt_Expyessorial Date | DATE | 7 |  | Y |
| 39 | `RCPT_CRS_DOCK_FLAG` | Rcpt_Crs_Dockessorial Flag | VARCHAR2 | 1 |  | N |
| 40 | `RCPT_LINE_ALTER_FLAG` | Rcpt_Line_Alteressorial Flag | VARCHAR2 | 1 |  | N |
| 41 | `RCPT_LINE_CONF_FLAG` | Rcpt_Line_Confessorial Flag | VARCHAR2 | 1 |  | N |
| 42 | `RCPT_LINE_RATE_FLAG` | Rcpt_Line_Rateessorial Flag | VARCHAR2 | 1 |  | N |
| 43 | `LINEAR_MEAS_CODE` | Linear Measurement Code | VARCHAR2 | 4 |  | N |
| 44 | `LINEAR_MEAS_CODE_ORG` | Linear_Meas_Codeessorial Org | VARCHAR2 | 4 |  | Y |
| 45 | `RCPT_TOT_CUBE` | Rcpt_Totessorial Cube | NUMBER | 22 | 12 | Y |
| 46 | `RCPT_TOT_CUBE_ORG` | Rcpt_Tot_Cubeessorial Org | NUMBER | 22 | 12 | Y |
| 47 | `RCPT_LINE_REM_FLAG` | Rcpt_Line_Remessorial Flag | VARCHAR2 | 1 |  | N |
| 48 | `RCPT_LINE_EXTRA_CHG_FLAG` | Rcpt_Line_Extra_Chgessorial Flag | VARCHAR2 | 1 |  | N |
| 49 | `RCPT_LINE_LOC_BAL_FLAG` | Rcpt_Line_Loc_Balessorial Flag | VARCHAR2 | 1 |  | N |
| 50 | `RCPT_LINE_LOC_ENT_FLAG` | Rcpt_Line_Loc_Entessorial Flag | VARCHAR2 | 1 |  | N |
| 51 | `RCPT_LINE_LOC_GEN_FLAG` | Rcpt_Line_Loc_Genessorial Flag | VARCHAR2 | 1 |  | N |
| 52 | `RCPT_LOC_SGL_MULT_FLAG` | Rcpt_Loc_Sgl_Multessorial Flag | VARCHAR2 | 1 |  | N |
| 53 | `RCPT_LOC_SGL_MULT_FLAG_ORG` | Rcpt_Loc_Sgl_Mult_Flagessorial Org | VARCHAR2 | 1 |  | Y |
| 54 | `RCPT_LINE_TP` | Rcpt_Lineessorial Tp | VARCHAR2 | 1 |  | N |

## `TE_RCPT_D5D`

- **Tipo:** Misc
- **Categoria:** Receipts
- **Campos:** 17
- **Campos-chave prováveis:** COMP_CODE, RCPT_NUM, LOC_CODE, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 6 | N |
| 3 | `RCPT_LINE_NUM` | Receipt Line Number | NUMBER | 22 | 4 | N |
| 4 | `RCPT_LOC_LINE_NUM` | Rcpt_Loc_Lineessorial Num | NUMBER | 22 | 4 | N |
| 5 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 6 | `WHSE_CODE_ORG` | Whse_Codeessorial Org | VARCHAR2 | 4 |  | Y |
| 7 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | Y |
| 8 | `LOC_CODE_ORG` | Loc_Codeessorial Org | VARCHAR2 | 12 |  | Y |
| 9 | `LOC_DESIG_CODE` | Loc_Desigessorial Code | VARCHAR2 | 4 |  | Y |
| 10 | `RCPT_LOC_QTY` | Rcpt_Locessorial Qty | NUMBER | 22 | 9 | N |
| 11 | `RCPT_LOC_QTY_ORG` | Rcpt_Loc_Qtyessorial Org | NUMBER | 22 | 9 | Y |
| 12 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |
| 13 | `HOLD_CODE_ORG` | Hold_Codeessorial Org | VARCHAR2 | 4 |  | Y |
| 14 | `HOLD_SHIP_FLAG` | Hold_Shipessorial Flag | VARCHAR2 | 1 |  | Y |
| 15 | `HOLD_SHIP_FLAG_ORG` | Hold_Ship_Flagessorial Org | VARCHAR2 | 1 |  | Y |
| 16 | `RCPT_LOC_HOLD_QTY` | Rcpt_Loc_Holdessorial Qty | NUMBER | 22 | 9 | Y |
| 17 | `RCPT_LOC_HOLD_QTY_ORG` | Rcpt_Loc_Hold_Qtyessorial Org | NUMBER | 22 | 9 | Y |

## `TE_RCPT_D6`

- **Tipo:** Misc
- **Categoria:** Receipts
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE, RCPT_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 6 | N |
| 3 | `INFO_FLOW_SEQ_NUM` | Info_Flow_Seqessorial Num | NUMBER | 22 | 2 | N |
| 4 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | N |
| 5 | `INFO_FLOW_MAND_FLAG` | Info_Flow_Mandessorial Flag | VARCHAR2 | 1 |  | N |
| 6 | `INFO_FLOW_DOC_SEQ_NUM` | Info_Flow_Doc_Seqessorial Num | NUMBER | 22 | 2 | N |
| 7 | `DOC_CODE` | Document Code | VARCHAR2 | 4 |  | Y |
| 8 | `FORM_CODE` | Form Code | VARCHAR2 | 4 |  | Y |
| 9 | `DOC_PRT_TP_FLAG` | Doc_Prt_Tpessorial Flag | VARCHAR2 | 1 |  | Y |
| 10 | `RCPT_DOC_PRT_STAT` | Rcpt_Doc_Prtessorial Stat | VARCHAR2 | 1 |  | Y |
| 11 | `RCPT_DOC_REPRT_CNT` | Rcpt_Doc_Reprtessorial Cnt | NUMBER | 22 | 4 | Y |

## `TE_RCPT_D7`

- **Tipo:** Misc
- **Categoria:** Receipts
- **Campos:** 27
- **Campos-chave prováveis:** COMP_CODE, RCPT_NUM, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 6 | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `CUST_INVT_PROF_CODE` | Cust_Invt_Professorial Code | VARCHAR2 | 4 |  | N |
| 5 | `RCPT_ITEM_LEV` | Rcpt_Itemessorial Lev | VARCHAR2 | 9 |  | N |
| 6 | `RCPT_ITEM_LEV_DES` | Rcpt_Item_Levessorial Des | VARCHAR2 | 13 |  | N |
| 7 | `RCPT_CHG_LEV_NUM` | Rcpt_Chg_Levessorial Num | NUMBER | 22 | 1 | N |
| 8 | `CHG_CODE` | Charge Code | VARCHAR2 | 6 |  | Y |
| 9 | `RCPT_INVT_LEV_DES` | Rcpt_Invt_Levessorial Des | VARCHAR2 | 13 |  | Y |
| 10 | `RCPT_INVT_TERMGY_CODE_LEV1` | Rcpt_Invt_Termgy_Codeessorial Lev1 | VARCHAR2 | 4 |  | N |
| 11 | `RCPT_LEV_NUM_LEV1` | Rcpt_Lev_Numessorial Lev1 | NUMBER | 22 | 1 | N |
| 12 | `RCPT_INVT_LEV1` | Rcpt_Invtessorial Lev1 | VARCHAR2 | 9 |  | N |
| 13 | `RCPT_ASS_FLAG_LEV1` | Rcpt_Ass_Flagessorial Lev1 | VARCHAR2 | 1 |  | N |
| 14 | `CUST_INVT_ASS_PROF_CODE_LEV1` | Cust_Invt_Ass_Prof_Codeessorial Lev1 | VARCHAR2 | 4 |  | Y |
| 15 | `RCPT_SEQ_NUM_FLAG_LEV1` | Rcpt_Seq_Num_Flagessorial Lev1 | VARCHAR2 | 1 |  | N |
| 16 | `RCPT_INVT_TERMGY_CODE_LEV2` | Rcpt_Invt_Termgy_Codeessorial Lev2 | VARCHAR2 | 4 |  | Y |
| 17 | `RCPT_LEV_NUM_LEV2` | Rcpt_Lev_Numessorial Lev2 | NUMBER | 22 | 1 | Y |
| 18 | `RCPT_INVT_LEV2` | Rcpt_Invtessorial Lev2 | VARCHAR2 | 9 |  | Y |
| 19 | `RCPT_ASS_FLAG_LEV2` | Rcpt_Ass_Flagessorial Lev2 | VARCHAR2 | 1 |  | Y |
| 20 | `CUST_INVT_ASS_PROF_CODE_LEV2` | Cust_Invt_Ass_Prof_Codeessorial Lev2 | VARCHAR2 | 4 |  | Y |
| 21 | `RCPT_SEQ_NUM_FLAG_LEV2` | Rcpt_Seq_Num_Flagessorial Lev2 | VARCHAR2 | 1 |  | Y |
| 22 | `RCPT_INVT_TERMGY_CODE_LEV3` | Rcpt_Invt_Termgy_Codeessorial Lev3 | VARCHAR2 | 4 |  | Y |
| 23 | `RCPT_LEV_NUM_LEV3` | Rcpt_Lev_Numessorial Lev3 | NUMBER | 22 | 1 | Y |
| 24 | `RCPT_INVT_LEV3` | Rcpt_Invtessorial Lev3 | VARCHAR2 | 9 |  | Y |
| 25 | `RCPT_ASS_FLAG_LEV3` | Rcpt_Ass_Flagessorial Lev3 | VARCHAR2 | 1 |  | Y |
| 26 | `CUST_INVT_ASS_PROF_CODE_LEV3` | Cust_Invt_Ass_Prof_Codeessorial Lev3 | VARCHAR2 | 4 |  | Y |
| 27 | `RCPT_SEQ_NUM_FLAG_LEV3` | Rcpt_Seq_Num_Flagessorial Lev3 | VARCHAR2 | 1 |  | Y |

## `TE_RCPT_H`

- **Tipo:** Misc
- **Categoria:** Receipts
- **Campos:** 46
- **Campos-chave prováveis:** COMP_CODE, RCPT_NUM, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 6 | N |
| 3 | `RCPT_PREX` | Rcptessorial Prex | VARCHAR2 | 4 |  | N |
| 4 | `RCPT_SUFX` | Rcptessorial Sufx | VARCHAR2 | 4 |  | Y |
| 5 | `RCPT_STAT` | Rcptessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `RCPT_TP` | Rcptessorial Tp | VARCHAR2 | 1 |  | N |
| 7 | `RCPT_PRTY_NUM` | Rcpt_Prtyessorial Num | NUMBER | 22 | 1 | N |
| 8 | `RCPT_INV_DATE` | Rcpt_Invessorial Date | DATE | 7 |  | Y |
| 9 | `RCPT_INV_REG_NUM` | Rcpt_Inv_Regessorial Num | NUMBER | 22 | 6 | Y |
| 10 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 11 | `SHIP_CODE` | Shipper Code | VARCHAR2 | 10 |  | N |
| 12 | `CUST_CODE_BILL_TO` | Cust_Code_Billessorial To | VARCHAR2 | 10 |  | N |
| 13 | `RCPT_DATE` | Rcptessorial Date | DATE | 7 |  | N |
| 14 | `RCPT_PRO_BILL_NUM` | Rcpt_Pro_Billessorial Num | VARCHAR2 | 20 |  | Y |
| 15 | `RCPT_REF_NUM` | Rcpt_Refessorial Num | VARCHAR2 | 20 |  | Y |
| 16 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | N |
| 17 | `LOAD_TP_CODE` | Load Type Code | VARCHAR2 | 4 |  | N |
| 18 | `RCPT_TOT_UNIT` | Rcpt_Totessorial Unit | NUMBER | 22 | 9 | N |
| 19 | `RCPT_REM_FLAG` | Rcpt_Remessorial Flag | VARCHAR2 | 1 |  | N |
| 20 | `RCPT_CARR_FLAG` | Rcpt_Carressorial Flag | VARCHAR2 | 1 |  | N |
| 21 | `RCPT_PALL_FLAG` | Rcpt_Pallessorial Flag | VARCHAR2 | 1 |  | N |
| 22 | `RCPT_BILL_FLAG` | Rcpt_Billessorial Flag | VARCHAR2 | 1 |  | N |
| 23 | `RCPT_EXTRA_CHG_FLAG` | Rcpt_Extra_Chgessorial Flag | VARCHAR2 | 1 |  | N |
| 24 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 25 | `RCPT_ENTRY_DATE` | Rcpt_Entryessorial Date | DATE | 7 |  | N |
| 26 | `RCPT_ALTER_FLAG` | Rcpt_Alteressorial Flag | VARCHAR2 | 1 |  | N |
| 27 | `RCPT_CONF_FLAG` | Rcpt_Confessorial Flag | VARCHAR2 | 1 |  | N |
| 28 | `RCPT_RATE_FLAG` | Rcpt_Rateessorial Flag | VARCHAR2 | 1 |  | N |
| 29 | `RCPT_LOC_GEN_FLAG` | Rcpt_Loc_Genessorial Flag | VARCHAR2 | 1 |  | N |
| 30 | `RCPT_LOC_STAT` | Rcpt_Locessorial Stat | VARCHAR2 | 1 |  | N |
| 31 | `RCPT_DAY_ACT_REP_PROS_FLAG` | Rcpt_Day_Act_Rep_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 32 | `INFO_FLOW_PROF_CODE` | Information Flow Profile Code | VARCHAR2 | 4 |  | N |
| 33 | `INFO_FLOW_SEQ_NUM` | Info_Flow_Seqessorial Num | NUMBER | 22 | 2 | N |
| 34 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | N |
| 35 | `SHIP_NAME_MAN` | Ship_Nameessorial Man | VARCHAR2 | 30 |  | Y |
| 36 | `SHIP_ADD1_MAN` | Ship_Add1essorial Man | VARCHAR2 | 30 |  | Y |
| 37 | `SHIP_ADD2_MAN` | Ship_Add2essorial Man | VARCHAR2 | 30 |  | Y |
| 38 | `SHIP_ADD3_MAN` | Ship_Add3essorial Man | VARCHAR2 | 30 |  | Y |
| 39 | `ZIP_CITY_SHIP_MAN` | Zarehouse City Ship Man | VARCHAR2 | 30 |  | Y |
| 40 | `STATE_CODE_SHIP_MAN` | State_Code_Shipessorial Man | VARCHAR2 | 4 |  | Y |
| 41 | `ZIP_CODE_SHIP_MAN` | Zarehouse Code Ship Man | VARCHAR2 | 10 |  | Y |
| 42 | `CARR_NAME_MAN` | Carr_Nameessorial Man | VARCHAR2 | 30 |  | Y |
| 43 | `RCPT_TRANS_ORD_NUM` | Rcpt_Trans_Ordessorial Num | NUMBER | 22 | 6 | Y |
| 44 | `RCPT_TRANS_ORD_PREX` | Rcpt_Trans_Ordessorial Prex | VARCHAR2 | 4 |  | Y |
| 45 | `RCPT_TRANS_ORD_SUFX` | Rcpt_Trans_Ordessorial Sufx | VARCHAR2 | 4 |  | Y |
| 46 | `RCPT_EDI_CREATE_FLAG` | Rcpt_Edi_Createessorial Flag | VARCHAR2 | 1 |  | N |

