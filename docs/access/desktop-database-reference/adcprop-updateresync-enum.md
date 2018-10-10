---
title: ADCPROP_UPDATERESYNC_ENUM
TOCTitle: ADCPROP_UPDATERESYNC_ENUM
ms:assetid: 890210c4-2290-ddb2-8814-022093c318de
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249600(v=office.15)
ms:contentKeyID: 48546145
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ce8a0555e758cf2f3435de755720f312705ba374
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478058"
---
# <a name="adcpropupdateresyncenum"></a><span data-ttu-id="6827e-102">ADCPROP\_UPDATERESYNC\_列挙型</span><span class="sxs-lookup"><span data-stu-id="6827e-102">ADCPROP\_UPDATERESYNC\_ENUM</span></span>

<span data-ttu-id="6827e-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="6827e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6827e-104">[UpdateBatch](updatebatch-method-ado.md) メソッドに暗黙の [Resync](resync-method-ado.md) メソッド操作が続くかどうかを示し、続く場合はその操作の適用範囲を指定します。</span><span class="sxs-lookup"><span data-stu-id="6827e-104">Specifies whether the [UpdateBatch](updatebatch-method-ado.md) method is followed by an implicit [Resync](resync-method-ado.md) method operation and if so, the scope of that operation.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6827e-105">定数</span><span class="sxs-lookup"><span data-stu-id="6827e-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="6827e-106">値</span><span class="sxs-lookup"><span data-stu-id="6827e-106">Value</span></span></p></th>
<th><p><span data-ttu-id="6827e-107">説明</span><span class="sxs-lookup"><span data-stu-id="6827e-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6827e-108"><strong>adResyncAll</strong></span><span class="sxs-lookup"><span data-stu-id="6827e-108"><strong>adResyncAll</strong></span></span></p></td>
<td><p><span data-ttu-id="6827e-109">15</span><span class="sxs-lookup"><span data-stu-id="6827e-109">15</span></span></p></td>
<td><p><span data-ttu-id="6827e-110">他のすべての ADCPROP_UPDATERESYNC_ENUM メンバーの結合された値を使用して、<strong>Resync</strong> を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="6827e-110">Invokes <strong>Resync</strong> with the combined value of all the other ADCPROP_UPDATERESYNC_ENUM members.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6827e-111"><strong>adResyncAutoIncrement</strong></span><span class="sxs-lookup"><span data-stu-id="6827e-111"><strong>adResyncAutoIncrement</strong></span></span></p></td>
<td><p><span data-ttu-id="6827e-112">1</span><span class="sxs-lookup"><span data-stu-id="6827e-112">1</span></span></p></td>
<td><p><span data-ttu-id="6827e-p101">既定値です。Microsoft Jet AutoNumber フィールドや Microsoft SQL Server の Identity 列など、データ ソースによって自動的に増分または生成される列の新しい ID 値を取得します。</span><span class="sxs-lookup"><span data-stu-id="6827e-p101">Default. Attempts to retrieve the new identity value for columns that are automatically incremented or generated by the data source, such as Microsoft Jet AutoNumber fields or Microsoft SQL Server Identity columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6827e-115"><strong>adResyncConflicts</strong></span><span class="sxs-lookup"><span data-stu-id="6827e-115"><strong>adResyncConflicts</strong></span></span></p></td>
<td><p><span data-ttu-id="6827e-116">2</span><span class="sxs-lookup"><span data-stu-id="6827e-116">2</span></span></p></td>
<td><p><span data-ttu-id="6827e-117">同時実行の競合により更新操作または削除操作が失敗したすべての行について、<strong>Resync</strong> を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="6827e-117">Invokes <strong>Resync</strong> for all rows in which the update or delete operation failed because of a concurrency conflict.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6827e-118"><strong>adResyncInserts</strong></span><span class="sxs-lookup"><span data-stu-id="6827e-118"><strong>adResyncInserts</strong></span></span></p></td>
<td><p><span data-ttu-id="6827e-119">8</span><span class="sxs-lookup"><span data-stu-id="6827e-119">8</span></span></p></td>
<td><p><span data-ttu-id="6827e-120">正常に挿入されたすべての行について、 <strong>Resync</strong>を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="6827e-120">Invokes <strong>Resync</strong> for all successfully inserted rows.</span></span> <span data-ttu-id="6827e-121">ただし、オートインクリメント ・ カラムの値は再同期できません。</span><span class="sxs-lookup"><span data-stu-id="6827e-121">However, AutoIncrement column values are not resynchronized.</span></span> <span data-ttu-id="6827e-122">代わりに、新しく挿入された行の内容は、既存の主キーの値に基づいて再同期化されます。</span><span class="sxs-lookup"><span data-stu-id="6827e-122">Instead, the contents of newly inserted rows are resynchronized based on the existing primary key value.</span></span> <span data-ttu-id="6827e-123">主キーがオートインクリメント値の場合は、<strong>再同期</strong>と、目的の行の内容を取得できません。</span><span class="sxs-lookup"><span data-stu-id="6827e-123">If the primary key is an AutoIncrement value, <strong>Resync</strong> won't retrieve the contents of the intended row.</span></span> <span data-ttu-id="6827e-124">オートインクリメント ・ プライマリ ・ キー値を自動的にインクリメントするには、合計値の<strong>adResyncAutoIncrement</strong> + <strong>adResyncInserts</strong>に<strong>UpdateBatch</strong>を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="6827e-124">For automatically incrementing AutoIncrement primary key values, call <strong>UpdateBatch</strong> with the combined value <strong>adResyncAutoIncrement</strong> + <strong>adResyncInserts</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6827e-125"><strong>adResyncNone</strong></span><span class="sxs-lookup"><span data-stu-id="6827e-125"><strong>adResyncNone</strong></span></span></p></td>
<td><p><span data-ttu-id="6827e-126">0</span><span class="sxs-lookup"><span data-stu-id="6827e-126">0</span></span></p></td>
<td><p><span data-ttu-id="6827e-127"><strong>Resync</strong> を呼び出しません。</span><span class="sxs-lookup"><span data-stu-id="6827e-127">Does not invoke <strong>Resync</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6827e-128"><strong>adResyncUpdates</strong></span><span class="sxs-lookup"><span data-stu-id="6827e-128"><strong>adResyncUpdates</strong></span></span></p></td>
<td><p><span data-ttu-id="6827e-129">4</span><span class="sxs-lookup"><span data-stu-id="6827e-129">4</span></span></p></td>
<td><p><span data-ttu-id="6827e-130">正常に更新されたすべての行について、<strong>Resync</strong> を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="6827e-130">Invokes <strong>Resync</strong> for all successfully updated rows.</span></span></p></td>
</tr>
</tbody>
</table>
