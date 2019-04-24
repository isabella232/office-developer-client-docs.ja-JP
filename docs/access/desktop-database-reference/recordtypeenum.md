---
title: recordtypeenum (Access デスクトップデータベースリファレンス)
TOCTitle: RecordTypeEnum
ms:assetid: 7edd6508-1507-4649-f1aa-03f1873ef09c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249534(v=office.15)
ms:contentKeyID: 48545890
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c95e4b78a3e2259c3dc5961e87b98ca65ea55692
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309284"
---
# <a name="recordtypeenum"></a><span data-ttu-id="14a66-102">RecordTypeEnum</span><span class="sxs-lookup"><span data-stu-id="14a66-102">RecordTypeEnum</span></span>

<span data-ttu-id="14a66-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="14a66-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="14a66-104">[Record](record-object-ado.md) オブジェクトの種類を表します。</span><span class="sxs-lookup"><span data-stu-id="14a66-104">Specifies the type of [Record](record-object-ado.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="14a66-105">定数</span><span class="sxs-lookup"><span data-stu-id="14a66-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="14a66-106">値</span><span class="sxs-lookup"><span data-stu-id="14a66-106">Value</span></span></p></th>
<th><p><span data-ttu-id="14a66-107">説明</span><span class="sxs-lookup"><span data-stu-id="14a66-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="14a66-108"><strong>adsimplerecord</strong></span><span class="sxs-lookup"><span data-stu-id="14a66-108"><strong>adSimpleRecord</strong></span></span></p></td>
<td><p><span data-ttu-id="14a66-109">.0</span><span class="sxs-lookup"><span data-stu-id="14a66-109">0</span></span></p></td>
<td><p><span data-ttu-id="14a66-110">"単純" レコード (子ノードがないレコード) を示します。</span><span class="sxs-lookup"><span data-stu-id="14a66-110">Indicates a <em>simple</em> record (does not contain child nodes).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14a66-111"><strong>adcollectionrecord</strong></span><span class="sxs-lookup"><span data-stu-id="14a66-111"><strong>adCollectionRecord</strong></span></span></p></td>
<td><p><span data-ttu-id="14a66-112">1-d</span><span class="sxs-lookup"><span data-stu-id="14a66-112">1</span></span></p></td>
<td><p><span data-ttu-id="14a66-113">"コレクション" レコード (子ノードがあるレコード) を示します。</span><span class="sxs-lookup"><span data-stu-id="14a66-113">Indicates a <em>collection</em> record (contains child nodes).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14a66-114"><strong>adrecordunknown</strong></span><span class="sxs-lookup"><span data-stu-id="14a66-114"><strong>adRecordUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="14a66-115">-1</span><span class="sxs-lookup"><span data-stu-id="14a66-115">-1</span></span></p></td>
<td><p><span data-ttu-id="14a66-116">この <strong>Record</strong> の種類が不明であることを示します。</span><span class="sxs-lookup"><span data-stu-id="14a66-116">Indicates that the type of this <strong>Record</strong> is unknown.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14a66-117"><strong>adStructDoc</strong></span><span class="sxs-lookup"><span data-stu-id="14a66-117"><strong>adStructDoc</strong></span></span></p></td>
<td><p><span data-ttu-id="14a66-118">pbm-2</span><span class="sxs-lookup"><span data-stu-id="14a66-118">2</span></span></p></td>
<td><p><span data-ttu-id="14a66-119">COM 構造化ドキュメントを表す特殊な "コレクション" レコードを示します。</span><span class="sxs-lookup"><span data-stu-id="14a66-119">Indicates a special kind of <em>collection</em> record that represents COM structured documents.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="14a66-120">ADO/WFC と同等</span><span class="sxs-lookup"><span data-stu-id="14a66-120">ADO/WFC equivalent</span></span>

<span data-ttu-id="14a66-121">これらの定数に ADO/WFC 等価はありません。</span><span class="sxs-lookup"><span data-stu-id="14a66-121">These constants do not have ADO/WFC equivalents.</span></span>

