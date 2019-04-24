---
title: XactAttributeEnum (Access デスクトップデータベースリファレンス)
TOCTitle: XactAttributeEnum
ms:assetid: 9206698b-7cfa-1229-2701-f2b6949e54fc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249643(v=office.15)
ms:contentKeyID: 48546366
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e79a6143c65637660b2d59b7c7efb6a21e8935bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302570"
---
# <a name="xactattributeenum"></a><span data-ttu-id="7e9c0-102">XactAttributeEnum</span><span class="sxs-lookup"><span data-stu-id="7e9c0-102">XactAttributeEnum</span></span>

<span data-ttu-id="7e9c0-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="7e9c0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7e9c0-104">[Connection](connection-object-ado.md) オブジェクトのトランザクション属性を表します。</span><span class="sxs-lookup"><span data-stu-id="7e9c0-104">Specifies the transaction attributes of a [Connection](connection-object-ado.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7e9c0-105">定数</span><span class="sxs-lookup"><span data-stu-id="7e9c0-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="7e9c0-106">値</span><span class="sxs-lookup"><span data-stu-id="7e9c0-106">Value</span></span></p></th>
<th><p><span data-ttu-id="7e9c0-107">説明</span><span class="sxs-lookup"><span data-stu-id="7e9c0-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7e9c0-108"><strong>adXactAbortRetaining</strong></span><span class="sxs-lookup"><span data-stu-id="7e9c0-108"><strong>adXactAbortRetaining</strong></span></span></p></td>
<td><p><span data-ttu-id="7e9c0-109">262144</span><span class="sxs-lookup"><span data-stu-id="7e9c0-109">262144</span></span></p></td>
<td><p><span data-ttu-id="7e9c0-110">中断の保持を実行します。つまり、 <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">RollbackTrans</a>を呼び出すと、新しいトランザクションが自動的に開始されます。</span><span class="sxs-lookup"><span data-stu-id="7e9c0-110">Performs retaining aborts; that is, calling <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">RollbackTrans</a> automatically starts a new transaction.</span></span> <span data-ttu-id="7e9c0-111">この設定をサポートしていないプロバイダーもあります。</span><span class="sxs-lookup"><span data-stu-id="7e9c0-111">Not all providers support this.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e9c0-112"><strong>adXactCommitRetaining</strong></span><span class="sxs-lookup"><span data-stu-id="7e9c0-112"><strong>adXactCommitRetaining</strong></span></span></p></td>
<td><p><span data-ttu-id="7e9c0-113">131072</span><span class="sxs-lookup"><span data-stu-id="7e9c0-113">131072</span></span></p></td>
<td><p><span data-ttu-id="7e9c0-114">保持コミットを実行します。つまり、 <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">CommitTrans</a>を呼び出すと、新しいトランザクションが自動的に開始されます。</span><span class="sxs-lookup"><span data-stu-id="7e9c0-114">Performs retaining commits; that is, calling <a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">CommitTrans</a> automatically starts a new transaction.</span></span> <span data-ttu-id="7e9c0-115">この設定をサポートしていないプロバイダーもあります。</span><span class="sxs-lookup"><span data-stu-id="7e9c0-115">Not all providers support this.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="7e9c0-116">ADO/WFC と同等</span><span class="sxs-lookup"><span data-stu-id="7e9c0-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="7e9c0-117">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="7e9c0-117">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7e9c0-118">定数</span><span class="sxs-lookup"><span data-stu-id="7e9c0-118">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7e9c0-119">XactAttribute 保持 AdoEnums</span><span class="sxs-lookup"><span data-stu-id="7e9c0-119">AdoEnums.XactAttribute.ABORTRETAINING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e9c0-120">AdoEnums XactAttribute</span><span class="sxs-lookup"><span data-stu-id="7e9c0-120">AdoEnums.XactAttribute.COMMITRETAINING</span></span></p></td>
</tr>
</tbody>
</table>

