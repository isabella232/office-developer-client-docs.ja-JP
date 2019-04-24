---
title: CopyRecordOptionsEnum
TOCTitle: CopyRecordOptionsEnum
ms:assetid: ab9426e9-0e4e-6c85-43cf-e4a205a7c4c0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249795(v=office.15)
ms:contentKeyID: 48546975
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: eb1637d1757a8507c6b6abb2a0c71867e3d1177b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295486"
---
# <a name="copyrecordoptionsenum"></a><span data-ttu-id="45a38-102">CopyRecordOptionsEnum</span><span class="sxs-lookup"><span data-stu-id="45a38-102">CopyRecordOptionsEnum</span></span>


<span data-ttu-id="45a38-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="45a38-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="45a38-104">[CopyRecord](copyrecord-method-ado.md) メソッドの動作を表します。</span><span class="sxs-lookup"><span data-stu-id="45a38-104">Specifies the behavior of the [CopyRecord](copyrecord-method-ado.md) method.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="45a38-105">定数</span><span class="sxs-lookup"><span data-stu-id="45a38-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="45a38-106">値</span><span class="sxs-lookup"><span data-stu-id="45a38-106">Value</span></span></p></th>
<th><p><span data-ttu-id="45a38-107">説明</span><span class="sxs-lookup"><span data-stu-id="45a38-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="45a38-108"><strong>adcopyallowemulation</strong></span><span class="sxs-lookup"><span data-stu-id="45a38-108"><strong>adCopyAllowEmulation</strong></span></span></p></td>
<td><p><span data-ttu-id="45a38-109">2/4</span><span class="sxs-lookup"><span data-stu-id="45a38-109">4</span></span></p></td>
<td><p><span data-ttu-id="45a38-p101">"コピー先" が別のサーバーにあるか、"コピー元" 以外のプロバイダーのサービスを受けているためにこのメソッドが失敗した場合、"コピー元" プロバイダーがダウンロード操作とアップロード操作を行ってコピーをシミュレートしようとすることを示します。プロバイダーの機能が異なると、パフォーマンスが低下したりデータが失われることがあります。</span><span class="sxs-lookup"><span data-stu-id="45a38-p101">Indicates that the <em>Source</em> provider attempts to simulate the copy using download and upload operations if this method fails due to <em>Destination</em> being on a different server or is serviced by a different provider than <em>Source</em>. Note that differing provider capabilities may hamper performance or lose data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45a38-112"><strong>adCopyNonRecursive</strong></span><span class="sxs-lookup"><span data-stu-id="45a38-112"><strong>adCopyNonRecursive</strong></span></span></p></td>
<td><p><span data-ttu-id="45a38-113">pbm-2</span><span class="sxs-lookup"><span data-stu-id="45a38-113">2</span></span></p></td>
<td><p><span data-ttu-id="45a38-p102">コピー先に現在のディレクトリをコピーしますが、サブディレクトリはコピーしません。コピー操作は再帰的ではありません。</span><span class="sxs-lookup"><span data-stu-id="45a38-p102">Copies the current directory, but none of its subdirectories, to the destination. The copy operation is not recursive.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45a38-116"><strong>adCopyOverWrite</strong></span><span class="sxs-lookup"><span data-stu-id="45a38-116"><strong>adCopyOverWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="45a38-117">1-d</span><span class="sxs-lookup"><span data-stu-id="45a38-117">1</span></span></p></td>
<td><p><span data-ttu-id="45a38-118">"コピー先" が既存のファイルやディレクトリを指す場合、そのファイルやディレクトリを上書きします。</span><span class="sxs-lookup"><span data-stu-id="45a38-118">Overwrites the file or directory if the <em>Destination</em> points to an existing file or directory.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45a38-119"><strong>adcopyunspecified</strong></span><span class="sxs-lookup"><span data-stu-id="45a38-119"><strong>adCopyUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="45a38-120">-1</span><span class="sxs-lookup"><span data-stu-id="45a38-120">-1</span></span></p></td>
<td><p><span data-ttu-id="45a38-p103">既定値。既定のコピー操作を実行します。コピー操作は再帰的に行われ、コピー先のファイルやディレクトリが既に存在する場合は操作が失敗します。</span><span class="sxs-lookup"><span data-stu-id="45a38-p103">Default. Performs the default copy operation: The operation fails if the destination file or directory already exists, and the operation copies recursively.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="45a38-123">ADO/WFC と同等</span><span class="sxs-lookup"><span data-stu-id="45a38-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="45a38-124">これらの定数に ADO/WFC 等価はありません。</span><span class="sxs-lookup"><span data-stu-id="45a38-124">These constants do not have ADO/WFC equivalents.</span></span>

