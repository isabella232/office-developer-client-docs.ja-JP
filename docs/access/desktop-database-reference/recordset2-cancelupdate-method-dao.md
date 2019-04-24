---
title: Recordset2 メソッド (DAO)
TOCTitle: CancelUpdate Method
ms:assetid: f741dec1-b9a4-506e-74ec-2bc309b0918e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836907(v=office.15)
ms:contentKeyID: 48548761
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 90378dc61d12485a290bbd7857d026a46cd9da96
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307400"
---
# <a name="recordset2cancelupdate-method-dao"></a><span data-ttu-id="15d44-102">Recordset2 メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="15d44-102">Recordset2.CancelUpdate method (DAO)</span></span>

<span data-ttu-id="15d44-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="15d44-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="15d44-104">**[Recordset](recordset-object-dao.md)** オブジェクトの保留中の更新をキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="15d44-104">Cancels any pending updates for a **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="15d44-105">構文</span><span class="sxs-lookup"><span data-stu-id="15d44-105">Syntax</span></span>

<span data-ttu-id="15d44-106">*式*。CancelUpdate (***updatetype***)</span><span class="sxs-lookup"><span data-stu-id="15d44-106">*expression* .CancelUpdate(***UpdateType***)</span></span>

<span data-ttu-id="15d44-107">\*式\***Recordset2**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="15d44-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="15d44-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="15d44-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="15d44-109">名前</span><span class="sxs-lookup"><span data-stu-id="15d44-109">Name</span></span></p></th>
<th><p><span data-ttu-id="15d44-110">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="15d44-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="15d44-111">データ型</span><span class="sxs-lookup"><span data-stu-id="15d44-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="15d44-112">説明</span><span class="sxs-lookup"><span data-stu-id="15d44-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="15d44-113"><em>updatetype</em></span><span class="sxs-lookup"><span data-stu-id="15d44-113"><em>UpdateType</em></span></span></p></td>
<td><p><span data-ttu-id="15d44-114">省略可能</span><span class="sxs-lookup"><span data-stu-id="15d44-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="15d44-115"><strong>長整数型 (Long)</strong></span><span class="sxs-lookup"><span data-stu-id="15d44-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="15d44-116"><strong><a href="updatetypeenum-enumeration-dao.md">updatetypeenum</a></strong>値の1つに設定します。</span><span class="sxs-lookup"><span data-stu-id="15d44-116">Set to one of the <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> values.</span></span></p><p><span data-ttu-id="15d44-117"><strong>注</strong>: <EM>dbUpdateRegular</EM>および<EM>dbUpdateBatch</EM>の値は、バッチ更新が有効になっている場合にのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="15d44-117"><strong>NOTE</strong>: The <EM>dbUpdateRegular</EM> and <EM>dbUpdateBatch</EM> values are valid only if batch updating is enabled.</span></span></p>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="15d44-118">注釈</span><span class="sxs-lookup"><span data-stu-id="15d44-118">Remarks</span></span>

<span data-ttu-id="15d44-p101">**CancelUpdate** メソッドを使用すると、 **[Edit](recordset2-edit-method-dao.md)** または **[AddNew](recordset2-addnew-method-dao.md)** のいずれかの操作によって生じた保留中の更新を取り消すこどができます。たとえば、 **Edit** メソッドまたは **AddNew** メソッドが呼び出されたが、 **Update** メソッドはまだ呼び出されていない場合、 **CancelUpdate** を使用すると、 **Edit** または **AddNew** の呼び出し後に加えられた変更が取り消されます。</span><span class="sxs-lookup"><span data-stu-id="15d44-p101">You can use the **CancelUpdate** method to cancel any pending updates resulting from an **[Edit](recordset2-edit-method-dao.md)** or **[AddNew](recordset2-addnew-method-dao.md)** operation. For example, if a user invokes the **Edit** or **AddNew** method and hasn't yet invoked the **Update** method, **CancelUpdate** cancels any changes made after **Edit** or **AddNew** was invoked.</span></span>

<span data-ttu-id="15d44-121">**Recordset**の**[EditMode](recordset2-editmode-property-dao.md)** プロパティを調べて、取り消すことができる保留中の操作があるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="15d44-121">Check the **[EditMode](recordset2-editmode-property-dao.md)** property of the **Recordset** to determine if there is a pending operation that can be canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="15d44-122">[!メモ] **CancelUpdate** メソッドを使用すると、 **[Update](recordset2-update-method-dao.md)** メソッドを使用せずに他のレコードへ移動するのと同じ効果が得られます。ただし、カレント レコードは変化せず、 **[BOF](recordset2-bof-property-dao.md)** プロパティや **[EOF](recordset2-eof-property-dao.md)** プロパティなどのさまざまなプロパティは更新されません。</span><span class="sxs-lookup"><span data-stu-id="15d44-122">Using the **CancelUpdate** method has the same effect as moving to another record without using the **[Update](recordset2-update-method-dao.md)** method, except that the current record doesn't change, and various properties, such as **[BOF](recordset2-bof-property-dao.md)** and **[EOF](recordset2-eof-property-dao.md)**, aren't updated.</span></span>

## <a name="example"></a><span data-ttu-id="15d44-123">例</span><span class="sxs-lookup"><span data-stu-id="15d44-123">Example</span></span>

<span data-ttu-id="15d44-124">次の例では、 **CancelUpdate** メソッドを **AddNew** メソッドと共に使用する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="15d44-124">This example shows how the **CancelUpdate** method is used with the **AddNew** method.</span></span>

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

<span data-ttu-id="15d44-125">次の例では、 **CancelUpdate** メソッドを **Edit** メソッドと共に使用する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="15d44-125">This example shows how the **CancelUpdate** method is used with the **Edit** method.</span></span>

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

