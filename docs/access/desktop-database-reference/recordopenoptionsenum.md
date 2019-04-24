---
title: RecordOpenOptionsEnum
TOCTitle: RecordOpenOptionsEnum
ms:assetid: 44a69719-0789-a084-fb96-21468e270205
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249207(v=office.15)
ms:contentKeyID: 48544534
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: caaf755ebd63f1805d0c77ef79a0f5863a85050e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300687"
---
# <a name="recordopenoptionsenum"></a><span data-ttu-id="8fc6c-102">RecordOpenOptionsEnum</span><span class="sxs-lookup"><span data-stu-id="8fc6c-102">RecordOpenOptionsEnum</span></span>


<span data-ttu-id="8fc6c-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="8fc6c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8fc6c-104">[Record](record-object-ado.md) を開くときのオプションを表します。</span><span class="sxs-lookup"><span data-stu-id="8fc6c-104">Specifies options for opening a [Record](record-object-ado.md).</span></span> <span data-ttu-id="8fc6c-105">これらの値は OR 演算子で結合できます。</span><span class="sxs-lookup"><span data-stu-id="8fc6c-105">These values may be combined by using OR.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8fc6c-106">定数</span><span class="sxs-lookup"><span data-stu-id="8fc6c-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="8fc6c-107">値</span><span class="sxs-lookup"><span data-stu-id="8fc6c-107">Value</span></span></p></th>
<th><p><span data-ttu-id="8fc6c-108">説明</span><span class="sxs-lookup"><span data-stu-id="8fc6c-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8fc6c-109"><strong>addelayfetchfields</strong></span><span class="sxs-lookup"><span data-stu-id="8fc6c-109"><strong>adDelayFetchFields</strong></span></span></p></td>
<td><p><span data-ttu-id="8fc6c-110">0x8000</span><span class="sxs-lookup"><span data-stu-id="8fc6c-110">0x8000</span></span></p></td>
<td><p><span data-ttu-id="8fc6c-p102">プロバイダーに対して、<strong>Record</strong> に関連付けられたフィールドは、当初は取得する必要がなく、フィールドへの最初のアクセス時に取得できることを示します。このフラグが指定されていない場合の既定動作では、<strong>Record</strong> オブジェクトのすべてのフィールドが取得されます。</span><span class="sxs-lookup"><span data-stu-id="8fc6c-p102">Indicates to the provider that the fields associated with the <strong>Record</strong> need not be retrieved initially, but can be retrieved at the first attempt to access the field. The default behavior, indicated by the absence of this flag, is to retrieve all the <strong>Record</strong> object fields.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8fc6c-113"><strong>addelayfetchstream</strong></span><span class="sxs-lookup"><span data-stu-id="8fc6c-113"><strong>adDelayFetchStream</strong></span></span></p></td>
<td><p><span data-ttu-id="8fc6c-114">0x4000</span><span class="sxs-lookup"><span data-stu-id="8fc6c-114">0x4000</span></span></p></td>
<td><p><span data-ttu-id="8fc6c-p103">プロバイダーに対して、<strong>Record</strong> に関連付けられた既定ストリームを当初は取得する必要がないことを示します。このフラグが指定されていない場合の既定動作では、<strong>Record</strong> オブジェクトに関連付けられた既定ストリームが取得されます。</span><span class="sxs-lookup"><span data-stu-id="8fc6c-p103">Indicates to the provider that the default stream associated with the <strong>Record</strong> need not be retrieved initially. The default behavior, indicated by the absence of this flag, is to retrieve the default stream associated with the <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8fc6c-117"><strong>adopenasync</strong></span><span class="sxs-lookup"><span data-stu-id="8fc6c-117"><strong>adOpenAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="8fc6c-118">0x1000</span><span class="sxs-lookup"><span data-stu-id="8fc6c-118">0x1000</span></span></p></td>
<td><p><span data-ttu-id="8fc6c-119"><strong>Record</strong> オブジェクトが非同期モードで開かれることを示します。</span><span class="sxs-lookup"><span data-stu-id="8fc6c-119">Indicates that the <strong>Record</strong> object is opened in asynchronous mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8fc6c-120"><strong>adOpenExecuteCommand</strong></span><span class="sxs-lookup"><span data-stu-id="8fc6c-120"><strong>adOpenExecuteCommand</strong></span></span></p></td>
<td><p><span data-ttu-id="8fc6c-121">「その他」</span><span class="sxs-lookup"><span data-stu-id="8fc6c-121">0x10000</span></span></p></td>
<td><p><span data-ttu-id="8fc6c-p104">Source 文字列に、実行されるコマンド テキストが含まれることを示します。この値は、<strong>Recordset.Open</strong> の <strong>adCmdText</strong> オプションと等価です。</span><span class="sxs-lookup"><span data-stu-id="8fc6c-p104">Indicates that the Source string contains command text that should be executed. This value is equivalent to the <strong>adCmdText</strong> option on <strong>Recordset.Open</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8fc6c-124"><strong>adopenrecordunspecified</strong></span><span class="sxs-lookup"><span data-stu-id="8fc6c-124"><strong>adOpenRecordUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="8fc6c-125">-1</span><span class="sxs-lookup"><span data-stu-id="8fc6c-125">-1</span></span></p></td>
<td><p><span data-ttu-id="8fc6c-p105">既定値。オプションが指定されていないことを示します。</span><span class="sxs-lookup"><span data-stu-id="8fc6c-p105">Default. Indicates no options are specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8fc6c-128"><strong>adopenoutput</strong></span><span class="sxs-lookup"><span data-stu-id="8fc6c-128"><strong>adOpenOutput</strong></span></span></p></td>
<td><p><span data-ttu-id="8fc6c-129">0x800000</span><span class="sxs-lookup"><span data-stu-id="8fc6c-129">0x800000</span></span></p></td>
<td><p><span data-ttu-id="8fc6c-p106">実行可能スクリプト (拡張子が .ASP のページなど) があるノードをソースが指定している場合、実行したスクリプトの結果が、開いている <strong>Record</strong> に含まれることを示します。この値は、コレクションのないレコードにのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="8fc6c-p106">Indicates that if the source points to a node that contains an executable script (such as an .ASP page), then the opened <strong>Record</strong> will contain the results of the executed script. This value is only valid with non-collection records.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="8fc6c-132">ADO/WFC と同等</span><span class="sxs-lookup"><span data-stu-id="8fc6c-132">ADO/WFC equivalent</span></span>

<span data-ttu-id="8fc6c-133">これらの定数に ADO/WFC 等価はありません。</span><span class="sxs-lookup"><span data-stu-id="8fc6c-133">These constants do not have ADO/WFC equivalents.</span></span>

