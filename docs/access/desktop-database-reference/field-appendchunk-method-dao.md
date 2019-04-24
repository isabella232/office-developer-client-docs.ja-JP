---
title: フィールド appendchunk メソッド (DAO)
TOCTitle: AppendChunk Method
ms:assetid: f98c6862-fecf-06cb-a7c0-42b0d3150a06
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837014(v=office.15)
ms:contentKeyID: 48548819
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b1ce1c359582194ce87dfaf4f409be4303486e09
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293169"
---
# <a name="fieldappendchunk-method-dao"></a>フィールド appendchunk メソッド (DAO)

**適用先:** Access 2013、Office 2013

文字列式から **[Recordset](field-object-dao.md)** のメモ型 (Memo) またはロング バイナリ型 (Long Binary) の **[Field](recordset-object-dao.md)** オブジェクトにデータを追加します。

## <a name="syntax"></a>構文

*式*。appendchunk (***Val***)

*式***Field**オブジェクトを表す変数を取得します。

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
<td><p><strong>Field</strong> オブジェクトに追加するバリアント型 (Variant) (文字列型 (String) サブタイプ) の式または変数です。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

**AppendChunk** メソッドと **[GetChunk](field-getchunk-method-dao.md)** メソッドを使用して、Memo フィールドまたは Long Binary フィールドのデータのサブセットにアクセスします。

この 2 つのメソッドを使用すると、Memo フィールドと Long Binary フィールドを操作する際に文字列のスペースを確保できます。コピーなどの操作では、一時的な文字列を使用します。文字列のスペースが限られている場合、フィールド全体ではなく一部の操作が必要な場合もあります。

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
