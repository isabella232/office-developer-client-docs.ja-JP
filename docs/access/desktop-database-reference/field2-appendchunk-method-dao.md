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
ms.openlocfilehash: 2c21ea4943531f7b4ae32d49a2cb223802c68fb0
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867385"
---
# <a name="field2appendchunk-method-dao"></a><span data-ttu-id="93adb-102">Field2.AppendChunk メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="93adb-102">Field2.AppendChunk Method (DAO)</span></span>


<span data-ttu-id="93adb-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="93adb-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="93adb-104">文字列式からのデータを [**Recordset**](recordset-object-dao.md) の、メモ型 (Memo) またはロング バイナリ型 (Long Binary) の **Field2** オブジェクトに追加します。</span><span class="sxs-lookup"><span data-stu-id="93adb-104">Appends data from a string expression to a Memo or Long Binary **Field2** object in a **[Recordset](recordset-object-dao.md)**.</span></span>

## <a name="syntax"></a><span data-ttu-id="93adb-105">構文</span><span class="sxs-lookup"><span data-stu-id="93adb-105">Syntax</span></span>

<span data-ttu-id="93adb-106">*式*です。AppendChunk (***Val***)</span><span class="sxs-lookup"><span data-stu-id="93adb-106">*expression* .AppendChunk(***Val***)</span></span>

<span data-ttu-id="93adb-107">\*式\***Field2**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="93adb-107">*expression* A variable that represents a **Field2** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="93adb-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="93adb-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="93adb-109">名前</span><span class="sxs-lookup"><span data-stu-id="93adb-109">Name</span></span></p></th>
<th><p><span data-ttu-id="93adb-110">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="93adb-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="93adb-111">データ型</span><span class="sxs-lookup"><span data-stu-id="93adb-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="93adb-112">説明</span><span class="sxs-lookup"><span data-stu-id="93adb-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="93adb-113">Val</span><span class="sxs-lookup"><span data-stu-id="93adb-113">Val</span></span></p></td>
<td><p><span data-ttu-id="93adb-114">必須</span><span class="sxs-lookup"><span data-stu-id="93adb-114">Required</span></span></p></td>
<td><p><span data-ttu-id="93adb-115"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="93adb-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="93adb-116"><strong>Field2</strong> オブジェクトに追加するデータが格納されている、サブタイプが文字列型 (String) であるバリアント型 (Variant) の式。</span><span class="sxs-lookup"><span data-stu-id="93adb-116">A Variant (String subtype) expression or variable containing the data you want to append to the <strong>Field2</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="93adb-117">注釈</span><span class="sxs-lookup"><span data-stu-id="93adb-117">Remarks</span></span>

<span data-ttu-id="93adb-118">**AppendChunk** メソッドおよび **GetChunk** メソッドを使用して、メモ型 (Memo) またはロング バイナリ型 (Long Binary) のフィールド内のデータのサブセットにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="93adb-118">You can use the **AppendChunk** and **GetChunk** methods to access subsets of data in a Memo or Long Binary field.</span></span>

<span data-ttu-id="93adb-p101">メモ型 (Memo) またはロング バイナリ型 (Long Binary) のフィールドを操作するときに、これらのメソッドを使用して、文字列領域を確保することもできます。コピーなどの一部の操作では、一時的な文字列が使用されます。文字列領域が制限されている場合は、フィールド全体ではなく、1 つのフィールドをいくつかのブロックに分けて操作する必要があることがあります。</span><span class="sxs-lookup"><span data-stu-id="93adb-p101">You can also use these methods to conserve string space when you work with Memo and Long Binary fields. Certain operations (copying, for example) involve temporary strings. If string space is limited, you may need to work with chunks of a field instead of the entire field.</span></span>

<span data-ttu-id="93adb-122">カレント レコードがない場合に **AppendChunk** を使用すると、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="93adb-122">If there is no current record when you use **AppendChunk**, an error occurs.</span></span>


> [!NOTE]
> <P><span data-ttu-id="93adb-p102"><A href="recordset-edit-method-dao.md"><STRONG>Edit</STRONG></A> メソッドまたは <A href="recordset-addnew-method-dao.md"><STRONG>AddNew</STRONG></A> メソッドの呼び出し後の <STRONG>AppendChunk</STRONG> の最初の操作では、既存のデータを上書きしてフィールドにデータを配置するだけです。同じ <STRONG>Edit</STRONG> または <STRONG>AddNew</STRONG> のセッションのその後の <STRONG>AppendChunk</STRONG> の呼び出しでは、既存のデータに追加されます。</span><span class="sxs-lookup"><span data-stu-id="93adb-p102">The initial <STRONG>AppendChunk</STRONG> operation (after an <STRONG><A href="recordset-edit-method-dao.md">Edit</A></STRONG> or <STRONG><A href="recordset-addnew-method-dao.md">AddNew</A></STRONG> call) will simply place the data in the field, overwriting any existing data. Subsequent <STRONG>AppendChunk</STRONG> calls within the same <STRONG>Edit</STRONG> or <STRONG>AddNew</STRONG> session will then add to the existing data.</span></span></P>



## <a name="example"></a><span data-ttu-id="93adb-125">例</span><span class="sxs-lookup"><span data-stu-id="93adb-125">Example</span></span>

<span data-ttu-id="93adb-p103">次の使用例では、 **AppendChunk** メソッドと **GetChunk** メソッドを使用して、別のレコードからのデータを一度に 32K ずつ読み込んで OLE オブジェクトのフィールドに設定します。実際のアプリケーションでは、たとえば、社員レコード (社員の写真を含む) をあるテーブルから別のテーブルにコピーするときに、このようなプロシージャを使用します。この使用例では、単にレコードを同じテーブルにコピーしています。すべてのブロック操作は、1 つの AddNew-Update シーケンス内で行われています。</span><span class="sxs-lookup"><span data-stu-id="93adb-p103">This example uses the **AppendChunk** and **GetChunk** methods to fill an OLE object field with data from another record, 32K at a time. In a real application, one might use a procedure like this to copy an employee record (including the employee's photo) from one table to another. In this example, the record is simply being copied back to same table. Note that all the chunk manipulation takes place within a single AddNew-Update sequence.</span></span>

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
