---
title: ConnectModeEnum (デスクトップ データベース参照のアクセス)
TOCTitle: ConnectModeEnum
ms:assetid: a15aa733-f899-5fe9-e705-67a4301706d1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249743(v=office.15)
ms:contentKeyID: 48546728
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5b39fc42259a1906891b82bf9b9ef252997e6240
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479106"
---
# <a name="connectmodeenum"></a><span data-ttu-id="cdd85-102">ConnectModeEnum</span><span class="sxs-lookup"><span data-stu-id="cdd85-102">ConnectModeEnum</span></span>


<span data-ttu-id="cdd85-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="cdd85-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="cdd85-104">[Connection](connection-object-ado.md) 内のデータの編集、 [Record](record-object-ado.md) のオープン、または [Record](mode-property-ado.md) および **Stream** オブジェクトの [Mode](stream-object-ado.md) プロパティの値の指定に対する権限を表します。</span><span class="sxs-lookup"><span data-stu-id="cdd85-104">Specifies the available permissions for modifying data in a [Connection](connection-object-ado.md), opening a [Record](record-object-ado.md), or specifying values for the [Mode](mode-property-ado.md) property of the **Record** and [Stream](stream-object-ado.md) objects.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cdd85-105">定数</span><span class="sxs-lookup"><span data-stu-id="cdd85-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="cdd85-106">値</span><span class="sxs-lookup"><span data-stu-id="cdd85-106">Value</span></span></p></th>
<th><p><span data-ttu-id="cdd85-107">説明</span><span class="sxs-lookup"><span data-stu-id="cdd85-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cdd85-108"><strong>adModeRead</strong></span><span class="sxs-lookup"><span data-stu-id="cdd85-108"><strong>adModeRead</strong></span></span></p></td>
<td><p><span data-ttu-id="cdd85-109">1</span><span class="sxs-lookup"><span data-stu-id="cdd85-109">1</span></span></p></td>
<td><p><span data-ttu-id="cdd85-110">読み取り専用の権限を表します。</span><span class="sxs-lookup"><span data-stu-id="cdd85-110">Indicates read-only permissions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdd85-111"><strong>adModeReadWrite</strong></span><span class="sxs-lookup"><span data-stu-id="cdd85-111"><strong>adModeReadWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="cdd85-112">3</span><span class="sxs-lookup"><span data-stu-id="cdd85-112">3</span></span></p></td>
<td><p><span data-ttu-id="cdd85-113">読み取り/書き込み両方の権限を表します。</span><span class="sxs-lookup"><span data-stu-id="cdd85-113">Indicates read/write permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdd85-114"><strong>adModeRecursive</strong></span><span class="sxs-lookup"><span data-stu-id="cdd85-114"><strong>adModeRecursive</strong></span></span></p></td>
<td><p><span data-ttu-id="cdd85-115">0x400000</span><span class="sxs-lookup"><span data-stu-id="cdd85-115">0x400000</span></span></p></td>
<td><p><span data-ttu-id="cdd85-116">(<strong>AdModeShareDenyNone</strong>、 <strong>adModeShareDenyWrite</strong>、または<strong>adModeShareDenyRead</strong>) サブのすべてのレコードをカレント<strong>レコード</strong>の共有の制限を適用するその他の<em>*ShareDeny*</em>値と組み合わせて使用します。</span><span class="sxs-lookup"><span data-stu-id="cdd85-116">Used in conjunction with the other <em>*ShareDeny*</em> values (<strong>adModeShareDenyNone</strong>, <strong>adModeShareDenyWrite</strong>, or <strong>adModeShareDenyRead</strong>) to propagate sharing restrictions to all sub-records of the current <strong>Record</strong>.</span></span> <span data-ttu-id="cdd85-117"><strong>レコード</strong>に子がない場合は影響ありません。</span><span class="sxs-lookup"><span data-stu-id="cdd85-117">It has no affect if the <strong>Record</strong> does not have any children.</span></span> <span data-ttu-id="cdd85-118"><strong>AdModeShareDenyNone</strong>のみで使用されている場合は、実行時エラーが生成されます。</span><span class="sxs-lookup"><span data-stu-id="cdd85-118">A run-time error is generated if it is used with <strong>adModeShareDenyNone</strong> only.</span></span> <span data-ttu-id="cdd85-119">ただし、 <strong>adModeShareDenyNone</strong>その他の値と組み合わせることで使用できます。</span><span class="sxs-lookup"><span data-stu-id="cdd85-119">However, it can be used with <strong>adModeShareDenyNone</strong> when combined with other values.</span></span> <span data-ttu-id="cdd85-120">たとえば、使用することができます&quot; <strong>adModeRead</strong>または<strong>adModeShareDenyNone</strong>または<strong>adModeRecursive</strong>&quot;。</span><span class="sxs-lookup"><span data-stu-id="cdd85-120">For example, you can use &quot;<strong>adModeRead</strong> Or <strong>adModeShareDenyNone</strong> Or <strong>adModeRecursive</strong>&quot;.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdd85-121"><strong>adModeShareDenyNone</strong></span><span class="sxs-lookup"><span data-stu-id="cdd85-121"><strong>adModeShareDenyNone</strong></span></span></p></td>
<td><p><span data-ttu-id="cdd85-122">16</span><span class="sxs-lookup"><span data-stu-id="cdd85-122">16</span></span></p></td>
<td><p><span data-ttu-id="cdd85-p102">権限の種類に関係なく、他のユーザーが接続を開けるようにします。他のユーザーに対して、読み取りと書き込みの両方のアクセスを許可します。</span><span class="sxs-lookup"><span data-stu-id="cdd85-p102">Allows others to open a connection with any permissions. Neither read nor write access can be denied to others.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdd85-125"><strong>adModeShareDenyRead</strong></span><span class="sxs-lookup"><span data-stu-id="cdd85-125"><strong>adModeShareDenyRead</strong></span></span></p></td>
<td><p><span data-ttu-id="cdd85-126">4</span><span class="sxs-lookup"><span data-stu-id="cdd85-126">4</span></span></p></td>
<td><p><span data-ttu-id="cdd85-127">他のユーザーが読み取り権限で接続を開くのを禁止します。</span><span class="sxs-lookup"><span data-stu-id="cdd85-127">Prevents others from opening a connection with read permissions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdd85-128"><strong>adModeShareDenyWrite</strong></span><span class="sxs-lookup"><span data-stu-id="cdd85-128"><strong>adModeShareDenyWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="cdd85-129">8</span><span class="sxs-lookup"><span data-stu-id="cdd85-129">8</span></span></p></td>
<td><p><span data-ttu-id="cdd85-130">他のユーザーが書き込み権限で接続を開くのを禁止します。</span><span class="sxs-lookup"><span data-stu-id="cdd85-130">Prevents others from opening a connection with write permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdd85-131"><strong>adModeShareExclusive</strong></span><span class="sxs-lookup"><span data-stu-id="cdd85-131"><strong>adModeShareExclusive</strong></span></span></p></td>
<td><p><span data-ttu-id="cdd85-132">12</span><span class="sxs-lookup"><span data-stu-id="cdd85-132">12</span></span></p></td>
<td><p><span data-ttu-id="cdd85-133">他のユーザーが接続を開くのを禁止します。</span><span class="sxs-lookup"><span data-stu-id="cdd85-133">Prevents others from opening a connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdd85-134"><strong>adModeUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="cdd85-134"><strong>adModeUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="cdd85-135">0</span><span class="sxs-lookup"><span data-stu-id="cdd85-135">0</span></span></p></td>
<td><p><span data-ttu-id="cdd85-p103">既定値。権限が設定されていないか、権限を判定できないことを示します。</span><span class="sxs-lookup"><span data-stu-id="cdd85-p103">Default. Indicates that the permissions have not yet been set or cannot be determined.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdd85-138"><strong>adModeWrite</strong></span><span class="sxs-lookup"><span data-stu-id="cdd85-138"><strong>adModeWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="cdd85-139">2</span><span class="sxs-lookup"><span data-stu-id="cdd85-139">2</span></span></p></td>
<td><p><span data-ttu-id="cdd85-140">書き込み専用の権限を示します。</span><span class="sxs-lookup"><span data-stu-id="cdd85-140">Indicates write-only permissions.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cdd85-141">**ADO/WFC 等価**</span><span class="sxs-lookup"><span data-stu-id="cdd85-141">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="cdd85-142">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="cdd85-142">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cdd85-143">定数</span><span class="sxs-lookup"><span data-stu-id="cdd85-143">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cdd85-144">AdoEnums.ConnectMode.READ</span><span class="sxs-lookup"><span data-stu-id="cdd85-144">AdoEnums.ConnectMode.READ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdd85-145">AdoEnums.ConnectMode.READWRITE</span><span class="sxs-lookup"><span data-stu-id="cdd85-145">AdoEnums.ConnectMode.READWRITE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdd85-146">(AdoEnums.ConnectMode.RECURSIVE と等価なものはありません)</span><span class="sxs-lookup"><span data-stu-id="cdd85-146">(There is no equivalent of AdoEnums.ConnectMode.RECURSIVE)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdd85-147">AdoEnums.ConnectMode.SHAREDENYNONE</span><span class="sxs-lookup"><span data-stu-id="cdd85-147">AdoEnums.ConnectMode.SHAREDENYNONE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdd85-148">AdoEnums.ConnectMode.SHAREDENYREAD</span><span class="sxs-lookup"><span data-stu-id="cdd85-148">AdoEnums.ConnectMode.SHAREDENYREAD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdd85-149">AdoEnums.ConnectMode.SHAREDENYWRITE</span><span class="sxs-lookup"><span data-stu-id="cdd85-149">AdoEnums.ConnectMode.SHAREDENYWRITE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdd85-150">AdoEnums.ConnectMode.SHAREEXCLUSIVE</span><span class="sxs-lookup"><span data-stu-id="cdd85-150">AdoEnums.ConnectMode.SHAREEXCLUSIVE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdd85-151">AdoEnums.ConnectMode.UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="cdd85-151">AdoEnums.ConnectMode.UNKNOWN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdd85-152">AdoEnums.ConnectMode.WRITE</span><span class="sxs-lookup"><span data-stu-id="cdd85-152">AdoEnums.ConnectMode.WRITE</span></span></p></td>
</tr>
</tbody>
</table>

