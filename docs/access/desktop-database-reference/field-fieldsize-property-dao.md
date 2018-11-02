---
title: Field.FieldSize プロパティ (DAO)
TOCTitle: FieldSize Property
ms:assetid: c81bd5cb-6b7c-5390-2d6b-049143f2f3b6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823165(v=office.15)
ms:contentKeyID: 48547645
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a6253979acb6948347f11e4a1d9770461ee63691
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920558"
---
# <a name="fieldfieldsize-property-dao"></a>Field.FieldSize プロパティ (DAO)


**適用されます**Access 2013、Office 2013。


**[Recordset](field-object-dao.md)** オブジェクトの **[Fields](fields-collection-dao.md)** コレクション内にあるメモ型 (Memo) またはロング バイナリ型 (Long Binary) の **[Field](recordset-object-dao.md)** オブジェクトを、メモリではなくデータベースで使用する場合のバイト数を取得します。

## <a name="syntax"></a>構文

*式*です。フィールド サイズします。

*式***Field**オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

[**AppendChunk**](field-appendchunk-method-dao.md) メソッドおよび [**GetChunk**](field-getchunk-method-dao.md) メソッドは、 **FieldSize** プロパティを指定すると、大きなフィールドを操作できます。

ロング バイナリ型 (Long Binary) またはメモ型 (Memo) のフィールドのサイズは 64 KB を超えることがあるため、長整数型 ( **Long**) の変数を格納できるサイズを持つ変数に、 **FieldSize** プロパティで取得する値を割り当てる必要があります。

メモ型 (Memo) およびロング バイナリ型 (Long Binary) 以外の **Field** オブジェクトのサイズを調べるには、 **[Size](field-size-property-dao.md)** プロパティを使用します。

  - データベース サーバーまたは ODBC ドライバーがサーバー側カーソルをサポートしていない。

  - ODBC カーソル ライブラリを使用している (つまり、 **DefaultCursorDriver** プロパティが **dbUseODBC** に設定されているか、またはサーバーがサーバー側カーソルをサポートしていない状況で **dbUseDefault** に設定されている) 場合。

  - カーソルレス クエリを使用している (つまり、 **DefaultCursorDriver** プロパティが **dbUseNoCursor** に設定されている) 場合。

**FieldSize**プロパティと、VBA **Len()** 関数または**LenB()** 関数は、同じ文字列の長さと異なる値を返すことがあります。 文字列は、マルチバイトの文字セット (MBCS) のフォームですが、Unicode 形式で VBA を通じて公開されている [Microsoft Access データベースに格納されます。 その結果、 **Len()** 関数は文字数を返します常に、 **lenb 関数**は、常に文字 (Unicode は、文字ごとに 2 バイトを使用) を X 2、数を返しますが、**フィールド サイズ**は文字列を返す場合の間にいくつかの値MBCS 文字があります。 などの 3 つから成る文字列を指定する通常の文字と 2 つの MBCS 文字、 **Len()** を返す 5、 **LenB()** は 10 を返します、**フィールド サイズ**は 7 では、それぞれ通常の文字と MBCS 文字ごとに 2 の 1 の合計を返します

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
