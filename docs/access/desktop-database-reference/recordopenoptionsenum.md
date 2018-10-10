---
title: RecordOpenOptionsEnum
TOCTitle: RecordOpenOptionsEnum
ms:assetid: 44a69719-0789-a084-fb96-21468e270205
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249207(v=office.15)
ms:contentKeyID: 48544534
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d9538e1fb4a712b109e021512a3d28d299deaeb3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477687"
---
# <a name="recordopenoptionsenum"></a><span data-ttu-id="844fd-102">RecordOpenOptionsEnum</span><span class="sxs-lookup"><span data-stu-id="844fd-102">RecordOpenOptionsEnum</span></span>


<span data-ttu-id="844fd-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="844fd-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="844fd-p101">[Record](record-object-ado.md) を開くときのオプションを表します。これらの値は OR 演算子で結合できます。</span><span class="sxs-lookup"><span data-stu-id="844fd-p101">Specifies options for opening a [Record](record-object-ado.md). These values may be combined by using OR.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="844fd-106">定数</span><span class="sxs-lookup"><span data-stu-id="844fd-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="844fd-107">値</span><span class="sxs-lookup"><span data-stu-id="844fd-107">Value</span></span></p></th>
<th><p><span data-ttu-id="844fd-108">説明</span><span class="sxs-lookup"><span data-stu-id="844fd-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="844fd-109"><strong>adDelayFetchFields</strong></span><span class="sxs-lookup"><span data-stu-id="844fd-109"><strong>adDelayFetchFields</strong></span></span></p></td>
<td><p><span data-ttu-id="844fd-110">0x8000</span><span class="sxs-lookup"><span data-stu-id="844fd-110">0x8000</span></span></p></td>
<td><p><span data-ttu-id="844fd-p102">プロバイダーに対して、<strong>Record</strong> に関連付けられたフィールドは、当初は取得する必要がなく、フィールドへの最初のアクセス時に取得できることを示します。このフラグが指定されていない場合の既定動作では、<strong>Record</strong> オブジェクトのすべてのフィールドが取得されます。</span><span class="sxs-lookup"><span data-stu-id="844fd-p102">Indicates to the provider that the fields associated with the <strong>Record</strong> need not be retrieved initially, but can be retrieved at the first attempt to access the field. The default behavior, indicated by the absence of this flag, is to retrieve all the <strong>Record</strong> object fields.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="844fd-113"><strong>adDelayFetchStream</strong></span><span class="sxs-lookup"><span data-stu-id="844fd-113"><strong>adDelayFetchStream</strong></span></span></p></td>
<td><p><span data-ttu-id="844fd-114">0x4000</span><span class="sxs-lookup"><span data-stu-id="844fd-114">0x4000</span></span></p></td>
<td><p><span data-ttu-id="844fd-p103">プロバイダーに対して、<strong>Record</strong> に関連付けられた既定ストリームを当初は取得する必要がないことを示します。このフラグが指定されていない場合の既定動作では、<strong>Record</strong> オブジェクトに関連付けられた既定ストリームが取得されます。</span><span class="sxs-lookup"><span data-stu-id="844fd-p103">Indicates to the provider that the default stream associated with the <strong>Record</strong> need not be retrieved initially. The default behavior, indicated by the absence of this flag, is to retrieve the default stream associated with the <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="844fd-117"><strong>adOpenAsync</strong></span><span class="sxs-lookup"><span data-stu-id="844fd-117"><strong>adOpenAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="844fd-118">0x1000</span><span class="sxs-lookup"><span data-stu-id="844fd-118">0x1000</span></span></p></td>
<td><p><span data-ttu-id="844fd-119"><strong>Record</strong> オブジェクトが非同期モードで開かれることを示します。</span><span class="sxs-lookup"><span data-stu-id="844fd-119">Indicates that the <strong>Record</strong> object is opened in asynchronous mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="844fd-120"><strong>adOpenExecuteCommand</strong></span><span class="sxs-lookup"><span data-stu-id="844fd-120"><strong>adOpenExecuteCommand</strong></span></span></p></td>
<td><p><span data-ttu-id="844fd-121">0x10000</span><span class="sxs-lookup"><span data-stu-id="844fd-121">0x10000</span></span></p></td>
<td><p><span data-ttu-id="844fd-p104">Source 文字列に、実行されるコマンド テキストが含まれることを示します。この値は、<strong>Recordset.Open</strong> の <strong>adCmdText</strong> オプションと等価です。</span><span class="sxs-lookup"><span data-stu-id="844fd-p104">Indicates that the Source string contains command text that should be executed. This value is equivalent to the <strong>adCmdText</strong> option on <strong>Recordset.Open</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="844fd-124"><strong>adOpenRecordUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="844fd-124"><strong>adOpenRecordUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="844fd-125">-1</span><span class="sxs-lookup"><span data-stu-id="844fd-125">-1</span></span></p></td>
<td><p><span data-ttu-id="844fd-p105">既定値。オプションが指定されていないことを示します。</span><span class="sxs-lookup"><span data-stu-id="844fd-p105">Default. Indicates no options are specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="844fd-128"><strong>adOpenOutput</strong></span><span class="sxs-lookup"><span data-stu-id="844fd-128"><strong>adOpenOutput</strong></span></span></p></td>
<td><p><span data-ttu-id="844fd-129">0x800000</span><span class="sxs-lookup"><span data-stu-id="844fd-129">0x800000</span></span></p></td>
<td><p><span data-ttu-id="844fd-p106">実行可能スクリプト (拡張子が .ASP のページなど) があるノードをソースが指定している場合、実行したスクリプトの結果が、開いている <strong>Record</strong> に含まれることを示します。この値は、コレクションのないレコードにのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="844fd-p106">Indicates that if the source points to a node that contains an executable script (such as an .ASP page), then the opened <strong>Record</strong> will contain the results of the executed script. This value is only valid with non-collection records.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="844fd-132">**ADO/WFC 等価**</span><span class="sxs-lookup"><span data-stu-id="844fd-132">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="844fd-133">これらの定数に ADO/WFC 等価はありません。</span><span class="sxs-lookup"><span data-stu-id="844fd-133">These constants do not have ADO/WFC equivalents.</span></span>
