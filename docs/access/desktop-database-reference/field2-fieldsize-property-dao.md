---
title: Field2.FieldSize プロパティ (DAO)
TOCTitle: FieldSize Property
ms:assetid: d609801d-7761-663f-2840-de5923bb120c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835039(v=office.15)
ms:contentKeyID: 48547976
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052870
f1_categories:
- Office.Version=v15
ms.openlocfilehash: b9021d8a9644dba7cbbb10711f1ecaa3e8b101c0
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25918857"
---
# <a name="field2fieldsize-property-dao"></a><span data-ttu-id="1ac03-102">Field2.FieldSize プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="1ac03-102">Field2.FieldSize property (DAO)</span></span>


<span data-ttu-id="1ac03-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="1ac03-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="1ac03-104">メモリではなくデータベースで使用される、 [**Recordset**](fields-collection-dao.md) オブジェクトの [**Fields**](recordset-object-dao.md) コレクションに含まれるメモ型 (Memo) またはロング バイナリ型 (Long Binary) の **Field2** オブジェクトのバイト数を返します。</span><span class="sxs-lookup"><span data-stu-id="1ac03-104">Returns the number of bytes used in the database (rather than in memory) of a Memo or Long Binary **Field2** object in the **[Fields](fields-collection-dao.md)** collection of a **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ac03-105">構文</span><span class="sxs-lookup"><span data-stu-id="1ac03-105">Syntax</span></span>

<span data-ttu-id="1ac03-106">*式*です。フィールド サイズします。</span><span class="sxs-lookup"><span data-stu-id="1ac03-106">*expression* .FieldSize</span></span>

<span data-ttu-id="1ac03-107">\*式\***Field2**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="1ac03-107">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ac03-108">注釈</span><span class="sxs-lookup"><span data-stu-id="1ac03-108">Remarks</span></span>

<span data-ttu-id="1ac03-109">[**AppendChunk**](field-appendchunk-method-dao.md) メソッドおよび [**GetChunk**](field-getchunk-method-dao.md) メソッドは、 **FieldSize** プロパティを指定すると、大きなフィールドを操作できます。</span><span class="sxs-lookup"><span data-stu-id="1ac03-109">You can use **FieldSize** with the **[AppendChunk](field-appendchunk-method-dao.md)** and **[GetChunk](field-getchunk-method-dao.md)** methods to manipulate large fields.</span></span>

<span data-ttu-id="1ac03-110">ロング バイナリ型 (Long Binary) またはメモ型 (Memo) のフィールドのサイズは 64K を超える可能性があるため、 **FieldSize** によって返された値は、長整数型 ( **Long**) の変数を格納できる大きさの変数に代入する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1ac03-110">Because the size of a Long Binary or Memo field can exceed 64K, you should assign the value returned by **FieldSize** to a variable large enough to store a **Long** variable.</span></span>

<span data-ttu-id="1ac03-111">メモ型 (Memo) およびロング バイナリ型 (Long Binary) 以外の **Field2** オブジェクトのサイズを確認するには、 **[Size](field-size-property-dao.md)** プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="1ac03-111">To determine the size of a **Field2** object other than Memo and Long Binary types, use the **[Size](field-size-property-dao.md)** property.</span></span>

  - <span data-ttu-id="1ac03-112">データベース サーバーまたは ODBC ドライバーがサーバー側カーソルをサポートしていない場合。</span><span class="sxs-lookup"><span data-stu-id="1ac03-112">If the database server or ODBC driver does not support server-side cursors.</span></span>

  - <span data-ttu-id="1ac03-113">ODBC カーソル ライブラリを使用している (つまり、 **DefaultCursorDriver** プロパティが **dbUseODBC** に設定されているか、またはサーバーがサーバー側カーソルをサポートしていない状況で **dbUseDefault** に設定されている) 場合。</span><span class="sxs-lookup"><span data-stu-id="1ac03-113">If you are using the ODBC cursor library (that is, the **DefaultCursorDriver** property is set to **dbUseODBC**, or to **dbUseDefault** when the server does not support server-side cursors).</span></span>

  - <span data-ttu-id="1ac03-114">カーソルレス クエリを使用している (つまり、 **DefaultCursorDriver** プロパティが **dbUseNoCursor** に設定されている) 場合。</span><span class="sxs-lookup"><span data-stu-id="1ac03-114">If you are using a cursorless query (that is, the **DefaultCursorDriver** property is set to **dbUseNoCursor**).</span></span>

<span data-ttu-id="1ac03-115">**FieldSize**プロパティと、VBA **Len()** 関数または**LenB()** 関数は、同じ文字列の長さと異なる値を返すことがあります。</span><span class="sxs-lookup"><span data-stu-id="1ac03-115">The **FieldSize** property and the VBA **Len()** or **LenB()** functions may return different values as the length of the same string.</span></span> <span data-ttu-id="1ac03-116">文字列は、マルチバイトの文字セット (MBCS) のフォームですが、Unicode 形式で VBA を通じて公開されている [Microsoft Access データベースに格納されます。</span><span class="sxs-lookup"><span data-stu-id="1ac03-116">Strings are stored in a Microsoft Access database in multi-byte character set (MBCS) form, but exposed through VBA in Unicode format.</span></span> <span data-ttu-id="1ac03-117">その結果、 **Len()** 関数は文字数を返します常に、 **lenb 関数**は、常に文字 (Unicode は、文字ごとに 2 バイトを使用) を X 2、数を返しますが、**フィールド サイズ**は文字列を返す場合の間にいくつかの値MBCS 文字があります。</span><span class="sxs-lookup"><span data-stu-id="1ac03-117">As a result, the **Len()** function will always return the number of characters, **LenB** will always return the number of characters X 2 (Unicode uses two bytes for each character), but **FieldSize** will return some value in between if the string has any MBCS characters.</span></span> <span data-ttu-id="1ac03-118">などの 3 つから成る文字列を指定する通常の文字と 2 つの MBCS 文字、 **Len()** を返す 5、 **LenB()** は 10 を返します、**フィールド サイズ**は 7 では、それぞれ通常の文字と MBCS 文字ごとに 2 の 1 の合計を返します</span><span class="sxs-lookup"><span data-stu-id="1ac03-118">For example, given a string consisting of three normal characters and two MBCS characters, **Len()** will return 5, **LenB()** will return 10, and **FieldSize** will return 7, the sum of 1 for each normal character and 2 for each MBCS character.</span></span>

## <a name="example"></a><span data-ttu-id="1ac03-119">例</span><span class="sxs-lookup"><span data-stu-id="1ac03-119">Example</span></span>

<span data-ttu-id="1ac03-120">次の使用例は、 **FieldSize** プロパティを使用して、2 つの異なるテーブルのメモ型 (Memo) とロング バイナリ型 (Long Binary) の Field オブジェクトで使用されるバイト数を一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="1ac03-120">This example uses the **FieldSize** property to list the number of bytes used by the Memo and Long Binary Field objects in two different tables.</span></span>

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

<span data-ttu-id="1ac03-p102">次の使用例では、 **AppendChunk** メソッドと **GetChunk** メソッドを使用して、別のレコードからのデータを一度に 32K ずつ読み込んで OLE オブジェクトのフィールドに設定します。実際のアプリケーションでは、たとえば、社員レコード (社員の写真を含む) をあるテーブルから別のテーブルにコピーするときに、このようなプロシージャを使用します。この使用例では、単にレコードを同じテーブルにコピーしています。すべてのブロック操作は、1 つの AddNew-Update シーケンス内で行われています。</span><span class="sxs-lookup"><span data-stu-id="1ac03-p102">This example uses the **AppendChunk** and **GetChunk** methods to fill an OLE object field with data from another record, 32K at a time. In a real application, one might use a procedure like this to copy an employee record (including the employee's photo) from one table to another. In this example, the record is simply being copied back to same table. Note that all the chunk manipulation takes place within a single AddNew-Update sequence.</span></span>

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
