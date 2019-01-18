---
title: PermissionEnum 列挙型 (DAO)
TOCTitle: PermissionEnum Enumeration
ms:assetid: dcce9940-f8a7-e915-1b69-05c341bea8cd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835373(v=office.15)
ms:contentKeyID: 48548147
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8d4f6741bd6203dbdeffb364650b5e3550ea8b1c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715460"
---
# <a name="permissionenum-enumeration-dao"></a><span data-ttu-id="02e45-102">PermissionEnum 列挙型 (DAO)</span><span class="sxs-lookup"><span data-stu-id="02e45-102">PermissionEnum enumeration (DAO)</span></span>


<span data-ttu-id="02e45-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="02e45-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="02e45-104">" **Permissions**/権限" プロパティで、権限の種類を指定するために使用します。</span><span class="sxs-lookup"><span data-stu-id="02e45-104">Used with the **Permissions** property to specify the type of permissions.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="02e45-105">名前</span><span class="sxs-lookup"><span data-stu-id="02e45-105">Name</span></span></p></th>
<th><p><span data-ttu-id="02e45-106">値</span><span class="sxs-lookup"><span data-stu-id="02e45-106">Value</span></span></p></th>
<th><p><span data-ttu-id="02e45-107">説明</span><span class="sxs-lookup"><span data-stu-id="02e45-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="02e45-108">dbSecCreate</span><span class="sxs-lookup"><span data-stu-id="02e45-108">dbSecCreate</span></span></p></td>
<td><p><span data-ttu-id="02e45-109">1</span><span class="sxs-lookup"><span data-stu-id="02e45-109">1</span></span></p></td>
<td><p><span data-ttu-id="02e45-110">ユーザーは新しいドキュメントを作成できます (Document オブジェクトに対しては無効)。</span><span class="sxs-lookup"><span data-stu-id="02e45-110">The user can create new documents (not valid for Document objects).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02e45-111">dbSecDBAdmin</span><span class="sxs-lookup"><span data-stu-id="02e45-111">dbSecDBAdmin</span></span></p></td>
<td><p><span data-ttu-id="02e45-112">8</span><span class="sxs-lookup"><span data-stu-id="02e45-112">8</span></span></p></td>
<td><p><span data-ttu-id="02e45-113">ユーザーはデータベースをレプリケートし、データベース パスワードを変更できます (Document オブジェクトに対しては無効)。</span><span class="sxs-lookup"><span data-stu-id="02e45-113">The user can replicate a database and change the database password (not valid for Document objects).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02e45-114">dbSecDBCreate</span><span class="sxs-lookup"><span data-stu-id="02e45-114">dbSecDBCreate</span></span></p></td>
<td><p><span data-ttu-id="02e45-115">1</span><span class="sxs-lookup"><span data-stu-id="02e45-115">1</span></span></p></td>
<td><p><span data-ttu-id="02e45-p101">ユーザーは新しいデータベースを作成できます。このオプションは、ワークグループ情報ファイル (Systen.mdw) の Databases コンテナーでのみ有効です。この定数は、Document オブジェクトに対しては無効です。</span><span class="sxs-lookup"><span data-stu-id="02e45-p101">The user can create new databases. This option is valid only on the Databases container in the workgroup information file (Systen.mdw). This constant is not valid for Document objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02e45-119">dbSecDBExclusive</span><span class="sxs-lookup"><span data-stu-id="02e45-119">dbSecDBExclusive</span></span></p></td>
<td><p><span data-ttu-id="02e45-120">4</span><span class="sxs-lookup"><span data-stu-id="02e45-120">4</span></span></p></td>
<td><p><span data-ttu-id="02e45-121">ユーザーはデータベースに排他的にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="02e45-121">The user has exclusive access to the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02e45-122">dbSecDBOpen</span><span class="sxs-lookup"><span data-stu-id="02e45-122">dbSecDBOpen</span></span></p></td>
<td><p><span data-ttu-id="02e45-123">2</span><span class="sxs-lookup"><span data-stu-id="02e45-123">2</span></span></p></td>
<td><p><span data-ttu-id="02e45-124">ユーザーはデータベースを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="02e45-124">The user can open the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02e45-125">dbSecDelete</span><span class="sxs-lookup"><span data-stu-id="02e45-125">dbSecDelete</span></span></p></td>
<td><p><span data-ttu-id="02e45-126">65536</span><span class="sxs-lookup"><span data-stu-id="02e45-126">65536</span></span></p></td>
<td><p><span data-ttu-id="02e45-127">ユーザーはオブジェクトを削除できます。</span><span class="sxs-lookup"><span data-stu-id="02e45-127">The user can delete the object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02e45-128">dbSecDeleteData</span><span class="sxs-lookup"><span data-stu-id="02e45-128">dbSecDeleteData</span></span></p></td>
<td><p><span data-ttu-id="02e45-129"> 
128 
</span><span class="sxs-lookup"><span data-stu-id="02e45-129">128</span></span></p></td>
<td><p><span data-ttu-id="02e45-130">ユーザーはレコードを削除できます。</span><span class="sxs-lookup"><span data-stu-id="02e45-130">The user can delete records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02e45-131">dbSecFullAccess</span><span class="sxs-lookup"><span data-stu-id="02e45-131">dbSecFullAccess</span></span></p></td>
<td><p><span data-ttu-id="02e45-132">1048575</span><span class="sxs-lookup"><span data-stu-id="02e45-132">1048575</span></span></p></td>
<td><p><span data-ttu-id="02e45-133">ユーザーはオブジェクトに完全にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="02e45-133">The user has full access to the object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02e45-134">dbSecInsertData</span><span class="sxs-lookup"><span data-stu-id="02e45-134">dbSecInsertData</span></span></p></td>
<td><p><span data-ttu-id="02e45-135">32</span><span class="sxs-lookup"><span data-stu-id="02e45-135">32</span></span></p></td>
<td><p><span data-ttu-id="02e45-136">ユーザーはレコードを追加できます。</span><span class="sxs-lookup"><span data-stu-id="02e45-136">The user can add records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02e45-137">dbSecNoAccess</span><span class="sxs-lookup"><span data-stu-id="02e45-137">dbSecNoAccess</span></span></p></td>
<td><p><span data-ttu-id="02e45-138">0</span><span class="sxs-lookup"><span data-stu-id="02e45-138">0</span></span></p></td>
<td><p><span data-ttu-id="02e45-139">ユーザーはオブジェクトにアクセスできません (Document オブジェクトに対しては無効)。</span><span class="sxs-lookup"><span data-stu-id="02e45-139">The user does not have access to the object (not valid for Document objects).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02e45-140">dbSecReadDef</span><span class="sxs-lookup"><span data-stu-id="02e45-140">dbSecReadDef</span></span></p></td>
<td><p><span data-ttu-id="02e45-141">4</span><span class="sxs-lookup"><span data-stu-id="02e45-141">4</span></span></p></td>
<td><p><span data-ttu-id="02e45-142">ユーザーは列情報およびインデックス情報を含むテーブル定義を読み取ることができます。</span><span class="sxs-lookup"><span data-stu-id="02e45-142">The user can read the table definition, including column and index information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02e45-143">dbSecReadSec</span><span class="sxs-lookup"><span data-stu-id="02e45-143">dbSecReadSec</span></span></p></td>
<td><p><span data-ttu-id="02e45-144">131072</span><span class="sxs-lookup"><span data-stu-id="02e45-144">131072</span></span></p></td>
<td><p><span data-ttu-id="02e45-145">ユーザーはオブジェクトのセキュリティ関連情報を読み取ることができます。</span><span class="sxs-lookup"><span data-stu-id="02e45-145">The user can read the object's security-related information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02e45-146">dbSecReplaceData</span><span class="sxs-lookup"><span data-stu-id="02e45-146">dbSecReplaceData</span></span></p></td>
<td><p><span data-ttu-id="02e45-147">64</span><span class="sxs-lookup"><span data-stu-id="02e45-147">64</span></span></p></td>
<td><p><span data-ttu-id="02e45-148">ユーザーはレコードを変更できます。</span><span class="sxs-lookup"><span data-stu-id="02e45-148">The user can modify records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02e45-149">dbSecRetrieveData</span><span class="sxs-lookup"><span data-stu-id="02e45-149">dbSecRetrieveData</span></span></p></td>
<td><p><span data-ttu-id="02e45-150">20</span><span class="sxs-lookup"><span data-stu-id="02e45-150">20</span></span></p></td>
<td><p><span data-ttu-id="02e45-151">ユーザーは Document オブジェクトからデータを取得できます。</span><span class="sxs-lookup"><span data-stu-id="02e45-151">The user can retrieve data from the Document object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02e45-152">dbSecWriteDef</span><span class="sxs-lookup"><span data-stu-id="02e45-152">dbSecWriteDef</span></span></p></td>
<td><p><span data-ttu-id="02e45-153">65548</span><span class="sxs-lookup"><span data-stu-id="02e45-153">65548</span></span></p></td>
<td><p><span data-ttu-id="02e45-154">ユーザーは列情報およびインデックス情報を含むテーブル定義を変更または削除できます。</span><span class="sxs-lookup"><span data-stu-id="02e45-154">The user can modify or delete the table definition, including column and index information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02e45-155">dbSecWriteOwner</span><span class="sxs-lookup"><span data-stu-id="02e45-155">dbSecWriteOwner</span></span></p></td>
<td><p><span data-ttu-id="02e45-156">524288</span><span class="sxs-lookup"><span data-stu-id="02e45-156">524288</span></span></p></td>
<td><p><span data-ttu-id="02e45-157">ユーザーは "Owner/所有者" プロパティの設定を変更できます。</span><span class="sxs-lookup"><span data-stu-id="02e45-157">The user can change the Owner property setting.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02e45-158">dbSecWriteSec</span><span class="sxs-lookup"><span data-stu-id="02e45-158">dbSecWriteSec</span></span></p></td>
<td><p><span data-ttu-id="02e45-159">262144</span><span class="sxs-lookup"><span data-stu-id="02e45-159">262144</span></span></p></td>
<td><p><span data-ttu-id="02e45-160">ユーザーはアクセス権限を変更できます。</span><span class="sxs-lookup"><span data-stu-id="02e45-160">The user can alter access permissions.</span></span></p></td>
</tr>
</tbody>
</table>

