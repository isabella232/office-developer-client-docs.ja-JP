---
<<<<<<< ヘッド タイトル: PageSize プロパティ (ADO) TOCTitle: PageSize プロパティ (ADO) === タイトル: PageSize プロパティ (ADO) TOCTitle: PageSize プロパティ (ADO)
>>>>>>> マスターの ms:assetid: da56edd8-8947-aeff-2ef5-a8535c66575b ms:mtpsurl: https://msdn.microsoft.com/library/JJ250099(v=office.15) ms:contentKeyID: 48548079 ms.date: 2015/09/18 mtps_version: v=office.15
---

<<<<<<< ヘッド
# <a name="pagesize-property-ado"></a>PageSize プロパティ (ADO)
=======
# <a name="pagesize-property-ado"></a>PageSize プロパティ (ADO)
>>>>>>> master


**適用されます**Access 2013 |。Office 2013

[Recordset](recordset-object-ado.md) の 1 ページを構成するレコード数を示します。

<<<<<<< ヘッド
## <a name="settings-and-return-values"></a>設定値と戻り値
=======
## <a name="settings-and-return-values"></a>設定値および戻り値
>>>>>>> master

1 ページのレコード数を示す長整数型 ( **Long** ) の値を設定または取得します。既定値は 10 です。

## <a name="remarks"></a>解説

<<<<<<< ヘッドは、データの論理ページを構成するレコード数を決定するのには**PageSize**プロパティを使用します。 ページ サイズを設定すると、 [AbsolutePage](absolutepage-property-ado.md) プロパティを使用して、特定のページの最初のレコードに移動できます。 これは、Web サーバーで、ユーザーが一度に特定の数のレコードを表示しながら、データのページ間を移動できるようにする場合に便利です。
=== データの論理ページを構成するレコード数を決定するのには、 **PageSize**プロパティを使用します。 ページ サイズを設定すると、 [AbsolutePage](absolutepage-property-ado.md) プロパティを使用して、特定のページの最初のレコードに移動できます。 これは、機能は、同時にレコード数を表示、データのページにユーザーを許可すると、web サーバーのシナリオで便利です。
>>>>>>> master

このプロパティはいつでも設定でき、その値は、特定のページの最初のレコードの位置を計算するために使用されます。

