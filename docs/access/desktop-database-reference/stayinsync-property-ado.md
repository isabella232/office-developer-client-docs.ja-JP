---
<<<<<<< ヘッド タイトル: StayInSync プロパティ (ADO) TOCTitle: StayInSync プロパティ (ADO) === タイトル: StayInSync プロパティ (ADO) TOCTitle: StayInSync プロパティ (ADO)
>>>>>>> マスターの ms:assetid: 02c95c10-4032-14e1-e506-f334a8787142 ms:mtpsurl: https://msdn.microsoft.com/library/JJ248792(v=office.15) ms:contentKeyID: 48542966 ms.date: 2015/09/18 mtps_version: v=office.15
---

<<<<<<< ヘッド
# <a name="stayinsync-property-ado"></a>StayInSync プロパティ (ADO)
=======
# <a name="stayinsync-property-ado"></a>StayInSync プロパティ (ADO)
>>>>>>> master


**適用されます**Access 2013 |。Office 2013

親の行の位置が変更されたときに、基になる子のレコード (つまり、この*章*) への参照が変更されたかどうかを階層[レコード セット](recordset-object-ado.md)オブジェクト内に示します。

<<<<<<< ヘッド
## <a name="settings-and-return-values"></a>設定値と戻り値
=======
## <a name="settings-and-return-values"></a>設定値および戻り値
>>>>>>> master

ブール型 ( **Boolean** ) の値を設定または取得します。既定値は **True** です。 **True** の場合は、親の **Recordset** オブジェクトの行位置が変更されるとチャプターが更新されます。 **False** の場合は、親の **Recordset** オブジェクトの行位置が変更されても、チャプターは以前のチャプターのデータを参照し続けます。

## <a name="remarks"></a>解説

このプロパティは、[Microsoft Data Shaping Service for OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) によってサポートされるような階層 Recordset に適用され、子の **Recordset** を取得する前に親の **Recordset** を設定しておく必要があります。このプロパティによって、階層レコードセット内の移動が容易になります。

