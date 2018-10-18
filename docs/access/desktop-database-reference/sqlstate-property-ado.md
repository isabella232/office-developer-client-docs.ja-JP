---
<<<<<<< ヘッド タイトル: SQLState プロパティ (ADO) TOCTitle: SQLState プロパティ (ADO) === タイトル: SQLState プロパティ (ADO) TOCTitle: SQLState プロパティ (ADO)
>>>>>>> マスターの ms:assetid: cf3b078a-849e-1ad2-cba4-a26160080868 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250029(v=office.15) ms:contentKeyID: 48547806 ms.date: 2015/09/18 mtps_version: v=office.15
---

<<<<<<< ヘッド
# <a name="sqlstate-property-ado"></a>SQLState プロパティ (ADO)
=======
# <a name="sqlstate-property-ado"></a>SQLState プロパティ (ADO)
>>>>>>> master


**適用されます**Access 2013 |。Office 2013

特定の [Error](error-object-ado.md) オブジェクトの SQL 状態を示します。

<<<<<<< ヘッド
## <a name="return-value"></a>戻り値
=======
## <a name="return-value"></a>戻り値
>>>>>>> master

ANSI SQL 標準に準拠し、エラー コードを示す 5 文字の文字列型 ( **String** ) の値を返します。

## <a name="remarks"></a>解説

SQL ステートメントの処理中にエラーが発生した場合に、プロバイダーが返す 5 文字のエラー コードを取得するには **SQLState** プロパティを使用します。たとえば、Microsoft OLE DB Provider for ODBC を Microsoft SQL Server データベースと共に使用する場合、ODBC に固有のエラー、または Microsoft SQL Server に起因するエラーに基づいて、ODBC から SQL 状態のエラー コードが生成された後、ODBC エラーにマップされます。これらのエラー コードは ANSI SQL 標準で規定されていますが、実装方法はデータ ソースによって異なる場合があります。

