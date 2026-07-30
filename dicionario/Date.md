# Tabelas — Date

> Categoria extraída da planilha `Tables-Database.xlsx`. Total de tabelas: **7**.

## `M_DATE_PROF_D`

- **Tipo:** Master
- **Categoria:** Date
- **Campos:** 9
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `DATE_PROF_CODE` | Date_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `DATE_START` | Dateessorial Start | DATE | 7 |  | N |
| 5 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 6 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 7 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 8 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_DATE_PROF_H`

- **Tipo:** Master
- **Categoria:** Date
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `DATE_PROF_CODE` | Date_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `DATE_PROF_DES` | Date_Professorial Des | VARCHAR2 | 30 |  | N |
| 5 | `DATE_PROF_STAT` | Date_Professorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_DAY_PROF_D`

- **Tipo:** Master
- **Categoria:** Date
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `DAY_PROF_CODE` | Day_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `DAY_PROF_DAY` | Day_Professorial Day | VARCHAR2 | 3 |  | N |
| 5 | `DAY_PROF_START_TIME` | Day_Prof_Startessorial Time | VARCHAR2 | 7 |  | N |
| 6 | `DAY_PROF_END_TIME` | Day_Prof_Endessorial Time | VARCHAR2 | 7 |  | N |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_DAY_PROF_H`

- **Tipo:** Master
- **Categoria:** Date
- **Campos:** 17
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `DAY_PROF_CODE` | Day_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `DAY_PROF_DES` | Day_Professorial Des | VARCHAR2 | 30 |  | N |
| 5 | `DAY_PROF_STAT` | Day_Professorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `DAY_MON_ACT_FLAG` | Day_Mon_Actessorial Flag | VARCHAR2 | 1 |  | N |
| 7 | `DAY_TUE_ACT_FLAG` | Day_Tue_Actessorial Flag | VARCHAR2 | 1 |  | N |
| 8 | `DAY_WED_ACT_FLAG` | Day_Wed_Actessorial Flag | VARCHAR2 | 1 |  | N |
| 9 | `DAY_THU_ACT_FLAG` | Day_Thu_Actessorial Flag | VARCHAR2 | 1 |  | N |
| 10 | `DAY_FRI_ACT_FLAG` | Day_Fri_Actessorial Flag | VARCHAR2 | 1 |  | N |
| 11 | `DAY_SAT_ACT_FLAG` | Day_Sat_Actessorial Flag | VARCHAR2 | 1 |  | N |
| 12 | `DAY_SUN_ACT_FLAG` | Day_Sun_Actessorial Flag | VARCHAR2 | 1 |  | N |
| 13 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 14 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 15 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 16 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 17 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_TIME_REP_PARA_D`

- **Tipo:** Master
- **Categoria:** Date
- **Campos:** 8
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `TIME_REP_PARA_CODE` | Time_Rep_Paraessorial Code | VARCHAR2 | 4 |  | N |
| 3 | `TIME_REP_PARA_COL_NUM` | Time_Rep_Para_Colessorial Num | NUMBER | 22 | 2 | N |
| 4 | `TIME_REP_PARA_COL_DES1` | Time_Rep_Para_Colessorial Des1 | VARCHAR2 | 10 |  | Y |
| 5 | `TIME_REP_PARA_COL_DES2` | Time_Rep_Para_Colessorial Des2 | VARCHAR2 | 10 |  | Y |
| 6 | `FLOW_PROS_CODE` | Flow Process Code | VARCHAR2 | 4 |  | Y |
| 7 | `DOC_CODE` | Document Code | VARCHAR2 | 4 |  | Y |
| 8 | `TIME_REP_PARA_ELAPSE_FLAG` | Time_Rep_Para_Elapseessorial Flag | VARCHAR2 | 1 |  | N |

## `M_TIME_REP_PARA_H`

- **Tipo:** Master
- **Categoria:** Date
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `TIME_REP_PARA_CODE` | Time_Rep_Paraessorial Code | VARCHAR2 | 4 |  | N |
| 3 | `TIME_REP_PARA_DES` | Time_Rep_Paraessorial Des | VARCHAR2 | 30 |  | N |
| 4 | `TIME_REP_PARA_FLOW_TP_FLAG` | Time_Rep_Para_Flow_Tpessorial Flag | VARCHAR2 | 1 |  | N |

## `M_TIME_STAMP_TP`

- **Tipo:** Master
- **Categoria:** Date
- **Campos:** 4
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 2 | `TIME_STAMP_TP_CODE` | Time_Stamp_Tpessorial Code | VARCHAR2 | 4 |  | N |
| 3 | `TIME_STAMP_TP_DES` | Time_Stamp_Tpessorial Des | VARCHAR2 | 30 |  | N |
| 4 | `TIME_STAMP_TP_STAT` | Time_Stamp_Tpessorial Stat | VARCHAR2 | 1 |  | N |

