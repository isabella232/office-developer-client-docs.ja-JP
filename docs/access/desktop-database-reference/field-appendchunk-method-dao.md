---
title: Field.AppendChunk メソッド (DAO)
TOCTitle: AppendChunk Method
ms:assetid: f98c6862-fecf-06cb-a7c0-42b0d3150a06
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837014(v=office.15)
ms:contentKeyID: 48548819
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 257dd342d0c0aa171d7961ab61a69da099497688
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997407"
---
# <a name="fieldappendchunk-method-dao"></a><span data-ttu-id="0e781-102">Field.AppendChunk メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="0e781-102">Field.AppendChunk method (DAO)</span></span>

<span data-ttu-id="0e781-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="0e781-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0e781-104">文字列式から **[Recordset](field-object-dao.md)** のメモ型 (Memo) またはロング バイナリ型 (Long Binary) の **[Field](recordset-object-dao.md)** オブジェクトにデータを追加します。</span><span class="sxs-lookup"><span data-stu-id="0e781-104">Appends data from a string expression to a Memo or Long Binary **[Field](field-object-dao.md)** object in a **[Recordset](recordset-object-dao.md)**.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e781-105">構文</span><span class="sxs-lookup"><span data-stu-id="0e781-105">Syntax</span></span>

<span data-ttu-id="0e781-106">*式*です。AppendChunk (***Val***)</span><span class="sxs-lookup"><span data-stu-id="0e781-106">*expression* .AppendChunk(***Val***)</span></span>

<span data-ttu-id="0e781-107">\*式\***Field**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="0e781-107">*expression* A variable that represents a **Field** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="0e781-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0e781-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0e781-109">名前</span><span class="sxs-lookup"><span data-stu-id="0e781-109">Name</span></span></p></th>
<th><p><span data-ttu-id="0e781-110">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="0e781-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="0e781-111">データ型</span><span class="sxs-lookup"><span data-stu-id="0e781-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="0e781-112">説明</span><span class="sxs-lookup"><span data-stu-id="0e781-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0e781-113"><em>Val</em></span><span class="sxs-lookup"><span data-stu-id="0e781-113"><em>Val</em></span></span></p></td>
<td><p><span data-ttu-id="0e781-114">必須</span><span class="sxs-lookup"><span data-stu-id="0e781-114">Required</span></span></p></td>
<td><p><span data-ttu-id="0e781-115"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="0e781-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="0e781-116"><strong>Field</strong> オブジェクトに追加するバリアント型 (Variant) (文字列型 (String) サブタイプ) の式または変数です。</span><span class="sxs-lookup"><span data-stu-id="0e781-116">A Variant (String subtype) expression or variable containing the data you want to append to the <strong>Field</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="0e781-117">注釈</span><span class="sxs-lookup"><span data-stu-id="0e781-117">Remarks</span></span>

<span data-ttu-id="0e781-118">**AppendChunk** メソッドと **[GetChunk](field-getchunk-method-dao.md)** メソッドを使用して、Memo フィールドまたは Long Binary フィールドのデータのサブセットにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="0e781-118">You can use the **AppendChunk** and **[GetChunk](field-getchunk-method-dao.md)** methods to access subsets of data in a Memo or Long Binary field.</span></span>

<span data-ttu-id="0e781-p101">この 2 つのメソッドを使用すると、Memo フィールドと Long Binary フィールドを操作する際に文字列のスペースを確保できます。コピーなどの操作では、一時的な文字列を使用します。文字列のスペースが限られている場合、フィールド全体ではなく一部の操作が必要な場合もあります。</span><span class="sxs-lookup"><span data-stu-id="0e781-p101">You can also use these methods to conserve string space when you work with Memo and Long Binary fields. Certain operations (copying, for example) involve temporary strings. If string space is limited, you may need to work with chunks of a field instead of the entire field.</span></span>

<span data-ttu-id="0e781-122">カレント レコードがない場合に **AppendChunk** を使用すると、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="0e781-122">If there is no current record when you use **AppendChunk**, an error occurs.</span></span>

> [!NOTE]
> <span data-ttu-id="0e781-p102">[**Edit**](recordset-edit-method-dao.md) メソッドまたは [**AddNew**](recordset-addnew-method-dao.md) メソッドの呼び出し後の **AppendChunk** の最初の操作では、既存のデータを上書きしてフィールドにデータを配置するだけです。同じ **Edit** または **AddNew** のセッションのその後の **AppendChunk** の呼び出しでは、既存のデータに追加されます。</span><span class="sxs-lookup"><span data-stu-id="0e781-p102">The initial **AppendChunk** operation (after an **[Edit](recordset-edit-method-dao.md)** or **[AddNew](recordset-addnew-method-dao.md)** call) will simply place the data in the field, overwriting any existing data. Subsequent **AppendChunk** calls within the same **Edit** or **AddNew** session will then add to the existing data.</span></span>

## <a name="example"></a><span data-ttu-id="0e781-125">例</span><span class="sxs-lookup"><span data-stu-id="0e781-125">Example</span></span>

<span data-ttu-id="0e781-p103">次の使用例では、 **AppendChunk** メソッドと **GetChunk** メソッドを使用して、別のレコードからのデータを一度に 32K ずつ読み込んで OLE オブジェクトのフィールドに設定します。実際のアプリケーションでは、たとえば、社員レコード (社員の写真を含む) をあるテーブルから別のテーブルにコピーするときに、このようなプロシージャを使用します。この使用例では、単にレコードを同じテーブルにコピーしています。すべてのブロック操作は、1 つの AddNew-Update シーケンス内で行われています。</span><span class="sxs-lookup"><span data-stu-id="0e781-p103">This example uses the **AppendChunk** and **GetChunk** methods to fill an OLE object field with data from another record, 32K at a time. In a real application, one might use a procedure like this to copy an employee record (including the employee's photo) from one table to another. In this example, the record is simply being copied back to same table. Note that all the chunk manipulation takes place within a single AddNew-Update sequence.</span></span>

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
