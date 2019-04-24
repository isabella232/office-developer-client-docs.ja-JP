---
title: connectmodeenum (Access デスクトップデータベースリファレンス)
TOCTitle: ConnectModeEnum
ms:assetid: a15aa733-f899-5fe9-e705-67a4301706d1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249743(v=office.15)
ms:contentKeyID: 48546728
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 453d84e687a31f7df5082e17b80fe2a1bda756be
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295696"
---
# <a name="connectmodeenum"></a><span data-ttu-id="7f88a-102">ConnectModeEnum</span><span class="sxs-lookup"><span data-stu-id="7f88a-102">ConnectModeEnum</span></span>

<span data-ttu-id="7f88a-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="7f88a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7f88a-104">[Connection](connection-object-ado.md) 内のデータの編集、[Record](record-object-ado.md) のオープン、または **Record** および [Stream](stream-object-ado.md) オブジェクトの [Mode](mode-property-ado.md) プロパティの値の指定に対する権限を表します。</span><span class="sxs-lookup"><span data-stu-id="7f88a-104">Specifies the available permissions for modifying data in a [Connection](connection-object-ado.md), opening a [Record](record-object-ado.md), or specifying values for the [Mode](mode-property-ado.md) property of the **Record** and [Stream](stream-object-ado.md) objects.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7f88a-105">定数</span><span class="sxs-lookup"><span data-stu-id="7f88a-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="7f88a-106">値</span><span class="sxs-lookup"><span data-stu-id="7f88a-106">Value</span></span></p></th>
<th><p><span data-ttu-id="7f88a-107">説明</span><span class="sxs-lookup"><span data-stu-id="7f88a-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7f88a-108"><strong>admoderead です</strong></span><span class="sxs-lookup"><span data-stu-id="7f88a-108"><strong>adModeRead</strong></span></span></p></td>
<td><p><span data-ttu-id="7f88a-109">1-d</span><span class="sxs-lookup"><span data-stu-id="7f88a-109">1</span></span></p></td>
<td><p><span data-ttu-id="7f88a-110">読み取り専用の権限を表します。</span><span class="sxs-lookup"><span data-stu-id="7f88a-110">Indicates read-only permissions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f88a-111"><strong>adModeReadWrite</strong></span><span class="sxs-lookup"><span data-stu-id="7f88a-111"><strong>adModeReadWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="7f88a-112">1/3</span><span class="sxs-lookup"><span data-stu-id="7f88a-112">3</span></span></p></td>
<td><p><span data-ttu-id="7f88a-113">読み取り/書き込み両方の権限を表します。</span><span class="sxs-lookup"><span data-stu-id="7f88a-113">Indicates read/write permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f88a-114"><strong>adModeRecursive</strong></span><span class="sxs-lookup"><span data-stu-id="7f88a-114"><strong>adModeRecursive</strong></span></span></p></td>
<td><p><span data-ttu-id="7f88a-115">0x400000</span><span class="sxs-lookup"><span data-stu-id="7f88a-115">0x400000</span></span></p></td>
<td><p><span data-ttu-id="7f88a-116">他の共有<em>*拒否*</em>値 (<strong>adModeShareDenyNone</strong>、 <strong>adModeShareDenyWrite</strong>、または<strong>adModeShareDenyRead</strong>) と共に使用して、現在の<strong>レコード</strong>のすべてのサブレコードに共有制限を伝達します。</span><span class="sxs-lookup"><span data-stu-id="7f88a-116">Used in conjunction with the other <em>*ShareDeny*</em> values (<strong>adModeShareDenyNone</strong>, <strong>adModeShareDenyWrite</strong>, or <strong>adModeShareDenyRead</strong>) to propagate sharing restrictions to all sub-records of the current <strong>Record</strong>.</span></span> <span data-ttu-id="7f88a-117"><strong>Record</strong> に子がない場合は機能しません。</span><span class="sxs-lookup"><span data-stu-id="7f88a-117">It has no affect if the <strong>Record</strong> does not have any children.</span></span></p><p><span data-ttu-id="7f88a-118"><strong>adModeShareDenyNone</strong> のみと組み合わせて使用すると、実行時エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="7f88a-118">A run-time error is generated if it is used with <strong>adModeShareDenyNone</strong> only.</span></span> <span data-ttu-id="7f88a-119">ただし、その他の値と組み合わせた場合は <strong>adModeShareDenyNone</strong> と組み合わせて使用できます。</span><span class="sxs-lookup"><span data-stu-id="7f88a-119">However, it can be used with <strong>adModeShareDenyNone</strong> when combined with other values.</span></span> <span data-ttu-id="7f88a-120">たとえば、 &quot; <strong>admoderead です</strong>または<strong>adModeShareDenyNone</strong>または<strong>adModeRecursive</strong>&quot;を使用できます。</span><span class="sxs-lookup"><span data-stu-id="7f88a-120">For example, you can use &quot;<strong>adModeRead</strong> or <strong>adModeShareDenyNone</strong> or <strong>adModeRecursive</strong>&quot;.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f88a-121"><strong>adModeShareDenyNone</strong></span><span class="sxs-lookup"><span data-stu-id="7f88a-121"><strong>adModeShareDenyNone</strong></span></span></p></td>
<td><p><span data-ttu-id="7f88a-122">16</span><span class="sxs-lookup"><span data-stu-id="7f88a-122">16</span></span></p></td>
<td><p><span data-ttu-id="7f88a-p103">権限の種類に関係なく、他のユーザーが接続を開けるようにします。他のユーザーに対して、読み取りと書き込みの両方のアクセスを許可します。</span><span class="sxs-lookup"><span data-stu-id="7f88a-p103">Allows others to open a connection with any permissions. Neither read nor write access can be denied to others.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f88a-125"><strong>adModeShareDenyRead</strong></span><span class="sxs-lookup"><span data-stu-id="7f88a-125"><strong>adModeShareDenyRead</strong></span></span></p></td>
<td><p><span data-ttu-id="7f88a-126">2/4</span><span class="sxs-lookup"><span data-stu-id="7f88a-126">4</span></span></p></td>
<td><p><span data-ttu-id="7f88a-127">他のユーザーが読み取り権限で接続を開くのを禁止します。</span><span class="sxs-lookup"><span data-stu-id="7f88a-127">Prevents others from opening a connection with read permissions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f88a-128"><strong>adModeShareDenyWrite</strong></span><span class="sxs-lookup"><span data-stu-id="7f88a-128"><strong>adModeShareDenyWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="7f88a-129">~</span><span class="sxs-lookup"><span data-stu-id="7f88a-129">8</span></span></p></td>
<td><p><span data-ttu-id="7f88a-130">他のユーザーが書き込み権限で接続を開くのを禁止します。</span><span class="sxs-lookup"><span data-stu-id="7f88a-130">Prevents others from opening a connection with write permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f88a-131"><strong>adModeShareExclusive</strong></span><span class="sxs-lookup"><span data-stu-id="7f88a-131"><strong>adModeShareExclusive</strong></span></span></p></td>
<td><p><span data-ttu-id="7f88a-132">個</span><span class="sxs-lookup"><span data-stu-id="7f88a-132">12</span></span></p></td>
<td><p><span data-ttu-id="7f88a-133">他のユーザーが接続を開くのを禁止します。</span><span class="sxs-lookup"><span data-stu-id="7f88a-133">Prevents others from opening a connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f88a-134"><strong>admodeunknown です</strong></span><span class="sxs-lookup"><span data-stu-id="7f88a-134"><strong>adModeUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="7f88a-135">.0</span><span class="sxs-lookup"><span data-stu-id="7f88a-135">0</span></span></p></td>
<td><p><span data-ttu-id="7f88a-p104">既定値。権限が設定されていないか、権限を判定できないことを示します。</span><span class="sxs-lookup"><span data-stu-id="7f88a-p104">Default. Indicates that the permissions have not yet been set or cannot be determined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f88a-138"><strong>admodewrite</strong></span><span class="sxs-lookup"><span data-stu-id="7f88a-138"><strong>adModeWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="7f88a-139">pbm-2</span><span class="sxs-lookup"><span data-stu-id="7f88a-139">2</span></span></p></td>
<td><p><span data-ttu-id="7f88a-140">書き込み専用の権限を示します。</span><span class="sxs-lookup"><span data-stu-id="7f88a-140">Indicates write-only permissions.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="7f88a-141">ADO/WFC と同等</span><span class="sxs-lookup"><span data-stu-id="7f88a-141">ADO/WFC equivalent</span></span>

<span data-ttu-id="7f88a-142">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="7f88a-142">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7f88a-143">定数</span><span class="sxs-lookup"><span data-stu-id="7f88a-143">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7f88a-144">AdoEnums モード。読み取り</span><span class="sxs-lookup"><span data-stu-id="7f88a-144">AdoEnums.ConnectMode.READ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f88a-145">AdoEnums の読み取りモード</span><span class="sxs-lookup"><span data-stu-id="7f88a-145">AdoEnums.ConnectMode.READWRITE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f88a-146">(AdoEnums.ConnectMode.RECURSIVE と等価なものはありません)</span><span class="sxs-lookup"><span data-stu-id="7f88a-146">(There is no equivalent of AdoEnums.ConnectMode.RECURSIVE)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f88a-147">AdoEnums を1つにします。</span><span class="sxs-lookup"><span data-stu-id="7f88a-147">AdoEnums.ConnectMode.SHAREDENYNONE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f88a-148">AdoEnums (読み取り専用)</span><span class="sxs-lookup"><span data-stu-id="7f88a-148">AdoEnums.ConnectMode.SHAREDENYREAD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f88a-149">AdoEnums の読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="7f88a-149">AdoEnums.ConnectMode.SHAREDENYWRITE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f88a-150">AdoEnums 排他的</span><span class="sxs-lookup"><span data-stu-id="7f88a-150">AdoEnums.ConnectMode.SHAREEXCLUSIVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f88a-151">AdoEnums モードが不明です。</span><span class="sxs-lookup"><span data-stu-id="7f88a-151">AdoEnums.ConnectMode.UNKNOWN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f88a-152">AdoEnums の書き込み</span><span class="sxs-lookup"><span data-stu-id="7f88a-152">AdoEnums.ConnectMode.WRITE</span></span></p></td>
</tr>
</tbody>
</table>

