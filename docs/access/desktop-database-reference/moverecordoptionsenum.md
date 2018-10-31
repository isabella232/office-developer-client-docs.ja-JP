---
title: MoveRecordOptionsEnum
TOCTitle: MoveRecordOptionsEnum
ms:assetid: 2785bca0-777c-a802-51d7-6f5cf0fb4210
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249039(v=office.15)
ms:contentKeyID: 48543842
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fc621f620a7d55571aa55296a4d294fff9566bf5
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862241"
---
# <a name="moverecordoptionsenum"></a><span data-ttu-id="3f49c-102">MoveRecordOptionsEnum</span><span class="sxs-lookup"><span data-stu-id="3f49c-102">MoveRecordOptionsEnum</span></span>


<span data-ttu-id="3f49c-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="3f49c-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="3f49c-104">[Record](record-object-ado.md) オブジェクトの [MoveRecord](moverecord-method-ado.md) メソッドの動作を表します。</span><span class="sxs-lookup"><span data-stu-id="3f49c-104">Specifies the behavior of the [Record](record-object-ado.md) object [MoveRecord](moverecord-method-ado.md) method.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3f49c-105">定数</span><span class="sxs-lookup"><span data-stu-id="3f49c-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="3f49c-106">値</span><span class="sxs-lookup"><span data-stu-id="3f49c-106">Value</span></span></p></th>
<th><p><span data-ttu-id="3f49c-107">説明</span><span class="sxs-lookup"><span data-stu-id="3f49c-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3f49c-108"><strong>adMoveUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="3f49c-108"><strong>adMoveUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="3f49c-109">-1</span><span class="sxs-lookup"><span data-stu-id="3f49c-109">-1</span></span></p></td>
<td><p><span data-ttu-id="3f49c-p101">既定値。既定の移動操作を実行します。既存の宛先ファイルまたはディレクトリがある場合は操作が失敗し、ハイパーテキスト リンクが更新されます。</span><span class="sxs-lookup"><span data-stu-id="3f49c-p101">Default. Performs the default move operation: The operation fails if the destination file or directory already exists, and the operation updates hypertext links.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f49c-112"><strong>adMoveOverWrite</strong></span><span class="sxs-lookup"><span data-stu-id="3f49c-112"><strong>adMoveOverWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="3f49c-113">1</span><span class="sxs-lookup"><span data-stu-id="3f49c-113">1</span></span></p></td>
<td><p><span data-ttu-id="3f49c-114">既存の宛先ファイルまたはディレクトリがあっても上書きします。</span><span class="sxs-lookup"><span data-stu-id="3f49c-114">Overwrites the destination file or directory, even if it already exists.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f49c-115"><strong>adMoveDontUpdateLinks</strong></span><span class="sxs-lookup"><span data-stu-id="3f49c-115"><strong>adMoveDontUpdateLinks</strong></span></span></p></td>
<td><p><span data-ttu-id="3f49c-116">2</span><span class="sxs-lookup"><span data-stu-id="3f49c-116">2</span></span></p></td>
<td><p><span data-ttu-id="3f49c-p102">ソース <strong>Record</strong> のハイパーテキスト リンクを更新しないことで、<strong>MoveRecord</strong> メソッドの既定動作を変更します。既定動作はプロバイダーの機能によって異なります。プロバイダーがサポートしていれば、移動操作でリンクが更新されます。プロバイダーがリンクの修正をサポートしていない場合、またはこの値が指定されていない場合、リンクを修正しなくても移動は成功します。</span><span class="sxs-lookup"><span data-stu-id="3f49c-p102">Modifies the default behavior of <strong>MoveRecord</strong> method by not updating the hypertext links of the source <strong>Record</strong>. The default behavior depends on the capabilities of the provider. Move operation updates links if the provider is capable. If the provider cannot fix links or if this value is not specified, then the move succeeds even when links have not been fixed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f49c-121"><strong>adMoveAllowEmulation</strong></span><span class="sxs-lookup"><span data-stu-id="3f49c-121"><strong>adMoveAllowEmulation</strong></span></span></p></td>
<td><p><span data-ttu-id="3f49c-122">4</span><span class="sxs-lookup"><span data-stu-id="3f49c-122">4</span></span></p></td>
<td><p><span data-ttu-id="3f49c-p103">プロバイダーによる移動 (ダウンロード、アップロード、削除の操作を使用) のシミュレーションを要求します。宛先 URL がソースとは別のサーバーにあったり、別のプロバイダーがサービスを提供しているために <strong>Record</strong> の移動が失敗すると、プロバイダー間でリソースを移動するときのプロバイダーの機能の違いにより、遅延時間の増加やデータの損失が起きることがあります。</span><span class="sxs-lookup"><span data-stu-id="3f49c-p103">Requests that the provider attempt to simulate the move (using download, upload, and delete operations). If the attempt to move the <strong>Record</strong> fails because the destination URL is on a different server or serviced by a different provider than the source, this may cause increased latency or data loss, due to different provider capabilities when moving resources between providers.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="3f49c-125">ADO/WFC に相当</span><span class="sxs-lookup"><span data-stu-id="3f49c-125">ADO/WFC equivalent</span></span>

<span data-ttu-id="3f49c-126">これらの定数に ADO/WFC 等価はありません。</span><span class="sxs-lookup"><span data-stu-id="3f49c-126">These constants do not have ADO/WFC equivalents.</span></span>

