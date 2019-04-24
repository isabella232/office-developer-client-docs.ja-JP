---
title: schemaenum (Access デスクトップデータベースリファレンス)
TOCTitle: SchemaEnum
ms:assetid: 6147b682-3c4f-ea91-fff6-ac73107d206d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249359(v=office.15)
ms:contentKeyID: 48545208
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aa70f275de164716b5b3975b56588e9dc4aec1a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308864"
---
# <a name="schemaenum"></a>SchemaEnum

**適用先:** Access 2013、Office 2013

**OpenSchema** メソッドが取得するスキーマ [Recordset](openschema-method-ado.md) の種類を表します。

## <a name="remarks"></a>注釈

各 ADO 定数に返される関数と列については、「OLE DB Programmer's Reference」 (英語) の Appendix B のトピックを参照してください。 各トピックの名前は、次の表の [説明] セクションにかっこで囲んで一覧表示されます。

各 ADO MD 定数に返される関数と列については、OLE DB for OLAP に関する Chapter 23 のトピックを参照してください。 各トピックの名前は、次の表の [説明] 列に\*、かっこで囲んで、アスタリスク () 付きでマークされています。

OLE DB ドキュメントの中の列のデータ型は、ADO の「[DataTypeEnum](datatypeenum.md)」の説明を参考に、ADO データ型に読み換えてください。 たとえば、 **DBTYPE\_WSTR**の OLE DB データ型は、ADO データ型の**adwchar**と同じです。

ADO generates schema-like results for the constants, **adSchemaDBInfoKeywords** and **adSchemaDBInfoLiterals**. ADO は**Recordset**を作成し、各行に、 **IDBInfo:: getkeywords**および**IDBInfo:: GetLiteralInfo**メソッドで返される値をそれぞれ入力します。 これらのメソッドの詳細については、「 *OLE DB プログラマリファレンス*」の「IDBInfo」セクションを参照してください。

<br/>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>定数</p></th>
<th><p>値</p></th>
<th><p>説明</p></th>
<th><p>制約列</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adschemaasserts</strong></p></td>
<td><p>.0</p></td>
<td><p>カタログに定義され、所定のユーザーが所有するアサーションを返します。 (ASSERTIONS 行セット)</p></td>
<td><p>CONSTRAINT_CATALOG<br />
CONSTRAINT_SCHEMA<br />
CONSTRAINT_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaCatalogs</strong></p></td>
<td><p>1-d</p></td>
<td><p>DBMS からアクセスできるカタログに関連付けられている物理的属性を返します。 (CATALOGS 行セット)</p></td>
<td><p>CATALOG_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaCharacterSets</strong></p></td>
<td><p>pbm-2</p></td>
<td><p>カタログに定義され、所定のユーザーがアクセスできる文字セットを返します。 (CHARACTER_SETS 行セット)</p></td>
<td><p>CHARACTER_SET_CATALOG<br />
CHARACTER_SET_SCHEMA<br />
CHARACTER_SET_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adschemacheckconstraints</strong></p></td>
<td><p>5</p></td>
<td><p>カタログに定義され、所定のユーザーが所有する CHECK 制約を返します。 (CHECK_CONSTRAINTS 行セット)</p></td>
<td><p>CONSTRAINT_CATALOG<br />
CONSTRAINT_SCHEMA<br />
CONSTRAINT_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaCollations</strong></p></td>
<td><p>1/3</p></td>
<td><p>カタログに定義され、所定のユーザーがアクセスできる文字照合順序を返します。 (COLLATIONS 行セット)</p></td>
<td><p>COLLATION_CATALOG<br />
COLLATION_SCHEMA<br />
COLLATION_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaColumnPrivileges</strong></p></td>
<td><p>スリー</p></td>
<td><p>カタログに定義され、所定のユーザーが利用できる、または権限を持つテーブルの列に対する特権を返します。 (COLUMN_PRIVILEGES 行セット)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
TABLE_NAME<br />
COLUMN_NAME<br />
交付<br />
与え</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaColumns</strong></p></td>
<td><p>2/4</p></td>
<td><p>カタログに定義され、所定のユーザーがアクセスできるテーブルの列 (ビューも含む) を返します。 (COLUMNS 行セット)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
TABLE_NAME<br />
COLUMN_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaColumnsDomainUsage</strong></p></td>
<td><p>#</p></td>
<td><p>カタログに定義され、そのカタログに定義されたドメインに依存し、所定のユーザーが所有する列を返します。 (COLUMN_DOMAIN_USAGE 行セット)</p></td>
<td><p>DOMAIN_CATALOG<br />
DOMAIN_SCHEMA<br />
ドメイン名<br />
COLUMN_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaConstraintColumnUsage</strong></p></td>
<td><p>シックス</p></td>
<td><p>カタログに定義され、所定のユーザーが所有し、参照制約、一意制約、CHECK 制約、およびアサーションに使う列を返します。 (CONSTRAINT_COLUMN_USAGE 行セット)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
TABLE_NAME<br />
COLUMN_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaConstraintTableUsage</strong></p></td>
<td><p>7</p></td>
<td><p>カタログに定義され、所定のユーザーが所有し、参照制約、一意制約、CHECK 制約、およびアサーションに使うテーブルを返します。 (CONSTRAINT_TABLE_USAGE 行セット)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
TABLE_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaCubes</strong></p></td>
<td><p>32</p></td>
<td><p>スキーマ (プロバイダーがスキーマをサポートしていない場合はカタログ) 内の利用できるキューブに関する情報を返します。 (CUBES 行セット *)</p></td>
<td><p>CATALOG_NAME<br />
SCHEMA_NAME<br />
CUBE_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adschemadbinのキーワード</strong></p></td>
<td><p>31</p></td>
<td><p>プロバイダー固有のキーワードの一覧を返します。 (IDBInfo:: getkeywords *)</p></td>
<td><p>&lt;なし&gt;</p></td>
</tr>
<tr class="odd">
<td><p><strong>adschemadbinの方法</strong></p></td>
<td><p>31</p></td>
<td><p>テキスト コマンドで使う、プロバイダー固有のリテラルの一覧を返します。 (IDBInfo:: GetLiteralInfo *)</p></td>
<td><p>&lt;なし&gt;</p></td>
</tr>
<tr class="even">
<td><p><strong>adschemadimensions</strong></p></td>
<td><p>33</p></td>
<td><p>所定のキューブの次元に関する情報を返します。 次元ごとに 1 行が割り当てられます。 (DIMENSIONS 行セット *)</p></td>
<td><p>CATALOG_NAME<br />
SCHEMA_NAME<br />
CUBE_NAME<br />
DIMENSION_NAME<br />
DIMENSION_UNIQUE_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaForeignKeys</strong></p></td>
<td><p>27</p></td>
<td><p>所定のユーザーがカタログに定義した外部キー列を返します。 (FOREIGN_KEYS 行セット)</p></td>
<td><p>PK_TABLE_CATALOG<br />
PK_TABLE_SCHEMA<br />
PK_TABLE_NAME<br />
FK_TABLE_CATALOG<br />
FK_TABLE_SCHEMA<br />
FK_TABLE_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adschemahierarchies</strong></p></td>
<td><p>34</p></td>
<td><p>次元で利用できる階層に関する情報を返します。 (HIERARCHIES 行セット *)</p></td>
<td><p>CATALOG_NAME<br />
SCHEMA_NAME<br />
CUBE_NAME<br />
DIMENSION_UNIQUE_NAME<br />
HIERARCHY_NAME<br />
HIERARCHY_UNIQUE_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adschemaindexes</strong></p></td>
<td><p>個</p></td>
<td><p>カタログに定義され、所定のユーザーが所有するインデックスを返します。 (INDEXES 行セット)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
INDEX_NAME<br />
種類<br />
TABLE_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adschemakeycolumnusage</strong></p></td>
<td><p>~</p></td>
<td><p>カタログに定義され、所定のユーザーがキーとして制約した列を返します。 (KEY_COLUMN_USAGE 行セット)</p></td>
<td><p>CONSTRAINT_CATALOG<br />
CONSTRAINT_SCHEMA<br />
CONSTRAINT_NAME<br />
TABLE_CATALOG<br />
TABLE_SCHEMA<br />
TABLE_NAME<br />
COLUMN_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaLevels</strong></p></td>
<td><p>35</p></td>
<td><p>次元で利用できるレベルに関する情報を返します。 (LEVELS 行セット *)</p></td>
<td><p>CATALOG_NAME<br />
SCHEMA_NAME<br />
CUBE_NAME<br />
DIMENSION_UNIQUE_NAME<br />
HIERARCHY_UNIQUE_NAME<br />
LEVEL_NAME<br />
LEVEL_UNIQUE_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adschemameasures</strong></p></td>
<td><p>36</p></td>
<td><p>利用できる単位に関する情報を返します。 (MEASURES 行セット *)</p></td>
<td><p>CATALOG_NAME<br />
SCHEMA_NAME<br />
CUBE_NAME<br />
MEASURE_NAME<br />
MEASURE_UNIQUE_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaMembers</strong></p></td>
<td><p>38</p></td>
<td><p>利用できるメンバーに関する情報を返します。 (MEMBERS 行セット *)</p></td>
<td><p>CATALOG_NAME<br />
SCHEMA_NAME<br />
CUBE_NAME<br />
DIMENSION_UNIQUE_NAME<br />
HIERARCHY_UNIQUE_NAME<br />
LEVEL_UNIQUE_NAME<br />
LEVEL_NUMBER<br />
MEMBER_NAME<br />
MEMBER_UNIQUE_NAME<br />
MEMBER_CAPTION<br />
MEMBER_TYPE<br />
Tree 演算子 (詳細については、「OLE DB For OLAP」ドキュメントを参照してください)。</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaPrimaryKeys</strong></p></td>
<td><p>個</p></td>
<td><p>所定のユーザーがカタログに定義した主キー列を返します。 (PRIMARY_KEYS 行セット)</p></td>
<td><p>PK_TABLE_CATALOG<br />
PK_TABLE_SCHEMA<br />
PK_TABLE_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaProcedureColumns</strong></p></td>
<td><p>29</p></td>
<td><p>プロシージャが返す行セットの列に関する情報を返します。 (PROCEDURE_COLUMNS Rowset)</p></td>
<td><p>PROCEDURE_CATALOG<br />
PROCEDURE_SCHEMA<br />
PROCEDURE_NAME<br />
COLUMN_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaProcedureParameters</strong></p></td>
<td><p>日</p></td>
<td><p>プロシージャのパラメーターとリターン コードに関する情報を返します。 (PROCEDURE_PARAMETERS 行セット)</p></td>
<td><p>PROCEDURE_CATALOG<br />
PROCEDURE_SCHEMA<br />
PROCEDURE_NAME<br />
PARAMETER_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adschemaprocedures</strong></p></td>
<td><p>16</p></td>
<td><p>カタログに定義され、所定のユーザーが所有するプロシージャを返します。 (PROCEDURES 行セット)</p></td>
<td><p>PROCEDURE_CATALOG<br />
PROCEDURE_SCHEMA<br />
PROCEDURE_NAME<br />
PROCEDURE_TYPE</p></td>
</tr>
<tr class="even">
<td><p><strong>adschemaproperties</strong></p></td>
<td><p>37</p></td>
<td><p>次元の各レベルで利用できるプロパティに関する情報を返します。 (PROPERTIES 行セット *)</p></td>
<td><p>CATALOG_NAME<br />
SCHEMA_NAME<br />
CUBE_NAME<br />
DIMENSION_UNIQUE_NAME<br />
HIERARCHY_UNIQUE_NAME<br />
LEVEL_UNIQUE_NAME<br />
MEMBER_UNIQUE_NAME<br />
PROPERTY_TYPE<br />
PROPERTY_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaProviderSpecific</strong></p></td>
<td><p>-1</p></td>
<td><p>プロバイダーが非標準の専用のスキーマ クエリを定義する場合に使います。</p></td>
<td><p>&lt;プロバイダー固有&gt;</p></td>
</tr>
<tr class="even">
<td><p><strong>adschemaprovidertypes</strong></p></td>
<td><p>×</p></td>
<td><p>データ プロバイダーがサポートする (基本) データ型を返します。 (PROVIDER_TYPES 行セット)</p></td>
<td><p>DATA_TYPE<br />
BEST_MATCH</p></td>
</tr>
<tr class="odd">
<td><p><strong>adschema・ entialconstraints</strong></p></td>
<td><p>i-9</p></td>
<td><p>カタログに定義され、所定のユーザーが所有する参照制約を返します。 (REFERENTIAL_CONSTRAINTS 行セット)</p></td>
<td><p>CONSTRAINT_CATALOG<br />
CONSTRAINT_SCHEMA<br />
CONSTRAINT_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaSchemata</strong></p></td>
<td><p>インチ</p></td>
<td><p>所定のユーザーが所有するスキーマ (データベース オブジェクト) を返します。 (SCHEMATA 行セット)</p></td>
<td><p>CATALOG_NAME<br />
SCHEMA_NAME<br />
SCHEMA_OWNER</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaSQLLanguages</strong></p></td>
<td><p>個</p></td>
<td><p>カタログに定義された SQL 実装処理データがサポートする準拠レベル、オプション、および言語を返します。 (SQL_LANGUAGES 行セット)</p></td>
<td><p>&lt;なし&gt;</p></td>
</tr>
<tr class="even">
<td><p><strong>adschemastatistics</strong></p></td>
<td><p>年</p></td>
<td><p>カタログに定義され、所定のユーザーが所有する統計値を返します。 (STATISTICS 行セット)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
TABLE_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaTableConstraints</strong></p></td>
<td><p>個</p></td>
<td><p>カタログに定義され、所定のユーザーが所有するテーブル制約を返します。 (TABLE_CONSTRAINTS 行セット)</p></td>
<td><p>CONSTRAINT_CATALOG<br />
CONSTRAINT_SCHEMA<br />
CONSTRAINT_NAME<br />
TABLE_CATALOG<br />
TABLE_SCHEMA<br />
TABLE_NAME<br />
CONSTRAINT_TYPE</p></td>
</tr>
<tr class="even">
<td><p><strong>adschematableprivileges</strong></p></td>
<td><p>第</p></td>
<td><p>カタログに定義され、所定のユーザーが利用できる、または権限を持つテーブルに対する特権を返します。 (TABLE_PRIVILEGES 行セット)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
TABLE_NAME<br />
交付<br />
与え</p></td>
</tr>
<tr class="odd">
<td><p><strong>adschematables ル</strong></p></td>
<td><p>1280</p></td>
<td><p>カタログに定義され、所定のユーザーがアクセスできるテーブル (ビューも含む) を返します。 (TABLES 行セット)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
TABLE_NAME<br />
TABLE_TYPE</p></td>
</tr>
<tr class="even">
<td><p><strong>adschematranslran</strong></p></td>
<td><p>21</p></td>
<td><p>カタログに定義され、所定のユーザーがアクセスできる文字変換を返します。 (TRANSLATIONS 行セット)</p></td>
<td><p>TRANSLATION_CATALOG<br />
TRANSLATION_SCHEMA<br />
TRANSLATION_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaTrustees</strong></p></td>
<td><p>39</p></td>
<td><p>将来使用するために予約されています。</p></td>
<td><p><br />
</p></td>
</tr>
<tr class="even">
<td><p><strong>adschemaの権限</strong></p></td>
<td><p>約</p></td>
<td><p>カタログに定義され、所定のユーザーが利用できる、または権限を持つオブジェクトに対する USAGE 特権を返します。 (USAGE_PRIVILEGES 行セット)</p></td>
<td><p>OBJECT_CATALOG<br />
OBJECT_SCHEMA<br />
OBJECT_NAME<br />
OBJECT_TYPE<br />
交付<br />
与え</p></td>
</tr>
<tr class="odd">
<td><p><strong>adschemaviewcolumnusage</strong></p></td>
<td><p>ソケット</p></td>
<td><p>カタログに定義され、所定のユーザーが所有する、表示テーブルが依存する列を返します。 (VIEW_COLUMN_USAGE 行セット)</p></td>
<td><p>VIEW_CATALOG<br />
VIEW_SCHEMA<br />
VIEW_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adschemaviews</strong></p></td>
<td><p>最高</p></td>
<td><p>カタログに定義され、所定のユーザーがアクセスできるビューを返します。 (VIEWS 行セット)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
TABLE_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adschemaviewtableusage</strong></p></td>
<td><p>まで</p></td>
<td><p>カタログに定義され、所定のユーザーが所有し、表示テーブルが依存するテーブルを返します。 (VIEW_TABLE_USAGE 行セット)</p></td>
<td><p>VIEW_CATALOG<br />
VIEW_SCHEMA<br />
VIEW_NAME</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>ADO/WFC と同等

パッケージ: **com.ms.wfc.data**

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>定数</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AdoEnums</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums セット</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums 制約</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums 特権</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums domainusage</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums CONSTRAINTCOLUMNUSAGE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums CONSTRAINTTABLEUSAGE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums DBINFOKEYWORDS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums DBINFOLITERALS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums FOREIGNKEYS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums (keycolumnusage)</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums キー</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums PROCEDURECOLUMNS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums PROCEDUREPARAMETERS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums 固有のスキーマ</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums の種類</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums REFERENTIALCONTRAINTS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums SCHEMATA</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums SQLLANGUAGES</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums TABLECONSTRAINTS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums 特権</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums 特権</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums columnusage</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums の使用</p></td>
</tr>
</tbody>
</table>

