# Tabelas — Address

> Categoria extraída da planilha `Tables-Database.xlsx`. Total de tabelas: **10**.

## `M_COUNTRY_D`

- **Tipo:** Master
- **Categoria:** Address
- **Campos:** 9

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COUNTRY_CODE` | Country Code | VARCHAR2 | 4 |  | N |
| 3 | `COUNTRY_BKD_NUM` | Country_Bkdessorial Num | NUMBER | 22 | 2 | N |
| 4 | `COUNTRY_BKD_DES` | Country_Bkdessorial Des | VARCHAR2 | 30 |  | N |
| 5 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 6 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 7 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 8 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 9 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_COUNTRY_DD`

- **Tipo:** Master
- **Categoria:** Address
- **Campos:** 12

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COUNTRY_CODE` | Country Code | VARCHAR2 | 4 |  | N |
| 3 | `COUNTRY_BKD_NUM` | Country_Bkdessorial Num | NUMBER | 22 | 2 | N |
| 4 | `COUNTRY_PARTIT_NUM` | Country_Partitessorial Num | NUMBER | 22 | 2 | N |
| 5 | `COUNTRY_PARTIT_LEN` | Country_Partitessorial Len | NUMBER | 22 | 2 | N |
| 6 | `COUNTRY_EXACT_LEN_FLAG` | Country_Exact_Lenessorial Flag | VARCHAR2 | 1 |  | N |
| 7 | `COUNTRY_PARTIT_VAL_CHAR` | Country_Partit_Valessorial Char | VARCHAR2 | 45 |  | N |
| 8 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 9 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 11 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_COUNTRY_H`

- **Tipo:** Master
- **Categoria:** Address
- **Campos:** 11

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COUNTRY_CODE` | Country Code | VARCHAR2 | 4 |  | N |
| 3 | `COUNTRY_DES` | Countryessorial Des | VARCHAR2 | 30 |  | N |
| 4 | `COUNTRY_NUM_BKD` | Country_Numessorial Bkd | NUMBER | 22 | 2 | N |
| 5 | `COUNTRY_STAT` | Countryessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 11 | `COUNTRY_CODE_ISO` | Country_Codeessorial Iso | VARCHAR2 | 2 |  | Y |

## `M_STATE`

- **Tipo:** Master
- **Categoria:** Address
- **Campos:** 10

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COUNTRY_CODE` | Country Code | VARCHAR2 | 4 |  | N |
| 3 | `STATE_CODE` | Stateessorial Code | VARCHAR2 | 4 |  | N |
| 4 | `STATE_DES` | Stateessorial Des | VARCHAR2 | 30 |  | N |
| 5 | `STATE_STAT` | Stateessorial Stat | VARCHAR2 | 1 |  | N |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_STATE_TAX`

- **Tipo:** Master
- **Categoria:** Address
- **Campos:** 4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `STATE_CODE_FROM` | State_Codeessorial From | VARCHAR2 | 4 |  | N |
| 2 | `STATE_CODE_TO` | State_Codeessorial To | VARCHAR2 | 4 |  | N |
| 3 | `STATE_TAX_DATE` | State_Taxessorial Date | DATE | 7 |  | N |
| 4 | `STATE_TAX_PCENT` | State_Taxessorial Pcent | NUMBER | 22 | 7 | N |

## `M_TEL`

- **Tipo:** Master
- **Categoria:** Address
- **Campos:** 14
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | N |
| 3 | `TEL_TP` | Telessorial Tp | VARCHAR2 | 4 |  | N |
| 4 | `TEL_ACC_CODE` | Tel_Accessorial Code | VARCHAR2 | 10 |  | N |
| 5 | `TEL_LIST_CODE` | Tel_Listessorial Code | VARCHAR2 | 4 |  | N |
| 6 | `TEL_NUM` | Telessorial Num | VARCHAR2 | 20 |  | N |
| 7 | `TEL_CONTACT` | Telessorial Contact | VARCHAR2 | 30 |  | N |
| 8 | `TEL_CONTACT_DES` | Tel_Contactessorial Des | VARCHAR2 | 20 |  | Y |
| 9 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 10 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 11 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 12 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 13 | `VERSION` | Version | NUMBER | 22 | 9 | N |
| 14 | `TEL_CONTACT_EMAIL_ADD` | Tel_Contact_Emailessorial Add | VARCHAR2 | 60 |  | Y |

## `M_TEL_LIST`

- **Tipo:** Master
- **Categoria:** Address
- **Campos:** 10
- **Campos-chave prováveis:** COMP_CODE

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `COMP_CODE` | Company Code | VARCHAR2 | 2 |  | Y |
| 3 | `TEL_LIST_CODE` | Tel_Listessorial Code | VARCHAR2 | 4 |  | Y |
| 4 | `TEL_LIST_DES` | Tel_Listessorial Des | VARCHAR2 | 30 |  | Y |
| 5 | `TEL_LIST_STAT` | Tel_Listessorial Stat | VARCHAR2 | 1 |  | Y |
| 6 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 7 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 8 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 9 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `M_ZIP`

- **Tipo:** Master
- **Categoria:** Address
- **Campos:** 12

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ID` | ID | RAW | 32 |  | N |
| 2 | `ZIP_CODE` | Zip Code | VARCHAR2 | 10 |  | N |
| 3 | `ZIP_CITY` | Zip Code City | VARCHAR2 | 30 |  | N |
| 4 | `ZIP_STAT` | Zarehouse Stat | VARCHAR2 | 1 |  | N |
| 5 | `STATE_CODE` | Stateessorial Code | VARCHAR2 | 4 |  | N |
| 6 | `COUNTRY_CODE` | Country Code | VARCHAR2 | 4 |  | N |
| 7 | `ZIP_DISP_CODE` | Zarehouse Disp Code | VARCHAR2 | 10 |  | Y |
| 8 | `CREATE_DATE` | Create Date | DATE | 7 |  | Y |
| 9 | `CREATE_OP_CODE` | Create Operator Code | VARCHAR2 | 100 |  | Y |
| 10 | `MODY_DATE` | Modify Date | DATE | 7 |  | Y |
| 11 | `MODY_OP_CODE` | Modify Operator Code | VARCHAR2 | 100 |  | Y |
| 12 | `VERSION` | Version | NUMBER | 22 | 9 | N |

## `TEMP_ZIP`

- **Tipo:** Misc
- **Categoria:** Address
- **Campos:** 10

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ZIP_CODE` | Zip Code | VARCHAR2 | 10 |  | Y |
| 2 | `CITY` | Cityessorial City | VARCHAR2 | 30 |  | Y |
| 3 | `STATE_CODE` | Stateessorial Code | VARCHAR2 | 5 |  | Y |
| 4 | `X` | X | VARCHAR2 | 1 |  | Y |
| 5 | `Y` | Y | VARCHAR2 | 1 |  | Y |
| 6 | `Z` | Z | VARCHAR2 | 1 |  | Y |
| 7 | `COUNTRY_CODE` | Country Code | VARCHAR2 | 2 |  | Y |
| 8 | `M` | Messorial M | VARCHAR2 | 1 |  | Y |
| 9 | `IDATE` | Idateessorial Idate | VARCHAR2 | 1 |  | Y |
| 10 | `COLONY` | Colonyessorial Colony | VARCHAR2 | 50 |  | Y |

## `TEMP_ZIP1`

- **Tipo:** Misc
- **Categoria:** Address
- **Campos:** 4

| # | Campo | Nome | Tipo | Tam. | Prec. | Nulls |
|---:|---|---|---|---:|---:|:---:|
| 1 | `ZIP_CODE` | Zip Code | VARCHAR2 | 10 |  | Y |
| 2 | `CITY` | Cityessorial City | VARCHAR2 | 30 |  | Y |
| 3 | `STATE_CODE` | Stateessorial Code | VARCHAR2 | 5 |  | Y |
| 4 | `COUNTRY_CODE` | Country Code | VARCHAR2 | 2 |  | Y |

