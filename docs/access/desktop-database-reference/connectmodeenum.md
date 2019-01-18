---
title: ConnectModeEnum (デスクトップ データベース参照のアクセス)
TOCTitle: ConnectModeEnum
ms:assetid: a15aa733-f899-5fe9-e705-67a4301706d1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249743(v=office.15)
ms:contentKeyID: 48546728
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 453d84e687a31f7df5082e17b80fe2a1bda756be
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708663"
---
# <a name="connectmodeenum"></a><span data-ttu-id="12dbb-102">ConnectModeEnum</span><span class="sxs-lookup"><span data-stu-id="12dbb-102">ConnectModeEnum</span></span>

<span data-ttu-id="12dbb-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="12dbb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="12dbb-104">[Connection](connection-object-ado.md) 内のデータの編集、 [Record](record-object-ado.md) のオープン、または [Record](mode-property-ado.md) および **Stream** オブジェクトの [Mode](stream-object-ado.md) プロパティの値の指定に対する権限を表します。</span><span class="sxs-lookup"><span data-stu-id="12dbb-104">Specifies the available permissions for modifying data in a [Connection](connection-object-ado.md), opening a [Record](record-object-ado.md), or specifying values for the [Mode](mode-property-ado.md) property of the **Record** and [Stream](stream-object-ado.md) objects.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="12dbb-105">定数</span><span class="sxs-lookup"><span data-stu-id="12dbb-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="12dbb-106">値</span><span class="sxs-lookup"><span data-stu-id="12dbb-106">Value</span></span></p></th>
<th><p><span data-ttu-id="12dbb-107">説明</span><span class="sxs-lookup"><span data-stu-id="12dbb-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="12dbb-108"><strong>adModeRead</strong></span><span class="sxs-lookup"><span data-stu-id="12dbb-108"><strong>adModeRead</strong></span></span></p></td>
<td><p><span data-ttu-id="12dbb-109">1</span><span class="sxs-lookup"><span data-stu-id="12dbb-109">1</span></span></p></td>
<td><p><span data-ttu-id="12dbb-110">読み取り専用の権限を表します。</span><span class="sxs-lookup"><span data-stu-id="12dbb-110">Indicates read-only permissions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12dbb-111"><strong>adModeReadWrite</strong></span><span class="sxs-lookup"><span data-stu-id="12dbb-111"><strong>adModeReadWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="12dbb-112">3</span><span class="sxs-lookup"><span data-stu-id="12dbb-112">3</span></span></p></td>
<td><p><span data-ttu-id="12dbb-113">読み取り/書き込み両方の権限を表します。</span><span class="sxs-lookup"><span data-stu-id="12dbb-113">Indicates read/write permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12dbb-114"><strong>adModeRecursive</strong></span><span class="sxs-lookup"><span data-stu-id="12dbb-114"><strong>adModeRecursive</strong></span></span></p></td>
<td><p><span data-ttu-id="12dbb-115">0x400000</span><span class="sxs-lookup"><span data-stu-id="12dbb-115">0x400000</span></span></p></td>
<td><p><span data-ttu-id="12dbb-116">(<strong>AdModeShareDenyNone</strong>、 <strong>adModeShareDenyWrite</strong>、または<strong>adModeShareDenyRead</strong>) サブのすべてのレコードをカレント<strong>レコード</strong>の共有の制限を適用するその他の<em>*ShareDeny*</em>値と組み合わせて使用します。</span><span class="sxs-lookup"><span data-stu-id="12dbb-116">Used in conjunction with the other <em>*ShareDeny*</em> values (<strong>adModeShareDenyNone</strong>, <strong>adModeShareDenyWrite</strong>, or <strong>adModeShareDenyRead</strong>) to propagate sharing restrictions to all sub-records of the current <strong>Record</strong>.</span></span> <span data-ttu-id="12dbb-117"><strong>レコード</strong>に子がない場合は影響ありません。</span><span class="sxs-lookup"><span data-stu-id="12dbb-117">It has no affect if the <strong>Record</strong> does not have any children.</span></span></p><p><span data-ttu-id="12dbb-118"><strong>AdModeShareDenyNone</strong>のみで使用されている場合は、実行時エラーが生成されます。</span><span class="sxs-lookup"><span data-stu-id="12dbb-118">A run-time error is generated if it is used with <strong>adModeShareDenyNone</strong> only.</span></span> <span data-ttu-id="12dbb-119">ただし、 <strong>adModeShareDenyNone</strong>その他の値と組み合わせることで使用できます。</span><span class="sxs-lookup"><span data-stu-id="12dbb-119">However, it can be used with <strong>adModeShareDenyNone</strong> when combined with other values.</span></span> <span data-ttu-id="12dbb-120">たとえば、使用することができます&quot; <strong>adModeRead</strong>または<strong>adModeShareDenyNone</strong>または<strong>adModeRecursive</strong>&quot;。</span><span class="sxs-lookup"><span data-stu-id="12dbb-120">For example, you can use &quot;<strong>adModeRead</strong> or <strong>adModeShareDenyNone</strong> or <strong>adModeRecursive</strong>&quot;.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12dbb-121"><strong>adModeShareDenyNone</strong></span><span class="sxs-lookup"><span data-stu-id="12dbb-121"><strong>adModeShareDenyNone</strong></span></span></p></td>
<td><p><span data-ttu-id="12dbb-122">16</span><span class="sxs-lookup"><span data-stu-id="12dbb-122">16</span></span></p></td>
<td><p><span data-ttu-id="12dbb-p103">権限の種類に関係なく、他のユーザーが接続を開けるようにします。他のユーザーに対して、読み取りと書き込みの両方のアクセスを許可します。</span><span class="sxs-lookup"><span data-stu-id="12dbb-p103">Allows others to open a connection with any permissions. Neither read nor write access can be denied to others.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12dbb-125"><strong>adModeShareDenyRead</strong></span><span class="sxs-lookup"><span data-stu-id="12dbb-125"><strong>adModeShareDenyRead</strong></span></span></p></td>
<td><p><span data-ttu-id="12dbb-126">4</span><span class="sxs-lookup"><span data-stu-id="12dbb-126">4</span></span></p></td>
<td><p><span data-ttu-id="12dbb-127">他のユーザーが読み取り権限で接続を開くのを禁止します。</span><span class="sxs-lookup"><span data-stu-id="12dbb-127">Prevents others from opening a connection with read permissions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12dbb-128"><strong>adModeShareDenyWrite</strong></span><span class="sxs-lookup"><span data-stu-id="12dbb-128"><strong>adModeShareDenyWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="12dbb-129">8</span><span class="sxs-lookup"><span data-stu-id="12dbb-129">8</span></span></p></td>
<td><p><span data-ttu-id="12dbb-130">他のユーザーが書き込み権限で接続を開くのを禁止します。</span><span class="sxs-lookup"><span data-stu-id="12dbb-130">Prevents others from opening a connection with write permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12dbb-131"><strong>adModeShareExclusive</strong></span><span class="sxs-lookup"><span data-stu-id="12dbb-131"><strong>adModeShareExclusive</strong></span></span></p></td>
<td><p><span data-ttu-id="12dbb-132">12</span><span class="sxs-lookup"><span data-stu-id="12dbb-132">12</span></span></p></td>
<td><p><span data-ttu-id="12dbb-133">他のユーザーが接続を開くのを禁止します。</span><span class="sxs-lookup"><span data-stu-id="12dbb-133">Prevents others from opening a connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12dbb-134"><strong>adModeUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="12dbb-134"><strong>adModeUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="12dbb-135">0</span><span class="sxs-lookup"><span data-stu-id="12dbb-135">0</span></span></p></td>
<td><p><span data-ttu-id="12dbb-p104">既定値。権限が設定されていないか、権限を判定できないことを示します。</span><span class="sxs-lookup"><span data-stu-id="12dbb-p104">Default. Indicates that the permissions have not yet been set or cannot be determined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12dbb-138"><strong>adModeWrite</strong></span><span class="sxs-lookup"><span data-stu-id="12dbb-138"><strong>adModeWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="12dbb-139">2</span><span class="sxs-lookup"><span data-stu-id="12dbb-139">2</span></span></p></td>
<td><p><span data-ttu-id="12dbb-140">書き込み専用の権限を示します。</span><span class="sxs-lookup"><span data-stu-id="12dbb-140">Indicates write-only permissions.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="12dbb-141">ADO/WFC に相当</span><span class="sxs-lookup"><span data-stu-id="12dbb-141">ADO/WFC equivalent</span></span>

<span data-ttu-id="12dbb-142">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="12dbb-142">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="12dbb-143">定数</span><span class="sxs-lookup"><span data-stu-id="12dbb-143">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="12dbb-144">AdoEnums.ConnectMode.READ</span><span class="sxs-lookup"><span data-stu-id="12dbb-144">AdoEnums.ConnectMode.READ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12dbb-145">AdoEnums.ConnectMode.READWRITE</span><span class="sxs-lookup"><span data-stu-id="12dbb-145">AdoEnums.ConnectMode.READWRITE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12dbb-146">(AdoEnums.ConnectMode.RECURSIVE と等価なものはありません)</span><span class="sxs-lookup"><span data-stu-id="12dbb-146">(There is no equivalent of AdoEnums.ConnectMode.RECURSIVE)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12dbb-147">AdoEnums.ConnectMode.SHAREDENYNONE</span><span class="sxs-lookup"><span data-stu-id="12dbb-147">AdoEnums.ConnectMode.SHAREDENYNONE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12dbb-148">AdoEnums.ConnectMode.SHAREDENYREAD</span><span class="sxs-lookup"><span data-stu-id="12dbb-148">AdoEnums.ConnectMode.SHAREDENYREAD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12dbb-149">AdoEnums.ConnectMode.SHAREDENYWRITE</span><span class="sxs-lookup"><span data-stu-id="12dbb-149">AdoEnums.ConnectMode.SHAREDENYWRITE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12dbb-150">AdoEnums.ConnectMode.SHAREEXCLUSIVE</span><span class="sxs-lookup"><span data-stu-id="12dbb-150">AdoEnums.ConnectMode.SHAREEXCLUSIVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12dbb-151">AdoEnums.ConnectMode.UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="12dbb-151">AdoEnums.ConnectMode.UNKNOWN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12dbb-152">AdoEnums.ConnectMode.WRITE</span><span class="sxs-lookup"><span data-stu-id="12dbb-152">AdoEnums.ConnectMode.WRITE</span></span></p></td>
</tr>
</tbody>
</table>

