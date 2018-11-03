---
title: '第 3 章: データを調べること。'
TOCTitle: 'Chapter 3: Examining data'
ms:assetid: 73c69134-3127-3344-d5c3-5ecb9e0e958b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249474(v=office.15)
ms:contentKeyID: 48545648
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4b489400536675fccced8f87aae515b019b87123
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936862"
---
# <a name="chapter-3-examining-data"></a><span data-ttu-id="b72bb-102">第 3 章: データを調べること。</span><span class="sxs-lookup"><span data-stu-id="b72bb-102">Chapter 3: Examining data</span></span>

<span data-ttu-id="b72bb-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="b72bb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b72bb-p101">2 章では、データ ソースのデータを **Recordset** オブジェクトとして取得する方法について説明しました。この章では、 **Recordset** 間を移動してそのデータを表示する方法を含め、 **Recordset** の詳細について説明します。</span><span class="sxs-lookup"><span data-stu-id="b72bb-p101">Chapter 2 explained how to retrieve data from a data source as a **Recordset** object. This chapter will discuss the **Recordset** in more detail, including how to navigate through the **Recordset** and view its data.</span></span>

<span data-ttu-id="b72bb-p102">**Recordsets** には、簡単にレコードセット間を移動しその内容を調べられるように設計されたメソッドとプロパティがあります。プロバイダーがサポートする機能によっては、一部の **Recordset** のメソッドまたはプロパティを使用できない場合があります。 **Recordset** オブジェクトの機能をさらに調べるために、次のコードを使用して、Microsoft SQL Server 2000 上の Northwind サンプル データベースから取得した **Recordset** について考えてみましょう。</span><span class="sxs-lookup"><span data-stu-id="b72bb-p102">**Recordsets** have methods and properties designed to make it easy to move through them and examine their contents. Depending on the functionality supported by the provider, some **Recordset** methods or properties might not be available. To continue exploring the **Recordset** object, consider a **Recordset** that would be returned from the Northwind sample database on Microsoft SQL Server 2000, using the following code:</span></span>

```vb 
 
'BeginRsTour 
Public Sub RecordsetTour() 
 On Error GoTo ErrHandler: 
 
 Dim objRs As New ADODB.Recordset 
 Dim strSQL As String 
 
 strSQL = "SELECT ProductID, ProductName, UnitPrice FROM Products " & _ 
 "WHERE CategoryID = 7" '7 = Produce 
 
 objRs.Open strSQL, strConnStr, adOpenForwardOnly, _ 
 adLockReadOnly, adCmdText 
 
 'Clean up 
 objRs.Close 
 Set objRs = Nothing 
 Exit Sub 
 
ErrHandler: 
 If Not objRs Is Nothing Then 
 If objRs.State = adStateOpen Then objRs.Close 
 Set objRs = Nothing 
 End If 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndRsTour 
```

<br/>

<span data-ttu-id="b72bb-p103">次の SQL クエリは、5 つの行 (レコード) と 3 つの列 (フィールド) を持つ **Recordset** を取得します。次の表に各行の値を示します。</span><span class="sxs-lookup"><span data-stu-id="b72bb-p103">This SQL query returns a **Recordset** with five rows (records) and three columns (fields). The values for each row are shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b72bb-111">フィールド 0</span><span class="sxs-lookup"><span data-stu-id="b72bb-111">FIELD 0</span></span><br />
<span data-ttu-id="b72bb-112">名 = [商品コード]</span><span class="sxs-lookup"><span data-stu-id="b72bb-112">Name = ProductID</span></span></p></th>
<th><p><span data-ttu-id="b72bb-113">フィールド 1</span><span class="sxs-lookup"><span data-stu-id="b72bb-113">FIELD 1</span></span><br />
<span data-ttu-id="b72bb-114">名 = [商品名]</span><span class="sxs-lookup"><span data-stu-id="b72bb-114">Name = ProductName</span></span></p></th>
<th><p><span data-ttu-id="b72bb-115">フィールド 2</span><span class="sxs-lookup"><span data-stu-id="b72bb-115">FIELD 2</span></span><br />
<span data-ttu-id="b72bb-116">名 = [単価]</span><span class="sxs-lookup"><span data-stu-id="b72bb-116">Name = UnitPrice</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b72bb-117">7</span><span class="sxs-lookup"><span data-stu-id="b72bb-117">7</span></span></p></td>
<td><p><span data-ttu-id="b72bb-118">Uncle Bob's Organic Dried Pears</span><span class="sxs-lookup"><span data-stu-id="b72bb-118">Uncle Bob's Organic Dried Pears</span></span></p></td>
<td><p><span data-ttu-id="b72bb-119">30.0000</span><span class="sxs-lookup"><span data-stu-id="b72bb-119">30.0000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b72bb-120">14</span><span class="sxs-lookup"><span data-stu-id="b72bb-120">14</span></span></p></td>
<td><p><span data-ttu-id="b72bb-121">Tofu</span><span class="sxs-lookup"><span data-stu-id="b72bb-121">Tofu</span></span></p></td>
<td><p><span data-ttu-id="b72bb-122">23.2500</span><span class="sxs-lookup"><span data-stu-id="b72bb-122">23.2500</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b72bb-123">28</span><span class="sxs-lookup"><span data-stu-id="b72bb-123">28</span></span></p></td>
<td><p><span data-ttu-id="b72bb-124">Rssle Sauerkraut</span><span class="sxs-lookup"><span data-stu-id="b72bb-124">Rssle Sauerkraut</span></span></p></td>
<td><p><span data-ttu-id="b72bb-125">45.6000</span><span class="sxs-lookup"><span data-stu-id="b72bb-125">45.6000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b72bb-126">51</span><span class="sxs-lookup"><span data-stu-id="b72bb-126">51</span></span></p></td>
<td><p><span data-ttu-id="b72bb-127">Manjimup Dried Apples</span><span class="sxs-lookup"><span data-stu-id="b72bb-127">Manjimup Dried Apples</span></span></p></td>
<td><p><span data-ttu-id="b72bb-128">53.0000</span><span class="sxs-lookup"><span data-stu-id="b72bb-128">53.0000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b72bb-129">74</span><span class="sxs-lookup"><span data-stu-id="b72bb-129">74</span></span></p></td>
<td><p><span data-ttu-id="b72bb-130">Longlife Tofu</span><span class="sxs-lookup"><span data-stu-id="b72bb-130">Longlife Tofu</span></span></p></td>
<td><p><span data-ttu-id="b72bb-131">10.0000</span><span class="sxs-lookup"><span data-stu-id="b72bb-131">10.0000</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b72bb-132">次のセクションでは、このサンプル**Recordset**でのカーソルの現在位置を検索する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="b72bb-132">The next section explains how to locate the current position of the cursor in this sample **Recordset**.</span></span>

<span data-ttu-id="b72bb-133">この章では、次のトピックについて説明します。</span><span class="sxs-lookup"><span data-stu-id="b72bb-133">This chapter covers the following topics:</span></span>

- [<span data-ttu-id="b72bb-134">(ADO) の現在のレコードを検索します。</span><span class="sxs-lookup"><span data-stu-id="b72bb-134">Locating the current record (ADO)</span></span>](locating-the-current-record.md)
- [<span data-ttu-id="b72bb-135">(ADO) のデータを移動します。</span><span class="sxs-lookup"><span data-stu-id="b72bb-135">Navigating through the data (ADO)</span></span>](navigating-through-the-data.md)
- [<span data-ttu-id="b72bb-136">(ADO) レコード セットの構造を理解します。</span><span class="sxs-lookup"><span data-stu-id="b72bb-136">Understanding Recordset structure (ADO)</span></span>](understanding-recordset-structure.md)