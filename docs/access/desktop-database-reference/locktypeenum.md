---
title: LockTypeEnum (デスクトップ データベース参照のアクセス)
TOCTitle: LockTypeEnum
ms:assetid: 966b4952-5591-4a99-82d5-99cb9ae3fc72
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249667(v=office.15)
ms:contentKeyID: 48546448
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cf882c6a63edbf3df067016a6ed793e05f41e74c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477805"
---
# <a name="locktypeenum"></a><span data-ttu-id="a1368-102">LockTypeEnum</span><span class="sxs-lookup"><span data-stu-id="a1368-102">LockTypeEnum</span></span>


<span data-ttu-id="a1368-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="a1368-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a1368-104">編集時にレコードに適用されるロックの種類を表します。</span><span class="sxs-lookup"><span data-stu-id="a1368-104">Specifies the type of lock placed on records during editing.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a1368-105">定数</span><span class="sxs-lookup"><span data-stu-id="a1368-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="a1368-106">値</span><span class="sxs-lookup"><span data-stu-id="a1368-106">Value</span></span></p></th>
<th><p><span data-ttu-id="a1368-107">説明</span><span class="sxs-lookup"><span data-stu-id="a1368-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a1368-108"><strong>adLockBatchOptimistic</strong></span><span class="sxs-lookup"><span data-stu-id="a1368-108"><strong>adLockBatchOptimistic</strong></span></span></p></td>
<td><p><span data-ttu-id="a1368-109">4</span><span class="sxs-lookup"><span data-stu-id="a1368-109">4</span></span></p></td>
<td><p><span data-ttu-id="a1368-p101">共有的バッチ更新を示します。バッチ更新モードの場合に必要です。</span><span class="sxs-lookup"><span data-stu-id="a1368-p101">Indicates optimistic batch updates. Required for batch update mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1368-112"><strong>adLockOptimistic</strong></span><span class="sxs-lookup"><span data-stu-id="a1368-112"><strong>adLockOptimistic</strong></span></span></p></td>
<td><p><span data-ttu-id="a1368-113">3</span><span class="sxs-lookup"><span data-stu-id="a1368-113">3</span></span></p></td>
<td><p><span data-ttu-id="a1368-p102">レコード単位の共有的ロックを示します。<a href="update-method-ado.md">Update</a> メソッドを呼び出した場合にのみ、プロバイダーは共有的ロックを使ってレコードをロックします。</span><span class="sxs-lookup"><span data-stu-id="a1368-p102">Indicates optimistic locking, record by record. The provider uses optimistic locking, locking records only when you call the <a href="update-method-ado.md">Update</a> method.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1368-116"><strong>adLockPessimistic</strong></span><span class="sxs-lookup"><span data-stu-id="a1368-116"><strong>adLockPessimistic</strong></span></span></p></td>
<td><p><span data-ttu-id="a1368-117">2</span><span class="sxs-lookup"><span data-stu-id="a1368-117">2</span></span></p></td>
<td><p><span data-ttu-id="a1368-p103">レコード単位の排他的ロックを示します。プロバイダーは、レコードを確実に編集するための措置を行います。通常は、編集直後にデータ ソースでレコードをロックします。</span><span class="sxs-lookup"><span data-stu-id="a1368-p103">Indicates pessimistic locking, record by record. The provider does what is necessary to ensure successful editing of the records, usually by locking records at the data source immediately after editing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1368-120"><strong>adLockReadOnly</strong></span><span class="sxs-lookup"><span data-stu-id="a1368-120"><strong>adLockReadOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="a1368-121">1</span><span class="sxs-lookup"><span data-stu-id="a1368-121">1</span></span></p></td>
<td><p><span data-ttu-id="a1368-p104">読み取り専用のレコードを示します。データの変更はできません。</span><span class="sxs-lookup"><span data-stu-id="a1368-p104">Indicates read-only records. You cannot alter the data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1368-124"><strong>adLockUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="a1368-124"><strong>adLockUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="a1368-125">-1</span><span class="sxs-lookup"><span data-stu-id="a1368-125">-1</span></span></p></td>
<td><p><span data-ttu-id="a1368-p105">ロックの種類を指定しません。複製の場合、複製元と同じロックの種類が適用されます。</span><span class="sxs-lookup"><span data-stu-id="a1368-p105">Does not specify a type of lock. For clones, the clone is created with the same lock type as the original.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a1368-128">**ADO/WFC 等価**</span><span class="sxs-lookup"><span data-stu-id="a1368-128">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="a1368-129">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="a1368-129">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a1368-130">定数</span><span class="sxs-lookup"><span data-stu-id="a1368-130">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a1368-131">AdoEnums.LockType.BATCHOPTIMISTIC</span><span class="sxs-lookup"><span data-stu-id="a1368-131">AdoEnums.LockType.BATCHOPTIMISTIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1368-132">AdoEnums.LockType.OPTIMISTIC</span><span class="sxs-lookup"><span data-stu-id="a1368-132">AdoEnums.LockType.OPTIMISTIC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1368-133">AdoEnums.LockType.PESSIMISTIC</span><span class="sxs-lookup"><span data-stu-id="a1368-133">AdoEnums.LockType.PESSIMISTIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1368-134">AdoEnums.LockType.READONLY</span><span class="sxs-lookup"><span data-stu-id="a1368-134">AdoEnums.LockType.READONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1368-135">AdoEnums.LockType.UNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="a1368-135">AdoEnums.LockType.UNSPECIFIED</span></span></p></td>
</tr>
</tbody>
</table>

