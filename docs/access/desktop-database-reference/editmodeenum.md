---
title: EditModeEnum (デスクトップ データベース参照のアクセス)
TOCTitle: EditModeEnum
ms:assetid: 4da0e504-aca2-b769-04a2-0df687fa4422
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249248(v=office.15)
ms:contentKeyID: 48544737
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7322193971e4230afaacbb1f614c7ab682f3c149
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478123"
---
# <a name="editmodeenum"></a><span data-ttu-id="245a3-102">EditModeEnum</span><span class="sxs-lookup"><span data-stu-id="245a3-102">EditModeEnum</span></span>


<span data-ttu-id="245a3-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="245a3-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="245a3-104">レコードの編集状況を示します。</span><span class="sxs-lookup"><span data-stu-id="245a3-104">Specifies the editing status of a record.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="245a3-105">定数</span><span class="sxs-lookup"><span data-stu-id="245a3-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="245a3-106">値</span><span class="sxs-lookup"><span data-stu-id="245a3-106">Value</span></span></p></th>
<th><p><span data-ttu-id="245a3-107">説明</span><span class="sxs-lookup"><span data-stu-id="245a3-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="245a3-108"><strong>adEditNone</strong></span><span class="sxs-lookup"><span data-stu-id="245a3-108"><strong>adEditNone</strong></span></span></p></td>
<td><p><span data-ttu-id="245a3-109">0</span><span class="sxs-lookup"><span data-stu-id="245a3-109">0</span></span></p></td>
<td><p><span data-ttu-id="245a3-110">進行中の編集操作がないことを示します。</span><span class="sxs-lookup"><span data-stu-id="245a3-110">Indicates that no editing operation is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="245a3-111"><strong>adEditInProgress</strong></span><span class="sxs-lookup"><span data-stu-id="245a3-111"><strong>adEditInProgress</strong></span></span></p></td>
<td><p><span data-ttu-id="245a3-112">1</span><span class="sxs-lookup"><span data-stu-id="245a3-112">1</span></span></p></td>
<td><p><span data-ttu-id="245a3-113">現在のレコードのデータが変更されたが、保存されていないことを示します。</span><span class="sxs-lookup"><span data-stu-id="245a3-113">Indicates that data in the current record has been modified but not saved.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="245a3-114"><strong>adEditAdd</strong></span><span class="sxs-lookup"><span data-stu-id="245a3-114"><strong>adEditAdd</strong></span></span></p></td>
<td><p><span data-ttu-id="245a3-115">2</span><span class="sxs-lookup"><span data-stu-id="245a3-115">2</span></span></p></td>
<td><p><span data-ttu-id="245a3-116"><a href="addnew-method-ado.md">AddNew</a> メソッドが呼び出され、コピー バッファー内の現在のレコードが、データベースに保存されていない新しいレコードであることを示します。</span><span class="sxs-lookup"><span data-stu-id="245a3-116">Indicates that the <a href="addnew-method-ado.md">AddNew</a> method has been called, and the current record in the copy buffer is a new record that has not been saved in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="245a3-117"><strong>adEditDelete</strong></span><span class="sxs-lookup"><span data-stu-id="245a3-117"><strong>adEditDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="245a3-118">4</span><span class="sxs-lookup"><span data-stu-id="245a3-118">4</span></span></p></td>
<td><p><span data-ttu-id="245a3-119">現在のレコードが削除されたことを示します。</span><span class="sxs-lookup"><span data-stu-id="245a3-119">Indicates that the current record has been deleted.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="245a3-120">**ADO/WFC 等価**</span><span class="sxs-lookup"><span data-stu-id="245a3-120">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="245a3-121">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="245a3-121">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="245a3-122">定数</span><span class="sxs-lookup"><span data-stu-id="245a3-122">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="245a3-123">AdoEnums.EditMode.NONE</span><span class="sxs-lookup"><span data-stu-id="245a3-123">AdoEnums.EditMode.NONE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="245a3-124">AdoEnums.EditMode.INPROGRESS</span><span class="sxs-lookup"><span data-stu-id="245a3-124">AdoEnums.EditMode.INPROGRESS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="245a3-125">AdoEnums.EditMode.ADD</span><span class="sxs-lookup"><span data-stu-id="245a3-125">AdoEnums.EditMode.ADD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="245a3-126">AdoEnums.EditMode.DELETE</span><span class="sxs-lookup"><span data-stu-id="245a3-126">AdoEnums.EditMode.DELETE</span></span></p></td>
</tr>
</tbody>
</table>

