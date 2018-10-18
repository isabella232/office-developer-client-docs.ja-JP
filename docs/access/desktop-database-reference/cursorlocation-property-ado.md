---
<<<<<<< ヘッド タイトル: CursorLocation プロパティ (ADO) TOCTitle: CursorLocation プロパティ (ADO) === タイトル: CursorLocation プロパティ (ADO) TOCTitle: CursorLocation プロパティ (ADO)
>>>>>>> マスターの ms:assetid: 8a048bd4-ae25-a555-1c07-14364b7e6560 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249606(v=office.15) ms:contentKeyID: 48546182 ms.date: 2015/09/18 mtps_version: v=office.15
---

<<<<<<< ヘッド
# <a name="cursorlocation-property-ado"></a>CursorLocation プロパティ (ADO)
=======
# <a name="cursorlocation-property-ado"></a>CursorLocation プロパティ (ADO)
>>>>>>> master


**適用されます**Access 2013 |。Office 2013

カーソル サービスの場所を示します。

## <a name="settings-and-return-values"></a>設定値と戻り値

**CursorLocationEnum** 値のいずれか 1 つに設定可能な長整数型 ( [Long](cursorlocationenum.md) ) の値を設定または取得します。

## <a name="remarks"></a>解説

このプロパティで、プロバイダーにアクセス可能なさまざまなカーソル ライブラリの中からカーソル サービスを選択します。通常は、クライアント側カーソル ライブラリ、またはサーバー側カーソル ライブラリから選択します。

このプロパティ設定は、プロパティが設定された後に確立された接続のみに作用します。 **CursorLocation** プロパティを変更しても既存の接続には影響しません。

[Execute](https://msdn.microsoft.com/library/jj249832\(v=office.15\)) メソッドが返すカーソルは、この設定を継承します。 **Recordset** オブジェクトは、関連付けられた接続からこの設定を自動的に継承します。

このプロパティは、[Connection](connection-object-ado.md) または閉じている [Recordset](recordset-object-ado.md) 上では読み取り/書き込み可能ですが、開いている **Recordset** 上では読み取り専用になります。

**リモート データ サービスの使用法**使用すると、クライアント側の**レコード セット**または**接続**オブジェクトの**CursorLocation**プロパティは**adUseClient**にのみ設定できます。

