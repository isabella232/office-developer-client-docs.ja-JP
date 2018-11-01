---
title: Recordset.Move メソッド (DAO)
TOCTitle: Move Method
ms:assetid: 21ca5ab5-ff71-1ae8-21b3-8991d5f795cf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191697(v=office.15)
ms:contentKeyID: 48543689
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052941
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 2caa468f189e30373e2818b090688ca6f239258d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870591"
---
# <a name="recordsetmove-method-dao"></a><span data-ttu-id="65da3-102">Recordset.Move メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="65da3-102">Recordset.Move Method (DAO)</span></span>


<span data-ttu-id="65da3-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="65da3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="65da3-104">**[Recordset](recordset-object-dao.md)** オブジェクトでカレント レコードの位置を移動します。</span><span class="sxs-lookup"><span data-stu-id="65da3-104">Moves the position of the current record in a **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="65da3-105">構文</span><span class="sxs-lookup"><span data-stu-id="65da3-105">Syntax</span></span>

<span data-ttu-id="65da3-106">*式*です。移動 (***行***、 ***StartBookmark***)</span><span class="sxs-lookup"><span data-stu-id="65da3-106">*expression* .Move(***Rows***, ***StartBookmark***)</span></span>

<span data-ttu-id="65da3-107">\*式\***レコード セット**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="65da3-107">*expression* A variable that represents a **Recordset** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="65da3-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="65da3-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="65da3-109">名前</span><span class="sxs-lookup"><span data-stu-id="65da3-109">Name</span></span></p></th>
<th><p><span data-ttu-id="65da3-110">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="65da3-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="65da3-111">データ型</span><span class="sxs-lookup"><span data-stu-id="65da3-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="65da3-112">説明</span><span class="sxs-lookup"><span data-stu-id="65da3-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="65da3-113">行</span><span class="sxs-lookup"><span data-stu-id="65da3-113">Rows</span></span></p></td>
<td><p><span data-ttu-id="65da3-114">必須</span><span class="sxs-lookup"><span data-stu-id="65da3-114">Required</span></span></p></td>
<td><p><span data-ttu-id="65da3-115"><strong>長整数型 (Long)</strong></span><span class="sxs-lookup"><span data-stu-id="65da3-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="65da3-p101">位置を移動する行数。rows が 0 より大きい場合は、前方 (ファイルの末尾) に向かって位置が移動します。rows が 0 より小さい場合は、後方 (ファイルの先頭) に向かって位置が移動します。</span><span class="sxs-lookup"><span data-stu-id="65da3-p101">The number of rows the position will move. If rows is greater than 0, the position is moved forward (toward the end of the file). If rows is less than 0, the position is moved backward (toward the beginning of the file).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65da3-119">StartBookmark</span><span class="sxs-lookup"><span data-stu-id="65da3-119">StartBookmark</span></span></p></td>
<td><p><span data-ttu-id="65da3-120">省略可能</span><span class="sxs-lookup"><span data-stu-id="65da3-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="65da3-121"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="65da3-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="65da3-p102">ブックマークを示す値。startbookmark を指定した場合、このブックマークが移動の開始位置となります。それ以外の場合は、カレント レコードが移動の開始位置となります。</span><span class="sxs-lookup"><span data-stu-id="65da3-p102">A value identifying a bookmark. If you specify startbookmark, the move begins relative to this bookmark. Otherwise, Move begins from the current record.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="65da3-125">注釈</span><span class="sxs-lookup"><span data-stu-id="65da3-125">Remarks</span></span>

<span data-ttu-id="65da3-p103">**Move** を使用して、カレント レコード ポインターの位置を最初のレコードより前に移動しようとすると、カレント レコード ポインターはファイルの先頭に移動します。 **Recordset** 内にレコードがなく、かつ **[BOF](recordset-bof-property-dao.md)** プロパティが **True** の場合、このメソッドを使用して後方に向かって移動すると、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="65da3-p103">If you use **Move** to position the current record pointer before the first record, the current record pointer moves to the beginning of the file. If the **Recordset** contains no records and its **[BOF](recordset-bof-property-dao.md)** property is **True**, using this method to move backward causes an error.</span></span>

<span data-ttu-id="65da3-p104">**Move** を使用して、カレント レコード ポインターの位置を最後のレコードよりも後に移動しようとすると、カレント レコード ポインターはファイルの末尾に移動します。 **Recordset** 内にレコードがなく、かつ **[EOF](recordset-eof-property-dao.md)** プロパティが **True** の場合、このメソッドを使用して前方に向かって移動しようとすると、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="65da3-p104">If you use **Move** to position the current record pointer after the last record, the current record pointer position moves to the end of the file. If the **Recordset** contains no records and its **[EOF](recordset-eof-property-dao.md)** property is **True**, then using this method to move forward causes an error.</span></span>

<span data-ttu-id="65da3-130">**BOF** プロパティまたは **EOF** プロパティが **True** の場合に、有効なブックマークを指定せずに **Move** メソッドを使用しようとすると、実行時エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="65da3-130">If either the **BOF** or **EOF** property is **True** and you attempt to use the **Move** method without a valid bookmark, a run-time error occurs.</span></span>


> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="65da3-p105">前方スクロール タイプの <STRONG>Recordset</STRONG> オブジェクトで <STRONG>Move</STRONG> を使用するときは、引数 rows に正の整数を指定する必要があり、ブックマークは指定できません。つまり、移動できる方向は前方のみです。</span><span class="sxs-lookup"><span data-stu-id="65da3-p105">When you use <STRONG>Move</STRONG> on a forward-only-type <STRONG>Recordset</STRONG> object, the rows argument must be a positive integer and bookmarks aren't allowed. This means you can only move forward.</span></span></P>
> <LI>
> <P><span data-ttu-id="65da3-133"><STRONG>Recordset</STRONG> の最初のレコード、最後のレコード、次のレコード、または前のレコードをカレント レコードにするには、 <STRONG>MoveFirst</STRONG>、 <STRONG>MoveLast</STRONG>、 <STRONG>MoveNext</STRONG>、または <STRONG>MovePrevious</STRONG> の各メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="65da3-133">To make the first, last, next, or previous record in a <STRONG>Recordset</STRONG> the current record, use either the <STRONG>MoveFirst</STRONG>, <STRONG>MoveLast</STRONG>, <STRONG>MoveNext</STRONG>, or <STRONG>MovePrevious</STRONG> method.</span></span></P>
> <LI>
> <P><span data-ttu-id="65da3-p106">rows に 0 を指定して <STRONG>Move</STRONG> を使用すると、カレント レコードの基になるデータを簡単に取得できます。この方法は、カレント レコードにベース テーブルの最新のデータが格納されていることを確認するときに便利です。またこの方法を使用すると、 <STRONG><A href="recordset2-edit-method-dao.md">Edit</A></STRONG> または <STRONG><A href="recordset-addnew-method-dao.md">AddNew</A></STRONG> に対する保留中の呼び出しが取り消されます。</span><span class="sxs-lookup"><span data-stu-id="65da3-p106">Using <STRONG>Move</STRONG> with rows equal to 0 is an easy way to retrieve the underlying data for the current record. This is useful if you want to make sure that the current record has the most recent data from the base tables. It will also cancel any pending <STRONG><A href="recordset2-edit-method-dao.md">Edit</A></STRONG> or <STRONG><A href="recordset-addnew-method-dao.md">AddNew</A></STRONG> calls.</span></span></P></LI></UL>



## <a name="example"></a><span data-ttu-id="65da3-137">例</span><span class="sxs-lookup"><span data-stu-id="65da3-137">Example</span></span>

<span data-ttu-id="65da3-138">この例では、 **Move** メソッドを使用して、ユーザーの入力に基づいてレコード ポインターを配置します。</span><span class="sxs-lookup"><span data-stu-id="65da3-138">This example uses the **Move** method to position the record pointer based on user input.</span></span>

```vb
    Sub MoveX() 
     
       Dim dbsNorthwind As Database 
       Dim rstSuppliers As Recordset 
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
