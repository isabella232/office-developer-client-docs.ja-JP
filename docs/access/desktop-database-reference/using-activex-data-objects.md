---
title: ActiveX データ オブジェクトを使用する
TOCTitle: Using ActiveX Data Objects
ms:assetid: 64055c45-7a27-2296-468a-015362898329
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194969(v=office.15)
ms:contentKeyID: 48545279
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5285627
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 1f7c57ca785e115e9278145921bf50e8afe870ab
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477335"
---
# <a name="using-activex-data-objects"></a><span data-ttu-id="5d58c-102">ActiveX データ オブジェクトを使用する</span><span class="sxs-lookup"><span data-stu-id="5d58c-102">Using ActiveX Data Objects</span></span>


<span data-ttu-id="5d58c-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="5d58c-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="5d58c-104">Microsoft Access では、Visual Basic を使って Access データベースとその関連データを作成、保守、および管理するための 3 つの新しいオブジェクト モデルが提供されています。</span><span class="sxs-lookup"><span data-stu-id="5d58c-104">Microsoft Access provides three object models to use in the creation, maintaining and managing of your Access databases and their related data by using Visual Basic.</span></span>

## <a name="microsoft-activex-data-objects-ado"></a><span data-ttu-id="5d58c-105">ADO (ActiveX データ オブジェクト)</span><span class="sxs-lookup"><span data-stu-id="5d58c-105">Microsoft ActiveX Data Objects (ADO)</span></span>

<span data-ttu-id="5d58c-106">ADO には、指定されたデータソースからレコードを作成、保守、および削除するために必要なオブジェクトが含まれてます。</span><span class="sxs-lookup"><span data-stu-id="5d58c-106">ADO contains the objects needed to create, maintain, and delete records in a given datasource.</span></span>

## <a name="microsoft-ado-ext-for-ddl-and-security-adox"></a><span data-ttu-id="5d58c-107">ADOX (ADO Ext. for DDL and Security)</span><span class="sxs-lookup"><span data-stu-id="5d58c-107">Microsoft ADO Ext. for DDL and Security (ADOX)</span></span>

<span data-ttu-id="5d58c-108">ADOX では、セキュリティ管理に必要なオブジェクトのほか、新しいデータベースに必要な DDL (データ定義言語) オブジェクト、およびそれに含まれるオブジェクトが提供されています。</span><span class="sxs-lookup"><span data-stu-id="5d58c-108">ADOX provides the Data Definition Language(DDL) objects needed to create a new database and its contained objects in addition to the objects needed to manage security.</span></span>

<span data-ttu-id="5d58c-109">**JRO (Jet and Replication Objects 2.5 Library)**</span><span class="sxs-lookup"><span data-stu-id="5d58c-109">**Microsoft Jet and Replication Objects 2.5 Library (JRO)**</span></span>

<span data-ttu-id="5d58c-110">ADO オブジェクトは、Jet データベースだけでなく、数多くのデータベースと共に動作するよう設計されています。JRO ライブラリには Jet 特有の機能を集めています。</span><span class="sxs-lookup"><span data-stu-id="5d58c-110">Since ADO objects were designed to work with many databases in addition to Microsoft Jet databases, functionality specific to Jet was broken out into the JRO library.</span></span>

<span data-ttu-id="5d58c-111">次の表は、各機能を DAO と比較したものです。</span><span class="sxs-lookup"><span data-stu-id="5d58c-111">The following table lists the functionality provided by each compared to DAO.</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5d58c-112">機能</span><span class="sxs-lookup"><span data-stu-id="5d58c-112">Functionality</span></span></p></th>
<th><p><span data-ttu-id="5d58c-113">DAO</span><span class="sxs-lookup"><span data-stu-id="5d58c-113">DAO</span></span></p></th>
<th><p><span data-ttu-id="5d58c-114">ADO1</span><span class="sxs-lookup"><span data-stu-id="5d58c-114">ADO1</span></span></p></th>
<th><p><span data-ttu-id="5d58c-115">ADOX2</span><span class="sxs-lookup"><span data-stu-id="5d58c-115">ADOX2</span></span></p></th>
<th><p><span data-ttu-id="5d58c-116">JRO</span><span class="sxs-lookup"><span data-stu-id="5d58c-116">JRO</span></span><br />
<span data-ttu-id="5d58c-117">(MDB ののみ)</span><span class="sxs-lookup"><span data-stu-id="5d58c-117">(MDB's Only)</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5d58c-118">レコードセットの作成</span><span class="sxs-lookup"><span data-stu-id="5d58c-118">Create Recordsets</span></span></p></td>
<td><p><span data-ttu-id="5d58c-119">X</span><span class="sxs-lookup"><span data-stu-id="5d58c-119">X</span></span></p></td>
<td><p><span data-ttu-id="5d58c-120">X</span><span class="sxs-lookup"><span data-stu-id="5d58c-120">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d58c-121">起動時の設定関連のプロパティの編集</span><span class="sxs-lookup"><span data-stu-id="5d58c-121">Edit Startup properties</span></span></p></td>
<td><p><span data-ttu-id="5d58c-122">X</span><span class="sxs-lookup"><span data-stu-id="5d58c-122">X</span></span></p></td>
<td><p><span data-ttu-id="5d58c-123">X\*\*</span><span class="sxs-lookup"><span data-stu-id="5d58c-123">X\*\*</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d58c-124">ANSI92 SQL のサポート \*\*\*</span><span class="sxs-lookup"><span data-stu-id="5d58c-124">Support ANSI92 SQL\*\*\*</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="5d58c-125">X</span><span class="sxs-lookup"><span data-stu-id="5d58c-125">X</span></span></p></td>
<td><p><span data-ttu-id="5d58c-126">X</span><span class="sxs-lookup"><span data-stu-id="5d58c-126">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d58c-127">テーブルの作成</span><span class="sxs-lookup"><span data-stu-id="5d58c-127">Create Tables</span></span></p></td>
<td><p><span data-ttu-id="5d58c-128">X</span><span class="sxs-lookup"><span data-stu-id="5d58c-128">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="5d58c-129">X</span><span class="sxs-lookup"><span data-stu-id="5d58c-129">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d58c-130">新しいデータベース</span><span class="sxs-lookup"><span data-stu-id="5d58c-130">Create New Database</span></span></p></td>
<td><p><span data-ttu-id="5d58c-131">X</span><span class="sxs-lookup"><span data-stu-id="5d58c-131">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="5d58c-132">X\*</span><span class="sxs-lookup"><span data-stu-id="5d58c-132">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d58c-133">既存のテーブルのプロパティの編集</span><span class="sxs-lookup"><span data-stu-id="5d58c-133">Edit Existing Table properties</span></span></p></td>
<td><p><span data-ttu-id="5d58c-134">X</span><span class="sxs-lookup"><span data-stu-id="5d58c-134">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="5d58c-135">X</span><span class="sxs-lookup"><span data-stu-id="5d58c-135">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d58c-136">テーブルのリレーションシップの作成</span><span class="sxs-lookup"><span data-stu-id="5d58c-136">Create table relationships</span></span></p></td>
<td><p><span data-ttu-id="5d58c-137">X</span><span class="sxs-lookup"><span data-stu-id="5d58c-137">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="5d58c-138">X\*</span><span class="sxs-lookup"><span data-stu-id="5d58c-138">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d58c-139">セキュリティ設定値の編集</span><span class="sxs-lookup"><span data-stu-id="5d58c-139">Edit security settings</span></span></p></td>
<td><p><span data-ttu-id="5d58c-140">X</span><span class="sxs-lookup"><span data-stu-id="5d58c-140">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="5d58c-141">X\*</span><span class="sxs-lookup"><span data-stu-id="5d58c-141">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d58c-142">列データの圧縮属性のサポート</span><span class="sxs-lookup"><span data-stu-id="5d58c-142">Support for Compression attribute for column data</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="5d58c-143">X</span><span class="sxs-lookup"><span data-stu-id="5d58c-143">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d58c-144">格納された基本 SQL クエリまたはビューの編集</span><span class="sxs-lookup"><span data-stu-id="5d58c-144">Edit stored, basic SQL queries or views</span></span></p></td>
<td><p><span data-ttu-id="5d58c-145">X</span><span class="sxs-lookup"><span data-stu-id="5d58c-145">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="5d58c-146">X\*</span><span class="sxs-lookup"><span data-stu-id="5d58c-146">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d58c-147">コードでのみアクセス可能なパーマネント クエリの作成</span><span class="sxs-lookup"><span data-stu-id="5d58c-147">Create permanent queries that are accessible only through code.</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="5d58c-148">X\*</span><span class="sxs-lookup"><span data-stu-id="5d58c-148">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d58c-149">コンテナー/UI およびコードでアクセス可能なクエリの作成</span><span class="sxs-lookup"><span data-stu-id="5d58c-149">Create queries accessible through database container/UI and code.</span></span></p></td>
<td><p><span data-ttu-id="5d58c-150">X</span><span class="sxs-lookup"><span data-stu-id="5d58c-150">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d58c-151">データベースの最適化/エンコード</span><span class="sxs-lookup"><span data-stu-id="5d58c-151">Compact/Encode database</span></span></p></td>
<td><p><span data-ttu-id="5d58c-152">X</span><span class="sxs-lookup"><span data-stu-id="5d58c-152">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="5d58c-153">X4</span><span class="sxs-lookup"><span data-stu-id="5d58c-153">X4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d58c-154">キャッシュの更新</span><span class="sxs-lookup"><span data-stu-id="5d58c-154">Refresh Cache</span></span></p></td>
<td><p><span data-ttu-id="5d58c-155">X</span><span class="sxs-lookup"><span data-stu-id="5d58c-155">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="5d58c-156">X</span><span class="sxs-lookup"><span data-stu-id="5d58c-156">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d58c-157">データベースをレプリケート可能にする</span><span class="sxs-lookup"><span data-stu-id="5d58c-157">Make Database Replicable</span></span></p></td>
<td><p><span data-ttu-id="5d58c-158">X</span><span class="sxs-lookup"><span data-stu-id="5d58c-158">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="5d58c-159">X3</span><span class="sxs-lookup"><span data-stu-id="5d58c-159">X3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d58c-160">データベース レプリカの作成</span><span class="sxs-lookup"><span data-stu-id="5d58c-160">Make Database Replicas</span></span></p></td>
<td><p><span data-ttu-id="5d58c-161">X</span><span class="sxs-lookup"><span data-stu-id="5d58c-161">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="5d58c-162">X3</span><span class="sxs-lookup"><span data-stu-id="5d58c-162">X3</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d58c-163">レプリカの同期をとる</span><span class="sxs-lookup"><span data-stu-id="5d58c-163">Synchronize Replicas</span></span></p></td>
<td><p><span data-ttu-id="5d58c-164">X</span><span class="sxs-lookup"><span data-stu-id="5d58c-164">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="5d58c-165">X3</span><span class="sxs-lookup"><span data-stu-id="5d58c-165">X3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d58c-166">データベース プロパティの編集</span><span class="sxs-lookup"><span data-stu-id="5d58c-166">Edit Database properties</span></span></p></td>
<td><p><span data-ttu-id="5d58c-167">X</span><span class="sxs-lookup"><span data-stu-id="5d58c-167">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d58c-168">カスタム データベース プロパティの作成</span><span class="sxs-lookup"><span data-stu-id="5d58c-168">Create custom database properties</span></span></p></td>
<td><p><span data-ttu-id="5d58c-169">X</span><span class="sxs-lookup"><span data-stu-id="5d58c-169">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d58c-170">列のプロパティの編集</span><span class="sxs-lookup"><span data-stu-id="5d58c-170">Edit table column properties</span></span></p></td>
<td><p><span data-ttu-id="5d58c-171">X</span><span class="sxs-lookup"><span data-stu-id="5d58c-171">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5d58c-p101">\* Microsoft Access データベースを操作するときのみ使用できます。SQL プロバイダーの将来のバージョンでは、この機能は Microsoft Access プロジェクト (.adp) で提供される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="5d58c-p101">\* Only available when working with Microsoft Access databases. Future versions of the SQL Provider may provide this functionality in Microsoft Access projects (.adp).</span></span>

<span data-ttu-id="5d58c-174">\*\* Access プロジェクトを操作するときのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="5d58c-174">\*\* Only available when working with Access projects.</span></span>

<span data-ttu-id="5d58c-175">\*\*\* Access データベース エンジンは、ANSI 92 SQL のいくつかをサポートしていますが、ANSI92 完全対応ではありません。</span><span class="sxs-lookup"><span data-stu-id="5d58c-175">\*\*\* Though the Access database engine does support some ANSI 92 SQL it is not yet fully ANSI92 compliant.</span></span>

<span data-ttu-id="5d58c-176">1データベースの参照には、 **Connection** オブジェクトを使用します。</span><span class="sxs-lookup"><span data-stu-id="5d58c-176">1 Uses **Connection** object to reference to database</span></span>

<span data-ttu-id="5d58c-177">2データベースの参照には、 **Catalog** オブジェクトを使用します。</span><span class="sxs-lookup"><span data-stu-id="5d58c-177">2 Uses **Catalog** object to reference database</span></span>

<span data-ttu-id="5d58c-178">3データベースの参照には、 **Replica** オブジェクトを使用します。</span><span class="sxs-lookup"><span data-stu-id="5d58c-178">3 Uses **Replica** object to reference database</span></span>

<span data-ttu-id="5d58c-179">4データベースの参照には、 **JetEngine** オブジェクトを使用します。</span><span class="sxs-lookup"><span data-stu-id="5d58c-179">4 Uses **JetEngine** object to reference database</span></span>


> [!NOTE]
> <P><span data-ttu-id="5d58c-180">DAO とは異なり、ADO および ADOX オブジェクトは、上記の印がついている動作を Jet ではなく、データベースで実行できます。ただし、使用するデータベースのプロバイダーが、それらの動作をサポートしている場合に限ります。</span><span class="sxs-lookup"><span data-stu-id="5d58c-180">Unlike DAO, ADO and ADOX objects can perform the marked actions in databases other then Jet as long as the provider for those databases supports that action.</span></span></P>


