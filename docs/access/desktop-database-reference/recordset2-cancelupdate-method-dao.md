---
title: Recordset2.CancelUpdate メソッド (DAO)
TOCTitle: CancelUpdate Method
ms:assetid: f741dec1-b9a4-506e-74ec-2bc309b0918e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836907(v=office.15)
ms:contentKeyID: 48548761
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 13516830ddb9cb22e8e50872b51743ea5d54ab98
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921489"
---
# <a name="recordset2cancelupdate-method-dao"></a><span data-ttu-id="0d8e1-102">Recordset2.CancelUpdate メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="0d8e1-102">Recordset2.CancelUpdate method (DAO)</span></span>


<span data-ttu-id="0d8e1-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="0d8e1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0d8e1-104">**[Recordset](recordset-object-dao.md)** オブジェクトで保留中のすべての更新を取り消します。</span><span class="sxs-lookup"><span data-stu-id="0d8e1-104">Cancels any pending updates for a **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d8e1-105">構文</span><span class="sxs-lookup"><span data-stu-id="0d8e1-105">Syntax</span></span>

<span data-ttu-id="0d8e1-106">*式*です。CancelUpdate (***UpdateType***)</span><span class="sxs-lookup"><span data-stu-id="0d8e1-106">*expression* .CancelUpdate(***UpdateType***)</span></span>

<span data-ttu-id="0d8e1-107">\*式\***Recordset2**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="0d8e1-107">*expression* A variable that represents a **Recordset2** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="0d8e1-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0d8e1-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0d8e1-109">名前</span><span class="sxs-lookup"><span data-stu-id="0d8e1-109">Name</span></span></p></th>
<th><p><span data-ttu-id="0d8e1-110">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="0d8e1-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="0d8e1-111">データ型</span><span class="sxs-lookup"><span data-stu-id="0d8e1-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="0d8e1-112">説明</span><span class="sxs-lookup"><span data-stu-id="0d8e1-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0d8e1-113">UpdateType</span><span class="sxs-lookup"><span data-stu-id="0d8e1-113">UpdateType</span></span></p></td>
<td><p><span data-ttu-id="0d8e1-114">省略可能</span><span class="sxs-lookup"><span data-stu-id="0d8e1-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="0d8e1-115"><strong>長整数型 (Long)</strong></span><span class="sxs-lookup"><span data-stu-id="0d8e1-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="0d8e1-116"><strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong>値のいずれかに設定します。</span><span class="sxs-lookup"><span data-stu-id="0d8e1-116">Set to one of the <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> values.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="0d8e1-117"><EM>DbUpdateRegular</EM>および<EM>dbUpdateBatch</EM>値は、バッチ更新が有効になっている場合にのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="0d8e1-117">The <EM>dbUpdateRegular</EM> and <EM>dbUpdateBatch</EM> values are valid only if batch updating is enabled.</span></span></P>


</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="0d8e1-118">注釈</span><span class="sxs-lookup"><span data-stu-id="0d8e1-118">Remarks</span></span>

<span data-ttu-id="0d8e1-p101">**CancelUpdate** メソッドを使用すると、 **[Edit](recordset2-edit-method-dao.md)** メソッドまたは **[AddNew](recordset2-addnew-method-dao.md)** メソッドの操作によるすべての保留中の更新を取り消すことができます。たとえば、ユーザーが **Edit** メソッドまたは **AddNew** メソッドを呼び出し、 **Update** メソッドを呼び出していない場合に **CancelUpdate** を使用すると、 **Edit** メソッドまたは **AddNew** メソッドを呼び出してから行われたすべての変更を取り消すことができます。</span><span class="sxs-lookup"><span data-stu-id="0d8e1-p101">You can use the **CancelUpdate** method to cancel any pending updates resulting from an **[Edit](recordset2-edit-method-dao.md)** or **[AddNew](recordset2-addnew-method-dao.md)** operation. For example, if a user invokes the **Edit** or **AddNew** method and hasn't yet invoked the **Update** method, **CancelUpdate** cancels any changes made after **Edit** or **AddNew** was invoked.</span></span>

<span data-ttu-id="0d8e1-121">[Recordset](recordset2-editmode-property-dao.md) の \*\*\*\*EditMode\*\*\*\* プロパティを確認して、取り消すことができる保留中の操作があるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="0d8e1-121">Check the **[EditMode](recordset2-editmode-property-dao.md)** property of the **Recordset** to determine if there is a pending operation that can be canceled.</span></span>


> [!NOTE]
> <P><span data-ttu-id="0d8e1-122">[!メモ] <STRONG>CancelUpdate</STRONG> メソッドを使用することは、カレント レコードが変更されないこと、 <STRONG><A href="recordset2-update-method-dao.md">BOF</A></STRONG> 、 <STRONG><A href="recordset2-bof-property-dao.md">EOF</A></STRONG> などの各種のプロパティが更新されないことを除いて、 <STRONG><A href="recordset2-eof-property-dao.md">Update</A></STRONG> メソッドを使用せずに別のレコードに移動することと同じです。</span><span class="sxs-lookup"><span data-stu-id="0d8e1-122">Using the <STRONG>CancelUpdate</STRONG> method has the same effect as moving to another record without using the <STRONG><A href="recordset2-update-method-dao.md">Update</A></STRONG> method, except that the current record doesn't change, and various properties, such as <STRONG><A href="recordset2-bof-property-dao.md">BOF</A></STRONG> and <STRONG><A href="recordset2-eof-property-dao.md">EOF</A></STRONG>, aren't updated.</span></span></P>



## <a name="example"></a><span data-ttu-id="0d8e1-123">例</span><span class="sxs-lookup"><span data-stu-id="0d8e1-123">Example</span></span>

<span data-ttu-id="0d8e1-124">この例では、 **CancelUpdate** メソッドを **AddNew** メソッドと共に使用する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="0d8e1-124">This example shows how the **CancelUpdate** method is used with the **AddNew** method.</span></span>

```vb
    Sub CancelUpdateX() 
     
       Dim dbsNorthwind As Database 
       Dim rstEmployees As Recordset2 
       Dim intCommand As Integer 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set rstEmployees = dbsNorthwind.OpenRecordset( _ 
          "Employees", dbOpenDynaset) 
     
       With rstEmployees 
          .AddNew 
          !FirstName = "Kimberly" 
          !LastName = "Bowen" 
          intCommand = MsgBox("Add new record for " & _ 
             !FirstName & " " & !LastName & "?", vbYesNo) 
          If intCommand = vbYes Then 
             .Update 
             MsgBox "Record added." 
             ' Delete new record because this is a  
             ' demonstration. 
             .Bookmark = .LastModified 
             .Delete 
          Else 
             .CancelUpdate 
             MsgBox "Record not added." 
          End If 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="0d8e1-125">この例では、 **CancelUpdate** メソッドを **Edit** メソッドと共に使用する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="0d8e1-125">This example shows how the **CancelUpdate** method is used with the **Edit** method.</span></span>

```vb
Sub CancelUpdateX2() 
 
   Dim dbsNorthwind As Database 
   Dim rstEmployees As Recordset 
   Dim strFirst As String 
   Dim strLast As String 
   Dim intCommand As Integer 
 
   Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
   Set rstEmployees = dbsNorthwind.OpenRecordset( _ 
      "Employees", dbOpenDynaset) 
 
   With rstEmployees 
      strFirst = !FirstName 
      strLast = !LastName 
      .Edit 
      !FirstName = "Cora" 
      !LastName = "Edmonds" 
      intCommand = MsgBox("Replace current name with " & _ 
         !FirstName & " " & !LastName & "?", vbYesNo) 
      If intCommand = vbYes Then 
         .Update 
         MsgBox "Record modified." 
         ' Restore data because this is a demonstration. 
         .Bookmark = .LastModified 
         .Edit 
         !FirstName = strFirst 
         !LastName = strLast 
         .Update 
      Else 
         .CancelUpdate 
         MsgBox "Record not modified." 
      End If 
      .Close 
   End With 
 
   dbsNorthwind.Close 
 
End Sub 
 
```

