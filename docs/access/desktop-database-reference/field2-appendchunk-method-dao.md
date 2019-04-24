---
title: Field2 の chunk メソッド (DAO)
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
localization_priority: Normal
ms.openlocfilehash: fda1ab5a3e339d951225f4f43ab4275cce2cdb80
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292882"
---
# <a name="field2appendchunk-method-dao"></a>Field2 の chunk メソッド (DAO)

**適用先:** Access 2013、Office 2013

文字列式からのデータを [**Recordset**](recordset-object-dao.md) の、メモ型 (Memo) またはロング バイナリ型 (Long Binary) の **Field2** オブジェクトに追加します。

## <a name="syntax"></a>構文

*式*。appendchunk (***Val***)

*式***Field2**オブジェクトを表す変数を取得します。

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
<th><p>必須/オプション</p></th>
<th><p>データ型</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Val</em></p></td>
<td><p>必須</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>Field2</strong> オブジェクトに追加するデータが格納されている、サブタイプが文字列型 (String) であるバリアント型 (Variant) の式。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

**AppendChunk** メソッドおよび **GetChunk** メソッドを使用して、メモ型 (Memo) またはロング バイナリ型 (Long Binary) のフィールド内のデータのサブセットにアクセスできます。

メモ型 (Memo) またはロング バイナリ型 (Long Binary) のフィールドを操作するときに、これらのメソッドを使用して、文字列領域を確保することもできます。コピーなどの一部の操作では、一時的な文字列が使用されます。文字列領域が制限されている場合は、フィールド全体ではなく、1 つのフィールドをいくつかのブロックに分けて操作する必要があることがあります。

カレント レコードがない場合に **AppendChunk** を使用すると、エラーが発生します。

> [!NOTE]
> [**Edit**](recordset-edit-method-dao.md) メソッドまたは [**AddNew**](recordset-addnew-method-dao.md) メソッドの呼び出し後の **AppendChunk** の最初の操作では、既存のデータを上書きしてフィールドにデータを配置するだけです。同じ **Edit** または **AddNew** のセッションのその後の **AppendChunk** の呼び出しでは、既存のデータに追加されます。

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
