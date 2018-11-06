---
title: Recordset2.CancelUpdate メソッド (DAO)
TOCTitle: CancelUpdate Method
ms:assetid: f741dec1-b9a4-506e-74ec-2bc309b0918e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836907(v=office.15)
ms:contentKeyID: 48548761
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e9679a39a8509bb73e9d788e776e208f3c899d3c
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998407"
---
# <a name="recordset2cancelupdate-method-dao"></a><span data-ttu-id="664fd-102">Recordset2.CancelUpdate メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="664fd-102">Recordset2.CancelUpdate method (DAO)</span></span>

<span data-ttu-id="664fd-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="664fd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="664fd-104">**[Recordset](recordset-object-dao.md)** オブジェクトで保留中のすべての更新を取り消します。</span><span class="sxs-lookup"><span data-stu-id="664fd-104">Cancels any pending updates for a **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="664fd-105">構文</span><span class="sxs-lookup"><span data-stu-id="664fd-105">Syntax</span></span>

<span data-ttu-id="664fd-106">*式*です。CancelUpdate (***UpdateType***)</span><span class="sxs-lookup"><span data-stu-id="664fd-106">*expression* .CancelUpdate(***UpdateType***)</span></span>

<span data-ttu-id="664fd-107">\*式\***Recordset2**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="664fd-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="664fd-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="664fd-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="664fd-109">名前</span><span class="sxs-lookup"><span data-stu-id="664fd-109">Name</span></span></p></th>
<th><p><span data-ttu-id="664fd-110">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="664fd-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="664fd-111">データ型</span><span class="sxs-lookup"><span data-stu-id="664fd-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="664fd-112">説明</span><span class="sxs-lookup"><span data-stu-id="664fd-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="664fd-113"><em>UpdateType</em></span><span class="sxs-lookup"><span data-stu-id="664fd-113"><em>UpdateType</em></span></span></p></td>
<td><p><span data-ttu-id="664fd-114">省略可能</span><span class="sxs-lookup"><span data-stu-id="664fd-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="664fd-115"><strong>長整数型 (Long)</strong></span><span class="sxs-lookup"><span data-stu-id="664fd-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="664fd-116"><strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong>値のいずれかに設定します。</span><span class="sxs-lookup"><span data-stu-id="664fd-116">Set to one of the <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> values.</span></span></p><p><span data-ttu-id="664fd-117"><strong>注</strong>: <EM>dbUpdateRegular</EM>および<EM>dbUpdateBatch</EM>値は、バッチ更新が有効になっている場合にのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="664fd-117"><strong>NOTE</strong>: The <EM>dbUpdateRegular</EM> and <EM>dbUpdateBatch</EM> values are valid only if batch updating is enabled.</span></span></p>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="664fd-118">注釈</span><span class="sxs-lookup"><span data-stu-id="664fd-118">Remarks</span></span>

<span data-ttu-id="664fd-p101">**CancelUpdate** メソッドを使用すると、 **[Edit](recordset2-edit-method-dao.md)** メソッドまたは **[AddNew](recordset2-addnew-method-dao.md)** メソッドの操作によるすべての保留中の更新を取り消すことができます。たとえば、ユーザーが **Edit** メソッドまたは **AddNew** メソッドを呼び出し、 **Update** メソッドを呼び出していない場合に **CancelUpdate** を使用すると、 **Edit** メソッドまたは **AddNew** メソッドを呼び出してから行われたすべての変更を取り消すことができます。</span><span class="sxs-lookup"><span data-stu-id="664fd-p101">You can use the **CancelUpdate** method to cancel any pending updates resulting from an **[Edit](recordset2-edit-method-dao.md)** or **[AddNew](recordset2-addnew-method-dao.md)** operation. For example, if a user invokes the **Edit** or **AddNew** method and hasn't yet invoked the **Update** method, **CancelUpdate** cancels any changes made after **Edit** or **AddNew** was invoked.</span></span>

<span data-ttu-id="664fd-121">[Recordset](recordset2-editmode-property-dao.md) の \*\*\*\*EditMode\*\*\*\* プロパティを確認して、取り消すことができる保留中の操作があるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="664fd-121">Check the **[EditMode](recordset2-editmode-property-dao.md)** property of the **Recordset** to determine if there is a pending operation that can be canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="664fd-122">[!メモ] **CancelUpdate** メソッドを使用することは、カレント レコードが変更されないこと、 **[BOF](recordset2-update-method-dao.md)** 、 **[EOF](recordset2-bof-property-dao.md)** などの各種のプロパティが更新されないことを除いて、 **[Update](recordset2-eof-property-dao.md)** メソッドを使用せずに別のレコードに移動することと同じです。</span><span class="sxs-lookup"><span data-stu-id="664fd-122">Using the **CancelUpdate** method has the same effect as moving to another record without using the **[Update](recordset2-update-method-dao.md)** method, except that the current record doesn't change, and various properties, such as **[BOF](recordset2-bof-property-dao.md)** and **[EOF](recordset2-eof-property-dao.md)**, aren't updated.</span></span>

## <a name="example"></a><span data-ttu-id="664fd-123">例</span><span class="sxs-lookup"><span data-stu-id="664fd-123">Example</span></span>

<span data-ttu-id="664fd-124">この例では、 **CancelUpdate** メソッドを **AddNew** メソッドと共に使用する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="664fd-124">This example shows how the **CancelUpdate** method is used with the **AddNew** method.</span></span>

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

<span data-ttu-id="664fd-125">この例では、 **CancelUpdate** メソッドを **Edit** メソッドと共に使用する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="664fd-125">This example shows how the **CancelUpdate** method is used with the **Edit** method.</span></span>

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

