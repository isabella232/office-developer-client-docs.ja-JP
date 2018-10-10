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
ms.openlocfilehash: 2931dcda3c344163f7286222d354f9303966ba45
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479183"
---
# <a name="fieldgetchunk-method-dao"></a><span data-ttu-id="0d6b7-102">Field.GetChunk メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="0d6b7-102">Field.GetChunk Method (DAO)</span></span>


<span data-ttu-id="0d6b7-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="0d6b7-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0d6b7-104">\*\*\*\*Recordset\*\*\*\* オブジェクトの **[Fields](field-object-dao.md)** コレクションに含まれる、メモ型 ( [Memo](fields-collection-dao.md)) またはロング バイナリ型 ( **Long Binary**) の **[Field](recordset-object-dao.md)** オブジェクトについて、全部または一部の内容を取得します。</span><span class="sxs-lookup"><span data-stu-id="0d6b7-104">Returns all or a portion of the contents of a **Memo** or **Long Binary** **[Field](field-object-dao.md)** object in the **[Fields](fields-collection-dao.md)** collection of a **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d6b7-105">構文</span><span class="sxs-lookup"><span data-stu-id="0d6b7-105">Syntax</span></span>

<span data-ttu-id="0d6b7-106">*式*です。GetChunk (***オフセット***、***バイト数***)</span><span class="sxs-lookup"><span data-stu-id="0d6b7-106">*expression* .GetChunk(***Offset***, ***Bytes***)</span></span>

<span data-ttu-id="0d6b7-107">\*式\***Field**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="0d6b7-107">*expression* A variable that represents a **Field** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="0d6b7-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0d6b7-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0d6b7-109">名前</span><span class="sxs-lookup"><span data-stu-id="0d6b7-109">Name</span></span></p></th>
<th><p><span data-ttu-id="0d6b7-110">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="0d6b7-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="0d6b7-111">データ型</span><span class="sxs-lookup"><span data-stu-id="0d6b7-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="0d6b7-112">説明</span><span class="sxs-lookup"><span data-stu-id="0d6b7-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0d6b7-113">Offset</span><span class="sxs-lookup"><span data-stu-id="0d6b7-113">Offset</span></span></p></td>
<td><p><span data-ttu-id="0d6b7-114">必須</span><span class="sxs-lookup"><span data-stu-id="0d6b7-114">Required</span></span></p></td>
<td><p><span data-ttu-id="0d6b7-115"><strong>長整数型 (Long)</strong></span><span class="sxs-lookup"><span data-stu-id="0d6b7-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="0d6b7-116">コピーを開始する前にスキップするバイト数。</span><span class="sxs-lookup"><span data-stu-id="0d6b7-116">The number of bytes to skip before copying begins.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0d6b7-117">バイト</span><span class="sxs-lookup"><span data-stu-id="0d6b7-117">Bytes</span></span></p></td>
<td><p><span data-ttu-id="0d6b7-118">必須</span><span class="sxs-lookup"><span data-stu-id="0d6b7-118">Required</span></span></p></td>
<td><p><span data-ttu-id="0d6b7-119"><strong>長整数型 (Long)</strong></span><span class="sxs-lookup"><span data-stu-id="0d6b7-119"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="0d6b7-120">取得するバイト数。</span><span class="sxs-lookup"><span data-stu-id="0d6b7-120">The number of bytes you want to return.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="0d6b7-121">戻り値</span><span class="sxs-lookup"><span data-stu-id="0d6b7-121">Return Value</span></span>

<span data-ttu-id="0d6b7-122">バリアント型 (Variant)</span><span class="sxs-lookup"><span data-stu-id="0d6b7-122">Variant</span></span>

## <a name="remarks"></a><span data-ttu-id="0d6b7-123">注釈</span><span class="sxs-lookup"><span data-stu-id="0d6b7-123">Remarks</span></span>

<span data-ttu-id="0d6b7-p101">**GetChunk** から返されたバイト数は変数に代入されます。 **GetChunk** を使用して、データの値全体の一部を 1 つずつ取得します。分割された値を集めて元の値に戻すには、 **[AppendChunk](field-appendchunk-method-dao.md)** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="0d6b7-p101">The bytes returned by **GetChunk** are assigned to variable. Use **GetChunk** to return a portion of the total data value at a time. You can use the **[AppendChunk](field-appendchunk-method-dao.md)** method to reassemble the pieces.</span></span>

<span data-ttu-id="0d6b7-127">**オフセットが 0 の場合は、フィールドの最初のバイトからコピーが開始します。**</span><span class="sxs-lookup"><span data-stu-id="0d6b7-127">If offset is 0, **GetChunk** begins copying from the first byte of the field.</span></span>

<span data-ttu-id="0d6b7-128">Numbytes がフィールド内のバイト数より大きい場合、 **GetChunk**はフィールドに実際の残りのバイト数を返します。</span><span class="sxs-lookup"><span data-stu-id="0d6b7-128">If numbytes is greater than the number of bytes in the field, **GetChunk** returns the actual number of remaining bytes in the field.</span></span>


> [!NOTE]
> <P><span data-ttu-id="0d6b7-p102">[!メモ] 文字列の場合はメモ型 ( <STRONG>Memo</STRONG>) のフィールドを使用し、ロング バイナリ型 ( <STRONG>Long Binary</STRONG>) のフィールドにはバイナリ データのみ格納してください。この逆を行うと、予期しない結果を招きます。</span><span class="sxs-lookup"><span data-stu-id="0d6b7-p102">Use a <STRONG>Memo</STRONG> field for text, and put binary data only in <STRONG>Long Binary</STRONG> fields. Doing otherwise will cause undesirable results.</span></span></P>



## <a name="example"></a><span data-ttu-id="0d6b7-131">例</span><span class="sxs-lookup"><span data-stu-id="0d6b7-131">Example</span></span>

<span data-ttu-id="0d6b7-p103">次の使用例では、 **AppendChunk** メソッドと **GetChunk** メソッドを使用して、別のレコードからのデータを一度に 32K ずつ読み込んで OLE オブジェクトのフィールドに設定します。実際のアプリケーションでは、たとえば、社員レコード (社員の写真を含む) をあるテーブルから別のテーブルにコピーするときに、このようなプロシージャを使用します。この使用例では、単にレコードを同じテーブルにコピーしています。すべてのブロック操作は、1 つの AddNew-Update シーケンス内で行われています。</span><span class="sxs-lookup"><span data-stu-id="0d6b7-p103">This example uses the **AppendChunk** and **GetChunk** methods to fill an OLE object field with data from another record, 32K at a time. In a real application, one might use a procedure like this to copy an employee record (including the employee's photo) from one table to another. In this example, the record is simply being copied back to same table. Note that all the chunk manipulation takes place within a single AddNew-Update sequence.</span></span>

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