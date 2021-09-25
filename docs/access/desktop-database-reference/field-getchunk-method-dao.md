---
title: Field.GetChunk メソッド (DAO)
TOCTitle: GetChunk Method
ms:assetid: b8984e79-54f7-8052-85a3-d12033daf7a1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822448(v=office.15)
ms:contentKeyID: 48547328
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052871
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 4219445f4e0369479023cffad59899b0aba95232
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602641"
---
# <a name="fieldgetchunk-method-dao"></a>Field.GetChunk メソッド (DAO)

**適用先**: Access 2013、Office 2013

Recordset オブジェクトの Fields コレクション内のMemo オブジェクトまたは **Long** Binary **[](fields-collection-dao.md)** **[Field](field-object-dao.md)** オブジェクトの内容のすべてまたは一部を **[返](recordset-object-dao.md)** します。

## <a name="syntax"></a>構文

*式* .GetChunk(***Offset** _, _*_Bytes_**)

*expression*: **Field** オブジェクトを表す変数。

## <a name="parameters"></a>パラメーター

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>名前</p></th>
<th><p>必須かどうか</p></th>
<th><p>データ型</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Offset</em></p></td>
<td><p>必須</p></td>
<td><p><strong>Long</strong></p></td>
<td><p>コピーを開始する前にスキップするバイト数。</p></td>
</tr>
<tr class="even">
<td><p><em>バイト数</em></p></td>
<td><p>必須</p></td>
<td><p><strong>Long</strong></p></td>
<td><p>取得するバイト数。</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>戻り値

バリアント型

## <a name="remarks"></a>注釈

**GetChunk** から返されたバイト数は変数に代入されます。 **GetChunk** を使用して、データの値全体の一部を 1 つずつ取得します。分割された値を集めて元の値に戻すには、 **[AppendChunk](field-appendchunk-method-dao.md)** メソッドを使用します。

offset が 0 の場合 **、GetChunk は** フィールドの最初のバイトからコピーを開始します。

numbytes がフィールド内のバイト数より大きい場合 **、GetChunk** はフィールド内の残りの実際のバイト数を返します。

> [!NOTE]
> [!メモ] 文字列の場合はメモ型 ( **Memo**) のフィールドを使用し、ロング バイナリ型 ( **Long Binary**) のフィールドにはバイナリ データのみ格納してください。この逆を行うと、予期しない結果を招きます。

## <a name="example"></a>例

次の使用例では、 **AppendChunk** メソッドと **GetChunk** メソッドを使用して、別のレコードからのデータを一度に 32K ずつ読み込んで OLE オブジェクトのフィールドに設定します。実際のアプリケーションでは、たとえば、社員レコード (社員の写真を含む) をあるテーブルから別のテーブルにコピーするときに、このようなプロシージャを使用します。この使用例では、単にレコードを同じテーブルにコピーしています。すべてのブロック操作は、1 つの AddNew-Update シーケンス内で行われています。

```vb
    Sub AppendChunkX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     Dim rstEmployees2 As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     ' Open two recordsets from the Employees table. 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     Set rstEmployees2 = rstEmployees.Clone 
     
     ' Add a new record to the first Recordset and copy the 
     ' data from a record in the second Recordset. 
     With rstEmployees 
     .AddNew 
     !FirstName = rstEmployees2!FirstName 
     !LastName = rstEmployees2!LastName 
     CopyLargeField rstEmployees2!Photo, !Photo 
     .Update 
     
     ' Delete new record because this is a demonstration. 
     .Bookmark = .LastModified 
     .Delete 
     .Close 
     End With 
     
     rstEmployees2.Close 
     dbsNorthwind.Close 
     
    End Sub 
     
    Function CopyLargeField(fldSource As Field, _ 
     fldDestination As Field) 
     
     ' Set size of chunk in bytes. 
     Const conChunkSize = 32768 
     
     Dim lngOffset As Long 
     Dim lngTotalSize As Long 
     Dim strChunk As String 
     
     ' Copy the photo from one Recordset to the other in 32K 
     ' chunks until the entire field is copied. 
     lngTotalSize = fldSource.FieldSize 
     Do While lngOffset < lngTotalSize 
     strChunk = fldSource.GetChunk(lngOffset, conChunkSize) 
     fldDestination.AppendChunk strChunk 
     lngOffset = lngOffset + conChunkSize 
     Loop 
     
    End Function
```
