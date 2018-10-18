---
<<<<<<< ヘッド タイトル: MaxRecords プロパティ (ADO) TOCTitle: MaxRecords プロパティ (ADO) === タイトル: MaxRecords プロパティ (ADO) TOCTitle: MaxRecords プロパティ (ADO)
>>>>>>> マスターの ms:assetid: 424b2d41-073a-3fbe-30aa-99fac94f9a81 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249195(v=office.15) ms:contentKeyID: 48544475 ms.date: 2015/09/18 mtps_version: v=office.15
---

<<<<<<< ヘッド
# <a name="maxrecords-property-ado"></a>MaxRecords プロパティ (ADO)
=======
# <a name="maxrecords-property-ado"></a>MaxRecords プロパティ (ADO)
>>>>>>> master


**適用されます**Access 2013 |。Office 2013

クエリから [Recordset](recordset-object-ado.md) に返す最大レコード数を示します。

<<<<<<< ヘッド
## <a name="settings-and-return-values"></a>設定値と戻り値
=======
## <a name="settings-and-return-values"></a>設定値および戻り値
>>>>>>> master

返される最大レコード数を示す長整数型 ( **Long** ) の値を設定または取得します。既定値は 0 (制限なし) です。

## <a name="remarks"></a>解説

**MaxRecords** プロパティは、プロバイダーがデータ ソースから返すレコード数を制限するために使用します。このプロパティの既定値は 0 で、プロバイダーが要求されたすべてのレコードを返すことを意味します。

**MaxRecords** プロパティは、 **Recordset** が閉じているときは読み取り/書き込み可能で、開いているときは読み取り専用になります。

