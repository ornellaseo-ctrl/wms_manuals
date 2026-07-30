# Tabelas — Cartonization

> Categoria extraída da planilha `Tables-Database.xlsx`. Total de tabelas: **7**.

## `C_CART_D`

- **Tipo:** Transactional
- **Categoria:** Cartonization
- **Campos:** 41
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4, HOLD_CODE, RCPT_NUM, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CART_ID` | Cart ID | VARCHAR2 | 40 |  | N |
| 4 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 5 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 6 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | N |
| 7 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | N |
| 8 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | N |
| 9 | `INVT_LEV5` | Inventory Level 5 | VARCHAR2 | 40 |  | Y |
| 10 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | N |
| 11 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | N |
| 12 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | Y |
| 13 | `RCPT_LINE_NUM` | Receipt Line Number | NUMBER | 22 | 4 | Y |
| 14 | `RCPT_LOC_LINE_NUM` | Rcpt_Loc_Lineessorial Num | NUMBER | 22 | 4 | Y |
| 15 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | Y |
| 16 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | Y |
| 17 | `ORD_LOC_LINE_NUM` | Ord_Loc_Lineessorial Num | NUMBER | 22 | 4 | Y |
| 18 | `ADJ_NUM` | Adjustment Number | NUMBER | 22 | 6 | Y |
| 19 | `ADJ_LINE_NUM` | Adjustment Line Number | NUMBER | 22 | 4 | Y |
| 20 | `PARENT_CHILD_FLAG` | Parent_Childessorial Flag | VARCHAR2 | 1 |  | N |
| 21 | `PARENT_CART_ID` | Parent_Cartessorial Id | VARCHAR2 | 40 |  | Y |
| 22 | `CHILD_CART_ID` | Child_Cartessorial Id | VARCHAR2 | 40 |  | Y |
| 23 | `STD_QTY` | Stdessorial Qty | NUMBER | 22 | 9 | N |
| 24 | `ON_HAND_QTY` | On Hand Quantity | NUMBER | 22 | 9 | N |
| 25 | `ON_ORD_QTY` | On Order Quantity | NUMBER | 22 | 9 | N |
| 26 | `ON_RCPT_QTY` | On_Rcptessorial Qty | NUMBER | 22 | 9 | N |
| 27 | `UNALLOC_QTY` | Unallocessorial Qty | NUMBER | 22 | 9 | N |
| 28 | `INTRANS_QTY` | Intransessorial Qty | NUMBER | 22 | 9 | N |
| 29 | `SKU` | Skuessorial Sku | VARCHAR2 | 4 |  | N |
| 30 | `ALLOW_BKD_SHIP_FLAG` | Allow_Bkd_Shipessorial Flag | VARCHAR2 | 1 |  | N |
| 31 | `ITEM_RETAIL_PRICE` | Item_Retailessorial Price | NUMBER | 22 | 12 | Y |
| 32 | `ITEM_DISC_PRICE` | Item_Discessorial Price | NUMBER | 22 | 12 | Y |
| 33 | `ITEM_COST` | Itemessorial Cost | NUMBER | 22 | 12 | Y |
| 34 | `CART_REF1` | Cartessorial Ref1 | VARCHAR2 | 20 |  | Y |
| 35 | `CART_REF2` | Cartessorial Ref2 | VARCHAR2 | 20 |  | Y |
| 36 | `CART_REF3` | Cartessorial Ref3 | VARCHAR2 | 20 |  | Y |
| 37 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 38 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 39 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 40 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 41 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `C_CART_H`

- **Tipo:** Transactional
- **Categoria:** Cartonization
- **Campos:** 70
- **Campos-chave prováveis:** COMP_CODE, RCPT_NUM, ORD_NUM, LOC_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CART_ID` | Cart ID | VARCHAR2 | 40 |  | N |
| 4 | `CREATE_DATE` | Create Date | DATE | 7 |  | N |
| 5 | `SHIP_DATE` | Shipessorial Date | DATE | 7 |  | Y |
| 6 | `CART_WGT` | Cartessorial Wgt | NUMBER | 22 | 16 | N |
| 7 | `CART_WGT_NET` | Cart_Wgtessorial Net | NUMBER | 22 | 16 | N |
| 8 | `CART_CUBE` | Cartessorial Cube | NUMBER | 22 | 16 | N |
| 9 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | Y |
| 10 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | Y |
| 11 | `ADJ_NUM` | Adjustment Number | NUMBER | 22 | 6 | Y |
| 12 | `CART_SEQ_NUM` | Cart_Seqessorial Num | VARCHAR2 | 20 |  | Y |
| 13 | `LOAD_NUM` | Load Number | NUMBER | 22 | 6 | Y |
| 14 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 15 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | N |
| 16 | `WHSE_CODE_TEMP` | Whse_Codeessorial Temp | VARCHAR2 | 4 |  | Y |
| 17 | `LOC_CODE_TEMP` | Loc_Codeessorial Temp | VARCHAR2 | 12 |  | Y |
| 18 | `PARENT_CART_ID` | Parent_Cartessorial Id | VARCHAR2 | 40 |  | Y |
| 19 | `CHILD_CART_ID` | Child_Cartessorial Id | VARCHAR2 | 40 |  | Y |
| 20 | `PARENT_CHILD_FLAG` | Parent_Childessorial Flag | VARCHAR2 | 1 |  | N |
| 21 | `CART_PROS_FLAG` | Cart_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 22 | `CART_SUSP_FLAG` | Cart_Suspessorial Flag | VARCHAR2 | 1 |  | Y |
| 23 | `MULTI_ENTITY_FLAG` | Multi_Entityessorial Flag | VARCHAR2 | 1 |  | N |
| 24 | `ALLOW_BKD_SHIP_FLAG` | Allow_Bkd_Shipessorial Flag | VARCHAR2 | 1 |  | N |
| 25 | `CART_STAT` | Cartessorial Stat | VARCHAR2 | 1 |  | Y |
| 26 | `PROS_AREA_CODE` | Pros_Areaessorial Code | VARCHAR2 | 4 |  | Y |
| 27 | `ZONE_CODE` | Zone Code | VARCHAR2 | 4 |  | Y |
| 28 | `CART_EXT_REF_NUM` | Cart_Ext_Refessorial Num | VARCHAR2 | 20 |  | Y |
| 29 | `CART_PROS_CODE` | Cart_Prosessorial Code | VARCHAR2 | 1 |  | Y |
| 30 | `CART_UCC_SER_NUM` | Cart_Ucc_Seressorial Num | VARCHAR2 | 250 |  | Y |
| 31 | `CART_UCC_ITEM_REF` | Cart_Ucc_Itemessorial Ref | VARCHAR2 | 40 |  | Y |
| 32 | `CART_UCC_PREX` | Cart_Uccessorial Prex | VARCHAR2 | 20 |  | Y |
| 33 | `CART_UCC_HEAD_NAME` | Cart_Ucc_Headessorial Name | VARCHAR2 | 40 |  | Y |
| 34 | `CART_UCC_HEAD_VALUE` | Cart_Ucc_Headessorial Value | VARCHAR2 | 20 |  | Y |
| 35 | `CART_RFID_READ_TP` | Cart_Rfid_Readessorial Tp | VARCHAR2 | 4 |  | Y |
| 36 | `PROS_VALUE_ORG` | Pros_Valueessorial Org | VARCHAR2 | 250 |  | Y |
| 37 | `MES_TEXT` | Mesessorial Text | VARCHAR2 | 250 |  | Y |
| 38 | `CART_SIZE_CODE` | Cart_Sizeessorial Code | VARCHAR2 | 4 |  | Y |
| 39 | `SHIPMENT_NUM` | Shipmentessorial Num | NUMBER | 22 | 9 | Y |
| 40 | `CART_UCC128_NUM` | Cart_Ucc128essorial Num | VARCHAR2 | 40 |  | Y |
| 41 | `CART_CARR_TRACK_NUM` | Cart_Carr_Trackessorial Num | VARCHAR2 | 40 |  | Y |
| 42 | `CART_BANDING_REF` | Cart_Bandingessorial Ref | VARCHAR2 | 40 |  | Y |
| 43 | `CART_INX_NUM` | Cart_Inxessorial Num | NUMBER | 22 | 9 | Y |
| 44 | `CART_INX_MAX` | Cart_Inxessorial Max | NUMBER | 22 | 9 | Y |
| 45 | `CART_PICK_BAT_NUM` | Cart_Pick_Batessorial Num | NUMBER | 22 | 9 | Y |
| 46 | `OP_CODE_AUDIT` | Op_Codeessorial Audit | VARCHAR2 | 20 |  | Y |
| 47 | `CART_AUDIT_DATE` | Cart_Auditessorial Date | DATE | 7 |  | Y |
| 48 | `CART_AUDIT_STAT` | Cart_Auditessorial Stat | VARCHAR2 | 1 |  | Y |
| 49 | `CART_SIZE_VAR_LEN` | Cart_Size_Varessorial Len | NUMBER | 22 | 7 | Y |
| 50 | `CART_SIZE_VAR_WID` | Cart_Size_Varessorial Wid | NUMBER | 22 | 7 | Y |
| 51 | `CART_SIZE_VAR_HGT` | Cart_Size_Varessorial Hgt | NUMBER | 22 | 7 | Y |
| 52 | `CART_PKG_ID` | Cart_Pkgessorial Id | VARCHAR2 | 20 |  | Y |
| 53 | `CART_SYS_CATRNZ_GEN_FLAG` | Cart_Sys_Catrnz_Genessorial Flag | VARCHAR2 | 1 |  | Y |
| 54 | `CART_SHIP_AMT` | Cart_Shipessorial Amt | NUMBER | 22 | 9 | Y |
| 55 | `CART_CARR_LABEL_DATA` | Cart_Carr_Labelessorial Data | CLOB | 4000 |  | Y |
| 56 | `CART_BAT_INTFACE_SEQ_NUM` | Cart_Bat_Intface_Seqessorial Num | NUMBER | 22 | 9 | Y |
| 57 | `PALL_CODE` | Pallessorial Code | VARCHAR2 | 4 |  | Y |
| 58 | `WRAP_NUM_TIME` | Warehouse Num Time | NUMBER | 22 | 1 | Y |
| 59 | `WRAP_TARGET_TIME` | Warehouse Target Time | NUMBER | 22 | 1 | Y |
| 60 | `CART_A1INSPECTION_STAT_MES` | Cart_A1Inspection_Statessorial Mes | VARCHAR2 | 100 |  | Y |
| 61 | `CART_A1INSPECTION_DATE` | Cart_A1Inspectionessorial Date | DATE | 7 |  | Y |
| 62 | `CART_A1INSPECTION_MES` | Cart_A1Inspectionessorial Mes | VARCHAR2 | 100 |  | Y |
| 63 | `CART_ID_ORIG` | Cart_Idessorial Orig | VARCHAR2 | 40 |  | Y |
| 64 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 65 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 66 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 67 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 68 | `CART_RENW_FLAG` | Cart_Renwessorial Flag | VARCHAR2 | 1 |  | Y |
| 69 | `CART_RENW_DATE` | Cart_Renwessorial Date | DATE | 7 |  | Y |
| 70 | `CART_BAT_NUM_RENW` | Cart_Bat_Numessorial Renw | NUMBER | 22 | 9 | Y |

## `C_CLIPPERSHIP`

- **Tipo:** Transactional
- **Categoria:** Cartonization
- **Campos:** 56
- **Campos-chave prováveis:** ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `CART_ID` | Cart ID | VARCHAR2 | 40 |  | N |
| 2 | `CLIPPERSHIP_PKG_CREATE_DATE` | Clippership_Pkg_Createessorial Date | DATE | 7 |  | N |
| 3 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | Y |
| 4 | `CON_NAME` | Consignee Name | VARCHAR2 | 30 |  | Y |
| 5 | `CON_ADD1` | Conessorial Add1 | VARCHAR2 | 30 |  | Y |
| 6 | `CON_ADD2` | Conessorial Add2 | VARCHAR2 | 30 |  | Y |
| 7 | `CON_ADD3` | Conessorial Add3 | VARCHAR2 | 30 |  | Y |
| 8 | `CON_ADD4` | Conessorial Add4 | VARCHAR2 | 30 |  | Y |
| 9 | `CON_CITY` | Conessorial City | VARCHAR2 | 30 |  | Y |
| 10 | `STATE_CODE_CON` | State_Codeessorial Con | VARCHAR2 | 4 |  | Y |
| 11 | `COUNTRY_CODE_CON` | Country_Codeessorial Con | VARCHAR2 | 4 |  | Y |
| 12 | `ZIP_CODE` | Zip Code | VARCHAR2 | 10 |  | Y |
| 13 | `TEL_NUM_CON` | Tel_Numessorial Con | VARCHAR2 | 80 |  | Y |
| 14 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | Y |
| 15 | `CLIPPER_SERVICE` | Clipperessorial Service | VARCHAR2 | 80 |  | Y |
| 16 | `ORD_CUST_ORD_NUM` | Ord_Cust_Ordessorial Num | VARCHAR2 | 80 |  | Y |
| 17 | `CLIPPER_RESIDENTIAL_FLAG` | Clipper_Residentialessorial Flag | VARCHAR2 | 80 |  | Y |
| 18 | `CLIPPER_SHIP_CODE` | Clipper_Shipessorial Code | VARCHAR2 | 80 |  | Y |
| 19 | `CLIPPER_INS_VALUE` | Clipper_Insessorial Value | VARCHAR2 | 80 |  | Y |
| 20 | `EXTRA_REF_NUM1` | Extra_Refessorial Num1 | VARCHAR2 | 20 |  | Y |
| 21 | `SOLDTO_NAME` | Soldtoessorial Name | VARCHAR2 | 30 |  | Y |
| 22 | `SOLDTO_ADD1` | Soldtoessorial Add1 | VARCHAR2 | 30 |  | Y |
| 23 | `SOLDTO_ADD2` | Soldtoessorial Add2 | VARCHAR2 | 30 |  | Y |
| 24 | `SOLDTO_ADD3` | Soldtoessorial Add3 | VARCHAR2 | 30 |  | Y |
| 25 | `CLIPPERSHIP_SOLDTO_CITY_ST_ZIP` | Clippership_Soldto_City_Stessorial Zip | VARCHAR2 | 80 |  | Y |
| 26 | `CLIPPERSHIP_COD_FLAG` | Clippership_Codessorial Flag | VARCHAR2 | 80 |  | Y |
| 27 | `CLIPPERSHIP_COD_AMOUNT` | Clippership_Codessorial Amount | VARCHAR2 | 80 |  | Y |
| 28 | `CLIPPERSHIP_REFERENCE1` | Clippershipessorial Reference1 | VARCHAR2 | 80 |  | Y |
| 29 | `CLIPPERSHIP_REFERENCE2` | Clippershipessorial Reference2 | VARCHAR2 | 80 |  | Y |
| 30 | `CLIPPERSHIP_SAT_SERVICE` | Clippership_Satessorial Service | VARCHAR2 | 80 |  | Y |
| 31 | `CLIPPERSHIP_COD_INCLUDE_FRT` | Clippership_Cod_Includeessorial Frt | VARCHAR2 | 80 |  | Y |
| 32 | `CLIPPERSHIP_COD_INCLUDE_CHARGE` | Clippership_Cod_Includeessorial Charge | VARCHAR2 | 80 |  | Y |
| 33 | `CLIPPERSHIP_SIGNATURE_REQUIRED` | Clippership_Signatureessorial Required | VARCHAR2 | 80 |  | Y |
| 34 | `CART_SIZE_LEN` | Cart_Sizeessorial Len | NUMBER | 22 | 7 | Y |
| 35 | `CART_SIZE_WID` | Cart_Sizeessorial Wid | NUMBER | 22 | 7 | Y |
| 36 | `CART_SIZE_HGT` | Cart_Sizeessorial Hgt | NUMBER | 22 | 7 | Y |
| 37 | `CLIPPERSHIP_FRT_COLLECT` | Clippership_Frtessorial Collect | VARCHAR2 | 80 |  | Y |
| 38 | `COUNTRY_CODE_SOLDTO` | Country_Codeessorial Soldto | VARCHAR2 | 10 |  | Y |
| 39 | `CLIPPERSHIP_TERMS` | Clippershipessorial Terms | VARCHAR2 | 80 |  | Y |
| 40 | `CLIPPERSHIP_COMMODITY_DES` | Clippership_Commodityessorial Des | VARCHAR2 | 80 |  | Y |
| 41 | `CUST_NAME` | Customer Name | VARCHAR2 | 30 |  | Y |
| 42 | `TEL_CONTACT_CUST` | Tel_Contactessorial Cust | VARCHAR2 | 30 |  | Y |
| 43 | `CUST_ADD1` | Custessorial Add1 | VARCHAR2 | 30 |  | Y |
| 44 | `CUST_ADD2` | Custessorial Add2 | VARCHAR2 | 30 |  | Y |
| 45 | `ZIP_CITY_CUST` | Zarehouse City Cust | VARCHAR2 | 30 |  | Y |
| 46 | `STATE_CODE_CUST` | State_Codeessorial Cust | VARCHAR2 | 4 |  | Y |
| 47 | `ZIP_CODE_CUST` | Zarehouse Code Cust | VARCHAR2 | 10 |  | Y |
| 48 | `COUNTRY_CODE_CUST` | Country_Codeessorial Cust | VARCHAR2 | 4 |  | Y |
| 49 | `COUNTRY_DES_CUST` | Country_Desessorial Cust | VARCHAR2 | 30 |  | Y |
| 50 | `TEL_NUM_CUST` | Tel_Numessorial Cust | VARCHAR2 | 10 |  | Y |
| 51 | `STD_QTY` | Stdessorial Qty | VARCHAR2 | 5 |  | Y |
| 52 | `CLIPPERSHIP_UNIT_VALUE` | Clippership_Unitessorial Value | VARCHAR2 | 10 |  | Y |
| 53 | `CLIPPERSHIP_ITEM_HARM_CODE` | Clippership_Item_Harmessorial Code | VARCHAR2 | 1 |  | Y |
| 54 | `CLIPPERSHIP_BOX_ITEM_DES` | Clippership_Box_Itemessorial Des | VARCHAR2 | 80 |  | Y |
| 55 | `CLIPPERSHIP_ORGIN_COUNTRY_CODE` | Clippership_Orgin_Countryessorial Code | VARCHAR2 | 80 |  | Y |
| 56 | `CLIPPERSHIP_ORGIN_COUNTRY_NAME` | Clippership_Orgin_Countryessorial Name | VARCHAR2 | 80 |  | Y |

## `H_CART_D`

- **Tipo:** Historical
- **Categoria:** Cartonization
- **Campos:** 44
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4, HOLD_CODE, RCPT_NUM, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `INSERT_TO_H_CART_D_DATE` | Insert_To_H_Cart_Dessorial Date | DATE | 7 |  | Y |
| 3 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | Y |
| 4 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | N |
| 5 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 6 | `CART_ID` | Cart ID | VARCHAR2 | 40 |  | N |
| 7 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 8 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 9 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | N |
| 10 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | N |
| 11 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | N |
| 12 | `INVT_LEV5` | Inventory Level 5 | VARCHAR2 | 40 |  | Y |
| 13 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | N |
| 14 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | N |
| 15 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | Y |
| 16 | `RCPT_LINE_NUM` | Receipt Line Number | NUMBER | 22 | 4 | Y |
| 17 | `RCPT_LOC_LINE_NUM` | Rcpt_Loc_Lineessorial Num | NUMBER | 22 | 4 | Y |
| 18 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | Y |
| 19 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | Y |
| 20 | `ORD_LOC_LINE_NUM` | Ord_Loc_Lineessorial Num | NUMBER | 22 | 4 | Y |
| 21 | `ADJ_NUM` | Adjustment Number | NUMBER | 22 | 6 | Y |
| 22 | `ADJ_LINE_NUM` | Adjustment Line Number | NUMBER | 22 | 4 | Y |
| 23 | `PARENT_CHILD_FLAG` | Parent_Childessorial Flag | VARCHAR2 | 1 |  | N |
| 24 | `PARENT_CART_ID` | Parent_Cartessorial Id | VARCHAR2 | 40 |  | Y |
| 25 | `CHILD_CART_ID` | Child_Cartessorial Id | VARCHAR2 | 40 |  | Y |
| 26 | `STD_QTY` | Stdessorial Qty | NUMBER | 22 | 9 | N |
| 27 | `ON_HAND_QTY` | On Hand Quantity | NUMBER | 22 | 9 | N |
| 28 | `ON_ORD_QTY` | On Order Quantity | NUMBER | 22 | 9 | N |
| 29 | `ON_RCPT_QTY` | On_Rcptessorial Qty | NUMBER | 22 | 9 | N |
| 30 | `UNALLOC_QTY` | Unallocessorial Qty | NUMBER | 22 | 9 | N |
| 31 | `INTRANS_QTY` | Intransessorial Qty | NUMBER | 22 | 9 | N |
| 32 | `SKU` | Skuessorial Sku | VARCHAR2 | 4 |  | N |
| 33 | `ALLOW_BKD_SHIP_FLAG` | Allow_Bkd_Shipessorial Flag | VARCHAR2 | 1 |  | N |
| 34 | `ITEM_RETAIL_PRICE` | Item_Retailessorial Price | NUMBER | 22 | 12 | Y |
| 35 | `ITEM_DISC_PRICE` | Item_Discessorial Price | NUMBER | 22 | 12 | Y |
| 36 | `ITEM_COST` | Itemessorial Cost | NUMBER | 22 | 12 | Y |
| 37 | `CART_REF1` | Cartessorial Ref1 | VARCHAR2 | 20 |  | Y |
| 38 | `CART_REF2` | Cartessorial Ref2 | VARCHAR2 | 20 |  | Y |
| 39 | `CART_REF3` | Cartessorial Ref3 | VARCHAR2 | 20 |  | Y |
| 40 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 41 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 42 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 43 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 44 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `H_CART_H`

- **Tipo:** Historical
- **Categoria:** Cartonization
- **Campos:** 71
- **Campos-chave prováveis:** COMP_CODE, RCPT_NUM, ORD_NUM, LOC_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `CART_ID` | Cart ID | VARCHAR2 | 40 |  | N |
| 5 | `CREATE_DATE` | Create Date | DATE | 7 |  | N |
| 6 | `SHIP_DATE` | Shipessorial Date | DATE | 7 |  | Y |
| 7 | `CART_WGT` | Cartessorial Wgt | NUMBER | 22 | 16 | N |
| 8 | `CART_WGT_NET` | Cart_Wgtessorial Net | NUMBER | 22 | 16 | N |
| 9 | `CART_CUBE` | Cartessorial Cube | NUMBER | 22 | 16 | N |
| 10 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | Y |
| 11 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | Y |
| 12 | `ADJ_NUM` | Adjustment Number | NUMBER | 22 | 6 | Y |
| 13 | `CART_SEQ_NUM` | Cart_Seqessorial Num | VARCHAR2 | 20 |  | Y |
| 14 | `LOAD_NUM` | Load Number | NUMBER | 22 | 6 | Y |
| 15 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 16 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | N |
| 17 | `WHSE_CODE_TEMP` | Whse_Codeessorial Temp | VARCHAR2 | 4 |  | Y |
| 18 | `LOC_CODE_TEMP` | Loc_Codeessorial Temp | VARCHAR2 | 12 |  | Y |
| 19 | `PARENT_CART_ID` | Parent_Cartessorial Id | VARCHAR2 | 40 |  | Y |
| 20 | `CHILD_CART_ID` | Child_Cartessorial Id | VARCHAR2 | 40 |  | Y |
| 21 | `PARENT_CHILD_FLAG` | Parent_Childessorial Flag | VARCHAR2 | 1 |  | N |
| 22 | `CART_PROS_FLAG` | Cart_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 23 | `CART_SUSP_FLAG` | Cart_Suspessorial Flag | VARCHAR2 | 1 |  | Y |
| 24 | `MULTI_ENTITY_FLAG` | Multi_Entityessorial Flag | VARCHAR2 | 1 |  | N |
| 25 | `ALLOW_BKD_SHIP_FLAG` | Allow_Bkd_Shipessorial Flag | VARCHAR2 | 1 |  | N |
| 26 | `CART_STAT` | Cartessorial Stat | VARCHAR2 | 1 |  | Y |
| 27 | `PROS_AREA_CODE` | Pros_Areaessorial Code | VARCHAR2 | 4 |  | Y |
| 28 | `ZONE_CODE` | Zone Code | VARCHAR2 | 4 |  | Y |
| 29 | `CART_EXT_REF_NUM` | Cart_Ext_Refessorial Num | VARCHAR2 | 20 |  | Y |
| 30 | `CART_PROS_CODE` | Cart_Prosessorial Code | VARCHAR2 | 1 |  | Y |
| 31 | `CART_UCC_SER_NUM` | Cart_Ucc_Seressorial Num | VARCHAR2 | 250 |  | Y |
| 32 | `CART_UCC_ITEM_REF` | Cart_Ucc_Itemessorial Ref | VARCHAR2 | 40 |  | Y |
| 33 | `CART_UCC_PREX` | Cart_Uccessorial Prex | VARCHAR2 | 20 |  | Y |
| 34 | `CART_UCC_HEAD_NAME` | Cart_Ucc_Headessorial Name | VARCHAR2 | 40 |  | Y |
| 35 | `CART_UCC_HEAD_VALUE` | Cart_Ucc_Headessorial Value | VARCHAR2 | 20 |  | Y |
| 36 | `CART_RFID_READ_TP` | Cart_Rfid_Readessorial Tp | VARCHAR2 | 4 |  | Y |
| 37 | `PROS_VALUE_ORG` | Pros_Valueessorial Org | VARCHAR2 | 250 |  | Y |
| 38 | `MES_TEXT` | Mesessorial Text | VARCHAR2 | 250 |  | Y |
| 39 | `CART_SIZE_CODE` | Cart_Sizeessorial Code | VARCHAR2 | 4 |  | Y |
| 40 | `SHIPMENT_NUM` | Shipmentessorial Num | NUMBER | 22 | 9 | Y |
| 41 | `CART_UCC128_NUM` | Cart_Ucc128essorial Num | VARCHAR2 | 40 |  | Y |
| 42 | `CART_CARR_TRACK_NUM` | Cart_Carr_Trackessorial Num | VARCHAR2 | 40 |  | Y |
| 43 | `CART_BANDING_REF` | Cart_Bandingessorial Ref | VARCHAR2 | 40 |  | Y |
| 44 | `CART_INX_NUM` | Cart_Inxessorial Num | NUMBER | 22 | 9 | Y |
| 45 | `CART_INX_MAX` | Cart_Inxessorial Max | NUMBER | 22 | 9 | Y |
| 46 | `CART_PICK_BAT_NUM` | Cart_Pick_Batessorial Num | NUMBER | 22 | 9 | Y |
| 47 | `OP_CODE_AUDIT` | Op_Codeessorial Audit | VARCHAR2 | 20 |  | Y |
| 48 | `CART_AUDIT_DATE` | Cart_Auditessorial Date | DATE | 7 |  | Y |
| 49 | `CART_AUDIT_STAT` | Cart_Auditessorial Stat | VARCHAR2 | 1 |  | Y |
| 50 | `CART_SIZE_VAR_LEN` | Cart_Size_Varessorial Len | NUMBER | 22 | 7 | Y |
| 51 | `CART_SIZE_VAR_WID` | Cart_Size_Varessorial Wid | NUMBER | 22 | 7 | Y |
| 52 | `CART_SIZE_VAR_HGT` | Cart_Size_Varessorial Hgt | NUMBER | 22 | 7 | Y |
| 53 | `CART_PKG_ID` | Cart_Pkgessorial Id | VARCHAR2 | 20 |  | Y |
| 54 | `CART_SYS_CATRNZ_GEN_FLAG` | Cart_Sys_Catrnz_Genessorial Flag | VARCHAR2 | 1 |  | Y |
| 55 | `CART_SHIP_AMT` | Cart_Shipessorial Amt | NUMBER | 22 | 9 | Y |
| 56 | `CART_CARR_LABEL_DATA` | Cart_Carr_Labelessorial Data | CLOB | 4000 |  | Y |
| 57 | `CART_BAT_INTFACE_SEQ_NUM` | Cart_Bat_Intface_Seqessorial Num | NUMBER | 22 | 9 | Y |
| 58 | `PALL_CODE` | Pallessorial Code | VARCHAR2 | 4 |  | Y |
| 59 | `WRAP_NUM_TIME` | Warehouse Num Time | NUMBER | 22 | 1 | Y |
| 60 | `WRAP_TARGET_TIME` | Warehouse Target Time | NUMBER | 22 | 1 | Y |
| 61 | `CART_A1INSPECTION_STAT_MES` | Cart_A1Inspection_Statessorial Mes | VARCHAR2 | 100 |  | Y |
| 62 | `CART_A1INSPECTION_DATE` | Cart_A1Inspectionessorial Date | DATE | 7 |  | Y |
| 63 | `CART_A1INSPECTION_MES` | Cart_A1Inspectionessorial Mes | VARCHAR2 | 100 |  | Y |
| 64 | `CART_ID_ORIG` | Cart_Idessorial Orig | VARCHAR2 | 40 |  | Y |
| 65 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 66 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 67 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 68 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 69 | `CART_RENW_FLAG` | Cart_Renwessorial Flag | VARCHAR2 | 1 |  | Y |
| 70 | `CART_RENW_DATE` | Cart_Renwessorial Date | DATE | 7 |  | Y |
| 71 | `CART_BAT_NUM_RENW` | Cart_Bat_Numessorial Renw | NUMBER | 22 | 9 | Y |

## `M_CART_SIZE`

- **Tipo:** Master
- **Categoria:** Cartonization
- **Campos:** 25
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CART_SIZE_CODE` | Cart_Sizeessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `CART_SIZE_DES` | Cart_Sizeessorial Des | VARCHAR2 | 30 |  | N |
| 5 | `CART_SIZE_STAT` | Cart_Sizeessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `LINEAR_MEAS_CODE` | Linear Measurement Code | VARCHAR2 | 4 |  | Y |
| 7 | `CART_SIZE_LEN` | Cart_Sizeessorial Len | NUMBER | 22 | 7 | Y |
| 8 | `CART_SIZE_WID` | Cart_Sizeessorial Wid | NUMBER | 22 | 7 | Y |
| 9 | `CART_SIZE_HGT` | Cart_Sizeessorial Hgt | NUMBER | 22 | 7 | Y |
| 10 | `CART_SIZE_CUBE` | Cart_Sizeessorial Cube | NUMBER | 22 | 10 | Y |
| 11 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | Y |
| 12 | `CART_SIZE_MAX_WGT` | Cart_Size_Maxessorial Wgt | NUMBER | 22 | 16 | Y |
| 13 | `CART_SIZE_WGT` | Cart_Sizeessorial Wgt | NUMBER | 22 | 16 | Y |
| 14 | `CART_SIZE_ITEM_CONFIG_FLAG` | Cart_Size_Item_Configessorial Flag | VARCHAR2 | 1 |  | N |
| 15 | `SKU_CLASS_NUM` | Sku_Classessorial Num | NUMBER | 22 | 1 | Y |
| 16 | `CART_SIZE_PCENT_UTIL` | Cart_Size_Pcentessorial Util | NUMBER | 22 | 6 | Y |
| 17 | `CART_SIZE_VAR_DIM_FLAG` | Cart_Size_Var_Dimessorial Flag | VARCHAR2 | 1 |  | Y |
| 18 | `CART_SIZE_UCC128_PKG_TP` | Cart_Size_Ucc128_Pkgessorial Tp | VARCHAR2 | 1 |  | Y |
| 19 | `CART_SIZE_OVERSIZE_FLAG` | Cart_Size_Oversizeessorial Flag | VARCHAR2 | 1 |  | Y |
| 20 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 21 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 22 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 23 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 24 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 25 | `UNIT_QTY_CUBE` | Unit_Qtyessorial Cube | NUMBER | 22 | 10 | Y |

## `S_CART_D`

- **Tipo:** System Setup Related
- **Categoria:** Cartonization
- **Campos:** 19
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, INVT_LEV1, INVT_LEV2, INVT_LEV3, INVT_LEV4, HOLD_CODE, RCPT_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CART_ID` | Cart ID | VARCHAR2 | 40 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `INVT_LEV1` | Inventory Level 1 | VARCHAR2 | 40 |  | N |
| 5 | `INVT_LEV2` | Inventory Level 2 | VARCHAR2 | 40 |  | N |
| 6 | `INVT_LEV3` | Inventory Level 3 | VARCHAR2 | 40 |  | N |
| 7 | `INVT_LEV4` | Inventory Level 4 | VARCHAR2 | 40 |  | N |
| 8 | `INVT_LEV5` | Inventory Level 5 | VARCHAR2 | 40 |  | Y |
| 9 | `HOLD_CODE` | Hold Code | VARCHAR2 | 4 |  | Y |
| 10 | `INVT_ACCESS` | Inventory Access | VARCHAR2 | 5 |  | N |
| 11 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | Y |
| 12 | `RCPT_LINE_NUM` | Receipt Line Number | NUMBER | 22 | 4 | Y |
| 13 | `RCPT_LOC_LINE_NUM` | Rcpt_Loc_Lineessorial Num | NUMBER | 22 | 4 | Y |
| 14 | `RCPT_LOC_QTY` | Rcpt_Locessorial Qty | NUMBER | 22 | 9 | N |
| 15 | `ON_HAND_QTY` | On Hand Quantity | NUMBER | 22 | 9 | N |
| 16 | `CART_QTY` | Cartessorial Qty | NUMBER | 22 | 9 | Y |
| 17 | `ADJ_QTY` | Adjessorial Qty | NUMBER | 22 | 9 | Y |
| 18 | `QTY_BKD_PROF_CODE` | Qty_Bkd_Professorial Code | VARCHAR2 | 4 |  | Y |
| 19 | `AVAIL_QTY` | Availessorial Qty | NUMBER | 22 | 9 | Y |

