---
title: EditModeEnum (デスクトップ データベース参照のアクセス)
TOCTitle: EditModeEnum
ms:assetid: 4da0e504-aca2-b769-04a2-0df687fa4422
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249248(v=office.15)
ms:contentKeyID: 48544737
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 246d9e29f084efb975783fd15c15993eba5a6e74
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726289"
---
# <a name="editmodeenum"></a><span data-ttu-id="71915-102">EditModeEnum</span><span class="sxs-lookup"><span data-stu-id="71915-102">EditModeEnum</span></span>

<span data-ttu-id="71915-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="71915-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="71915-104">レコードの編集状況を示します。</span><span class="sxs-lookup"><span data-stu-id="71915-104">Specifies the editing status of a record.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="71915-105">定数</span><span class="sxs-lookup"><span data-stu-id="71915-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="71915-106">値</span><span class="sxs-lookup"><span data-stu-id="71915-106">Value</span></span></p></th>
<th><p><span data-ttu-id="71915-107">説明</span><span class="sxs-lookup"><span data-stu-id="71915-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="71915-108"><strong>adEditNone</strong></span><span class="sxs-lookup"><span data-stu-id="71915-108"><strong>adEditNone</strong></span></span></p></td>
<td><p><span data-ttu-id="71915-109">0</span><span class="sxs-lookup"><span data-stu-id="71915-109">0</span></span></p></td>
<td><p><span data-ttu-id="71915-110">進行中の編集操作がないことを示します。</span><span class="sxs-lookup"><span data-stu-id="71915-110">Indicates that no editing operation is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71915-111"><strong>adEditInProgress</strong></span><span class="sxs-lookup"><span data-stu-id="71915-111"><strong>adEditInProgress</strong></span></span></p></td>
<td><p><span data-ttu-id="71915-112">1</span><span class="sxs-lookup"><span data-stu-id="71915-112">1</span></span></p></td>
<td><p><span data-ttu-id="71915-113">現在のレコードのデータが変更されたが、保存されていないことを示します。</span><span class="sxs-lookup"><span data-stu-id="71915-113">Indicates that data in the current record has been modified but not saved.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71915-114"><strong>adEditAdd</strong></span><span class="sxs-lookup"><span data-stu-id="71915-114"><strong>adEditAdd</strong></span></span></p></td>
<td><p><span data-ttu-id="71915-115">2</span><span class="sxs-lookup"><span data-stu-id="71915-115">2</span></span></p></td>
<td><p><span data-ttu-id="71915-116"><a href="addnew-method-ado.md">AddNew</a> メソッドが呼び出され、コピー バッファー内の現在のレコードが、データベースに保存されていない新しいレコードであることを示します。</span><span class="sxs-lookup"><span data-stu-id="71915-116">Indicates that the <a href="addnew-method-ado.md">AddNew</a> method has been called, and the current record in the copy buffer is a new record that has not been saved in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71915-117"><strong>adEditDelete</strong></span><span class="sxs-lookup"><span data-stu-id="71915-117"><strong>adEditDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="71915-118">4</span><span class="sxs-lookup"><span data-stu-id="71915-118">4</span></span></p></td>
<td><p><span data-ttu-id="71915-119">現在のレコードが削除されたことを示します。</span><span class="sxs-lookup"><span data-stu-id="71915-119">Indicates that the current record has been deleted.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="71915-120">ADO/WFC に相当</span><span class="sxs-lookup"><span data-stu-id="71915-120">ADO/WFC equivalent</span></span>

<span data-ttu-id="71915-121">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="71915-121">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="71915-122">定数</span><span class="sxs-lookup"><span data-stu-id="71915-122">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="71915-123">AdoEnums.EditMode.NONE</span><span class="sxs-lookup"><span data-stu-id="71915-123">AdoEnums.EditMode.NONE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71915-124">AdoEnums.EditMode.INPROGRESS</span><span class="sxs-lookup"><span data-stu-id="71915-124">AdoEnums.EditMode.INPROGRESS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71915-125">AdoEnums.EditMode.ADD</span><span class="sxs-lookup"><span data-stu-id="71915-125">AdoEnums.EditMode.ADD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71915-126">AdoEnums.EditMode.DELETE</span><span class="sxs-lookup"><span data-stu-id="71915-126">AdoEnums.EditMode.DELETE</span></span></p></td>
</tr>
</tbody>
</table>

