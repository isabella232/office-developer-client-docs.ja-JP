---
title: RightsEnum (デスクトップ データベース参照のアクセス)
TOCTitle: RightsEnum
ms:assetid: 7647b9d5-5271-fdcf-489d-5a8beb931ca5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249485(v=office.15)
ms:contentKeyID: 48545693
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 535c80bf5cd3dbfecae0e004082ce20d01c31fde
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877388"
---
# <a name="rightsenum"></a><span data-ttu-id="83fe6-102">RightsEnum</span><span class="sxs-lookup"><span data-stu-id="83fe6-102">RightsEnum</span></span>

<span data-ttu-id="83fe6-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="83fe6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="83fe6-104">オブジェクトに対するグループまたはユーザーの権限を指定します。</span><span class="sxs-lookup"><span data-stu-id="83fe6-104">Specifies the rights or permissions for a group or user on an object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="83fe6-105">定数</span><span class="sxs-lookup"><span data-stu-id="83fe6-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="83fe6-106">値</span><span class="sxs-lookup"><span data-stu-id="83fe6-106">Value</span></span></p></th>
<th><p><span data-ttu-id="83fe6-107">説明</span><span class="sxs-lookup"><span data-stu-id="83fe6-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="83fe6-108"><strong>adRightCreate</strong></span><span class="sxs-lookup"><span data-stu-id="83fe6-108"><strong>adRightCreate</strong></span></span></p></td>
<td><p><span data-ttu-id="83fe6-109">16384</span><span class="sxs-lookup"><span data-stu-id="83fe6-109">16384</span></span><br />
<span data-ttu-id="83fe6-110">(&amp;H4000)</span><span class="sxs-lookup"><span data-stu-id="83fe6-110">(&amp;H4000)</span></span></p></td>
<td><p><span data-ttu-id="83fe6-111">ユーザーまたはグループは、この種類の新規オブジェクトを作成する権限を持っています。</span><span class="sxs-lookup"><span data-stu-id="83fe6-111">The user or group has permission to create new objects of this type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83fe6-112"><strong>adRightDelete</strong></span><span class="sxs-lookup"><span data-stu-id="83fe6-112"><strong>adRightDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="83fe6-113">65536</span><span class="sxs-lookup"><span data-stu-id="83fe6-113">65536</span></span><br />
<span data-ttu-id="83fe6-114">(&amp;H10000)</span><span class="sxs-lookup"><span data-stu-id="83fe6-114">(&amp;H10000)</span></span></p></td>
<td><p><span data-ttu-id="83fe6-p101">ユーザーまたはグループは、オブジェクトからデータを削除する権限を持っています。<strong>Tables</strong> などのオブジェクトでは、ユーザーはレコードからデータ値を削除する権限を持っています。</span><span class="sxs-lookup"><span data-stu-id="83fe6-p101">The user or group has permission to delete data from an object. For objects such as <strong>Tables</strong>, the user has permission to delete data values from records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83fe6-117"><strong>adRightDrop</strong></span><span class="sxs-lookup"><span data-stu-id="83fe6-117"><strong>adRightDrop</strong></span></span></p></td>
<td><p><span data-ttu-id="83fe6-118">256</span><span class="sxs-lookup"><span data-stu-id="83fe6-118">256</span></span><br />
<span data-ttu-id="83fe6-119">(&amp;H100)</span><span class="sxs-lookup"><span data-stu-id="83fe6-119">(&amp;H100)</span></span></p></td>
<td><p><span data-ttu-id="83fe6-p102">ユーザーまたはグループは、カタログからオブジェクトを削除する権限を持っています。たとえば、<strong>Tables</strong> を DROP TABLE SQL コマンドによって削除できます。</span><span class="sxs-lookup"><span data-stu-id="83fe6-p102">The user or group has permission to remove objects from the catalog. For example, <strong>Tables</strong> can be deleted by a DROP TABLE SQL command.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83fe6-122"><strong>adRightExclusive</strong></span><span class="sxs-lookup"><span data-stu-id="83fe6-122"><strong>adRightExclusive</strong></span></span></p></td>
<td><p><span data-ttu-id="83fe6-123">512</span><span class="sxs-lookup"><span data-stu-id="83fe6-123">512</span></span><br />
<span data-ttu-id="83fe6-124">(&amp;H200)</span><span class="sxs-lookup"><span data-stu-id="83fe6-124">(&amp;H200)</span></span></p></td>
<td><p><span data-ttu-id="83fe6-125">ユーザーまたはグループは、排他的にオブジェクトにアクセスする権限を持っています。</span><span class="sxs-lookup"><span data-stu-id="83fe6-125">The user or group has permission to access the object exclusively.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83fe6-126"><strong>adRightExecute</strong></span><span class="sxs-lookup"><span data-stu-id="83fe6-126"><strong>adRightExecute</strong></span></span></p></td>
<td><p><span data-ttu-id="83fe6-127">536870912</span><span class="sxs-lookup"><span data-stu-id="83fe6-127">536870912</span></span><br />
<span data-ttu-id="83fe6-128">(&amp;H20000000)</span><span class="sxs-lookup"><span data-stu-id="83fe6-128">(&amp;H20000000)</span></span></p></td>
<td><p><span data-ttu-id="83fe6-129">ユーザーまたはグループは、オブジェクトを実行する権限を持っています。</span><span class="sxs-lookup"><span data-stu-id="83fe6-129">The user or group has permission to execute the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83fe6-130"><strong>adRightFull</strong></span><span class="sxs-lookup"><span data-stu-id="83fe6-130"><strong>adRightFull</strong></span></span></p></td>
<td><p><span data-ttu-id="83fe6-131">268435456</span><span class="sxs-lookup"><span data-stu-id="83fe6-131">268435456</span></span><br />
<span data-ttu-id="83fe6-132">(&amp;H10000000)</span><span class="sxs-lookup"><span data-stu-id="83fe6-132">(&amp;H10000000)</span></span></p></td>
<td><p><span data-ttu-id="83fe6-133">ユーザーまたはグループは、オブジェクトに対するすべての権限を持っています。</span><span class="sxs-lookup"><span data-stu-id="83fe6-133">The user or group has all permissions on the object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83fe6-134"><strong>adRightInsert</strong></span><span class="sxs-lookup"><span data-stu-id="83fe6-134"><strong>adRightInsert</strong></span></span></p></td>
<td><p><span data-ttu-id="83fe6-135">32768</span><span class="sxs-lookup"><span data-stu-id="83fe6-135">32768</span></span><br />
<span data-ttu-id="83fe6-136">(&amp;H8000)</span><span class="sxs-lookup"><span data-stu-id="83fe6-136">(&amp;H8000)</span></span></p></td>
<td><p><span data-ttu-id="83fe6-p103">ユーザーまたはグループは、オブジェクトを挿入する権限を持っています。<strong>Tables</strong> などのオブジェクトでは、ユーザーはデータをテーブルに挿入する権限を持っています。</span><span class="sxs-lookup"><span data-stu-id="83fe6-p103">The user or group has permission to insert the object. For objects such as <strong>Tables</strong>, the user has permission to insert data into the table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83fe6-139"><strong>adRightMaximumAllowed</strong></span><span class="sxs-lookup"><span data-stu-id="83fe6-139"><strong>adRightMaximumAllowed</strong></span></span></p></td>
<td><p><span data-ttu-id="83fe6-140">33554432 (&amp;H2000000)</span><span class="sxs-lookup"><span data-stu-id="83fe6-140">33554432 (&amp;H2000000)</span></span></p></td>
<td><p><span data-ttu-id="83fe6-p104">ユーザーまたはグループは、プロバイダーによって許可される最大数の権限を持っています。指定される権限は、プロバイダーの設定によって決まります。</span><span class="sxs-lookup"><span data-stu-id="83fe6-p104">The user or group has the maximum number of permissions allowed by the provider. Specific permissions are provider-dependent.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83fe6-143"><strong>adRightNone</strong></span><span class="sxs-lookup"><span data-stu-id="83fe6-143"><strong>adRightNone</strong></span></span></p></td>
<td><p><span data-ttu-id="83fe6-144">0</span><span class="sxs-lookup"><span data-stu-id="83fe6-144">0</span></span></p></td>
<td><p><span data-ttu-id="83fe6-145">ユーザーまたはグループは、オブジェクトに対する権限を持ちません。</span><span class="sxs-lookup"><span data-stu-id="83fe6-145">The user or group has no permissions for the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83fe6-146"><strong>adRightRead</strong></span><span class="sxs-lookup"><span data-stu-id="83fe6-146"><strong>adRightRead</strong></span></span></p></td>
<td><p><span data-ttu-id="83fe6-147">-2147483648</span><span class="sxs-lookup"><span data-stu-id="83fe6-147">-2147483648</span></span><br />
<span data-ttu-id="83fe6-148">(&amp;H80000000)</span><span class="sxs-lookup"><span data-stu-id="83fe6-148">(&amp;H80000000)</span></span></p></td>
<td><p><span data-ttu-id="83fe6-p105">ユーザーまたはグループは、オブジェクトを読み取る権限を持っています。<a href="table-object-adox.md">Tables</a> などのオブジェクトでは、ユーザーはテーブル内のデータを読み取る権限を持っています。</span><span class="sxs-lookup"><span data-stu-id="83fe6-p105">The user or group has permission to read the object. For objects such as <a href="table-object-adox.md">Tables</a>, the user has permission to read the data in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83fe6-151"><strong>adRightReadDesign</strong></span><span class="sxs-lookup"><span data-stu-id="83fe6-151"><strong>adRightReadDesign</strong></span></span></p></td>
<td><p><span data-ttu-id="83fe6-152">1024</span><span class="sxs-lookup"><span data-stu-id="83fe6-152">1024</span></span><br />
<span data-ttu-id="83fe6-153">(&amp;H400)</span><span class="sxs-lookup"><span data-stu-id="83fe6-153">(&amp;H400)</span></span></p></td>
<td><p><span data-ttu-id="83fe6-154">ユーザーまたはグループは、オブジェクトのデザインを読み取る権限を持っています。</span><span class="sxs-lookup"><span data-stu-id="83fe6-154">The user or group has permission to read the design for the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83fe6-155"><strong>adRightReadPermissions</strong></span><span class="sxs-lookup"><span data-stu-id="83fe6-155"><strong>adRightReadPermissions</strong></span></span></p></td>
<td><p><span data-ttu-id="83fe6-156">131072</span><span class="sxs-lookup"><span data-stu-id="83fe6-156">131072</span></span><br />
<span data-ttu-id="83fe6-157">(&amp;H20000)</span><span class="sxs-lookup"><span data-stu-id="83fe6-157">(&amp;H20000)</span></span></p></td>
<td><p><span data-ttu-id="83fe6-158">ユーザーまたはグループは、カタログ内のオブジェクトの特定の権限を表示することができますが、変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="83fe6-158">The user or group can view, but not change, the specific permissions for an object in the catalog.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83fe6-159"><strong>adRightReference</strong></span><span class="sxs-lookup"><span data-stu-id="83fe6-159"><strong>adRightReference</strong></span></span></p></td>
<td><p><span data-ttu-id="83fe6-160">8192</span><span class="sxs-lookup"><span data-stu-id="83fe6-160">8192</span></span><br />
<span data-ttu-id="83fe6-161">(&amp;H2000)</span><span class="sxs-lookup"><span data-stu-id="83fe6-161">(&amp;H2000)</span></span></p></td>
<td><p><span data-ttu-id="83fe6-162">ユーザーまたはグループは、オブジェクトを参照する権限を持っています。</span><span class="sxs-lookup"><span data-stu-id="83fe6-162">The user or group has permission to reference the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83fe6-163"><strong>adRightUpdate</strong></span><span class="sxs-lookup"><span data-stu-id="83fe6-163"><strong>adRightUpdate</strong></span></span></p></td>
<td><p><span data-ttu-id="83fe6-164">1073741824</span><span class="sxs-lookup"><span data-stu-id="83fe6-164">1073741824</span></span><br />
<span data-ttu-id="83fe6-165">(&amp;H40000000)</span><span class="sxs-lookup"><span data-stu-id="83fe6-165">(&amp;H40000000)</span></span></p></td>
<td><p><span data-ttu-id="83fe6-p106">ユーザーまたはグループは、オブジェクトを更新する権限を持っています。<strong>Tables</strong> などのオブジェクトでは、ユーザーはテーブル内のデータを更新する権限を持っています。</span><span class="sxs-lookup"><span data-stu-id="83fe6-p106">The user or group has permission to update the object. For objects such as <strong>Tables</strong>, the user has permission to update the data in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83fe6-168"><strong>adRightWithGrant</strong></span><span class="sxs-lookup"><span data-stu-id="83fe6-168"><strong>adRightWithGrant</strong></span></span></p></td>
<td><p><span data-ttu-id="83fe6-169">4096</span><span class="sxs-lookup"><span data-stu-id="83fe6-169">4096</span></span><br />
<span data-ttu-id="83fe6-170">(&amp;H1000)</span><span class="sxs-lookup"><span data-stu-id="83fe6-170">(&amp;H1000)</span></span></p></td>
<td><p><span data-ttu-id="83fe6-171">ユーザーまたはグループは、オブジェクトに対する権限を与える権限を持っています。</span><span class="sxs-lookup"><span data-stu-id="83fe6-171">The user or group has permission to grant permissions on the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83fe6-172"><strong>adRightWriteDesign</strong></span><span class="sxs-lookup"><span data-stu-id="83fe6-172"><strong>adRightWriteDesign</strong></span></span></p></td>
<td><p><span data-ttu-id="83fe6-173">2048</span><span class="sxs-lookup"><span data-stu-id="83fe6-173">2048</span></span><br />
<span data-ttu-id="83fe6-174">(&amp;H800)</span><span class="sxs-lookup"><span data-stu-id="83fe6-174">(&amp;H800)</span></span></p></td>
<td><p><span data-ttu-id="83fe6-175">ユーザーまたはグループは、オブジェクトのデザインを修正する権限を持っています。</span><span class="sxs-lookup"><span data-stu-id="83fe6-175">The user or group has permission to modify the design for the object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83fe6-176"><strong>adRightWriteOwner</strong></span><span class="sxs-lookup"><span data-stu-id="83fe6-176"><strong>adRightWriteOwner</strong></span></span></p></td>
<td><p><span data-ttu-id="83fe6-177">524288</span><span class="sxs-lookup"><span data-stu-id="83fe6-177">524288</span></span><br />
<span data-ttu-id="83fe6-178">(&amp;H80000)</span><span class="sxs-lookup"><span data-stu-id="83fe6-178">(&amp;H80000)</span></span></p></td>
<td><p><span data-ttu-id="83fe6-179">ユーザーまたはグループは、オブジェクトの所有者を変更する権限を持っています。</span><span class="sxs-lookup"><span data-stu-id="83fe6-179">The user or group has permission to modify the owner of the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83fe6-180"><strong>adRightWritePermissions</strong></span><span class="sxs-lookup"><span data-stu-id="83fe6-180"><strong>adRightWritePermissions</strong></span></span></p></td>
<td><p><span data-ttu-id="83fe6-181">262144</span><span class="sxs-lookup"><span data-stu-id="83fe6-181">262144</span></span><br />
<span data-ttu-id="83fe6-182">(&amp;H40000)</span><span class="sxs-lookup"><span data-stu-id="83fe6-182">(&amp;H40000)</span></span></p></td>
<td><p><span data-ttu-id="83fe6-183">ユーザーまたはグループは、カタログ内のオブジェクトに対する特定の権限を変更することができます。</span><span class="sxs-lookup"><span data-stu-id="83fe6-183">The user or group can modify the specific permissions for an object in the catalog.</span></span></p></td>
</tr>
</tbody>
</table>

