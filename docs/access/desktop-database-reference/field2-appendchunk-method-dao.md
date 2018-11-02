---
title: Field2.AppendChunk メソッド (DAO)
TOCTitle: AppendChunk Method
ms:assetid: 540cd02d-1fc6-81d1-ac08-1e3df72a7208
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194088(v=office.15)
ms:contentKeyID: 48544886
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052867
f1_categories:
- Office.Version=v15
ms.openlocfilehash: f999a0519fccb8f896ed07963db621065530c1a3
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929770"
---
# <a name="field2appendchunk-method-dao"></a>Field2.AppendChunk メソッド (DAO)


**適用されます**Access 2013、Office 2013。


文字列式からのデータを [**Recordset**](recordset-object-dao.md) の、メモ型 (Memo) またはロング バイナリ型 (Long Binary) の **Field2** オブジェクトに追加します。

## <a name="syntax"></a>構文

*式*です。AppendChunk (***Val***)

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
<td><p>Val</p></td>
<td><p>必須</p></td>
<td><p><strong>バリアント型 (Variant)</strong></p></td>
<td><p><strong>Field2</strong> オブジェクトに追加するデータが格納されている、サブタイプが文字列型 (String) であるバリアント型 (Variant) の式。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

**AppendChunk** メソッドおよび **GetChunk** メソッドを使用して、メモ型 (Memo) またはロング バイナリ型 (Long Binary) のフィールド内のデータのサブセットにアクセスできます。

メモ型 (Memo) またはロング バイナリ型 (Long Binary) のフィールドを操作するときに、これらのメソッドを使用して、文字列領域を確保することもできます。コピーなどの一部の操作では、一時的な文字列が使用されます。文字列領域が制限されている場合は、フィールド全体ではなく、1 つのフィールドをいくつかのブロックに分けて操作する必要があることがあります。

カレント レコードがない場合に **AppendChunk** を使用すると、エラーが発生します。


> [!NOTE]
> <P><A href="recordset-edit-method-dao.md"><STRONG>Edit</STRONG></A> メソッドまたは <A href="recordset-addnew-method-dao.md"><STRONG>AddNew</STRONG></A> メソッドの呼び出し後の <STRONG>AppendChunk</STRONG> の最初の操作では、既存のデータを上書きしてフィールドにデータを配置するだけです。同じ <STRONG>Edit</STRONG> または <STRONG>AddNew</STRONG> のセッションのその後の <STRONG>AppendChunk</STRONG> の呼び出しでは、既存のデータに追加されます。</P>



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
