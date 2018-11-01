---
title: CopyRecordOptionsEnum
TOCTitle: CopyRecordOptionsEnum
ms:assetid: ab9426e9-0e4e-6c85-43cf-e4a205a7c4c0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249795(v=office.15)
ms:contentKeyID: 48546975
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d3c3ddd8174a646bccd37cec758e85e17f4cdaec
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882778"
---
# <a name="copyrecordoptionsenum"></a><span data-ttu-id="86e8d-102">CopyRecordOptionsEnum</span><span class="sxs-lookup"><span data-stu-id="86e8d-102">CopyRecordOptionsEnum</span></span>


<span data-ttu-id="86e8d-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="86e8d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="86e8d-104">[CopyRecord](copyrecord-method-ado.md) メソッドの動作を表します。</span><span class="sxs-lookup"><span data-stu-id="86e8d-104">Specifies the behavior of the [CopyRecord](copyrecord-method-ado.md) method.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="86e8d-105">定数</span><span class="sxs-lookup"><span data-stu-id="86e8d-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="86e8d-106">値</span><span class="sxs-lookup"><span data-stu-id="86e8d-106">Value</span></span></p></th>
<th><p><span data-ttu-id="86e8d-107">説明</span><span class="sxs-lookup"><span data-stu-id="86e8d-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="86e8d-108"><strong>adCopyAllowEmulation</strong></span><span class="sxs-lookup"><span data-stu-id="86e8d-108"><strong>adCopyAllowEmulation</strong></span></span></p></td>
<td><p><span data-ttu-id="86e8d-109">4</span><span class="sxs-lookup"><span data-stu-id="86e8d-109">4</span></span></p></td>
<td><p><span data-ttu-id="86e8d-110"><em>同期元</em>プロバイダーがダウンロードを使用してコピーをシミュレートし、このメソッドは、<em>リンク先</em>が別のサーバー上にあるもののために障害が発生したり、<em>ソース</em>以外のプロバイダーがサービスを提供、アップロード操作をしようとすることを示します。</span><span class="sxs-lookup"><span data-stu-id="86e8d-110">Indicates that the <em>Source</em> provider attempts to simulate the copy using download and upload operations if this method fails due to <em>Destination</em> being on a different server or is serviced by a different provider than <em>Source</em>.</span></span> <span data-ttu-id="86e8d-111">プロバイダーの機能のさまざまなパフォーマンスが低下したりデータが失われることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="86e8d-111">Note that differing provider capabilities may hamper performance or lose data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="86e8d-112"><strong>adCopyNonRecursive</strong></span><span class="sxs-lookup"><span data-stu-id="86e8d-112"><strong>adCopyNonRecursive</strong></span></span></p></td>
<td><p><span data-ttu-id="86e8d-113">2</span><span class="sxs-lookup"><span data-stu-id="86e8d-113">2</span></span></p></td>
<td><p><span data-ttu-id="86e8d-p102">コピー先に現在のディレクトリをコピーしますが、サブディレクトリはコピーしません。コピー操作は再帰的ではありません。</span><span class="sxs-lookup"><span data-stu-id="86e8d-p102">Copies the current directory, but none of its subdirectories, to the destination. The copy operation is not recursive.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="86e8d-116"><strong>adCopyOverWrite</strong></span><span class="sxs-lookup"><span data-stu-id="86e8d-116"><strong>adCopyOverWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="86e8d-117">1</span><span class="sxs-lookup"><span data-stu-id="86e8d-117">1</span></span></p></td>
<td><p><span data-ttu-id="86e8d-118"><em>宛先</em>は、既存のファイルまたはディレクトリを指している場合は、ファイルまたはディレクトリを上書きします。</span><span class="sxs-lookup"><span data-stu-id="86e8d-118">Overwrites the file or directory if the <em>Destination</em> points to an existing file or directory.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="86e8d-119"><strong>adCopyUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="86e8d-119"><strong>adCopyUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="86e8d-120">-1</span><span class="sxs-lookup"><span data-stu-id="86e8d-120">-1</span></span></p></td>
<td><p><span data-ttu-id="86e8d-p103">既定値。既定のコピー操作を実行します。コピー操作は再帰的に行われ、コピー先のファイルやディレクトリが既に存在する場合は操作が失敗します。</span><span class="sxs-lookup"><span data-stu-id="86e8d-p103">Default. Performs the default copy operation: The operation fails if the destination file or directory already exists, and the operation copies recursively.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="86e8d-123">ADO/WFC に相当</span><span class="sxs-lookup"><span data-stu-id="86e8d-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="86e8d-124">これらの定数に ADO/WFC 等価はありません。</span><span class="sxs-lookup"><span data-stu-id="86e8d-124">These constants do not have ADO/WFC equivalents.</span></span>

