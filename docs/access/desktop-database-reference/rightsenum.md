---
title: RightsEnum (デスクトップ データベース参照のアクセス)
TOCTitle: RightsEnum
ms:assetid: 7647b9d5-5271-fdcf-489d-5a8beb931ca5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249485(v=office.15)
ms:contentKeyID: 48545693
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 40cd7f789461e5b354186c2d5b8f81ec18344435
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861982"
---
# <a name="rightsenum"></a><span data-ttu-id="77d4c-102">RightsEnum</span><span class="sxs-lookup"><span data-stu-id="77d4c-102">RightsEnum</span></span>

<span data-ttu-id="77d4c-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="77d4c-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="77d4c-104">オブジェクトに対するグループまたはユーザーの権限を指定します。</span><span class="sxs-lookup"><span data-stu-id="77d4c-104">Specifies the rights or permissions for a group or user on an object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="77d4c-105">定数</span><span class="sxs-lookup"><span data-stu-id="77d4c-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="77d4c-106">値</span><span class="sxs-lookup"><span data-stu-id="77d4c-106">Value</span></span></p></th>
<th><p><span data-ttu-id="77d4c-107">説明</span><span class="sxs-lookup"><span data-stu-id="77d4c-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="77d4c-108"><strong>adRightCreate</strong></span><span class="sxs-lookup"><span data-stu-id="77d4c-108"><strong>adRightCreate</strong></span></span></p></td>
<td><p><span data-ttu-id="77d4c-109">16384</span><span class="sxs-lookup"><span data-stu-id="77d4c-109">16384</span></span><br />
<span data-ttu-id="77d4c-110">(&amp;H4000)</span><span class="sxs-lookup"><span data-stu-id="77d4c-110">(&amp;H4000)</span></span></p></td>
<td><p><span data-ttu-id="77d4c-111">ユーザーまたはグループは、この種類の新規オブジェクトを作成する権限を持っています。</span><span class="sxs-lookup"><span data-stu-id="77d4c-111">The user or group has permission to create new objects of this type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77d4c-112"><strong>adRightDelete</strong></span><span class="sxs-lookup"><span data-stu-id="77d4c-112"><strong>adRightDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="77d4c-113">65536</span><span class="sxs-lookup"><span data-stu-id="77d4c-113">65536</span></span><br />
<span data-ttu-id="77d4c-114">(&amp;H10000)</span><span class="sxs-lookup"><span data-stu-id="77d4c-114">(&amp;H10000)</span></span></p></td>
<td><p><span data-ttu-id="77d4c-p101">ユーザーまたはグループは、オブジェクトからデータを削除する権限を持っています。<strong>Tables</strong> などのオブジェクトでは、ユーザーはレコードからデータ値を削除する権限を持っています。</span><span class="sxs-lookup"><span data-stu-id="77d4c-p101">The user or group has permission to delete data from an object. For objects such as <strong>Tables</strong>, the user has permission to delete data values from records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77d4c-117"><strong>adRightDrop</strong></span><span class="sxs-lookup"><span data-stu-id="77d4c-117"><strong>adRightDrop</strong></span></span></p></td>
<td><p><span data-ttu-id="77d4c-118">256</span><span class="sxs-lookup"><span data-stu-id="77d4c-118">256</span></span><br />
<span data-ttu-id="77d4c-119">(&amp;H100)</span><span class="sxs-lookup"><span data-stu-id="77d4c-119">(&amp;H100)</span></span></p></td>
<td><p><span data-ttu-id="77d4c-p102">ユーザーまたはグループは、カタログからオブジェクトを削除する権限を持っています。たとえば、<strong>Tables</strong> を DROP TABLE SQL コマンドによって削除できます。</span><span class="sxs-lookup"><span data-stu-id="77d4c-p102">The user or group has permission to remove objects from the catalog. For example, <strong>Tables</strong> can be deleted by a DROP TABLE SQL command.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77d4c-122"><strong>adRightExclusive</strong></span><span class="sxs-lookup"><span data-stu-id="77d4c-122"><strong>adRightExclusive</strong></span></span></p></td>
<td><p><span data-ttu-id="77d4c-123">512</span><span class="sxs-lookup"><span data-stu-id="77d4c-123">512</span></span><br />
<span data-ttu-id="77d4c-124">(&amp;H200)</span><span class="sxs-lookup"><span data-stu-id="77d4c-124">(&amp;H200)</span></span></p></td>
<td><p><span data-ttu-id="77d4c-125">ユーザーまたはグループは、排他的にオブジェクトにアクセスする権限を持っています。</span><span class="sxs-lookup"><span data-stu-id="77d4c-125">The user or group has permission to access the object exclusively.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77d4c-126"><strong>adRightExecute</strong></span><span class="sxs-lookup"><span data-stu-id="77d4c-126"><strong>adRightExecute</strong></span></span></p></td>
<td><p><span data-ttu-id="77d4c-127">536870912</span><span class="sxs-lookup"><span data-stu-id="77d4c-127">536870912</span></span><br />
<span data-ttu-id="77d4c-128">(&amp;H20000000)</span><span class="sxs-lookup"><span data-stu-id="77d4c-128">(&amp;H20000000)</span></span></p></td>
<td><p><span data-ttu-id="77d4c-129">ユーザーまたはグループは、オブジェクトを実行する権限を持っています。</span><span class="sxs-lookup"><span data-stu-id="77d4c-129">The user or group has permission to execute the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77d4c-130"><strong>adRightFull</strong></span><span class="sxs-lookup"><span data-stu-id="77d4c-130"><strong>adRightFull</strong></span></span></p></td>
<td><p><span data-ttu-id="77d4c-131">268435456</span><span class="sxs-lookup"><span data-stu-id="77d4c-131">268435456</span></span><br />
<span data-ttu-id="77d4c-132">(&amp;H10000000)</span><span class="sxs-lookup"><span data-stu-id="77d4c-132">(&amp;H10000000)</span></span></p></td>
<td><p><span data-ttu-id="77d4c-133">ユーザーまたはグループは、オブジェクトに対するすべての権限を持っています。</span><span class="sxs-lookup"><span data-stu-id="77d4c-133">The user or group has all permissions on the object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77d4c-134"><strong>adRightInsert</strong></span><span class="sxs-lookup"><span data-stu-id="77d4c-134"><strong>adRightInsert</strong></span></span></p></td>
<td><p><span data-ttu-id="77d4c-135">32768</span><span class="sxs-lookup"><span data-stu-id="77d4c-135">32768</span></span><br />
<span data-ttu-id="77d4c-136">(&amp;H8000)</span><span class="sxs-lookup"><span data-stu-id="77d4c-136">(&amp;H8000)</span></span></p></td>
<td><p><span data-ttu-id="77d4c-p103">ユーザーまたはグループは、オブジェクトを挿入する権限を持っています。<strong>Tables</strong> などのオブジェクトでは、ユーザーはデータをテーブルに挿入する権限を持っています。</span><span class="sxs-lookup"><span data-stu-id="77d4c-p103">The user or group has permission to insert the object. For objects such as <strong>Tables</strong>, the user has permission to insert data into the table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77d4c-139"><strong>adRightMaximumAllowed</strong></span><span class="sxs-lookup"><span data-stu-id="77d4c-139"><strong>adRightMaximumAllowed</strong></span></span></p></td>
<td><p><span data-ttu-id="77d4c-140">33554432 (&amp;H2000000)</span><span class="sxs-lookup"><span data-stu-id="77d4c-140">33554432 (&amp;H2000000)</span></span></p></td>
<td><p><span data-ttu-id="77d4c-p104">ユーザーまたはグループは、プロバイダーによって許可される最大数の権限を持っています。指定される権限は、プロバイダーの設定によって決まります。</span><span class="sxs-lookup"><span data-stu-id="77d4c-p104">The user or group has the maximum number of permissions allowed by the provider. Specific permissions are provider-dependent.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77d4c-143"><strong>adRightNone</strong></span><span class="sxs-lookup"><span data-stu-id="77d4c-143"><strong>adRightNone</strong></span></span></p></td>
<td><p><span data-ttu-id="77d4c-144">0</span><span class="sxs-lookup"><span data-stu-id="77d4c-144">0</span></span></p></td>
<td><p><span data-ttu-id="77d4c-145">ユーザーまたはグループは、オブジェクトに対する権限を持ちません。</span><span class="sxs-lookup"><span data-stu-id="77d4c-145">The user or group has no permissions for the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77d4c-146"><strong>adRightRead</strong></span><span class="sxs-lookup"><span data-stu-id="77d4c-146"><strong>adRightRead</strong></span></span></p></td>
<td><p><span data-ttu-id="77d4c-147">-2147483648</span><span class="sxs-lookup"><span data-stu-id="77d4c-147">-2147483648</span></span><br />
<span data-ttu-id="77d4c-148">(&amp;H80000000)</span><span class="sxs-lookup"><span data-stu-id="77d4c-148">(&amp;H80000000)</span></span></p></td>
<td><p><span data-ttu-id="77d4c-p105">ユーザーまたはグループは、オブジェクトを読み取る権限を持っています。<a href="table-object-adox.md">Tables</a> などのオブジェクトでは、ユーザーはテーブル内のデータを読み取る権限を持っています。</span><span class="sxs-lookup"><span data-stu-id="77d4c-p105">The user or group has permission to read the object. For objects such as <a href="table-object-adox.md">Tables</a>, the user has permission to read the data in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77d4c-151"><strong>adRightReadDesign</strong></span><span class="sxs-lookup"><span data-stu-id="77d4c-151"><strong>adRightReadDesign</strong></span></span></p></td>
<td><p><span data-ttu-id="77d4c-152">1024</span><span class="sxs-lookup"><span data-stu-id="77d4c-152">1024</span></span><br />
<span data-ttu-id="77d4c-153">(&amp;H400)</span><span class="sxs-lookup"><span data-stu-id="77d4c-153">(&amp;H400)</span></span></p></td>
<td><p><span data-ttu-id="77d4c-154">ユーザーまたはグループは、オブジェクトのデザインを読み取る権限を持っています。</span><span class="sxs-lookup"><span data-stu-id="77d4c-154">The user or group has permission to read the design for the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77d4c-155"><strong>adRightReadPermissions</strong></span><span class="sxs-lookup"><span data-stu-id="77d4c-155"><strong>adRightReadPermissions</strong></span></span></p></td>
<td><p><span data-ttu-id="77d4c-156">131072</span><span class="sxs-lookup"><span data-stu-id="77d4c-156">131072</span></span><br />
<span data-ttu-id="77d4c-157">(&amp;H20000)</span><span class="sxs-lookup"><span data-stu-id="77d4c-157">(&amp;H20000)</span></span></p></td>
<td><p><span data-ttu-id="77d4c-158">ユーザーまたはグループは、カタログ内のオブジェクトの特定の権限を表示することができますが、変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="77d4c-158">The user or group can view, but not change, the specific permissions for an object in the catalog.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77d4c-159"><strong>adRightReference</strong></span><span class="sxs-lookup"><span data-stu-id="77d4c-159"><strong>adRightReference</strong></span></span></p></td>
<td><p><span data-ttu-id="77d4c-160">8192</span><span class="sxs-lookup"><span data-stu-id="77d4c-160">8192</span></span><br />
<span data-ttu-id="77d4c-161">(&amp;H2000)</span><span class="sxs-lookup"><span data-stu-id="77d4c-161">(&amp;H2000)</span></span></p></td>
<td><p><span data-ttu-id="77d4c-162">ユーザーまたはグループは、オブジェクトを参照する権限を持っています。</span><span class="sxs-lookup"><span data-stu-id="77d4c-162">The user or group has permission to reference the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77d4c-163"><strong>adRightUpdate</strong></span><span class="sxs-lookup"><span data-stu-id="77d4c-163"><strong>adRightUpdate</strong></span></span></p></td>
<td><p><span data-ttu-id="77d4c-164">1073741824</span><span class="sxs-lookup"><span data-stu-id="77d4c-164">1073741824</span></span><br />
<span data-ttu-id="77d4c-165">(&amp;H40000000)</span><span class="sxs-lookup"><span data-stu-id="77d4c-165">(&amp;H40000000)</span></span></p></td>
<td><p><span data-ttu-id="77d4c-p106">ユーザーまたはグループは、オブジェクトを更新する権限を持っています。<strong>Tables</strong> などのオブジェクトでは、ユーザーはテーブル内のデータを更新する権限を持っています。</span><span class="sxs-lookup"><span data-stu-id="77d4c-p106">The user or group has permission to update the object. For objects such as <strong>Tables</strong>, the user has permission to update the data in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77d4c-168"><strong>adRightWithGrant</strong></span><span class="sxs-lookup"><span data-stu-id="77d4c-168"><strong>adRightWithGrant</strong></span></span></p></td>
<td><p><span data-ttu-id="77d4c-169">4096</span><span class="sxs-lookup"><span data-stu-id="77d4c-169">4096</span></span><br />
<span data-ttu-id="77d4c-170">(&amp;H1000)</span><span class="sxs-lookup"><span data-stu-id="77d4c-170">(&amp;H1000)</span></span></p></td>
<td><p><span data-ttu-id="77d4c-171">ユーザーまたはグループは、オブジェクトに対する権限を与える権限を持っています。</span><span class="sxs-lookup"><span data-stu-id="77d4c-171">The user or group has permission to grant permissions on the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77d4c-172"><strong>adRightWriteDesign</strong></span><span class="sxs-lookup"><span data-stu-id="77d4c-172"><strong>adRightWriteDesign</strong></span></span></p></td>
<td><p><span data-ttu-id="77d4c-173">2048</span><span class="sxs-lookup"><span data-stu-id="77d4c-173">2048</span></span><br />
<span data-ttu-id="77d4c-174">(&amp;H800)</span><span class="sxs-lookup"><span data-stu-id="77d4c-174">(&amp;H800)</span></span></p></td>
<td><p><span data-ttu-id="77d4c-175">ユーザーまたはグループは、オブジェクトのデザインを修正する権限を持っています。</span><span class="sxs-lookup"><span data-stu-id="77d4c-175">The user or group has permission to modify the design for the object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77d4c-176"><strong>adRightWriteOwner</strong></span><span class="sxs-lookup"><span data-stu-id="77d4c-176"><strong>adRightWriteOwner</strong></span></span></p></td>
<td><p><span data-ttu-id="77d4c-177">524288</span><span class="sxs-lookup"><span data-stu-id="77d4c-177">524288</span></span><br />
<span data-ttu-id="77d4c-178">(&amp;H80000)</span><span class="sxs-lookup"><span data-stu-id="77d4c-178">(&amp;H80000)</span></span></p></td>
<td><p><span data-ttu-id="77d4c-179">ユーザーまたはグループは、オブジェクトの所有者を変更する権限を持っています。</span><span class="sxs-lookup"><span data-stu-id="77d4c-179">The user or group has permission to modify the owner of the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77d4c-180"><strong>adRightWritePermissions</strong></span><span class="sxs-lookup"><span data-stu-id="77d4c-180"><strong>adRightWritePermissions</strong></span></span></p></td>
<td><p><span data-ttu-id="77d4c-181">262144</span><span class="sxs-lookup"><span data-stu-id="77d4c-181">262144</span></span><br />
<span data-ttu-id="77d4c-182">(&amp;H40000)</span><span class="sxs-lookup"><span data-stu-id="77d4c-182">(&amp;H40000)</span></span></p></td>
<td><p><span data-ttu-id="77d4c-183">ユーザーまたはグループは、カタログ内のオブジェクトに対する特定の権限を変更することができます。</span><span class="sxs-lookup"><span data-stu-id="77d4c-183">The user or group can modify the specific permissions for an object in the catalog.</span></span></p></td>
</tr>
</tbody>
</table>

