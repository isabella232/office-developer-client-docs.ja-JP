---
title: SchemaEnum (デスクトップ データベース参照のアクセス)
TOCTitle: SchemaEnum
ms:assetid: 6147b682-3c4f-ea91-fff6-ac73107d206d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249359(v=office.15)
ms:contentKeyID: 48545208
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: c7f9f9e52f2220a384ba73a64d96dd93fec2cd91
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871284"
---
# <a name="schemaenum"></a>SchemaEnum

**適用されます**Access 2013、Office 2013。

**OpenSchema** メソッドが取得するスキーマ [Recordset](openschema-method-ado.md) の種類を表します。

## <a name="remarks"></a>備考

機能と各 ADO 定数に返される列の詳細については、 *OLE DB プログラマ リファレンス*の「付録 B トピックを参照して。 各トピックの名前は、次の表の [説明] セクションでは、かっこ内に表示されます。

機能と各 ADO MD 定数に返される列の詳細については、 *OLE DB for OLAP*のマニュアルの第 23 章のトピックを参照しています。 各トピックの名前を括弧内に表示し、アスタリスクでマークされている (\*) 次の表の [説明] 列にします。

OLE DB ドキュメントの中の列のデータ型は、ADO の「[DataTypeEnum](datatypeenum.md)」の説明を参考に、ADO データ型に読み換えてください。 など、OLE DB データ型の**DBTYPE\_WSTR**は、ADO データ型**adWChar**に相当します。

ADO では、定数**adSchemaDBInfoKeywords**と**adSchemaDBInfoLiterals**のスキーマのような結果が生成されます。 ADO では、**レコード セット**を作成し、それぞれ**IDBInfo::GetKeywords**と**IDBInfo::GetLiteralInfo**メソッドの戻り値を使用して各行を入力します。 これらのメソッドに関する追加情報については、 *OLE DB プログラマ リファレンス*」の IDBInfo セクションを参照しています。

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
<td><p><strong>adSchemaAsserts</strong></p></td>
<td><p>0</p></td>
<td><p>カタログに定義され、所定のユーザーが所有するアサーションを返します。
 (ASSERTIONS 行セット)</p></td>
<td><p>CONSTRAINT_CATALOG<br />
CONSTRAINT_SCHEMA<br />
CONSTRAINT_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaCatalogs</strong></p></td>
<td><p>1</p></td>
<td><p>DBMS からアクセスできるカタログに関連付けられている物理的属性を返します。
 (CATALOGS 行セット)</p></td>
<td><p>CATALOG_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaCharacterSets</strong></p></td>
<td><p>2</p></td>
<td><p>カタログに定義され、所定のユーザーがアクセスできる文字セットを返します。
 (CHARACTER_SETS 行セット)</p></td>
<td><p>CHARACTER_SET_CATALOG<br />
CHARACTER_SET_SCHEMA<br />
CHARACTER_SET_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaCheckConstraints</strong></p></td>
<td><p>5</p></td>
<td><p>カタログに定義され、所定のユーザーが所有する CHECK 制約を返します。
 (CHECK_CONSTRAINTS 行セット)</p></td>
<td><p>CONSTRAINT_CATALOG<br />
CONSTRAINT_SCHEMA<br />
CONSTRAINT_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaCollations</strong></p></td>
<td><p>3</p></td>
<td><p>カタログに定義され、所定のユーザーがアクセスできる文字照合順序を返します。
 (COLLATIONS 行セット)</p></td>
<td><p>COLLATION_CATALOG<br />
COLLATION_SCHEMA<br />
COLLATION_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaColumnPrivileges</strong></p></td>
<td><p>13</p></td>
<td><p>カタログに定義され、所定のユーザーが利用できる、または権限を持つテーブルの列に対する特権を返します。
 (COLUMN_PRIVILEGES 行セット)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
TABLE_NAME<br />
COLUMN_NAME<br />
権限の許可者<br />
被設定者</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaColumns</strong></p></td>
<td><p>4</p></td>
<td><p>カタログに定義され、所定のユーザーがアクセスできるテーブルの列 (ビューも含む) を返します。
 (COLUMNS 行セット)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
TABLE_NAME<br />
COLUMN_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaColumnsDomainUsage</strong></p></td>
<td><p>11</p></td>
<td><p>カタログに定義され、そのカタログに定義されたドメインに依存し、所定のユーザーが所有する列を返します。
 (COLUMN_DOMAIN_USAGE 行セット)</p></td>
<td><p>DOMAIN_CATALOG<br />
DOMAIN_SCHEMA<br />
ドメイン名<br />
COLUMN_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaConstraintColumnUsage</strong></p></td>
<td><p>6</p></td>
<td><p>カタログに定義され、所定のユーザーが所有し、参照制約、一意制約、CHECK 制約、およびアサーションに使う列を返します。
 (CONSTRAINT_COLUMN_USAGE 行セット)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
TABLE_NAME<br />
COLUMN_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaConstraintTableUsage</strong></p></td>
<td><p>7</p></td>
<td><p>カタログに定義され、所定のユーザーが所有し、参照制約、一意制約、CHECK 制約、およびアサーションに使うテーブルを返します。
 (CONSTRAINT_TABLE_USAGE 行セット)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
TABLE_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaCubes</strong></p></td>
<td><p>32</p></td>
<td><p>スキーマ (プロバイダーがスキーマをサポートしていない場合はカタログ) 内の利用できるキューブに関する情報を返します。
 (CUBES 行セット *)</p></td>
<td><p>CATALOG_NAME<br />
SCHEMA_NAME<br />
CUBE_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaDBInfoKeywords</strong></p></td>
<td><p>30</p></td>
<td><p>プロバイダー固有のキーワードの一覧を返します。
 (IDBInfo::GetKeywords *)</p></td>
<td><p>&lt;なし&gt;</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaDBInfoLiterals</strong></p></td>
<td><p>31</p></td>
<td><p>テキスト コマンドで使う、プロバイダー固有のリテラルの一覧を返します。
 (IDBInfo::GetLiteralInfo *)</p></td>
<td><p>&lt;なし&gt;</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaDimensions</strong></p></td>
<td><p>33</p></td>
<td><p>所定のキューブの分析コードに関する情報を返します。 各ディメンションに対して 1 つの行があります。 (DIMENSIONS 行セット *)</p></td>
<td><p>CATALOG_NAME<br />
SCHEMA_NAME<br />
CUBE_NAME<br />
DIMENSION_NAME<br />
DIMENSION_UNIQUE_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaForeignKeys</strong></p></td>
<td><p>27</p></td>
<td><p>所定のユーザーがカタログに定義した外部キー列を返します。
 (FOREIGN_KEYS 行セット)</p></td>
<td><p>PK_TABLE_CATALOG<br />
PK_TABLE_SCHEMA<br />
PK_TABLE_NAME<br />
FK_TABLE_CATALOG<br />
FK_TABLE_SCHEMA<br />
FK_TABLE_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaHierarchies</strong></p></td>
<td><p>34</p></td>
<td><p>次元で利用できる階層に関する情報を返します。
 (HIERARCHIES 行セット *)</p></td>
<td><p>CATALOG_NAME<br />
SCHEMA_NAME<br />
CUBE_NAME<br />
DIMENSION_UNIQUE_NAME<br />
HIERARCHY_NAME<br />
HIERARCHY_UNIQUE_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaIndexes</strong></p></td>
<td><p>12</p></td>
<td><p>カタログに定義され、所定のユーザーが所有するインデックスを返します。
 (INDEXES 行セット)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
INDEX_NAME を指定<br />
TYPE<br />
TABLE_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaKeyColumnUsage</strong></p></td>
<td><p>8</p></td>
<td><p>カタログに定義され、所定のユーザーがキーとして制約した列を返します。
 (KEY_COLUMN_USAGE 行セット)</p></td>
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
<td><p>次元で利用できるレベルに関する情報を返します。
 (LEVELS 行セット *)</p></td>
<td><p>CATALOG_NAME<br />
SCHEMA_NAME<br />
CUBE_NAME<br />
DIMENSION_UNIQUE_NAME<br />
HIERARCHY_UNIQUE_NAME<br />
LEVEL_NAME<br />
LEVEL_UNIQUE_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaMeasures</strong></p></td>
<td><p>36</p></td>
<td><p>利用できる単位に関する情報を返します。
 (MEASURES 行セット *)</p></td>
<td><p>CATALOG_NAME<br />
SCHEMA_NAME<br />
CUBE_NAME<br />
MEASURE_NAME<br />
MEASURE_UNIQUE_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaMembers</strong></p></td>
<td><p>38</p></td>
<td><p>利用できるメンバーに関する情報を返します。
 (MEMBERS 行セット *)</p></td>
<td><p>CATALOG_NAME<br />
SCHEMA_NAME<br />
CUBE_NAME<br />
DIMENSION_UNIQUE_NAME<br />
HIERARCHY_UNIQUE_NAME<br />
LEVEL_UNIQUE_NAME<br />
LEVEL_NUMBER<br />
順序付けが MEMBER_NAME<br />
MEMBER_UNIQUE_NAME<br />
MEMBER_CAPTION<br />
MEMBER_TYPE<br />
ツリー演算子 (詳細については、OLE DB for OLAP のマニュアルを参照してください)。</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaPrimaryKeys</strong></p></td>
<td><p>28</p></td>
<td><p>所定のユーザーがカタログに定義した主キー列を返します。
 (PRIMARY_KEYS 行セット)</p></td>
<td><p>PK_TABLE_CATALOG<br />
PK_TABLE_SCHEMA<br />
PK_TABLE_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaProcedureColumns</strong></p></td>
<td><p>29</p></td>
<td><p>プロシージャが返す行セットの列に関する情報を返します。
 (PROCEDURE_COLUMNS Rowset)</p></td>
<td><p>PROCEDURE_CATALOG<br />
PROCEDURE_SCHEMA<br />
PROCEDURE_NAME<br />
COLUMN_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaProcedureParameters</strong></p></td>
<td><p>26</p></td>
<td><p>プロシージャのパラメーターとリターン コードに関する情報を返します。
 (PROCEDURE_PARAMETERS 行セット)</p></td>
<td><p>PROCEDURE_CATALOG<br />
PROCEDURE_SCHEMA<br />
PROCEDURE_NAME<br />
PARAMETER_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaProcedures</strong></p></td>
<td><p>16</p></td>
<td><p>カタログに定義され、所定のユーザーが所有するプロシージャを返します。
 (PROCEDURES 行セット)</p></td>
<td><p>PROCEDURE_CATALOG<br />
PROCEDURE_SCHEMA<br />
PROCEDURE_NAME<br />
PROCEDURE_TYPE</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaProperties</strong></p></td>
<td><p>37</p></td>
<td><p>次元の各レベルで利用できるプロパティに関する情報を返します。
 (PROPERTIES 行セット *)</p></td>
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
<td><p>&lt;プロバイダーの特定&gt;</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaProviderTypes</strong></p></td>
<td><p>22</p></td>
<td><p>データ プロバイダーがサポートする (基本) データ型を返します。
 (PROVIDER_TYPES 行セット)</p></td>
<td><p>DATA_TYPE<br />
BEST_MATCH</p></td>
</tr>
<tr class="odd">
<td><p><strong>AdSchemaReferentialConstraints</strong></p></td>
<td><p>9</p></td>
<td><p>カタログに定義され、所定のユーザーが所有する参照制約を返します。
 (REFERENTIAL_CONSTRAINTS 行セット)</p></td>
<td><p>CONSTRAINT_CATALOG<br />
CONSTRAINT_SCHEMA<br />
CONSTRAINT_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaSchemata</strong></p></td>
<td><p>17</p></td>
<td><p>所定のユーザーが所有するスキーマ (データベース オブジェクト) を返します。
 (SCHEMATA 行セット)</p></td>
<td><p>CATALOG_NAME<br />
SCHEMA_NAME<br />
SCHEMA_OWNER</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaSQLLanguages</strong></p></td>
<td><p>18</p></td>
<td><p>カタログに定義された SQL 実装処理データがサポートする準拠レベル、オプション、および言語を返します。
 (SQL_LANGUAGES 行セット)</p></td>
<td><p>&lt;なし&gt;</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaStatistics</strong></p></td>
<td><p>19</p></td>
<td><p>カタログに定義され、所定のユーザーが所有する統計値を返します。
 (STATISTICS 行セット)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
TABLE_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaTableConstraints</strong></p></td>
<td><p>10</p></td>
<td><p>カタログに定義され、所定のユーザーが所有するテーブル制約を返します。
 (TABLE_CONSTRAINTS 行セット)</p></td>
<td><p>CONSTRAINT_CATALOG<br />
CONSTRAINT_SCHEMA<br />
CONSTRAINT_NAME<br />
TABLE_CATALOG<br />
TABLE_SCHEMA<br />
TABLE_NAME<br />
CONSTRAINT_TYPE</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaTablePrivileges</strong></p></td>
<td><p>14</p></td>
<td><p>カタログに定義され、所定のユーザーが利用できる、または権限を持つテーブルに対する特権を返します。
 (TABLE_PRIVILEGES 行セット)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
TABLE_NAME<br />
権限の許可者<br />
被設定者</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaTables</strong></p></td>
<td><p>20</p></td>
<td><p>カタログに定義され、所定のユーザーがアクセスできるテーブル (ビューも含む) を返します。
 (TABLES 行セット)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
TABLE_NAME<br />
TABLE_TYPE</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaTranslations</strong></p></td>
<td><p>21</p></td>
<td><p>カタログに定義され、所定のユーザーがアクセスできる文字変換を返します。
 (TRANSLATIONS 行セット)</p></td>
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
<td><p><strong>adSchemaUsagePrivileges</strong></p></td>
<td><p>15</p></td>
<td><p>カタログに定義され、所定のユーザーが利用できる、または権限を持つオブジェクトに対する USAGE 特権を返します。
 (USAGE_PRIVILEGES 行セット)</p></td>
<td><p>OBJECT_CATALOG<br />
OBJECT_SCHEMA<br />
OBJECT_NAME<br />
OBJECT_TYPE<br />
権限の許可者<br />
被設定者</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaViewColumnUsage</strong></p></td>
<td><p>24</p></td>
<td><p>カタログに定義され、所定のユーザーが所有する、表示テーブルが依存する列を返します。
 (VIEW_COLUMN_USAGE 行セット)</p></td>
<td><p>VIEW_CATALOG<br />
VIEW_SCHEMA<br />
VIEW_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaViews</strong></p></td>
<td><p>23</p></td>
<td><p>カタログに定義され、所定のユーザーがアクセスできるビューを返します。
 (VIEWS 行セット)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
TABLE_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaViewTableUsage</strong></p></td>
<td><p>25</p></td>
<td><p>カタログに定義され、所定のユーザーが所有し、表示テーブルが依存するテーブルを返します。
 (VIEW_TABLE_USAGE 行セット)</p></td>
<td><p>VIEW_CATALOG<br />
VIEW_SCHEMA<br />
VIEW_NAME</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>ADO/WFC に相当

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
<td><p>AdoEnums.Schema.ASSERTS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.CATALOGS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.CHARACTERSETS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.CHECKCONSTRAINTS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.COLLATIONS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.COLUMNPRIVILEGES</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.COLUMNS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.COLUMNSDOMAINUSAGE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.CONSTRAINTCOLUMNUSAGE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.CONSTRAINTTABLEUSAGE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.CUBES</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.DBINFOKEYWORDS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.DBINFOLITERALS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.DIMENSIONS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.FOREIGNKEYS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.HIERARCHIES</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.INDEXES</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.KEYCOLUMNUSAGE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.LEVELS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.MEASURES</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.MEMBERS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.PRIMARYKEYS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.PROCEDURECOLUMNS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.PROCEDUREPARAMETERS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.PROCEDURES</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.PROPERTIES</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.PROVIDERSPECIFIC</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.PROVIDERTYPES</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.REFERENTIALCONTRAINTS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.SCHEMATA</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.SQLLANGUAGES</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.STATISTICS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.TABLECONSTRAINTS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.TABLEPRIVILEGES</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.TABLES</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.TRANSLATIONS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.TRUSTEES</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.USAGEPRIVILEGES</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.VIEWCOLUMNUSAGE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.VIEWS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.VIEWTABLEUSAGE</p></td>
</tr>
</tbody>
</table>

