# Tabelas — Orders

> Categoria extraída da planilha `Tables-Database.xlsx`. Total de tabelas: **184**.

## `C_CREATE_ORD_D`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 12
- **Campos-chave prováveis:** INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4, CUST_CODE, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ORD_SEQ_NUM` | Ord_Seqessorial Num | NUMBER | 22 | 6 | Y |
| 2 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | Y |
| 3 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | Y |
| 4 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | Y |
| 5 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | Y |
| 6 | `INVT_LEV5` | Inventory Level 5 | VARCHAR2 | 40 |  | Y |
| 7 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 8 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | Y |
| 9 | `ORD_ORD_QTY` | Ord_Ordessorial Qty | NUMBER | 22 | 9 | Y |
| 10 | `ORD_SHIP_QTY` | Ord_Shipessorial Qty | NUMBER | 22 | 9 | Y |
| 11 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |
| 12 | `ORD_LINE_TP` | Order Line Type | VARCHAR2 | 1 |  | Y |

## `C_CREATE_ORD_H`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 23
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ORD_SEQ_NUM` | Ord_Seqessorial Num | NUMBER | 22 | 6 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | Y |
| 3 | `ORD_TP` | Ordessorial Tp | VARCHAR2 | 1 |  | Y |
| 4 | `ORD_PRTY_NUM` | Ord_Prtyessorial Num | NUMBER | 22 | 1 | Y |
| 5 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | Y |
| 6 | `CON_CODE` | Consignee Code | VARCHAR2 | 10 |  | Y |
| 7 | `CON_NAME` | Consignee Name | VARCHAR2 | 30 |  | Y |
| 8 | `SOLDTO_CODE` | Soldtoessorial Code | VARCHAR2 | 10 |  | Y |
| 9 | `SOLDTO_NAME` | Soldtoessorial Name | VARCHAR2 | 30 |  | Y |
| 10 | `ORD_DATE` | Ordessorial Date | DATE | 7 |  | Y |
| 11 | `ORD_TO_SHIP_DATE` | Ord_To_Shipessorial Date | DATE | 7 |  | Y |
| 12 | `ORD_TO_ARR_DATE` | Ord_To_Arressorial Date | DATE | 7 |  | Y |
| 13 | `ORD_CUST_ORD_NUM` | Ord_Cust_Ordessorial Num | VARCHAR2 | 20 |  | Y |
| 14 | `ORD_PO_NUM` | Ord_Poessorial Num | VARCHAR2 | 20 |  | Y |
| 15 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | Y |
| 16 | `CARR_NAME` | Carrier Name | VARCHAR2 | 30 |  | Y |
| 17 | `LOAD_TP_CODE` | Load Type Code | VARCHAR2 | 4 |  | Y |
| 18 | `FRT_TERM_CODE` | Frt_Termessorial Code | VARCHAR2 | 4 |  | Y |
| 19 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | Y |
| 20 | `ORD_ALT_REF1` | Ord_Altessorial Ref1 | VARCHAR2 | 20 |  | Y |
| 21 | `ORD_ALT_REF2` | Ord_Altessorial Ref2 | VARCHAR2 | 20 |  | Y |
| 22 | `LOAD_NUM` | Load Number | NUMBER | 22 | 6 | Y |
| 23 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | Y |

## `C_CREATE_ORD_TRIG`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 2

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ORD_SEQ_NUM` | Ord_Seqessorial Num | NUMBER | 22 | 6 | N |
| 2 | `COMP_ID` | Compessorial Id | VARCHAR2 | 10 |  | Y |

## `C_INTFACE_SHIPMENT_MES`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 106
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM, SKU_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `INTFACE_SEQ_NUM` | Intface_Seqessorial Num | NUMBER | 22 | 9 | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `SHIPMENT_NUM` | Shipmentessorial Num | NUMBER | 22 | 9 | N |
| 5 | `SHIPMENT_SRCE_FLAG` | Shipment_Srceessorial Flag | VARCHAR2 | 1 |  | N |
| 6 | `ACTION_FLAG` | Actionessorial Flag | VARCHAR2 | 1 |  | N |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | N |
| 8 | `PROS_FLAG` | Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 9 | `PROS_DATE` | Prosessorial Date | DATE | 7 |  | Y |
| 10 | `CART_ID` | Cart ID | VARCHAR2 | 40 |  | N |
| 11 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 12 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |
| 13 | `ORD_LOC_LINE_NUM` | Ord_Loc_Lineessorial Num | NUMBER | 22 | 4 | N |
| 14 | `ORD_CUST_ORD_NUM` | Ord_Cust_Ordessorial Num | VARCHAR2 | 20 |  | Y |
| 15 | `ORD_PO_NUM` | Ord_Poessorial Num | VARCHAR2 | 20 |  | Y |
| 16 | `CUST_NAME` | Customer Name | VARCHAR2 | 30 |  | N |
| 17 | `CUST_ADD1` | Custessorial Add1 | VARCHAR2 | 60 |  | N |
| 18 | `CUST_ADD2` | Custessorial Add2 | VARCHAR2 | 60 |  | Y |
| 19 | `CUST_CITY` | Custessorial City | VARCHAR2 | 30 |  | Y |
| 20 | `CUST_STATE` | Custessorial State | VARCHAR2 | 4 |  | Y |
| 21 | `CUST_ZIP` | Custessorial Zip | VARCHAR2 | 10 |  | N |
| 22 | `CUST_COUNTRY_CODE` | Cust_Countryessorial Code | VARCHAR2 | 4 |  | N |
| 23 | `CUST_TEL_NUM` | Cust_Telessorial Num | VARCHAR2 | 20 |  | Y |
| 24 | `CUST_TEL_CONTACT` | Cust_Telessorial Contact | VARCHAR2 | 30 |  | Y |
| 25 | `CON_NAME` | Consignee Name | VARCHAR2 | 30 |  | N |
| 26 | `CON_ADD1` | Conessorial Add1 | VARCHAR2 | 60 |  | N |
| 27 | `CON_ADD2` | Conessorial Add2 | VARCHAR2 | 60 |  | Y |
| 28 | `CON_CITY` | Conessorial City | VARCHAR2 | 30 |  | Y |
| 29 | `CON_STATE` | Conessorial State | VARCHAR2 | 4 |  | Y |
| 30 | `CON_ZIP` | Conessorial Zip | VARCHAR2 | 10 |  | N |
| 31 | `CON_COUNTRY_CODE` | Con_Countryessorial Code | VARCHAR2 | 4 |  | N |
| 32 | `CON_TEL_NUM` | Con_Telessorial Num | VARCHAR2 | 20 |  | Y |
| 33 | `CON_TEL_CONTACT` | Con_Telessorial Contact | VARCHAR2 | 30 |  | Y |
| 34 | `ORD_CART_QTY` | Ord_Cartessorial Qty | NUMBER | 22 | 9 | N |
| 35 | `SKU_CODE` | SKU Code | VARCHAR2 | 4 |  | N |
| 36 | `ORD_CART_WGT` | Ord_Cartessorial Wgt | NUMBER | 22 | 16 | N |
| 37 | `ORD_CART_WGT_NET` | Ord_Cart_Wgtessorial Net | NUMBER | 22 | 16 | N |
| 38 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | N |
| 39 | `ORD_CART_CUBE` | Ord_Cartessorial Cube | NUMBER | 22 | 12 | N |
| 40 | `LINEAR_MEAS_CODE` | Linear Measurement Code | VARCHAR2 | 4 |  | N |
| 41 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | N |
| 42 | `CARR_NAME` | Carrier Name | VARCHAR2 | 30 |  | N |
| 43 | `ACC_NUM` | Accessorial Num | VARCHAR2 | 20 |  | Y |
| 44 | `FRT_TERM_CODE` | Frt_Termessorial Code | VARCHAR2 | 4 |  | Y |
| 45 | `WAY_BILL_NUM` | Way_Billessorial Num | VARCHAR2 | 250 |  | Y |
| 46 | `LABEL_EXT_FILE_SEQ_NUM` | Label_Ext_File_Seqessorial Num | NUMBER | 22 | 9 | Y |
| 47 | `RATE` | Rateessorial Rate | NUMBER | 22 | 9 | Y |
| 48 | `ERR_TEXT` | Error Text | VARCHAR2 | 250 |  | Y |
| 49 | `ERR_NUM` | Erressorial Num | NUMBER | 22 | 9 | Y |
| 50 | `ORD_CART_LEN` | Ord_Cartessorial Len | NUMBER | 22 | 7 | Y |
| 51 | `ORD_CART_WID` | Ord_Cartessorial Wid | NUMBER | 22 | 7 | Y |
| 52 | `ORD_CART_HGT` | Ord_Cartessorial Hgt | NUMBER | 22 | 7 | Y |
| 53 | `PARCEL_CARR_ACC_NUM` | Parcel_Carr_Accessorial Num | VARCHAR2 | 20 |  | Y |
| 54 | `BILL_THIRD_PARTY_NAME` | Bill_Third_Partyessorial Name | VARCHAR2 | 30 |  | Y |
| 55 | `BILL_THIRD_PARTY_ADD1` | Bill_Third_Partyessorial Add1 | VARCHAR2 | 30 |  | Y |
| 56 | `BILL_THIRD_PARTY_ADD2` | Bill_Third_Partyessorial Add2 | VARCHAR2 | 30 |  | Y |
| 57 | `BILL_THIRD_PARTY_CITY` | Bill_Third_Partyessorial City | VARCHAR2 | 30 |  | Y |
| 58 | `BILL_THIRD_PARTY_STATE` | Bill_Third_Partyessorial State | VARCHAR2 | 4 |  | Y |
| 59 | `BILL_THIRD_PARTY_ZIP` | Bill_Third_Partyessorial Zip | VARCHAR2 | 10 |  | Y |
| 60 | `BILL_THIRD_PARTY_COUNTRY_CODE` | Bill_Third_Party_Countryessorial Code | VARCHAR2 | 4 |  | Y |
| 61 | `CON_CODE` | Consignee Code | VARCHAR2 | 10 |  | Y |
| 62 | `ORD_TO_SHIP_DATE` | Ord_To_Shipessorial Date | DATE | 7 |  | Y |
| 63 | `RQST_TO_CANCEL_DATE` | Rqst_To_Cancelessorial Date | DATE | 7 |  | Y |
| 64 | `CARR_A1SHIP_REF_NUM` | Carr_A1Ship_Refessorial Num | VARCHAR2 | 250 |  | Y |
| 65 | `ORD_BILLTO_EMAIL_ADD` | Ord_Billto_Emailessorial Add | VARCHAR2 | 250 |  | Y |
| 66 | `ORD_CON_EMAIL_ADD` | Ord_Con_Emailessorial Add | VARCHAR2 | 250 |  | Y |
| 67 | `ORD_PARCEL_RESIDENTIAL_FLAG` | Ord_Parcel_Residentialessorial Flag | VARCHAR2 | 1 |  | Y |
| 68 | `ORD_PARCEL_SIGNATURE_REQ_TP` | Ord_Parcel_Signature_Reqessorial Tp | VARCHAR2 | 1 |  | Y |
| 69 | `ORD_PARCEL_DELV_CONF` | Ord_Parcel_Delvessorial Conf | VARCHAR2 | 1 |  | Y |
| 70 | `ORD_PARCEL_SATURDAY` | Ord_Parcelessorial Saturday | VARCHAR2 | 1 |  | Y |
| 71 | `ORD_PARCEL_INS_FLAG` | Ord_Parcel_Insessorial Flag | VARCHAR2 | 1 |  | Y |
| 72 | `ORD_PARCEL_INS_CHG_AMT` | Ord_Parcel_Ins_Chgessorial Amt | NUMBER | 22 | 15 | Y |
| 73 | `ORD_PARCEL_INS_DECLARE_AMT` | Ord_Parcel_Ins_Declareessorial Amt | NUMBER | 22 | 15 | Y |
| 74 | `ORD_PARCEL_MES` | Ord_Parcelessorial Mes | VARCHAR2 | 250 |  | Y |
| 75 | `ORD_PARCEL_SHIP_REF1` | Ord_Parcel_Shipessorial Ref1 | VARCHAR2 | 40 |  | Y |
| 76 | `ORD_PARCEL_SHIP_REF2` | Ord_Parcel_Shipessorial Ref2 | VARCHAR2 | 40 |  | Y |
| 77 | `ORD_PARCEL_SHIP_REF3` | Ord_Parcel_Shipessorial Ref3 | VARCHAR2 | 40 |  | Y |
| 78 | `ORD_PARCEL_SHIP_REF4` | Ord_Parcel_Shipessorial Ref4 | VARCHAR2 | 40 |  | Y |
| 79 | `ORD_PARCEL_SHIP_REF5` | Ord_Parcel_Shipessorial Ref5 | VARCHAR2 | 40 |  | Y |
| 80 | `ORD_PARCEL_COD_METH_PAY` | Ord_Parcel_Cod_Methessorial Pay | VARCHAR2 | 40 |  | Y |
| 81 | `ORD_PARCEL_INSIDE_DELV_FLAG` | Ord_Parcel_Inside_Delvessorial Flag | VARCHAR2 | 1 |  | Y |
| 82 | `ORD_PARCEL_HOLD_LOC_FLAG` | Ord_Parcel_Hold_Locessorial Flag | VARCHAR2 | 1 |  | Y |
| 83 | `CART_OVERSIZE_FLAG` | Cart_Oversizeessorial Flag | VARCHAR2 | 1 |  | Y |
| 84 | `ORD_INTERNTNAL_FLAG` | Ord_Interntnalessorial Flag | VARCHAR2 | 1 |  | Y |
| 85 | `CLASS_DES` | Class Description | VARCHAR2 | 30 |  | Y |
| 86 | `ORD_REASON_FOR_EXPORT` | Ord_Reason_Foressorial Export | VARCHAR2 | 30 |  | Y |
| 87 | `ORD_TERM_OF_SALE` | Ord_Term_Ofessorial Sale | VARCHAR2 | 30 |  | Y |
| 88 | `CUST_EMP_ID_NUM` | Cust_Emp_Idessorial Num | VARCHAR2 | 20 |  | Y |
| 89 | `CON_EMP_ID_NUM` | Con_Emp_Idessorial Num | VARCHAR2 | 20 |  | Y |
| 90 | `ORD_INPROGRESS_FLAG` | Ord_Inprogressessorial Flag | VARCHAR2 | 1 |  | Y |
| 91 | `ORD_PARCEL_CALL_TAG_FLAG` | Ord_Parcel_Call_Tagessorial Flag | VARCHAR2 | 1 |  | Y |
| 92 | `ORD_COD_AMT` | Ord_Codessorial Amt | NUMBER | 22 | 9 | Y |
| 93 | `A1SHIP_SHIP_ID` | A1Ship Shipment ID | VARCHAR2 | 100 |  | Y |
| 94 | `PRT_CODE` | Printer Code | VARCHAR2 | 4 |  | Y |
| 95 | `DOC_CODE` | Document Code | VARCHAR2 | 4 |  | Y |
| 96 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | Y |
| 97 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | Y |
| 98 | `FLAT_BOX_TP_DES` | Flat_Box_Tpessorial Des | VARCHAR2 | 250 |  | Y |
| 99 | `SHIPMENT_LABEL_TP` | Shipment_Labelessorial Tp | VARCHAR2 | 4 |  | Y |
| 100 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 101 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 102 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 103 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 104 | `PMT_TP_CODE` | Pmt_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 105 | `CON_ADD3` | Conessorial Add3 | VARCHAR2 | 30 |  | Y |
| 106 | `CON_ADD4` | Conessorial Add4 | VARCHAR2 | 30 |  | Y |

## `C_INTFACE_SHIPMENT_MES_ITEM`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 18
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `INTFACE_SEQ_NUM` | Intface_Seqessorial Num | NUMBER | 22 | 9 | N |
| 3 | `INTFACE_SEQ_NUM_MES` | Intface_Seq_Numessorial Mes | NUMBER | 22 | 9 | N |
| 4 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 5 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 6 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | N |
| 7 | `ITEM_DES1` | Item Code Description 1 | VARCHAR2 | 40 |  | N |
| 8 | `ITEM_DES2` | Item Code Description 2 | VARCHAR2 | 60 |  | Y |
| 9 | `COUNTRY_CODE` | Country Code | VARCHAR2 | 4 |  | Y |
| 10 | `ITEM_VALUE` | Itemessorial Value | NUMBER | 22 | 12 | Y |
| 11 | `CART_ITEM_WGT` | Cart_Itemessorial Wgt | NUMBER | 22 | 16 | N |
| 12 | `CART_ITEM_QTY` | Cart_Itemessorial Qty | NUMBER | 22 | 9 | N |
| 13 | `CART_ITEM_TARRIF_CODE` | Cart_Item_Tarrifessorial Code | VARCHAR2 | 20 |  | Y |
| 14 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 15 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 16 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 17 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 18 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `C_INTFACE_SHIPMENT_QUEUE`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `SHIPMENT_NUM` | Shipmentessorial Num | NUMBER | 22 | 9 | N |
| 4 | `SHIPMENT_SRCE_FLAG` | Shipment_Srceessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `ACTION_FLAG` | Actionessorial Flag | VARCHAR2 | 1 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | N |
| 7 | `NUM_OF_CART` | Num_Ofessorial Cart | NUMBER | 22 | 9 | N |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `C_LOAD`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 130
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | N |
| 4 | `LOAD_TP_CODE` | Load Type Code | VARCHAR2 | 4 |  | N |
| 5 | `YEAR_LOAD` | Yarehouse Load | NUMBER | 22 | 4 | N |
| 6 | `MONTH_LOAD` | Monthessorial Load | VARCHAR2 | 3 |  | N |
| 7 | `DAY1_INB_LOAD` | Day1_Inbessorial Load | NUMBER | 22 | 9 | Y |
| 8 | `DAY1_INB_WGT` | Day1_Inbessorial Wgt | NUMBER | 22 | 11 | Y |
| 9 | `DAY2_INB_LOAD` | Day2_Inbessorial Load | NUMBER | 22 | 9 | Y |
| 10 | `DAY2_INB_WGT` | Day2_Inbessorial Wgt | NUMBER | 22 | 11 | Y |
| 11 | `DAY3_INB_LOAD` | Day3_Inbessorial Load | NUMBER | 22 | 9 | Y |
| 12 | `DAY3_INB_WGT` | Day3_Inbessorial Wgt | NUMBER | 22 | 11 | Y |
| 13 | `DAY4_INB_LOAD` | Day4_Inbessorial Load | NUMBER | 22 | 9 | Y |
| 14 | `DAY4_INB_WGT` | Day4_Inbessorial Wgt | NUMBER | 22 | 11 | Y |
| 15 | `DAY5_INB_LOAD` | Day5_Inbessorial Load | NUMBER | 22 | 9 | Y |
| 16 | `DAY5_INB_WGT` | Day5_Inbessorial Wgt | NUMBER | 22 | 11 | Y |
| 17 | `DAY6_INB_LOAD` | Day6_Inbessorial Load | NUMBER | 22 | 9 | Y |
| 18 | `DAY6_INB_WGT` | Day6_Inbessorial Wgt | NUMBER | 22 | 11 | Y |
| 19 | `DAY7_INB_LOAD` | Day7_Inbessorial Load | NUMBER | 22 | 9 | Y |
| 20 | `DAY7_INB_WGT` | Day7_Inbessorial Wgt | NUMBER | 22 | 11 | Y |
| 21 | `DAY8_INB_LOAD` | Day8_Inbessorial Load | NUMBER | 22 | 9 | Y |
| 22 | `DAY8_INB_WGT` | Day8_Inbessorial Wgt | NUMBER | 22 | 11 | Y |
| 23 | `DAY9_INB_LOAD` | Day9_Inbessorial Load | NUMBER | 22 | 9 | Y |
| 24 | `DAY9_INB_WGT` | Day9_Inbessorial Wgt | NUMBER | 22 | 11 | Y |
| 25 | `DAY10_INB_LOAD` | Day10_Inbessorial Load | NUMBER | 22 | 9 | Y |
| 26 | `DAY10_INB_WGT` | Day10_Inbessorial Wgt | NUMBER | 22 | 11 | Y |
| 27 | `DAY11_INB_LOAD` | Day11_Inbessorial Load | NUMBER | 22 | 9 | Y |
| 28 | `DAY11_INB_WGT` | Day11_Inbessorial Wgt | NUMBER | 22 | 11 | Y |
| 29 | `DAY12_INB_LOAD` | Day12_Inbessorial Load | NUMBER | 22 | 9 | Y |
| 30 | `DAY12_INB_WGT` | Day12_Inbessorial Wgt | NUMBER | 22 | 11 | Y |
| 31 | `DAY13_INB_LOAD` | Day13_Inbessorial Load | NUMBER | 22 | 9 | Y |
| 32 | `DAY13_INB_WGT` | Day13_Inbessorial Wgt | NUMBER | 22 | 11 | Y |
| 33 | `DAY14_INB_LOAD` | Day14_Inbessorial Load | NUMBER | 22 | 9 | Y |
| 34 | `DAY14_INB_WGT` | Day14_Inbessorial Wgt | NUMBER | 22 | 11 | Y |
| 35 | `DAY15_INB_LOAD` | Day15_Inbessorial Load | NUMBER | 22 | 9 | Y |
| 36 | `DAY15_INB_WGT` | Day15_Inbessorial Wgt | NUMBER | 22 | 11 | Y |
| 37 | `DAY16_INB_LOAD` | Day16_Inbessorial Load | NUMBER | 22 | 9 | Y |
| 38 | `DAY16_INB_WGT` | Day16_Inbessorial Wgt | NUMBER | 22 | 11 | Y |
| 39 | `DAY17_INB_LOAD` | Day17_Inbessorial Load | NUMBER | 22 | 9 | Y |
| 40 | `DAY17_INB_WGT` | Day17_Inbessorial Wgt | NUMBER | 22 | 11 | Y |
| 41 | `DAY18_INB_LOAD` | Day18_Inbessorial Load | NUMBER | 22 | 9 | Y |
| 42 | `DAY18_INB_WGT` | Day18_Inbessorial Wgt | NUMBER | 22 | 11 | Y |
| 43 | `DAY19_INB_LOAD` | Day19_Inbessorial Load | NUMBER | 22 | 9 | Y |
| 44 | `DAY19_INB_WGT` | Day19_Inbessorial Wgt | NUMBER | 22 | 11 | Y |
| 45 | `DAY20_INB_LOAD` | Day20_Inbessorial Load | NUMBER | 22 | 9 | Y |
| 46 | `DAY20_INB_WGT` | Day20_Inbessorial Wgt | NUMBER | 22 | 11 | Y |
| 47 | `DAY21_INB_LOAD` | Day21_Inbessorial Load | NUMBER | 22 | 9 | Y |
| 48 | `DAY21_INB_WGT` | Day21_Inbessorial Wgt | NUMBER | 22 | 11 | Y |
| 49 | `DAY22_INB_LOAD` | Day22_Inbessorial Load | NUMBER | 22 | 9 | Y |
| 50 | `DAY22_INB_WGT` | Day22_Inbessorial Wgt | NUMBER | 22 | 11 | Y |
| 51 | `DAY23_INB_LOAD` | Day23_Inbessorial Load | NUMBER | 22 | 9 | Y |
| 52 | `DAY23_INB_WGT` | Day23_Inbessorial Wgt | NUMBER | 22 | 11 | Y |
| 53 | `DAY24_INB_LOAD` | Day24_Inbessorial Load | NUMBER | 22 | 9 | Y |
| 54 | `DAY24_INB_WGT` | Day24_Inbessorial Wgt | NUMBER | 22 | 11 | Y |
| 55 | `DAY25_INB_LOAD` | Day25_Inbessorial Load | NUMBER | 22 | 9 | Y |
| 56 | `DAY25_INB_WGT` | Day25_Inbessorial Wgt | NUMBER | 22 | 11 | Y |
| 57 | `DAY26_INB_LOAD` | Day26_Inbessorial Load | NUMBER | 22 | 9 | Y |
| 58 | `DAY26_INB_WGT` | Day26_Inbessorial Wgt | NUMBER | 22 | 11 | Y |
| 59 | `DAY27_INB_LOAD` | Day27_Inbessorial Load | NUMBER | 22 | 9 | Y |
| 60 | `DAY27_INB_WGT` | Day27_Inbessorial Wgt | NUMBER | 22 | 11 | Y |
| 61 | `DAY28_INB_LOAD` | Day28_Inbessorial Load | NUMBER | 22 | 9 | Y |
| 62 | `DAY28_INB_WGT` | Day28_Inbessorial Wgt | NUMBER | 22 | 11 | Y |
| 63 | `DAY29_INB_LOAD` | Day29_Inbessorial Load | NUMBER | 22 | 9 | Y |
| 64 | `DAY29_INB_WGT` | Day29_Inbessorial Wgt | NUMBER | 22 | 11 | Y |
| 65 | `DAY30_INB_LOAD` | Day30_Inbessorial Load | NUMBER | 22 | 9 | Y |
| 66 | `DAY30_INB_WGT` | Day30_Inbessorial Wgt | NUMBER | 22 | 11 | Y |
| 67 | `DAY31_INB_LOAD` | Day31_Inbessorial Load | NUMBER | 22 | 9 | Y |
| 68 | `DAY31_INB_WGT` | Day31_Inbessorial Wgt | NUMBER | 22 | 11 | Y |
| 69 | `DAY1_OUTB_LOAD` | Day1_Outbessorial Load | NUMBER | 22 | 9 | Y |
| 70 | `DAY1_OUTB_WGT` | Day1_Outbessorial Wgt | NUMBER | 22 | 11 | Y |
| 71 | `DAY2_OUTB_LOAD` | Day2_Outbessorial Load | NUMBER | 22 | 9 | Y |
| 72 | `DAY2_OUTB_WGT` | Day2_Outbessorial Wgt | NUMBER | 22 | 11 | Y |
| 73 | `DAY3_OUTB_LOAD` | Day3_Outbessorial Load | NUMBER | 22 | 9 | Y |
| 74 | `DAY3_OUTB_WGT` | Day3_Outbessorial Wgt | NUMBER | 22 | 11 | Y |
| 75 | `DAY4_OUTB_LOAD` | Day4_Outbessorial Load | NUMBER | 22 | 9 | Y |
| 76 | `DAY4_OUTB_WGT` | Day4_Outbessorial Wgt | NUMBER | 22 | 11 | Y |
| 77 | `DAY5_OUTB_LOAD` | Day5_Outbessorial Load | NUMBER | 22 | 9 | Y |
| 78 | `DAY5_OUTB_WGT` | Day5_Outbessorial Wgt | NUMBER | 22 | 11 | Y |
| 79 | `DAY6_OUTB_LOAD` | Day6_Outbessorial Load | NUMBER | 22 | 9 | Y |
| 80 | `DAY6_OUTB_WGT` | Day6_Outbessorial Wgt | NUMBER | 22 | 11 | Y |
| 81 | `DAY7_OUTB_LOAD` | Day7_Outbessorial Load | NUMBER | 22 | 9 | Y |
| 82 | `DAY7_OUTB_WGT` | Day7_Outbessorial Wgt | NUMBER | 22 | 11 | Y |
| 83 | `DAY8_OUTB_LOAD` | Day8_Outbessorial Load | NUMBER | 22 | 9 | Y |
| 84 | `DAY8_OUTB_WGT` | Day8_Outbessorial Wgt | NUMBER | 22 | 11 | Y |
| 85 | `DAY9_OUTB_LOAD` | Day9_Outbessorial Load | NUMBER | 22 | 9 | Y |
| 86 | `DAY9_OUTB_WGT` | Day9_Outbessorial Wgt | NUMBER | 22 | 11 | Y |
| 87 | `DAY10_OUTB_LOAD` | Day10_Outbessorial Load | NUMBER | 22 | 9 | Y |
| 88 | `DAY10_OUTB_WGT` | Day10_Outbessorial Wgt | NUMBER | 22 | 11 | Y |
| 89 | `DAY11_OUTB_LOAD` | Day11_Outbessorial Load | NUMBER | 22 | 9 | Y |
| 90 | `DAY11_OUTB_WGT` | Day11_Outbessorial Wgt | NUMBER | 22 | 11 | Y |
| 91 | `DAY12_OUTB_LOAD` | Day12_Outbessorial Load | NUMBER | 22 | 9 | Y |
| 92 | `DAY12_OUTB_WGT` | Day12_Outbessorial Wgt | NUMBER | 22 | 11 | Y |
| 93 | `DAY13_OUTB_LOAD` | Day13_Outbessorial Load | NUMBER | 22 | 9 | Y |
| 94 | `DAY13_OUTB_WGT` | Day13_Outbessorial Wgt | NUMBER | 22 | 11 | Y |
| 95 | `DAY14_OUTB_LOAD` | Day14_Outbessorial Load | NUMBER | 22 | 9 | Y |
| 96 | `DAY14_OUTB_WGT` | Day14_Outbessorial Wgt | NUMBER | 22 | 11 | Y |
| 97 | `DAY15_OUTB_LOAD` | Day15_Outbessorial Load | NUMBER | 22 | 9 | Y |
| 98 | `DAY15_OUTB_WGT` | Day15_Outbessorial Wgt | NUMBER | 22 | 11 | Y |
| 99 | `DAY16_OUTB_LOAD` | Day16_Outbessorial Load | NUMBER | 22 | 9 | Y |
| 100 | `DAY16_OUTB_WGT` | Day16_Outbessorial Wgt | NUMBER | 22 | 11 | Y |
| 101 | `DAY17_OUTB_LOAD` | Day17_Outbessorial Load | NUMBER | 22 | 9 | Y |
| 102 | `DAY17_OUTB_WGT` | Day17_Outbessorial Wgt | NUMBER | 22 | 11 | Y |
| 103 | `DAY18_OUTB_LOAD` | Day18_Outbessorial Load | NUMBER | 22 | 9 | Y |
| 104 | `DAY18_OUTB_WGT` | Day18_Outbessorial Wgt | NUMBER | 22 | 11 | Y |
| 105 | `DAY19_OUTB_LOAD` | Day19_Outbessorial Load | NUMBER | 22 | 9 | Y |
| 106 | `DAY19_OUTB_WGT` | Day19_Outbessorial Wgt | NUMBER | 22 | 11 | Y |
| 107 | `DAY20_OUTB_LOAD` | Day20_Outbessorial Load | NUMBER | 22 | 9 | Y |
| 108 | `DAY20_OUTB_WGT` | Day20_Outbessorial Wgt | NUMBER | 22 | 11 | Y |
| 109 | `DAY21_OUTB_LOAD` | Day21_Outbessorial Load | NUMBER | 22 | 9 | Y |
| 110 | `DAY21_OUTB_WGT` | Day21_Outbessorial Wgt | NUMBER | 22 | 11 | Y |
| 111 | `DAY22_OUTB_LOAD` | Day22_Outbessorial Load | NUMBER | 22 | 9 | Y |
| 112 | `DAY22_OUTB_WGT` | Day22_Outbessorial Wgt | NUMBER | 22 | 11 | Y |
| 113 | `DAY23_OUTB_LOAD` | Day23_Outbessorial Load | NUMBER | 22 | 9 | Y |
| 114 | `DAY23_OUTB_WGT` | Day23_Outbessorial Wgt | NUMBER | 22 | 11 | Y |
| 115 | `DAY24_OUTB_LOAD` | Day24_Outbessorial Load | NUMBER | 22 | 9 | Y |
| 116 | `DAY24_OUTB_WGT` | Day24_Outbessorial Wgt | NUMBER | 22 | 11 | Y |
| 117 | `DAY25_OUTB_LOAD` | Day25_Outbessorial Load | NUMBER | 22 | 9 | Y |
| 118 | `DAY25_OUTB_WGT` | Day25_Outbessorial Wgt | NUMBER | 22 | 11 | Y |
| 119 | `DAY26_OUTB_LOAD` | Day26_Outbessorial Load | NUMBER | 22 | 9 | Y |
| 120 | `DAY26_OUTB_WGT` | Day26_Outbessorial Wgt | NUMBER | 22 | 11 | Y |
| 121 | `DAY27_OUTB_LOAD` | Day27_Outbessorial Load | NUMBER | 22 | 9 | Y |
| 122 | `DAY27_OUTB_WGT` | Day27_Outbessorial Wgt | NUMBER | 22 | 11 | Y |
| 123 | `DAY28_OUTB_LOAD` | Day28_Outbessorial Load | NUMBER | 22 | 9 | Y |
| 124 | `DAY28_OUTB_WGT` | Day28_Outbessorial Wgt | NUMBER | 22 | 11 | Y |
| 125 | `DAY29_OUTB_LOAD` | Day29_Outbessorial Load | NUMBER | 22 | 9 | Y |
| 126 | `DAY29_OUTB_WGT` | Day29_Outbessorial Wgt | NUMBER | 22 | 11 | Y |
| 127 | `DAY30_OUTB_LOAD` | Day30_Outbessorial Load | NUMBER | 22 | 9 | Y |
| 128 | `DAY30_OUTB_WGT` | Day30_Outbessorial Wgt | NUMBER | 22 | 11 | Y |
| 129 | `DAY31_OUTB_LOAD` | Day31_Outbessorial Load | NUMBER | 22 | 9 | Y |
| 130 | `DAY31_OUTB_WGT` | Day31_Outbessorial Wgt | NUMBER | 22 | 11 | Y |

## `C_ORD_ALLOC_D`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 22
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 9 | N |
| 3 | `TRACE_LEVEL` | Traceessorial Level | NUMBER | 22 | 1 | N |
| 4 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 5 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 6 | `ORD_ALLOC_DATE` | Ord_Allocessorial Date | VARCHAR2 | 30 |  | N |
| 7 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |
| 8 | `ORD_LINE_TP_PRIOR` | Ord_Line_Tpessorial Prior | VARCHAR2 | 1 |  | N |
| 9 | `ORD_LINE_TP_ALLOC` | Ord_Line_Tpessorial Alloc | VARCHAR2 | 1 |  | Y |
| 10 | `ORD_LINE_LOC_BAL_FLAG` | Ord_Line_Loc_Balessorial Flag | VARCHAR2 | 1 |  | Y |
| 11 | `ORD_LINE_LOC_GEN_FLAG` | Ord_Line_Loc_Genessorial Flag | VARCHAR2 | 1 |  | Y |
| 12 | `ORD_ALLOC_LINE_INFO` | Ord_Alloc_Lineessorial Info | VARCHAR2 | 4000 |  | Y |
| 13 | `ORD_ALLOC_LINE_MES` | Ord_Alloc_Lineessorial Mes | VARCHAR2 | 250 |  | Y |
| 14 | `ORD_ALLOC_LINE_ALLOC_FLAG` | Ord_Alloc_Line_Allocessorial Flag | VARCHAR2 | 1 |  | N |
| 15 | `ORD_ALLOC_LINE_REPI_FLAG` | Ord_Alloc_Line_Repiessorial Flag | VARCHAR2 | 1 |  | N |
| 16 | `ORD_ALLOC_LINE_SUB_FLAG` | Ord_Alloc_Line_Subessorial Flag | VARCHAR2 | 1 |  | N |
| 17 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 18 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 19 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 20 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 21 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 22 | `BEFORE_AFTER_FLAG` | Before_Afteressorial Flag | VARCHAR2 | 1 |  | N |

## `C_ORD_ALLOC_DD1`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 14
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 9 | N |
| 3 | `TRACE_LEVEL` | Traceessorial Level | NUMBER | 22 | 1 | N |
| 4 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 5 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 6 | `ORD_ALLOC_DATE` | Ord_Allocessorial Date | VARCHAR2 | 30 |  | N |
| 7 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |
| 8 | `ORD_ALLOC_LINE_CONF_SEQ` | Ord_Alloc_Line_Confessorial Seq | NUMBER | 22 | 9 | N |
| 9 | `ORD_ALLOC_LINE_CONF_INFO` | Ord_Alloc_Line_Confessorial Info | VARCHAR2 | 4000 |  | Y |
| 10 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 11 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 13 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 14 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `C_ORD_ALLOC_DD2`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 14
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 9 | N |
| 3 | `TRACE_LEVEL` | Traceessorial Level | NUMBER | 22 | 1 | N |
| 4 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 5 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 6 | `ORD_ALLOC_DATE` | Ord_Allocessorial Date | VARCHAR2 | 30 |  | N |
| 7 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |
| 8 | `ORD_ALLOC_LINE_GRP_SEQ` | Ord_Alloc_Line_Grpessorial Seq | NUMBER | 22 | 9 | N |
| 9 | `ORD_ALLOC_LINE_GRP_INFO` | Ord_Alloc_Line_Grpessorial Info | VARCHAR2 | 4000 |  | Y |
| 10 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 11 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 13 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 14 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `C_ORD_ALLOC_DD2D`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 18
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 9 | N |
| 3 | `TRACE_LEVEL` | Traceessorial Level | NUMBER | 22 | 1 | N |
| 4 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 5 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 6 | `ORD_ALLOC_DATE` | Ord_Allocessorial Date | VARCHAR2 | 30 |  | N |
| 7 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |
| 8 | `ORD_ALLOC_LINE_GRP_SEQ` | Ord_Alloc_Line_Grpessorial Seq | NUMBER | 22 | 9 | N |
| 9 | `ORD_ALLOC_LINE_GRP_BKD_SEQ` | Ord_Alloc_Line_Grp_Bkdessorial Seq | NUMBER | 22 | 9 | N |
| 10 | `ORD_ALLOC_LINE_GRP_BKD_INFO` | Ord_Alloc_Line_Grp_Bkdessorial Info | VARCHAR2 | 4000 |  | Y |
| 11 | `ORD_ALLOC_LINE_ALLOC_FLAG` | Ord_Alloc_Line_Allocessorial Flag | VARCHAR2 | 1 |  | N |
| 12 | `ORD_ALLOC_LINE_REPI_FLAG` | Ord_Alloc_Line_Repiessorial Flag | VARCHAR2 | 1 |  | N |
| 13 | `ORD_ALLOC_LINE_SUB_FLAG` | Ord_Alloc_Line_Subessorial Flag | VARCHAR2 | 1 |  | N |
| 14 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 15 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 16 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 17 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 18 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `C_ORD_ALLOC_DD2DD1`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 17
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 9 | N |
| 3 | `TRACE_LEVEL` | Traceessorial Level | NUMBER | 22 | 1 | N |
| 4 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 5 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 6 | `ORD_ALLOC_DATE` | Ord_Allocessorial Date | VARCHAR2 | 30 |  | N |
| 7 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |
| 8 | `ORD_ALLOC_LINE_GRP_SEQ` | Ord_Alloc_Line_Grpessorial Seq | NUMBER | 22 | 9 | N |
| 9 | `ORD_ALLOC_LINE_GRP_BKD_SEQ` | Ord_Alloc_Line_Grp_Bkdessorial Seq | NUMBER | 22 | 9 | N |
| 10 | `ORD_ALLOC_LINE_LOC_SEQ` | Ord_Alloc_Line_Locessorial Seq | NUMBER | 22 | 9 | N |
| 11 | `ORD_ALLOC_LINE_LOC_INFO` | Ord_Alloc_Line_Locessorial Info | VARCHAR2 | 4000 |  | Y |
| 12 | `ORD_ALLOC_LINE_ALLOC_FLAG` | Ord_Alloc_Line_Allocessorial Flag | VARCHAR2 | 1 |  | N |
| 13 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 14 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 15 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 16 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 17 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `C_ORD_ALLOC_DD2DD2`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 17
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 9 | N |
| 3 | `TRACE_LEVEL` | Traceessorial Level | NUMBER | 22 | 1 | N |
| 4 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 5 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 6 | `ORD_ALLOC_DATE` | Ord_Allocessorial Date | VARCHAR2 | 30 |  | N |
| 7 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |
| 8 | `ORD_ALLOC_LINE_GRP_SEQ` | Ord_Alloc_Line_Grpessorial Seq | NUMBER | 22 | 9 | N |
| 9 | `ORD_ALLOC_LINE_GRP_BKD_SEQ` | Ord_Alloc_Line_Grp_Bkdessorial Seq | NUMBER | 22 | 9 | N |
| 10 | `ORD_ALLOC_LINE_LOC_SEQ` | Ord_Alloc_Line_Locessorial Seq | NUMBER | 22 | 9 | N |
| 11 | `ORD_ALLOC_LINE_LOC_INFO` | Ord_Alloc_Line_Locessorial Info | VARCHAR2 | 4000 |  | Y |
| 12 | `ORD_ALLOC_LINE_REPI_FLAG` | Ord_Alloc_Line_Repiessorial Flag | VARCHAR2 | 1 |  | N |
| 13 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 14 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 15 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 16 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 17 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `C_ORD_ALLOC_DD2DD3`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 17
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 9 | N |
| 3 | `TRACE_LEVEL` | Traceessorial Level | NUMBER | 22 | 1 | N |
| 4 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 5 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 6 | `ORD_ALLOC_DATE` | Ord_Allocessorial Date | VARCHAR2 | 30 |  | N |
| 7 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |
| 8 | `ORD_ALLOC_LINE_GRP_SEQ` | Ord_Alloc_Line_Grpessorial Seq | NUMBER | 22 | 9 | N |
| 9 | `ORD_ALLOC_LINE_GRP_BKD_SEQ` | Ord_Alloc_Line_Grp_Bkdessorial Seq | NUMBER | 22 | 9 | N |
| 10 | `ORD_ALLOC_LINE_LOC_SEQ` | Ord_Alloc_Line_Locessorial Seq | NUMBER | 22 | 9 | N |
| 11 | `ORD_ALLOC_LINE_LOC_INFO` | Ord_Alloc_Line_Locessorial Info | VARCHAR2 | 4000 |  | Y |
| 12 | `ORD_ALLOC_LINE_SUB_FLAG` | Ord_Alloc_Line_Subessorial Flag | VARCHAR2 | 1 |  | N |
| 13 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 14 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 15 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 16 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 17 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `C_ORD_ALLOC_H`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 22
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 9 | N |
| 3 | `TRACE_LEVEL` | Traceessorial Level | NUMBER | 22 | 1 | N |
| 4 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 5 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 6 | `ORD_ALLOC_DATE` | Ord_Allocessorial Date | VARCHAR2 | 30 |  | N |
| 7 | `ORD_ALLOC_MODE` | Ord_Allocessorial Mode | VARCHAR2 | 1 |  | N |
| 8 | `ORD_ALLOC_P_LINE_PRIOR` | Ord_Alloc_P_Lineessorial Prior | NUMBER | 22 | 9 | Y |
| 9 | `ORD_ALLOC_W_LINE_PRIOR` | Ord_Alloc_W_Lineessorial Prior | NUMBER | 22 | 9 | Y |
| 10 | `ORD_ALLOC_R_LINE_PRIOR` | Ord_Alloc_R_Lineessorial Prior | NUMBER | 22 | 9 | Y |
| 11 | `ORD_ALLOC_U_LINE_PRIOR` | Ord_Alloc_U_Lineessorial Prior | NUMBER | 22 | 9 | Y |
| 12 | `ORD_ALLOC_P_LINE_ALLOC` | Ord_Alloc_P_Lineessorial Alloc | NUMBER | 22 | 9 | Y |
| 13 | `ORD_ALLOC_W_LINE_ALLOC` | Ord_Alloc_W_Lineessorial Alloc | NUMBER | 22 | 9 | Y |
| 14 | `ORD_ALLOC_R_LINE_ALLOC` | Ord_Alloc_R_Lineessorial Alloc | NUMBER | 22 | 9 | Y |
| 15 | `ORD_ALLOC_U_LINE_ALLOC` | Ord_Alloc_U_Lineessorial Alloc | NUMBER | 22 | 9 | Y |
| 16 | `ORD_ALLOC_INFO` | Ord_Allocessorial Info | VARCHAR2 | 4000 |  | Y |
| 17 | `ORD_ALLOC_MES` | Ord_Allocessorial Mes | VARCHAR2 | 250 |  | Y |
| 18 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 19 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 20 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 21 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 22 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `C_ORD_BAT`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 16
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `ORD_NUM_BAT` | Ord_Numessorial Bat | NUMBER | 22 | 9 | N |
| 3 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 4 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |
| 5 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 6 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 7 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | Y |
| 8 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | Y |
| 9 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | Y |
| 10 | `INVT_LEV5` | Inventory Level 5 | VARCHAR2 | 40 |  | Y |
| 11 | `ORD_ORD_QTY` | Ord_Ordessorial Qty | NUMBER | 22 | 9 | Y |
| 12 | `ORD_SHIP_QTY` | Ord_Shipessorial Qty | NUMBER | 22 | 9 | Y |
| 13 | `ORD_COMPL_FLAG` | Ord_Complessorial Flag | VARCHAR2 | 1 |  | Y |
| 14 | `ORD_ORD_ENT_QTY` | Ord_Ord_Entessorial Qty | VARCHAR2 | 20 |  | Y |
| 15 | `ORD_SHIP_ENT_QTY` | Ord_Ship_Entessorial Qty | VARCHAR2 | 20 |  | Y |
| 16 | `ORD_LINE_NUM_BAT` | Ord_Line_Numessorial Bat | NUMBER | 22 | 4 | Y |

## `C_ORD_LINE_PROS_EXCP`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 9
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 3 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |
| 4 | `PROS_CODE` | Prosessorial Code | VARCHAR2 | 4 |  | N |
| 5 | `PROS_VALUE` | Prosessorial Value | VARCHAR2 | 250 |  | Y |
| 6 | `REAS_CODE` | Reasessorial Code | VARCHAR2 | 4 |  | Y |
| 7 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 8 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 9 | `ORD_PROS_LINE_EXCP_DATE` | Ord_Pros_Line_Excpessorial Date | DATE | 7 |  | N |

## `C_ORD_LOG`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 29
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4, HOLD_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ORD_LOG_SEQ_NUM` | Ord_Log_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `REC_CNT` | Recessorial Cnt | NUMBER | 22 | 9 | N |
| 3 | `CREATE_DATE` | Create Date | DATE | 7 |  | N |
| 4 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 5 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 6 | `CALLING_PGM_DES` | Calling_Pgmessorial Des | VARCHAR2 | 30 |  | N |
| 7 | `REC_TP` | Recessorial Tp | VARCHAR2 | 30 |  | N |
| 8 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 9 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 10 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 11 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | Y |
| 12 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | Y |
| 13 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | Y |
| 14 | `INVT_LEV5` | Inventory Level 5 | VARCHAR2 | 40 |  | Y |
| 15 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |
| 16 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 17 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |
| 18 | `ORD_LINE_TP` | Order Line Type | VARCHAR2 | 1 |  | Y |
| 19 | `ORD_LOC_LINE_NUM` | Ord_Loc_Lineessorial Num | NUMBER | 22 | 4 | Y |
| 20 | `WHSE_CODE_FROM` | Whse_Codeessorial From | VARCHAR2 | 4 |  | Y |
| 21 | `LOC_CODE_FROM` | Loc_Codeessorial From | VARCHAR2 | 12 |  | Y |
| 22 | `WHSE_CODE_TO` | Warehouse Code To | VARCHAR2 | 4 |  | Y |
| 23 | `LOC_CODE_TO` | Loc_Codeessorial To | VARCHAR2 | 12 |  | Y |
| 24 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | Y |
| 25 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | Y |
| 26 | `ORD_SHIP_QTY` | Ord_Shipessorial Qty | NUMBER | 22 | 9 | Y |
| 27 | `ORD_TOT_WGT` | Ord_Totessorial Wgt | NUMBER | 22 | 16 | Y |
| 28 | `ORD_TOT_WGT_NET` | Ord_Tot_Wgtessorial Net | NUMBER | 22 | 16 | Y |
| 29 | `ORD_TOT_CUBE` | Ord_Totessorial Cube | NUMBER | 22 | 16 | Y |

## `C_ORD_PEND`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 22
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 3 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |
| 4 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 5 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 6 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | N |
| 7 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | N |
| 8 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | N |
| 9 | `INVT_LEV5` | Inventory Level 5 | VARCHAR2 | 40 |  | Y |
| 10 | `ORD_PEND_QTY` | Ord_Pendessorial Qty | NUMBER | 22 | 9 | N |
| 11 | `ORD_PEND_WGT` | Ord_Pendessorial Wgt | NUMBER | 22 | 16 | N |
| 12 | `ORD_PEND_CUBE` | Ord_Pendessorial Cube | NUMBER | 22 | 16 | N |
| 13 | `ORD_LINE_TP` | Order Line Type | VARCHAR2 | 1 |  | Y |
| 14 | `WAVE_SEQ_NUM` | Wave_Seqessorial Num | NUMBER | 22 | 9 | Y |
| 15 | `PACK_STN_CODE` | Pack_Stnessorial Code | VARCHAR2 | 4 |  | Y |
| 16 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |
| 17 | `HOLD_RENW_FLAG` | Hold_Renwessorial Flag | VARCHAR2 | 1 |  | Y |
| 18 | `ORD_LINE_TP_ORG` | Ord_Line_Tpessorial Org | VARCHAR2 | 1 |  | Y |
| 19 | `ORD_PEND_WGT_ORG` | Ord_Pend_Wgtessorial Org | NUMBER | 22 | 16 | Y |
| 20 | `ORD_PEND_ITSH_WGT_SHIP_FLAG` | Ord_Pend_Itsh_Wgt_Shipessorial Flag | VARCHAR2 | 1 |  | Y |
| 21 | `ORD_PEND_EXPY_DATE_OVRR` | Ord_Pend_Expy_Dateessorial Ovrr | DATE | 7 |  | Y |
| 22 | `ORD_PEND_SHIP_FLIFO_FLAG` | Ord_Pend_Ship_Flifoessorial Flag | VARCHAR2 | 1 |  | Y |

## `C_ORD_SPC_PROS_LINE`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 3 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |
| 4 | `ORD_LINE_SRCE_LINE` | Ord_Line_Srceessorial Line | NUMBER | 22 | 4 | N |
| 5 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | N |
| 6 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 7 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 8 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | N |
| 9 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | N |
| 10 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | N |
| 11 | `INVT_LEV5` | Inventory Level 5 | VARCHAR2 | 40 |  | Y |
| 12 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |

## `C_ORD_STATS`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 8
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 3 | `ORD_STATS_ITEM_CNT` | Ord_Stats_Itemessorial Cnt | NUMBER | 22 | 4 | Y |
| 4 | `ORD_STATS_ITEM_VAL` | Ord_Stats_Itemessorial Val | VARCHAR2 | 250 |  | Y |
| 5 | `ORD_STATS_LOC_CNT` | Ord_Stats_Locessorial Cnt | NUMBER | 22 | 4 | Y |
| 6 | `ORD_STATS_LOC_VAL` | Ord_Stats_Locessorial Val | VARCHAR2 | 250 |  | Y |
| 7 | `ORD_STATS_PROS_FLAG` | Ord_Stats_Prosessorial Flag | VARCHAR2 | 1 |  | Y |
| 8 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | Y |

## `C_ORD_VIRT`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 22

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE_VIRT` | Comp_Codeessorial Virt | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE_VIRT` | Cust_Codeessorial Virt | VARCHAR2 | 10 |  | N |
| 3 | `INVT_LEV1_VIRT` | Invt_Lev1essorial Virt | VARCHAR2 | 40 |  | N |
| 4 | `INVT_LEV2_VIRT` | Invt_Lev2essorial Virt | VARCHAR2 | 40 |  | N |
| 5 | `INVT_LEV3_VIRT` | Invt_Lev3essorial Virt | VARCHAR2 | 40 |  | N |
| 6 | `INVT_LEV4_VIRT` | Invt_Lev4essorial Virt | VARCHAR2 | 40 |  | N |
| 7 | `INVT_ACCESS_VIRT` | Invt_Accessessorial Virt | VARCHAR2 | 5 |  | N |
| 8 | `ORD_NUM_VIRT` | Ord_Numessorial Virt | NUMBER | 22 | 9 | N |
| 9 | `ORD_LINE_NUM_VIRT` | Ord_Line_Numessorial Virt | NUMBER | 22 | 4 | N |
| 10 | `ORD_SHIP_QTY_VIRT` | Ord_Ship_Qtyessorial Virt | NUMBER | 22 | 9 | N |
| 11 | `ORD_SHIP_ENT_QTY_VIRT` | Ord_Ship_Ent_Qtyessorial Virt | VARCHAR2 | 20 |  | N |
| 12 | `ORD_SHIP_DATE_VIRT` | Ord_Ship_Dateessorial Virt | DATE | 7 |  | N |
| 13 | `COMP_CODE_ORD` | Comp_Codeessorial Ord | VARCHAR2 | 2 |  | N |
| 14 | `CUST_CODE_ORD` | Cust_Codeessorial Ord | VARCHAR2 | 10 |  | N |
| 15 | `INVT_LEV1_ORD` | Invt_Lev1essorial Ord | VARCHAR2 | 40 |  | N |
| 16 | `INVT_LEV2_ORD` | Invt_Lev2essorial Ord | VARCHAR2 | 40 |  | N |
| 17 | `INVT_LEV3_ORD` | Invt_Lev3essorial Ord | VARCHAR2 | 40 |  | N |
| 18 | `INVT_LEV4_ORD` | Invt_Lev4essorial Ord | VARCHAR2 | 40 |  | N |
| 19 | `ORD_NUM_ORD` | Ord_Numessorial Ord | NUMBER | 22 | 9 | N |
| 20 | `ORD_LINE_NUM_ORD` | Ord_Line_Numessorial Ord | NUMBER | 22 | 4 | N |
| 21 | `ORD_SHIP_QTY_ORD` | Ord_Ship_Qtyessorial Ord | NUMBER | 22 | 9 | N |
| 22 | `ORD_SHIP_ENT_QTY_ORD` | Ord_Ship_Ent_Qtyessorial Ord | VARCHAR2 | 20 |  | N |

## `C_ORG_RATE`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4, RCPT_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 4 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | N |
| 5 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | N |
| 6 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | N |
| 7 | `INVT_LEV5` | Inventory Level 5 | VARCHAR2 | 40 |  | Y |
| 8 | `ORG_UNIT` | Orgessorial Unit | NUMBER | 22 | 9 | N |
| 9 | `ORG_WGT` | Orgessorial Wgt | NUMBER | 22 | 11 | N |
| 10 | `ORG_CUBE` | Orgessorial Cube | NUMBER | 22 | 12 | N |
| 11 | `ORG_DENS` | Orgessorial Dens | NUMBER | 22 | 12 | N |
| 12 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | N |

## `C_PACK_STN_WAVE`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `PACK_STN_CODE` | Pack_Stnessorial Code | VARCHAR2 | 4 |  | N |
| 3 | `WAVE_SEQ_NUM` | Wave_Seqessorial Num | NUMBER | 22 | 9 | N |
| 4 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |

## `C_PALL_HIST`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `PALL_ACC_TP` | Pall_Accessorial Tp | VARCHAR2 | 4 |  | N |
| 3 | `PALL_ACC_CODE` | Pall_Accessorial Code | VARCHAR2 | 10 |  | N |
| 4 | `PALL_HIST_TP` | Pall_Histessorial Tp | VARCHAR2 | 1 |  | N |
| 5 | `PALL_TRANS_TP` | Pall_Transessorial Tp | VARCHAR2 | 1 |  | N |
| 6 | `PALL_TRANS_DATE` | Pall_Transessorial Date | DATE | 7 |  | N |
| 7 | `PALL_TRANS_CONF_FLAG` | Pall_Trans_Confessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `PALL_CODE` | Pallessorial Code | VARCHAR2 | 4 |  | N |
| 9 | `PALL_QTY` | Pallessorial Qty | NUMBER | 22 | 4 | N |
| 10 | `DOC_NUM` | Document Number | NUMBER | 22 | 9 | N |
| 11 | `PALL_HIST_QTY` | Pall_Histessorial Qty | NUMBER | 22 | 4 | N |
| 12 | `PALL_REF_DES` | Pall_Refessorial Des | VARCHAR2 | 60 |  | Y |

## `C_PICK_CART`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CART_SEQ_NUM` | Cart_Seqessorial Num | VARCHAR2 | 20 |  | N |
| 3 | `PICK_CART_CREATE_DATE` | Pick_Cart_Createessorial Date | DATE | 7 |  | N |
| 4 | `PICK_CART_PROS_FLAG` | Pick_Cart_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `PICK_CART_END_DATE` | Pick_Cart_Endessorial Date | DATE | 7 |  | Y |
| 6 | `CART_ID` | Cart ID | VARCHAR2 | 40 |  | N |
| 7 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 8 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |
| 9 | `ORD_LOC_LINE_NUM` | Ord_Loc_Lineessorial Num | NUMBER | 22 | 4 | N |
| 10 | `ORD_LOC_QTY` | Ord_Locessorial Qty | NUMBER | 22 | 9 | N |
| 11 | `EMP_TASK_SEQ_NUM` | Emp_Task_Seqessorial Num | NUMBER | 22 | 9 | N |
| 12 | `ACC_CODE` | Accessorial Code | VARCHAR2 | 10 |  | N |

## `C_PLT_BUILD`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `PLT_BUILD_SEQ_NUM` | Plt_Build_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `CART_SEQ_NUM` | Cart_Seqessorial Num | VARCHAR2 | 20 |  | N |
| 3 | `PLT_BUILD_MODE` | Plt_Buildessorial Mode | VARCHAR2 | 4 |  | N |
| 4 | `PLT_BUILD_RQST_DATE` | Plt_Build_Rqstessorial Date | DATE | 7 |  | N |
| 5 | `PLT_BUILD_PROS_FLAG` | Plt_Build_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 6 | `PLT_BUILD_END_DATE` | Plt_Build_Endessorial Date | DATE | 7 |  | Y |
| 7 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 8 | `CART_ID` | Cart ID | VARCHAR2 | 40 |  | Y |
| 9 | `WHSE_CODE_FLOOR` | Whse_Codeessorial Floor | VARCHAR2 | 4 |  | N |
| 10 | `LOC_CODE_FLOOR` | Loc_Codeessorial Floor | VARCHAR2 | 12 |  | N |
| 11 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | N |
| 12 | `FLOW_PROS_CODE_NEXT` | Flow_Pros_Codeessorial Next | VARCHAR2 | 4 |  | N |

## `C_PROD_ORD_H`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 23
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE, LOC_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `PROD_ORD_NUM` | Prod_Ordessorial Num | NUMBER | 22 | 9 | N |
| 4 | `PROD_ORD_PROF_CODE` | Prod_Ord_Professorial Code | VARCHAR2 | 4 |  | N |
| 5 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 6 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | N |
| 7 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 8 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | N |
| 9 | `PROD_ORD_CREATE_DATE` | Prod_Ord_Createessorial Date | DATE | 7 |  | Y |
| 10 | `PROD_ORD_CLOSE_DATE` | Prod_Ord_Closeessorial Date | DATE | 7 |  | Y |
| 11 | `PROD_ORD_STAT` | Prod_Ordessorial Stat | VARCHAR2 | 1 |  | N |
| 12 | `PROD_ORD_REF` | Prod_Ordessorial Ref | VARCHAR2 | 20 |  | Y |
| 13 | `PROD_ORD_CREATE_INIT_RCPT_FLAG` | Prod_Ord_Create_Init_Rcptessorial Flag | VARCHAR2 | 1 |  | N |
| 14 | `PROD_ORD_INVT_TOP_UP_FLAG` | Prod_Ord_Invt_Top_Upessorial Flag | VARCHAR2 | 1 |  | N |
| 15 | `PROD_ORD_INVT_REMAIN_FLAG` | Prod_Ord_Invt_Remainessorial Flag | VARCHAR2 | 1 |  | N |
| 16 | `RCPT_NUM_INIT` | Rcpt_Numessorial Init | NUMBER | 22 | 9 | Y |
| 17 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | Y |
| 18 | `RCPT_NUM_PROD` | Rcpt_Numessorial Prod | NUMBER | 22 | 9 | Y |
| 19 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 20 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 21 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 22 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 23 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `C_PROS_ACT_INVESTGN_LOG`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 18
- **Campos-chave prováveis:** COMP_CODE, LOC_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ACT_INVESTGN_SEQ_NUM` | Act_Investgn_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `ACT_INVESTGN_PROS_DATE` | Act_Investgn_Prosessorial Date | DATE | 7 |  | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `DOC_NUM` | Document Number | NUMBER | 22 | 9 | N |
| 5 | `DOC_LINE_NUM` | Document Line Number | NUMBER | 22 | 4 | N |
| 6 | `DOC_LOC_LINE_NUM` | Document Location Line Number | NUMBER | 22 | 4 | N |
| 7 | `DOC_TP_FLAG` | Doc_Tpessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | N |
| 9 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 10 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | N |
| 11 | `RF_PROF_INVT_CNT_VAL_TP` | Rf_Prof_Invt_Cnt_Valessorial Tp | VARCHAR2 | 1 |  | N |
| 12 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 13 | `BOOK_QTY` | Bookessorial Qty | NUMBER | 22 | 9 | N |
| 14 | `CNT_QTY` | Cntessorial Qty | NUMBER | 22 | 9 | N |
| 15 | `SUPERVISOR_OP_CODE` | Supervisor_Opessorial Code | VARCHAR2 | 20 |  | Y |
| 16 | `SUPERVISOR_APPRV_FLAG` | Supervisor_Apprvessorial Flag | VARCHAR2 | 1 |  | Y |
| 17 | `SEL_CODE` | Selessorial Code | VARCHAR2 | 6 |  | Y |
| 18 | `ACT_INVESTGN_TP_FLAG` | Act_Investgn_Tpessorial Flag | VARCHAR2 | 1 |  | Y |

## `C_PROS_EDI_CHANGE`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 17
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4, LOC_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 2 | `PRT_CODE` | Printer Code | VARCHAR2 | 4 |  | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `DOC_NUM` | Document Number | NUMBER | 22 | 9 | N |
| 5 | `DOC_LINE_NUM` | Document Line Number | NUMBER | 22 | 4 | N |
| 6 | `DOC_TP` | Docessorial Tp | VARCHAR2 | 1 |  | N |
| 7 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 8 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 9 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | N |
| 10 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | N |
| 11 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | N |
| 12 | `INVT_LEV5` | Inventory Level 5 | VARCHAR2 | 40 |  | Y |
| 13 | `QTY_OLD` | Quantity Old | NUMBER | 22 | 9 | N |
| 14 | `QTY_NEW` | Quantity New | NUMBER | 22 | 9 | N |
| 15 | `TRANS_DATE` | Transaction Date | DATE | 7 |  | N |
| 16 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 17 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | N |

## `C_PROS_MVT`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 23
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | N |
| 2 | `PROS_TRANS_DATE` | Pros_Transessorial Date | DATE | 7 |  | N |
| 3 | `PROS_CODE` | Prosessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `PROS_TRANS_TP` | Pros_Transessorial Tp | VARCHAR2 | 2 |  | N |
| 5 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 6 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 7 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 8 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | N |
| 9 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | N |
| 10 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | N |
| 11 | `INVT_LEV5` | Inventory Level 5 | VARCHAR2 | 40 |  | Y |
| 12 | `PROS_VALUE` | Prosessorial Value | VARCHAR2 | 250 |  | N |
| 13 | `PROS_ENT_QTY` | Pros_Entessorial Qty | VARCHAR2 | 20 |  | Y |
| 14 | `PROS_QTY` | Prosessorial Qty | NUMBER | 22 | 9 | Y |
| 15 | `PROS_WGT` | Prosessorial Wgt | NUMBER | 22 | 16 | Y |
| 16 | `PROS_WGT_NET` | Pros_Wgtessorial Net | NUMBER | 22 | 16 | Y |
| 17 | `PROS_CUBE` | Prosessorial Cube | NUMBER | 22 | 16 | Y |
| 18 | `DOC_NUM` | Document Number | NUMBER | 22 | 9 | N |
| 19 | `DOC_LINE_NUM` | Document Line Number | NUMBER | 22 | 4 | N |
| 20 | `DOC_LOC_LINE_NUM` | Document Location Line Number | NUMBER | 22 | 4 | N |
| 21 | `PROS_LINE_NUM` | Pros_Lineessorial Num | NUMBER | 22 | 6 | N |
| 22 | `PROS_PICK_FLAG` | Pros_Pickessorial Flag | VARCHAR2 | 1 |  | Y |
| 23 | `PROS_REF` | Prosessorial Ref | VARCHAR2 | 250 |  | Y |

## `C_PROS_VAL_D`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | N |
| 4 | `PROS_VAL` | Prosessorial Val | VARCHAR2 | 250 |  | N |
| 5 | `CUST_CODE_COMPN` | Cust_Codeessorial Compn | VARCHAR2 | 10 |  | N |
| 6 | `ITEM_CODE_COMPN` | Item_Codeessorial Compn | VARCHAR2 | 20 |  | N |
| 7 | `PROS_VAL_COMPN` | Pros_Valessorial Compn | VARCHAR2 | 250 |  | N |
| 8 | `INVT_LEV2_COMPN` | Invt_Lev2essorial Compn | VARCHAR2 | 40 |  | Y |
| 9 | `INVT_LEV3_COMPN` | Invt_Lev3essorial Compn | VARCHAR2 | 40 |  | Y |
| 10 | `INVT_LEV4_COMPN` | Invt_Lev4essorial Compn | VARCHAR2 | 40 |  | Y |
| 11 | `INVT_LEV5_COMPN` | Invt_Lev5essorial Compn | VARCHAR2 | 40 |  | Y |
| 12 | `COUNTRY_CODE_COMPN` | Country_Codeessorial Compn | VARCHAR2 | 4 |  | Y |

## `C_PROS_VAL_H`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 21
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE, INVT_LEV2, INVT_LEV3, INVT_LEV4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | N |
| 4 | `PROS_VAL` | Prosessorial Val | VARCHAR2 | 250 |  | N |
| 5 | `DOC_TP_FLAG` | Doc_Tpessorial Flag | VARCHAR2 | 1 |  | N |
| 6 | `DOC_NUM` | Document Number | NUMBER | 22 | 9 | N |
| 7 | `DOC_LINE_NUM` | Document Line Number | NUMBER | 22 | 4 | N |
| 8 | `CUST_CODE_SHIP` | Cust_Codeessorial Ship | VARCHAR2 | 10 |  | Y |
| 9 | `ORD_NUM_SHIP` | Ord_Numessorial Ship | NUMBER | 22 | 9 | Y |
| 10 | `PROS_CREATE_DATE` | Pros_Createessorial Date | DATE | 7 |  | N |
| 11 | `PROS_STAT` | Prosessorial Stat | VARCHAR2 | 1 |  | N |
| 12 | `LOAD_NUM` | Load Number | NUMBER | 22 | 6 | Y |
| 13 | `ORD_PACK_NUM` | Ord_Packessorial Num | NUMBER | 22 | 9 | Y |
| 14 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | Y |
| 15 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | Y |
| 16 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | Y |
| 17 | `INVT_LEV5` | Inventory Level 5 | VARCHAR2 | 40 |  | Y |
| 18 | `COUNTRY_CODE` | Country Code | VARCHAR2 | 4 |  | Y |
| 19 | `RCPT_PO_NUM` | Rcpt_Poessorial Num | VARCHAR2 | 20 |  | Y |
| 20 | `RCPT_CONF_DATE` | Rcpt_Confessorial Date | DATE | 7 |  | Y |
| 21 | `ORD_CONF_DATE` | Ord_Confessorial Date | DATE | 7 |  | Y |

## `C_TOTE_ASS`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 17
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `WHSE_CODE_FLT_ASS` | Whse_Code_Fltessorial Ass | VARCHAR2 | 4 |  | N |
| 3 | `LOC_CODE_FLT_ASS` | Loc_Code_Fltessorial Ass | VARCHAR2 | 12 |  | N |
| 4 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | Y |
| 5 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | N |
| 6 | `WHSE_CODE_STATIC` | Whse_Codeessorial Static | VARCHAR2 | 4 |  | N |
| 7 | `LOC_CODE_STATIC` | Loc_Codeessorial Static | VARCHAR2 | 12 |  | N |
| 8 | `ZONE_CODE` | Zone Code | VARCHAR2 | 4 |  | N |
| 9 | `ZONE_CODE_NXT` | Zarehouse Code Nxt | VARCHAR2 | 4 |  | Y |
| 10 | `WAVE_SEQ_NUM` | Wave_Seqessorial Num | NUMBER | 22 | 9 | Y |
| 11 | `JOB_NUM` | Job Number | NUMBER | 22 | 9 | Y |
| 12 | `LOC_SIZE_CODE` | Loc_Sizeessorial Code | VARCHAR2 | 4 |  | N |
| 13 | `WHSE_CODE_DEST` | Whse_Codeessorial Dest | VARCHAR2 | 4 |  | N |
| 14 | `LOC_CODE_DEST` | Loc_Codeessorial Dest | VARCHAR2 | 12 |  | N |
| 15 | `TOTE_ASS_SEQ_NUM` | Tote_Ass_Seqessorial Num | NUMBER | 22 | 9 | N |
| 16 | `TOTE_ASS_ARR_DATE` | Tote_Ass_Arressorial Date | DATE | 7 |  | Y |
| 17 | `TOTE_ASS_CREATE_DATE` | Tote_Ass_Createessorial Date | DATE | 7 |  | N |

## `C_TOTE_ASS_HIST`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 17
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `WHSE_CODE_FLT_ASS` | Whse_Code_Fltessorial Ass | VARCHAR2 | 4 |  | N |
| 3 | `LOC_CODE_FLT_ASS` | Loc_Code_Fltessorial Ass | VARCHAR2 | 12 |  | N |
| 4 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | Y |
| 5 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | N |
| 6 | `WHSE_CODE_STATIC` | Whse_Codeessorial Static | VARCHAR2 | 4 |  | N |
| 7 | `LOC_CODE_STATIC` | Loc_Codeessorial Static | VARCHAR2 | 12 |  | N |
| 8 | `ZONE_CODE` | Zone Code | VARCHAR2 | 4 |  | N |
| 9 | `ZONE_CODE_NXT` | Zarehouse Code Nxt | VARCHAR2 | 4 |  | Y |
| 10 | `WAVE_SEQ_NUM` | Wave_Seqessorial Num | NUMBER | 22 | 9 | Y |
| 11 | `JOB_NUM` | Job Number | NUMBER | 22 | 6 | Y |
| 12 | `LOC_SIZE_CODE` | Loc_Sizeessorial Code | VARCHAR2 | 4 |  | N |
| 13 | `WHSE_CODE_DEST` | Whse_Codeessorial Dest | VARCHAR2 | 4 |  | N |
| 14 | `LOC_CODE_DEST` | Loc_Codeessorial Dest | VARCHAR2 | 12 |  | N |
| 15 | `TOTE_ASS_SEQ_NUM` | Tote_Ass_Seqessorial Num | NUMBER | 22 | 9 | N |
| 16 | `TOTE_ASS_ARR_DATE` | Tote_Ass_Arressorial Date | DATE | 7 |  | Y |
| 17 | `TOTE_ASS_CREATE_DATE` | Tote_Ass_Createessorial Date | DATE | 7 |  | N |

## `C_TRANS`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 18
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `TRANS_DATE` | Transaction Date | DATE | 7 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 5 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | N |
| 6 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | N |
| 7 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | N |
| 8 | `INVT_LEV5` | Inventory Level 5 | VARCHAR2 | 40 |  | Y |
| 9 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 10 | `ORD_PREX` | Ordessorial Prex | VARCHAR2 | 4 |  | N |
| 11 | `TRANS_TP` | Transessorial Tp | VARCHAR2 | 1 |  | N |
| 12 | `ORD_DATE` | Ordessorial Date | DATE | 7 |  | N |
| 13 | `CONF_DATE` | Confessorial Date | DATE | 7 |  | N |
| 14 | `CON_CODE` | Consignee Code | VARCHAR2 | 10 |  | N |
| 15 | `ORD_UNIT` | Ordessorial Unit | NUMBER | 22 | 9 | N |
| 16 | `ORD_SUFX` | Ordessorial Sufx | VARCHAR2 | 4 |  | Y |
| 17 | `INVT_LEV_DES` | Invt_Levessorial Des | VARCHAR2 | 40 |  | Y |
| 18 | `CON_NAME_MAN` | Con_Nameessorial Man | VARCHAR2 | 30 |  | Y |

## `EVCOROUT`

- **Tipo:** Misc
- **Categoria:** Orders
- **Campos:** 22

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `BOXID` | Boxidessorial Boxid | VARCHAR2 | 20 |  | N |
| 2 | `ORDERID` | Orderidessorial Orderid | VARCHAR2 | 20 |  | N |
| 3 | `ORDERCOUNT` | Ordercountessorial Ordercount | VARCHAR2 | 3 |  | Y |
| 4 | `BOXESPERORDER` | Boxesperorderessorial Boxesperorder | VARCHAR2 | 30 |  | Y |
| 5 | `ACTUALSHIPVIA` | Actualshipviaessorial Actualshipvia | VARCHAR2 | 10 |  | Y |
| 6 | `SHIP_DATE` | Shipessorial Date | VARCHAR2 | 20 |  | Y |
| 7 | `SHIP_TIME` | Shipessorial Time | VARCHAR2 | 8 |  | Y |
| 8 | `TRACKNO` | Tracknoessorial Trackno | VARCHAR2 | 20 |  | Y |
| 9 | `CODAMOUNT` | Codamountessorial Codamount | VARCHAR2 | 10 |  | Y |
| 10 | `FREIGHT_CHARGE` | Freightessorial Charge | VARCHAR2 | 8 |  | Y |
| 11 | `ACTUALWEIGHT` | Actualweightessorial Actualweight | VARCHAR2 | 10 |  | Y |
| 12 | `BILLEDWEIGHT` | Billedweightessorial Billedweight | VARCHAR2 | 10 |  | Y |
| 13 | `STATUS` | Statusessorial Status | VARCHAR2 | 30 |  | Y |
| 14 | `DELIVERY_DATE` | Deliveryessorial Date | VARCHAR2 | 8 |  | Y |
| 15 | `DELIVERY_TIME` | Deliveryessorial Time | VARCHAR2 | 8 |  | Y |
| 16 | `DELIVERY_SHIP_VIA` | Delivery_Shipessorial Via | VARCHAR2 | 10 |  | Y |
| 17 | `DELIVERY_RECEIVED_BY` | Delivery_Receivedessorial By | VARCHAR2 | 20 |  | Y |
| 18 | `DELIVERY_LOCATION` | Deliveryessorial Location | VARCHAR2 | 30 |  | Y |
| 19 | `DELIVERY_STATUS` | Deliveryessorial Status | VARCHAR2 | 30 |  | Y |
| 20 | `ACT_FREIGHT_CHARGE` | Act_Freightessorial Charge | VARCHAR2 | 10 |  | Y |
| 21 | `CUST_FREIGHT` | Custessorial Freight | VARCHAR2 | 8 |  | Y |
| 22 | `CUSTORDNUM` | Custordnumessorial Custordnum | VARCHAR2 | 20 |  | Y |

## `E_LOAD_PACK`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 33
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `LOAD_NUM` | Load Number | NUMBER | 22 | 6 | N |
| 3 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | N |
| 4 | `SHIP_LANE_CODE` | Ship_Laneessorial Code | VARCHAR2 | 4 |  | N |
| 5 | `LOAD_PACK_POW_UNIT_NUM` | Load_Pack_Pow_Unitessorial Num | VARCHAR2 | 20 |  | Y |
| 6 | `LOAD_PACK_CARRY_UNIT_NUM` | Load_Pack_Carry_Unitessorial Num | VARCHAR2 | 20 |  | Y |
| 7 | `CON_CODE` | Consignee Code | VARCHAR2 | 10 |  | N |
| 8 | `MHE_TP_CODE` | Mhe_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 9 | `LOAD_PACK_CREATE_DATE` | Load_Pack_Createessorial Date | DATE | 7 |  | N |
| 10 | `LOAD_PACK_SHIP_DATE` | Load_Pack_Shipessorial Date | DATE | 7 |  | Y |
| 11 | `LOAD_PACK_CLOSE_DATE` | Load_Pack_Closeessorial Date | DATE | 7 |  | Y |
| 12 | `LOAD_PACK_EXIT_DATE` | Load_Pack_Exitessorial Date | DATE | 7 |  | Y |
| 13 | `LOAD_PACK_SEAL_NUM1` | Load_Pack_Sealessorial Num1 | VARCHAR2 | 20 |  | Y |
| 14 | `LOAD_PACK_SEAL_NUM2` | Load_Pack_Sealessorial Num2 | VARCHAR2 | 20 |  | Y |
| 15 | `DRIVER_NAME` | Driveressorial Name | VARCHAR2 | 20 |  | Y |
| 16 | `LIC_PLATE` | Licessorial Plate | VARCHAR2 | 20 |  | Y |
| 17 | `TRUCK_FILL_CODE` | Truck_Fillessorial Code | VARCHAR2 | 20 |  | Y |
| 18 | `LOAD_PACK_WGT_CAPC` | Load_Pack_Wgtessorial Capc | NUMBER | 22 | 9 | Y |
| 19 | `LOAD_PACK_STAT` | Load_Packessorial Stat | VARCHAR2 | 1 |  | Y |
| 20 | `LOAD_PACK_REF_NUM1` | Load_Pack_Refessorial Num1 | VARCHAR2 | 40 |  | Y |
| 21 | `LOAD_PACK_REF_NUM2` | Load_Pack_Refessorial Num2 | VARCHAR2 | 40 |  | Y |
| 22 | `LOAD_PACK_REF_NUM3` | Load_Pack_Refessorial Num3 | VARCHAR2 | 40 |  | Y |
| 23 | `ERR_CODE` | Error Code | VARCHAR2 | 6 |  | Y |
| 24 | `ERR_TEXT` | Error Text | VARCHAR2 | 100 |  | Y |
| 25 | `LOAD_PACK_FULL_FLAG` | Load_Pack_Fullessorial Flag | VARCHAR2 | 1 |  | Y |
| 26 | `LOAD_PACK_LOAD_PREX` | Load_Pack_Loadessorial Prex | VARCHAR2 | 4 |  | Y |
| 27 | `LOAD_PACK_LOAD_DATE` | Load_Pack_Loadessorial Date | DATE | 7 |  | Y |
| 28 | `LOAD_PACK_WGT_TARE` | Load_Pack_Wgtessorial Tare | NUMBER | 22 | 14 | Y |
| 29 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | Y |
| 30 | `PO_NUM` | PO Number | VARCHAR2 | 20 |  | Y |
| 31 | `DELV_DATE` | Delvessorial Date | DATE | 7 |  | Y |
| 32 | `TEND_STAT` | Tendessorial Stat | VARCHAR2 | 1 |  | Y |
| 33 | `LOAD_PACK_ORD_NOT_CONF_FLAG` | Load_Pack_Ord_Not_Confessorial Flag | VARCHAR2 | 1 |  | Y |

## `E_LOAD_REM`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `LOAD_NUM` | Load Number | NUMBER | 22 | 6 | N |
| 3 | `LOAD_REM_LINE_NUM` | Load_Rem_Lineessorial Num | NUMBER | 22 | 3 | N |
| 4 | `LOAD_REM_LINE_TEXT` | Load_Rem_Lineessorial Text | VARCHAR2 | 45 |  | Y |

## `E_MAN_ORD`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 8
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM, CUST_CODE, INVT_LEV1

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 3 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |
| 4 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 5 | `ORD_LINE_TP` | Order Line Type | VARCHAR2 | 1 |  | N |
| 6 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 7 | `ORD_ENT_QTY` | Ord_Entessorial Qty | VARCHAR2 | 20 |  | N |
| 8 | `ORD_QTY` | Ordessorial Qty | NUMBER | 22 | 9 | N |

## `E_ORD_ASS_PARA_D`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 13
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 4 | `FUNC_CODE` | Funcessorial Code | VARCHAR2 | 20 |  | N |
| 5 | `REGION_CODE` | Region Code | VARCHAR2 | 20 |  | N |
| 6 | `REGION_TP` | Regionessorial Tp | VARCHAR2 | 1 |  | N |
| 7 | `REGION_FILTER_COL_NAME` | Region_Filter_Colessorial Name | VARCHAR2 | 30 |  | N |
| 8 | `REGION_FILTER_COL_VAL` | Region_Filter_Colessorial Val | VARCHAR2 | 255 |  | Y |
| 9 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 10 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 12 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 13 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `E_ORD_ASS_PARA_H`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 33
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 4 | `FUNC_CODE` | Funcessorial Code | VARCHAR2 | 20 |  | N |
| 5 | `REGION_CODE` | Region Code | VARCHAR2 | 20 |  | N |
| 6 | `REGION_DES` | Regionessorial Des | VARCHAR2 | 100 |  | N |
| 7 | `GLOBAL_COMP` | Globalessorial Comp | VARCHAR2 | 2 |  | N |
| 8 | `VOICE_PROF_CODE` | Voice_Professorial Code | VARCHAR2 | 4 |  | N |
| 9 | `STAG_WHSE_CODE` | Stag_Whseessorial Code | VARCHAR2 | 4 |  | Y |
| 10 | `STAG_LOC_CODE` | Stag_Locessorial Code | VARCHAR2 | 12 |  | Y |
| 11 | `REGION_STAT` | Regionessorial Stat | VARCHAR2 | 1 |  | N |
| 12 | `OPID_PREX` | Opidessorial Prex | VARCHAR2 | 30 |  | Y |
| 13 | `OPID_SPOKEN_LEN` | Opid_Spokenessorial Len | NUMBER | 22 | 2 | Y |
| 14 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | Y |
| 15 | `LINEAR_MEAS_CODE` | Linear Measurement Code | VARCHAR2 | 4 |  | Y |
| 16 | `MAX_PALL_WGT` | Max_Pallessorial Wgt | NUMBER | 22 | 14 | Y |
| 17 | `MAX_PALL_CUBE` | Max_Pallessorial Cube | NUMBER | 22 | 14 | Y |
| 18 | `MAX_HALF_PALL_CUBE` | Max_Half_Pallessorial Cube | NUMBER | 22 | 14 | Y |
| 19 | `SORT_SEQ_CODE` | Sort_Seqessorial Code | VARCHAR2 | 4 |  | Y |
| 20 | `OPID_SPOKEN_NUM_FLAG` | Opid_Spoken_Numessorial Flag | VARCHAR2 | 1 |  | Y |
| 21 | `UI_LOC_CHECK_DIGIT_LEN` | Ui_Loc_Check_Digitessorial Len | NUMBER | 22 | 2 | Y |
| 22 | `PICK_PATH_MODE_CODE` | Pick_Path_Modeessorial Code | VARCHAR2 | 4 |  | Y |
| 23 | `MAX_NUM_OF_CART` | Max_Num_Ofessorial Cart | NUMBER | 22 | 9 | Y |
| 24 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 25 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 26 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 27 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 28 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 29 | `MAX_PALL_HGT` | Max_Pallessorial Hgt | NUMBER | 22 | 7 | Y |
| 30 | `MAX_OP_NUM_AISLE` | Max_Op_Numessorial Aisle | NUMBER | 22 | 2 | Y |
| 31 | `ALT_INVT_REP_TP_CODE` | Alt_Invt_Rep_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 32 | `ALT_INVT_REP_CODE` | Alt_Invt_Repessorial Code | VARCHAR2 | 20 |  | Y |
| 33 | `CUST_VOICE_PROF_CODE` | Cust_Voice_Professorial Code | VARCHAR2 | 4 |  | Y |

## `E_ORD_ASS_PARA_ORG_D`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 13
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 4 | `FUNC_CODE` | Funcessorial Code | VARCHAR2 | 20 |  | N |
| 5 | `REGION_CODE` | Region Code | VARCHAR2 | 20 |  | N |
| 6 | `REGION_TP` | Regionessorial Tp | VARCHAR2 | 1 |  | N |
| 7 | `REGION_FILTER_COL_NAME` | Region_Filter_Colessorial Name | VARCHAR2 | 30 |  | N |
| 8 | `REGION_FILTER_COL_VAL` | Region_Filter_Colessorial Val | VARCHAR2 | 255 |  | Y |
| 9 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 10 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 12 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 13 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `E_ORD_ASS_PARA_ORG_H`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 33
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 4 | `FUNC_CODE` | Funcessorial Code | VARCHAR2 | 20 |  | N |
| 5 | `REGION_CODE` | Region Code | VARCHAR2 | 20 |  | N |
| 6 | `REGION_DES` | Regionessorial Des | VARCHAR2 | 100 |  | N |
| 7 | `GLOBAL_COMP` | Globalessorial Comp | VARCHAR2 | 2 |  | N |
| 8 | `VOICE_PROF_CODE` | Voice_Professorial Code | VARCHAR2 | 4 |  | N |
| 9 | `STAG_WHSE_CODE` | Stag_Whseessorial Code | VARCHAR2 | 4 |  | Y |
| 10 | `STAG_LOC_CODE` | Stag_Locessorial Code | VARCHAR2 | 12 |  | Y |
| 11 | `REGION_STAT` | Regionessorial Stat | VARCHAR2 | 1 |  | N |
| 12 | `OPID_PREX` | Opidessorial Prex | VARCHAR2 | 30 |  | Y |
| 13 | `OPID_SPOKEN_LEN` | Opid_Spokenessorial Len | NUMBER | 22 | 2 | Y |
| 14 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | Y |
| 15 | `LINEAR_MEAS_CODE` | Linear Measurement Code | VARCHAR2 | 4 |  | Y |
| 16 | `MAX_PALL_WGT` | Max_Pallessorial Wgt | NUMBER | 22 | 14 | Y |
| 17 | `MAX_PALL_CUBE` | Max_Pallessorial Cube | NUMBER | 22 | 14 | Y |
| 18 | `MAX_HALF_PALL_CUBE` | Max_Half_Pallessorial Cube | NUMBER | 22 | 14 | Y |
| 19 | `SORT_SEQ_CODE` | Sort_Seqessorial Code | VARCHAR2 | 4 |  | Y |
| 20 | `OPID_SPOKEN_NUM_FLAG` | Opid_Spoken_Numessorial Flag | VARCHAR2 | 1 |  | Y |
| 21 | `UI_LOC_CHECK_DIGIT_LEN` | Ui_Loc_Check_Digitessorial Len | NUMBER | 22 | 2 | Y |
| 22 | `PICK_PATH_MODE_CODE` | Pick_Path_Modeessorial Code | VARCHAR2 | 4 |  | Y |
| 23 | `MAX_NUM_OF_CART` | Max_Num_Ofessorial Cart | NUMBER | 22 | 9 | Y |
| 24 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 25 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 26 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 27 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 28 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 29 | `MAX_PALL_HGT` | Max_Pallessorial Hgt | NUMBER | 22 | 7 | Y |
| 30 | `MAX_OP_NUM_AISLE` | Max_Op_Numessorial Aisle | NUMBER | 22 | 2 | Y |
| 31 | `ALT_INVT_REP_TP_CODE` | Alt_Invt_Rep_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 32 | `ALT_INVT_REP_CODE` | Alt_Invt_Repessorial Code | VARCHAR2 | 20 |  | Y |
| 33 | `CUST_VOICE_PROF_CODE` | Cust_Voice_Professorial Code | VARCHAR2 | 4 |  | Y |

## `E_ORD_D1`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 14
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 4 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |
| 5 | `CUST_CODE_CHG` | Cust_Codeessorial Chg | VARCHAR2 | 10 |  | Y |
| 6 | `CHG_CODE` | Charge Code | VARCHAR2 | 6 |  | Y |
| 7 | `CHG_DATE` | Charge Date | DATE | 7 |  | Y |
| 8 | `ORD_REM_LINE_NUM` | Ord_Rem_Lineessorial Num | NUMBER | 22 | 3 | N |
| 9 | `ORD_REM_LINE_TEXT` | Ord_Rem_Lineessorial Text | VARCHAR2 | 45 |  | Y |
| 10 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 11 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 13 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 14 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `E_ORD_D10`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 20
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 4 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |
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

## `E_ORD_D11`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 18
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 4 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |
| 5 | `ORD_KIT_LINE_NUM` | Ord_Kit_Lineessorial Num | NUMBER | 22 | 4 | N |
| 6 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 7 | `ORD_KIT_INVT_LEV1` | Ord_Kit_Invtessorial Lev1 | VARCHAR2 | 40 |  | N |
| 8 | `ORD_COMPN_INVT_LEV1` | Ord_Compn_Invtessorial Lev1 | VARCHAR2 | 40 |  | N |
| 9 | `ITEM_COMPN_QTY` | Item_Compnessorial Qty | NUMBER | 22 | 16 | Y |
| 10 | `ITEM_COMPN_WGT` | Item_Compnessorial Wgt | NUMBER | 22 | 16 | Y |
| 11 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | Y |
| 12 | `CUST_CODE_COMPN` | Cust_Codeessorial Compn | VARCHAR2 | 10 |  | N |
| 13 | `ITEM_COMPN_PER_KIT_QTY` | Item_Compn_Per_Kitessorial Qty | NUMBER | 22 | 9 | Y |
| 14 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 15 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 16 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 17 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 18 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `E_ORD_D12`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 17
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `ORD_REM_SEQ_NUM` | Ord_Rem_Seqessorial Num | NUMBER | 22 | 9 | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 5 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |
| 6 | `ORD_REM_CUST_FLAG` | Ord_Rem_Custessorial Flag | VARCHAR2 | 1 |  | N |
| 7 | `ORD_REM_CON_FLAG` | Ord_Rem_Conessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `ORD_REM_CARR_FLAG` | Ord_Rem_Carressorial Flag | VARCHAR2 | 1 |  | N |
| 9 | `ORD_REM_RF_FLAG` | Ord_Rem_Rfessorial Flag | VARCHAR2 | 1 |  | N |
| 10 | `ORD_DOC_CODE_REST` | Ord_Doc_Codeessorial Rest | VARCHAR2 | 4 |  | Y |
| 11 | `ORD_REM_MES_CODE` | Ord_Rem_Mesessorial Code | VARCHAR2 | 4 |  | Y |
| 12 | `ORD_REM_TEXT` | Ord_Remessorial Text | VARCHAR2 | 2000 |  | Y |
| 13 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 14 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 15 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 16 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 17 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `E_ORD_D2`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 25
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 4 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |
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
| 15 | `ORD_EXTRA_CHG_QTY` | Ord_Extra_Chgessorial Qty | NUMBER | 22 | 16 | Y |
| 16 | `ORD_EXTRA_CHG_PROS_FLAG` | Ord_Extra_Chg_Prosessorial Flag | VARCHAR2 | 1 |  | Y |
| 17 | `ORD_EXTRA_CHG_ACCEPT_FLAG` | Ord_Extra_Chg_Acceptessorial Flag | VARCHAR2 | 1 |  | Y |
| 18 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | Y |
| 19 | `ORD_EXTRA_CHG_LAST_DATE` | Ord_Extra_Chg_Lastessorial Date | DATE | 7 |  | Y |
| 20 | `PRO_FORMA_PROS_FLAG` | Pro_Forma_Prosessorial Flag | VARCHAR2 | 1 |  | Y |
| 21 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 22 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 23 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 24 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 25 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `E_ORD_D3`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 49
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 4 | `DRV_CODE` | Driver Code | VARCHAR2 | 4 |  | Y |
| 5 | `ORD_POW_UNIT_NUM` | Ord_Pow_Unitessorial Num | VARCHAR2 | 20 |  | Y |
| 6 | `ORD_CARRY_UNIT_NUM` | Ord_Carry_Unitessorial Num | VARCHAR2 | 20 |  | Y |
| 7 | `ORD_VES` | Ordessorial Ves | VARCHAR2 | 20 |  | Y |
| 8 | `ORD_VOY` | Ordessorial Voy | VARCHAR2 | 20 |  | Y |
| 9 | `ORD_SEAL1` | Ordessorial Seal1 | VARCHAR2 | 20 |  | Y |
| 10 | `ORD_SEAL2` | Ordessorial Seal2 | VARCHAR2 | 20 |  | Y |
| 11 | `ORD_TEMP_FRONT` | Ord_Tempessorial Front | VARCHAR2 | 10 |  | Y |
| 12 | `ORD_TEMP_MID` | Ord_Tempessorial Mid | VARCHAR2 | 10 |  | Y |
| 13 | `ORD_TEMP_BACK` | Ord_Tempessorial Back | VARCHAR2 | 10 |  | Y |
| 14 | `DRV_NAME_MAN` | Drv_Nameessorial Man | VARCHAR2 | 30 |  | Y |
| 15 | `ORD_TEMP_SET` | Ord_Tempessorial Set | VARCHAR2 | 10 |  | Y |
| 16 | `ORD_TEMP_AMB` | Ord_Tempessorial Amb | VARCHAR2 | 10 |  | Y |
| 17 | `ORD_SEAL1_INTACT` | Ord_Seal1essorial Intact | VARCHAR2 | 1 |  | Y |
| 18 | `ORD_PALL_QTY_IN` | Ord_Pall_Qtyessorial In | NUMBER | 22 | 4 | Y |
| 19 | `ORD_PALL_QTY_OUT` | Ord_Pall_Qtyessorial Out | NUMBER | 22 | 4 | Y |
| 20 | `ORD_TEMP_6` | Ord_Tempessorial 6 | VARCHAR2 | 10 |  | Y |
| 21 | `ORD_BILLTO_TEL_NUM` | Ord_Billto_Telessorial Num | VARCHAR2 | 20 |  | Y |
| 22 | `ORD_BILLTO_EMAIL_ADD` | Ord_Billto_Emailessorial Add | VARCHAR2 | 250 |  | Y |
| 23 | `ORD_CON_TEL_NUM` | Ord_Con_Telessorial Num | VARCHAR2 | 20 |  | Y |
| 24 | `ORD_CON_EMAIL_ADD` | Ord_Con_Emailessorial Add | VARCHAR2 | 250 |  | Y |
| 25 | `ORD_CON_EIN` | Ord_Conessorial Ein | VARCHAR2 | 20 |  | Y |
| 26 | `ORD_PARCEL_RESIDENTIAL_FLAG` | Ord_Parcel_Residentialessorial Flag | VARCHAR2 | 1 |  | Y |
| 27 | `ORD_PARCEL_SIGNATURE_REQ_TP` | Ord_Parcel_Signature_Reqessorial Tp | VARCHAR2 | 1 |  | Y |
| 28 | `ORD_PARCEL_DELV_CONF` | Ord_Parcel_Delvessorial Conf | VARCHAR2 | 1 |  | Y |
| 29 | `ORD_PARCEL_SATURDAY` | Ord_Parcelessorial Saturday | VARCHAR2 | 1 |  | Y |
| 30 | `ORD_PARCEL_INS_FLAG` | Ord_Parcel_Insessorial Flag | VARCHAR2 | 1 |  | Y |
| 31 | `ORD_PARCEL_INS_CHG_AMT` | Ord_Parcel_Ins_Chgessorial Amt | NUMBER | 22 | 15 | Y |
| 32 | `ORD_PARCEL_INS_DECLARE_AMT` | Ord_Parcel_Ins_Declareessorial Amt | NUMBER | 22 | 15 | Y |
| 33 | `ORD_PARCEL_MES` | Ord_Parcelessorial Mes | VARCHAR2 | 250 |  | Y |
| 34 | `ORD_PARCEL_SHIP_REF1` | Ord_Parcel_Shipessorial Ref1 | VARCHAR2 | 40 |  | Y |
| 35 | `ORD_PARCEL_SHIP_REF2` | Ord_Parcel_Shipessorial Ref2 | VARCHAR2 | 40 |  | Y |
| 36 | `ORD_PARCEL_SHIP_REF3` | Ord_Parcel_Shipessorial Ref3 | VARCHAR2 | 40 |  | Y |
| 37 | `ORD_PARCEL_SHIP_REF4` | Ord_Parcel_Shipessorial Ref4 | VARCHAR2 | 40 |  | Y |
| 38 | `ORD_PARCEL_SHIP_REF5` | Ord_Parcel_Shipessorial Ref5 | VARCHAR2 | 40 |  | Y |
| 39 | `ORD_PARCEL_COD_METH_PAY` | Ord_Parcel_Cod_Methessorial Pay | VARCHAR2 | 40 |  | Y |
| 40 | `ORD_PARCEL_INSIDE_DELV_FLAG` | Ord_Parcel_Inside_Delvessorial Flag | VARCHAR2 | 1 |  | Y |
| 41 | `ORD_PARCEL_HOLD_LOC_FLAG` | Ord_Parcel_Hold_Locessorial Flag | VARCHAR2 | 1 |  | Y |
| 42 | `ORD_PARCEL_CALL_TAG_FLAG` | Ord_Parcel_Call_Tagessorial Flag | VARCHAR2 | 1 |  | Y |
| 43 | `ORD_BILLTO_CONTACT_NAME` | Ord_Billto_Contactessorial Name | VARCHAR2 | 30 |  | Y |
| 44 | `ORD_CON_CONTACT_NAME` | Ord_Con_Contactessorial Name | VARCHAR2 | 30 |  | Y |
| 45 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 46 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 47 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 48 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 49 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `E_ORD_D4`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 14
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
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

## `E_ORD_D5`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 73
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM, CUST_CODE, SKU_CODE, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 4 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |
| 5 | `ORD_LINE_TP` | Order Line Type | VARCHAR2 | 1 |  | N |
| 6 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 7 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | N |
| 8 | `ORD_ORD_ENT_QTY` | Ord_Ord_Entessorial Qty | VARCHAR2 | 20 |  | N |
| 9 | `ORD_ORD_QTY` | Ord_Ordessorial Qty | NUMBER | 22 | 9 | N |
| 10 | `ORD_SHIP_ENT_QTY` | Ord_Ship_Entessorial Qty | VARCHAR2 | 20 |  | N |
| 11 | `ORD_SHIP_QTY` | Ord_Shipessorial Qty | NUMBER | 22 | 9 | N |
| 12 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | N |
| 13 | `ORD_UNIT_WGT` | Ord_Unitessorial Wgt | NUMBER | 22 | 16 | N |
| 14 | `SKU_CODE` | SKU Code | VARCHAR2 | 4 |  | N |
| 15 | `ORD_TOT_WGT` | Ord_Totessorial Wgt | NUMBER | 22 | 16 | N |
| 16 | `ORD_TOT_WGT_NET` | Ord_Tot_Wgtessorial Net | NUMBER | 22 | 16 | N |
| 17 | `LINEAR_MEAS_CODE` | Linear Measurement Code | VARCHAR2 | 4 |  | N |
| 18 | `ORD_TOT_CUBE` | Ord_Totessorial Cube | NUMBER | 22 | 16 | N |
| 19 | `ORD_LINE_REM_FLAG` | Ord_Line_Remessorial Flag | VARCHAR2 | 1 |  | N |
| 20 | `ORD_LINE_EXTRA_CHG_FLAG` | Ord_Line_Extra_Chgessorial Flag | VARCHAR2 | 1 |  | N |
| 21 | `ORD_LINE_ALTER_FLAG` | Ord_Line_Alteressorial Flag | VARCHAR2 | 1 |  | N |
| 22 | `ORD_LINE_LOC_BAL_FLAG` | Ord_Line_Loc_Balessorial Flag | VARCHAR2 | 1 |  | N |
| 23 | `ORD_LINE_LOC_GEN_FLAG` | Ord_Line_Loc_Genessorial Flag | VARCHAR2 | 1 |  | N |
| 24 | `ORD_LINE_CONF_FLAG` | Ord_Line_Confessorial Flag | VARCHAR2 | 1 |  | N |
| 25 | `ORD_LINE_EDI_INFO_FLAG` | Ord_Line_Edi_Infoessorial Flag | VARCHAR2 | 1 |  | N |
| 26 | `ORD_LINE_ITEM_PROS_FLAG` | Ord_Line_Item_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 27 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |
| 28 | `HOLD_RENW_FLAG` | Hold_Renwessorial Flag | VARCHAR2 | 1 |  | Y |
| 29 | `ORD_LEV1` | Ordessorial Lev1 | VARCHAR2 | 40 |  | Y |
| 30 | `ORD_SEQ_QTY_LEV1` | Ord_Seq_Qtyessorial Lev1 | NUMBER | 22 | 4 | Y |
| 31 | `ORD_LEV2` | Ordessorial Lev2 | VARCHAR2 | 40 |  | Y |
| 32 | `ORD_SEQ_QTY_LEV2` | Ord_Seq_Qtyessorial Lev2 | NUMBER | 22 | 4 | Y |
| 33 | `ORD_LEV3` | Ordessorial Lev3 | VARCHAR2 | 40 |  | Y |
| 34 | `ORD_SEQ_QTY_LEV3` | Ord_Seq_Qtyessorial Lev3 | NUMBER | 22 | 4 | Y |
| 35 | `ORD_LEV4` | Ordessorial Lev4 | VARCHAR2 | 40 |  | Y |
| 36 | `ORD_SEQ_QTY_LEV4` | Ord_Seq_Qtyessorial Lev4 | VARCHAR2 | 4 |  | Y |
| 37 | `ORD_LEV5` | Ordessorial Lev5 | VARCHAR2 | 40 |  | Y |
| 38 | `ORD_SEQ_QTY_LEV5` | Ord_Seq_Qtyessorial Lev5 | VARCHAR2 | 4 |  | Y |
| 39 | `ORD_LINE_CONF_DATE` | Ord_Line_Confessorial Date | DATE | 7 |  | Y |
| 40 | `ORD_LINE_SRCE_LINE` | Ord_Line_Srceessorial Line | NUMBER | 22 | 4 | Y |
| 41 | `ITEM_CODE_SUB` | Item_Codeessorial Sub | VARCHAR2 | 20 |  | Y |
| 42 | `FRT_CLASS_DES` | Frt_Classessorial Des | VARCHAR2 | 30 |  | Y |
| 43 | `ORD_PALL` | Ordessorial Pall | NUMBER | 22 | 11 | Y |
| 44 | `ORD_TL_AMT` | Ord_Tlessorial Amt | NUMBER | 22 | 9 | Y |
| 45 | `REAS_CODE` | Reasessorial Code | VARCHAR2 | 4 |  | Y |
| 46 | `ORD_DIST_RCPT_LINE_NUM` | Ord_Dist_Rcpt_Lineessorial Num | NUMBER | 22 | 4 | Y |
| 47 | `ORD_XDOCK_OVER_QTY` | Ord_Xdock_Overessorial Qty | NUMBER | 22 | 9 | Y |
| 48 | `BOND_NUM` | Bond Number | VARCHAR2 | 20 |  | Y |
| 49 | `ISOL_CODE` | ISOL Code | VARCHAR2 | 4 |  | Y |
| 50 | `ORD_EXT_INV_NUM` | Ord_Ext_Invessorial Num | NUMBER | 22 | 16 | Y |
| 51 | `ORD_EXT_INV_PREX` | Ord_Ext_Invessorial Prex | VARCHAR2 | 4 |  | Y |
| 52 | `ORD_EXT_INV_DATE` | Ord_Ext_Invessorial Date | DATE | 7 |  | Y |
| 53 | `ORD_EXT_INV_SEAL_SERIES` | Ord_Ext_Inv_Sealessorial Series | VARCHAR2 | 3 |  | Y |
| 54 | `ORD_EXT_INV_SEAL_NUM` | Ord_Ext_Inv_Sealessorial Num | NUMBER | 22 | 10 | Y |
| 55 | `ORD_DELV_QTY` | Ord_Delvessorial Qty | NUMBER | 22 | 9 | Y |
| 56 | `ORD_DELV_ENT_QTY` | Ord_Delv_Entessorial Qty | VARCHAR2 | 20 |  | Y |
| 57 | `WHSE_CODE_REST` | Whse_Codeessorial Rest | VARCHAR2 | 4 |  | Y |
| 58 | `ORD_LINE_NUM_UPDOWNSTREAM` | Ord_Line_Numessorial Updownstream | NUMBER | 22 | 4 | Y |
| 59 | `ORD_UNALLOC_PICKLINE_PICK_TP` | Ord_Unalloc_Pickline_Pickessorial Tp | VARCHAR2 | 1 |  | Y |
| 60 | `DYN_DAY_RECALC_INVT_EXPY_DATE` | Dyn_Day_Recalc_Invt_Expyessorial Date | NUMBER | 22 | 3 | Y |
| 61 | `ORD_DIST_RCPT_NUM` | Ord_Dist_Rcptessorial Num | NUMBER | 22 | 9 | Y |
| 62 | `ORD_ALLOC_TIME_OLD_INVT_ACCESS` | Ord_Alloc_Time_Old_Invtessorial Access | VARCHAR2 | 5 |  | Y |
| 63 | `ORD_LINE_PICK_METH` | Ord_Line_Pickessorial Meth | VARCHAR2 | 4 |  | Y |
| 64 | `WHSE_CODE_SUG` | Whse_Codeessorial Sug | VARCHAR2 | 4 |  | Y |
| 65 | `LOC_CODE_SUG` | Loc_Codeessorial Sug | VARCHAR2 | 12 |  | Y |
| 66 | `LAST_PICK_QTY_ON_PLT_FLAG` | Last_Pick_Qty_On_Pltessorial Flag | VARCHAR2 | 1 |  | Y |
| 67 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 68 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 69 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 70 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 71 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 72 | `ORD_LINE_EXPY_DATE_OVRR` | Ord_Line_Expy_Dateessorial Ovrr | DATE | 7 |  | Y |
| 73 | `ORD_LINE_SHIP_FLIFO_FLAG` | Ord_Line_Ship_Flifoessorial Flag | VARCHAR2 | 1 |  | Y |

## `E_ORD_D5D1`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 37
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM, CUST_CODE, INVT_LEV1, LOC_CODE, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 4 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |
| 5 | `ORD_LOC_LINE_NUM` | Ord_Loc_Lineessorial Num | NUMBER | 22 | 4 | N |
| 6 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 7 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 8 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | N |
| 9 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 10 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | N |
| 11 | `ORD_LOC_ENT_QTY` | Ord_Loc_Entessorial Qty | VARCHAR2 | 20 |  | N |
| 12 | `ORD_LOC_QTY` | Ord_Locessorial Qty | NUMBER | 22 | 9 | N |
| 13 | `ORD_LOC_CNVC_QTY` | Ord_Loc_Cnvcessorial Qty | NUMBER | 22 | 6 | Y |
| 14 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | N |
| 15 | `ORD_LOC_PROS_FLAG` | Ord_Loc_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 16 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |
| 17 | `HOLD_SHIP_FLAG` | Hold_Shipessorial Flag | VARCHAR2 | 1 |  | Y |
| 18 | `HOLD_RENW_FLAG` | Hold_Renwessorial Flag | VARCHAR2 | 1 |  | Y |
| 19 | `WHSE_CODE_ORG` | Whse_Codeessorial Org | VARCHAR2 | 4 |  | Y |
| 20 | `LOC_CODE_ORG` | Loc_Codeessorial Org | VARCHAR2 | 12 |  | Y |
| 21 | `OUTB_PALL_NUM` | Outb_Pallessorial Num | VARCHAR2 | 20 |  | Y |
| 22 | `WHSE_CODE_STATIC` | Whse_Codeessorial Static | VARCHAR2 | 4 |  | Y |
| 23 | `LOC_CODE_STATIC` | Loc_Codeessorial Static | VARCHAR2 | 12 |  | Y |
| 24 | `WHSE_CODE_MOVE` | Whse_Codeessorial Move | VARCHAR2 | 4 |  | Y |
| 25 | `LOC_CODE_MOVE` | Loc_Codeessorial Move | VARCHAR2 | 12 |  | Y |
| 26 | `UNIT_RETAIL_PRICE` | Unit_Retailessorial Price | NUMBER | 22 | 12 | Y |
| 27 | `UNIT_DISC_PRICE` | Unit_Discessorial Price | NUMBER | 22 | 12 | Y |
| 28 | `UNIT_COST` | Unitessorial Cost | NUMBER | 22 | 12 | Y |
| 29 | `WHSE_ACT_TP_NUM` | Whse_Act_Tpessorial Num | NUMBER | 22 | 2 | Y |
| 30 | `ORD_LOC_CASE_PICK_FLAG` | Ord_Loc_Case_Pickessorial Flag | VARCHAR2 | 1 |  | Y |
| 31 | `RELO_SEQ_NUM` | Relo_Seqessorial Num | NUMBER | 22 | 9 | Y |
| 32 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 33 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 34 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 35 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 36 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 37 | `REGION_CODE` | Region Code | VARCHAR2 | 20 |  | Y |

## `E_ORD_D5D2`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 24
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 4 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |
| 5 | `PROS_CODE` | Prosessorial Code | VARCHAR2 | 4 |  | N |
| 6 | `PROS_LINE_NUM` | Pros_Lineessorial Num | NUMBER | 22 | 6 | N |
| 7 | `PROS_DES` | Prosessorial Des | VARCHAR2 | 30 |  | N |
| 8 | `PROS_TP_CODE` | Pros_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 9 | `PROS_LEN` | Prosessorial Len | VARCHAR2 | 6 |  | N |
| 10 | `COL_TP_CODE` | Col_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 11 | `SKU_CLASS_NUM` | Sku_Classessorial Num | NUMBER | 22 | 1 | N |
| 12 | `PROS_VALUE` | Prosessorial Value | VARCHAR2 | 250 |  | Y |
| 13 | `QRS_NUM` | Qrsessorial Num | VARCHAR2 | 19 |  | Y |
| 14 | `ORD_LOC_LINE_NUM` | Ord_Loc_Lineessorial Num | NUMBER | 22 | 4 | Y |
| 15 | `ORD_PACK_NUM` | Ord_Packessorial Num | NUMBER | 22 | 9 | Y |
| 16 | `ORD_PROS_PRT_FLAG` | Ord_Pros_Prtessorial Flag | VARCHAR2 | 1 |  | Y |
| 17 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | Y |
| 18 | `PROS_REF` | Prosessorial Ref | VARCHAR2 | 250 |  | Y |
| 19 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 20 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 21 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 22 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 23 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 24 | `SORT_VALID_FLAG` | Sort_Validessorial Flag | VARCHAR2 | 1 |  | Y |

## `E_ORD_D5D3`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 4 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |
| 5 | `DOC_CODE` | Document Code | VARCHAR2 | 4 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `E_ORD_D5D4`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 15
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 4 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |
| 5 | `ORD_SALE_EXT_INV_NUM` | Ord_Sale_Ext_Invessorial Num | NUMBER | 22 | 16 | Y |
| 6 | `ORD_SALE_EXT_INV_PREX` | Ord_Sale_Ext_Invessorial Prex | VARCHAR2 | 4 |  | Y |
| 7 | `ORD_SALE_EXT_INV_DATE` | Ord_Sale_Ext_Invessorial Date | DATE | 7 |  | Y |
| 8 | `ORD_SALE_EXT_INV_SEAL_SERIES` | Ord_Sale_Ext_Inv_Sealessorial Series | VARCHAR2 | 3 |  | Y |
| 9 | `ORD_SALE_EXT_INV_SEAL_NUM` | Ord_Sale_Ext_Inv_Sealessorial Num | NUMBER | 22 | 10 | Y |
| 10 | `ORD_SALE_EXT_INV_VALUE` | Ord_Sale_Ext_Invessorial Value | NUMBER | 22 | 16 | Y |
| 11 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 12 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 13 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 14 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 15 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `E_ORD_D5D5`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 4 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |
| 5 | `ORD_REF_VAL` | Ord_Refessorial Val | VARCHAR2 | 40 |  | N |
| 6 | `ORD_REF_QUAL_CODE` | Ord_Ref_Qualessorial Code | VARCHAR2 | 4 |  | Y |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `E_ORD_D5D6`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 21
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM, CUST_CODE, INVT_LEV1

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 4 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |
| 5 | `CREATE_DATE` | Create Date | DATE | 7 |  | N |
| 6 | `SEQ_NUM_SUG` | Seq_Numessorial Sug | NUMBER | 22 | 4 | N |
| 7 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 8 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 9 | `INVT_LEV2_SUG` | Invt_Lev2essorial Sug | VARCHAR2 | 40 |  | Y |
| 10 | `INVT_LEV3_SUG` | Invt_Lev3essorial Sug | VARCHAR2 | 40 |  | Y |
| 11 | `INVT_LEV4_SUG` | Invt_Lev4essorial Sug | VARCHAR2 | 40 |  | Y |
| 12 | `INVT_LEV5_SUG` | Invt_Lev5essorial Sug | VARCHAR2 | 40 |  | Y |
| 13 | `INVT_ACCESS_SUG` | Invt_Accessessorial Sug | VARCHAR2 | 5 |  | Y |
| 14 | `WHSE_CODE_SUG` | Whse_Codeessorial Sug | VARCHAR2 | 4 |  | Y |
| 15 | `LOC_CODE_SUG` | Loc_Codeessorial Sug | VARCHAR2 | 12 |  | Y |
| 16 | `HOLD_CODE_SUG` | Hold_Codeessorial Sug | VARCHAR2 | 4 |  | Y |
| 17 | `QTY_SUG` | Qtyessorial Sug | NUMBER | 22 | 9 | Y |
| 18 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 19 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 20 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 21 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `E_ORD_D5D7`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 13
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 4 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |
| 5 | `INVT_ATTR_PROF_CODE` | Invt_Attr_Professorial Code | VARCHAR2 | 4 |  | N |
| 6 | `INVT_ATTR_NAME` | Invt_Attressorial Name | VARCHAR2 | 20 |  | N |
| 7 | `INVT_ATTR_ALLOC_SORT_SEQ_NUM` | Invt_Attr_Alloc_Sort_Seqessorial Num | NUMBER | 22 | 2 | Y |
| 8 | `INVT_ATTR_VAL_REST` | Invt_Attr_Valessorial Rest | VARCHAR2 | 255 |  | Y |
| 9 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 10 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 12 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 13 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `E_ORD_D6`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 23
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 4 | `INFO_FLOW_SEQ_NUM` | Info_Flow_Seqessorial Num | NUMBER | 22 | 2 | N |
| 5 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | N |
| 6 | `INFO_FLOW_MAND_FLAG` | Info_Flow_Mandessorial Flag | VARCHAR2 | 1 |  | N |
| 7 | `INFO_FLOW_DOC_SEQ_NUM` | Info_Flow_Doc_Seqessorial Num | NUMBER | 22 | 2 | N |
| 8 | `DOC_CODE` | Document Code | VARCHAR2 | 4 |  | Y |
| 9 | `FORM_CODE` | Form Code | VARCHAR2 | 4 |  | Y |
| 10 | `DOC_PRT_TP_FLAG` | Doc_Prt_Tpessorial Flag | VARCHAR2 | 1 |  | Y |
| 11 | `ORD_DOC_PRT_STAT` | Ord_Doc_Prtessorial Stat | VARCHAR2 | 1 |  | Y |
| 12 | `ORD_DOC_REPRT_CNT` | Ord_Doc_Reprtessorial Cnt | NUMBER | 22 | 4 | Y |
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

## `E_ORD_D7`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 46
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 4 | `CUST_CODE_BROK` | Cust_Codeessorial Brok | VARCHAR2 | 10 |  | N |
| 5 | `CUST_INVT_PROF_CODE` | Cust_Invt_Professorial Code | VARCHAR2 | 4 |  | N |
| 6 | `ORD_ITEM_LEV` | Ord_Itemessorial Lev | VARCHAR2 | 8 |  | N |
| 7 | `ORD_ITEM_LEV_DES` | Ord_Item_Levessorial Des | VARCHAR2 | 12 |  | N |
| 8 | `ORD_CHG_LEV_NUM` | Ord_Chg_Levessorial Num | NUMBER | 22 | 1 | N |
| 9 | `ORD_FLIFO_ACTUAL_LEV_VALUE` | Ord_Flifo_Actual_Levessorial Value | NUMBER | 22 | 2 | N |
| 10 | `ORD_FLIFO_ORD_BY_CLAUSE` | Ord_Flifo_Ord_Byessorial Clause | VARCHAR2 | 240 |  | N |
| 11 | `ORD_INVT_TERMGY_CODE_LEV1` | Ord_Invt_Termgy_Codeessorial Lev1 | VARCHAR2 | 4 |  | N |
| 12 | `ORD_LEV_NUM_LEV1` | Ord_Lev_Numessorial Lev1 | NUMBER | 22 | 1 | N |
| 13 | `ORD_INVT_LEV1` | Ord_Invtessorial Lev1 | VARCHAR2 | 9 |  | N |
| 14 | `ORD_FIELD_LEV1` | Ord_Fieldessorial Lev1 | VARCHAR2 | 8 |  | N |
| 15 | `ORD_FLIFO_INVT_VALUE_LEV1` | Ord_Flifo_Invt_Valueessorial Lev1 | NUMBER | 22 | 2 | N |
| 16 | `ORD_SEQ_NUM_FLAG_LEV1` | Ord_Seq_Num_Flagessorial Lev1 | VARCHAR2 | 1 |  | Y |
| 17 | `ORD_INVT_LEV_DES` | Ord_Invt_Levessorial Des | VARCHAR2 | 12 |  | Y |
| 18 | `ORD_INVT_TERMGY_CODE_LEV2` | Ord_Invt_Termgy_Codeessorial Lev2 | VARCHAR2 | 4 |  | Y |
| 19 | `ORD_LEV_NUM_LEV2` | Ord_Lev_Numessorial Lev2 | NUMBER | 22 | 1 | Y |
| 20 | `ORD_INVT_LEV2` | Ord_Invtessorial Lev2 | VARCHAR2 | 9 |  | Y |
| 21 | `ORD_FIELD_LEV2` | Ord_Fieldessorial Lev2 | VARCHAR2 | 8 |  | Y |
| 22 | `ORD_FLIFO_INVT_VALUE_LEV2` | Ord_Flifo_Invt_Valueessorial Lev2 | NUMBER | 22 | 2 | Y |
| 23 | `ORD_SEQ_NUM_FLAG_LEV2` | Ord_Seq_Num_Flagessorial Lev2 | VARCHAR2 | 1 |  | Y |
| 24 | `ORD_INVT_TERMGY_CODE_LEV3` | Ord_Invt_Termgy_Codeessorial Lev3 | VARCHAR2 | 4 |  | Y |
| 25 | `ORD_LEV_NUM_LEV3` | Ord_Lev_Numessorial Lev3 | NUMBER | 22 | 1 | Y |
| 26 | `ORD_INVT_LEV3` | Ord_Invtessorial Lev3 | VARCHAR2 | 9 |  | Y |
| 27 | `ORD_FIELD_LEV3` | Ord_Fieldessorial Lev3 | VARCHAR2 | 8 |  | Y |
| 28 | `ORD_FLIFO_INVT_VALUE_LEV3` | Ord_Flifo_Invt_Valueessorial Lev3 | NUMBER | 22 | 2 | Y |
| 29 | `ORD_SEQ_NUM_FLAG_LEV3` | Ord_Seq_Num_Flagessorial Lev3 | VARCHAR2 | 1 |  | Y |
| 30 | `ORD_INVT_TERMGY_CODE_LEV4` | Ord_Invt_Termgy_Codeessorial Lev4 | VARCHAR2 | 4 |  | Y |
| 31 | `ORD_LEV_NUM_LEV4` | Ord_Lev_Numessorial Lev4 | NUMBER | 22 | 1 | Y |
| 32 | `ORD_INVT_LEV4` | Ord_Invtessorial Lev4 | VARCHAR2 | 9 |  | Y |
| 33 | `ORD_FIELD_LEV4` | Ord_Fieldessorial Lev4 | VARCHAR2 | 8 |  | Y |
| 34 | `ORD_FLIFO_INVT_VALUE_LEV4` | Ord_Flifo_Invt_Valueessorial Lev4 | NUMBER | 22 | 2 | Y |
| 35 | `ORD_SEQ_NUM_FLAG_LEV4` | Ord_Seq_Num_Flagessorial Lev4 | VARCHAR2 | 1 |  | Y |
| 36 | `ORD_INVT_TERMGY_CODE_LEV5` | Ord_Invt_Termgy_Codeessorial Lev5 | VARCHAR2 | 4 |  | Y |
| 37 | `ORD_LEV_NUM_LEV5` | Ord_Lev_Numessorial Lev5 | NUMBER | 22 | 1 | Y |
| 38 | `ORD_INVT_LEV5` | Ord_Invtessorial Lev5 | VARCHAR2 | 9 |  | Y |
| 39 | `ORD_FIELD_LEV5` | Ord_Fieldessorial Lev5 | VARCHAR2 | 8 |  | Y |
| 40 | `ORD_FLIFO_INVT_VALUE_LEV5` | Ord_Flifo_Invt_Valueessorial Lev5 | NUMBER | 22 | 2 | Y |
| 41 | `ORD_SEQ_NUM_FLAG_LEV5` | Ord_Seq_Num_Flagessorial Lev5 | VARCHAR2 | 1 |  | Y |
| 42 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 43 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 44 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 45 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 46 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `E_ORD_D8`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 3 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |
| 4 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 5 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | N |
| 6 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | N |
| 7 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | N |
| 8 | `INVT_LEV5` | Inventory Level 5 | VARCHAR2 | 40 |  | Y |
| 9 | `ORD_DEALLOC_QTY` | Ord_Deallocessorial Qty | NUMBER | 22 | 9 | N |
| 10 | `ORD_DEALLOC_DATE` | Ord_Deallocessorial Date | DATE | 7 |  | N |
| 11 | `ORD_NUM_DEALLOC_FOR` | Ord_Num_Deallocessorial For | NUMBER | 22 | 9 | Y |
| 12 | `ORD_LINE_NUM_DEALLOC_FOR` | Ord_Line_Num_Deallocessorial For | NUMBER | 22 | 4 | Y |

## `E_ORD_D9`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM, LOC_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 4 | `ORD_NUM_BAT` | Ord_Numessorial Bat | NUMBER | 22 | 9 | N |
| 5 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | Y |
| 6 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 7 | `BAT_TP_FLAG` | Bat_Tpessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 9 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 11 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `E_ORD_DRAFT`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 25
- **Campos-chave prováveis:** ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `ORD_DRAFT_STAT_ID` | Ord_Draft_Statessorial Id | RAW | 32 |  | Y |
| 3 | `COMP_ID` | Compessorial Id | RAW | 32 |  | Y |
| 4 | `CUST_ID` | Customer ID | RAW | 32 |  | Y |
| 5 | `ORD_DRAFT_ORD_TP_ID` | Ord_Draft_Ord_Tpessorial Id | RAW | 32 |  | Y |
| 6 | `ORD_DRAFT_PRTY_NUM_ID` | Ord_Draft_Prty_Numessorial Id | RAW | 32 |  | Y |
| 7 | `ORD_DRAFT_CUST_ORD_NUM` | Ord_Draft_Cust_Ordessorial Num | VARCHAR2 | 20 |  | Y |
| 8 | `ORD_DRAFT_PO_NUM` | Ord_Draft_Poessorial Num | VARCHAR2 | 20 |  | Y |
| 9 | `ORD_DRAFT_ORD_ALT_REF1` | Ord_Draft_Ord_Altessorial Ref1 | VARCHAR2 | 20 |  | Y |
| 10 | `ORD_DRAFT_ORD_ALT_REF2` | Ord_Draft_Ord_Altessorial Ref2 | VARCHAR2 | 20 |  | Y |
| 11 | `ORD_DRAFT_ORD_DATE_GMT` | Ord_Draft_Ord_Dateessorial Gmt | DATE | 7 |  | Y |
| 12 | `ORD_DRAFT_ORD_TO_SHIP_DATE_GMT` | Ord_Draft_Ord_To_Ship_Dateessorial Gmt | DATE | 7 |  | Y |
| 13 | `ORD_DRAFT_ORD_TO_ARR_DATE_GMT` | Ord_Draft_Ord_To_Arr_Dateessorial Gmt | DATE | 7 |  | Y |
| 14 | `WHSE_CODE_ID` | Whse_Codeessorial Id | RAW | 32 |  | Y |
| 15 | `ORD_DRAFT_PROS_FLAG` | Ord_Draft_Prosessorial Flag | VARCHAR2 | 1 |  | Y |
| 16 | `ORD_ID` | Ordessorial Id | RAW | 32 |  | Y |
| 17 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 18 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 19 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 20 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 21 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 22 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | Y |
| 23 | `ORD_DRAFT_CARR_FLAG` | Ord_Draft_Carressorial Flag | VARCHAR2 | 1 |  | Y |
| 24 | `ORD_DRAFT_PALL_FLAG` | Ord_Draft_Pallessorial Flag | VARCHAR2 | 1 |  | Y |
| 25 | `LOCK_OP_CODE` | Lock_Opessorial Code | VARCHAR2 | 100 |  | Y |

## `E_ORD_DRAFT_ADDR`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 18

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `ORD_DRAFT_ID` | Ord_Draftessorial Id | RAW | 32 |  | Y |
| 3 | `ORD_DRAFT_ADDR_TP_ID` | Ord_Draft_Addr_Tpessorial Id | RAW | 32 |  | Y |
| 4 | `ORD_DRAFT_ADDR_CODE_ID` | Ord_Draft_Addr_Codeessorial Id | RAW | 32 |  | Y |
| 5 | `ORD_DRAFT_ADDR_NAME` | Ord_Draft_Addressorial Name | VARCHAR2 | 30 |  | Y |
| 6 | `ORD_DRAFT_ADDR_ADD1` | Ord_Draft_Addressorial Add1 | VARCHAR2 | 30 |  | Y |
| 7 | `ORD_DRAFT_ADDR_ADD2` | Ord_Draft_Addressorial Add2 | VARCHAR2 | 30 |  | Y |
| 8 | `ORD_DRAFT_ADDR_ADD3` | Ord_Draft_Addressorial Add3 | VARCHAR2 | 30 |  | Y |
| 9 | `ORD_DRAFT_ADDR_ADD4` | Ord_Draft_Addressorial Add4 | VARCHAR2 | 30 |  | Y |
| 10 | `ORD_DRAFT_ADDR_CITY` | Ord_Draft_Addressorial City | VARCHAR2 | 30 |  | Y |
| 11 | `ORD_DRAFT_ADDR_ZIP` | Ord_Draft_Addressorial Zip | VARCHAR2 | 10 |  | Y |
| 12 | `ORD_DRAFT_ADDR_STATE` | Ord_Draft_Addressorial State | VARCHAR2 | 4 |  | Y |
| 13 | `ORD_DRAFT_ADDR_COUNTRY` | Ord_Draft_Addressorial Country | VARCHAR2 | 4 |  | Y |
| 14 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 15 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 16 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 17 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 18 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `E_ORD_DRAFT_CARR_DET`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 24

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `ORD_DRAFT_ID` | Ord_Draftessorial Id | RAW | 32 |  | Y |
| 3 | `DRV_ID` | Drvessorial Id | RAW | 32 |  | Y |
| 4 | `DRV_NAME` | Drvessorial Name | VARCHAR2 | 30 |  | Y |
| 5 | `ORD_DRAFT_POW_UNIT_NUM` | Ord_Draft_Pow_Unitessorial Num | VARCHAR2 | 20 |  | Y |
| 6 | `ORD_DRAFT_CARRY_UNIT_NUM` | Ord_Draft_Carry_Unitessorial Num | VARCHAR2 | 20 |  | Y |
| 7 | `ORD_DRAFT_VES` | Ord_Draftessorial Ves | VARCHAR2 | 20 |  | Y |
| 8 | `ORD_DRAFT_VOY` | Ord_Draftessorial Voy | VARCHAR2 | 20 |  | Y |
| 9 | `ORD_DRAFT_SEAL1` | Ord_Draftessorial Seal1 | VARCHAR2 | 20 |  | Y |
| 10 | `ORD_DRAFT_SEAL2` | Ord_Draftessorial Seal2 | VARCHAR2 | 20 |  | Y |
| 11 | `ORD_DRAFT_TEMP_FRONT` | Ord_Draft_Tempessorial Front | VARCHAR2 | 10 |  | Y |
| 12 | `ORD_DRAFT_TEMP_MID` | Ord_Draft_Tempessorial Mid | VARCHAR2 | 10 |  | Y |
| 13 | `ORD_DRAFT_TEMP_BACK` | Ord_Draft_Tempessorial Back | VARCHAR2 | 10 |  | Y |
| 14 | `ORD_DRAFT_TEMP_SET` | Ord_Draft_Tempessorial Set | VARCHAR2 | 10 |  | Y |
| 15 | `ORD_DRAFT_TEMP_AMB` | Ord_Draft_Tempessorial Amb | VARCHAR2 | 10 |  | Y |
| 16 | `ORD_DRAFT_TEMP6` | Ord_Draftessorial Temp6 | VARCHAR2 | 10 |  | Y |
| 17 | `ORD_DRAFT_SEAL1_INTACT` | Ord_Draft_Seal1essorial Intact | VARCHAR2 | 1 |  | Y |
| 18 | `ORD_DRAFT_PALL_QTY_IN` | Ord_Draft_Pall_Qtyessorial In | NUMBER | 22 | 4 | Y |
| 19 | `ORD_DRAFT_PALL_QTY_OUT` | Ord_Draft_Pall_Qtyessorial Out | NUMBER | 22 | 4 | Y |
| 20 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 21 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 22 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 23 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 24 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `E_ORD_DRAFT_EDI`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 10

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `ORD_DRAFT_ID` | Ord_Draftessorial Id | RAW | 32 |  | Y |
| 3 | `ORD_DRAFT_LINE_ID` | Ord_Draft_Lineessorial Id | RAW | 32 |  | Y |
| 4 | `EDI_DATA_ID_ID` | Edi_Data_Idessorial Id | RAW | 32 |  | Y |
| 5 | `EDI_DATA_ID_VALUE` | Edi_Data_Idessorial Value | VARCHAR2 | 250 |  | Y |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `E_ORD_DRAFT_LINE`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 24
- **Campos-chave prováveis:** INVT_LEV2, INVT_LEV3, INVT_LEV4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `ORD_DRAFT_ID` | Ord_Draftessorial Id | RAW | 32 |  | Y |
| 3 | `ORD_DRAFT_LINE_TP_ID` | Ord_Draft_Line_Tpessorial Id | RAW | 32 |  | Y |
| 4 | `CUST_ID` | Customer ID | RAW | 32 |  | Y |
| 5 | `ITEM_ID` | Itemessorial Id | RAW | 32 |  | Y |
| 6 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | Y |
| 7 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | Y |
| 8 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | Y |
| 9 | `WHSE_ID` | Warehouse Id | RAW | 32 |  | Y |
| 10 | `ORD_DRAFT_LINE_ORD_QTY` | Ord_Draft_Line_Ordessorial Qty | NUMBER | 22 | 9 | Y |
| 11 | `ORD_DRAFT_LINE_ORD_ENT_QTY` | Ord_Draft_Line_Ord_Entessorial Qty | VARCHAR2 | 20 |  | Y |
| 12 | `ORD_DRAFT_LINE_SHIP_QTY` | Ord_Draft_Line_Shipessorial Qty | NUMBER | 22 | 9 | Y |
| 13 | `ORD_DRAFT_LINE_SHIP_ENT_QTY` | Ord_Draft_Line_Ship_Entessorial Qty | VARCHAR2 | 20 |  | Y |
| 14 | `ORD_DRAFT_LINE_UNIT_WGT` | Ord_Draft_Line_Unitessorial Wgt | NUMBER | 22 | 16 | Y |
| 15 | `SKU_ID` | Skuessorial Id | RAW | 32 |  | Y |
| 16 | `ORD_DRAFT_LINE_WGT` | Ord_Draft_Lineessorial Wgt | NUMBER | 22 | 16 | Y |
| 17 | `ORD_DRAFT_LINE_WGT_NET` | Ord_Draft_Line_Wgtessorial Net | NUMBER | 22 | 16 | Y |
| 18 | `WGT_MEAS_ID` | Wgt_Measessorial Id | RAW | 32 |  | Y |
| 19 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 20 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 21 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 22 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 23 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 24 | `HOLD_ID` | Holdessorial Id | RAW | 32 |  | Y |

## `E_ORD_DRAFT_LINE_PROS`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 11

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `ORD_DRAFT_ID` | Ord_Draftessorial Id | RAW | 32 |  | Y |
| 3 | `ORD_DRAFT_LINE_ID` | Ord_Draft_Lineessorial Id | RAW | 32 |  | Y |
| 4 | `ORD_DRAFT_LOC_LINE_ID` | Ord_Draft_Loc_Lineessorial Id | RAW | 32 |  | Y |
| 5 | `PROS_ID` | Prosessorial Id | RAW | 32 |  | Y |
| 6 | `PROS_VALUE` | Prosessorial Value | VARCHAR2 | 250 |  | Y |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `E_ORD_DRAFT_LOC_LINE`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 12

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `ORD_DRAFT_ID` | Ord_Draftessorial Id | RAW | 32 |  | Y |
| 3 | `ORD_DRAFT_LINE_ID` | Ord_Draft_Lineessorial Id | RAW | 32 |  | Y |
| 4 | `LOC_ID` | Locessorial Id | RAW | 32 |  | Y |
| 5 | `ITEM_ID` | Itemessorial Id | RAW | 32 |  | Y |
| 6 | `ORD_DRAFT_LOC_LINE_QTY` | Ord_Draft_Loc_Lineessorial Qty | NUMBER | 22 | 9 | Y |
| 7 | `ORD_DRAFT_LOC_LINE_ENT_QTY` | Ord_Draft_Loc_Line_Entessorial Qty | VARCHAR2 | 20 |  | Y |
| 8 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 9 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 11 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `E_ORD_DRAFT_MISC`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 27

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `ORD_DRAFT_ID` | Ord_Draftessorial Id | RAW | 32 |  | Y |
| 3 | `LOAD_TP_ID` | Load_Tpessorial Id | RAW | 32 |  | Y |
| 4 | `FRT_TERM_ID` | Frt_Termessorial Id | RAW | 32 |  | Y |
| 5 | `ORD_DRAFT_COD_AMT` | Ord_Draft_Codessorial Amt | NUMBER | 22 | 9 | Y |
| 6 | `PMT_TP_ID` | Pmt_Tpessorial Id | RAW | 32 |  | Y |
| 7 | `MES_ID` | Mesessorial Id | RAW | 32 |  | Y |
| 8 | `ORD_DRAFT_GRP_VAL` | Ord_Draft_Grpessorial Val | VARCHAR2 | 30 |  | Y |
| 9 | `DIST_TP_ID` | Dist_Tpessorial Id | RAW | 32 |  | Y |
| 10 | `ORD_DRAFT_COMPL_ORD_FLAG` | Ord_Draft_Compl_Ordessorial Flag | VARCHAR2 | 1 |  | Y |
| 11 | `ORD_DRAFT_ALLOW_PICKSUB_FLAG` | Ord_Draft_Allow_Picksubessorial Flag | VARCHAR2 | 1 |  | Y |
| 12 | `ORD_DRAFT_ALLOW_OVERPICK_FLAG` | Ord_Draft_Allow_Overpickessorial Flag | VARCHAR2 | 1 |  | Y |
| 13 | `ORD_DRAFT_ALLOW_STAGESOR_FLAG` | Ord_Draft_Allow_Stagesoressorial Flag | VARCHAR2 | 1 |  | Y |
| 14 | `ORD_DRAFT_SHIP_PLT` | Ord_Draft_Shipessorial Plt | NUMBER | 22 | 9 | Y |
| 15 | `ORD_DRAFT_PALL_WGT` | Ord_Draft_Pallessorial Wgt | NUMBER | 22 | 16 | Y |
| 16 | `WGT_MEAS_ID` | Wgt_Measessorial Id | RAW | 32 |  | Y |
| 17 | `PARCEL_CARR_ACC_NUM` | Parcel_Carr_Accessorial Num | VARCHAR2 | 20 |  | Y |
| 18 | `ORD_DRAFT_SHIP_NUM_EXT_REF` | Ord_Draft_Ship_Num_Extessorial Ref | VARCHAR2 | 20 |  | Y |
| 19 | `ORD_DRAFT_FRT_EST_AMT` | Ord_Draft_Frt_Estessorial Amt | NUMBER | 22 | 16 | Y |
| 20 | `ITEM_LOC_PROF_ID` | Item_Loc_Professorial Id | RAW | 32 |  | Y |
| 21 | `SHIP_LANE_ID` | Ship_Laneessorial Id | RAW | 32 |  | Y |
| 22 | `DOC_ID_PACK` | Doc_Idessorial Pack | RAW | 32 |  | Y |
| 23 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 24 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 25 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 26 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 27 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `E_ORD_DRAFT_PALL_DET`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 13

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `ORD_DRAFT_ID` | Ord_Draftessorial Id | RAW | 32 |  | Y |
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

## `E_ORD_DRAFT_PARCEL_DET`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 31

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `ORD_DRAFT_ID` | Ord_Draftessorial Id | RAW | 32 |  | Y |
| 3 | `BILLTO_TEL_NUM` | Billto_Telessorial Num | VARCHAR2 | 20 |  | Y |
| 4 | `BILLTO_EMAIL_ADD` | Billto_Emailessorial Add | VARCHAR2 | 250 |  | Y |
| 5 | `BILLTO_CONTACT_NAME` | Billto_Contactessorial Name | VARCHAR2 | 30 |  | Y |
| 6 | `CON_TEL_NUM` | Con_Telessorial Num | VARCHAR2 | 20 |  | Y |
| 7 | `CON_EMAIL_ADD` | Con_Emailessorial Add | VARCHAR2 | 250 |  | Y |
| 8 | `CON_CONTACT_NAME` | Con_Contactessorial Name | VARCHAR2 | 30 |  | Y |
| 9 | `CON_EIN` | Conessorial Ein | VARCHAR2 | 20 |  | Y |
| 10 | `PARCEL_RESIDENTIAL_FLAG` | Parcel_Residentialessorial Flag | VARCHAR2 | 1 |  | Y |
| 11 | `PARCEL_SIGNATURE_REQ_TP` | Parcel_Signature_Reqessorial Tp | VARCHAR2 | 1 |  | Y |
| 12 | `PARCEL_DELV_CONF` | Parcel_Delvessorial Conf | VARCHAR2 | 1 |  | Y |
| 13 | `PARCEL_SATURDAY` | Parcelessorial Saturday | VARCHAR2 | 1 |  | Y |
| 14 | `PARCEL_INS_FLAG` | Parcel_Insessorial Flag | VARCHAR2 | 1 |  | Y |
| 15 | `PARCEL_INS_CHG_AMT` | Parcel_Ins_Chgessorial Amt | NUMBER | 22 | 15 | Y |
| 16 | `PARCEL_INS_DECLARE_AMT` | Parcel_Ins_Declareessorial Amt | NUMBER | 22 | 15 | Y |
| 17 | `PARCEL_MES` | Parcelessorial Mes | VARCHAR2 | 250 |  | Y |
| 18 | `PARCEL_SHIP_REF1` | Parcel_Shipessorial Ref1 | VARCHAR2 | 40 |  | Y |
| 19 | `PARCEL_SHIP_REF2` | Parcel_Shipessorial Ref2 | VARCHAR2 | 40 |  | Y |
| 20 | `PARCEL_SHIP_REF3` | Parcel_Shipessorial Ref3 | VARCHAR2 | 40 |  | Y |
| 21 | `PARCEL_SHIP_REF4` | Parcel_Shipessorial Ref4 | VARCHAR2 | 40 |  | Y |
| 22 | `PARCEL_SHIP_REF5` | Parcel_Shipessorial Ref5 | VARCHAR2 | 40 |  | Y |
| 23 | `PARCEL_COD_METH_PAY` | Parcel_Cod_Methessorial Pay | VARCHAR2 | 40 |  | Y |
| 24 | `PARCEL_INSIDE_DELV_FLAG` | Parcel_Inside_Delvessorial Flag | VARCHAR2 | 1 |  | Y |
| 25 | `PARCEL_HOLD_LOC_FLAG` | Parcel_Hold_Locessorial Flag | VARCHAR2 | 1 |  | Y |
| 26 | `PARCEL_CALL_TAG_FLAG` | Parcel_Call_Tagessorial Flag | VARCHAR2 | 1 |  | Y |
| 27 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 28 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 29 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 30 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 31 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `E_ORD_DRAFT_PROS`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 8

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `ORD_ID` | Ordessorial Id | RAW | 32 |  | Y |
| 3 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | Y |
| 4 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 5 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 6 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 7 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `E_ORD_DRAFT_REM`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 15

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `ORD_DRAFT_ID` | Ord_Draftessorial Id | RAW | 32 |  | Y |
| 3 | `ORD_DRAFT_LINE_ID` | Ord_Draft_Lineessorial Id | RAW | 32 |  | Y |
| 4 | `ORD_DRAFT_REM_CUST_FLAG` | Ord_Draft_Rem_Custessorial Flag | VARCHAR2 | 1 |  | Y |
| 5 | `ORD_DRAFT_REM_CON_FLAG` | Ord_Draft_Rem_Conessorial Flag | VARCHAR2 | 1 |  | Y |
| 6 | `ORD_DRAFT_REM_CARR_FLAG` | Ord_Draft_Rem_Carressorial Flag | VARCHAR2 | 1 |  | Y |
| 7 | `ORD_DRAFT_REM_RF_FLAG` | Ord_Draft_Rem_Rfessorial Flag | VARCHAR2 | 1 |  | Y |
| 8 | `DOC_ID_REST` | Doc_Idessorial Rest | RAW | 32 |  | Y |
| 9 | `MES_ID` | Mesessorial Id | RAW | 32 |  | Y |
| 10 | `ORD_DRAFT_REM_TEXT` | Ord_Draft_Remessorial Text | VARCHAR2 | 2000 |  | Y |
| 11 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 12 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 13 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 14 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 15 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `E_ORD_H`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 91
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 4 | `ORD_PREX` | Ordessorial Prex | VARCHAR2 | 4 |  | N |
| 5 | `ORD_SUFX` | Ordessorial Sufx | VARCHAR2 | 4 |  | Y |
| 6 | `ORD_STAT` | Ordessorial Stat | VARCHAR2 | 1 |  | N |
| 7 | `ORD_TP` | Ordessorial Tp | VARCHAR2 | 1 |  | N |
| 8 | `ORD_PRTY_NUM` | Ord_Prtyessorial Num | NUMBER | 22 | 1 | N |
| 9 | `ORD_CONF_DATE` | Ord_Confessorial Date | DATE | 7 |  | Y |
| 10 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 11 | `CON_CODE` | Consignee Code | VARCHAR2 | 10 |  | N |
| 12 | `SOLDTO_CODE` | Soldtoessorial Code | VARCHAR2 | 10 |  | N |
| 13 | `ORD_DATE` | Ordessorial Date | DATE | 7 |  | N |
| 14 | `ORD_TO_SHIP_DATE` | Ord_To_Shipessorial Date | DATE | 7 |  | N |
| 15 | `ORD_TO_ARR_DATE` | Ord_To_Arressorial Date | DATE | 7 |  | N |
| 16 | `ORD_CUST_ORD_NUM` | Ord_Cust_Ordessorial Num | VARCHAR2 | 20 |  | Y |
| 17 | `ORD_PO_NUM` | Ord_Poessorial Num | VARCHAR2 | 20 |  | Y |
| 18 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | N |
| 19 | `LOAD_TP_CODE` | Load Type Code | VARCHAR2 | 4 |  | N |
| 20 | `FRT_TERM_CODE` | Frt_Termessorial Code | VARCHAR2 | 4 |  | N |
| 21 | `MES_CODE` | Message Code | VARCHAR2 | 4 |  | Y |
| 22 | `ORD_REM_FLAG` | Ord_Remessorial Flag | VARCHAR2 | 1 |  | N |
| 23 | `ORD_CARR_FLAG` | Ord_Carressorial Flag | VARCHAR2 | 1 |  | N |
| 24 | `ORD_PALL_FLAG` | Ord_Pallessorial Flag | VARCHAR2 | 1 |  | N |
| 25 | `ORD_BILL_FLAG` | Ord_Billessorial Flag | VARCHAR2 | 1 |  | N |
| 26 | `ORD_EXTRA_CHG_FLAG` | Ord_Extra_Chgessorial Flag | VARCHAR2 | 1 |  | N |
| 27 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 28 | `ORD_ENTRY_DATE` | Ord_Entryessorial Date | DATE | 7 |  | N |
| 29 | `ORD_ALTER_FLAG` | Ord_Alteressorial Flag | VARCHAR2 | 1 |  | N |
| 30 | `ORD_CONF_FLAG` | Ord_Confessorial Flag | VARCHAR2 | 1 |  | N |
| 31 | `ORD_LOC_GEN_FLAG` | Ord_Loc_Genessorial Flag | VARCHAR2 | 1 |  | N |
| 32 | `ORD_LOC_STAT` | Ord_Locessorial Stat | VARCHAR2 | 1 |  | N |
| 33 | `ORD_DAY_ACT_REP_PROS_FLAG` | Ord_Day_Act_Rep_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 34 | `INFO_FLOW_PROF_CODE` | Information Flow Profile Code | VARCHAR2 | 4 |  | N |
| 35 | `INFO_FLOW_SEQ_NUM` | Info_Flow_Seqessorial Num | NUMBER | 22 | 2 | N |
| 36 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | N |
| 37 | `ORD_TRANS_FLAG` | Ord_Transessorial Flag | VARCHAR2 | 1 |  | Y |
| 38 | `ORD_TRANS_RCPT_NUM` | Ord_Trans_Rcptessorial Num | NUMBER | 22 | 9 | Y |
| 39 | `ORD_TRANS_RCPT_PREX` | Ord_Trans_Rcptessorial Prex | VARCHAR2 | 4 |  | Y |
| 40 | `ORD_TRANS_RCPT_SUFX` | Ord_Trans_Rcptessorial Sufx | VARCHAR2 | 4 |  | Y |
| 41 | `ORD_SHIP_WGT` | Ord_Shipessorial Wgt | NUMBER | 22 | 9 | Y |
| 42 | `ORD_SHIP_UNIT` | Ord_Shipessorial Unit | NUMBER | 22 | 9 | Y |
| 43 | `ORD_EDI_CREATE_FLAG` | Ord_Edi_Createessorial Flag | VARCHAR2 | 1 |  | N |
| 44 | `ORD_COD_AMT` | Ord_Codessorial Amt | NUMBER | 22 | 9 | Y |
| 45 | `PMT_TP_CODE` | Pmt_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 46 | `ORD_QRS_FLAG` | Ord_Qrsessorial Flag | VARCHAR2 | 1 |  | N |
| 47 | `EDI_INFO_FLAG` | Edi_Infoessorial Flag | VARCHAR2 | 1 |  | N |
| 48 | `ORD_APPO_DATE` | Ord_Appoessorial Date | DATE | 7 |  | Y |
| 49 | `DAY_ACT_REG_NUM` | Day_Act_Regessorial Num | NUMBER | 22 | 6 | Y |
| 50 | `ORD_CARR_FRT_FLAG` | Ord_Carr_Frtessorial Flag | VARCHAR2 | 1 |  | N |
| 51 | `ORD_EDI_GRP_VAL` | Ord_Edi_Grpessorial Val | VARCHAR2 | 30 |  | Y |
| 52 | `ORD_ALT_REF1` | Ord_Altessorial Ref1 | VARCHAR2 | 20 |  | Y |
| 53 | `ORD_ALT_REF2` | Ord_Altessorial Ref2 | VARCHAR2 | 20 |  | Y |
| 54 | `ORD_SHIP_PLT` | Ord_Shipessorial Plt | NUMBER | 22 | 9 | Y |
| 55 | `BORD_NUM` | Bordessorial Num | NUMBER | 22 | 9 | Y |
| 56 | `BORD_FLAG` | Bordessorial Flag | VARCHAR2 | 1 |  | Y |
| 57 | `ORD_SRCE_ORD_NUM` | Ord_Srce_Ordessorial Num | NUMBER | 22 | 9 | Y |
| 58 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 59 | `ORD_PACK_FLAG` | Ord_Packessorial Flag | VARCHAR2 | 1 |  | Y |
| 60 | `BAT_NUM` | Batch Number | NUMBER | 22 | 9 | Y |
| 61 | `MHE_TP_CODE` | Mhe_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 62 | `DIST_TP_CODE` | Dist_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 63 | `PACK_STN_CODE` | Pack_Stnessorial Code | VARCHAR2 | 4 |  | Y |
| 64 | `ORD_COMPL_ORD_FLAG` | Ord_Compl_Ordessorial Flag | VARCHAR2 | 1 |  | Y |
| 65 | `COMP_CODE_UPDOWNSTREAM` | Comp_Codeessorial Updownstream | VARCHAR2 | 2 |  | Y |
| 66 | `ORD_NUM_UPDOWNSTREAM` | Ord_Numessorial Updownstream | NUMBER | 22 | 9 | Y |
| 67 | `ORD_ALLOW_PICK_SUB_FLAG` | Ord_Allow_Pick_Subessorial Flag | VARCHAR2 | 1 |  | Y |
| 68 | `ORD_ALLOW_OVER_PICK_FLAG` | Ord_Allow_Over_Pickessorial Flag | VARCHAR2 | 1 |  | Y |
| 69 | `ORD_SHIP_PALL_WGT` | Ord_Ship_Pallessorial Wgt | NUMBER | 22 | 16 | Y |
| 70 | `WGT_MEAS_CODE_PALL` | Wgt_Meas_Codeessorial Pall | VARCHAR2 | 4 |  | Y |
| 71 | `PARCEL_CARR_ACC_NUM` | Parcel_Carr_Accessorial Num | VARCHAR2 | 20 |  | Y |
| 72 | `ORD_VICS_BOL_NUM` | Ord_Vics_Bolessorial Num | VARCHAR2 | 20 |  | Y |
| 73 | `ORD_VICS_BOL_NUM_LOAD` | Ord_Vics_Bol_Numessorial Load | VARCHAR2 | 20 |  | Y |
| 74 | `ORD_VICS_BOL_NUM_STOP` | Ord_Vics_Bol_Numessorial Stop | VARCHAR2 | 20 |  | Y |
| 75 | `ORD_SHIP_NUM_EXT_REF` | Ord_Ship_Num_Extessorial Ref | VARCHAR2 | 20 |  | Y |
| 76 | `ITEM_LOC_PROF_CODE` | Item_Loc_Professorial Code | VARCHAR2 | 4 |  | Y |
| 77 | `ORD_FRT_EST_AMT` | Ord_Frt_Estessorial Amt | NUMBER | 22 | 16 | Y |
| 78 | `BAT_NUM_PRO_FORMA` | Bat_Num_Proessorial Forma | NUMBER | 22 | 9 | Y |
| 79 | `ORD_A1INSPECTION_STAT_MES` | Ord_A1Inspection_Statessorial Mes | VARCHAR2 | 100 |  | Y |
| 80 | `SHIP_LANE_CODE` | Ship_Laneessorial Code | VARCHAR2 | 4 |  | Y |
| 81 | `ORD_PACK_DOC_CODE` | Ord_Pack_Docessorial Code | VARCHAR2 | 4 |  | Y |
| 82 | `ORD_ALLOW_STAGE_STOR_LOC` | Ord_Allow_Stage_Storessorial Loc | VARCHAR2 | 1 |  | Y |
| 83 | `ORD_CART_NOT_MIX_ITEM` | Ord_Cart_Not_Mixessorial Item | VARCHAR2 | 1 |  | Y |
| 84 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 85 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 86 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 87 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 88 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 89 | `ORD_LABEL_PRT_FLAG` | Ord_Label_Prtessorial Flag | VARCHAR2 | 1 |  | Y |
| 90 | `ORD_CANCEL_FLAG` | Ord_Cancelessorial Flag | VARCHAR2 | 1 |  | Y |
| 91 | `ORD_SOFT_CONF_FLAG` | Ord_Soft_Confessorial Flag | VARCHAR2 | 1 |  | Y |

## `E_ORD_PACK_D`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 13
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 3 | `ORD_PACK_NUM` | Ord_Packessorial Num | NUMBER | 22 | 9 | N |
| 4 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |
| 5 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 6 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | Y |
| 7 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | Y |
| 8 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | Y |
| 9 | `INVT_LEV5` | Inventory Level 5 | VARCHAR2 | 40 |  | Y |
| 10 | `ORD_PACK_ENT_QTY` | Ord_Pack_Entessorial Qty | VARCHAR2 | 20 |  | Y |
| 11 | `ORD_PACK_QTY` | Ord_Packessorial Qty | NUMBER | 22 | 9 | Y |
| 12 | `ITEM_SET_CODE` | Item_Setessorial Code | VARCHAR2 | 20 |  | Y |
| 13 | `ITEM_SET_QTY` | Item_Setessorial Qty | NUMBER | 22 | 9 | Y |

## `E_ORD_PACK_H`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 30
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 3 | `ORD_PACK_NUM` | Ord_Packessorial Num | NUMBER | 22 | 9 | N |
| 4 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 5 | `CON_CODE` | Consignee Code | VARCHAR2 | 10 |  | N |
| 6 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | N |
| 7 | `ORD_PACK_WAYBILL_NUM` | Ord_Pack_Waybillessorial Num | VARCHAR2 | 40 |  | Y |
| 8 | `ORD_PACK_WGT` | Ord_Packessorial Wgt | NUMBER | 22 | 16 | Y |
| 9 | `ORD_PACK_CUBE_CODE` | Ord_Pack_Cubeessorial Code | VARCHAR2 | 4 |  | Y |
| 10 | `ORD_PACK_UNIT` | Ord_Packessorial Unit | NUMBER | 22 | 9 | Y |
| 11 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 12 | `ORD_PACK_FULL_FLAG` | Ord_Pack_Fullessorial Flag | VARCHAR2 | 1 |  | Y |
| 13 | `ORD_PACK_STR_VALUE` | Ord_Pack_Stressorial Value | VARCHAR2 | 250 |  | Y |
| 14 | `ORD_PACK_STN` | Ord_Packessorial Stn | VARCHAR2 | 10 |  | Y |
| 15 | `ORD_PACK_REF_NUM1` | Ord_Pack_Refessorial Num1 | VARCHAR2 | 20 |  | Y |
| 16 | `ORD_PACK_REF_NUM2` | Ord_Pack_Refessorial Num2 | VARCHAR2 | 20 |  | Y |
| 17 | `ORD_PACK_FILE_LABEL` | Ord_Pack_Fileessorial Label | VARCHAR2 | 20 |  | Y |
| 18 | `ORD_PACK_FILE_COD_LABEL` | Ord_Pack_File_Codessorial Label | VARCHAR2 | 20 |  | Y |
| 19 | `ORD_PACK_FILE_DIR` | Ord_Pack_Fileessorial Dir | VARCHAR2 | 60 |  | Y |
| 20 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | Y |
| 21 | `ERR_CODE` | Error Code | VARCHAR2 | 6 |  | Y |
| 22 | `ERR_TEXT` | Error Text | VARCHAR2 | 100 |  | Y |
| 23 | `LOAD_NUM` | Load Number | NUMBER | 22 | 6 | Y |
| 24 | `WAVE_SEQ_NUM` | Wave_Seqessorial Num | NUMBER | 22 | 9 | Y |
| 25 | `POD_DATE` | Podessorial Date | DATE | 7 |  | Y |
| 26 | `POD_NAME` | Podessorial Name | VARCHAR2 | 40 |  | Y |
| 27 | `ORD_PACK_FRT_AMT` | Ord_Pack_Frtessorial Amt | NUMBER | 22 | 9 | Y |
| 28 | `ORD_PACK_COD_AMT` | Ord_Pack_Codessorial Amt | NUMBER | 22 | 9 | Y |
| 29 | `ORD_PACK_PRICE_AMT` | Ord_Pack_Priceessorial Amt | NUMBER | 22 | 9 | Y |
| 30 | `ORD_PACK_EDI_SEND_FLAG` | Ord_Pack_Edi_Sendessorial Flag | VARCHAR2 | 1 |  | Y |

## `E_ORD_PACK_LABEL`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 25
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM, LOC_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4, SKU_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 3 | `ORD_PACK_LABEL_ID` | Ord_Pack_Labelessorial Id | VARCHAR2 | 30 |  | N |
| 4 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |
| 5 | `ORD_LOC_LINE_NUM` | Ord_Loc_Lineessorial Num | NUMBER | 22 | 4 | N |
| 6 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 7 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | N |
| 8 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 9 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 10 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | Y |
| 11 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | Y |
| 12 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | Y |
| 13 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | Y |
| 14 | `ORD_PACK_LABEL_QTY` | Ord_Pack_Labelessorial Qty | NUMBER | 22 | 9 | N |
| 15 | `SKU_CODE` | SKU Code | VARCHAR2 | 4 |  | N |
| 16 | `WAVE_NUM` | Waveessorial Num | NUMBER | 22 | 6 | Y |
| 17 | `PACK_STN_CODE` | Pack_Stnessorial Code | VARCHAR2 | 4 |  | Y |
| 18 | `SORT_SEQ_NUM` | Sort_Seqessorial Num | NUMBER | 22 | 6 | Y |
| 19 | `ORD_PACK_NUM` | Ord_Packessorial Num | NUMBER | 22 | 9 | Y |
| 20 | `EXT_REF_NUM1` | Ext_Refessorial Num1 | VARCHAR2 | 20 |  | Y |
| 21 | `ORD_PACK_PICK_FLAG` | Ord_Pack_Pickessorial Flag | VARCHAR2 | 1 |  | Y |
| 22 | `ORD_PACK_LABEL_DATA` | Ord_Pack_Labelessorial Data | CLOB | 4000 |  | Y |
| 23 | `RATE_NUM` | Rateessorial Num | NUMBER | 22 | 9 | Y |
| 24 | `CART_ID` | Cart ID | VARCHAR2 | 40 |  | Y |
| 25 | `OPID_PROS_VALUE` | Opid_Prosessorial Value | VARCHAR2 | 250 |  | Y |

## `E_ORD_PEND_ORG`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 18
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 3 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |
| 4 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 5 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 6 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | N |
| 7 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | N |
| 8 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | N |
| 9 | `INVT_LEV5` | Inventory Level 5 | VARCHAR2 | 40 |  | Y |
| 10 | `ORD_PEND_QTY` | Ord_Pendessorial Qty | NUMBER | 22 | 9 | N |
| 11 | `ORD_PEND_WGT` | Ord_Pendessorial Wgt | NUMBER | 22 | 16 | N |
| 12 | `ORD_PEND_CUBE` | Ord_Pendessorial Cube | NUMBER | 22 | 16 | N |
| 13 | `ORD_LINE_TP` | Order Line Type | VARCHAR2 | 1 |  | Y |
| 14 | `WAVE_SEQ_NUM` | Wave_Seqessorial Num | NUMBER | 22 | 9 | Y |
| 15 | `PACK_STN_CODE` | Pack_Stnessorial Code | VARCHAR2 | 4 |  | Y |
| 16 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |
| 17 | `HOLD_RENW_FLAG` | Hold_Renwessorial Flag | VARCHAR2 | 1 |  | Y |
| 18 | `CREATE_DATE` | Create Date | DATE | 7 |  | N |

## `E_ORD_POD`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 6
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 3 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |
| 4 | `ORD_POD_ENT_QTY` | Ord_Pod_Entessorial Qty | VARCHAR2 | 20 |  | Y |
| 5 | `ORD_POD_QTY` | Ord_Podessorial Qty | NUMBER | 22 | 9 | Y |
| 6 | `ORD_POD_UPD_FLAG` | Ord_Pod_Updessorial Flag | VARCHAR2 | 1 |  | Y |

## `E_ORD_QRS_D`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 8
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 3 | `QRS_NUM` | Qrsessorial Num | NUMBER | 22 | 9 | N |
| 4 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 5 | `QRS_UNIT` | Qrsessorial Unit | NUMBER | 22 | 9 | N |
| 6 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | Y |
| 7 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | Y |
| 8 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | Y |

## `E_ORD_QRS_H`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 13
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 3 | `QRS_PREX` | Qrsessorial Prex | VARCHAR2 | 2 |  | N |
| 4 | `QRS_TP` | Qrsessorial Tp | NUMBER | 22 | 1 | N |
| 5 | `QRS_MEMB_NUM` | Qrs_Membessorial Num | VARCHAR2 | 7 |  | N |
| 6 | `QRS_NUM` | Qrsessorial Num | NUMBER | 22 | 9 | N |
| 7 | `QRS_NUM_CHK_DIG` | Qrs_Num_Chkessorial Dig | NUMBER | 22 | 1 | N |
| 8 | `EXT_REF_NUM1` | Ext_Refessorial Num1 | VARCHAR2 | 20 |  | Y |
| 9 | `QRS_PRT_FLAG` | Qrs_Prtessorial Flag | VARCHAR2 | 1 |  | Y |
| 10 | `QRS_SCAN_FLAG` | Qrs_Scanessorial Flag | VARCHAR2 | 1 |  | Y |
| 11 | `QRS_NUM_LAY` | Qrs_Numessorial Lay | NUMBER | 22 | 3 | Y |
| 12 | `QRS_QTY_PER_LAY` | Qrs_Qty_Peressorial Lay | NUMBER | 22 | 3 | Y |
| 13 | `QRS_QTY_ODD_LAY` | Qrs_Qty_Oddessorial Lay | NUMBER | 22 | 3 | Y |

## `E_ORD_VIRT_D`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 8
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 3 | `COMP_CODE_VIRT` | Comp_Codeessorial Virt | VARCHAR2 | 2 |  | N |
| 4 | `ORD_NUM_VIRT` | Ord_Numessorial Virt | NUMBER | 22 | 9 | N |
| 5 | `ORD_LINE_NUM_VIRT` | Ord_Line_Numessorial Virt | NUMBER | 22 | 4 | N |
| 6 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |
| 7 | `ORD_ASSIGN_ENT_QTY` | Ord_Assign_Entessorial Qty | VARCHAR2 | 20 |  | N |
| 8 | `ORD_ASSIGN_QTY` | Ord_Assignessorial Qty | NUMBER | 22 | 9 | N |

## `E_ORD_VIRT_H`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 9
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 3 | `COMP_CODE_VIRT` | Comp_Codeessorial Virt | VARCHAR2 | 2 |  | N |
| 4 | `ORD_NUM_VIRT` | Ord_Numessorial Virt | NUMBER | 22 | 9 | N |
| 5 | `ORD_LINE_NUM_VIRT` | Ord_Line_Numessorial Virt | NUMBER | 22 | 4 | N |
| 6 | `INVT_LEV1_VIRT` | Invt_Lev1essorial Virt | VARCHAR2 | 40 |  | N |
| 7 | `HOLD_CODE_VIRT` | Hold_Codeessorial Virt | VARCHAR2 | 4 |  | N |
| 8 | `ORD_SHIP_ENT_QTY_VIRT` | Ord_Ship_Ent_Qtyessorial Virt | VARCHAR2 | 20 |  | N |
| 9 | `ORD_SHIP_QTY_VIRT` | Ord_Ship_Qtyessorial Virt | NUMBER | 22 | 9 | N |

## `E_PROS_ORD`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 9
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 3 | `ORD_PROS_FLAG` | Ord_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 4 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 5 | `ORD_PRTY_NUM` | Ord_Prtyessorial Num | NUMBER | 22 | 1 | N |
| 6 | `ORD_PROS_DATE` | Ord_Prosessorial Date | DATE | 7 |  | Y |
| 7 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | Y |
| 8 | `ORD_PROS_SEQ_NUM` | Ord_Pros_Seqessorial Num | NUMBER | 22 | 4 | Y |
| 9 | `ORD_SORT_CODE` | Ord_Sortessorial Code | VARCHAR2 | 20 |  | Y |

## `E_PROS_ORD_LINE`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 3 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |
| 4 | `ORD_PROS_FLAG` | Ord_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 6 | `ORD_PRTY_NUM` | Ord_Prtyessorial Num | NUMBER | 22 | 1 | N |
| 7 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | Y |
| 8 | `ORD_SORT_CODE` | Ord_Sortessorial Code | VARCHAR2 | 20 |  | Y |
| 9 | `ORD_LINE_ACPT_REF_VALUE` | Ord_Line_Acpt_Refessorial Value | VARCHAR2 | 20 |  | Y |
| 10 | `ORD_PROS_LINE_PROS_STAT` | Ord_Pros_Line_Prosessorial Stat | VARCHAR2 | 4 |  | Y |

## `E_PROS_ORD_LOC_LINE`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 3 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |
| 4 | `ORD_LOC_LINE_NUM` | Ord_Loc_Lineessorial Num | NUMBER | 22 | 4 | N |
| 5 | `ORD_PROS_FLAG` | Ord_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 6 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 7 | `ORD_PRTY_NUM` | Ord_Prtyessorial Num | NUMBER | 22 | 1 | N |
| 8 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | Y |
| 9 | `ORD_SORT_CODE` | Ord_Sortessorial Code | VARCHAR2 | 20 |  | Y |
| 10 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |

## `E_PROS_PO`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 6
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `PO_NUM` | PO Number | NUMBER | 22 | 9 | N |
| 3 | `PO_PROS_FLAG` | Po_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 4 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 5 | `PO_PROS_DATE` | Po_Prosessorial Date | DATE | 7 |  | Y |
| 6 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | Y |

## `E_PROS_RF_DEVICE`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 2 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 3 | `RF_DEVICE_CODE` | Rf_Deviceessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |

## `E_PROS_TASK_PEND`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 16
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `ASS_DATE` | Assessorial Date | DATE | 7 |  | N |
| 3 | `ASS_NUM` | Assessorial Num | NUMBER | 22 | 9 | Y |
| 4 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | Y |
| 5 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | Y |
| 6 | `LOC_AISLE_FROM` | Loc_Aisleessorial From | VARCHAR2 | 12 |  | Y |
| 7 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | Y |
| 8 | `DOC_TP_FLAG` | Doc_Tpessorial Flag | VARCHAR2 | 1 |  | Y |
| 9 | `DOC_NUM` | Document Number | NUMBER | 22 | 9 | Y |
| 10 | `DOC_LINE_NUM` | Document Line Number | NUMBER | 22 | 9 | Y |
| 11 | `DOC_LOC_LINE_NUM` | Document Location Line Number | NUMBER | 22 | 4 | Y |
| 12 | `WHSE_CODE_FROM` | Whse_Codeessorial From | VARCHAR2 | 4 |  | Y |
| 13 | `LOC_CODE_FROM` | Loc_Codeessorial From | VARCHAR2 | 12 |  | Y |
| 14 | `WHSE_ACT_TP_NUM` | Whse_Act_Tpessorial Num | NUMBER | 22 | 2 | Y |
| 15 | `PICK_METH` | Pickessorial Meth | VARCHAR2 | 4 |  | Y |
| 16 | `CART_ID` | Cart ID | VARCHAR2 | 40 |  | Y |

## `E_PROS_TRSPT_UNIT`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 6
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `TRSPT_EQP_OWN_CODE` | Trspt_Eqp_Ownessorial Code | VARCHAR2 | 10 |  | N |
| 3 | `TRSPT_UNIT_ID` | Trspt_Unitessorial Id | VARCHAR2 | 20 |  | N |
| 4 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 5 | `TRSPT_UNIT_SORT_CODE` | Trspt_Unit_Sortessorial Code | VARCHAR2 | 20 |  | Y |
| 6 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | Y |

## `E_PROS_WHSE_LOC_ATTR`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 6
- **Campos-chave prováveis:** COMP_CODE, LOC_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 3 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | N |
| 4 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 5 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | Y |
| 6 | `MHE_TP_CODE` | Mhe_Tpessorial Code | VARCHAR2 | 4 |  | Y |

## `E_REPI_LOCK`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 8
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 4 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |
| 5 | `ORD_LOC_LINE_NUM` | Ord_Loc_Lineessorial Num | NUMBER | 22 | 4 | N |
| 6 | `WHSE_CODE_FROM` | Whse_Codeessorial From | VARCHAR2 | 4 |  | N |
| 7 | `LOC_CODE_FROM` | Loc_Codeessorial From | VARCHAR2 | 12 |  | N |
| 8 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |

## `E_SAND_ORD_D`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 13
- **Campos-chave prováveis:** INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4, LOC_CODE, HOLD_CODE, SKU_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SAND_ORD_SEQ_NUM` | Sand_Ord_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `SAND_ORD_LINE_NUM` | Sand_Ord_Lineessorial Num | NUMBER | 22 | 4 | N |
| 3 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | Y |
| 4 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | Y |
| 5 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | Y |
| 6 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | Y |
| 7 | `SAND_ORD_QTY` | Sand_Ordessorial Qty | NUMBER | 22 | 9 | Y |
| 8 | `SAND_ORD_UNIT` | Sand_Ordessorial Unit | NUMBER | 22 | 9 | Y |
| 9 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 10 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | Y |
| 11 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |
| 12 | `SKU_CODE` | SKU Code | VARCHAR2 | 4 |  | Y |
| 13 | `SAND_REM_TEXT` | Sand_Remessorial Text | VARCHAR2 | 2000 |  | Y |

## `E_SAND_ORD_H`

- **Tipo:** Transactional
- **Categoria:** Orders
- **Campos:** 31
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `SAND_ORD_SEQ_NUM` | Sand_Ord_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `CON_CODE` | Consignee Code | VARCHAR2 | 10 |  | Y |
| 5 | `CON_NAME` | Consignee Name | VARCHAR2 | 30 |  | Y |
| 6 | `CON_ADD1_MAN` | Con_Add1essorial Man | VARCHAR2 | 30 |  | Y |
| 7 | `CON_ADD2_MAN` | Con_Add2essorial Man | VARCHAR2 | 30 |  | Y |
| 8 | `CON_ADD3_MAN` | Con_Add3essorial Man | VARCHAR2 | 30 |  | Y |
| 9 | `CON_ZIP_CODE_MAN` | Con_Zip_Codeessorial Man | VARCHAR2 | 10 |  | Y |
| 10 | `CON_ZIP_CITY_MAN` | Con_Zip_Cityessorial Man | VARCHAR2 | 30 |  | Y |
| 11 | `CON_STATE_CODE_MAN` | Con_State_Codeessorial Man | VARCHAR2 | 4 |  | Y |
| 12 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | Y |
| 13 | `CARR_NAME` | Carrier Name | VARCHAR2 | 30 |  | Y |
| 14 | `SAND_CUST_ORD_NUM` | Sand_Cust_Ordessorial Num | VARCHAR2 | 20 |  | N |
| 15 | `SAND_ORD_DATE` | Sand_Ordessorial Date | DATE | 7 |  | N |
| 16 | `SAND_ORD_TO_SHIP_DATE` | Sand_Ord_To_Shipessorial Date | DATE | 7 |  | Y |
| 17 | `SAND_ORD_LINE_CNT` | Sand_Ord_Lineessorial Cnt | NUMBER | 22 | 3 | N |
| 18 | `WHSE_CODE_DEF` | Whse_Codeessorial Def | VARCHAR2 | 4 |  | Y |
| 19 | `LOC_CODE_DEF` | Loc_Codeessorial Def | VARCHAR2 | 12 |  | Y |
| 20 | `SKU_CODE_DEF` | Sku_Codeessorial Def | VARCHAR2 | 4 |  | Y |
| 21 | `INVT_LEV1_DEF` | Invt_Lev1essorial Def | VARCHAR2 | 40 |  | Y |
| 22 | `INVT_LEV2_DEF` | Invt_Lev2essorial Def | VARCHAR2 | 40 |  | Y |
| 23 | `INVT_LEV3_DEF` | Invt_Lev3essorial Def | VARCHAR2 | 40 |  | Y |
| 24 | `INVT_LEV4_DEF` | Invt_Lev4essorial Def | VARCHAR2 | 40 |  | Y |
| 25 | `SAND_ORD_TOT_UNIT` | Sand_Ord_Totessorial Unit | NUMBER | 22 | 9 | Y |
| 26 | `SAND_REM_TEXT` | Sand_Remessorial Text | VARCHAR2 | 2000 |  | Y |
| 27 | `SAND_ORD_TO_ARR_DATE` | Sand_Ord_To_Arressorial Date | DATE | 7 |  | Y |
| 28 | `SAND_ORD_PRTY_NUM` | Sand_Ord_Prtyessorial Num | NUMBER | 22 | 1 | Y |
| 29 | `SAND_ORD_PO_NUM` | Sand_Ord_Poessorial Num | VARCHAR2 | 20 |  | Y |
| 30 | `SAND_ORD_ALT_REF2` | Sand_Ord_Altessorial Ref2 | VARCHAR2 | 20 |  | Y |
| 31 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |

## `H_ASS_TASK`

- **Tipo:** Historical
- **Categoria:** Orders
- **Campos:** 30
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM, CUST_CODE, INVT_LEV1, LOC_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 3 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |
| 4 | `ORD_LOC_LINE_NUM` | Ord_Loc_Lineessorial Num | NUMBER | 22 | 4 | N |
| 5 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 6 | `ASS_NUM` | Assessorial Num | NUMBER | 22 | 9 | N |
| 7 | `ORD_TOT_WGT` | Ord_Totessorial Wgt | NUMBER | 22 | 16 | N |
| 8 | `ORD_TOT_CUBE` | Ord_Totessorial Cube | NUMBER | 22 | 16 | N |
| 9 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 10 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 11 | `CREATE_DATE` | Create Date | DATE | 7 |  | N |
| 12 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 9 | N |
| 13 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | N |
| 14 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 15 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | N |
| 16 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | N |
| 17 | `ORD_LOC_ENT_QTY` | Ord_Loc_Entessorial Qty | VARCHAR2 | 20 |  | N |
| 18 | `ORD_LOC_QTY` | Ord_Locessorial Qty | NUMBER | 22 | 9 | N |
| 19 | `CART_ID` | Cart ID | VARCHAR2 | 40 |  | Y |
| 20 | `ASS_SKIP_FLAG` | Ass_Skipessorial Flag | VARCHAR2 | 1 |  | Y |
| 21 | `LOAD_NUM` | Load Number | NUMBER | 22 | 6 | Y |
| 22 | `STOP_NUM` | Stop Number | NUMBER | 22 | 4 | Y |
| 23 | `BILL_DELV_GRP_ORD_NUM` | Bill_Delv_Grp_Ordessorial Num | NUMBER | 22 | 9 | Y |
| 24 | `REGION_CODE` | Region Code | VARCHAR2 | 20 |  | Y |
| 25 | `AUDIT_MESSAGE` | Auditessorial Message | VARCHAR2 | 500 |  | Y |
| 26 | `NOT_INCLUDED_IN_ASS_FLAG` | Not_Included_In_Assessorial Flag | VARCHAR2 | 1 |  | Y |
| 27 | `CP_FROM_C_TO_H_ASS_TASK_DATE` | Cp_From_C_To_H_Ass_Taskessorial Date | DATE | 7 |  | Y |
| 28 | `TER_CODE_DEL` | Ter_Codeessorial Del | VARCHAR2 | 10 |  | Y |
| 29 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | Y |
| 30 | `RELO_SEQ_NUM` | Relo_Seqessorial Num | NUMBER | 22 | 9 | Y |

## `H_LOAD_ORD_REL`

- **Tipo:** Historical
- **Categoria:** Orders
- **Campos:** 15
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `LOAD_ORD_REL_FUN_CODE` | Load_Ord_Rel_Funessorial Code | VARCHAR2 | 4 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `FRT_TER_CODE_LOAD` | Frt_Ter_Codeessorial Load | VARCHAR2 | 4 |  | N |
| 4 | `LOAD_NUM` | Load Number | NUMBER | 22 | 6 | N |
| 5 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | N |
| 6 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 7 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | Y |
| 8 | `STOP_NUM` | Stop Number | NUMBER | 22 | 4 | Y |
| 9 | `BILL_GRP_ORD_NUM` | Bill Group Order Number | VARCHAR2 | 8 |  | Y |
| 10 | `DELV_GRP_ORD_NUM` | Delv_Grp_Ordessorial Num | VARCHAR2 | 8 |  | Y |
| 11 | `LOAD_ORD_REL_PICK_DATE_TIME` | Load_Ord_Rel_Pick_Dateessorial Time | DATE | 7 |  | Y |
| 12 | `LOAD_ORD_REL_RQST_DATE_TIME` | Load_Ord_Rel_Rqst_Dateessorial Time | DATE | 7 |  | Y |
| 13 | `COMP_CODE_ACTUAL` | Comp_Codeessorial Actual | VARCHAR2 | 2 |  | N |
| 14 | `BACKUP_DATE` | Backupessorial Date | DATE | 7 |  | Y |
| 15 | `DP300_DELETE_DATE` | Dp300_Deleteessorial Date | DATE | 7 |  | Y |

## `H_MAN_ORD`

- **Tipo:** Historical
- **Categoria:** Orders
- **Campos:** 9
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM, CUST_CODE, INVT_LEV1

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 4 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |
| 5 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 6 | `ORD_LINE_TP` | Order Line Type | VARCHAR2 | 1 |  | N |
| 7 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 8 | `ORD_ENT_QTY` | Ord_Entessorial Qty | VARCHAR2 | 20 |  | N |
| 9 | `ORD_QTY` | Ordessorial Qty | NUMBER | 22 | 9 | N |

## `H_ORD_D1`

- **Tipo:** Historical
- **Categoria:** Orders
- **Campos:** 15
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 5 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |
| 6 | `CUST_CODE_CHG` | Cust_Codeessorial Chg | VARCHAR2 | 10 |  | Y |
| 7 | `CHG_CODE` | Charge Code | VARCHAR2 | 6 |  | Y |
| 8 | `CHG_DATE` | Charge Date | DATE | 7 |  | Y |
| 9 | `ORD_REM_LINE_NUM` | Ord_Rem_Lineessorial Num | NUMBER | 22 | 3 | N |
| 10 | `ORD_REM_LINE_TEXT` | Ord_Rem_Lineessorial Text | VARCHAR2 | 45 |  | Y |
| 11 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 12 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 13 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 14 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 15 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `H_ORD_D10`

- **Tipo:** Historical
- **Categoria:** Orders
- **Campos:** 21
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 5 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |
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

## `H_ORD_D11`

- **Tipo:** Historical
- **Categoria:** Orders
- **Campos:** 19
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 5 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |
| 6 | `ORD_KIT_LINE_NUM` | Ord_Kit_Lineessorial Num | NUMBER | 22 | 4 | N |
| 7 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 8 | `ORD_KIT_INVT_LEV1` | Ord_Kit_Invtessorial Lev1 | VARCHAR2 | 40 |  | N |
| 9 | `ORD_COMPN_INVT_LEV1` | Ord_Compn_Invtessorial Lev1 | VARCHAR2 | 40 |  | N |
| 10 | `ITEM_COMPN_QTY` | Item_Compnessorial Qty | NUMBER | 22 | 16 | Y |
| 11 | `ITEM_COMPN_WGT` | Item_Compnessorial Wgt | NUMBER | 22 | 16 | Y |
| 12 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | Y |
| 13 | `CUST_CODE_COMPN` | Cust_Codeessorial Compn | VARCHAR2 | 10 |  | N |
| 14 | `ITEM_COMPN_PER_KIT_QTY` | Item_Compn_Per_Kitessorial Qty | NUMBER | 22 | 9 | Y |
| 15 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 16 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 17 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 18 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 19 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `H_ORD_D12`

- **Tipo:** Historical
- **Categoria:** Orders
- **Campos:** 18
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | N |
| 3 | `ORD_REM_SEQ_NUM` | Ord_Rem_Seqessorial Num | NUMBER | 22 | 9 | N |
| 4 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 5 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 6 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |
| 7 | `ORD_REM_CUST_FLAG` | Ord_Rem_Custessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `ORD_REM_CON_FLAG` | Ord_Rem_Conessorial Flag | VARCHAR2 | 1 |  | N |
| 9 | `ORD_REM_CARR_FLAG` | Ord_Rem_Carressorial Flag | VARCHAR2 | 1 |  | N |
| 10 | `ORD_REM_RF_FLAG` | Ord_Rem_Rfessorial Flag | VARCHAR2 | 1 |  | N |
| 11 | `ORD_DOC_CODE_REST` | Ord_Doc_Codeessorial Rest | VARCHAR2 | 4 |  | Y |
| 12 | `ORD_REM_MES_CODE` | Ord_Rem_Mesessorial Code | VARCHAR2 | 4 |  | Y |
| 13 | `ORD_REM_TEXT` | Ord_Remessorial Text | VARCHAR2 | 2000 |  | Y |
| 14 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 15 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 16 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 17 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 18 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `H_ORD_D2`

- **Tipo:** Historical
- **Categoria:** Orders
- **Campos:** 26
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 5 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |
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
| 16 | `ORD_EXTRA_CHG_QTY` | Ord_Extra_Chgessorial Qty | NUMBER | 22 | 16 | Y |
| 17 | `ORD_EXTRA_CHG_PROS_FLAG` | Ord_Extra_Chg_Prosessorial Flag | VARCHAR2 | 1 |  | Y |
| 18 | `ORD_EXTRA_CHG_ACCEPT_FLAG` | Ord_Extra_Chg_Acceptessorial Flag | VARCHAR2 | 1 |  | Y |
| 19 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | Y |
| 20 | `ORD_EXTRA_CHG_LAST_DATE` | Ord_Extra_Chg_Lastessorial Date | DATE | 7 |  | Y |
| 21 | `PRO_FORMA_PROS_FLAG` | Pro_Forma_Prosessorial Flag | VARCHAR2 | 1 |  | Y |
| 22 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 23 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 24 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 25 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 26 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `H_ORD_D3`

- **Tipo:** Historical
- **Categoria:** Orders
- **Campos:** 50
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 5 | `DRV_CODE` | Driver Code | VARCHAR2 | 4 |  | Y |
| 6 | `ORD_POW_UNIT_NUM` | Ord_Pow_Unitessorial Num | VARCHAR2 | 20 |  | Y |
| 7 | `ORD_CARRY_UNIT_NUM` | Ord_Carry_Unitessorial Num | VARCHAR2 | 20 |  | Y |
| 8 | `ORD_VES` | Ordessorial Ves | VARCHAR2 | 20 |  | Y |
| 9 | `ORD_VOY` | Ordessorial Voy | VARCHAR2 | 20 |  | Y |
| 10 | `ORD_SEAL1` | Ordessorial Seal1 | VARCHAR2 | 20 |  | Y |
| 11 | `ORD_SEAL2` | Ordessorial Seal2 | VARCHAR2 | 20 |  | Y |
| 12 | `ORD_TEMP_FRONT` | Ord_Tempessorial Front | VARCHAR2 | 10 |  | Y |
| 13 | `ORD_TEMP_MID` | Ord_Tempessorial Mid | VARCHAR2 | 10 |  | Y |
| 14 | `ORD_TEMP_BACK` | Ord_Tempessorial Back | VARCHAR2 | 10 |  | Y |
| 15 | `DRV_NAME_MAN` | Drv_Nameessorial Man | VARCHAR2 | 30 |  | Y |
| 16 | `ORD_TEMP_SET` | Ord_Tempessorial Set | VARCHAR2 | 10 |  | Y |
| 17 | `ORD_TEMP_AMB` | Ord_Tempessorial Amb | VARCHAR2 | 10 |  | Y |
| 18 | `ORD_SEAL1_INTACT` | Ord_Seal1essorial Intact | VARCHAR2 | 1 |  | Y |
| 19 | `ORD_PALL_QTY_IN` | Ord_Pall_Qtyessorial In | NUMBER | 22 | 4 | Y |
| 20 | `ORD_PALL_QTY_OUT` | Ord_Pall_Qtyessorial Out | NUMBER | 22 | 4 | Y |
| 21 | `ORD_TEMP_6` | Ord_Tempessorial 6 | VARCHAR2 | 10 |  | Y |
| 22 | `ORD_BILLTO_TEL_NUM` | Ord_Billto_Telessorial Num | VARCHAR2 | 20 |  | Y |
| 23 | `ORD_BILLTO_EMAIL_ADD` | Ord_Billto_Emailessorial Add | VARCHAR2 | 250 |  | Y |
| 24 | `ORD_CON_TEL_NUM` | Ord_Con_Telessorial Num | VARCHAR2 | 20 |  | Y |
| 25 | `ORD_CON_EMAIL_ADD` | Ord_Con_Emailessorial Add | VARCHAR2 | 250 |  | Y |
| 26 | `ORD_CON_EIN` | Ord_Conessorial Ein | VARCHAR2 | 20 |  | Y |
| 27 | `ORD_PARCEL_RESIDENTIAL_FLAG` | Ord_Parcel_Residentialessorial Flag | VARCHAR2 | 1 |  | Y |
| 28 | `ORD_PARCEL_SIGNATURE_REQ_TP` | Ord_Parcel_Signature_Reqessorial Tp | VARCHAR2 | 1 |  | Y |
| 29 | `ORD_PARCEL_DELV_CONF` | Ord_Parcel_Delvessorial Conf | VARCHAR2 | 1 |  | Y |
| 30 | `ORD_PARCEL_SATURDAY` | Ord_Parcelessorial Saturday | VARCHAR2 | 1 |  | Y |
| 31 | `ORD_PARCEL_INS_FLAG` | Ord_Parcel_Insessorial Flag | VARCHAR2 | 1 |  | Y |
| 32 | `ORD_PARCEL_INS_CHG_AMT` | Ord_Parcel_Ins_Chgessorial Amt | NUMBER | 22 | 15 | Y |
| 33 | `ORD_PARCEL_INS_DECLARE_AMT` | Ord_Parcel_Ins_Declareessorial Amt | NUMBER | 22 | 15 | Y |
| 34 | `ORD_PARCEL_MES` | Ord_Parcelessorial Mes | VARCHAR2 | 250 |  | Y |
| 35 | `ORD_PARCEL_SHIP_REF1` | Ord_Parcel_Shipessorial Ref1 | VARCHAR2 | 40 |  | Y |
| 36 | `ORD_PARCEL_SHIP_REF2` | Ord_Parcel_Shipessorial Ref2 | VARCHAR2 | 40 |  | Y |
| 37 | `ORD_PARCEL_SHIP_REF3` | Ord_Parcel_Shipessorial Ref3 | VARCHAR2 | 40 |  | Y |
| 38 | `ORD_PARCEL_SHIP_REF4` | Ord_Parcel_Shipessorial Ref4 | VARCHAR2 | 40 |  | Y |
| 39 | `ORD_PARCEL_SHIP_REF5` | Ord_Parcel_Shipessorial Ref5 | VARCHAR2 | 40 |  | Y |
| 40 | `ORD_PARCEL_COD_METH_PAY` | Ord_Parcel_Cod_Methessorial Pay | VARCHAR2 | 40 |  | Y |
| 41 | `ORD_PARCEL_INSIDE_DELV_FLAG` | Ord_Parcel_Inside_Delvessorial Flag | VARCHAR2 | 1 |  | Y |
| 42 | `ORD_PARCEL_HOLD_LOC_FLAG` | Ord_Parcel_Hold_Locessorial Flag | VARCHAR2 | 1 |  | Y |
| 43 | `ORD_PARCEL_CALL_TAG_FLAG` | Ord_Parcel_Call_Tagessorial Flag | VARCHAR2 | 1 |  | Y |
| 44 | `ORD_BILLTO_CONTACT_NAME` | Ord_Billto_Contactessorial Name | VARCHAR2 | 30 |  | Y |
| 45 | `ORD_CON_CONTACT_NAME` | Ord_Con_Contactessorial Name | VARCHAR2 | 30 |  | Y |
| 46 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 47 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 48 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 49 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 50 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `H_ORD_D4`

- **Tipo:** Historical
- **Categoria:** Orders
- **Campos:** 15
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
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

## `H_ORD_D5`

- **Tipo:** Historical
- **Categoria:** Orders
- **Campos:** 72
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM, CUST_CODE, SKU_CODE, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 5 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |
| 6 | `ORD_LINE_TP` | Order Line Type | VARCHAR2 | 1 |  | N |
| 7 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 8 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | N |
| 9 | `ORD_ORD_ENT_QTY` | Ord_Ord_Entessorial Qty | VARCHAR2 | 20 |  | N |
| 10 | `ORD_ORD_QTY` | Ord_Ordessorial Qty | NUMBER | 22 | 9 | N |
| 11 | `ORD_SHIP_ENT_QTY` | Ord_Ship_Entessorial Qty | VARCHAR2 | 20 |  | N |
| 12 | `ORD_SHIP_QTY` | Ord_Shipessorial Qty | NUMBER | 22 | 9 | N |
| 13 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | N |
| 14 | `ORD_UNIT_WGT` | Ord_Unitessorial Wgt | NUMBER | 22 | 16 | N |
| 15 | `SKU_CODE` | SKU Code | VARCHAR2 | 4 |  | N |
| 16 | `ORD_TOT_WGT` | Ord_Totessorial Wgt | NUMBER | 22 | 16 | N |
| 17 | `ORD_TOT_WGT_NET` | Ord_Tot_Wgtessorial Net | NUMBER | 22 | 16 | N |
| 18 | `LINEAR_MEAS_CODE` | Linear Measurement Code | VARCHAR2 | 4 |  | N |
| 19 | `ORD_TOT_CUBE` | Ord_Totessorial Cube | NUMBER | 22 | 16 | N |
| 20 | `ORD_LINE_REM_FLAG` | Ord_Line_Remessorial Flag | VARCHAR2 | 1 |  | N |
| 21 | `ORD_LINE_EXTRA_CHG_FLAG` | Ord_Line_Extra_Chgessorial Flag | VARCHAR2 | 1 |  | N |
| 22 | `ORD_LINE_ALTER_FLAG` | Ord_Line_Alteressorial Flag | VARCHAR2 | 1 |  | N |
| 23 | `ORD_LINE_LOC_BAL_FLAG` | Ord_Line_Loc_Balessorial Flag | VARCHAR2 | 1 |  | N |
| 24 | `ORD_LINE_LOC_GEN_FLAG` | Ord_Line_Loc_Genessorial Flag | VARCHAR2 | 1 |  | N |
| 25 | `ORD_LINE_CONF_FLAG` | Ord_Line_Confessorial Flag | VARCHAR2 | 1 |  | N |
| 26 | `ORD_LINE_EDI_INFO_FLAG` | Ord_Line_Edi_Infoessorial Flag | VARCHAR2 | 1 |  | N |
| 27 | `ORD_LINE_ITEM_PROS_FLAG` | Ord_Line_Item_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 28 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |
| 29 | `HOLD_RENW_FLAG` | Hold_Renwessorial Flag | VARCHAR2 | 1 |  | Y |
| 30 | `ORD_LEV1` | Ordessorial Lev1 | VARCHAR2 | 40 |  | Y |
| 31 | `ORD_SEQ_QTY_LEV1` | Ord_Seq_Qtyessorial Lev1 | NUMBER | 22 | 4 | Y |
| 32 | `ORD_LEV2` | Ordessorial Lev2 | VARCHAR2 | 40 |  | Y |
| 33 | `ORD_SEQ_QTY_LEV2` | Ord_Seq_Qtyessorial Lev2 | NUMBER | 22 | 4 | Y |
| 34 | `ORD_LEV3` | Ordessorial Lev3 | VARCHAR2 | 40 |  | Y |
| 35 | `ORD_SEQ_QTY_LEV3` | Ord_Seq_Qtyessorial Lev3 | NUMBER | 22 | 4 | Y |
| 36 | `ORD_LEV4` | Ordessorial Lev4 | VARCHAR2 | 40 |  | Y |
| 37 | `ORD_SEQ_QTY_LEV4` | Ord_Seq_Qtyessorial Lev4 | VARCHAR2 | 4 |  | Y |
| 38 | `ORD_LEV5` | Ordessorial Lev5 | VARCHAR2 | 40 |  | Y |
| 39 | `ORD_SEQ_QTY_LEV5` | Ord_Seq_Qtyessorial Lev5 | VARCHAR2 | 4 |  | Y |
| 40 | `ORD_LINE_CONF_DATE` | Ord_Line_Confessorial Date | DATE | 7 |  | Y |
| 41 | `ORD_LINE_SRCE_LINE` | Ord_Line_Srceessorial Line | NUMBER | 22 | 4 | Y |
| 42 | `ITEM_CODE_SUB` | Item_Codeessorial Sub | VARCHAR2 | 20 |  | Y |
| 43 | `FRT_CLASS_DES` | Frt_Classessorial Des | VARCHAR2 | 30 |  | Y |
| 44 | `ORD_PALL` | Ordessorial Pall | NUMBER | 22 | 11 | Y |
| 45 | `ORD_TL_AMT` | Ord_Tlessorial Amt | NUMBER | 22 | 9 | Y |
| 46 | `REAS_CODE` | Reasessorial Code | VARCHAR2 | 4 |  | Y |
| 47 | `ORD_DIST_RCPT_LINE_NUM` | Ord_Dist_Rcpt_Lineessorial Num | NUMBER | 22 | 4 | Y |
| 48 | `ORD_XDOCK_OVER_QTY` | Ord_Xdock_Overessorial Qty | NUMBER | 22 | 9 | Y |
| 49 | `BOND_NUM` | Bond Number | VARCHAR2 | 20 |  | Y |
| 50 | `ISOL_CODE` | ISOL Code | VARCHAR2 | 4 |  | Y |
| 51 | `ORD_EXT_INV_NUM` | Ord_Ext_Invessorial Num | NUMBER | 22 | 16 | Y |
| 52 | `ORD_EXT_INV_PREX` | Ord_Ext_Invessorial Prex | VARCHAR2 | 4 |  | Y |
| 53 | `ORD_EXT_INV_DATE` | Ord_Ext_Invessorial Date | DATE | 7 |  | Y |
| 54 | `ORD_EXT_INV_SEAL_SERIES` | Ord_Ext_Inv_Sealessorial Series | VARCHAR2 | 3 |  | Y |
| 55 | `ORD_EXT_INV_SEAL_NUM` | Ord_Ext_Inv_Sealessorial Num | NUMBER | 22 | 10 | Y |
| 56 | `ORD_DELV_QTY` | Ord_Delvessorial Qty | NUMBER | 22 | 9 | Y |
| 57 | `ORD_DELV_ENT_QTY` | Ord_Delv_Entessorial Qty | VARCHAR2 | 20 |  | Y |
| 58 | `WHSE_CODE_REST` | Whse_Codeessorial Rest | VARCHAR2 | 4 |  | Y |
| 59 | `ORD_LINE_NUM_UPDOWNSTREAM` | Ord_Line_Numessorial Updownstream | NUMBER | 22 | 4 | Y |
| 60 | `ORD_UNALLOC_PICKLINE_PICK_TP` | Ord_Unalloc_Pickline_Pickessorial Tp | VARCHAR2 | 1 |  | Y |
| 61 | `DYN_DAY_RECALC_INVT_EXPY_DATE` | Dyn_Day_Recalc_Invt_Expyessorial Date | NUMBER | 22 | 3 | Y |
| 62 | `ORD_DIST_RCPT_NUM` | Ord_Dist_Rcptessorial Num | NUMBER | 22 | 9 | Y |
| 63 | `ORD_ALLOC_TIME_OLD_INVT_ACCESS` | Ord_Alloc_Time_Old_Invtessorial Access | VARCHAR2 | 5 |  | Y |
| 64 | `ORD_LINE_PICK_METH` | Ord_Line_Pickessorial Meth | VARCHAR2 | 4 |  | Y |
| 65 | `WHSE_CODE_SUG` | Whse_Codeessorial Sug | VARCHAR2 | 4 |  | Y |
| 66 | `LOC_CODE_SUG` | Loc_Codeessorial Sug | VARCHAR2 | 12 |  | Y |
| 67 | `LAST_PICK_QTY_ON_PLT_FLAG` | Last_Pick_Qty_On_Pltessorial Flag | VARCHAR2 | 1 |  | Y |
| 68 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 69 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 70 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 71 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 72 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `H_ORD_D5D1`

- **Tipo:** Historical
- **Categoria:** Orders
- **Campos:** 37
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM, CUST_CODE, INVT_LEV1, LOC_CODE, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 5 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |
| 6 | `ORD_LOC_LINE_NUM` | Ord_Loc_Lineessorial Num | NUMBER | 22 | 4 | N |
| 7 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 8 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 9 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | N |
| 10 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 11 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | N |
| 12 | `ORD_LOC_ENT_QTY` | Ord_Loc_Entessorial Qty | VARCHAR2 | 20 |  | N |
| 13 | `ORD_LOC_QTY` | Ord_Locessorial Qty | NUMBER | 22 | 9 | N |
| 14 | `ORD_LOC_CNVC_QTY` | Ord_Loc_Cnvcessorial Qty | NUMBER | 22 | 6 | Y |
| 15 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | N |
| 16 | `ORD_LOC_PROS_FLAG` | Ord_Loc_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 17 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |
| 18 | `HOLD_SHIP_FLAG` | Hold_Shipessorial Flag | VARCHAR2 | 1 |  | Y |
| 19 | `HOLD_RENW_FLAG` | Hold_Renwessorial Flag | VARCHAR2 | 1 |  | Y |
| 20 | `WHSE_CODE_ORG` | Whse_Codeessorial Org | VARCHAR2 | 4 |  | Y |
| 21 | `LOC_CODE_ORG` | Loc_Codeessorial Org | VARCHAR2 | 12 |  | Y |
| 22 | `OUTB_PALL_NUM` | Outb_Pallessorial Num | VARCHAR2 | 20 |  | Y |
| 23 | `WHSE_CODE_STATIC` | Whse_Codeessorial Static | VARCHAR2 | 4 |  | Y |
| 24 | `LOC_CODE_STATIC` | Loc_Codeessorial Static | VARCHAR2 | 12 |  | Y |
| 25 | `WHSE_CODE_MOVE` | Whse_Codeessorial Move | VARCHAR2 | 4 |  | Y |
| 26 | `LOC_CODE_MOVE` | Loc_Codeessorial Move | VARCHAR2 | 12 |  | Y |
| 27 | `UNIT_RETAIL_PRICE` | Unit_Retailessorial Price | NUMBER | 22 | 12 | Y |
| 28 | `UNIT_DISC_PRICE` | Unit_Discessorial Price | NUMBER | 22 | 12 | Y |
| 29 | `UNIT_COST` | Unitessorial Cost | NUMBER | 22 | 12 | Y |
| 30 | `WHSE_ACT_TP_NUM` | Whse_Act_Tpessorial Num | NUMBER | 22 | 2 | Y |
| 31 | `ORD_LOC_CASE_PICK_FLAG` | Ord_Loc_Case_Pickessorial Flag | VARCHAR2 | 1 |  | Y |
| 32 | `RELO_SEQ_NUM` | Relo_Seqessorial Num | NUMBER | 22 | 9 | Y |
| 33 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 34 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 35 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 36 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 37 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `H_ORD_D5D2`

- **Tipo:** Historical
- **Categoria:** Orders
- **Campos:** 25
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 5 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |
| 6 | `PROS_CODE` | Prosessorial Code | VARCHAR2 | 4 |  | N |
| 7 | `PROS_LINE_NUM` | Pros_Lineessorial Num | NUMBER | 22 | 6 | N |
| 8 | `PROS_DES` | Prosessorial Des | VARCHAR2 | 30 |  | N |
| 9 | `PROS_TP_CODE` | Pros_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 10 | `PROS_LEN` | Prosessorial Len | VARCHAR2 | 6 |  | N |
| 11 | `COL_TP_CODE` | Col_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 12 | `SKU_CLASS_NUM` | Sku_Classessorial Num | NUMBER | 22 | 1 | N |
| 13 | `PROS_VALUE` | Prosessorial Value | VARCHAR2 | 250 |  | Y |
| 14 | `QRS_NUM` | Qrsessorial Num | VARCHAR2 | 19 |  | Y |
| 15 | `ORD_LOC_LINE_NUM` | Ord_Loc_Lineessorial Num | NUMBER | 22 | 4 | Y |
| 16 | `ORD_PACK_NUM` | Ord_Packessorial Num | NUMBER | 22 | 9 | Y |
| 17 | `ORD_PROS_PRT_FLAG` | Ord_Pros_Prtessorial Flag | VARCHAR2 | 1 |  | Y |
| 18 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | Y |
| 19 | `PROS_REF` | Prosessorial Ref | VARCHAR2 | 250 |  | Y |
| 20 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 21 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 22 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 23 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 24 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 25 | `SORT_VALID_FLAG` | Sort_Validessorial Flag | VARCHAR2 | 1 |  | Y |

## `H_ORD_D5D3`

- **Tipo:** Historical
- **Categoria:** Orders
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 5 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |
| 6 | `DOC_CODE` | Document Code | VARCHAR2 | 4 |  | N |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `H_ORD_D5D4`

- **Tipo:** Historical
- **Categoria:** Orders
- **Campos:** 16
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 5 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |
| 6 | `ORD_SALE_EXT_INV_NUM` | Ord_Sale_Ext_Invessorial Num | NUMBER | 22 | 16 | Y |
| 7 | `ORD_SALE_EXT_INV_PREX` | Ord_Sale_Ext_Invessorial Prex | VARCHAR2 | 4 |  | Y |
| 8 | `ORD_SALE_EXT_INV_DATE` | Ord_Sale_Ext_Invessorial Date | DATE | 7 |  | Y |
| 9 | `ORD_SALE_EXT_INV_SEAL_SERIES` | Ord_Sale_Ext_Inv_Sealessorial Series | VARCHAR2 | 3 |  | Y |
| 10 | `ORD_SALE_EXT_INV_SEAL_NUM` | Ord_Sale_Ext_Inv_Sealessorial Num | NUMBER | 22 | 10 | Y |
| 11 | `ORD_SALE_EXT_INV_VALUE` | Ord_Sale_Ext_Invessorial Value | NUMBER | 22 | 16 | Y |
| 12 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 13 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 14 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 15 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 16 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `H_ORD_D5D5`

- **Tipo:** Historical
- **Categoria:** Orders
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 5 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |
| 6 | `ORD_REF_VAL` | Ord_Refessorial Val | VARCHAR2 | 40 |  | N |
| 7 | `ORD_REF_QUAL_CODE` | Ord_Ref_Qualessorial Code | VARCHAR2 | 4 |  | Y |
| 8 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 9 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 11 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `H_ORD_D5D6`

- **Tipo:** Historical
- **Categoria:** Orders
- **Campos:** 22
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM, CUST_CODE, INVT_LEV1

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 5 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | N |
| 7 | `SEQ_NUM_SUG` | Seq_Numessorial Sug | NUMBER | 22 | 4 | N |
| 8 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 9 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 10 | `INVT_LEV2_SUG` | Invt_Lev2essorial Sug | VARCHAR2 | 40 |  | Y |
| 11 | `INVT_LEV3_SUG` | Invt_Lev3essorial Sug | VARCHAR2 | 40 |  | Y |
| 12 | `INVT_LEV4_SUG` | Invt_Lev4essorial Sug | VARCHAR2 | 40 |  | Y |
| 13 | `INVT_LEV5_SUG` | Invt_Lev5essorial Sug | VARCHAR2 | 40 |  | Y |
| 14 | `INVT_ACCESS_SUG` | Invt_Accessessorial Sug | VARCHAR2 | 5 |  | Y |
| 15 | `WHSE_CODE_SUG` | Whse_Codeessorial Sug | VARCHAR2 | 4 |  | Y |
| 16 | `LOC_CODE_SUG` | Loc_Codeessorial Sug | VARCHAR2 | 12 |  | Y |
| 17 | `HOLD_CODE_SUG` | Hold_Codeessorial Sug | VARCHAR2 | 4 |  | Y |
| 18 | `QTY_SUG` | Qtyessorial Sug | NUMBER | 22 | 9 | Y |
| 19 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 20 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 21 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 22 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `H_ORD_D6`

- **Tipo:** Historical
- **Categoria:** Orders
- **Campos:** 24
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 5 | `INFO_FLOW_SEQ_NUM` | Info_Flow_Seqessorial Num | NUMBER | 22 | 2 | N |
| 6 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | N |
| 7 | `INFO_FLOW_MAND_FLAG` | Info_Flow_Mandessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `INFO_FLOW_DOC_SEQ_NUM` | Info_Flow_Doc_Seqessorial Num | NUMBER | 22 | 2 | N |
| 9 | `DOC_CODE` | Document Code | VARCHAR2 | 4 |  | Y |
| 10 | `FORM_CODE` | Form Code | VARCHAR2 | 4 |  | Y |
| 11 | `DOC_PRT_TP_FLAG` | Doc_Prt_Tpessorial Flag | VARCHAR2 | 1 |  | Y |
| 12 | `ORD_DOC_PRT_STAT` | Ord_Doc_Prtessorial Stat | VARCHAR2 | 1 |  | Y |
| 13 | `ORD_DOC_REPRT_CNT` | Ord_Doc_Reprtessorial Cnt | NUMBER | 22 | 4 | Y |
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

## `H_ORD_D7`

- **Tipo:** Historical
- **Categoria:** Orders
- **Campos:** 47
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 5 | `CUST_CODE_BROK` | Cust_Codeessorial Brok | VARCHAR2 | 10 |  | N |
| 6 | `CUST_INVT_PROF_CODE` | Cust_Invt_Professorial Code | VARCHAR2 | 4 |  | N |
| 7 | `ORD_ITEM_LEV` | Ord_Itemessorial Lev | VARCHAR2 | 8 |  | N |
| 8 | `ORD_ITEM_LEV_DES` | Ord_Item_Levessorial Des | VARCHAR2 | 12 |  | N |
| 9 | `ORD_CHG_LEV_NUM` | Ord_Chg_Levessorial Num | NUMBER | 22 | 1 | N |
| 10 | `ORD_FLIFO_ACTUAL_LEV_VALUE` | Ord_Flifo_Actual_Levessorial Value | NUMBER | 22 | 2 | N |
| 11 | `ORD_FLIFO_ORD_BY_CLAUSE` | Ord_Flifo_Ord_Byessorial Clause | VARCHAR2 | 240 |  | N |
| 12 | `ORD_INVT_TERMGY_CODE_LEV1` | Ord_Invt_Termgy_Codeessorial Lev1 | VARCHAR2 | 4 |  | N |
| 13 | `ORD_LEV_NUM_LEV1` | Ord_Lev_Numessorial Lev1 | NUMBER | 22 | 1 | N |
| 14 | `ORD_INVT_LEV1` | Ord_Invtessorial Lev1 | VARCHAR2 | 9 |  | N |
| 15 | `ORD_FIELD_LEV1` | Ord_Fieldessorial Lev1 | VARCHAR2 | 8 |  | N |
| 16 | `ORD_FLIFO_INVT_VALUE_LEV1` | Ord_Flifo_Invt_Valueessorial Lev1 | NUMBER | 22 | 2 | N |
| 17 | `ORD_SEQ_NUM_FLAG_LEV1` | Ord_Seq_Num_Flagessorial Lev1 | VARCHAR2 | 1 |  | Y |
| 18 | `ORD_INVT_LEV_DES` | Ord_Invt_Levessorial Des | VARCHAR2 | 12 |  | Y |
| 19 | `ORD_INVT_TERMGY_CODE_LEV2` | Ord_Invt_Termgy_Codeessorial Lev2 | VARCHAR2 | 4 |  | Y |
| 20 | `ORD_LEV_NUM_LEV2` | Ord_Lev_Numessorial Lev2 | NUMBER | 22 | 1 | Y |
| 21 | `ORD_INVT_LEV2` | Ord_Invtessorial Lev2 | VARCHAR2 | 9 |  | Y |
| 22 | `ORD_FIELD_LEV2` | Ord_Fieldessorial Lev2 | VARCHAR2 | 8 |  | Y |
| 23 | `ORD_FLIFO_INVT_VALUE_LEV2` | Ord_Flifo_Invt_Valueessorial Lev2 | NUMBER | 22 | 2 | Y |
| 24 | `ORD_SEQ_NUM_FLAG_LEV2` | Ord_Seq_Num_Flagessorial Lev2 | VARCHAR2 | 1 |  | Y |
| 25 | `ORD_INVT_TERMGY_CODE_LEV3` | Ord_Invt_Termgy_Codeessorial Lev3 | VARCHAR2 | 4 |  | Y |
| 26 | `ORD_LEV_NUM_LEV3` | Ord_Lev_Numessorial Lev3 | NUMBER | 22 | 1 | Y |
| 27 | `ORD_INVT_LEV3` | Ord_Invtessorial Lev3 | VARCHAR2 | 9 |  | Y |
| 28 | `ORD_FIELD_LEV3` | Ord_Fieldessorial Lev3 | VARCHAR2 | 8 |  | Y |
| 29 | `ORD_FLIFO_INVT_VALUE_LEV3` | Ord_Flifo_Invt_Valueessorial Lev3 | NUMBER | 22 | 2 | Y |
| 30 | `ORD_SEQ_NUM_FLAG_LEV3` | Ord_Seq_Num_Flagessorial Lev3 | VARCHAR2 | 1 |  | Y |
| 31 | `ORD_INVT_TERMGY_CODE_LEV4` | Ord_Invt_Termgy_Codeessorial Lev4 | VARCHAR2 | 4 |  | Y |
| 32 | `ORD_LEV_NUM_LEV4` | Ord_Lev_Numessorial Lev4 | NUMBER | 22 | 1 | Y |
| 33 | `ORD_INVT_LEV4` | Ord_Invtessorial Lev4 | VARCHAR2 | 9 |  | Y |
| 34 | `ORD_FIELD_LEV4` | Ord_Fieldessorial Lev4 | VARCHAR2 | 8 |  | Y |
| 35 | `ORD_FLIFO_INVT_VALUE_LEV4` | Ord_Flifo_Invt_Valueessorial Lev4 | NUMBER | 22 | 2 | Y |
| 36 | `ORD_SEQ_NUM_FLAG_LEV4` | Ord_Seq_Num_Flagessorial Lev4 | VARCHAR2 | 1 |  | Y |
| 37 | `ORD_INVT_TERMGY_CODE_LEV5` | Ord_Invt_Termgy_Codeessorial Lev5 | VARCHAR2 | 4 |  | Y |
| 38 | `ORD_LEV_NUM_LEV5` | Ord_Lev_Numessorial Lev5 | NUMBER | 22 | 1 | Y |
| 39 | `ORD_INVT_LEV5` | Ord_Invtessorial Lev5 | VARCHAR2 | 9 |  | Y |
| 40 | `ORD_FIELD_LEV5` | Ord_Fieldessorial Lev5 | VARCHAR2 | 8 |  | Y |
| 41 | `ORD_FLIFO_INVT_VALUE_LEV5` | Ord_Flifo_Invt_Valueessorial Lev5 | NUMBER | 22 | 2 | Y |
| 42 | `ORD_SEQ_NUM_FLAG_LEV5` | Ord_Seq_Num_Flagessorial Lev5 | VARCHAR2 | 1 |  | Y |
| 43 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 44 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 45 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 46 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 47 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `H_ORD_D8`

- **Tipo:** Historical
- **Categoria:** Orders
- **Campos:** 13
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 4 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |
| 5 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 6 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | N |
| 7 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | N |
| 8 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | N |
| 9 | `INVT_LEV5` | Inventory Level 5 | VARCHAR2 | 40 |  | Y |
| 10 | `ORD_DEALLOC_QTY` | Ord_Deallocessorial Qty | NUMBER | 22 | 9 | N |
| 11 | `ORD_DEALLOC_DATE` | Ord_Deallocessorial Date | DATE | 7 |  | N |
| 12 | `ORD_NUM_DEALLOC_FOR` | Ord_Num_Deallocessorial For | NUMBER | 22 | 9 | Y |
| 13 | `ORD_LINE_NUM_DEALLOC_FOR` | Ord_Line_Num_Deallocessorial For | NUMBER | 22 | 4 | Y |

## `H_ORD_D9`

- **Tipo:** Historical
- **Categoria:** Orders
- **Campos:** 13
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM, LOC_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 5 | `ORD_NUM_BAT` | Ord_Numessorial Bat | NUMBER | 22 | 9 | N |
| 6 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | Y |
| 7 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 8 | `BAT_TP_FLAG` | Bat_Tpessorial Flag | VARCHAR2 | 1 |  | N |
| 9 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 10 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 12 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 13 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `H_ORD_H`

- **Tipo:** Historical
- **Categoria:** Orders
- **Campos:** 92
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 5 | `ORD_PREX` | Ordessorial Prex | VARCHAR2 | 4 |  | N |
| 6 | `ORD_SUFX` | Ordessorial Sufx | VARCHAR2 | 4 |  | Y |
| 7 | `ORD_STAT` | Ordessorial Stat | VARCHAR2 | 1 |  | N |
| 8 | `ORD_TP` | Ordessorial Tp | VARCHAR2 | 1 |  | N |
| 9 | `ORD_PRTY_NUM` | Ord_Prtyessorial Num | NUMBER | 22 | 1 | N |
| 10 | `ORD_CONF_DATE` | Ord_Confessorial Date | DATE | 7 |  | Y |
| 11 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 12 | `CON_CODE` | Consignee Code | VARCHAR2 | 10 |  | N |
| 13 | `SOLDTO_CODE` | Soldtoessorial Code | VARCHAR2 | 10 |  | N |
| 14 | `ORD_DATE` | Ordessorial Date | DATE | 7 |  | N |
| 15 | `ORD_TO_SHIP_DATE` | Ord_To_Shipessorial Date | DATE | 7 |  | N |
| 16 | `ORD_TO_ARR_DATE` | Ord_To_Arressorial Date | DATE | 7 |  | N |
| 17 | `ORD_CUST_ORD_NUM` | Ord_Cust_Ordessorial Num | VARCHAR2 | 20 |  | Y |
| 18 | `ORD_PO_NUM` | Ord_Poessorial Num | VARCHAR2 | 20 |  | Y |
| 19 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | N |
| 20 | `LOAD_TP_CODE` | Load Type Code | VARCHAR2 | 4 |  | N |
| 21 | `FRT_TERM_CODE` | Frt_Termessorial Code | VARCHAR2 | 4 |  | N |
| 22 | `MES_CODE` | Message Code | VARCHAR2 | 4 |  | Y |
| 23 | `ORD_REM_FLAG` | Ord_Remessorial Flag | VARCHAR2 | 1 |  | N |
| 24 | `ORD_CARR_FLAG` | Ord_Carressorial Flag | VARCHAR2 | 1 |  | N |
| 25 | `ORD_PALL_FLAG` | Ord_Pallessorial Flag | VARCHAR2 | 1 |  | N |
| 26 | `ORD_BILL_FLAG` | Ord_Billessorial Flag | VARCHAR2 | 1 |  | N |
| 27 | `ORD_EXTRA_CHG_FLAG` | Ord_Extra_Chgessorial Flag | VARCHAR2 | 1 |  | N |
| 28 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 29 | `ORD_ENTRY_DATE` | Ord_Entryessorial Date | DATE | 7 |  | N |
| 30 | `ORD_ALTER_FLAG` | Ord_Alteressorial Flag | VARCHAR2 | 1 |  | N |
| 31 | `ORD_CONF_FLAG` | Ord_Confessorial Flag | VARCHAR2 | 1 |  | N |
| 32 | `ORD_LOC_GEN_FLAG` | Ord_Loc_Genessorial Flag | VARCHAR2 | 1 |  | N |
| 33 | `ORD_LOC_STAT` | Ord_Locessorial Stat | VARCHAR2 | 1 |  | N |
| 34 | `ORD_DAY_ACT_REP_PROS_FLAG` | Ord_Day_Act_Rep_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 35 | `INFO_FLOW_PROF_CODE` | Information Flow Profile Code | VARCHAR2 | 4 |  | N |
| 36 | `INFO_FLOW_SEQ_NUM` | Info_Flow_Seqessorial Num | NUMBER | 22 | 2 | N |
| 37 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | N |
| 38 | `ORD_TRANS_FLAG` | Ord_Transessorial Flag | VARCHAR2 | 1 |  | Y |
| 39 | `ORD_TRANS_RCPT_NUM` | Ord_Trans_Rcptessorial Num | NUMBER | 22 | 9 | Y |
| 40 | `ORD_TRANS_RCPT_PREX` | Ord_Trans_Rcptessorial Prex | VARCHAR2 | 4 |  | Y |
| 41 | `ORD_TRANS_RCPT_SUFX` | Ord_Trans_Rcptessorial Sufx | VARCHAR2 | 4 |  | Y |
| 42 | `ORD_SHIP_WGT` | Ord_Shipessorial Wgt | NUMBER | 22 | 9 | Y |
| 43 | `ORD_SHIP_UNIT` | Ord_Shipessorial Unit | NUMBER | 22 | 9 | Y |
| 44 | `ORD_EDI_CREATE_FLAG` | Ord_Edi_Createessorial Flag | VARCHAR2 | 1 |  | N |
| 45 | `ORD_COD_AMT` | Ord_Codessorial Amt | NUMBER | 22 | 9 | Y |
| 46 | `PMT_TP_CODE` | Pmt_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 47 | `ORD_QRS_FLAG` | Ord_Qrsessorial Flag | VARCHAR2 | 1 |  | N |
| 48 | `EDI_INFO_FLAG` | Edi_Infoessorial Flag | VARCHAR2 | 1 |  | N |
| 49 | `ORD_APPO_DATE` | Ord_Appoessorial Date | DATE | 7 |  | Y |
| 50 | `DAY_ACT_REG_NUM` | Day_Act_Regessorial Num | NUMBER | 22 | 6 | Y |
| 51 | `ORD_CARR_FRT_FLAG` | Ord_Carr_Frtessorial Flag | VARCHAR2 | 1 |  | N |
| 52 | `ORD_EDI_GRP_VAL` | Ord_Edi_Grpessorial Val | VARCHAR2 | 30 |  | Y |
| 53 | `ORD_ALT_REF1` | Ord_Altessorial Ref1 | VARCHAR2 | 20 |  | Y |
| 54 | `ORD_ALT_REF2` | Ord_Altessorial Ref2 | VARCHAR2 | 20 |  | Y |
| 55 | `ORD_SHIP_PLT` | Ord_Shipessorial Plt | NUMBER | 22 | 9 | Y |
| 56 | `BORD_NUM` | Bordessorial Num | NUMBER | 22 | 9 | Y |
| 57 | `BORD_FLAG` | Bordessorial Flag | VARCHAR2 | 1 |  | Y |
| 58 | `ORD_SRCE_ORD_NUM` | Ord_Srce_Ordessorial Num | NUMBER | 22 | 9 | Y |
| 59 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 60 | `ORD_PACK_FLAG` | Ord_Packessorial Flag | VARCHAR2 | 1 |  | Y |
| 61 | `BAT_NUM` | Batch Number | NUMBER | 22 | 9 | Y |
| 62 | `MHE_TP_CODE` | Mhe_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 63 | `DIST_TP_CODE` | Dist_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 64 | `PACK_STN_CODE` | Pack_Stnessorial Code | VARCHAR2 | 4 |  | Y |
| 65 | `ORD_COMPL_ORD_FLAG` | Ord_Compl_Ordessorial Flag | VARCHAR2 | 1 |  | Y |
| 66 | `COMP_CODE_UPDOWNSTREAM` | Comp_Codeessorial Updownstream | VARCHAR2 | 2 |  | Y |
| 67 | `ORD_NUM_UPDOWNSTREAM` | Ord_Numessorial Updownstream | NUMBER | 22 | 9 | Y |
| 68 | `ORD_ALLOW_PICK_SUB_FLAG` | Ord_Allow_Pick_Subessorial Flag | VARCHAR2 | 1 |  | Y |
| 69 | `ORD_ALLOW_OVER_PICK_FLAG` | Ord_Allow_Over_Pickessorial Flag | VARCHAR2 | 1 |  | Y |
| 70 | `ORD_SHIP_PALL_WGT` | Ord_Ship_Pallessorial Wgt | NUMBER | 22 | 16 | Y |
| 71 | `WGT_MEAS_CODE_PALL` | Wgt_Meas_Codeessorial Pall | VARCHAR2 | 4 |  | Y |
| 72 | `PARCEL_CARR_ACC_NUM` | Parcel_Carr_Accessorial Num | VARCHAR2 | 20 |  | Y |
| 73 | `ORD_VICS_BOL_NUM` | Ord_Vics_Bolessorial Num | VARCHAR2 | 20 |  | Y |
| 74 | `ORD_VICS_BOL_NUM_LOAD` | Ord_Vics_Bol_Numessorial Load | VARCHAR2 | 20 |  | Y |
| 75 | `ORD_VICS_BOL_NUM_STOP` | Ord_Vics_Bol_Numessorial Stop | VARCHAR2 | 20 |  | Y |
| 76 | `ORD_SHIP_NUM_EXT_REF` | Ord_Ship_Num_Extessorial Ref | VARCHAR2 | 20 |  | Y |
| 77 | `ITEM_LOC_PROF_CODE` | Item_Loc_Professorial Code | VARCHAR2 | 4 |  | Y |
| 78 | `ORD_FRT_EST_AMT` | Ord_Frt_Estessorial Amt | NUMBER | 22 | 16 | Y |
| 79 | `BAT_NUM_PRO_FORMA` | Bat_Num_Proessorial Forma | NUMBER | 22 | 9 | Y |
| 80 | `ORD_A1INSPECTION_STAT_MES` | Ord_A1Inspection_Statessorial Mes | VARCHAR2 | 100 |  | Y |
| 81 | `SHIP_LANE_CODE` | Ship_Laneessorial Code | VARCHAR2 | 4 |  | Y |
| 82 | `ORD_PACK_DOC_CODE` | Ord_Pack_Docessorial Code | VARCHAR2 | 4 |  | Y |
| 83 | `ORD_ALLOW_STAGE_STOR_LOC` | Ord_Allow_Stage_Storessorial Loc | VARCHAR2 | 1 |  | Y |
| 84 | `ORD_CART_NOT_MIX_ITEM` | Ord_Cart_Not_Mixessorial Item | VARCHAR2 | 1 |  | Y |
| 85 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 86 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 87 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 88 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 89 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 90 | `ORD_LABEL_PRT_FLAG` | Ord_Label_Prtessorial Flag | VARCHAR2 | 1 |  | Y |
| 91 | `ORD_CANCEL_FLAG` | Ord_Cancelessorial Flag | VARCHAR2 | 1 |  | Y |
| 92 | `ORD_SOFT_CONF_FLAG` | Ord_Soft_Confessorial Flag | VARCHAR2 | 1 |  | Y |

## `H_ORD_PACK_D`

- **Tipo:** Historical
- **Categoria:** Orders
- **Campos:** 14
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 4 | `ORD_PACK_NUM` | Ord_Packessorial Num | NUMBER | 22 | 9 | N |
| 5 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |
| 6 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 7 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | Y |
| 8 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | Y |
| 9 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | Y |
| 10 | `INVT_LEV5` | Inventory Level 5 | VARCHAR2 | 40 |  | Y |
| 11 | `ORD_PACK_ENT_QTY` | Ord_Pack_Entessorial Qty | VARCHAR2 | 20 |  | Y |
| 12 | `ORD_PACK_QTY` | Ord_Packessorial Qty | NUMBER | 22 | 9 | Y |
| 13 | `ITEM_SET_CODE` | Item_Setessorial Code | VARCHAR2 | 20 |  | Y |
| 14 | `ITEM_SET_QTY` | Item_Setessorial Qty | NUMBER | 22 | 9 | Y |

## `H_ORD_PACK_H`

- **Tipo:** Historical
- **Categoria:** Orders
- **Campos:** 31
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 4 | `ORD_PACK_NUM` | Ord_Packessorial Num | NUMBER | 22 | 9 | N |
| 5 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 6 | `CON_CODE` | Consignee Code | VARCHAR2 | 10 |  | N |
| 7 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | N |
| 8 | `ORD_PACK_WAYBILL_NUM` | Ord_Pack_Waybillessorial Num | VARCHAR2 | 40 |  | Y |
| 9 | `ORD_PACK_WGT` | Ord_Packessorial Wgt | NUMBER | 22 | 16 | Y |
| 10 | `ORD_PACK_CUBE_CODE` | Ord_Pack_Cubeessorial Code | VARCHAR2 | 4 |  | Y |
| 11 | `ORD_PACK_UNIT` | Ord_Packessorial Unit | NUMBER | 22 | 9 | Y |
| 12 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 13 | `ORD_PACK_FULL_FLAG` | Ord_Pack_Fullessorial Flag | VARCHAR2 | 1 |  | Y |
| 14 | `ORD_PACK_STR_VALUE` | Ord_Pack_Stressorial Value | VARCHAR2 | 250 |  | Y |
| 15 | `ORD_PACK_STN` | Ord_Packessorial Stn | VARCHAR2 | 10 |  | Y |
| 16 | `ORD_PACK_REF_NUM1` | Ord_Pack_Refessorial Num1 | VARCHAR2 | 20 |  | Y |
| 17 | `ORD_PACK_REF_NUM2` | Ord_Pack_Refessorial Num2 | VARCHAR2 | 20 |  | Y |
| 18 | `ORD_PACK_FILE_LABEL` | Ord_Pack_Fileessorial Label | VARCHAR2 | 20 |  | Y |
| 19 | `ORD_PACK_FILE_COD_LABEL` | Ord_Pack_File_Codessorial Label | VARCHAR2 | 20 |  | Y |
| 20 | `ORD_PACK_FILE_DIR` | Ord_Pack_Fileessorial Dir | VARCHAR2 | 60 |  | Y |
| 21 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | Y |
| 22 | `ERR_CODE` | Error Code | VARCHAR2 | 6 |  | Y |
| 23 | `ERR_TEXT` | Error Text | VARCHAR2 | 100 |  | Y |
| 24 | `LOAD_NUM` | Load Number | NUMBER | 22 | 6 | Y |
| 25 | `WAVE_SEQ_NUM` | Wave_Seqessorial Num | NUMBER | 22 | 9 | Y |
| 26 | `POD_DATE` | Podessorial Date | DATE | 7 |  | Y |
| 27 | `POD_NAME` | Podessorial Name | VARCHAR2 | 40 |  | Y |
| 28 | `ORD_PACK_FRT_AMT` | Ord_Pack_Frtessorial Amt | NUMBER | 22 | 9 | Y |
| 29 | `ORD_PACK_COD_AMT` | Ord_Pack_Codessorial Amt | NUMBER | 22 | 9 | Y |
| 30 | `ORD_PACK_PRICE_AMT` | Ord_Pack_Priceessorial Amt | NUMBER | 22 | 9 | Y |
| 31 | `ORD_PACK_EDI_SEND_FLAG` | Ord_Pack_Edi_Sendessorial Flag | VARCHAR2 | 1 |  | Y |

## `H_ORD_PACK_LABEL`

- **Tipo:** Historical
- **Categoria:** Orders
- **Campos:** 26
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM, LOC_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4, SKU_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 4 | `ORD_PACK_LABEL_ID` | Ord_Pack_Labelessorial Id | VARCHAR2 | 30 |  | N |
| 5 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |
| 6 | `ORD_LOC_LINE_NUM` | Ord_Loc_Lineessorial Num | NUMBER | 22 | 4 | N |
| 7 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 8 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | N |
| 9 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 10 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 11 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | Y |
| 12 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | Y |
| 13 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | Y |
| 14 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | Y |
| 15 | `ORD_PACK_LABEL_QTY` | Ord_Pack_Labelessorial Qty | NUMBER | 22 | 9 | N |
| 16 | `SKU_CODE` | SKU Code | VARCHAR2 | 4 |  | N |
| 17 | `WAVE_NUM` | Waveessorial Num | NUMBER | 22 | 6 | Y |
| 18 | `PACK_STN_CODE` | Pack_Stnessorial Code | VARCHAR2 | 4 |  | Y |
| 19 | `SORT_SEQ_NUM` | Sort_Seqessorial Num | NUMBER | 22 | 6 | Y |
| 20 | `ORD_PACK_NUM` | Ord_Packessorial Num | NUMBER | 22 | 9 | Y |
| 21 | `EXT_REF_NUM1` | Ext_Refessorial Num1 | VARCHAR2 | 20 |  | Y |
| 22 | `ORD_PACK_PICK_FLAG` | Ord_Pack_Pickessorial Flag | VARCHAR2 | 1 |  | Y |
| 23 | `ORD_PACK_LABEL_DATA` | Ord_Pack_Labelessorial Data | CLOB | 4000 |  | Y |
| 24 | `RATE_NUM` | Rateessorial Num | NUMBER | 22 | 9 | Y |
| 25 | `CART_ID` | Cart ID | VARCHAR2 | 40 |  | Y |
| 26 | `OPID_PROS_VALUE` | Opid_Prosessorial Value | VARCHAR2 | 250 |  | Y |

## `H_ORD_PEND`

- **Tipo:** Historical
- **Categoria:** Orders
- **Campos:** 20
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 3 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |
| 4 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 5 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 6 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | N |
| 7 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | N |
| 8 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | N |
| 9 | `INVT_LEV5` | Inventory Level 5 | VARCHAR2 | 40 |  | Y |
| 10 | `ORD_PEND_QTY` | Ord_Pendessorial Qty | NUMBER | 22 | 9 | N |
| 11 | `ORD_PEND_WGT` | Ord_Pendessorial Wgt | NUMBER | 22 | 16 | N |
| 12 | `ORD_PEND_CUBE` | Ord_Pendessorial Cube | NUMBER | 22 | 16 | N |
| 13 | `ORD_LINE_TP` | Order Line Type | VARCHAR2 | 1 |  | Y |
| 14 | `WAVE_SEQ_NUM` | Wave_Seqessorial Num | NUMBER | 22 | 9 | Y |
| 15 | `PACK_STN_CODE` | Pack_Stnessorial Code | VARCHAR2 | 4 |  | Y |
| 16 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |
| 17 | `HOLD_RENW_FLAG` | Hold_Renwessorial Flag | VARCHAR2 | 1 |  | Y |
| 18 | `ORD_LINE_TP_ORG` | Ord_Line_Tpessorial Org | VARCHAR2 | 1 |  | Y |
| 19 | `ORD_PEND_WGT_ORG` | Ord_Pend_Wgtessorial Org | NUMBER | 22 | 16 | Y |
| 20 | `ORD_PEND_ITSH_WGT_SHIP_FLAG` | Ord_Pend_Itsh_Wgt_Shipessorial Flag | VARCHAR2 | 1 |  | Y |

## `H_ORD_QRS_D`

- **Tipo:** Historical
- **Categoria:** Orders
- **Campos:** 9
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 4 | `QRS_NUM` | Qrsessorial Num | NUMBER | 22 | 9 | N |
| 5 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 6 | `QRS_UNIT` | Qrsessorial Unit | NUMBER | 22 | 9 | N |
| 7 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | Y |
| 8 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | Y |
| 9 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | Y |

## `H_ORD_QRS_H`

- **Tipo:** Historical
- **Categoria:** Orders
- **Campos:** 14
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 4 | `QRS_PREX` | Qrsessorial Prex | VARCHAR2 | 2 |  | N |
| 5 | `QRS_TP` | Qrsessorial Tp | NUMBER | 22 | 1 | N |
| 6 | `QRS_MEMB_NUM` | Qrs_Membessorial Num | VARCHAR2 | 7 |  | N |
| 7 | `QRS_NUM` | Qrsessorial Num | NUMBER | 22 | 9 | N |
| 8 | `QRS_NUM_CHK_DIG` | Qrs_Num_Chkessorial Dig | NUMBER | 22 | 1 | N |
| 9 | `EXT_REF_NUM1` | Ext_Refessorial Num1 | VARCHAR2 | 20 |  | Y |
| 10 | `QRS_PRT_FLAG` | Qrs_Prtessorial Flag | VARCHAR2 | 1 |  | Y |
| 11 | `QRS_SCAN_FLAG` | Qrs_Scanessorial Flag | VARCHAR2 | 1 |  | Y |
| 12 | `QRS_NUM_LAY` | Qrs_Numessorial Lay | NUMBER | 22 | 3 | Y |
| 13 | `QRS_QTY_PER_LAY` | Qrs_Qty_Peressorial Lay | NUMBER | 22 | 3 | Y |
| 14 | `QRS_QTY_ODD_LAY` | Qrs_Qty_Oddessorial Lay | NUMBER | 22 | 3 | Y |

## `H_PLT_CONSL`

- **Tipo:** Historical
- **Categoria:** Orders
- **Campos:** 23
- **Campos-chave prováveis:** COMP_CODE, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `INSERT_TO_H_PLT_CONSL_DATE` | Insert_To_H_Plt_Conslessorial Date | DATE | 7 |  | N |
| 2 | `PLT_CONSL_NUM` | Plt_Conslessorial Num | NUMBER | 22 | 9 | N |
| 3 | `PLT_CONSL_LINE_NUM` | Plt_Consl_Lineessorial Num | NUMBER | 22 | 9 | N |
| 4 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 5 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | N |
| 7 | `PROS_FLAG` | Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `PROS_DATE` | Prosessorial Date | DATE | 7 |  | Y |
| 9 | `OP_CODE_PROS` | Op_Codeessorial Pros | VARCHAR2 | 20 |  | Y |
| 10 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 11 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | N |
| 12 | `PLT_CONSL_QTY` | Plt_Conslessorial Qty | NUMBER | 22 | 9 | N |
| 13 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | N |
| 14 | `WHSE_CODE_FROM` | Whse_Codeessorial From | VARCHAR2 | 4 |  | N |
| 15 | `LOC_CODE_FROM` | Loc_Codeessorial From | VARCHAR2 | 12 |  | N |
| 16 | `WHSE_CODE_TO` | Warehouse Code To | VARCHAR2 | 4 |  | Y |
| 17 | `LOC_CODE_TO` | Loc_Codeessorial To | VARCHAR2 | 12 |  | Y |
| 18 | `PLT_CONSL_MAX_HGT` | Plt_Consl_Maxessorial Hgt | NUMBER | 22 | 7 | Y |
| 19 | `LINEAR_MEAS_CODE` | Linear Measurement Code | VARCHAR2 | 4 |  | Y |
| 20 | `ITEM_QTY_BKD_NUM_LAY` | Item_Qty_Bkd_Numessorial Lay | NUMBER | 22 | 3 | Y |
| 21 | `ASS_NUM` | Assessorial Num | NUMBER | 22 | 9 | Y |
| 22 | `ASS_NUM_SEQ` | Ass_Numessorial Seq | NUMBER | 22 | 9 | Y |
| 23 | `PLT_CONSL_GRP_STR` | Plt_Consl_Grpessorial Str | VARCHAR2 | 2000 |  | Y |

## `H_PROS_ACT_INVESTGN_LOG`

- **Tipo:** Historical
- **Categoria:** Orders
- **Campos:** 18
- **Campos-chave prováveis:** COMP_CODE, LOC_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ACT_INVESTGN_SEQ_NUM` | Act_Investgn_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `ACT_INVESTGN_PROS_DATE` | Act_Investgn_Prosessorial Date | DATE | 7 |  | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `DOC_NUM` | Document Number | NUMBER | 22 | 9 | N |
| 5 | `DOC_LINE_NUM` | Document Line Number | NUMBER | 22 | 4 | N |
| 6 | `DOC_LOC_LINE_NUM` | Document Location Line Number | NUMBER | 22 | 4 | N |
| 7 | `DOC_TP_FLAG` | Doc_Tpessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | N |
| 9 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 10 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | N |
| 11 | `RF_PROF_INVT_CNT_VAL_TP` | Rf_Prof_Invt_Cnt_Valessorial Tp | VARCHAR2 | 1 |  | N |
| 12 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 13 | `BOOK_QTY` | Bookessorial Qty | NUMBER | 22 | 9 | N |
| 14 | `CNT_QTY` | Cntessorial Qty | NUMBER | 22 | 9 | N |
| 15 | `SUPERVISOR_OP_CODE` | Supervisor_Opessorial Code | VARCHAR2 | 20 |  | Y |
| 16 | `SUPERVISOR_APPRV_FLAG` | Supervisor_Apprvessorial Flag | VARCHAR2 | 1 |  | Y |
| 17 | `SEL_CODE` | Selessorial Code | VARCHAR2 | 6 |  | Y |
| 18 | `ACT_INVESTGN_TP_FLAG` | Act_Investgn_Tpessorial Flag | VARCHAR2 | 1 |  | Y |

## `H_PROS_ORD_LINE`

- **Tipo:** Historical
- **Categoria:** Orders
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 3 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |
| 4 | `ORD_PROS_FLAG` | Ord_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 6 | `ORD_PRTY_NUM` | Ord_Prtyessorial Num | NUMBER | 22 | 1 | N |
| 7 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | Y |
| 8 | `ORD_SORT_CODE` | Ord_Sortessorial Code | VARCHAR2 | 20 |  | Y |
| 9 | `ORD_LINE_ACPT_REF_VALUE` | Ord_Line_Acpt_Refessorial Value | VARCHAR2 | 20 |  | Y |
| 10 | `ORD_PROS_LINE_PROS_STAT` | Ord_Pros_Line_Prosessorial Stat | VARCHAR2 | 4 |  | Y |
| 11 | `INSERT_TO_H_DATE` | Insert_To_Hessorial Date | DATE | 7 |  | N |
| 12 | `TER_CODE_DEL` | Ter_Codeessorial Del | VARCHAR2 | 10 |  | Y |

## `H_PROS_ORD_LOC_LINE`

- **Tipo:** Historical
- **Categoria:** Orders
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 3 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |
| 4 | `ORD_LOC_LINE_NUM` | Ord_Loc_Lineessorial Num | NUMBER | 22 | 4 | N |
| 5 | `ORD_PROS_FLAG` | Ord_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 6 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 7 | `ORD_PRTY_NUM` | Ord_Prtyessorial Num | NUMBER | 22 | 1 | N |
| 8 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | Y |
| 9 | `ORD_SORT_CODE` | Ord_Sortessorial Code | VARCHAR2 | 20 |  | Y |
| 10 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 11 | `INSERT_TO_H_DATE` | Insert_To_Hessorial Date | DATE | 7 |  | N |
| 12 | `TER_CODE_DEL` | Ter_Codeessorial Del | VARCHAR2 | 10 |  | Y |

## `H_TEXT_MES`

- **Tipo:** Historical
- **Categoria:** Orders
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

## `H_TOTE_ASS`

- **Tipo:** Historical
- **Categoria:** Orders
- **Campos:** 17
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `WHSE_CODE_FLT_ASS` | Whse_Code_Fltessorial Ass | VARCHAR2 | 4 |  | N |
| 3 | `LOC_CODE_FLT_ASS` | Loc_Code_Fltessorial Ass | VARCHAR2 | 12 |  | N |
| 4 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | Y |
| 5 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | N |
| 6 | `WHSE_CODE_STATIC` | Whse_Codeessorial Static | VARCHAR2 | 4 |  | N |
| 7 | `LOC_CODE_STATIC` | Loc_Codeessorial Static | VARCHAR2 | 12 |  | N |
| 8 | `ZONE_CODE` | Zone Code | VARCHAR2 | 4 |  | N |
| 9 | `ZONE_CODE_NXT` | Zarehouse Code Nxt | VARCHAR2 | 4 |  | Y |
| 10 | `WAVE_SEQ_NUM` | Wave_Seqessorial Num | NUMBER | 22 | 9 | Y |
| 11 | `JOB_NUM` | Job Number | NUMBER | 22 | 9 | Y |
| 12 | `LOC_SIZE_CODE` | Loc_Sizeessorial Code | VARCHAR2 | 4 |  | N |
| 13 | `WHSE_CODE_DEST` | Whse_Codeessorial Dest | VARCHAR2 | 4 |  | N |
| 14 | `LOC_CODE_DEST` | Loc_Codeessorial Dest | VARCHAR2 | 12 |  | N |
| 15 | `TOTE_ASS_SEQ_NUM` | Tote_Ass_Seqessorial Num | NUMBER | 22 | 9 | N |
| 16 | `TOTE_ASS_ARR_DATE` | Tote_Ass_Arressorial Date | DATE | 7 |  | Y |
| 17 | `TOTE_ASS_CREATE_DATE` | Tote_Ass_Createessorial Date | DATE | 7 |  | N |

## `H_TRSPT_UNIT_D1`

- **Tipo:** Historical
- **Categoria:** Orders
- **Campos:** 17
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `TRSPT_UNIT_HIST_SEQ_NUM` | Trspt_Unit_Hist_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `TRSPT_EQP_OWN_CODE` | Trspt_Eqp_Ownessorial Code | VARCHAR2 | 10 |  | N |
| 4 | `TRSPT_UNIT_ID` | Trspt_Unitessorial Id | VARCHAR2 | 20 |  | N |
| 5 | `INB_OUTB_FLAG` | Inb_Outbessorial Flag | VARCHAR2 | 1 |  | N |
| 6 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | N |
| 7 | `POW_UNIT_TRSPT_EQP_OWN_CODE` | Pow_Unit_Trspt_Eqp_Ownessorial Code | VARCHAR2 | 10 |  | N |
| 8 | `POW_UNIT_TRSPT_UNIT_ID` | Pow_Unit_Trspt_Unitessorial Id | VARCHAR2 | 20 |  | N |
| 9 | `SEAL_NUM1` | Sealessorial Num1 | VARCHAR2 | 20 |  | Y |
| 10 | `SEAL_NUM2` | Sealessorial Num2 | VARCHAR2 | 20 |  | Y |
| 11 | `SEAL_NUM3` | Sealessorial Num3 | VARCHAR2 | 20 |  | Y |
| 12 | `SEAL_NUM1_ENTRY` | Seal_Num1essorial Entry | VARCHAR2 | 20 |  | Y |
| 13 | `SEAL_NUM2_ENTRY` | Seal_Num2essorial Entry | VARCHAR2 | 20 |  | Y |
| 14 | `SEAL_NUM3_ENTRY` | Seal_Num3essorial Entry | VARCHAR2 | 20 |  | Y |
| 15 | `SEAL_NUM1_INTACT_FLAG` | Seal_Num1_Intactessorial Flag | VARCHAR2 | 1 |  | Y |
| 16 | `SEAL_NUM2_INTACT_FLAG` | Seal_Num2_Intactessorial Flag | VARCHAR2 | 1 |  | Y |
| 17 | `SEAL_NUM3_INTACT_FLAG` | Seal_Num3_Intactessorial Flag | VARCHAR2 | 1 |  | Y |

## `H_TRSPT_UNIT_D2`

- **Tipo:** Historical
- **Categoria:** Orders
- **Campos:** 7
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `TRSPT_UNIT_HIST_SEQ_NUM` | Trspt_Unit_Hist_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `TRSPT_EQP_OWN_CODE` | Trspt_Eqp_Ownessorial Code | VARCHAR2 | 10 |  | N |
| 4 | `TRSPT_UNIT_ID` | Trspt_Unitessorial Id | VARCHAR2 | 20 |  | N |
| 5 | `SEQ_NUM` | Sequence Number | NUMBER | 22 | 2 | N |
| 6 | `LOAD_SEQ_NUM` | Load_Seqessorial Num | NUMBER | 22 | 6 | N |
| 7 | `LOAD_INB_OUTB_TP` | Load_Inb_Outbessorial Tp | VARCHAR2 | 1 |  | N |

## `H_TRSPT_UNIT_D3`

- **Tipo:** Historical
- **Categoria:** Orders
- **Campos:** 6
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `TRSPT_UNIT_HIST_SEQ_NUM` | Trspt_Unit_Hist_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `TRSPT_EQP_OWN_CODE` | Trspt_Eqp_Ownessorial Code | VARCHAR2 | 10 |  | N |
| 4 | `TRSPT_UNIT_ID` | Trspt_Unitessorial Id | VARCHAR2 | 20 |  | N |
| 5 | `YARD_ATTR_TP_CODE` | Yarehouse Attr Tp Code | VARCHAR2 | 4 |  | N |
| 6 | `YARD_ATTR_CODE` | Yard Attitbute Code | VARCHAR2 | 20 |  | N |

## `H_TRSPT_UNIT_D4`

- **Tipo:** Historical
- **Categoria:** Orders
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `TRSPT_UNIT_HIST_SEQ_NUM` | Trspt_Unit_Hist_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `TRSPT_EQP_OWN_CODE` | Trspt_Eqp_Ownessorial Code | VARCHAR2 | 10 |  | N |
| 4 | `TRSPT_UNIT_ID` | Trspt_Unitessorial Id | VARCHAR2 | 20 |  | N |
| 5 | `FLOW_DATE` | Flow Date | DATE | 7 |  | N |
| 6 | `FLOW_CODE` | Flowessorial Code | VARCHAR2 | 4 |  | N |
| 7 | `FLOW_CODE_TP_FLAG` | Flow_Code_Tpessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `FLOW_INFO_NUM` | Flow Information Number | NUMBER | 22 | 9 | N |
| 9 | `FLOW_INFO_DATE` | Flow_Infoessorial Date | DATE | 7 |  | Y |
| 10 | `FLOW_INFO_DES` | Flow_Infoessorial Des | VARCHAR2 | 30 |  | Y |
| 11 | `SPOOL_FILE_NAME` | Spool_Fileessorial Name | VARCHAR2 | 60 |  | Y |
| 12 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | Y |

## `H_TRSPT_UNIT_D6`

- **Tipo:** Historical
- **Categoria:** Orders
- **Campos:** 13
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `TRSPT_UNIT_HIST_SEQ_NUM` | Trspt_Unit_Hist_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `TRSPT_EQP_OWN_CODE` | Trspt_Eqp_Ownessorial Code | VARCHAR2 | 10 |  | N |
| 4 | `TRSPT_UNIT_ID` | Trspt_Unitessorial Id | VARCHAR2 | 20 |  | N |
| 5 | `INFO_FLOW_SEQ_NUM` | Info_Flow_Seqessorial Num | NUMBER | 22 | 2 | N |
| 6 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | N |
| 7 | `INFO_FLOW_MAND_FLAG` | Info_Flow_Mandessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `INFO_FLOW_DOC_SEQ_NUM` | Info_Flow_Doc_Seqessorial Num | NUMBER | 22 | 2 | N |
| 9 | `DOC_CODE` | Document Code | VARCHAR2 | 4 |  | Y |
| 10 | `FORM_CODE` | Form Code | VARCHAR2 | 4 |  | Y |
| 11 | `DOC_PRT_TP_FLAG` | Doc_Prt_Tpessorial Flag | VARCHAR2 | 1 |  | Y |
| 12 | `TRSPT_DOC_PRT_STAT` | Trspt_Doc_Prtessorial Stat | VARCHAR2 | 1 |  | Y |
| 13 | `TRSPT_DOC_REPRT_CNT` | Trspt_Doc_Reprtessorial Cnt | NUMBER | 22 | 4 | Y |

## `H_TRSPT_UNIT_H`

- **Tipo:** Historical
- **Categoria:** Orders
- **Campos:** 25
- **Campos-chave prováveis:** COMP_CODE, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `TRSPT_UNIT_HIST_SEQ_NUM` | Trspt_Unit_Hist_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `TRSPT_UNIT_HIST_DATE` | Trspt_Unit_Histessorial Date | DATE | 7 |  | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `TRSPT_EQP_OWN_CODE` | Trspt_Eqp_Ownessorial Code | VARCHAR2 | 10 |  | N |
| 5 | `TRSPT_UNIT_ID` | Trspt_Unitessorial Id | VARCHAR2 | 20 |  | N |
| 6 | `TRSPT_UNIT_STAT` | Trspt_Unitessorial Stat | VARCHAR2 | 1 |  | N |
| 7 | `TRSPT_UNIT_ACTN_FLAG` | Trspt_Unit_Actnessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `TRSPT_TP` | Trsptessorial Tp | VARCHAR2 | 1 |  | N |
| 9 | `TRSPT_EQP_TP_CODE` | Trspt_Eqp_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 10 | `TRSPT_EQP_CODE` | Trspt_Eqpessorial Code | VARCHAR2 | 10 |  | Y |
| 11 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |
| 12 | `INFO_FLOW_SEQ_NUM` | Info_Flow_Seqessorial Num | NUMBER | 22 | 2 | Y |
| 13 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | Y |
| 14 | `YARD_CODE` | Yard Code | VARCHAR2 | 4 |  | Y |
| 15 | `YARD_LOC_CODE` | Yard Location Code | VARCHAR2 | 12 |  | Y |
| 16 | `YARD_LOC_BLK_FLAG` | Yarehouse Loc Blk Flag | VARCHAR2 | 1 |  | Y |
| 17 | `YARD_LOC_VERT_LEV` | Yarehouse Loc Vert Lev | NUMBER | 22 | 2 | Y |
| 18 | `BLDG_CODE` | Building Code | VARCHAR2 | 4 |  | Y |
| 19 | `DOOR_CODE` | Door Code | VARCHAR2 | 4 |  | Y |
| 20 | `LOAD_SEQ_NUM` | Load_Seqessorial Num | NUMBER | 22 | 6 | Y |
| 21 | `STOP_NUM` | Stop Number | NUMBER | 22 | 4 | Y |
| 22 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | Y |
| 23 | `TRSPT_UNIT_REF_NUM1` | Trspt_Unit_Refessorial Num1 | VARCHAR2 | 20 |  | Y |
| 24 | `TRSPT_UNIT_REF_NUM2` | Trspt_Unit_Refessorial Num2 | VARCHAR2 | 20 |  | Y |
| 25 | `TRSPT_UNIT_EDI_CREATE_FLAG` | Trspt_Unit_Edi_Createessorial Flag | VARCHAR2 | 1 |  | N |

## `L_ASL_ORD_D`

- **Tipo:** Custom
- **Categoria:** Orders
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `BAT_NUM` | Batch Number | NUMBER | 22 | 9 | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 5 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | N |
| 6 | `ASL_ORD_ENT_QTY` | Asl_Ord_Entessorial Qty | VARCHAR2 | 20 |  | N |
| 7 | `ASL_ORD_QTY` | Asl_Ordessorial Qty | NUMBER | 22 | 9 | N |
| 8 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | N |
| 9 | `ASL_ORD_TOT_WGT` | Asl_Ord_Totessorial Wgt | NUMBER | 22 | 16 | N |
| 10 | `ORD_GEN_FLAG` | Ord_Genessorial Flag | VARCHAR2 | 1 |  | N |

## `L_ASL_ORD_DD`

- **Tipo:** Custom
- **Categoria:** Orders
- **Campos:** 8
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `BAT_NUM` | Batch Number | NUMBER | 22 | 9 | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 5 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | N |
| 6 | `CON_CODE` | Consignee Code | VARCHAR2 | 10 |  | N |
| 7 | `ASL_CON_ORD_ENT_QTY` | Asl_Con_Ord_Entessorial Qty | VARCHAR2 | 20 |  | N |
| 8 | `ASL_CON_ORD_QTY` | Asl_Con_Ordessorial Qty | NUMBER | 22 | 9 | N |

## `L_ASL_ORD_H`

- **Tipo:** Custom
- **Categoria:** Orders
- **Campos:** 6
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `BAT_NUM` | Batch Number | NUMBER | 22 | 9 | N |
| 3 | `ORD_PO_NUM` | Ord_Poessorial Num | VARCHAR2 | 20 |  | Y |
| 4 | `ORD_TO_SHIP_DATE` | Ord_To_Shipessorial Date | DATE | 7 |  | N |
| 5 | `ASL_ORD_BAT_STAT` | Asl_Ord_Batessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | Y |

## `L_ASL_PROS_ORD`

- **Tipo:** Custom
- **Categoria:** Orders
- **Campos:** 7
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `BAT_NUM` | Batch Number | NUMBER | 22 | 9 | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `CON_CODE` | Consignee Code | VARCHAR2 | 10 |  | N |
| 5 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 6 | `ORD_PREX` | Ordessorial Prex | VARCHAR2 | 4 |  | N |
| 7 | `ORD_SUFX` | Ordessorial Sufx | VARCHAR2 | 4 |  | Y |

## `L_FRT_LOAD`

- **Tipo:** Custom
- **Categoria:** Orders
- **Campos:** 21
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | N |
| 3 | `LOAD_NUM` | Load Number | NUMBER | 22 | 6 | N |
| 4 | `LOAD_REF_NUM` | Load_Refessorial Num | NUMBER | 22 | 6 | N |
| 5 | `LOAD_TYPE` | Loadessorial Type | VARCHAR2 | 1 |  | N |
| 6 | `LOAD_FLOW_STAT` | Load_Flowessorial Stat | VARCHAR2 | 4 |  | N |
| 7 | `FRT_DEST_CODE_ORIGIN` | Frt_Dest_Codeessorial Origin | VARCHAR2 | 10 |  | N |
| 8 | `FRT_DEST_CODE` | Frt_Destessorial Code | VARCHAR2 | 10 |  | N |
| 9 | `COMP_CODE_ACTUAL` | Comp_Codeessorial Actual | VARCHAR2 | 2 |  | N |
| 10 | `LOAD_DES` | Loadessorial Des | VARCHAR2 | 30 |  | Y |
| 11 | `FRT_ZONE_CODE` | Frt_Zoneessorial Code | VARCHAR2 | 6 |  | Y |
| 12 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | Y |
| 13 | `LOAD_DATE` | Loadessorial Date | DATE | 7 |  | Y |
| 14 | `LOAD_FRONT_TEMP` | Load_Frontessorial Temp | VARCHAR2 | 5 |  | Y |
| 15 | `LOAD_MID_TEMP` | Load_Midessorial Temp | VARCHAR2 | 5 |  | Y |
| 16 | `LOAD_BACK_TEMP` | Load_Backessorial Temp | VARCHAR2 | 5 |  | Y |
| 17 | `TRACTOR_NUM` | Tractoressorial Num | VARCHAR2 | 10 |  | Y |
| 18 | `UNIT_NUM` | Unitessorial Num | VARCHAR2 | 10 |  | Y |
| 19 | `LOAD_DRIVER_NAME` | Load_Driveressorial Name | VARCHAR2 | 30 |  | Y |
| 20 | `LOAD_TO_SHIP_DATE_SCH` | Load_To_Ship_Dateessorial Sch | DATE | 7 |  | Y |
| 21 | `LOAD_TO_ARR_DATE_SCH` | Load_To_Arr_Dateessorial Sch | DATE | 7 |  | Y |

## `L_FRT_ORD`

- **Tipo:** Custom
- **Categoria:** Orders
- **Campos:** 16
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | N |
| 3 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 4 | `COMP_CODE_ACTUAL` | Comp_Codeessorial Actual | VARCHAR2 | 2 |  | N |
| 5 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | Y |
| 6 | `ORD_TO_SHIP_DATE` | Ord_To_Shipessorial Date | DATE | 7 |  | Y |
| 7 | `ORD_TO_ARR_DATE` | Ord_To_Arressorial Date | DATE | 7 |  | Y |
| 8 | `COMP_CODE_LOAD_FINAL` | Comp_Code_Loadessorial Final | VARCHAR2 | 2 |  | Y |
| 9 | `FRT_TER_CODE_LOAD_FINAL` | Frt_Ter_Code_Loadessorial Final | VARCHAR2 | 4 |  | Y |
| 10 | `LOAD_NUM_LOAD_FINAL` | Load_Num_Loadessorial Final | NUMBER | 22 | 6 | Y |
| 11 | `ORD_PICK_UP_NUM` | Ord_Pick_Upessorial Num | VARCHAR2 | 20 |  | Y |
| 12 | `BILL_GRP_ORD_NUM` | Bill Group Order Number | NUMBER | 22 | 9 | Y |
| 13 | `ORD_STOP_NUM` | Ord_Stopessorial Num | VARCHAR2 | 2 |  | Y |
| 14 | `FRT_TER_CODE_LOAD` | Frt_Ter_Codeessorial Load | VARCHAR2 | 4 |  | Y |
| 15 | `LOAD_NUM` | Load Number | NUMBER | 22 | 6 | Y |
| 16 | `DRV_NAME_MAN` | Drv_Nameessorial Man | VARCHAR2 | 30 |  | Y |

## `M_BILL_TO_CUST_PROF`

- **Tipo:** Master
- **Categoria:** Orders
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `CUST_CODE_BILL_TO` | Cust_Code_Billessorial To | VARCHAR2 | 10 |  | N |
| 5 | `ITEM_BILL_PROF_CODE` | Item_Bill_Professorial Code | VARCHAR2 | 4 |  | N |
| 6 | `BILL_EVENT_TP_CODE` | Bill_Event_Tpessorial Code | VARCHAR2 | 1 |  | N |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_BILL_TO_CUST_PROF_IBIP_REF`

- **Tipo:** Master
- **Categoria:** Orders
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `CUST_CODE_BILL_TO` | Cust_Code_Billessorial To | VARCHAR2 | 10 |  | N |
| 5 | `ITEM_BILL_PROF_CODE_BILLTO` | Item_Bill_Prof_Codeessorial Billto | VARCHAR2 | 6 |  | N |
| 6 | `ITEM_BILL_PROF_CODE_INVT` | Item_Bill_Prof_Codeessorial Invt | VARCHAR2 | 6 |  | N |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_CONTAIN_PICKUP_RETURN_DAY`

- **Tipo:** Master
- **Categoria:** Orders
- **Campos:** 7
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CARR_CODE_SHIP_LINE` | Carr_Code_Shipessorial Line | VARCHAR2 | 10 |  | N |
| 3 | `CARR_CODE_PIER` | Carr_Codeessorial Pier | VARCHAR2 | 10 |  | N |
| 4 | `CONTAIN_PICKUP_DAY` | Contain_Pickupessorial Day | NUMBER | 22 | 2 | Y |
| 5 | `CONTAIN_RETURN_DAY` | Contain_Returnessorial Day | NUMBER | 22 | 2 | Y |
| 6 | `CONTAIN_PICKUP_RETURN_DATE` | Contain_Pickup_Returnessorial Date | DATE | 7 |  | N |
| 7 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |

## `M_CON_D1`

- **Tipo:** Master
- **Categoria:** Orders
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CON_CODE` | Consignee Code | VARCHAR2 | 10 |  | N |
| 4 | `CON_PREF_NUM` | Con_Prefessorial Num | NUMBER | 22 | 2 | N |
| 5 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_CON_D2`

- **Tipo:** Master
- **Categoria:** Orders
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CON_CODE` | Consignee Code | VARCHAR2 | 10 |  | N |
| 4 | `PRTY_SEQ_NUM` | Prty_Seqessorial Num | NUMBER | 22 | 3 | N |
| 5 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | N |
| 6 | `FRT_TER_CODE_DIRECT_SERV_CNTR` | Frt_Ter_Code_Direct_Servessorial Cntr | VARCHAR2 | 4 |  | Y |
| 7 | `CON_ROUTE_DES` | Con_Routeessorial Des | VARCHAR2 | 40 |  | Y |
| 8 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 9 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 11 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_CON_D3`

- **Tipo:** Master
- **Categoria:** Orders
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CON_CODE` | Consignee Code | VARCHAR2 | 10 |  | N |
| 4 | `ALT_CON_REP_TP_CODE` | Alt_Con_Rep_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 5 | `ALT_CON_REP_CODE` | Alt_Con_Repessorial Code | VARCHAR2 | 20 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_CON_H`

- **Tipo:** Master
- **Categoria:** Orders
- **Campos:** 59
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CON_CODE` | Consignee Code | VARCHAR2 | 10 |  | N |
| 4 | `CON_NAME` | Consignee Name | VARCHAR2 | 30 |  | N |
| 5 | `CON_STAT` | Conessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `CON_ADD1` | Conessorial Add1 | VARCHAR2 | 30 |  | N |
| 7 | `CON_ADD2` | Conessorial Add2 | VARCHAR2 | 30 |  | Y |
| 8 | `CON_ADD3` | Conessorial Add3 | VARCHAR2 | 30 |  | Y |
| 9 | `ZIP_CODE` | Zip Code | VARCHAR2 | 10 |  | N |
| 10 | `MES_CODE` | Message Code | VARCHAR2 | 4 |  | Y |
| 11 | `CON_LAST_ACT_DATE` | Con_Last_Actessorial Date | DATE | 7 |  | Y |
| 12 | `LOAD_ANAL_CODE` | Load_Analessorial Code | VARCHAR2 | 4 |  | Y |
| 13 | `CON_FRT_APPO_FLAG` | Con_Frt_Appoessorial Flag | VARCHAR2 | 1 |  | N |
| 14 | `CON_FRT_DISC_PCENT` | Con_Frt_Discessorial Pcent | NUMBER | 22 | 6 | N |
| 15 | `FRT_DEST_CODE` | Frt_Destessorial Code | VARCHAR2 | 10 |  | N |
| 16 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 17 | `PICK_PROF_CODE` | Pick_Professorial Code | VARCHAR2 | 4 |  | Y |
| 18 | `INFO_FLOW_PROF_CODE` | Information Flow Profile Code | VARCHAR2 | 4 |  | Y |
| 19 | `PRTY_NUM` | Prtyessorial Num | NUMBER | 22 | 1 | Y |
| 20 | `DAY_PROF_CODE` | Day_Professorial Code | VARCHAR2 | 4 |  | Y |
| 21 | `CON_BORD_FLAG` | Con_Bordessorial Flag | VARCHAR2 | 1 |  | N |
| 22 | `CON_LAB_STD_MODY_NUM` | Con_Lab_Std_Modyessorial Num | NUMBER | 22 | 4 | Y |
| 23 | `EXTRA_CHG_PROF_CODE` | Extra_Chg_Professorial Code | VARCHAR2 | 4 |  | Y |
| 24 | `CON_ADD4` | Conessorial Add4 | VARCHAR2 | 30 |  | Y |
| 25 | `COUNTRY_CODE` | Country Code | VARCHAR2 | 4 |  | N |
| 26 | `EXT_REF_NUM1` | Ext_Refessorial Num1 | VARCHAR2 | 20 |  | Y |
| 27 | `LANG_CODE` | Language Code | VARCHAR2 | 4 |  | N |
| 28 | `EDI_PROF_CODE` | Edi_Professorial Code | VARCHAR2 | 4 |  | Y |
| 29 | `CON_RETAIL_PROF_CODE` | Con_Retail_Professorial Code | VARCHAR2 | 4 |  | Y |
| 30 | `ITEM_LOC_PROF_CODE` | Item_Loc_Professorial Code | VARCHAR2 | 4 |  | Y |
| 31 | `CON_COMPL_ORD_FLAG` | Con_Compl_Ordessorial Flag | VARCHAR2 | 1 |  | N |
| 32 | `CON_FRT_TER_FLAG` | Con_Frt_Teressorial Flag | VARCHAR2 | 1 |  | Y |
| 33 | `CON_CODE_MAST` | Con_Codeessorial Mast | VARCHAR2 | 10 |  | Y |
| 34 | `CON_CODE_MAST_FLAG` | Con_Code_Mastessorial Flag | VARCHAR2 | 1 |  | Y |
| 35 | `SKU_CLASS_NUM` | Sku_Classessorial Num | NUMBER | 22 | 1 | Y |
| 36 | `SKU_CLASS_NUM_RND_FLAG` | Sku_Class_Num_Rndessorial Flag | VARCHAR2 | 1 |  | Y |
| 37 | `EXT_REF_NUM2` | Ext_Refessorial Num2 | VARCHAR2 | 20 |  | Y |
| 38 | `EXT_REF_NUM3` | Ext_Refessorial Num3 | VARCHAR2 | 20 |  | Y |
| 39 | `EXT_REF_NUM4` | Ext_Refessorial Num4 | VARCHAR2 | 20 |  | Y |
| 40 | `CON_ALLOW_BANDING_FLAG` | Con_Allow_Bandingessorial Flag | VARCHAR2 | 1 |  | Y |
| 41 | `CON_BANDING_SKU_CLASS_NUM` | Con_Banding_Sku_Classessorial Num | NUMBER | 22 | 1 | Y |
| 42 | `CON_CONSL_TP` | Con_Conslessorial Tp | VARCHAR2 | 1 |  | Y |
| 43 | `PALL_CODE` | Pallessorial Code | VARCHAR2 | 4 |  | Y |
| 44 | `CON_SPS_REQ_FLAG` | Con_Sps_Reqessorial Flag | VARCHAR2 | 1 |  | Y |
| 45 | `CON_ASN_REP_TP` | Con_Asn_Repessorial Tp | VARCHAR2 | 1 |  | Y |
| 46 | `CON_MSDS_REQ_FLAG` | Con_Msds_Reqessorial Flag | VARCHAR2 | 1 |  | Y |
| 47 | `CON_UCC128_LABEL_REQ_FLAG` | Con_Ucc128_Label_Reqessorial Flag | VARCHAR2 | 1 |  | Y |
| 48 | `CON_SKIP_CARTZN_FLAG` | Con_Skip_Cartznessorial Flag | VARCHAR2 | 1 |  | Y |
| 49 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 50 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 51 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 52 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 53 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 54 | `CON_DATA_SERVICE_ID` | Con_Data_Serviceessorial Id | VARCHAR2 | 100 |  | Y |
| 55 | `CON_EMP_ID_NUM` | Con_Emp_Idessorial Num | VARCHAR2 | 20 |  | Y |
| 56 | `ZIP_ID` | Zip ID | RAW | 32 |  | N |
| 57 | `CON_ASS_REST_BY_ITEM` | Con_Ass_Rest_Byessorial Item | VARCHAR2 | 1 |  | Y |
| 58 | `LOAD_MAX_WGT` | Load_Maxessorial Wgt | NUMBER | 22 | 16 | Y |
| 59 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | Y |

## `M_CON_ITEM_PRICE`

- **Tipo:** Master
- **Categoria:** Orders
- **Campos:** 8
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | N |
| 4 | `CON_CODE` | Consignee Code | VARCHAR2 | 10 |  | N |
| 5 | `CON_ITEM_PRICE_EFF_DATE` | Con_Item_Price_Effessorial Date | DATE | 7 |  | N |
| 6 | `CON_ITEM_PRICE_RETAIL` | Con_Item_Priceessorial Retail | NUMBER | 22 | 12 | Y |
| 7 | `CON_ITEM_PRICE_DISC` | Con_Item_Priceessorial Disc | NUMBER | 22 | 12 | Y |
| 8 | `CON_ITEM_PRICE_COST` | Con_Item_Priceessorial Cost | NUMBER | 22 | 12 | Y |

## `M_CON_RETAIL_PROF`

- **Tipo:** Master
- **Categoria:** Orders
- **Campos:** 13
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CON_RETAIL_PROF_CODE` | Con_Retail_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `CON_RETAIL_PROF_DES` | Con_Retail_Professorial Des | VARCHAR2 | 30 |  | N |
| 5 | `CON_RETAIL_PROF_STAT` | Con_Retail_Professorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `CON_RETAIL_TP_CODE` | Con_Retail_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 7 | `CON_RETAIL_HD_FLAG` | Con_Retail_Hdessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `CON_RETAIL_RETICK_FLAG` | Con_Retail_Retickessorial Flag | VARCHAR2 | 1 |  | N |
| 9 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 10 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 12 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 13 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_DEST_FWD`

- **Tipo:** Master
- **Categoria:** Orders
- **Campos:** 17
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `DEST_FWD_CODE` | Dest_Fwdessorial Code | VARCHAR2 | 10 |  | N |
| 4 | `DEST_FWD_NAME` | Dest_Fwdessorial Name | VARCHAR2 | 30 |  | N |
| 5 | `DEST_FWD_STAT` | Dest_Fwdessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `DEST_FWD_ADD1` | Dest_Fwdessorial Add1 | VARCHAR2 | 30 |  | N |
| 7 | `DEST_FWD_ADD2` | Dest_Fwdessorial Add2 | VARCHAR2 | 30 |  | Y |
| 8 | `DEST_FWD_ADD3` | Dest_Fwdessorial Add3 | VARCHAR2 | 30 |  | Y |
| 9 | `DEST_FWD_ADD4` | Dest_Fwdessorial Add4 | VARCHAR2 | 30 |  | Y |
| 10 | `ZIP_CODE` | Zip Code | VARCHAR2 | 10 |  | N |
| 11 | `COUNTRY_CODE` | Country Code | VARCHAR2 | 4 |  | N |
| 12 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 13 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 14 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 15 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 16 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 17 | `ZIP_ID` | Zip ID | RAW | 32 |  | N |

## `M_LOAD_ANAL`

- **Tipo:** Master
- **Categoria:** Orders
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `LOAD_ANAL_CODE` | Load_Analessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `LOAD_ANAL_DES` | Load_Analessorial Des | VARCHAR2 | 30 |  | N |
| 5 | `LOAD_ANAL_STAT` | Load_Analessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_LOAD_TP_D1`

- **Tipo:** Master
- **Categoria:** Orders
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `LOAD_TP_CODE` | Load Type Code | VARCHAR2 | 4 |  | N |
| 4 | `LOAD_INB_OUTB_FLAG` | Load_Inb_Outbessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | N |
| 6 | `LOAD_TP_QTY` | Load_Tpessorial Qty | NUMBER | 22 | 16 | N |
| 7 | `LOAD_TP_MI` | Load_Tpessorial Mi | NUMBER | 22 | 4 | Y |
| 8 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 9 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 11 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_LOAD_TP_D2`

- **Tipo:** Master
- **Categoria:** Orders
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `LOAD_TP_CODE` | Load Type Code | VARCHAR2 | 4 |  | N |
| 4 | `LOAD_INB_OUTB_FLAG` | Load_Inb_Outbessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `SKU_CLASS_NUM` | Sku_Classessorial Num | NUMBER | 22 | 1 | N |
| 6 | `LOAD_TP_QTY` | Load_Tpessorial Qty | NUMBER | 22 | 16 | N |
| 7 | `LOAD_TP_MI` | Load_Tpessorial Mi | NUMBER | 22 | 4 | Y |
| 8 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 9 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 11 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_LOAD_TP_H`

- **Tipo:** Master
- **Categoria:** Orders
- **Campos:** 15
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `LOAD_TP_CODE` | Load Type Code | VARCHAR2 | 4 |  | N |
| 4 | `LOAD_TP_DES` | Load_Tpessorial Des | VARCHAR2 | 30 |  | N |
| 5 | `LOAD_TP_STAT` | Load_Tpessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `LOAD_LAB_STD_MODY_NUM` | Load_Lab_Std_Modyessorial Num | NUMBER | 22 | 4 | Y |
| 7 | `LOAD_TP_TEMP_CNT` | Load_Tp_Tempessorial Cnt | NUMBER | 22 | 1 | Y |
| 8 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 9 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 11 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 13 | `LOAD_TP_OVRR_PICK_METH_FLAG` | Load_Tp_Ovrr_Pick_Methessorial Flag | VARCHAR2 | 1 |  | Y |
| 14 | `LOAD_TIME_INB_FIX_MI` | Load_Time_Inb_Fixessorial Mi | NUMBER | 22 | 4 | Y |
| 15 | `LOAD_TIME_OUTB_FIX_MI` | Load_Time_Outb_Fixessorial Mi | NUMBER | 22 | 4 | Y |

## `M_LOAD_TP_REGION`

- **Tipo:** Master
- **Categoria:** Orders
- **Campos:** 9
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `LOAD_TP_CODE` | Load Type Code | VARCHAR2 | 4 |  | N |
| 4 | `REGION_CODE` | Region Code | VARCHAR2 | 20 |  | N |
| 5 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 6 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 7 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 8 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_ORD_PACK_D`

- **Tipo:** Master
- **Categoria:** Orders
- **Campos:** 6
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `CON_CODE` | Consignee Code | VARCHAR2 | 10 |  | N |
| 4 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | N |
| 5 | `PROS_LINE_NUM` | Pros_Lineessorial Num | NUMBER | 22 | 6 | N |
| 6 | `PROS_VALUE` | Prosessorial Value | VARCHAR2 | 250 |  | N |

## `M_ORD_PACK_H`

- **Tipo:** Master
- **Categoria:** Orders
- **Campos:** 37
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 3 | `CON_CODE` | Consignee Code | VARCHAR2 | 10 |  | N |
| 4 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | N |
| 5 | `ORD_PACK_ITEM_VAL_RTN_CODE` | Ord_Pack_Item_Val_Rtnessorial Code | VARCHAR2 | 20 |  | Y |
| 6 | `ORD_PACK_WAYBILL_TERMGY` | Ord_Pack_Waybillessorial Termgy | VARCHAR2 | 10 |  | Y |
| 7 | `ORD_PACK_WAYBILL_REQ_FLAG` | Ord_Pack_Waybill_Reqessorial Flag | VARCHAR2 | 1 |  | Y |
| 8 | `ORD_PACK_SKU_FLAG` | Ord_Pack_Skuessorial Flag | VARCHAR2 | 1 |  | N |
| 9 | `ORD_PACK_NUM_START` | Ord_Pack_Numessorial Start | NUMBER | 22 | 9 | N |
| 10 | `ORD_PACK_NUM_END` | Ord_Pack_Numessorial End | NUMBER | 22 | 9 | N |
| 11 | `ORD_PACK_NUM_CRNT` | Ord_Pack_Numessorial Crnt | NUMBER | 22 | 9 | N |
| 12 | `ORD_PACK_DOC_RSP_FLAG` | Ord_Pack_Doc_Rspessorial Flag | VARCHAR2 | 1 |  | N |
| 13 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | Y |
| 14 | `ORD_PACK_FULL_IND` | Ord_Pack_Fullessorial Ind | VARCHAR2 | 10 |  | Y |
| 15 | `ORD_PACK_STN_REQ_FLAG` | Ord_Pack_Stn_Reqessorial Flag | VARCHAR2 | 1 |  | Y |
| 16 | `ORD_PACK_REF_NUM1` | Ord_Pack_Refessorial Num1 | VARCHAR2 | 20 |  | Y |
| 17 | `ORD_PACK_REF_NUM2` | Ord_Pack_Refessorial Num2 | VARCHAR2 | 20 |  | Y |
| 18 | `ORD_PACK_FILE_LABEL` | Ord_Pack_Fileessorial Label | VARCHAR2 | 20 |  | Y |
| 19 | `ORD_PACK_FILE_COD_LABEL` | Ord_Pack_File_Codessorial Label | VARCHAR2 | 20 |  | Y |
| 20 | `ORD_PACK_FILE_DIR` | Ord_Pack_Fileessorial Dir | VARCHAR2 | 20 |  | Y |
| 21 | `ORD_PACK_KEWILL_INTFACE_FLAG` | Ord_Pack_Kewill_Intfaceessorial Flag | VARCHAR2 | 1 |  | Y |
| 22 | `ORD_PACK_START_FLOW_CODE` | Ord_Pack_Start_Flowessorial Code | VARCHAR2 | 4 |  | Y |
| 23 | `ORD_PACK_END_FLOW_CODE` | Ord_Pack_End_Flowessorial Code | VARCHAR2 | 4 |  | Y |
| 24 | `ORD_PACK_PRE_PACK_FLOW_CODE` | Ord_Pack_Pre_Pack_Flowessorial Code | VARCHAR2 | 4 |  | Y |
| 25 | `ORD_PACK_DEL_FLAG` | Ord_Pack_Delessorial Flag | VARCHAR2 | 1 |  | Y |
| 26 | `ORD_PACK_UNIQUE_SER_NUM` | Ord_Pack_Unique_Seressorial Num | VARCHAR2 | 1 |  | N |
| 27 | `ORD_PACK_DEF_DUP_SER_NUM` | Ord_Pack_Def_Dup_Seressorial Num | VARCHAR2 | 4 |  | Y |
| 28 | `ORD_PACK_MIN_LEN_SER_NUM` | Ord_Pack_Min_Len_Seressorial Num | NUMBER | 22 | 4 | Y |
| 29 | `ORD_PACK_CART_DET_ENTRY_FLAG` | Ord_Pack_Cart_Det_Entryessorial Flag | VARCHAR2 | 1 |  | Y |
| 30 | `ORD_PACK_VALID_RULE_FLAG` | Ord_Pack_Valid_Ruleessorial Flag | VARCHAR2 | 1 |  | Y |
| 31 | `EDI_TRANS_SET_CODE` | Edi_Trans_Setessorial Code | VARCHAR2 | 4 |  | Y |
| 32 | `EDI_DATA_ID_CODE` | Edi_Data_Idessorial Code | VARCHAR2 | 20 |  | Y |
| 33 | `ORD_PACK_SCAN_QTY_FLAG` | Ord_Pack_Scan_Qtyessorial Flag | VARCHAR2 | 1 |  | Y |
| 34 | `EDI_VERS_CODE` | Edi_Versessorial Code | VARCHAR2 | 4 |  | Y |
| 35 | `ORD_PACK_CONF_ORD_COMPL_FLAG` | Ord_Pack_Conf_Ord_Complessorial Flag | VARCHAR2 | 1 |  | Y |
| 36 | `ORD_PACK_VAL_SER_NUM_PROS_FLAG` | Ord_Pack_Val_Ser_Num_Prosessorial Flag | VARCHAR2 | 1 |  | Y |
| 37 | `ORD_PACK_VAL_FLAG` | Ord_Pack_Valessorial Flag | VARCHAR2 | 1 |  | Y |

## `M_ORD_PRTY`

- **Tipo:** Master
- **Categoria:** Orders
- **Campos:** 14
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ORD_PRTY_NUM` | Ord_Prtyessorial Num | NUMBER | 22 | 1 | N |
| 4 | `ORD_PRTY_DES` | Ord_Prtyessorial Des | VARCHAR2 | 30 |  | N |
| 5 | `ORD_PRTY_STAT` | Ord_Prtyessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `ORD_PRTY_AUTO_ALLOC_FLAG` | Ord_Prty_Auto_Allocessorial Flag | VARCHAR2 | 1 |  | N |
| 7 | `ORD_PRTY_EVAL_ITEM_MIN_FLAG` | Ord_Prty_Eval_Item_Minessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `ORD_PRTY_ALLOC_TP_FLAG` | Ord_Prty_Alloc_Tpessorial Flag | VARCHAR2 | 1 |  | N |
| 9 | `ORD_PRTY_DEALLOC_FLAG` | Ord_Prty_Deallocessorial Flag | VARCHAR2 | 1 |  | N |
| 10 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 11 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 13 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 14 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_PICK_PROF`

- **Tipo:** Master
- **Categoria:** Orders
- **Campos:** 35
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `PICK_PROF_CODE` | Pick_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `PICK_PROF_DES` | Pick_Professorial Des | VARCHAR2 | 30 |  | N |
| 5 | `PICK_PROF_STAT` | Pick_Professorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `PICK_PROF_BK_QTY_CODE` | Pick_Prof_Bk_Qtyessorial Code | VARCHAR2 | 4 |  | N |
| 7 | `PICK_PROF_SHIP_FLIFO_FLAG` | Pick_Prof_Ship_Flifoessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `PICK_PROF_SHIP_FLIFO_CODE` | Pick_Prof_Ship_Flifoessorial Code | VARCHAR2 | 4 |  | N |
| 9 | `PICK_PROF_SHIP_FLIFO_FORUL` | Pick_Prof_Ship_Flifoessorial Forul | VARCHAR2 | 255 |  | Y |
| 10 | `PICK_PROF_FLIFO_CSTM_SEL_CODE` | Pick_Prof_Flifo_Cstm_Selessorial Code | VARCHAR2 | 4 |  | Y |
| 11 | `PICK_PROF_PICK_TP_FLAG` | Pick_Prof_Pick_Tpessorial Flag | VARCHAR2 | 1 |  | N |
| 12 | `PICK_PROF_RGE_DAY_FROM_NUM` | Pick_Prof_Rge_Day_Fromessorial Num | NUMBER | 22 | 4 | Y |
| 13 | `PICK_PROF_RGE_DAY_TO_NUM` | Pick_Prof_Rge_Day_Toessorial Num | NUMBER | 22 | 4 | Y |
| 14 | `PICK_PROF_NUM_DAY_AFTER_EXPY` | Pick_Prof_Num_Day_Afteressorial Expy | NUMBER | 22 | 4 | Y |
| 15 | `PICK_PROF_RGE_DATE_CODE` | Pick_Prof_Rge_Dateessorial Code | VARCHAR2 | 4 |  | Y |
| 16 | `PICK_PROF_MAX_NUM_REC` | Pick_Prof_Max_Numessorial Rec | NUMBER | 22 | 4 | Y |
| 17 | `PICK_PROF_REPL_MES_FLAG` | Pick_Prof_Repl_Mesessorial Flag | VARCHAR2 | 1 |  | N |
| 18 | `SORT_SEQ_CODE` | Sort_Seqessorial Code | VARCHAR2 | 4 |  | Y |
| 19 | `CART_ACTIVE_FLAG` | Cart_Activeessorial Flag | VARCHAR2 | 1 |  | N |
| 20 | `EDI_VERS_CODE` | Edi_Versessorial Code | VARCHAR2 | 4 |  | Y |
| 21 | `EDI_TRANS_SET_CODE` | Edi_Trans_Setessorial Code | VARCHAR2 | 4 |  | Y |
| 22 | `EDI_DATA_ID_CODE` | Edi_Data_Idessorial Code | VARCHAR2 | 20 |  | Y |
| 23 | `PICK_PROF_PICKL_FLIFO_FLAG` | Pick_Prof_Pickl_Flifoessorial Flag | VARCHAR2 | 1 |  | N |
| 24 | `PICK_PROF_OVRR_FLIFO_REPL_FLAG` | Pick_Prof_Ovrr_Flifo_Replessorial Flag | VARCHAR2 | 1 |  | N |
| 25 | `PICK_PROF_REPL_LEV` | Pick_Prof_Replessorial Lev | NUMBER | 22 | 1 | N |
| 26 | `PICK_PROF_OVPI_FLAG` | Pick_Prof_Ovpiessorial Flag | VARCHAR2 | 1 |  | Y |
| 27 | `PICK_PROF_FLIFO_NON_PICKL_FLAG` | Pick_Prof_Flifo_Non_Picklessorial Flag | VARCHAR2 | 1 |  | Y |
| 28 | `PICK_SUB_PROF_CODE` | Pick_Sub_Professorial Code | VARCHAR2 | 4 |  | Y |
| 29 | `PICK_RGE_DAY_START_DATE_CODE` | Pick_Rge_Day_Start_Dateessorial Code | VARCHAR2 | 4 |  | Y |
| 30 | `PICK_PROF_S_P_AVAIL_CAL_FLAG` | Pick_Prof_S_P_Avail_Calessorial Flag | VARCHAR2 | 1 |  | Y |
| 31 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 32 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 33 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 34 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 35 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_PICK_SUB_PROF_D`

- **Tipo:** Master
- **Categoria:** Orders
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `PICK_SUB_PROF_CODE` | Pick_Sub_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `LOC_TP_CODE` | Loc_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 5 | `LOC_SORT_SEQ_CODE` | Loc_Sort_Seqessorial Code | VARCHAR2 | 4 |  | Y |
| 6 | `PICK_SUB_PROF_RGE_DAY_FROM_NUM` | Pick_Sub_Prof_Rge_Day_Fromessorial Num | NUMBER | 22 | 4 | Y |
| 7 | `PICK_SUB_PROF_RGE_DT_FROM_MODE` | Pick_Sub_Prof_Rge_Dt_Fromessorial Mode | VARCHAR2 | 1 |  | Y |
| 8 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 9 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 11 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_PICK_SUB_PROF_DD`

- **Tipo:** Master
- **Categoria:** Orders
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `PICK_SUB_PROF_CODE` | Pick_Sub_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `LOC_TP_CODE` | Loc_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 5 | `PICK_SUB_PROF_PARA_NUM` | Pick_Sub_Prof_Paraessorial Num | NUMBER | 22 | 2 | N |
| 6 | `PICK_SUB_PROF_PARA_OPT_NUM` | Pick_Sub_Prof_Para_Optessorial Num | NUMBER | 22 | 2 | N |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_PICK_SUB_PROF_H`

- **Tipo:** Master
- **Categoria:** Orders
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `PICK_SUB_PROF_CODE` | Pick_Sub_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `PICK_SUB_PROF_DES` | Pick_Sub_Professorial Des | VARCHAR2 | 30 |  | N |
| 5 | `PICK_SUB_PROF_REPI_SUB_FLAG` | Pick_Sub_Prof_Repi_Subessorial Flag | VARCHAR2 | 1 |  | Y |
| 6 | `PICK_SUB_PROF_STAT` | Pick_Sub_Professorial Stat | VARCHAR2 | 1 |  | N |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_PKG`

- **Tipo:** Master
- **Categoria:** Orders
- **Campos:** 6
- **Campos-chave prováveis:** COMP_CODE, SKU_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `PKG_CODE` | Pkgessorial Code | VARCHAR2 | 4 |  | N |
| 3 | `PKG_DES` | Pkgessorial Des | VARCHAR2 | 30 |  | N |
| 4 | `PKG_STAT` | Pkgessorial Stat | VARCHAR2 | 1 |  | N |
| 5 | `SKU_CODE` | SKU Code | VARCHAR2 | 4 |  | N |
| 6 | `STACK_FLAG` | Stackessorial Flag | VARCHAR2 | 1 |  | N |

## `M_PLACD`

- **Tipo:** Master
- **Categoria:** Orders
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `PLACD_CODE` | Placdessorial Code | VARCHAR2 | 4 |  | N |
| 3 | `PLACD_DES` | Placdessorial Des | VARCHAR2 | 30 |  | N |
| 4 | `PLACD_STAT` | Placdessorial Stat | VARCHAR2 | 1 |  | N |

## `M_PMT_PRTY`

- **Tipo:** Master
- **Categoria:** Orders
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `PMT_PRTY_CODE` | Pmt_Prtyessorial Code | VARCHAR2 | 4 |  | N |
| 3 | `PMT_PRTY_DES` | Pmt_Prtyessorial Des | VARCHAR2 | 30 |  | N |
| 4 | `PMT_PRTY_STAT` | Pmt_Prtyessorial Stat | VARCHAR2 | 1 |  | N |

## `M_PO_TP`

- **Tipo:** Master
- **Categoria:** Orders
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `PO_TP_CODE` | Po_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 3 | `PO_TP_DES` | Po_Tpessorial Des | VARCHAR2 | 30 |  | N |
| 4 | `PO_TP_STAT` | Po_Tpessorial Stat | VARCHAR2 | 1 |  | N |

## `M_PROD_ORD_PROF_D1`

- **Tipo:** Master
- **Categoria:** Orders
- **Campos:** 13
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `PROD_ORD_PROF_CODE` | Prod_Ord_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 5 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | N |
| 6 | `PROD_ORD_PROF_QTY` | Prod_Ord_Professorial Qty | NUMBER | 22 | 9 | Y |
| 7 | `PROD_ORD_PROF_WGT` | Prod_Ord_Professorial Wgt | NUMBER | 22 | 16 | Y |
| 8 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | Y |
| 9 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 10 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 12 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 13 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_PROD_ORD_PROF_D2`

- **Tipo:** Master
- **Categoria:** Orders
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `PROD_ORD_PROF_CODE` | Prod_Ord_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `CUST_INVT_PROF_LEV_NUM` | Cust_Invt_Prof_Levessorial Num | NUMBER | 22 | 1 | N |
| 5 | `PROD_ORD_PROF_LEV_ENTRY_FLAG` | Prod_Ord_Prof_Lev_Entryessorial Flag | VARCHAR2 | 1 |  | N |
| 6 | `PROD_ORD_PROF_VAL_TP_CODE` | Prod_Ord_Prof_Val_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_PROD_ORD_PROF_H`

- **Tipo:** Master
- **Categoria:** Orders
- **Campos:** 14
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE, LOC_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `PROD_ORD_PROF_CODE` | Prod_Ord_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `PROD_ORD_PROF_DES` | Prod_Ord_Professorial Des | VARCHAR2 | 30 |  | N |
| 5 | `PROD_ORD_PROF_STAT` | Prod_Ord_Professorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 7 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | N |
| 8 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 9 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | N |
| 10 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 11 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 13 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 14 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_UPS_SHIP_TO_INFO`

- **Tipo:** Master
- **Categoria:** Orders
- **Campos:** 19
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 4 | `ORD_CUST_ORD_NUM` | Ord_Cust_Ordessorial Num | VARCHAR2 | 20 |  | N |
| 5 | `CON_NAME` | Consignee Name | VARCHAR2 | 30 |  | N |
| 6 | `CON_ADD1` | Conessorial Add1 | VARCHAR2 | 30 |  | N |
| 7 | `CON_ADD2` | Conessorial Add2 | VARCHAR2 | 30 |  | Y |
| 8 | `CON_ADD3` | Conessorial Add3 | VARCHAR2 | 30 |  | Y |
| 9 | `ZIP_CODE` | Zip Code | VARCHAR2 | 10 |  | N |
| 10 | `ZIP_CITY` | Zip Code City | VARCHAR2 | 30 |  | N |
| 11 | `STATE_CODE` | Stateessorial Code | VARCHAR2 | 4 |  | N |
| 12 | `COUNTRY_CODE` | Country Code | VARCHAR2 | 4 |  | N |
| 13 | `LAST_ACT_DATE` | Last_Actessorial Date | DATE | 7 |  | N |
| 14 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 15 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 16 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 17 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 18 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 19 | `ZIP_ID` | Zip ID | RAW | 32 |  | N |

## `S_ORD_H`

- **Tipo:** System Setup Related
- **Categoria:** Orders
- **Campos:** 7
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | Y |
| 4 | `CON_CODE` | Consignee Code | VARCHAR2 | 10 |  | Y |
| 5 | `SHIP_CODE` | Shipper Code | VARCHAR2 | 10 |  | Y |
| 6 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | Y |
| 7 | `CUST_CODE_BILL_TO` | Cust_Code_Billessorial To | VARCHAR2 | 10 |  | Y |

## `S_PICKLIST`

- **Tipo:** System Setup Related
- **Categoria:** Orders
- **Campos:** 16

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `PICKLIST_CODE` | Picklistessorial Code | VARCHAR2 | 10 |  | N |
| 2 | `PICKLIST_SEQ_NUM` | Picklist_Seqessorial Num | NUMBER | 22 | 2 | N |
| 3 | `PICKLIST_DES` | Picklistessorial Des | VARCHAR2 | 40 |  | N |
| 4 | `PICKLIST_HEAD` | Picklistessorial Head | VARCHAR2 | 255 |  | N |
| 5 | `PICKLIST_SQL` | Picklistessorial Sql | VARCHAR2 | 2000 |  | N |
| 6 | `PICKLIST_STAT_SQL` | Picklist_Statessorial Sql | VARCHAR2 | 512 |  | Y |
| 7 | `PICKLIST_SUPPRESS_INPUT` | Picklist_Suppressessorial Input | VARCHAR2 | 20 |  | Y |
| 8 | `EXE_JOB_CODE` | Exe_Jobessorial Code | VARCHAR2 | 10 |  | Y |
| 9 | `OLD_EXE_JOB_CODE` | Old_Exe_Jobessorial Code | VARCHAR2 | 10 |  | Y |
| 10 | `PICKLIST_DROPLIST_SELECT` | Picklist_Droplistessorial Select | VARCHAR2 | 500 |  | Y |
| 11 | `PICKLIST_DROPLIST_SELECT2` | Picklist_Droplistessorial Select2 | VARCHAR2 | 255 |  | Y |
| 12 | `PICKLIST_DROPLIST_SELECT3` | Picklist_Droplistessorial Select3 | VARCHAR2 | 255 |  | Y |
| 13 | `PICKLIST_DROPLIST_SELECT4` | Picklist_Droplistessorial Select4 | VARCHAR2 | 160 |  | Y |
| 14 | `PICKLIST_DROPLIST_SELECT5` | Picklist_Droplistessorial Select5 | VARCHAR2 | 255 |  | Y |
| 15 | `PICKLIST_MULTI_SELECT_FLAG` | Picklist_Multi_Selectessorial Flag | VARCHAR2 | 1 |  | Y |
| 16 | `PICKLIST_AUTO_QU_FLAG` | Picklist_Auto_Quessorial Flag | VARCHAR2 | 1 |  | Y |

## `S_PICK_LIST_PROF_D`

- **Tipo:** System Setup Related
- **Categoria:** Orders
- **Campos:** 16
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `PICK_LIST_PROF_CODE` | Pick_List_Professorial Code | VARCHAR2 | 20 |  | N |
| 2 | `PICK_LIST_TITLE` | Pick_Listessorial Title | VARCHAR2 | 40 |  | N |
| 3 | `PICK_LIST_SELECT` | Pick_Listessorial Select | VARCHAR2 | 1000 |  | N |
| 4 | `PICK_LIST_WHERE` | Pick_Listessorial Where | VARCHAR2 | 1000 |  | Y |
| 5 | `PICK_LIST_GROUP_BY` | Pick_List_Groupessorial By | VARCHAR2 | 500 |  | Y |
| 6 | `PICK_LIST_ORDER_BY` | Pick_List_Orderessorial By | VARCHAR2 | 500 |  | N |
| 7 | `PICK_LIST_COL_LABEL1` | Pick_List_Colessorial Label1 | VARCHAR2 | 40 |  | N |
| 8 | `PICK_LIST_COL_LABEL2` | Pick_List_Colessorial Label2 | VARCHAR2 | 40 |  | N |
| 9 | `PICK_LIST_COL_LABEL3` | Pick_List_Colessorial Label3 | VARCHAR2 | 40 |  | Y |
| 10 | `PICK_LIST_COL_LABEL4` | Pick_List_Colessorial Label4 | VARCHAR2 | 40 |  | Y |
| 11 | `PICK_LIST_COL_NAME1` | Pick_List_Colessorial Name1 | VARCHAR2 | 40 |  | N |
| 12 | `PICK_LIST_COL_NAME2` | Pick_List_Colessorial Name2 | VARCHAR2 | 40 |  | N |
| 13 | `PICK_LIST_COL_NAME3` | Pick_List_Colessorial Name3 | VARCHAR2 | 40 |  | Y |
| 14 | `PICK_LIST_COL_NAME4` | Pick_List_Colessorial Name4 | VARCHAR2 | 40 |  | Y |
| 15 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | Y |
| 16 | `COMP_CODE_FLAG` | Comp_Codeessorial Flag | VARCHAR2 | 1 |  | Y |

## `S_PICK_LIST_PROF_H`

- **Tipo:** System Setup Related
- **Categoria:** Orders
- **Campos:** 3

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `PICK_LIST_PROF_CODE` | Pick_List_Professorial Code | VARCHAR2 | 20 |  | N |
| 2 | `PICK_LIST_PROF_DES` | Pick_List_Professorial Des | VARCHAR2 | 60 |  | N |
| 3 | `PICK_LIST_TP_FLAG` | Pick_List_Tpessorial Flag | VARCHAR2 | 1 |  | N |

## `S_PICK_SUB_PARA`

- **Tipo:** System Setup Related
- **Categoria:** Orders
- **Campos:** 3

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `PICK_SUB_PROF_PARA_NUM` | Pick_Sub_Prof_Paraessorial Num | NUMBER | 22 | 2 | N |
| 2 | `PICK_SUB_PROF_PARA_OPT_NUM` | Pick_Sub_Prof_Para_Optessorial Num | NUMBER | 22 | 2 | N |
| 3 | `PICK_SUB_PROF_PARA_OPT_DES` | Pick_Sub_Prof_Para_Optessorial Des | VARCHAR2 | 80 |  | N |

## `T_INTFACE_SHIPMENT_QUEUE`

- **Tipo:** Temporary
- **Categoria:** Orders
- **Campos:** 6
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `SHIPMENT_NUM` | Shipmentessorial Num | NUMBER | 22 | 9 | N |
| 3 | `SHIPMENT_SRCE_FLAG` | Shipment_Srceessorial Flag | VARCHAR2 | 1 |  | N |
| 4 | `ACTION_FLAG` | Actionessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `CREATE_DATE` | Create Date | DATE | 7 |  | N |
| 6 | `NUM_OF_CART` | Num_Ofessorial Cart | NUMBER | 22 | 9 | N |

## `T_LOAD_ORD_REL`

- **Tipo:** Temporary
- **Categoria:** Orders
- **Campos:** 13
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `LOAD_ORD_REL_FUN_CODE` | Load_Ord_Rel_Funessorial Code | VARCHAR2 | 4 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `FRT_TER_CODE_LOAD` | Frt_Ter_Codeessorial Load | VARCHAR2 | 4 |  | N |
| 4 | `LOAD_NUM` | Load Number | NUMBER | 22 | 6 | N |
| 5 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | N |
| 6 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 7 | `COMP_CODE_ACTUAL` | Comp_Codeessorial Actual | VARCHAR2 | 2 |  | N |
| 8 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | Y |
| 9 | `STOP_NUM` | Stop Number | NUMBER | 22 | 4 | Y |
| 10 | `BILL_GRP_ORD_NUM` | Bill Group Order Number | VARCHAR2 | 8 |  | Y |
| 11 | `DELV_GRP_ORD_NUM` | Delv_Grp_Ordessorial Num | VARCHAR2 | 8 |  | Y |
| 12 | `LOAD_ORD_REL_PICK_DATE_TIME` | Load_Ord_Rel_Pick_Dateessorial Time | DATE | 7 |  | Y |
| 13 | `LOAD_ORD_REL_RQST_DATE_TIME` | Load_Ord_Rel_Rqst_Dateessorial Time | DATE | 7 |  | Y |

## `T_ORD_D5D1_INVT`

- **Tipo:** Temporary
- **Categoria:** Orders
- **Campos:** 27
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4, LOC_CODE, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 2 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 3 | `BOOKMARK_SEQ_NUM` | Bookmark_Seqessorial Num | NUMBER | 22 | 9 | N |
| 4 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | Y |
| 5 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | Y |
| 6 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | Y |
| 7 | `ORD_LOC_LINE_NUM` | Ord_Loc_Lineessorial Num | NUMBER | 22 | 4 | Y |
| 8 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | Y |
| 9 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | Y |
| 10 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | Y |
| 11 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | Y |
| 12 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | Y |
| 13 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | Y |
| 14 | `INVT_LEV5` | Inventory Level 5 | VARCHAR2 | 40 |  | Y |
| 15 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 16 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | Y |
| 17 | `ORD_LOC_QTY` | Ord_Locessorial Qty | NUMBER | 22 | 9 | Y |
| 18 | `ORD_LOC_ENT_QTY` | Ord_Loc_Entessorial Qty | VARCHAR2 | 20 |  | Y |
| 19 | `ORD_LOC_CNVC_QTY` | Ord_Loc_Cnvcessorial Qty | NUMBER | 22 | 6 | Y |
| 20 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | Y |
| 21 | `ORD_LOC_PROS_FLAG` | Ord_Loc_Prosessorial Flag | VARCHAR2 | 1 |  | Y |
| 22 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |
| 23 | `HOLD_SHIP_FLAG` | Hold_Shipessorial Flag | VARCHAR2 | 1 |  | Y |
| 24 | `HOLD_RENW_FLAG` | Hold_Renwessorial Flag | VARCHAR2 | 1 |  | Y |
| 25 | `LOC_TP_CODE` | Loc_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 26 | `INVT_EXPY_DATE` | Invt_Expyessorial Date | DATE | 7 |  | Y |
| 27 | `PICK_SEQ_NUM` | Pick_Seqessorial Num | NUMBER | 22 | 9 | Y |

## `T_ORD_VIRT`

- **Tipo:** Temporary
- **Categoria:** Orders
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 4 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |
| 5 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 6 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | N |
| 7 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | N |
| 8 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | N |
| 9 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | N |
| 10 | `ON_ORD_QTY` | On Order Quantity | NUMBER | 22 | 9 | N |
| 11 | `ORD_KIT_COMPN_FLAG` | Ord_Kit_Compnessorial Flag | VARCHAR2 | 1 |  | N |
| 12 | `ORD_KIT_LINE_NUM` | Ord_Kit_Lineessorial Num | NUMBER | 22 | 4 | Y |

## `T_PICK_SUB_INVT_D`

- **Tipo:** Temporary
- **Categoria:** Orders
- **Campos:** 8

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `PICK_SUB_INVT_D_SEQ_NUM` | Pick_Sub_Invt_D_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `PICK_SUB_INVT_H_SEQ_NUM` | Pick_Sub_Invt_H_Seqessorial Num | NUMBER | 22 | 9 | N |
| 3 | `ON_ORD_ORD_NUM` | On_Ord_Ordessorial Num | NUMBER | 22 | 9 | N |
| 4 | `ON_ORD_ORD_LINE_NUM` | On_Ord_Ord_Lineessorial Num | NUMBER | 22 | 4 | N |
| 5 | `ON_ORD_ORD_LOC_LINE_NUM` | On_Ord_Ord_Loc_Lineessorial Num | NUMBER | 22 | 4 | N |
| 6 | `ON_ORD_QTY` | On Order Quantity | NUMBER | 22 | 9 | N |
| 7 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | Y |
| 8 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | Y |

## `T_PICK_SUB_INVT_H`

- **Tipo:** Temporary
- **Categoria:** Orders
- **Campos:** 22
- **Campos-chave prováveis:** COMP_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4, LOC_CODE, HOLD_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `PICK_SUB_INVT_H_SEQ_NUM` | Pick_Sub_Invt_H_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `PICK_SUB_INVT_BAT_NUM` | Pick_Sub_Invt_Batessorial Num | NUMBER | 22 | 9 | N |
| 3 | `PICK_SUB_INVT_ORDER_BY_NUM` | Pick_Sub_Invt_Order_Byessorial Num | NUMBER | 22 | 9 | N |
| 4 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 5 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 6 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 7 | `PICK_SUB_INVT_CREATE_DATE` | Pick_Sub_Invt_Createessorial Date | DATE | 7 |  | N |
| 8 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | N |
| 9 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 10 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | N |
| 11 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | N |
| 12 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | N |
| 13 | `INVT_LEV5` | Inventory Level 5 | VARCHAR2 | 40 |  | Y |
| 14 | `INVT_EXPY_DATE` | Invt_Expyessorial Date | DATE | 7 |  | Y |
| 15 | `INVT_ORG_RECD_DATE` | Invt_Org_Recdessorial Date | DATE | 7 |  | Y |
| 16 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 17 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | N |
| 18 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | N |
| 19 | `ON_HAND_QTY` | On Hand Quantity | NUMBER | 22 | 9 | N |
| 20 | `ON_ORD_QTY` | On Order Quantity | NUMBER | 22 | 9 | N |
| 21 | `PICK_SUB_QTY` | Pick_Subessorial Qty | NUMBER | 22 | 9 | N |
| 22 | `PICK_SUB_INVT_STOCK_OPT_NUM` | Pick_Sub_Invt_Stock_Optessorial Num | NUMBER | 22 | 2 | N |

## `T_PICK_SUB_REPI`

- **Tipo:** Temporary
- **Categoria:** Orders
- **Campos:** 14

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `PICK_SUB_REPI_SEQ_NUM` | Pick_Sub_Repi_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `PICK_SUB_INVT_H_SEQ_NUM` | Pick_Sub_Invt_H_Seqessorial Num | NUMBER | 22 | 9 | N |
| 3 | `REPI_COMP_CODE` | Repi_Compessorial Code | VARCHAR2 | 2 |  | N |
| 4 | `REPI_ORD_NUM` | Repi_Ordessorial Num | NUMBER | 22 | 9 | N |
| 5 | `REPI_ORD_LINE_NUM` | Repi_Ord_Lineessorial Num | NUMBER | 22 | 4 | N |
| 6 | `REPI_ORD_LOC_LINE_NUM` | Repi_Ord_Loc_Lineessorial Num | NUMBER | 22 | 4 | N |
| 7 | `REPI_WHSE_CODE_FROM` | Repi_Whse_Codeessorial From | VARCHAR2 | 4 |  | N |
| 8 | `REPI_LOC_CODE_FROM` | Repi_Loc_Codeessorial From | VARCHAR2 | 12 |  | N |
| 9 | `REPI_WHSE_CODE_TO` | Repi_Whse_Codeessorial To | VARCHAR2 | 4 |  | N |
| 10 | `REPI_LOC_CODE_TO` | Repi_Loc_Codeessorial To | VARCHAR2 | 12 |  | N |
| 11 | `REPI_INVT_ACCESS` | Repi_Invtessorial Access | VARCHAR2 | 5 |  | N |
| 12 | `REPI_RELO_QTY` | Repi_Reloessorial Qty | NUMBER | 22 | 9 | N |
| 13 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 14 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |

