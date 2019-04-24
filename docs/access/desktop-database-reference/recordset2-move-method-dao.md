---
title: Move メソッド (DAO)
TOCTitle: Move Method
ms:assetid: df39c05e-c5f8-3b66-fa5f-c91b687c147d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835635(v=office.15)
ms:contentKeyID: 48548211
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d57e73c52ca515f13d613ed3aeb9cf361054396e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307267"
---
# <a name="recordset2move-method-dao"></a><span data-ttu-id="8d754-102">Move メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="8d754-102">Recordset2.Move method (DAO)</span></span>

<span data-ttu-id="8d754-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="8d754-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8d754-104">**[Recordset](recordset-object-dao.md)** オブジェクトのカレント レコードの位置を移動します。</span><span class="sxs-lookup"><span data-stu-id="8d754-104">Moves the position of the current record in a **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d754-105">構文</span><span class="sxs-lookup"><span data-stu-id="8d754-105">Syntax</span></span>

<span data-ttu-id="8d754-106">*式*。Move (***Rows***、 ***startbookmark***)</span><span class="sxs-lookup"><span data-stu-id="8d754-106">*expression* .Move(***Rows***, ***StartBookmark***)</span></span>

<span data-ttu-id="8d754-107">\*式\***Recordset2**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="8d754-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="8d754-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8d754-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8d754-109">名前</span><span class="sxs-lookup"><span data-stu-id="8d754-109">Name</span></span></p></th>
<th><p><span data-ttu-id="8d754-110">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="8d754-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="8d754-111">データ型</span><span class="sxs-lookup"><span data-stu-id="8d754-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="8d754-112">説明</span><span class="sxs-lookup"><span data-stu-id="8d754-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8d754-113"><em>Rows</em></span><span class="sxs-lookup"><span data-stu-id="8d754-113"><em>Rows</em></span></span></p></td>
<td><p><span data-ttu-id="8d754-114">必須</span><span class="sxs-lookup"><span data-stu-id="8d754-114">Required</span></span></p></td>
<td><p><span data-ttu-id="8d754-115"><strong>長整数型 (Long)</strong></span><span class="sxs-lookup"><span data-stu-id="8d754-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="8d754-p101">位置を移動する行数。rows が 0 より大きい場合は、前方 (ファイルの末尾) に向かって位置が移動します。rows が 0 より小さい場合は、後方 (ファイルの先頭) に向かって位置が移動します。</span><span class="sxs-lookup"><span data-stu-id="8d754-p101">The number of rows the position will move. If rows is greater than 0, the position is moved forward (toward the end of the file). If rows is less than 0, the position is moved backward (toward the beginning of the file).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d754-119"><em>StartBookmark</em></span><span class="sxs-lookup"><span data-stu-id="8d754-119"><em>StartBookmark</em></span></span></p></td>
<td><p><span data-ttu-id="8d754-120">Optional</span><span class="sxs-lookup"><span data-stu-id="8d754-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="8d754-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="8d754-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="8d754-p102">ブックマークを示す値。startbookmark を指定した場合、このブックマークが移動の開始位置となります。それ以外の場合は、カレント レコードが移動の開始位置となります。</span><span class="sxs-lookup"><span data-stu-id="8d754-p102">A value identifying a bookmark. If you specify startbookmark, the move begins relative to this bookmark. Otherwise, Move begins from the current record.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="8d754-125">注釈</span><span class="sxs-lookup"><span data-stu-id="8d754-125">Remarks</span></span>

<span data-ttu-id="8d754-p103">**Move** を使用して、カレント レコードを参照するポインターを最初のレコードよりも前に設定すると、カレント レコードを参照するポインターはファイルの先頭に移動します。 **Recordset** にレコードが含まれておらず、 **[BOF](recordset2-bof-property-dao.md)** プロパティが **True** の場合は、このメソッドを使用して後方に移動しようとするとエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="8d754-p103">If you use **Move** to position the current record pointer before the first record, the current record pointer moves to the beginning of the file. If the **Recordset** contains no records and its **[BOF](recordset2-bof-property-dao.md)** property is **True**, using this method to move backward causes an error.</span></span>

<span data-ttu-id="8d754-p104">**Move** を使用して、カレント レコードを参照するポインターを最後のレコードよりも後ろに設定すると、カレント レコードを参照するポインターはファイルの末尾に移動します。 **Recordset** にレコードが含まれておらず、 **[EOF](recordset2-eof-property-dao.md)** プロパティが **True** の場合は、このメソッドを使用して前方に移動しようとするとエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="8d754-p104">If you use **Move** to position the current record pointer after the last record, the current record pointer position moves to the end of the file. If the **Recordset** contains no records and its **[EOF](recordset2-eof-property-dao.md)** property is **True**, then using this method to move forward causes an error.</span></span>

<span data-ttu-id="8d754-130">**BOF** プロパティまたは **EOF** プロパティが **True** の場合に、有効なブックマークを指定せずに **Move** メソッドを使用しようとすると、実行時エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="8d754-130">If either the **BOF** or **EOF** property is **True** and you attempt to use the **Move** method without a valid bookmark, a run-time error occurs.</span></span>

> [!NOTE]
> - <span data-ttu-id="8d754-p105">前方スクロール タイプの **Recordset** オブジェクトで **Move** を使用するときは、引数 rows に正の整数を指定する必要があり、ブックマークは指定できません。つまり、移動できる方向は前方のみです。</span><span class="sxs-lookup"><span data-stu-id="8d754-p105">When you use **Move** on a forward-only-type **Recordset** object, the rows argument must be a positive integer and bookmarks aren't allowed. This means you can only move forward.</span></span>
> - <span data-ttu-id="8d754-133">**Recordset** の最初のレコード、最後のレコード、次のレコード、または前のレコードをカレント レコードにするには、 **MoveFirst**、 **MoveLast**、 **MoveNext**、または **MovePrevious** の各メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="8d754-133">To make the first, last, next, or previous record in a **Recordset** the current record, use either the **MoveFirst**, **MoveLast**, **MoveNext**, or **MovePrevious** method.</span></span>
> - <span data-ttu-id="8d754-p106">rows に 0 を指定して **Move** を使用すると、カレント レコードの基になるデータを簡単に取得できます。この方法は、カレント レコードにベース テーブルの最新のデータが格納されていることを確認するときに便利です。またこの方法を使用すると、 **[Edit](recordset2-edit-method-dao.md)** または **[AddNew](recordset-addnew-method-dao.md)** に対する保留中の呼び出しが取り消されます。</span><span class="sxs-lookup"><span data-stu-id="8d754-p106">Using **Move** with rows equal to 0 is an easy way to retrieve the underlying data for the current record. This is useful if you want to make sure that the current record has the most recent data from the base tables. It will also cancel any pending **[Edit](recordset2-edit-method-dao.md)** or **[AddNew](recordset-addnew-method-dao.md)** calls.</span></span>


## <a name="example"></a><span data-ttu-id="8d754-137">例</span><span class="sxs-lookup"><span data-stu-id="8d754-137">Example</span></span>

<span data-ttu-id="8d754-138">この例では、**Move** メソッドを使用して、ユーザーの入力に基づいてレコード ポインターを配置します。</span><span class="sxs-lookup"><span data-stu-id="8d754-138">This example uses the **Move** method to position the record pointer based on user input.</span></span>

```vb
    Sub MoveX() 
     
       Dim dbsNorthwind As Database 
       Dim rstSuppliers As Recordset2 
       Dim varBookmark As Variant 
       Dim strCommand As String 
       Dim lngMove As Long 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set rstSuppliers = _ 
          dbsNorthwind.OpenRecordset("SELECT CompanyName, " & _ 
          "City, Country FROM Suppliers ORDER BY CompanyName", _ 
          dbOpenDynaset) 
     
       With rstSuppliers 
          ' Populate recordset. 
          .MoveLast 
          .MoveFirst 
     
          Do While True 
             ' Display information about current record and ask  
             ' how many records to move. 
             strCommand = InputBox( _ 
                "Record " & (.AbsolutePosition + 1) & " of " & _ 
                .RecordCount & vbCr & "Company: " & _ 
                !CompanyName & vbCr & "Location: " & !City & _ 
                ", " & !Country & vbCr & vbCr & _ 
                "Enter number of records to Move " & _ 
                "(positive or negative).") 
     
             If strCommand = "" Then Exit Do 
     
             ' Store bookmark in case the Move doesn't work. 
             varBookmark = .Bookmark 
     
             ' Move method requires parameter of data type Long. 
             lngMove = CLng(strCommand) 
             .Move lngMove 
     
             ' Trap for BOF or EOF. 
             If .BOF Then 
                MsgBox "Too far backward! " & _ 
                   "Returning to current record." 
                .Bookmark = varBookmark 
             End If 
             If .EOF Then 
                MsgBox "Too far forward! " & _ 
                   "Returning to current record." 
                .Bookmark = varBookmark 
             End If 
          Loop 
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub
```
