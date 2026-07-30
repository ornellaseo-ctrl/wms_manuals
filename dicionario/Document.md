# Tabelas — Document

> Categoria extraída da planilha `Tables-Database.xlsx`. Total de tabelas: **17**.

## `C_EXT_FILE`

- **Tipo:** Transactional
- **Categoria:** Document
- **Campos:** 12

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `EXT_FILE_SEQ_NUM` | Ext_File_Seqessorial Num | NUMBER | 22 | 9 | N |
| 3 | `EXT_FILE_DES` | Ext_Fileessorial Des | VARCHAR2 | 40 |  | N |
| 4 | `EXT_FILE_DATE` | Ext_Fileessorial Date | DATE | 7 |  | N |
| 5 | `APP_CODE` | Application Code | VARCHAR2 | 10 |  | N |
| 6 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 7 | `EXT_FILE_BLOB` | Ext_Fileessorial Blob | BLOB | 4000 |  | N |
| 8 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 9 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 11 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `C_EXT_IMAGE`

- **Tipo:** Transactional
- **Categoria:** Document
- **Campos:** 35
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE, ITEM_CODE, ORD_NUM, RCPT_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | Y |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | Y |
| 4 | `SHIP_CODE` | Shipper Code | VARCHAR2 | 10 |  | Y |
| 5 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | Y |
| 6 | `CON_CODE` | Consignee Code | VARCHAR2 | 10 |  | Y |
| 7 | `ITEM_CODE` | Item Code | VARCHAR2 | 20 |  | Y |
| 8 | `INV_NUM` | Invoice Number | NUMBER | 22 | 9 | Y |
| 9 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | Y |
| 10 | `RCPT_NUM` | Receipt Number | NUMBER | 22 | 9 | Y |
| 11 | `DOC_USER` | Docessorial User | VARCHAR2 | 20 |  | N |
| 12 | `DOC_INDEX` | Docessorial Index | VARCHAR2 | 64 |  | N |
| 13 | `DOC_DATE` | Docessorial Date | DATE | 7 |  | N |
| 14 | `DOC_SIZE` | Docessorial Size | NUMBER | 22 | 9 | N |
| 15 | `DOC_TP` | Docessorial Tp | VARCHAR2 | 128 |  | N |
| 16 | `DOC_STAT` | Docessorial Stat | VARCHAR2 | 4 |  | N |
| 17 | `DOC_FILE` | Docessorial File | VARCHAR2 | 256 |  | N |
| 18 | `DOC_NAME` | Docessorial Name | VARCHAR2 | 256 |  | N |
| 19 | `DOC_SIGN` | Docessorial Sign | VARCHAR2 | 256 |  | Y |
| 20 | `DOC_DES` | Docessorial Des | VARCHAR2 | 256 |  | Y |
| 21 | `EXT_FILE_SEQ_NUM` | Ext_File_Seqessorial Num | NUMBER | 22 | 9 | Y |
| 22 | `INV_PREX` | Invoice Prefix | VARCHAR2 | 4 |  | Y |
| 23 | `INV_TP` | Invessorial Tp | VARCHAR2 | 4 |  | Y |
| 24 | `DOC_CODE` | Document Code | VARCHAR2 | 4 |  | Y |
| 25 | `RF_TER_ID` | Rf_Teressorial Id | VARCHAR2 | 256 |  | Y |
| 26 | `RF_TER_IP` | Rf_Teressorial Ip | VARCHAR2 | 64 |  | Y |
| 27 | `RF_IMAGE_DATE` | Rf_Imageessorial Date | DATE | 7 |  | Y |
| 28 | `RF_UPLOAD_DATE` | Rf_Uploadessorial Date | DATE | 7 |  | Y |
| 29 | `RF_PROS_DATE` | Rf_Prosessorial Date | DATE | 7 |  | Y |
| 30 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 31 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 32 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 33 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 34 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 35 | `LOAD_NUM` | Load Number | NUMBER | 22 | 10 | Y |

## `C_EXT_LAB_SWARE_QUEUE`

- **Tipo:** Transactional
- **Categoria:** Document
- **Campos:** 9

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `LAB_UNIQUE_SEQ_NUM` | Lab_Unique_Seqessorial Num | NUMBER | 22 | 9 | N |
| 3 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 4 | `LAB_TIME_DATE` | Lab_Timeessorial Date | DATE | 7 |  | N |
| 5 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 6 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 7 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 8 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `C_LOG_EXCP_VARC`

- **Tipo:** Transactional
- **Categoria:** Document
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CUST_CODE` | Customer Code | VARCHAR2 | 12 |  | N |
| 3 | `DOC_TP` | Docessorial Tp | VARCHAR2 | 2 |  | N |
| 4 | `DOC_NUM` | Document Number | NUMBER | 22 | 9 | N |
| 5 | `DOC_LINE_NUM` | Document Line Number | NUMBER | 22 | 4 | N |
| 6 | `DOC_LOC_LINE_NUM` | Document Location Line Number | NUMBER | 22 | 4 | N |
| 7 | `REC_TP` | Recessorial Tp | VARCHAR2 | 1 |  | N |
| 8 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 9 | `LOG_DATE` | Logessorial Date | DATE | 7 |  | N |
| 10 | `LOG_MES` | Logessorial Mes | VARCHAR2 | 60 |  | Y |
| 11 | `REAS_CODE` | Reasessorial Code | VARCHAR2 | 4 |  | Y |
| 12 | `AUD_NUM` | Audessorial Num | NUMBER | 22 | 6 | Y |

## `C_OP_APP_OVRR`

- **Tipo:** Transactional
- **Categoria:** Document
- **Campos:** 9
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `FUNC_CODE` | Funcessorial Code | VARCHAR2 | 20 |  | N |
| 4 | `DOC_NUM` | Document Number | NUMBER | 22 | 9 | N |
| 5 | `DOC_LINE_NUM` | Document Line Number | NUMBER | 22 | 4 | N |
| 6 | `DOC_LOC_LINE_NUM` | Document Location Line Number | NUMBER | 22 | 4 | N |
| 7 | `OP_APP_OVRR_SEQ_NUM` | Op_App_Ovrr_Seqessorial Num | NUMBER | 22 | 6 | Y |
| 8 | `STAG_WHSE_CODE` | Stag_Whseessorial Code | VARCHAR2 | 4 |  | Y |
| 9 | `STAG_LOC_CODE` | Stag_Locessorial Code | VARCHAR2 | 12 |  | Y |

## `E_PROS_DOC_LOC_LINE_MHE`

- **Tipo:** Transactional
- **Categoria:** Document
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `DOC_INB_OUTB_FLAG` | Doc_Inb_Outbessorial Flag | VARCHAR2 | 1 |  | N |
| 3 | `DOC_NUM` | Document Number | NUMBER | 22 | 9 | N |
| 4 | `DOC_LINE_NUM` | Document Line Number | NUMBER | 22 | 4 | N |
| 5 | `DOC_LOC_LINE_NUM` | Document Location Line Number | NUMBER | 22 | 4 | N |
| 6 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 7 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | Y |
| 8 | `EXE_JOB_CODE` | Exe_Jobessorial Code | VARCHAR2 | 10 |  | N |
| 9 | `MHE_CODE` | Mheessorial Code | VARCHAR2 | 10 |  | Y |
| 10 | `WHSE_CODE_FROM` | Whse_Codeessorial From | VARCHAR2 | 4 |  | Y |
| 11 | `LOC_CODE_FROM` | Loc_Codeessorial From | VARCHAR2 | 12 |  | Y |
| 12 | `LOCK_CREATE_DATE` | Lock_Createessorial Date | DATE | 7 |  | Y |

## `E_PROS_FRT_BILL_GRP`

- **Tipo:** Transactional
- **Categoria:** Document
- **Campos:** 7
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | N |
| 3 | `BILL_GRP_ORD_NUM` | Bill Group Order Number | NUMBER | 22 | 9 | N |
| 4 | `ORD_PROS_FLAG` | Ord_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 6 | `ORD_PROS_DATE` | Ord_Prosessorial Date | DATE | 7 |  | Y |
| 7 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | Y |

## `E_PROS_FRT_DELV_GRP`

- **Tipo:** Transactional
- **Categoria:** Document
- **Campos:** 7
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | N |
| 3 | `DELV_GRP_ORD_NUM` | Delv_Grp_Ordessorial Num | NUMBER | 22 | 9 | N |
| 4 | `ORD_PROS_FLAG` | Ord_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 6 | `ORD_PROS_DATE` | Ord_Prosessorial Date | DATE | 7 |  | Y |
| 7 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | Y |

## `E_PROS_FRT_LOAD`

- **Tipo:** Transactional
- **Categoria:** Document
- **Campos:** 8
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | N |
| 3 | `LOAD_NUM` | Load Number | NUMBER | 22 | 10 | N |
| 4 | `ORD_PROS_FLAG` | Ord_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 6 | `ORD_PROS_DATE` | Ord_Prosessorial Date | DATE | 7 |  | Y |
| 7 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | Y |
| 8 | `LOAD_SOFT_LOCK` | Load_Softessorial Lock | VARCHAR2 | 20 |  | Y |

## `E_PROS_FRT_ORD`

- **Tipo:** Transactional
- **Categoria:** Document
- **Campos:** 7
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `FRT_TER_CODE` | Frt_Teressorial Code | VARCHAR2 | 4 |  | N |
| 3 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 4 | `ORD_PROS_FLAG` | Ord_Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | N |
| 6 | `ORD_PROS_DATE` | Ord_Prosessorial Date | DATE | 7 |  | Y |
| 7 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | Y |

## `H_DOC_MAN`

- **Tipo:** Historical
- **Categoria:** Document
- **Campos:** 17
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ARCH_PURGE_REG_NUM` | Archive Purge Register Number | NUMBER | 22 | 9 | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `DOC_NUM` | Document Number | NUMBER | 22 | 9 | N |
| 4 | `DOC_TP_FLAG` | Doc_Tpessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `DOC_MAN_CODE_TP_FLAG` | Doc_Man_Code_Tpessorial Flag | VARCHAR2 | 1 |  | N |
| 6 | `DOC_MAN_NAME` | Doc_Manessorial Name | VARCHAR2 | 30 |  | N |
| 7 | `DOC_MAN_ADD1` | Doc_Manessorial Add1 | VARCHAR2 | 30 |  | Y |
| 8 | `DOC_MAN_ADD2` | Doc_Manessorial Add2 | VARCHAR2 | 30 |  | Y |
| 9 | `DOC_MAN_ADD3` | Doc_Manessorial Add3 | VARCHAR2 | 30 |  | Y |
| 10 | `ZIP_CODE_DOC_MAN` | Zarehouse Code Doc Man | VARCHAR2 | 10 |  | Y |
| 11 | `ZIP_CITY_DOC_MAN` | Zarehouse City Doc Man | VARCHAR2 | 30 |  | Y |
| 12 | `STATE_CODE_DOC_MAN` | State_Code_Docessorial Man | VARCHAR2 | 4 |  | Y |
| 13 | `FRT_DEST_CODE` | Frt_Destessorial Code | VARCHAR2 | 10 |  | Y |
| 14 | `DOC_MAN_ADD4` | Doc_Manessorial Add4 | VARCHAR2 | 30 |  | Y |
| 15 | `COUNTRY_CODE` | Country Code | VARCHAR2 | 4 |  | Y |
| 16 | `EXT_REF_NUM1` | Ext_Refessorial Num1 | VARCHAR2 | 20 |  | Y |
| 17 | `LANG_CODE` | Language Code | VARCHAR2 | 4 |  | Y |

## `M_DOC_ATTR_PROF_D`

- **Tipo:** Master
- **Categoria:** Document
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `DOC_ATTR_PROF_CODE` | Doc_Attr_Professorial Code | VARCHAR2 | 4 |  | N |
| 3 | `DOC_ATTR_PROF_COPY_SEQ_NUM` | Doc_Attr_Prof_Copy_Seqessorial Num | NUMBER | 22 | 2 | N |
| 4 | `DOC_ATTR_PROF_COPY_DES` | Doc_Attr_Prof_Copyessorial Des | VARCHAR2 | 45 |  | Y |

## `M_DOC_ATTR_PROF_H`

- **Tipo:** Master
- **Categoria:** Document
- **Campos:** 8
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `DOC_ATTR_PROF_CODE` | Doc_Attr_Professorial Code | VARCHAR2 | 4 |  | N |
| 3 | `DOC_ATTR_PROF_DES` | Doc_Attr_Professorial Des | VARCHAR2 | 30 |  | N |
| 4 | `DOC_ATTR_PROF_NUM_OF_COPY` | Doc_Attr_Prof_Num_Ofessorial Copy | NUMBER | 22 | 2 | Y |
| 5 | `DOC_ATTR_PROF_DOC_GRP_TP` | Doc_Attr_Prof_Doc_Grpessorial Tp | VARCHAR2 | 2 |  | Y |
| 6 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | Y |
| 7 | `LINEAR_MEAS_CODE` | Linear Measurement Code | VARCHAR2 | 4 |  | Y |
| 8 | `CUBE_MEAS_CODE` | Cube_Measessorial Code | VARCHAR2 | 4 |  | Y |

## `M_DOC_D`

- **Tipo:** Master
- **Categoria:** Document
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `DOC_CODE` | Document Code | VARCHAR2 | 4 |  | N |
| 4 | `PRT_CODE` | Printer Code | VARCHAR2 | 4 |  | N |
| 5 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_DOC_H`

- **Tipo:** Master
- **Categoria:** Document
- **Campos:** 44
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `DOC_CODE` | Document Code | VARCHAR2 | 4 |  | N |
| 4 | `DOC_DES` | Docessorial Des | VARCHAR2 | 30 |  | N |
| 5 | `DOC_STAT` | Docessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `DOC_TP_CODE` | Doc_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 7 | `FORM_CODE` | Form Code | VARCHAR2 | 4 |  | N |
| 8 | `DOC_REPRT_FLAG` | Doc_Reprtessorial Flag | VARCHAR2 | 1 |  | N |
| 9 | `DOC_CNT_REPRT_FLAG` | Doc_Cnt_Reprtessorial Flag | VARCHAR2 | 1 |  | Y |
| 10 | `DOC_FLAG_REPRT_FLAG` | Doc_Flag_Reprtessorial Flag | VARCHAR2 | 1 |  | N |
| 11 | `DOC_REPRT_MES` | Doc_Reprtessorial Mes | VARCHAR2 | 45 |  | Y |
| 12 | `DOC_PRT_MULT_DOC_FLAG` | Doc_Prt_Mult_Docessorial Flag | VARCHAR2 | 1 |  | N |
| 13 | `DOC_PRT_LINE_FLAG` | Doc_Prt_Lineessorial Flag | VARCHAR2 | 1 |  | N |
| 14 | `DOC_FMT_EXE_JOB` | Doc_Fmt_Exeessorial Job | VARCHAR2 | 10 |  | N |
| 15 | `PRT_CODE` | Printer Code | VARCHAR2 | 4 |  | Y |
| 16 | `DOC_FMT_TP_FLAG` | Doc_Fmt_Tpessorial Flag | VARCHAR2 | 1 |  | N |
| 17 | `DOC_DIR` | Docessorial Dir | VARCHAR2 | 60 |  | Y |
| 18 | `DOC_FILE_PREX` | Doc_Fileessorial Prex | VARCHAR2 | 30 |  | Y |
| 19 | `DOC_FILE_SUFX` | Doc_Fileessorial Sufx | VARCHAR2 | 30 |  | Y |
| 20 | `DOC_UPD_FLOW_FLAG` | Doc_Upd_Flowessorial Flag | VARCHAR2 | 1 |  | Y |
| 21 | `PROS_CODE` | Prosessorial Code | VARCHAR2 | 4 |  | Y |
| 22 | `DOC_BARCODE_DIR` | Doc_Barcodeessorial Dir | VARCHAR2 | 60 |  | Y |
| 23 | `DOC_BARCODE_FILE_EXACT` | Doc_Barcode_Fileessorial Exact | VARCHAR2 | 20 |  | Y |
| 24 | `DOC_ID` | Docessorial Id | VARCHAR2 | 2 |  | Y |
| 25 | `FRONT_FAX_OVRL_CODE` | Front_Fax_Ovrlessorial Code | VARCHAR2 | 4 |  | Y |
| 26 | `BACK_FAX_OVRL_CODE` | Back_Fax_Ovrlessorial Code | VARCHAR2 | 4 |  | Y |
| 27 | `DOC_ATTR_PROF_CODE` | Doc_Attr_Professorial Code | VARCHAR2 | 4 |  | Y |
| 28 | `DOC_SIGNATURE_FLAG` | Doc_Signatureessorial Flag | VARCHAR2 | 1 |  | Y |
| 29 | `DOC_COMP_WHSE_ADD_FLAG` | Doc_Comp_Whse_Addessorial Flag | VARCHAR2 | 1 |  | Y |
| 30 | `LABEL_SWARE_LABEL_NAME` | Label_Sware_Labelessorial Name | VARCHAR2 | 100 |  | Y |
| 31 | `LABEL_SWARE_LABEL_NAME_ADD` | Label_Sware_Label_Nameessorial Add | VARCHAR2 | 30 |  | Y |
| 32 | `LABEL_SWARE_LABEL_NAME_SEP` | Label_Sware_Label_Nameessorial Sep | VARCHAR2 | 30 |  | Y |
| 33 | `LABEL_SWARE_SORT_SEQ_CODE` | Label_Sware_Sort_Seqessorial Code | VARCHAR2 | 4 |  | Y |
| 34 | `DOC_PRT_SKIP_ALLOC_FLAG` | Doc_Prt_Skip_Allocessorial Flag | VARCHAR2 | 1 |  | Y |
| 35 | `SKU_CLASS_NUM` | Sku_Classessorial Num | NUMBER | 22 | 1 | Y |
| 36 | `SKU_CLASS_NUM_RND_FLAG` | Sku_Class_Num_Rndessorial Flag | VARCHAR2 | 1 |  | Y |
| 37 | `ORA_REP_EXE_JOB` | Ora_Rep_Exeessorial Job | VARCHAR2 | 40 |  | Y |
| 38 | `DOC_LOAD_FORM_TP` | Doc_Load_Formessorial Tp | VARCHAR2 | 1 |  | Y |
| 39 | `EV_DOC_SUPPRESS_FLAG` | Ev_Doc_Suppressessorial Flag | VARCHAR2 | 1 |  | Y |
| 40 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 41 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 42 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 43 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 44 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_DOC_TP`

- **Tipo:** Master
- **Categoria:** Document
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `DOC_TP_CODE` | Doc_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `DOC_TP_DES` | Doc_Tpessorial Des | VARCHAR2 | 30 |  | N |
| 5 | `DOC_TP_STAT` | Doc_Tpessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `DOC_TP_INB_OUTB_BILL_FLAG` | Doc_Tp_Inb_Outb_Billessorial Flag | VARCHAR2 | 2 |  | N |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_DOC_WHSE_PRT`

- **Tipo:** Master
- **Categoria:** Document
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `DOC_CODE` | Document Code | VARCHAR2 | 4 |  | N |
| 4 | `COMP_CODE_ACTUAL` | Comp_Codeessorial Actual | VARCHAR2 | 2 |  | N |
| 5 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 6 | `PRT_CODE` | Printer Code | VARCHAR2 | 4 |  | N |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

