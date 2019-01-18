---
title: Field2.GetChunk メソッド (DAO)
TOCTitle: GetChunk method
ms:assetid: 5d3a66c0-8216-d701-0a91-b79fbbc822b8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194600(v=office.15)
ms:contentKeyID: 48545101
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6a4b850658ca4ab36b0d4f4cbed7266d39b4ff8d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722859"
---
# <a name="field2getchunk-method-dao"></a><span data-ttu-id="4e9b1-102">Field2.GetChunk メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="4e9b1-102">Field2.GetChunk method (DAO)</span></span>

<span data-ttu-id="4e9b1-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="4e9b1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4e9b1-104">すべてを返します。 または**[Recordset](recordset-object-dao.md)** オブジェクトの**[Fields](fields-collection-dao.md)** コレクション内の**メモ**型または**長の BinaryField2**オブジェクトの内容の一部です。</span><span class="sxs-lookup"><span data-stu-id="4e9b1-104">Returns all or a portion of the contents of a **Memo** or **Long BinaryField2** object in the **[Fields](fields-collection-dao.md)** collection of a **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e9b1-105">構文</span><span class="sxs-lookup"><span data-stu-id="4e9b1-105">Syntax</span></span>

<span data-ttu-id="4e9b1-106">*式*です。GetChunk (***オフセット***、***バイト数***)</span><span class="sxs-lookup"><span data-stu-id="4e9b1-106">*expression* .GetChunk(***Offset***, ***Bytes***)</span></span>

<span data-ttu-id="4e9b1-107">\*式\***Field2**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="4e9b1-107">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="4e9b1-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="4e9b1-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4e9b1-109">名前</span><span class="sxs-lookup"><span data-stu-id="4e9b1-109">Name</span></span></p></th>
<th><p><span data-ttu-id="4e9b1-110">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="4e9b1-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="4e9b1-111">データ型</span><span class="sxs-lookup"><span data-stu-id="4e9b1-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="4e9b1-112">説明</span><span class="sxs-lookup"><span data-stu-id="4e9b1-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4e9b1-113"><em>Offset</em></span><span class="sxs-lookup"><span data-stu-id="4e9b1-113"><em>Offset</em></span></span></p></td>
<td><p><span data-ttu-id="4e9b1-114">必須</span><span class="sxs-lookup"><span data-stu-id="4e9b1-114">Required</span></span></p></td>
<td><p><span data-ttu-id="4e9b1-115"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="4e9b1-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="4e9b1-116">コピーを開始する前にスキップするバイト数。</span><span class="sxs-lookup"><span data-stu-id="4e9b1-116">The number of bytes to skip before copying begins.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e9b1-117"><em>バイト</em></span><span class="sxs-lookup"><span data-stu-id="4e9b1-117"><em>Bytes</em></span></span></p></td>
<td><p><span data-ttu-id="4e9b1-118">必須</span><span class="sxs-lookup"><span data-stu-id="4e9b1-118">Required</span></span></p></td>
<td><p><span data-ttu-id="4e9b1-119"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="4e9b1-119"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="4e9b1-120">取得するバイト数。</span><span class="sxs-lookup"><span data-stu-id="4e9b1-120">The number of bytes you want to return.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="4e9b1-121">戻り値</span><span class="sxs-lookup"><span data-stu-id="4e9b1-121">Return value</span></span>

<span data-ttu-id="4e9b1-122">バリアント型</span><span class="sxs-lookup"><span data-stu-id="4e9b1-122">Variant</span></span>

## <a name="remarks"></a><span data-ttu-id="4e9b1-123">注釈</span><span class="sxs-lookup"><span data-stu-id="4e9b1-123">Remarks</span></span>

<span data-ttu-id="4e9b1-p101">**GetChunk** から返されたバイト数は変数に代入されます。 **GetChunk** を使用して、データの値全体の一部を 1 つずつ取得します。分割された値を集めて元の値に戻すには、 **[AppendChunk](field-appendchunk-method-dao.md)** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="4e9b1-p101">The bytes returned by **GetChunk** are assigned to variable. Use **GetChunk** to return a portion of the total data value at a time. You can use the **[AppendChunk](field-appendchunk-method-dao.md)** method to reassemble the pieces.</span></span>

<span data-ttu-id="4e9b1-127">**オフセットが 0 の場合は、フィールドの最初のバイトからコピーが開始します。**</span><span class="sxs-lookup"><span data-stu-id="4e9b1-127">If offset is 0, **GetChunk** begins copying from the first byte of the field.</span></span>

<span data-ttu-id="4e9b1-128">Numbytes がフィールド内のバイト数より大きい場合、 **GetChunk**はフィールドに実際の残りのバイト数を返します。</span><span class="sxs-lookup"><span data-stu-id="4e9b1-128">If numbytes is greater than the number of bytes in the field, **GetChunk** returns the actual number of remaining bytes in the field.</span></span>

> [!NOTE]
> <span data-ttu-id="4e9b1-p102">[!メモ] 文字列の場合はメモ型 ( **Memo**) のフィールドを使用し、ロング バイナリ型 ( **Long Binary**) のフィールドにはバイナリ データのみ格納してください。この逆を行うと、予期しない結果を招きます。</span><span class="sxs-lookup"><span data-stu-id="4e9b1-p102">Use a **Memo** field for text, and put binary data only in **Long Binary** fields. Doing otherwise will cause undesirable results.</span></span>

## <a name="example"></a><span data-ttu-id="4e9b1-131">例</span><span class="sxs-lookup"><span data-stu-id="4e9b1-131">Example</span></span>

<span data-ttu-id="4e9b1-p103">次の使用例では、 **AppendChunk** メソッドと **GetChunk** メソッドを使用して、別のレコードからのデータを一度に 32K ずつ読み込んで OLE オブジェクトのフィールドに設定します。実際のアプリケーションでは、たとえば、社員レコード (社員の写真を含む) をあるテーブルから別のテーブルにコピーするときに、このようなプロシージャを使用します。この使用例では、単にレコードを同じテーブルにコピーしています。すべてのブロック操作は、1 つの AddNew-Update シーケンス内で行われています。</span><span class="sxs-lookup"><span data-stu-id="4e9b1-p103">This example uses the **AppendChunk** and **GetChunk** methods to fill an OLE object field with data from another record, 32K at a time. In a real application, one might use a procedure like this to copy an employee record (including the employee's photo) from one table to another. In this example, the record is simply being copied back to same table. Note that all the chunk manipulation takes place within a single AddNew-Update sequence.</span></span>

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
