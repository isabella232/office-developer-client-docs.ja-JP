---
title: Field2.GetChunk メソッド (DAO)
TOCTitle: GetChunk Method
ms:assetid: 5d3a66c0-8216-d701-0a91-b79fbbc822b8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194600(v=office.15)
ms:contentKeyID: 48545101
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 09660c472a6fd799c111214dafe3266cdec9eced
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926648"
---
# <a name="field2getchunk-method-dao"></a>Field2.GetChunk メソッド (DAO)


**適用されます**Access 2013、Office 2013。

すべてを返します。 または**[Recordset](recordset-object-dao.md)** オブジェクトの**[Fields](fields-collection-dao.md)** コレクション内の**メモ**型または**長の BinaryField2**オブジェクトの内容の一部です。

## <a name="syntax"></a>構文

*式*です。GetChunk (***オフセット***、***バイト数***)

*式***Field2**オブジェクトを表す変数です。

### <a name="parameters"></a>パラメーター

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
<th><p>必須/オプション</p></th>
<th><p>データ型</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Offset</p></td>
<td><p>必須</p></td>
<td><p><strong>長整数型 (Long)</strong></p></td>
<td><p>コピーを開始する前にスキップするバイト数。</p></td>
</tr>
<tr class="even">
<td><p>バイト</p></td>
<td><p>必須</p></td>
<td><p><strong>長整数型 (Long)</strong></p></td>
<td><p>取得するバイト数。</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>戻り値

バリアント型

## <a name="remarks"></a>注釈

**GetChunk** から返されたバイト数は変数に代入されます。 **GetChunk** を使用して、データの値全体の一部を 1 つずつ取得します。分割された値を集めて元の値に戻すには、 **[AppendChunk](field-appendchunk-method-dao.md)** メソッドを使用します。

**オフセットが 0 の場合は、フィールドの最初のバイトからコピーが開始します。**

Numbytes がフィールド内のバイト数より大きい場合、 **GetChunk**はフィールドに実際の残りのバイト数を返します。


> [!NOTE]
> <P>[!メモ] 文字列の場合はメモ型 ( <STRONG>Memo</STRONG>) のフィールドを使用し、ロング バイナリ型 ( <STRONG>Long Binary</STRONG>) のフィールドにはバイナリ データのみ格納してください。この逆を行うと、予期しない結果を招きます。</P>



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
     
    Function CopyLargeField(fldSource As Field2, _ 
     fldDestination As Field2) 
     
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
