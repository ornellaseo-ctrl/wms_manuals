# Tabelas — Voice

> Categoria extraída da planilha `Tables-Database.xlsx`. Total de tabelas: **2**.

## `M_VOICE_PROF_D`

- **Tipo:** Master
- **Categoria:** Voice
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `VOICE_PROF_CODE` | Voice_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `VOICE_PROF_PROP_CODE` | Voice_Prof_Propessorial Code | VARCHAR2 | 60 |  | N |
| 5 | `VOICE_PROF_TP` | Voice_Professorial Tp | VARCHAR2 | 1 |  | N |
| 6 | `VOICE_PROF_PROP_VAL` | Voice_Prof_Propessorial Val | VARCHAR2 | 255 |  | Y |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_VOICE_PROF_H`

- **Tipo:** Master
- **Categoria:** Voice
- **Campos:** 11
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `VOICE_PROF_CODE` | Voice_Professorial Code | VARCHAR2 | 4 |  | N |
| 4 | `VOICE_PROF_TP` | Voice_Professorial Tp | VARCHAR2 | 1 |  | N |
| 5 | `VOICE_PROF_DES` | Voice_Professorial Des | VARCHAR2 | 30 |  | N |
| 6 | `VOICE_PROF_STAT` | Voice_Professorial Stat | VARCHAR2 | 1 |  | N |
| 7 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 8 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 10 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `VERSION` | Version | NUMBER | 22 | 9 | N |

