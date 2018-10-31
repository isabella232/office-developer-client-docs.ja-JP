---
title: XactAttributeEnum (デスクトップ データベース参照のアクセス)
TOCTitle: XactAttributeEnum
ms:assetid: 9206698b-7cfa-1229-2701-f2b6949e54fc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249643(v=office.15)
ms:contentKeyID: 48546366
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 2d39cc24feb377cf61e7c2d0a39e11513f4c0616
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25864061"
---
# <a name="xactattributeenum"></a><span data-ttu-id="fa4be-102">XactAttributeEnum</span><span class="sxs-lookup"><span data-stu-id="fa4be-102">XactAttributeEnum</span></span>

<span data-ttu-id="fa4be-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="fa4be-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="fa4be-104">[Connection](connection-object-ado.md) オブジェクトのトランザクション属性を表します。</span><span class="sxs-lookup"><span data-stu-id="fa4be-104">Specifies the transaction attributes of a [Connection](connection-object-ado.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fa4be-105">定数</span><span class="sxs-lookup"><span data-stu-id="fa4be-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="fa4be-106">値</span><span class="sxs-lookup"><span data-stu-id="fa4be-106">Value</span></span></p></th>
<th><p><span data-ttu-id="fa4be-107">説明</span><span class="sxs-lookup"><span data-stu-id="fa4be-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fa4be-108"><strong>adXactAbortRetaining</strong></span><span class="sxs-lookup"><span data-stu-id="fa4be-108"><strong>adXactAbortRetaining</strong></span></span></p></td>
<td><p><span data-ttu-id="fa4be-109">262144</span><span class="sxs-lookup"><span data-stu-id="fa4be-109">262144</span></span></p></td>
<td><p><span data-ttu-id="fa4be-110">保持中止は; を実行します。つまり、 <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">RollbackTrans</a>を自動的に呼び出すことは、新しいトランザクションを開始します。</span><span class="sxs-lookup"><span data-stu-id="fa4be-110">Performs retaining aborts; that is, calling <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">RollbackTrans</a> automatically starts a new transaction.</span></span> <span data-ttu-id="fa4be-111">すべてのプロバイダーは、これをサポートします。</span><span class="sxs-lookup"><span data-stu-id="fa4be-111">Not all providers support this.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa4be-112"><strong>adXactCommitRetaining</strong></span><span class="sxs-lookup"><span data-stu-id="fa4be-112"><strong>adXactCommitRetaining</strong></span></span></p></td>
<td><p><span data-ttu-id="fa4be-113">131072</span><span class="sxs-lookup"><span data-stu-id="fa4be-113">131072</span></span></p></td>
<td><p><span data-ttu-id="fa4be-114">保持コミット; を実行します。つまり、 <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">CommitTrans</a>を自動的に呼び出すことは、新しいトランザクションを開始します。</span><span class="sxs-lookup"><span data-stu-id="fa4be-114">Performs retaining commits; that is, calling <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">CommitTrans</a> automatically starts a new transaction.</span></span> <span data-ttu-id="fa4be-115">すべてのプロバイダーは、これをサポートします。</span><span class="sxs-lookup"><span data-stu-id="fa4be-115">Not all providers support this.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="fa4be-116">ADO/WFC に相当</span><span class="sxs-lookup"><span data-stu-id="fa4be-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="fa4be-117">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="fa4be-117">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fa4be-118">定数</span><span class="sxs-lookup"><span data-stu-id="fa4be-118">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fa4be-119">AdoEnums.XactAttribute.ABORTRETAINING</span><span class="sxs-lookup"><span data-stu-id="fa4be-119">AdoEnums.XactAttribute.ABORTRETAINING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa4be-120">AdoEnums.XactAttribute.COMMITRETAINING</span><span class="sxs-lookup"><span data-stu-id="fa4be-120">AdoEnums.XactAttribute.COMMITRETAINING</span></span></p></td>
</tr>
</tbody>
</table>

