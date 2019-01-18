---
title: RightsEnum (デスクトップ データベース参照のアクセス)
TOCTitle: RightsEnum
ms:assetid: 7647b9d5-5271-fdcf-489d-5a8beb931ca5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249485(v=office.15)
ms:contentKeyID: 48545693
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3c7bf2f88632265cda7537215f2ea3c68507f16f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706605"
---
# <a name="rightsenum"></a><span data-ttu-id="24667-102">RightsEnum</span><span class="sxs-lookup"><span data-stu-id="24667-102">RightsEnum</span></span>

<span data-ttu-id="24667-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="24667-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="24667-104">オブジェクトに対するグループまたはユーザーの権限を指定します。</span><span class="sxs-lookup"><span data-stu-id="24667-104">Specifies the rights or permissions for a group or user on an object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="24667-105">定数</span><span class="sxs-lookup"><span data-stu-id="24667-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="24667-106">値</span><span class="sxs-lookup"><span data-stu-id="24667-106">Value</span></span></p></th>
<th><p><span data-ttu-id="24667-107">説明</span><span class="sxs-lookup"><span data-stu-id="24667-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="24667-108"><strong>adRightCreate</strong></span><span class="sxs-lookup"><span data-stu-id="24667-108"><strong>adRightCreate</strong></span></span></p></td>
<td><p><span data-ttu-id="24667-109">16384</span><span class="sxs-lookup"><span data-stu-id="24667-109">16384</span></span><br />
<span data-ttu-id="24667-110">(&amp;H4000)</span><span class="sxs-lookup"><span data-stu-id="24667-110">(&amp;H4000)</span></span></p></td>
<td><p><span data-ttu-id="24667-111">ユーザーまたはグループは、この種類の新規オブジェクトを作成する権限を持っています。</span><span class="sxs-lookup"><span data-stu-id="24667-111">The user or group has permission to create new objects of this type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24667-112"><strong>adRightDelete</strong></span><span class="sxs-lookup"><span data-stu-id="24667-112"><strong>adRightDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="24667-113">65536</span><span class="sxs-lookup"><span data-stu-id="24667-113">65536</span></span><br />
<span data-ttu-id="24667-114">(&amp;H10000)</span><span class="sxs-lookup"><span data-stu-id="24667-114">(&amp;H10000)</span></span></p></td>
<td><p><span data-ttu-id="24667-p101">ユーザーまたはグループは、オブジェクトからデータを削除する権限を持っています。<strong>Tables</strong> などのオブジェクトでは、ユーザーはレコードからデータ値を削除する権限を持っています。</span><span class="sxs-lookup"><span data-stu-id="24667-p101">The user or group has permission to delete data from an object. For objects such as <strong>Tables</strong>, the user has permission to delete data values from records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24667-117"><strong>adRightDrop</strong></span><span class="sxs-lookup"><span data-stu-id="24667-117"><strong>adRightDrop</strong></span></span></p></td>
<td><p><span data-ttu-id="24667-118">256</span><span class="sxs-lookup"><span data-stu-id="24667-118">256</span></span><br />
<span data-ttu-id="24667-119">(&amp;H100)</span><span class="sxs-lookup"><span data-stu-id="24667-119">(&amp;H100)</span></span></p></td>
<td><p><span data-ttu-id="24667-p102">ユーザーまたはグループは、カタログからオブジェクトを削除する権限を持っています。たとえば、<strong>Tables</strong> を DROP TABLE SQL コマンドによって削除できます。</span><span class="sxs-lookup"><span data-stu-id="24667-p102">The user or group has permission to remove objects from the catalog. For example, <strong>Tables</strong> can be deleted by a DROP TABLE SQL command.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24667-122"><strong>adRightExclusive</strong></span><span class="sxs-lookup"><span data-stu-id="24667-122"><strong>adRightExclusive</strong></span></span></p></td>
<td><p><span data-ttu-id="24667-123">512</span><span class="sxs-lookup"><span data-stu-id="24667-123">512</span></span><br />
<span data-ttu-id="24667-124">(&amp;H200)</span><span class="sxs-lookup"><span data-stu-id="24667-124">(&amp;H200)</span></span></p></td>
<td><p><span data-ttu-id="24667-125">ユーザーまたはグループは、排他的にオブジェクトにアクセスする権限を持っています。</span><span class="sxs-lookup"><span data-stu-id="24667-125">The user or group has permission to access the object exclusively.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24667-126"><strong>adRightExecute</strong></span><span class="sxs-lookup"><span data-stu-id="24667-126"><strong>adRightExecute</strong></span></span></p></td>
<td><p><span data-ttu-id="24667-127">536870912</span><span class="sxs-lookup"><span data-stu-id="24667-127">536870912</span></span><br />
<span data-ttu-id="24667-128">(&amp;H20000000)</span><span class="sxs-lookup"><span data-stu-id="24667-128">(&amp;H20000000)</span></span></p></td>
<td><p><span data-ttu-id="24667-129">ユーザーまたはグループは、オブジェクトを実行する権限を持っています。</span><span class="sxs-lookup"><span data-stu-id="24667-129">The user or group has permission to execute the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24667-130"><strong>adRightFull</strong></span><span class="sxs-lookup"><span data-stu-id="24667-130"><strong>adRightFull</strong></span></span></p></td>
<td><p><span data-ttu-id="24667-131">268435456</span><span class="sxs-lookup"><span data-stu-id="24667-131">268435456</span></span><br />
<span data-ttu-id="24667-132">(&amp;H10000000)</span><span class="sxs-lookup"><span data-stu-id="24667-132">(&amp;H10000000)</span></span></p></td>
<td><p><span data-ttu-id="24667-133">ユーザーまたはグループは、オブジェクトに対するすべての権限を持っています。</span><span class="sxs-lookup"><span data-stu-id="24667-133">The user or group has all permissions on the object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24667-134"><strong>adRightInsert</strong></span><span class="sxs-lookup"><span data-stu-id="24667-134"><strong>adRightInsert</strong></span></span></p></td>
<td><p><span data-ttu-id="24667-135">32768</span><span class="sxs-lookup"><span data-stu-id="24667-135">32768</span></span><br />
<span data-ttu-id="24667-136">(&amp;H8000)</span><span class="sxs-lookup"><span data-stu-id="24667-136">(&amp;H8000)</span></span></p></td>
<td><p><span data-ttu-id="24667-p103">ユーザーまたはグループは、オブジェクトを挿入する権限を持っています。<strong>Tables</strong> などのオブジェクトでは、ユーザーはデータをテーブルに挿入する権限を持っています。</span><span class="sxs-lookup"><span data-stu-id="24667-p103">The user or group has permission to insert the object. For objects such as <strong>Tables</strong>, the user has permission to insert data into the table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24667-139"><strong>adRightMaximumAllowed</strong></span><span class="sxs-lookup"><span data-stu-id="24667-139"><strong>adRightMaximumAllowed</strong></span></span></p></td>
<td><p><span data-ttu-id="24667-140">33554432 (&amp;H2000000)</span><span class="sxs-lookup"><span data-stu-id="24667-140">33554432 (&amp;H2000000)</span></span></p></td>
<td><p><span data-ttu-id="24667-p104">ユーザーまたはグループは、プロバイダーによって許可される最大数の権限を持っています。指定される権限は、プロバイダーの設定によって決まります。</span><span class="sxs-lookup"><span data-stu-id="24667-p104">The user or group has the maximum number of permissions allowed by the provider. Specific permissions are provider-dependent.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24667-143"><strong>adRightNone</strong></span><span class="sxs-lookup"><span data-stu-id="24667-143"><strong>adRightNone</strong></span></span></p></td>
<td><p><span data-ttu-id="24667-144">0</span><span class="sxs-lookup"><span data-stu-id="24667-144">0</span></span></p></td>
<td><p><span data-ttu-id="24667-145">ユーザーまたはグループは、オブジェクトに対する権限を持ちません。</span><span class="sxs-lookup"><span data-stu-id="24667-145">The user or group has no permissions for the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24667-146"><strong>adRightRead</strong></span><span class="sxs-lookup"><span data-stu-id="24667-146"><strong>adRightRead</strong></span></span></p></td>
<td><p><span data-ttu-id="24667-147">-2147483648</span><span class="sxs-lookup"><span data-stu-id="24667-147">-2147483648</span></span><br />
<span data-ttu-id="24667-148">(&amp;H80000000)</span><span class="sxs-lookup"><span data-stu-id="24667-148">(&amp;H80000000)</span></span></p></td>
<td><p><span data-ttu-id="24667-p105">ユーザーまたはグループは、オブジェクトを読み取る権限を持っています。<a href="table-object-adox.md">Tables</a> などのオブジェクトでは、ユーザーはテーブル内のデータを読み取る権限を持っています。</span><span class="sxs-lookup"><span data-stu-id="24667-p105">The user or group has permission to read the object. For objects such as <a href="table-object-adox.md">Tables</a>, the user has permission to read the data in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24667-151"><strong>adRightReadDesign</strong></span><span class="sxs-lookup"><span data-stu-id="24667-151"><strong>adRightReadDesign</strong></span></span></p></td>
<td><p><span data-ttu-id="24667-152">1024</span><span class="sxs-lookup"><span data-stu-id="24667-152">1024</span></span><br />
<span data-ttu-id="24667-153">(&amp;H400)</span><span class="sxs-lookup"><span data-stu-id="24667-153">(&amp;H400)</span></span></p></td>
<td><p><span data-ttu-id="24667-154">ユーザーまたはグループは、オブジェクトのデザインを読み取る権限を持っています。</span><span class="sxs-lookup"><span data-stu-id="24667-154">The user or group has permission to read the design for the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24667-155"><strong>adRightReadPermissions</strong></span><span class="sxs-lookup"><span data-stu-id="24667-155"><strong>adRightReadPermissions</strong></span></span></p></td>
<td><p><span data-ttu-id="24667-156">131072</span><span class="sxs-lookup"><span data-stu-id="24667-156">131072</span></span><br />
<span data-ttu-id="24667-157">(&amp;H20000)</span><span class="sxs-lookup"><span data-stu-id="24667-157">(&amp;H20000)</span></span></p></td>
<td><p><span data-ttu-id="24667-158">ユーザーまたはグループは、カタログ内のオブジェクトの特定の権限を表示することができますが、変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="24667-158">The user or group can view, but not change, the specific permissions for an object in the catalog.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24667-159"><strong>adRightReference</strong></span><span class="sxs-lookup"><span data-stu-id="24667-159"><strong>adRightReference</strong></span></span></p></td>
<td><p><span data-ttu-id="24667-160">8192</span><span class="sxs-lookup"><span data-stu-id="24667-160">8192</span></span><br />
<span data-ttu-id="24667-161">(&amp;H2000)</span><span class="sxs-lookup"><span data-stu-id="24667-161">(&amp;H2000)</span></span></p></td>
<td><p><span data-ttu-id="24667-162">ユーザーまたはグループは、オブジェクトを参照する権限を持っています。</span><span class="sxs-lookup"><span data-stu-id="24667-162">The user or group has permission to reference the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24667-163"><strong>adRightUpdate</strong></span><span class="sxs-lookup"><span data-stu-id="24667-163"><strong>adRightUpdate</strong></span></span></p></td>
<td><p><span data-ttu-id="24667-164">1073741824</span><span class="sxs-lookup"><span data-stu-id="24667-164">1073741824</span></span><br />
<span data-ttu-id="24667-165">(&amp;H40000000)</span><span class="sxs-lookup"><span data-stu-id="24667-165">(&amp;H40000000)</span></span></p></td>
<td><p><span data-ttu-id="24667-p106">ユーザーまたはグループは、オブジェクトを更新する権限を持っています。<strong>Tables</strong> などのオブジェクトでは、ユーザーはテーブル内のデータを更新する権限を持っています。</span><span class="sxs-lookup"><span data-stu-id="24667-p106">The user or group has permission to update the object. For objects such as <strong>Tables</strong>, the user has permission to update the data in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24667-168"><strong>adRightWithGrant</strong></span><span class="sxs-lookup"><span data-stu-id="24667-168"><strong>adRightWithGrant</strong></span></span></p></td>
<td><p><span data-ttu-id="24667-169">4096</span><span class="sxs-lookup"><span data-stu-id="24667-169">4096</span></span><br />
<span data-ttu-id="24667-170">(&amp;H1000)</span><span class="sxs-lookup"><span data-stu-id="24667-170">(&amp;H1000)</span></span></p></td>
<td><p><span data-ttu-id="24667-171">ユーザーまたはグループは、オブジェクトに対する権限を与える権限を持っています。</span><span class="sxs-lookup"><span data-stu-id="24667-171">The user or group has permission to grant permissions on the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24667-172"><strong>adRightWriteDesign</strong></span><span class="sxs-lookup"><span data-stu-id="24667-172"><strong>adRightWriteDesign</strong></span></span></p></td>
<td><p><span data-ttu-id="24667-173">2048</span><span class="sxs-lookup"><span data-stu-id="24667-173">2048</span></span><br />
<span data-ttu-id="24667-174">(&amp;H800)</span><span class="sxs-lookup"><span data-stu-id="24667-174">(&amp;H800)</span></span></p></td>
<td><p><span data-ttu-id="24667-175">ユーザーまたはグループは、オブジェクトのデザインを修正する権限を持っています。</span><span class="sxs-lookup"><span data-stu-id="24667-175">The user or group has permission to modify the design for the object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="24667-176"><strong>adRightWriteOwner</strong></span><span class="sxs-lookup"><span data-stu-id="24667-176"><strong>adRightWriteOwner</strong></span></span></p></td>
<td><p><span data-ttu-id="24667-177">524288</span><span class="sxs-lookup"><span data-stu-id="24667-177">524288</span></span><br />
<span data-ttu-id="24667-178">(&amp;H80000)</span><span class="sxs-lookup"><span data-stu-id="24667-178">(&amp;H80000)</span></span></p></td>
<td><p><span data-ttu-id="24667-179">ユーザーまたはグループは、オブジェクトの所有者を変更する権限を持っています。</span><span class="sxs-lookup"><span data-stu-id="24667-179">The user or group has permission to modify the owner of the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="24667-180"><strong>adRightWritePermissions</strong></span><span class="sxs-lookup"><span data-stu-id="24667-180"><strong>adRightWritePermissions</strong></span></span></p></td>
<td><p><span data-ttu-id="24667-181">262144</span><span class="sxs-lookup"><span data-stu-id="24667-181">262144</span></span><br />
<span data-ttu-id="24667-182">(&amp;H40000)</span><span class="sxs-lookup"><span data-stu-id="24667-182">(&amp;H40000)</span></span></p></td>
<td><p><span data-ttu-id="24667-183">ユーザーまたはグループは、カタログ内のオブジェクトに対する特定の権限を変更することができます。</span><span class="sxs-lookup"><span data-stu-id="24667-183">The user or group can modify the specific permissions for an object in the catalog.</span></span></p></td>
</tr>
</tbody>
</table>

