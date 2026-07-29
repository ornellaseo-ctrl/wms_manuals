# Tabelas — Appointment

> Categoria extraída da planilha `Tables-Database.xlsx`. Total de tabelas: **12**.

## `C_A1SCH_INTFACE_APPO`

- **Tipo:** Transactional
- **Categoria:** Appointment
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

## `C_A1SCH_INTFACE_APPO_DOC`

- **Tipo:** Transactional
- **Categoria:** Appointment
- **Campos:** 5
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `INTFACE_SEQ_NUM` | Intface_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `INTFACE_SEQ_NUM_APPO` | Intface_Seq_Numessorial Appo | NUMBER | 22 | 9 | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `DOC_NUM` | Document Number | NUMBER | 22 | 9 | Y |
| 5 | `DOC_TP_FLAG` | Doc_Tpessorial Flag | VARCHAR2 | 1 |  | Y |

## `C_A1SCH_INTFACE_APPO_STAT`

- **Tipo:** Transactional
- **Categoria:** Appointment
- **Campos:** 9

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `INTFACE_SEQ_NUM` | Intface_Seqessorial Num | NUMBER | 22 | 9 | N |
| 2 | `APPO_A1SCH_ID` | Appo_A1Schessorial Id | VARCHAR2 | 100 |  | N |
| 3 | `APPO_STAT_DATE` | Appo_Statessorial Date | DATE | 7 |  | N |
| 4 | `APPO_STAT` | Appoessorial Stat | VARCHAR2 | 1 |  | N |
| 5 | `CREATE_DATE` | Create Date | DATE | 7 |  | N |
| 6 | `PROS_DATE` | Prosessorial Date | DATE | 7 |  | Y |
| 7 | `PROS_FLAG` | Prosessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `ERR_MES` | Erressorial Mes | VARCHAR2 | 250 |  | Y |
| 9 | `APPO_A1SCH_STAT` | Appo_A1Schessorial Stat | VARCHAR2 | 100 |  | Y |

## `C_API_ORD_LINE`

- **Tipo:** Transactional
- **Categoria:** Appointment
- **Campos:** 6
- **Campos-chave prováveis:** COMP_CODE, ORD_NUM

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `ORD_NUM` | Order Number | NUMBER | 22 | 9 | N |
| 3 | `ORD_LINE_NUM` | Order Line Number | NUMBER | 22 | 4 | N |
| 4 | `ORD_SHIP_QTY` | Ord_Shipessorial Qty | NUMBER | 22 | 9 | N |
| 5 | `API_ORD_LINE_PROS_DATE` | Api_Ord_Line_Prosessorial Date | DATE | 7 |  | Y |
| 6 | `API_ORD_LINE_PROS_FLAG` | Api_Ord_Line_Prosessorial Flag | VARCHAR2 | 1 |  | N |

## `C_APPO_SLOT`

- **Tipo:** Transactional
- **Categoria:** Appointment
- **Campos:** 6
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `APPO_NUM` | Appointment Number | NUMBER | 22 | 6 | N |
| 3 | `BLDG_CODE` | Building Code | VARCHAR2 | 4 |  | N |
| 4 | `DOOR_CODE` | Door Code | VARCHAR2 | 4 |  | Y |
| 5 | `APPO_START_DATE` | Appo_Startessorial Date | DATE | 7 |  | Y |
| 6 | `APPO_END_DATE` | Appo_Endessorial Date | DATE | 7 |  | Y |

## `C_APPO_TIME`

- **Tipo:** Transactional
- **Categoria:** Appointment
- **Campos:** 9
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `APPO_NUM` | Appointment Number | NUMBER | 22 | 6 | N |
| 3 | `APPO_INB_OUTB_FLAG` | Appo_Inb_Outbessorial Flag | VARCHAR2 | 1 |  | N |
| 4 | `APPO_TP_FLAG` | Appo_Tpessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `APPO_TP_DATE` | Appo_Tpessorial Date | DATE | 7 |  | N |
| 6 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 7 | `APPO_DATE` | Appointment Date | DATE | 7 |  | N |
| 8 | `APPO_DATE_ORIG` | Appo_Dateessorial Orig | DATE | 7 |  | Y |
| 9 | `REAS_CODE` | Reasessorial Code | VARCHAR2 | 4 |  | Y |

## `E_APPO_D`

- **Tipo:** Transactional
- **Categoria:** Appointment
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `APPO_NUM` | Appointment Number | NUMBER | 22 | 6 | N |
| 3 | `APPO_INB_OUTB_FLAG` | Appo_Inb_Outbessorial Flag | VARCHAR2 | 1 |  | N |
| 4 | `DOC_NUM` | Document Number | NUMBER | 22 | 9 | N |

## `E_APPO_H`

- **Tipo:** Transactional
- **Categoria:** Appointment
- **Campos:** 57
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `APPO_NUM` | Appointment Number | NUMBER | 22 | 6 | N |
| 3 | `LOAD_TP_CODE` | Load Type Code | VARCHAR2 | 4 |  | N |
| 4 | `APPO_INB_OUTB_FLAG` | Appo_Inb_Outbessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `FAX_CODE` | Faxessorial Code | VARCHAR2 | 10 |  | N |
| 6 | `FAX_TP` | Faxessorial Tp | VARCHAR2 | 4 |  | N |
| 7 | `FAX_NAME_MAN` | Fax_Nameessorial Man | VARCHAR2 | 30 |  | Y |
| 8 | `DOC_NUM` | Document Number | NUMBER | 22 | 9 | Y |
| 9 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | N |
| 10 | `CARR_NAME_MAN` | Carr_Nameessorial Man | VARCHAR2 | 30 |  | Y |
| 11 | `APPO_REF_NUM` | Appo_Refessorial Num | VARCHAR2 | 20 |  | Y |
| 12 | `BLDG_CODE` | Building Code | VARCHAR2 | 4 |  | N |
| 13 | `APPO_DATE` | Appointment Date | DATE | 7 |  | N |
| 14 | `OP_CODE_SCH` | Op_Codeessorial Sch | VARCHAR2 | 20 |  | N |
| 15 | `APPO_CONTACT` | Appoessorial Contact | VARCHAR2 | 30 |  | Y |
| 16 | `APPO_WHS_SUPERVISOR` | Appo_Whsessorial Supervisor | VARCHAR2 | 30 |  | Y |
| 17 | `APPO_WGT` | Appoessorial Wgt | NUMBER | 22 | 16 | Y |
| 18 | `WGT_MEAS_CODE` | Weight Measurement Code | VARCHAR2 | 4 |  | Y |
| 19 | `APPO_QTY` | Appoessorial Qty | NUMBER | 22 | 9 | Y |
| 20 | `SKU_CLASS_NUM` | Sku_Classessorial Num | NUMBER | 22 | 1 | Y |
| 21 | `APPO_START_DATE` | Appo_Startessorial Date | DATE | 7 |  | Y |
| 22 | `APPO_END_DATE` | Appo_Endessorial Date | DATE | 7 |  | Y |
| 23 | `APPO_LAPSE_TIME` | Appo_Lapseessorial Time | NUMBER | 22 | 5 | N |
| 24 | `DOOR_CODE` | Door Code | VARCHAR2 | 4 |  | Y |
| 25 | `APPO_DES` | Appoessorial Des | VARCHAR2 | 30 |  | Y |
| 26 | `APPO_CANCEL_DATE` | Appo_Cancelessorial Date | DATE | 7 |  | Y |
| 27 | `APPO_DELETE_DATE` | Appo_Deleteessorial Date | DATE | 7 |  | Y |
| 28 | `APPO_ARRIVE_DATE` | Appo_Arriveessorial Date | DATE | 7 |  | Y |
| 29 | `APPO_COMPLETE_DATE` | Appo_Completeessorial Date | DATE | 7 |  | Y |
| 30 | `APPO_STAT` | Appoessorial Stat | VARCHAR2 | 1 |  | Y |
| 31 | `REAS_CODE` | Reasessorial Code | VARCHAR2 | 4 |  | Y |
| 32 | `APPO_NUM_PARENT` | Appo_Numessorial Parent | NUMBER | 22 | 6 | Y |
| 33 | `APPO_STDNG_PARENT_FLAG` | Appo_Stdng_Parentessorial Flag | VARCHAR2 | 1 |  | Y |
| 34 | `APPO_STDNG_FREQ_TP` | Appo_Stdng_Freqessorial Tp | VARCHAR2 | 1 |  | Y |
| 35 | `APPO_STDNG_END_DATE` | Appo_Stdng_Endessorial Date | DATE | 7 |  | Y |
| 36 | `APPO_STDNG_PARENT_APPO_NUM` | Appo_Stdng_Parent_Appoessorial Num | NUMBER | 22 | 6 | Y |
| 37 | `APPO_REM` | Appoessorial Rem | VARCHAR2 | 1000 |  | Y |
| 38 | `APPO_DROP_TRLR_FLAG` | Appo_Drop_Trlressorial Flag | VARCHAR2 | 1 |  | Y |
| 39 | `APPO_A1SCHEDULE_ID` | Appo_A1Scheduleessorial Id | VARCHAR2 | 100 |  | Y |
| 40 | `APPO_A1SCHEDULE_NUM` | Appo_A1Scheduleessorial Num | VARCHAR2 | 100 |  | Y |
| 41 | `APPO_A1SCHEDULE_STAT` | Appo_A1Scheduleessorial Stat | VARCHAR2 | 100 |  | Y |
| 42 | `APPO_A1SCHEDULE_CONTAIN_ID` | Appo_A1Schedule_Containessorial Id | VARCHAR2 | 50 |  | Y |
| 43 | `APPO_A1SCHEDULE_CONTAIN_SEAL` | Appo_A1Schedule_Containessorial Seal | VARCHAR2 | 50 |  | Y |
| 44 | `VEH_TP_CODE` | Veh_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 45 | `APPO_ALT_REF1` | Appo_Altessorial Ref1 | VARCHAR2 | 20 |  | Y |
| 46 | `APPO_ALT_REF2` | Appo_Altessorial Ref2 | VARCHAR2 | 20 |  | Y |
| 47 | `APPO_ALT_REF3` | Appo_Altessorial Ref3 | VARCHAR2 | 20 |  | Y |
| 48 | `APPO_ALT_REF4` | Appo_Altessorial Ref4 | VARCHAR2 | 20 |  | Y |
| 49 | `APPO_BLDG_DATE` | Appo_Bldgessorial Date | DATE | 7 |  | Y |
| 50 | `APPO_DOOR_DATE` | Appo_Dooressorial Date | DATE | 7 |  | Y |
| 51 | `APPO_PLT_NUM` | Appo_Pltessorial Num | NUMBER | 22 | 6 | Y |
| 52 | `APPO_LIFT_NUM` | Appo_Liftessorial Num | NUMBER | 22 | 6 | Y |
| 53 | `APPO_MASS_RULE_FLAG` | Appo_Mass_Ruleessorial Flag | VARCHAR2 | 1 |  | Y |
| 54 | `APPO_ALLOW_GVM_GCM_FLAG` | Appo_Allow_Gvm_Gcmessorial Flag | VARCHAR2 | 1 |  | Y |
| 55 | `APPO_CARRY_CAPC` | Appo_Carryessorial Capc | NUMBER | 22 | 16 | Y |
| 56 | `APPO_EQP_WGT` | Appo_Eqpessorial Wgt | NUMBER | 22 | 16 | Y |
| 57 | `APPO_INSPECT_FLAG` | Appo_Inspectessorial Flag | VARCHAR2 | 1 |  | Y |

## `E_APPO_UNLOAD_LOC`

- **Tipo:** Transactional
- **Categoria:** Appointment
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE, LOC_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `APPO_NUM` | Appointment Number | NUMBER | 22 | 6 | N |
| 4 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 5 | `LOC_CODE` | Location Code | VARCHAR2 | 12 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `S_APP_PROP_D`

- **Tipo:** System Setup Related
- **Categoria:** Appointment
- **Campos:** 11

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `APP_CODE` | Application Code | VARCHAR2 | 30 |  | N |
| 3 | `APP_PROP_CODE` | App_Propessorial Code | VARCHAR2 | 60 |  | N |
| 4 | `APP_PROP_OPT_NUM` | App_Prop_Optessorial Num | NUMBER | 22 | 4 | N |
| 5 | `APP_PROP_OPT_DES` | App_Prop_Optessorial Des | VARCHAR2 | 80 |  | N |
| 6 | `APP_PROP_OPT_VAL` | App_Prop_Optessorial Val | VARCHAR2 | 20 |  | N |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `S_APP_PROP_H`

- **Tipo:** System Setup Related
- **Categoria:** Appointment
- **Campos:** 30

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `APP_CODE` | Application Code | VARCHAR2 | 30 |  | N |
| 3 | `APP_PROP_CODE` | App_Propessorial Code | VARCHAR2 | 60 |  | N |
| 4 | `APP_PROP_SEQ_NUM` | App_Prop_Seqessorial Num | NUMBER | 22 | 4 | N |
| 5 | `APP_PROP_GRP_CODE` | App_Prop_Grpessorial Code | VARCHAR2 | 4 |  | N |
| 6 | `APP_PROP_DES` | App_Propessorial Des | VARCHAR2 | 60 |  | N |
| 7 | `APP_PROP_HELP` | App_Propessorial Help | VARCHAR2 | 80 |  | Y |
| 8 | `APP_PROP_TP` | App_Propessorial Tp | VARCHAR2 | 1 |  | Y |
| 9 | `APP_PROP_LEN` | App_Propessorial Len | NUMBER | 22 | 3 | Y |
| 10 | `APP_PROP_DEF_VAL` | App_Prop_Defessorial Val | VARCHAR2 | 20 |  | Y |
| 11 | `APP_PROP_MAND_FLAG` | App_Prop_Mandessorial Flag | VARCHAR2 | 1 |  | Y |
| 12 | `APP_PROP_TEXT_FLAG` | App_Prop_Textessorial Flag | VARCHAR2 | 1 |  | Y |
| 13 | `APP_PROP_TEXT_VALIDATION` | App_Prop_Textessorial Validation | VARCHAR2 | 80 |  | Y |
| 14 | `APP_PROP_ERR_MES` | App_Prop_Erressorial Mes | VARCHAR2 | 80 |  | Y |
| 15 | `APP_PROP_TRACE_FLAG` | App_Prop_Traceessorial Flag | VARCHAR2 | 1 |  | Y |
| 16 | `PICKLIST_CODE` | Picklistessorial Code | VARCHAR2 | 10 |  | Y |
| 17 | `PICKLIST_SEQ_NUM` | Picklist_Seqessorial Num | NUMBER | 22 | 2 | Y |
| 18 | `PICKLIST_PARAM_3` | Picklist_Paramessorial 3 | VARCHAR2 | 30 |  | Y |
| 19 | `PICKLIST_PARAM_4` | Picklist_Paramessorial 4 | VARCHAR2 | 30 |  | Y |
| 20 | `PICKLIST_PARAM_5` | Picklist_Paramessorial 5 | VARCHAR2 | 30 |  | Y |
| 21 | `PICKLIST_PARAM_6` | Picklist_Paramessorial 6 | VARCHAR2 | 30 |  | Y |
| 22 | `PICKLIST_PARAM_7` | Picklist_Paramessorial 7 | VARCHAR2 | 30 |  | Y |
| 23 | `PICKLIST_PARAM_8` | Picklist_Paramessorial 8 | VARCHAR2 | 30 |  | Y |
| 24 | `APP_PROP_TABLE_NAME` | App_Prop_Tableessorial Name | VARCHAR2 | 30 |  | Y |
| 25 | `APP_PROP_READ_ONLY_FLAG` | App_Prop_Read_Onlyessorial Flag | VARCHAR2 | 1 |  | Y |
| 26 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 27 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 28 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 29 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 30 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `S_APP_VERS`

- **Tipo:** System Setup Related
- **Categoria:** Appointment
- **Campos:** 2

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `APP_CODE` | Application Code | VARCHAR2 | 30 |  | N |
| 2 | `VERS_CODE` | Versessorial Code | VARCHAR2 | 30 |  | N |

