---
title: XactAttributeEnum (デスクトップ データベース参照のアクセス)
TOCTitle: XactAttributeEnum
ms:assetid: 9206698b-7cfa-1229-2701-f2b6949e54fc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249643(v=office.15)
ms:contentKeyID: 48546366
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 28b81c45921120b8a3cd8768d22559355d8ff623
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870493"
---
# <a name="xactattributeenum"></a><span data-ttu-id="bec43-102">XactAttributeEnum</span><span class="sxs-lookup"><span data-stu-id="bec43-102">XactAttributeEnum</span></span>

<span data-ttu-id="bec43-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="bec43-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bec43-104">[Connection](connection-object-ado.md) オブジェクトのトランザクション属性を表します。</span><span class="sxs-lookup"><span data-stu-id="bec43-104">Specifies the transaction attributes of a [Connection](connection-object-ado.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bec43-105">定数</span><span class="sxs-lookup"><span data-stu-id="bec43-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="bec43-106">値</span><span class="sxs-lookup"><span data-stu-id="bec43-106">Value</span></span></p></th>
<th><p><span data-ttu-id="bec43-107">説明</span><span class="sxs-lookup"><span data-stu-id="bec43-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bec43-108"><strong>adXactAbortRetaining</strong></span><span class="sxs-lookup"><span data-stu-id="bec43-108"><strong>adXactAbortRetaining</strong></span></span></p></td>
<td><p><span data-ttu-id="bec43-109">262144</span><span class="sxs-lookup"><span data-stu-id="bec43-109">262144</span></span></p></td>
<td><p><span data-ttu-id="bec43-110">保持中止は; を実行します。つまり、 <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">RollbackTrans</a>を自動的に呼び出すことは、新しいトランザクションを開始します。</span><span class="sxs-lookup"><span data-stu-id="bec43-110">Performs retaining aborts; that is, calling <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">RollbackTrans</a> automatically starts a new transaction.</span></span> <span data-ttu-id="bec43-111">すべてのプロバイダーは、これをサポートします。</span><span class="sxs-lookup"><span data-stu-id="bec43-111">Not all providers support this.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bec43-112"><strong>adXactCommitRetaining</strong></span><span class="sxs-lookup"><span data-stu-id="bec43-112"><strong>adXactCommitRetaining</strong></span></span></p></td>
<td><p><span data-ttu-id="bec43-113">131072</span><span class="sxs-lookup"><span data-stu-id="bec43-113">131072</span></span></p></td>
<td><p><span data-ttu-id="bec43-114">保持コミット; を実行します。つまり、 <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">CommitTrans</a>を自動的に呼び出すことは、新しいトランザクションを開始します。</span><span class="sxs-lookup"><span data-stu-id="bec43-114">Performs retaining commits; that is, calling <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">CommitTrans</a> automatically starts a new transaction.</span></span> <span data-ttu-id="bec43-115">すべてのプロバイダーは、これをサポートします。</span><span class="sxs-lookup"><span data-stu-id="bec43-115">Not all providers support this.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="bec43-116">ADO/WFC に相当</span><span class="sxs-lookup"><span data-stu-id="bec43-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="bec43-117">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="bec43-117">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bec43-118">定数</span><span class="sxs-lookup"><span data-stu-id="bec43-118">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bec43-119">AdoEnums.XactAttribute.ABORTRETAINING</span><span class="sxs-lookup"><span data-stu-id="bec43-119">AdoEnums.XactAttribute.ABORTRETAINING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bec43-120">AdoEnums.XactAttribute.COMMITRETAINING</span><span class="sxs-lookup"><span data-stu-id="bec43-120">AdoEnums.XactAttribute.COMMITRETAINING</span></span></p></td>
</tr>
</tbody>
</table>

