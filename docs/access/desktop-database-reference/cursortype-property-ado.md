---
<<<<<<< ヘッド タイトル: CursorType プロパティ (ADO) TOCTitle: CursorType プロパティ (ADO) === タイトル: CursorType プロパティ (ADO) TOCTitle: CursorType プロパティ (ADO)
>>>>>>> マスターの ms:assetid: f42ded8f-9f92-ef03-a198-ffb892324611 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250239(v=office.15) ms:contentKeyID: 48548682 ms.date: 2015/09/18 mtps_version: v=office.15
---

<<<<<<< 見出し
# <a name="cursortype-property-ado"></a>CursorType プロパティ (ADO)
=======
# <a name="cursortype-property-ado"></a>CursorType プロパティ (ADO)
>>>>>>> master


**適用されます**Access 2013 |。Office 2013

[Recordset](recordset-object-ado.md) オブジェクトで使用されているカーソルの種類を示します。

<<<<<<< 見出し
## <a name="settings-and-return-values"></a>設定値と戻り値
=======
## <a name="settings-and-return-values"></a>設定値および戻り値
>>>>>>> master

[CursorTypeEnum](cursortypeenum.md) の値を設定または取得します。既定値は **adOpenForwardOnly** です。

## <a name="remarks"></a>解説

**CursorType** プロパティでは、 **Recordset** オブジェクトを開くときに使うカーソルの種類を指定します。

**CursorLocation** プロパティが [adUseClient](cursorlocation-property-ado.md) に設定されている場合は、 **adOpenStatic** の設定だけがサポートされます。サポートされていない値が設定された場合でも、エラーは発生しません。サポートされている **CursorType** のうち、一番近い値で代用されます。

要求されたカーソルの種類をサポートしていない場合、プロバイダーは他のカーソルの種類を返します。**Recordset** オブジェクトが開いているときには、 [CursorType](recordset-object-ado.md) プロパティは実際に使用されているカーソルの種類に合わせて変更されます。返されたカーソル特有の機能を調べるには、 [Supports](supports-method-ado.md) メソッドを使用します。 **Recordset** を閉じると、 **CursorType** プロパティは元の設定値に戻ります。

次の表では、各カーソルの種類に必要なプロバイダーの機能 ( **Supports** メソッドの定数によって識別されます) を示します。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Recordset の CursorType</p></th>
<th><p>Supports メソッドが True を返す定数</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adOpenForwardOnly</strong></p></td>
<td><p>none</p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenKeyset</strong></p></td>
<td><p><strong>adBookmark</strong>、 <strong>adHoldRecords</strong>、 <strong>adMovePrevious</strong>、 <strong>adResync</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>adOpenDynamic</strong></p></td>
<td><p><strong>adMovePrevious</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenStatic</strong></p></td>
<td><p><strong>adBookmark</strong>、 <strong>adHoldRecords</strong>、 <strong>adMovePrevious</strong>、 <strong>adResync</strong></p></td>
</tr>
</tbody>
</table>


> [!NOTE]
> 動的カーソルまたは前方のみカーソルで **Supports**(**adUpdateBatch**) が True を返すことがありますが、一括更新ではキーセット カーソルまたは静的カーソルを使用する必要があります。一括更新に必要な Cursor Service for OLE DB を有効にするには、[LockType](locktype-property-ado.md) プロパティを **adLockBatchOptimistic** に設定し、**CursorLocation** プロパティを **adUseClient** に設定します。

**CursorType** プロパティは、 **Recordset** が閉じているときは読み取り/書き込み可能で、開いているときは読み取り専用になります。

**リモート データ サービスの使用法**クライアント側の Recordset オブジェクトで使用するとは、 **adOpenStatic**にのみ**CursorType**プロパティを設定できます。

