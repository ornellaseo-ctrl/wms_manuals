# Tabelas — Carrier

> Categoria extraída da planilha `Tables-Database.xlsx`. Total de tabelas: **8**.

## `C_A1SCH_INTFACE_CARR`

- **Tipo:** Transactional
- **Categoria:** Carrier
- **Campos:** 9
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | N |
| 3 | `CARR_NAME` | Carrier Name | VARCHAR2 | 30 |  | N |
| 4 | `CARR_STAT` | Carressorial Stat | VARCHAR2 | 1 |  | N |
| 5 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 6 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 20 |  | Y |
| 7 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 8 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 20 |  | Y |
| 9 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_CARR_D1`

- **Tipo:** Master
- **Categoria:** Carrier
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | N |
| 4 | `FRT_MOTOR_CARR_CODE` | Frt_Motor_Carressorial Code | VARCHAR2 | 20 |  | N |
| 5 | `FRT_TP_CODE` | Frt_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_CARR_D2`

- **Tipo:** Master
- **Categoria:** Carrier
- **Campos:** 13
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | N |
| 4 | `CARR_FRT_INS_POL_CODE` | Carr_Frt_Ins_Polessorial Code | VARCHAR2 | 20 |  | N |
| 5 | `CARR_FRT_INS_DES` | Carr_Frt_Insessorial Des | VARCHAR2 | 30 |  | N |
| 6 | `CARR_FRT_INS_DED_AMT` | Carr_Frt_Ins_Dedessorial Amt | NUMBER | 22 | 9 | N |
| 7 | `CARR_FRT_INS_EFF_DATE` | Carr_Frt_Ins_Effessorial Date | DATE | 7 |  | N |
| 8 | `CARR_FRT_INS_EXPY_DATE` | Carr_Frt_Ins_Expyessorial Date | DATE | 7 |  | N |
| 9 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 10 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 12 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 13 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_CARR_D2_TEMP`

- **Tipo:** Master
- **Categoria:** Carrier
- **Campos:** 7
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | N |
| 3 | `CARR_FRT_INS_POL_CODE` | Carr_Frt_Ins_Polessorial Code | VARCHAR2 | 20 |  | N |
| 4 | `CARR_FRT_INS_DES` | Carr_Frt_Insessorial Des | VARCHAR2 | 30 |  | N |
| 5 | `CARR_FRT_INS_DED_AMT` | Carr_Frt_Ins_Dedessorial Amt | NUMBER | 22 | 9 | N |
| 6 | `CARR_FRT_INS_EFF_DATE` | Carr_Frt_Ins_Effessorial Date | DATE | 7 |  | N |
| 7 | `CARR_FRT_INS_EXP_DATE` | Carr_Frt_Ins_Expessorial Date | DATE | 7 |  | N |

## `M_CARR_H`

- **Tipo:** Master
- **Categoria:** Carrier
- **Campos:** 46
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | N |
| 4 | `CARR_NAME` | Carrier Name | VARCHAR2 | 30 |  | N |
| 5 | `CARR_STAT` | Carressorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `CARR_ADD1` | Carressorial Add1 | VARCHAR2 | 30 |  | N |
| 7 | `CARR_ADD2` | Carressorial Add2 | VARCHAR2 | 30 |  | Y |
| 8 | `CARR_ADD3` | Carressorial Add3 | VARCHAR2 | 30 |  | Y |
| 9 | `ZIP_CODE` | Zip Code | VARCHAR2 | 10 |  | N |
| 10 | `CARR_WGT_MEAS_FLAG` | Carr_Wgt_Measessorial Flag | VARCHAR2 | 1 |  | N |
| 11 | `MES_CODE` | Message Code | VARCHAR2 | 4 |  | Y |
| 12 | `CARR_CODE_PAY` | Carr_Codeessorial Pay | VARCHAR2 | 10 |  | Y |
| 13 | `FRT_TP_CODE` | Frt_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 14 | `CARR_FRT_MIN_AMT` | Carr_Frt_Minessorial Amt | NUMBER | 22 | 9 | Y |
| 15 | `CARR_FRT_MILE_AMT` | Carr_Frt_Mileessorial Amt | NUMBER | 22 | 11 | Y |
| 16 | `CARR_FRT_DISC_PCENT` | Carr_Frt_Discessorial Pcent | NUMBER | 22 | 6 | Y |
| 17 | `CARR_LAST_ACT_DATE` | Carr_Last_Actessorial Date | DATE | 7 |  | Y |
| 18 | `CARR_STD_ALPHA_CODE` | Carr_Std_Alphaessorial Code | VARCHAR2 | 4 |  | N |
| 19 | `CARR_TP_CODE` | Carr_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 20 | `GEN_NUM_PROF_CODE` | Gen_Num_Professorial Code | VARCHAR2 | 4 |  | Y |
| 21 | `EXTRA_CHG_PROF_CODE` | Extra_Chg_Professorial Code | VARCHAR2 | 4 |  | Y |
| 22 | `CARR_LAB_STD_MODY_NUM` | Carr_Lab_Std_Modyessorial Num | NUMBER | 22 | 4 | Y |
| 23 | `CARR_ADD4` | Carressorial Add4 | VARCHAR2 | 30 |  | Y |
| 24 | `COUNTRY_CODE` | Country Code | VARCHAR2 | 4 |  | N |
| 25 | `EDI_PROF_CODE` | Edi_Professorial Code | VARCHAR2 | 4 |  | Y |
| 26 | `TRSPT_MODE_CODE` | Trspt_Modeessorial Code | VARCHAR2 | 4 |  | Y |
| 27 | `ISOL_CODE` | ISOL Code | VARCHAR2 | 4 |  | Y |
| 28 | `YARD_LOC_PROF_CODE` | Yarehouse Loc Prof Code | VARCHAR2 | 4 |  | Y |
| 29 | `TRSPT_UNIT_VAL_HIST_FLAG` | Trspt_Unit_Val_Histessorial Flag | VARCHAR2 | 1 |  | N |
| 30 | `CARR_EXT_FRT_FLAG` | Carr_Ext_Frtessorial Flag | VARCHAR2 | 1 |  | Y |
| 31 | `SKU_CLASS_NUM` | Sku_Classessorial Num | NUMBER | 22 | 1 | Y |
| 32 | `SKU_CLASS_NUM_RND_FLAG` | Sku_Class_Num_Rndessorial Flag | VARCHAR2 | 1 |  | Y |
| 33 | `CARR_ALLOW_BANDING_FLAG` | Carr_Allow_Bandingessorial Flag | VARCHAR2 | 1 |  | Y |
| 34 | `CARR_COMPL_LABEL_FLAG` | Carr_Compl_Labelessorial Flag | VARCHAR2 | 1 |  | Y |
| 35 | `CARR_REQ_EDI_FLAG` | Carr_Req_Ediessorial Flag | VARCHAR2 | 1 |  | Y |
| 36 | `CARR_TP_TRUE_CODE` | Carr_Tp_Trueessorial Code | VARCHAR2 | 4 |  | Y |
| 37 | `CARR_SKIP_CARTZN_FLAG` | Carr_Skip_Cartznessorial Flag | VARCHAR2 | 1 |  | Y |
| 38 | `CARR_A1SHIP_REF_NUM` | Carr_A1Ship_Refessorial Num | VARCHAR2 | 250 |  | Y |
| 39 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 40 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 41 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 42 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 43 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 44 | `CARR_DATA_SERVICE_ID` | Carr_Data_Serviceessorial Id | VARCHAR2 | 100 |  | Y |
| 45 | `CARR_PARCEL_IND_CART_ALLOW` | Carr_Parcel_Ind_Cartessorial Allow | VARCHAR2 | 1 |  | Y |
| 46 | `ZIP_ID` | Zip ID | RAW | 32 |  | N |

## `M_CARR_SHIP_LANE`

- **Tipo:** Master
- **Categoria:** Carrier
- **Campos:** 3
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | N |
| 3 | `SHIP_LANE_CODE` | Ship_Laneessorial Code | VARCHAR2 | 4 |  | N |

## `M_SCAC_CART_SIZE_FLAT_BOX`

- **Tipo:** Master
- **Categoria:** Carrier
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `SCAC_CODE` | Scacessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `CART_SIZE_CODE` | Cart_Sizeessorial Code | VARCHAR2 | 4 |  | N |
| 5 | `FLAT_BOX_TP_CODE` | Flat_Box_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_SCAC_CUST_ACC`

- **Tipo:** Master
- **Categoria:** Carrier
- **Campos:** 12
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `SCAC_CODE` | Scacessorial Code | VARCHAR2 | 4 |  | N |
| 3 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 4 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 5 | `COMM_ADD1` | Commessorial Add1 | VARCHAR2 | 20 |  | Y |
| 6 | `COMM_ADD2` | Commessorial Add2 | VARCHAR2 | 20 |  | Y |
| 7 | `ACC_PARTIT_1` | Acc_Partitessorial 1 | VARCHAR2 | 20 |  | N |
| 8 | `ACC_PARTIT_2` | Acc_Partitessorial 2 | VARCHAR2 | 20 |  | Y |
| 9 | `ACC_PARTIT_3` | Acc_Partitessorial 3 | VARCHAR2 | 20 |  | Y |
| 10 | `ACC_PARTIT_4` | Acc_Partitessorial 4 | VARCHAR2 | 20 |  | Y |
| 11 | `ACC_PARTIT_5` | Acc_Partitessorial 5 | VARCHAR2 | 20 |  | Y |
| 12 | `MAN_NUM_CODE` | Man_Numessorial Code | VARCHAR2 | 4 |  | Y |

