# Tabelas — User

> Categoria extraída da planilha `Tables-Database.xlsx`. Total de tabelas: **29**.

## `C_OP_ATTEND`

- **Tipo:** Transactional
- **Categoria:** User
- **Campos:** 19
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 3 | `OP_ATTEND_DATE` | Op_Attendessorial Date | DATE | 7 |  | N |
| 4 | `OP_ATTEND_START_DATE` | Op_Attend_Startessorial Date | DATE | 7 |  | N |
| 5 | `OP_ATTEND_END_DATE` | Op_Attend_Endessorial Date | DATE | 7 |  | N |
| 6 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 7 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 8 | `WHSE_SHIFT_CODE` | Warehouse Shift Code | VARCHAR2 | 4 |  | N |
| 9 | `OP_ATTEND_SHIFT_START_FLAG` | Op_Attend_Shift_Startessorial Flag | VARCHAR2 | 1 |  | N |
| 10 | `OP_ATTEND_SHIFT_END_FLAG` | Op_Attend_Shift_Endessorial Flag | VARCHAR2 | 1 |  | N |
| 11 | `OP_ATTEND_ATTEND_ID` | Op_Attend_Attendessorial Id | VARCHAR2 | 100 |  | N |
| 12 | `OP_ATTEND_VERSION` | Op_Attendessorial Version | NUMBER | 22 | 4 | Y |
| 13 | `AUDIT_NUM` | Audit Number | NUMBER | 22 | 6 | Y |
| 14 | `OP_ATTEND_AUDIT_DATE` | Op_Attend_Auditessorial Date | DATE | 7 |  | Y |
| 15 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 16 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 17 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 18 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 19 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `C_OP_SEL_AUD`

- **Tipo:** Transactional
- **Categoria:** User
- **Campos:** 9
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `SEL_CODE` | Selessorial Code | VARCHAR2 | 6 |  | N |
| 4 | `SEL_READ_ONLY_FLAG` | Sel_Read_Onlyessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `SEL_RUN_DATE` | Sel_Runessorial Date | DATE | 7 |  | N |
| 6 | `SEL_END_DATE` | Sel_Endessorial Date | DATE | 7 |  | Y |
| 7 | `OP_SEL_AUD_NUM` | Op_Sel_Audessorial Num | NUMBER | 22 | 6 | Y |
| 8 | `TER_CODE` | Teressorial Code | VARCHAR2 | 10 |  | Y |
| 9 | `MHE_CODE` | Mheessorial Code | VARCHAR2 | 10 |  | Y |

## `M_EMP_PAY_FACT`

- **Tipo:** Master
- **Categoria:** User
- **Campos:** 4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `OP_CODE_EMP` | Op_Codeessorial Emp | VARCHAR2 | 20 |  | N |
| 2 | `EMP_PAY_FACT` | Emp_Payessorial Fact | NUMBER | 22 | 5 | N |
| 3 | `EMP_PAY_FACT_DES` | Emp_Pay_Factessorial Des | VARCHAR2 | 30 |  | N |
| 4 | `EMP_PAY_FACT_STAT` | Emp_Pay_Factessorial Stat | VARCHAR2 | 1 |  | N |

## `M_OP`

- **Tipo:** Master
- **Categoria:** User
- **Campos:** 36
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 3 | `OP_NAME` | Opessorial Name | VARCHAR2 | 30 |  | N |
| 4 | `OP_STAT` | Opessorial Stat | VARCHAR2 | 1 |  | N |
| 5 | `OP_PWORD` | Opessorial Pword | RAW | 128 |  | Y |
| 6 | `OP_DBA_FLAG` | Op_Dbaessorial Flag | VARCHAR2 | 1 |  | Y |
| 7 | `OP_EMP_FLAG` | Op_Empessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | Y |
| 9 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | Y |
| 10 | `MHE_TP_CODE` | Mhe_Tpessorial Code | VARCHAR2 | 4 |  | Y |
| 11 | `MHE_CODE` | Mheessorial Code | VARCHAR2 | 10 |  | Y |
| 12 | `EMP_LAB_CAPT_FLAG` | Emp_Lab_Captessorial Flag | VARCHAR2 | 1 |  | Y |
| 13 | `WHSE_SHIFT_CODE` | Warehouse Shift Code | VARCHAR2 | 4 |  | Y |
| 14 | `EMP_HOURS` | Empessorial Hours | NUMBER | 22 | 8 | Y |
| 15 | `EMP_TEMPY_FLAG` | Emp_Tempyessorial Flag | VARCHAR2 | 1 |  | Y |
| 16 | `EMP_SUPERVISOR_FLAG` | Emp_Supervisoressorial Flag | VARCHAR2 | 1 |  | Y |
| 17 | `EMP_AUTHORITY_FLAG` | Emp_Authorityessorial Flag | VARCHAR2 | 1 |  | N |
| 18 | `EMP_LAB_STD_MODY_NUM` | Emp_Lab_Std_Modyessorial Num | NUMBER | 22 | 4 | Y |
| 19 | `EMP_HOURLY_PAY` | Emp_Hourlyessorial Pay | NUMBER | 22 | 8 | Y |
| 20 | `OP_PWORD_DATE` | Op_Pwordessorial Date | DATE | 7 |  | N |
| 21 | `LANG_CODE` | Language Code | VARCHAR2 | 4 |  | N |
| 22 | `SYVOX_WORK_CLASS_CODE` | Syvox_Work_Classessorial Code | VARCHAR2 | 4 |  | Y |
| 23 | `SYVOX_EMP_ID` | Syvox_Empessorial Id | NUMBER | 22 | 6 | Y |
| 24 | `OP_EMAIL_ADD` | Op_Emailessorial Add | VARCHAR2 | 60 |  | Y |
| 25 | `SHOW_FIELD_FLAG` | Show_Fieldessorial Flag | VARCHAR2 | 1 |  | N |
| 26 | `OP_GRP_CODE` | Op_Grpessorial Code | VARCHAR2 | 4 |  | Y |
| 27 | `OP_ENTRY_CHG_RATE_REST_FLAG` | Op_Entry_Chg_Rate_Restessorial Flag | VARCHAR2 | 1 |  | Y |
| 28 | `OP_EXT_REF_NUM1` | Op_Ext_Refessorial Num1 | VARCHAR2 | 20 |  | Y |
| 29 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 30 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 31 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 32 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 33 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 34 | `OP_ARCH_DISP_FLAG` | Op_Arch_Dispessorial Flag | VARCHAR2 | 1 |  | Y |
| 35 | `WS_USER_EMAIL_ADD` | Warehouse User Email Add | VARCHAR2 | 256 |  | Y |
| 36 | `WS_USER_ID` | Warehouse User Id | VARCHAR2 | 100 |  | Y |

## `M_OP_APP_D`

- **Tipo:** Master
- **Categoria:** User
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `FUNC_CODE` | Funcessorial Code | VARCHAR2 | 20 |  | N |
| 5 | `REGION_CODE` | Region Code | VARCHAR2 | 20 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_OP_APP_H`

- **Tipo:** Master
- **Categoria:** User
- **Campos:** 10

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 3 | `OP_DEF_COMP_CODE` | Op_Def_Compessorial Code | VARCHAR2 | 2 |  | N |
| 4 | `OP_VOICE_PWORD` | Op_Voiceessorial Pword | VARCHAR2 | 10 |  | N |
| 5 | `OP_APP_STAT` | Op_Appessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_OP_APP_MHE_TP_EXCL`

- **Tipo:** Master
- **Categoria:** User
- **Campos:** 8

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 3 | `MHE_TP_CODE_EXCL` | Mhe_Tp_Codeessorial Excl | VARCHAR2 | 4 |  | N |
| 4 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 5 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 6 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 7 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_OP_CALD`

- **Tipo:** Master
- **Categoria:** User
- **Campos:** 6
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 2 | `OP_REST_CALD_DATE` | Op_Rest_Caldessorial Date | DATE | 7 |  | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `WHSE_CODE` | Warehouse Code | VARCHAR2 | 4 |  | N |
| 5 | `WHSE_SHIFT_CODE` | Warehouse Shift Code | VARCHAR2 | 4 |  | Y |
| 6 | `OP_CALD_HOUR` | Op_Caldessorial Hour | NUMBER | 22 | 3 | N |

## `M_OP_COMP`

- **Tipo:** Master
- **Categoria:** User
- **Campos:** 8
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 5 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 6 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 7 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_OP_COMP_CARR_REST`

- **Tipo:** Master
- **Categoria:** User
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `CARR_CODE` | Carrier Code | VARCHAR2 | 10 |  | N |
| 5 | `OP_COMP_CARR_REST_TP_FLAG` | Op_Comp_Carr_Rest_Tpessorial Flag | VARCHAR2 | 1 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_OP_COMP_CON_REST`

- **Tipo:** Master
- **Categoria:** User
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `CON_CODE` | Consignee Code | VARCHAR2 | 10 |  | N |
| 5 | `OP_COMP_CON_REST_TP_FLAG` | Op_Comp_Con_Rest_Tpessorial Flag | VARCHAR2 | 1 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_OP_COMP_CUST_REST`

- **Tipo:** Master
- **Categoria:** User
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE, CUST_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `CUST_CODE` | Customer Code | VARCHAR2 | 10 |  | N |
| 5 | `OP_COMP_CUST_REST_TP_FLAG` | Op_Comp_Cust_Rest_Tpessorial Flag | VARCHAR2 | 1 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_OP_COMP_DOC_REST`

- **Tipo:** Master
- **Categoria:** User
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `DOC_CODE` | Document Code | VARCHAR2 | 4 |  | N |
| 5 | `OP_COMP_DOC_REST_TP_FLAG` | Op_Comp_Doc_Rest_Tpessorial Flag | VARCHAR2 | 1 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_OP_COMP_REST`

- **Tipo:** Master
- **Categoria:** User
- **Campos:** 9
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `OP_COMP_REST_TP_FLAG` | Op_Comp_Rest_Tpessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 6 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 7 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 8 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_OP_COMP_SHIP_REST`

- **Tipo:** Master
- **Categoria:** User
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `SHIP_CODE` | Shipper Code | VARCHAR2 | 10 |  | N |
| 5 | `OP_COMP_SHIP_REST_TP_FLAG` | Op_Comp_Ship_Rest_Tpessorial Flag | VARCHAR2 | 1 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_OP_D`

- **Tipo:** Master
- **Categoria:** User
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `JOB_FUN_CODE` | Job_Funessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `CHG_CODE` | Charge Code | VARCHAR2 | 4 |  | N |

## `M_OP_GRP`

- **Tipo:** Master
- **Categoria:** User
- **Campos:** 3

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `OP_GRP_CODE` | Op_Grpessorial Code | VARCHAR2 | 4 |  | N |
| 2 | `OP_GRP_DES` | Op_Grpessorial Des | VARCHAR2 | 30 |  | N |
| 3 | `OP_GRP_STAT` | Op_Grpessorial Stat | VARCHAR2 | 1 |  | N |

## `M_OP_PRT`

- **Tipo:** Master
- **Categoria:** User
- **Campos:** 3

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 2 | `DOC_TP` | Docessorial Tp | VARCHAR2 | 10 |  | N |
| 3 | `PRT_CODE` | Printer Code | VARCHAR2 | 4 |  | N |

## `M_OP_PRT_REST`

- **Tipo:** Master
- **Categoria:** User
- **Campos:** 8

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 3 | `PRT_CODE` | Printer Code | VARCHAR2 | 4 |  | N |
| 4 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 5 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 6 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 7 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_OP_QU_PARAM_D`

- **Tipo:** Master
- **Categoria:** User
- **Campos:** 3

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `OP_QU_PARAM_ID` | Op_Qu_Paramessorial Id | NUMBER | 22 | 6 | N |
| 2 | `OP_QU_PARAM_PROP_CODE` | Op_Qu_Param_Propessorial Code | VARCHAR2 | 30 |  | N |
| 3 | `OP_QU_PARAM_PROP_VAL` | Op_Qu_Param_Propessorial Val | VARCHAR2 | 40 |  | Y |

## `M_OP_QU_PARAM_H`

- **Tipo:** Master
- **Categoria:** User
- **Campos:** 6
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `OP_QU_PARAM_ID` | Op_Qu_Paramessorial Id | NUMBER | 22 | 6 | N |
| 2 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 3 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 4 | `OP_QU_PARAM_NAME` | Op_Qu_Paramessorial Name | VARCHAR2 | 20 |  | N |
| 5 | `OP_QU_PARAM_AUTO_QU_FLAG` | Op_Qu_Param_Auto_Quessorial Flag | VARCHAR2 | 1 |  | Y |
| 6 | `EXE_JOB_CODE` | Exe_Jobessorial Code | VARCHAR2 | 30 |  | N |

## `M_OP_REST_JOB`

- **Tipo:** Master
- **Categoria:** User
- **Campos:** 5
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `JOB_TYPE_CODE` | Job_Typeessorial Code | VARCHAR2 | 2 |  | N |
| 4 | `OP_REST_JOB_DATE` | Op_Rest_Jobessorial Date | DATE | 7 |  | N |
| 5 | `OP_REST_JOB_TP_FLAG` | Op_Rest_Job_Tpessorial Flag | VARCHAR2 | 1 |  | N |

## `M_OP_ROLE`

- **Tipo:** Master
- **Categoria:** User
- **Campos:** 2

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 2 | `ROLE_ID` | Roleessorial Id | NUMBER | 22 | 6 | N |

## `M_OP_SEL`

- **Tipo:** Master
- **Categoria:** User
- **Campos:** 9

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `SEL_CODE` | Selessorial Code | VARCHAR2 | 6 |  | N |
| 3 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 4 | `SEL_READ_ONLY_FLAG` | Sel_Read_Onlyessorial Flag | VARCHAR2 | 1 |  | N |
| 5 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 6 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 7 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 8 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_OP_WHSE_ACT_TP_NUM_EXCL`

- **Tipo:** Master
- **Categoria:** User
- **Campos:** 8

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `OP_CODE` | Operator Code | VARCHAR2 | 20 |  | N |
| 3 | `WHSE_ACT_TP_NUM_EXCL` | Whse_Act_Tp_Numessorial Excl | NUMBER | 22 | 2 | N |
| 4 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 5 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 6 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 7 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_ROLE_D1`

- **Tipo:** Master
- **Categoria:** User
- **Campos:** 2

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ROLE_ID` | Roleessorial Id | NUMBER | 22 | 6 | N |
| 2 | `ROLE_PARENT_ID` | Role_Parentessorial Id | NUMBER | 22 | 6 | N |

## `M_ROLE_D2`

- **Tipo:** Master
- **Categoria:** User
- **Campos:** 5

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ROLE_ID` | Roleessorial Id | NUMBER | 22 | 6 | N |
| 1 | `ROLE_ID` | Roleessorial Id | NUMBER | 22 | 6 | N |
| 2 | `ROLE_DOC_TP_CODE` | Role_Doc_Tpessorial Code | VARCHAR2 | 20 |  | N |
| 2 | `ROLE_DOC_TP_CODE` | Role_Doc_Tpessorial Code | VARCHAR2 | 20 |  | N |
| 3 | `ROLE_FUNC_CODE` | Role_Funcessorial Code | VARCHAR2 | 20 |  | N |

## `M_ROLE_H`

- **Tipo:** Master
- **Categoria:** User
- **Campos:** 4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ROLE_ID` | Roleessorial Id | NUMBER | 22 | 6 | N |
| 2 | `ROLE_SHORT` | Roleessorial Short | VARCHAR2 | 20 |  | N |
| 3 | `ROLE_DES` | Roleessorial Des | VARCHAR2 | 40 |  | N |
| 4 | `ROLE_STAT` | Roleessorial Stat | VARCHAR2 | 1 |  | N |

## `USER_PROFILE`

- **Tipo:** Misc
- **Categoria:** User
- **Campos:** 8

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `PRODUCT` | Productessorial Product | VARCHAR2 | 30 |  | Y |
| 2 | `USERID` | Useridessorial Userid | VARCHAR2 | 30 |  | Y |
| 3 | `PROFILE` | Profileessorial Profile | VARCHAR2 | 240 |  | Y |
| 4 | `ATTRIBUTE` | Attributeessorial Attribute | VARCHAR2 | 240 |  | Y |
| 5 | `NUMERIC_VALUE` | Numericessorial Value | NUMBER | 22 | 15 | Y |
| 6 | `CHAR_VALUE` | Charessorial Value | VARCHAR2 | 240 |  | Y |
| 7 | `DATE_VALUE` | Dateessorial Value | DATE | 7 |  | Y |
| 8 | `LONG_VALUE` | Longessorial Value | LONG | 0 |  | Y |

