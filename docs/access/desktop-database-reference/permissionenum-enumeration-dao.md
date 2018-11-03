---
title: PermissionEnum 列挙型 (DAO)
TOCTitle: PermissionEnum Enumeration
ms:assetid: dcce9940-f8a7-e915-1b69-05c341bea8cd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835373(v=office.15)
ms:contentKeyID: 48548147
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ed3abb0e3ff76ae19c6c19a3e2040b338e2b5ff3
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945867"
---
# <a name="permissionenum-enumeration-dao"></a><span data-ttu-id="5dd56-102">PermissionEnum 列挙型 (DAO)</span><span class="sxs-lookup"><span data-stu-id="5dd56-102">PermissionEnum enumeration (DAO)</span></span>


<span data-ttu-id="5dd56-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="5dd56-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5dd56-104">" **Permissions**/権限" プロパティで、権限の種類を指定するために使用します。</span><span class="sxs-lookup"><span data-stu-id="5dd56-104">Used with the **Permissions** property to specify the type of permissions.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5dd56-105">名前</span><span class="sxs-lookup"><span data-stu-id="5dd56-105">Name</span></span></p></th>
<th><p><span data-ttu-id="5dd56-106">値</span><span class="sxs-lookup"><span data-stu-id="5dd56-106">Value</span></span></p></th>
<th><p><span data-ttu-id="5dd56-107">説明</span><span class="sxs-lookup"><span data-stu-id="5dd56-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5dd56-108">dbSecCreate</span><span class="sxs-lookup"><span data-stu-id="5dd56-108">dbSecCreate</span></span></p></td>
<td><p><span data-ttu-id="5dd56-109">1</span><span class="sxs-lookup"><span data-stu-id="5dd56-109">1</span></span></p></td>
<td><p><span data-ttu-id="5dd56-110">ユーザーは新しいドキュメントを作成できます (Document オブジェクトに対しては無効)。</span><span class="sxs-lookup"><span data-stu-id="5dd56-110">The user can create new documents (not valid for Document objects).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dd56-111">dbSecDBAdmin</span><span class="sxs-lookup"><span data-stu-id="5dd56-111">dbSecDBAdmin</span></span></p></td>
<td><p><span data-ttu-id="5dd56-112">8</span><span class="sxs-lookup"><span data-stu-id="5dd56-112">8</span></span></p></td>
<td><p><span data-ttu-id="5dd56-113">ユーザーはデータベースをレプリケートし、データベース パスワードを変更できます (Document オブジェクトに対しては無効)。</span><span class="sxs-lookup"><span data-stu-id="5dd56-113">The user can replicate a database and change the database password (not valid for Document objects).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dd56-114">dbSecDBCreate</span><span class="sxs-lookup"><span data-stu-id="5dd56-114">dbSecDBCreate</span></span></p></td>
<td><p><span data-ttu-id="5dd56-115">1</span><span class="sxs-lookup"><span data-stu-id="5dd56-115">1</span></span></p></td>
<td><p><span data-ttu-id="5dd56-p101">ユーザーは新しいデータベースを作成できます。このオプションは、ワークグループ情報ファイル (Systen.mdw) の Databases コンテナーでのみ有効です。この定数は、Document オブジェクトに対しては無効です。</span><span class="sxs-lookup"><span data-stu-id="5dd56-p101">The user can create new databases. This option is valid only on the Databases container in the workgroup information file (Systen.mdw). This constant is not valid for Document objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dd56-119">dbSecDBExclusive</span><span class="sxs-lookup"><span data-stu-id="5dd56-119">dbSecDBExclusive</span></span></p></td>
<td><p><span data-ttu-id="5dd56-120">4</span><span class="sxs-lookup"><span data-stu-id="5dd56-120">4</span></span></p></td>
<td><p><span data-ttu-id="5dd56-121">ユーザーはデータベースに排他的にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="5dd56-121">The user has exclusive access to the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dd56-122">dbSecDBOpen</span><span class="sxs-lookup"><span data-stu-id="5dd56-122">dbSecDBOpen</span></span></p></td>
<td><p><span data-ttu-id="5dd56-123">2</span><span class="sxs-lookup"><span data-stu-id="5dd56-123">2</span></span></p></td>
<td><p><span data-ttu-id="5dd56-124">ユーザーはデータベースを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="5dd56-124">The user can open the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dd56-125">dbSecDelete</span><span class="sxs-lookup"><span data-stu-id="5dd56-125">dbSecDelete</span></span></p></td>
<td><p><span data-ttu-id="5dd56-126">65536</span><span class="sxs-lookup"><span data-stu-id="5dd56-126">65536</span></span></p></td>
<td><p><span data-ttu-id="5dd56-127">ユーザーはオブジェクトを削除できます。</span><span class="sxs-lookup"><span data-stu-id="5dd56-127">The user can delete the object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dd56-128">dbSecDeleteData</span><span class="sxs-lookup"><span data-stu-id="5dd56-128">dbSecDeleteData</span></span></p></td>
<td><p><span data-ttu-id="5dd56-129"> 
128 
</span><span class="sxs-lookup"><span data-stu-id="5dd56-129">128</span></span></p></td>
<td><p><span data-ttu-id="5dd56-130">ユーザーはレコードを削除できます。</span><span class="sxs-lookup"><span data-stu-id="5dd56-130">The user can delete records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dd56-131">dbSecFullAccess</span><span class="sxs-lookup"><span data-stu-id="5dd56-131">dbSecFullAccess</span></span></p></td>
<td><p><span data-ttu-id="5dd56-132">1048575</span><span class="sxs-lookup"><span data-stu-id="5dd56-132">1048575</span></span></p></td>
<td><p><span data-ttu-id="5dd56-133">ユーザーはオブジェクトに完全にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="5dd56-133">The user has full access to the object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dd56-134">dbSecInsertData</span><span class="sxs-lookup"><span data-stu-id="5dd56-134">dbSecInsertData</span></span></p></td>
<td><p><span data-ttu-id="5dd56-135">32</span><span class="sxs-lookup"><span data-stu-id="5dd56-135">32</span></span></p></td>
<td><p><span data-ttu-id="5dd56-136">ユーザーはレコードを追加できます。</span><span class="sxs-lookup"><span data-stu-id="5dd56-136">The user can add records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dd56-137">dbSecNoAccess</span><span class="sxs-lookup"><span data-stu-id="5dd56-137">dbSecNoAccess</span></span></p></td>
<td><p><span data-ttu-id="5dd56-138">0</span><span class="sxs-lookup"><span data-stu-id="5dd56-138">0</span></span></p></td>
<td><p><span data-ttu-id="5dd56-139">ユーザーはオブジェクトにアクセスできません (Document オブジェクトに対しては無効)。</span><span class="sxs-lookup"><span data-stu-id="5dd56-139">The user does not have access to the object (not valid for Document objects).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dd56-140">dbSecReadDef</span><span class="sxs-lookup"><span data-stu-id="5dd56-140">dbSecReadDef</span></span></p></td>
<td><p><span data-ttu-id="5dd56-141">4</span><span class="sxs-lookup"><span data-stu-id="5dd56-141">4</span></span></p></td>
<td><p><span data-ttu-id="5dd56-142">ユーザーは列情報およびインデックス情報を含むテーブル定義を読み取ることができます。</span><span class="sxs-lookup"><span data-stu-id="5dd56-142">The user can read the table definition, including column and index information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dd56-143">dbSecReadSec</span><span class="sxs-lookup"><span data-stu-id="5dd56-143">dbSecReadSec</span></span></p></td>
<td><p><span data-ttu-id="5dd56-144">131072</span><span class="sxs-lookup"><span data-stu-id="5dd56-144">131072</span></span></p></td>
<td><p><span data-ttu-id="5dd56-145">ユーザーはオブジェクトのセキュリティ関連情報を読み取ることができます。</span><span class="sxs-lookup"><span data-stu-id="5dd56-145">The user can read the object's security-related information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dd56-146">dbSecReplaceData</span><span class="sxs-lookup"><span data-stu-id="5dd56-146">dbSecReplaceData</span></span></p></td>
<td><p><span data-ttu-id="5dd56-147">64</span><span class="sxs-lookup"><span data-stu-id="5dd56-147">64</span></span></p></td>
<td><p><span data-ttu-id="5dd56-148">ユーザーはレコードを変更できます。</span><span class="sxs-lookup"><span data-stu-id="5dd56-148">The user can modify records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dd56-149">dbSecRetrieveData</span><span class="sxs-lookup"><span data-stu-id="5dd56-149">dbSecRetrieveData</span></span></p></td>
<td><p><span data-ttu-id="5dd56-150">20</span><span class="sxs-lookup"><span data-stu-id="5dd56-150">20</span></span></p></td>
<td><p><span data-ttu-id="5dd56-151">ユーザーは Document オブジェクトからデータを取得できます。</span><span class="sxs-lookup"><span data-stu-id="5dd56-151">The user can retrieve data from the Document object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dd56-152">dbSecWriteDef</span><span class="sxs-lookup"><span data-stu-id="5dd56-152">dbSecWriteDef</span></span></p></td>
<td><p><span data-ttu-id="5dd56-153">65548</span><span class="sxs-lookup"><span data-stu-id="5dd56-153">65548</span></span></p></td>
<td><p><span data-ttu-id="5dd56-154">ユーザーは列情報およびインデックス情報を含むテーブル定義を変更または削除できます。</span><span class="sxs-lookup"><span data-stu-id="5dd56-154">The user can modify or delete the table definition, including column and index information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dd56-155">dbSecWriteOwner</span><span class="sxs-lookup"><span data-stu-id="5dd56-155">dbSecWriteOwner</span></span></p></td>
<td><p><span data-ttu-id="5dd56-156">524288</span><span class="sxs-lookup"><span data-stu-id="5dd56-156">524288</span></span></p></td>
<td><p><span data-ttu-id="5dd56-157">ユーザーは "Owner/所有者" プロパティの設定を変更できます。</span><span class="sxs-lookup"><span data-stu-id="5dd56-157">The user can change the Owner property setting.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dd56-158">dbSecWriteSec</span><span class="sxs-lookup"><span data-stu-id="5dd56-158">dbSecWriteSec</span></span></p></td>
<td><p><span data-ttu-id="5dd56-159">262144</span><span class="sxs-lookup"><span data-stu-id="5dd56-159">262144</span></span></p></td>
<td><p><span data-ttu-id="5dd56-160">ユーザーはアクセス権限を変更できます。</span><span class="sxs-lookup"><span data-stu-id="5dd56-160">The user can alter access permissions.</span></span></p></td>
</tr>
</tbody>
</table>

