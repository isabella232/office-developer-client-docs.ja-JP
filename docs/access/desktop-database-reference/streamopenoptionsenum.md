---
title: StreamOpenOptionsEnum
TOCTitle: StreamOpenOptionsEnum
ms:assetid: d4bbd6be-41f1-cdf2-9d8f-b77ce83fb88e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250069(v=office.15)
ms:contentKeyID: 48547951
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3998f41c1400a2870633f19228cbf73189e9527a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478346"
---
# <a name="streamopenoptionsenum"></a><span data-ttu-id="6e046-102">StreamOpenOptionsEnum</span><span class="sxs-lookup"><span data-stu-id="6e046-102">StreamOpenOptionsEnum</span></span>


<span data-ttu-id="6e046-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="6e046-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6e046-p101">[Stream](stream-object-ado.md) オブジェクトを開くときのオプションを表します。これらの値は OR 演算子で結合できます。</span><span class="sxs-lookup"><span data-stu-id="6e046-p101">Specifies options for opening a [Stream](stream-object-ado.md) object. The values can be combined with an OR operation.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6e046-106">定数</span><span class="sxs-lookup"><span data-stu-id="6e046-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="6e046-107">値</span><span class="sxs-lookup"><span data-stu-id="6e046-107">Value</span></span></p></th>
<th><p><span data-ttu-id="6e046-108">説明</span><span class="sxs-lookup"><span data-stu-id="6e046-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6e046-109"><strong>adOpenStreamAsync</strong></span><span class="sxs-lookup"><span data-stu-id="6e046-109"><strong>adOpenStreamAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="6e046-110">1</span><span class="sxs-lookup"><span data-stu-id="6e046-110">1</span></span></p></td>
<td><p><span data-ttu-id="6e046-111">非同期モードで <strong>Stream</strong> オブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="6e046-111">Opens the <strong>Stream</strong> object in asynchronous mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e046-112"><strong>adOpenStreamFromRecord</strong></span><span class="sxs-lookup"><span data-stu-id="6e046-112"><strong>adOpenStreamFromRecord</strong></span></span></p></td>
<td><p><span data-ttu-id="6e046-113">4</span><span class="sxs-lookup"><span data-stu-id="6e046-113">4</span></span></p></td>
<td><p><span data-ttu-id="6e046-p102"><em>Source</em> パラメーターの内容を、既に開かれている <a href="record-object-ado.md">Record</a> オブジェクトとして識別します。既定動作では、<em>Source</em> は、ツリー構造のノードを直接指定する URL として処理します。このノードに関連付けられた既定ストリームが開かれます。</span><span class="sxs-lookup"><span data-stu-id="6e046-p102">Identifies the contents of the <em>Source</em> parameter to be an already open <a href="record-object-ado.md">Record</a> object. The default behavior is to treat <em>Source</em> as a URL that points directly to a node in a tree structure. The default stream associated with that node is opened.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e046-117"><strong>adOpenStreamUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="6e046-117"><strong>adOpenStreamUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="6e046-118">-1</span><span class="sxs-lookup"><span data-stu-id="6e046-118">-1</span></span></p></td>
<td><p><span data-ttu-id="6e046-p103">既定値。既定のオプションで <strong>Stream</strong> オブジェクトを開くことを表します。</span><span class="sxs-lookup"><span data-stu-id="6e046-p103">Default. Specifies opening the <strong>Stream</strong> object with default options.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6e046-121">**ADO/WFC 等価**</span><span class="sxs-lookup"><span data-stu-id="6e046-121">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="6e046-122">これらの定数に ADO/WFC 等価はありません。</span><span class="sxs-lookup"><span data-stu-id="6e046-122">These constants do not have ADO/WFC equivalents.</span></span>
