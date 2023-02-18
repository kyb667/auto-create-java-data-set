# auto-create-java-data-set README

자바 dataset을 자동으로 만들어줍니다.<br/>
This extension make dataset files for DB Model in Java automatically.<br/>
データベースのデータを取得し、JAVAのDataSetを自動的に作成してくれます。

<br/>

## Features
---

데이터 타입을 확인해 주세요.<br/>
Please check the data type.<br/>
モデルのタイプは以下のようになります。ご参考ください。<br/>

### (1) postgres

| postgres data type       | java data type        |
|-------------------|-------------|
| smallint       | short      |
| smallserial       | short   |
| integer            | Integer     |
| real            | float     |
| serial            | Integer     |
| bigint            | Long     |
| double precision            | Double     |
| bigserial            | Long     |
| decimal            | Double     |
| numeric            | Double     |
| money            | BigDecimal     |
| character varying            | String     |
| varchar            | String     |
| character            | String     |
| char            | String     |
| text            | String     |
| bytea            | Double     |
| timestamp with time zone            | Timestamp     |
| timestamp without time zone            | Timestamp     |
| time with time zone            | Time     |
| time without time zone            | Time     |
| date            | Date     |
| interval            | IfxIntervalDF     |
| boolean            | Boolean     |
| enum            | enum     |
| macaddr            | String     |
| macaddr8            | String     |
| etc            | String     |


<br/>

### (2) Oracle

<a href="https://docs.oracle.com/database/121/JJPUB/datamap.htm#JJPUB24090" target="_blank">Click me !</a>

| Oracle data type       | java data type        |
|-------------------|-------------|
|CHAR | String
|CHARACTER | String
|LONG | String
|STRING | String
|VARCHAR | String
|VARCHAR2 | String
|VARCHAR_VARCHAR2 | String
|NCHAR | String
|NVARCHAR2 | String
|RAW | byte[]
|LONG RAW | byte[]
|BINARY_INTEGER | int
|NATURAL | int
|NATURALN | int
|PLS_INTEGER | int
|POSITIVE | int
|POSITIVEN | int
|SIGNTYPE | int
|INT_INTEGER | int
|INT | int
|INTEGER | int
|DEC |  BigDecimal
|DECIMAL |  BigDecimal
|NUMBER |  BigDecimal
|NUMERIC |  BigDecimal
|DOUBLE PRECISION |  double
|FLOAT |  double
|SMALLINT |  int
|REAL |  float
|DATE |  Timestamp
|TIMESTAMP |  Timestamp
|TIMESTAMP WITH TZ |  Timestamp
|TIMESTAMP WITH LOCAL TZ |  Timestamp
|TIMESTAMP(6) |  Timestamp
|INTERVAL YEAR TO MONTH |  String
|INTERVAL DAY TO SECOND |  String
|ROWID |  ROWID
|UROWID |  ROWID
|BOOLEAN |  boolean
|CLOB |  Clob
|BLOB |  Blob
|BFILE |  byte[]
|REF CURSOR |  ResultSet
|REF |  ResultSet
|CURSOR |  ResultSet
| etc            | String     |

<br/>

## Requirements
---
<br/>

<img width="80%" src="https://user-images.githubusercontent.com/22291462/219850988-033cce0f-7b72-44fe-a4b3-7aad49e9ab34.gif"/>
<br/>
<br/>

시작하려면 매개 변수를 입력해야 합니다. <br/>
You should pass parameter to start.<br/>
モデルを作成するためにはデータベースの情報を入力する必要があります。<br/>
データベースの種別によって入力パラメータが変わります。<br/><br/>

1. postgres<br/>

    1) 데이터베이스의 유저 이름을 입력해주세요<br/>
    please enter the user name of the database.<br/>
    データベースのユーザー名を入力してください。

    2) 데이터베이스의 호스트를 입력해주세요<br/>
    please enter the host of the database.<br/>
    データベースのホストを入力してください。

    3) 데이터베이스 이름을 입력해주세요<br/>
    please enter the database name of the database.<br/>
    データベースのスキーマを入力してください。

    4) 패스워드를 입력해주세요<br/>
    please enter the password of the database.<br/>
    データベースのパスワードを入力してください。

    5) 포트를 입력해주세요<br/>
    please enter the port of the database.<br/>
    データベースのポートを入力してください。

2. Oracle<br/>

    1) 데이터베이스의 유저 이름을 입력해주세요.<br/>
    please enter the user name of the database.<br/>
    データベースのユーザー名を入力してください。

    2) 패스워드를 입력해주세요<br/>
    please enter the password of the database.<br/>
    データベースのパスワードを入力してください。

    3) 데이터베이스의 호스트, 포트, 이름을 입력해주세요<br/>
    please enter the host, port, schema of the database.<br/>
    データベースのホスト、ポート、スキーマを入力してください。<br/>
    ex ) localhost:1521/xe

<br/>
전부 입력하셨다면 해당 데이터베이스의 테이블과 컬럼 정보가 담긴 dataset이 만들어집니다.<br/>

When All parameters being passed normally You can get dataset files which have information based on your parameter.

C:\auto-create-java-data-set 폴더를 확인해주세요<br/>
Check the C:\auto-create-java-data-set folder.

<br/>

## Release Notes
---

### 0.0.0

initial release of auto-create-java-data-set
- Apply postgres

### 1.0.0
- Apply Oracle

#### 1.0.1
- Add data type
- Error correction
