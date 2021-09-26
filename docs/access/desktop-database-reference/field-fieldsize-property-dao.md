---
title: Field.FieldSize プロパティ (DAO)
TOCTitle: FieldSize Property
ms:assetid: c81bd5cb-6b7c-5390-2d6b-049143f2f3b6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823165(v=office.15)
ms:contentKeyID: 48547645
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: eaa25eaf1ac7070eddb87e9be53077a094c9556b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59626681"
---
# <a name="fieldfieldsize-property-dao"></a>Field.FieldSize プロパティ (DAO)


**適用先**: Access 2013、Office 2013


**[Recordset](field-object-dao.md)** オブジェクトの **[Fields](fields-collection-dao.md)** コレクション内にあるメモ型 (Memo) またはロング バイナリ型 (Long Binary) の **[Field](recordset-object-dao.md)** オブジェクトを、メモリではなくデータベースで使用する場合のバイト数を取得します。

## <a name="syntax"></a>構文

*式* .FieldSize

*expression*: **Field** オブジェクトを表す変数。

## <a name="remarks"></a>注釈

[**AppendChunk**](field-appendchunk-method-dao.md) メソッドおよび [**GetChunk**](field-getchunk-method-dao.md) メソッドは、 **FieldSize** プロパティを指定すると、大きなフィールドを操作できます。

ロング バイナリ型 (Long Binary) またはメモ型 (Memo) のフィールドのサイズは 64 KB を超えることがあるため、長整数型 ( **Long**) の変数を格納できるサイズを持つ変数に、 **FieldSize** プロパティで取得する値を割り当てる必要があります。

メモ型 (Memo) およびロング バイナリ型 (Long Binary) 以外の **Field** オブジェクトのサイズを調べるには、 **[Size](field-size-property-dao.md)** プロパティを使用します。

  - データベース サーバーまたは ODBC ドライバーがサーバー側カーソルをサポートしていない。

  - ODBC カーソル ライブラリを使用している (つまり、 **DefaultCursorDriver** プロパティが **dbUseODBC** に設定されているか、またはサーバーがサーバー側カーソルをサポートしていない状況で **dbUseDefault** に設定されている) 場合。

  - カーソルレス クエリを使用している (つまり、 **DefaultCursorDriver** プロパティが **dbUseNoCursor** に設定されている) 場合。

The **FieldSize** property and the VBA **Len()** or **LenB()** functions may return different values as the length of the same string. Strings are stored in a Microsoft Access database in multi-byte character set (MBCS) form, but exposed through VBA in Unicode format. As a result, the **Len()** function will always return the number of characters, **LenB** will always return the number of characters X 2 (Unicode uses two bytes for each character), but **FieldSize** will return some value in between if the string has any MBCS characters. For example, given a string consisting of three normal characters and two MBCS characters, **Len()** will return 5, **LenB()** will return 10, and **FieldSize** will return 7, the sum of 1 for each normal character and 2 for each MBCS character.

## <a name="example"></a>例

次の使用例は、 **FieldSize** プロパティを使用して、2 つの異なるテーブルのメモ型 (Memo) とロング バイナリ型 (Long Binary) の Field オブジェクトで使用されるバイト数を一覧表示します。

```vb
    Sub FieldSizeX() 
     
     Dim dbsNorthwind As Database 
     Dim rstCategories As Recordset 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstCategories = _ 
     dbsNorthwind.OpenRecordset("Categories", _ 
     dbOpenDynaset) 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     
     Debug.Print _ 
     "Field sizes from records in Categories table" 
     
     With rstCategories 
     Debug.Print " CategoryName - " & _ 
     "Description (bytes) - Picture (bytes)" 
     
     ' Enumerate the Categories Recordset and print the size 
     ' in bytes of the picture field for each record. 
     Do While Not .EOF 
     Debug.Print " " & !CategoryName & " - " & _ 
     !Description.FieldSize & " - " & _ 
     !Picture.FieldSize 
     .MoveNext 
     Loop 
     
     .Close 
     End With 
     
     Debug.Print "Field sizes from records in Employees table" 
     
     With rstEmployees 
     Debug.Print " LastName - Notes (bytes) - " & _ 
     "Photo (bytes)" 
     
     ' Enumerate the Employees Recordset and print the size 
     ' in bytes of the picture field for each record. 
     Do While Not .EOF 
     Debug.Print " " & !LastName & " - " & _ 
     !Notes.FieldSize & " - " & !Photo.FieldSize 
     .MoveNext 
     Loop 
     
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
```

<br/>

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
