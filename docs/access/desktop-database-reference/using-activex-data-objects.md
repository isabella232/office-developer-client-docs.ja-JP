---
title: ActiveX データ オブジェクトを使う
TOCTitle: Use ActiveX Data Objects
description: Microsoft access では、Visual Basic を使用して access データベースとその関連データを作成、保守、および管理するための3つのオブジェクトモデルを使用できます。
ms:assetid: 64055c45-7a27-2296-468a-015362898329
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194969(v=office.15)
ms:contentKeyID: 48545279
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5285627
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 3b530db43a816e66b9fbef254984142aadf0b841
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312741"
---
# <a name="use-activex-data-objects"></a><span data-ttu-id="14319-103">ActiveX データ オブジェクトを使う</span><span class="sxs-lookup"><span data-stu-id="14319-103">Use ActiveX Data Objects</span></span>

<span data-ttu-id="14319-104">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="14319-104">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="14319-105">Microsoft access では、Visual Basic を使用して access データベースとその関連データを作成、保守、および管理するための3つのオブジェクトモデルを使用できます。</span><span class="sxs-lookup"><span data-stu-id="14319-105">Microsoft Access provides three object models to use in the creation, maintaining, and managing of your Access databases and their related data by using Visual Basic.</span></span>

## <a name="microsoft-activex-data-objects-ado"></a><span data-ttu-id="14319-106">ADO (ActiveX データ オブジェクト)</span><span class="sxs-lookup"><span data-stu-id="14319-106">Microsoft ActiveX Data Objects (ADO)</span></span>

<span data-ttu-id="14319-107">ADO には、指定されたデータソースからレコードを作成、保守、および削除するために必要なオブジェクトが含まれてます。</span><span class="sxs-lookup"><span data-stu-id="14319-107">ADO contains the objects needed to create, maintain, and delete records in a given datasource.</span></span>

## <a name="microsoft-ado-ext-for-ddl-and-security-adox"></a><span data-ttu-id="14319-108">DDL およびセキュリティのための Microsoft ADO ext (ADOX)</span><span class="sxs-lookup"><span data-stu-id="14319-108">Microsoft ADO ext. for DDL and security (ADOX)</span></span>

<span data-ttu-id="14319-109">ADOX には、セキュリティを管理するために必要なオブジェクトに加えて、新しいデータベースおよびその中に含まれるオブジェクトを作成するために必要なデータ定義言語 (DDL) オブジェクトが用意されています。</span><span class="sxs-lookup"><span data-stu-id="14319-109">ADOX provides the Data Definition Language (DDL) objects needed to create a new database and its contained objects in addition to the objects needed to manage security.</span></span>

### <a name="microsoft-jet-and-replication-objects-25-library-jro"></a><span data-ttu-id="14319-110">Microsoft Jet および Replication オブジェクト2.5 ライブラリ (JRO)</span><span class="sxs-lookup"><span data-stu-id="14319-110">Microsoft Jet and Replication Objects 2.5 library (JRO)</span></span>

<span data-ttu-id="14319-111">ADO オブジェクトは Microsoft Jet データベースに加えて多くのデータベースで動作するように設計されているため、jet 固有の機能が JRO ライブラリに分割されています。</span><span class="sxs-lookup"><span data-stu-id="14319-111">Because ADO objects were designed to work with many databases in addition to Microsoft Jet databases, functionality specific to Jet was broken out into the JRO library.</span></span>

<span data-ttu-id="14319-112">次の表は、各機能を DAO と比較したものです。</span><span class="sxs-lookup"><span data-stu-id="14319-112">The following table lists the functionality provided by each compared to DAO.</span></span>

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
<th><p><span data-ttu-id="14319-113">機能</span><span class="sxs-lookup"><span data-stu-id="14319-113">Functionality</span></span></p></th>
<th><p><span data-ttu-id="14319-114">DAO</span><span class="sxs-lookup"><span data-stu-id="14319-114">DAO</span></span></p></th>
<th><p><span data-ttu-id="14319-115">ADO1</span><span class="sxs-lookup"><span data-stu-id="14319-115">ADO1</span></span></p></th>
<th><p><span data-ttu-id="14319-116">ADOX2</span><span class="sxs-lookup"><span data-stu-id="14319-116">ADOX2</span></span></p></th>
<th><p><span data-ttu-id="14319-117">JRO</span><span class="sxs-lookup"><span data-stu-id="14319-117">JRO</span></span><br />
<span data-ttu-id="14319-118">(mdb のみ)</span><span class="sxs-lookup"><span data-stu-id="14319-118">(MDBs only)</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="14319-119">レコードセットを作成します。</span><span class="sxs-lookup"><span data-stu-id="14319-119">Create Recordsets.</span></span></p></td>
<td><p><span data-ttu-id="14319-120">X</span><span class="sxs-lookup"><span data-stu-id="14319-120">X</span></span></p></td>
<td><p><span data-ttu-id="14319-121">X</span><span class="sxs-lookup"><span data-stu-id="14319-121">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14319-122">スタートアッププロパティを編集します。</span><span class="sxs-lookup"><span data-stu-id="14319-122">Edit Startup properties.</span></span></p></td>
<td><p><span data-ttu-id="14319-123">X</span><span class="sxs-lookup"><span data-stu-id="14319-123">X</span></span></p></td>
<td><p><span data-ttu-id="14319-124">X \* \*</span><span class="sxs-lookup"><span data-stu-id="14319-124">X\*\*</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14319-125">ANSI92 SQL. \* \* \* をサポートします。</span><span class="sxs-lookup"><span data-stu-id="14319-125">Support ANSI92 SQL.\*\*\*</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="14319-126">X</span><span class="sxs-lookup"><span data-stu-id="14319-126">X</span></span></p></td>
<td><p><span data-ttu-id="14319-127">X</span><span class="sxs-lookup"><span data-stu-id="14319-127">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14319-128">テーブルを作成します。</span><span class="sxs-lookup"><span data-stu-id="14319-128">Create tables.</span></span></p></td>
<td><p><span data-ttu-id="14319-129">X</span><span class="sxs-lookup"><span data-stu-id="14319-129">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="14319-130">X</span><span class="sxs-lookup"><span data-stu-id="14319-130">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14319-131">新しいデータベースを作成します。</span><span class="sxs-lookup"><span data-stu-id="14319-131">Create new database.</span></span></p></td>
<td><p><span data-ttu-id="14319-132">X</span><span class="sxs-lookup"><span data-stu-id="14319-132">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="14319-133">エックス</span><span class="sxs-lookup"><span data-stu-id="14319-133">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14319-134">既存の表のプロパティを編集します。</span><span class="sxs-lookup"><span data-stu-id="14319-134">Edit existing table properties.</span></span></p></td>
<td><p><span data-ttu-id="14319-135">X</span><span class="sxs-lookup"><span data-stu-id="14319-135">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="14319-136">X</span><span class="sxs-lookup"><span data-stu-id="14319-136">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14319-137">テーブルのリレーションシップを作成します。</span><span class="sxs-lookup"><span data-stu-id="14319-137">Create table relationships.</span></span></p></td>
<td><p><span data-ttu-id="14319-138">X</span><span class="sxs-lookup"><span data-stu-id="14319-138">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="14319-139">エックス</span><span class="sxs-lookup"><span data-stu-id="14319-139">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14319-140">セキュリティ設定を編集します。</span><span class="sxs-lookup"><span data-stu-id="14319-140">Edit security settings.</span></span></p></td>
<td><p><span data-ttu-id="14319-141">X</span><span class="sxs-lookup"><span data-stu-id="14319-141">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="14319-142">エックス</span><span class="sxs-lookup"><span data-stu-id="14319-142">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14319-143">列データの圧縮属性のサポート。</span><span class="sxs-lookup"><span data-stu-id="14319-143">Support for Compression attribute for column data.</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="14319-144">X</span><span class="sxs-lookup"><span data-stu-id="14319-144">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14319-145">保存された基本的な SQL クエリまたはビューを編集します。</span><span class="sxs-lookup"><span data-stu-id="14319-145">Edit stored, basic SQL queries or views.</span></span></p></td>
<td><p><span data-ttu-id="14319-146">X</span><span class="sxs-lookup"><span data-stu-id="14319-146">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="14319-147">エックス</span><span class="sxs-lookup"><span data-stu-id="14319-147">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14319-148">コードでのみアクセス可能なパーマネント クエリの作成</span><span class="sxs-lookup"><span data-stu-id="14319-148">Create permanent queries that are accessible only through code.</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="14319-149">エックス</span><span class="sxs-lookup"><span data-stu-id="14319-149">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14319-150">コンテナー/UI およびコードでアクセス可能なクエリの作成</span><span class="sxs-lookup"><span data-stu-id="14319-150">Create queries accessible through database container/UI and code.</span></span></p></td>
<td><p><span data-ttu-id="14319-151">X</span><span class="sxs-lookup"><span data-stu-id="14319-151">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14319-152">データベースの最適化/エンコードを行います。</span><span class="sxs-lookup"><span data-stu-id="14319-152">Compact/encode database.</span></span></p></td>
<td><p><span data-ttu-id="14319-153">X</span><span class="sxs-lookup"><span data-stu-id="14319-153">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="14319-154">X4</span><span class="sxs-lookup"><span data-stu-id="14319-154">X4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14319-155">キャッシュを更新します。</span><span class="sxs-lookup"><span data-stu-id="14319-155">Refresh cache.</span></span></p></td>
<td><p><span data-ttu-id="14319-156">X</span><span class="sxs-lookup"><span data-stu-id="14319-156">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="14319-157">X</span><span class="sxs-lookup"><span data-stu-id="14319-157">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14319-158">データベースをレプリケート可能にします。</span><span class="sxs-lookup"><span data-stu-id="14319-158">Make database replicable.</span></span></p></td>
<td><p><span data-ttu-id="14319-159">X</span><span class="sxs-lookup"><span data-stu-id="14319-159">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="14319-160">X3</span><span class="sxs-lookup"><span data-stu-id="14319-160">X3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14319-161">データベースのレプリカを作成します。</span><span class="sxs-lookup"><span data-stu-id="14319-161">Make database replicas.</span></span></p></td>
<td><p><span data-ttu-id="14319-162">X</span><span class="sxs-lookup"><span data-stu-id="14319-162">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="14319-163">X3</span><span class="sxs-lookup"><span data-stu-id="14319-163">X3</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14319-164">レプリカを同期します。</span><span class="sxs-lookup"><span data-stu-id="14319-164">Synchronize replicas.</span></span></p></td>
<td><p><span data-ttu-id="14319-165">X</span><span class="sxs-lookup"><span data-stu-id="14319-165">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="14319-166">X3</span><span class="sxs-lookup"><span data-stu-id="14319-166">X3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14319-167">データベースのプロパティを編集します。</span><span class="sxs-lookup"><span data-stu-id="14319-167">Edit database properties.</span></span></p></td>
<td><p><span data-ttu-id="14319-168">X</span><span class="sxs-lookup"><span data-stu-id="14319-168">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14319-169">カスタムデータベースプロパティを作成します。</span><span class="sxs-lookup"><span data-stu-id="14319-169">Create custom database properties.</span></span></p></td>
<td><p><span data-ttu-id="14319-170">X</span><span class="sxs-lookup"><span data-stu-id="14319-170">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14319-171">テーブルの列のプロパティを編集します。</span><span class="sxs-lookup"><span data-stu-id="14319-171">Edit table column properties.</span></span></p></td>
<td><p><span data-ttu-id="14319-172">X</span><span class="sxs-lookup"><span data-stu-id="14319-172">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="14319-p101">\* Microsoft Access データベースを操作するときのみ使用できます。SQL プロバイダーの将来のバージョンでは、この機能は Microsoft Access プロジェクト (.adp) で提供される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="14319-p101">\* Only available when working with Microsoft Access databases. Future versions of the SQL Provider may provide this functionality in Microsoft Access projects (.adp).</span></span>

<span data-ttu-id="14319-175">\*\* Access プロジェクトを操作するときのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="14319-175">\*\* Only available when working with Access projects.</span></span>

<span data-ttu-id="14319-176">\*\*\*Access データベースエンジンはいくつかの ANSI 92 SQL をサポートしていますが、完全に ANSI92 に準拠しているわけではありません。</span><span class="sxs-lookup"><span data-stu-id="14319-176">\*\*\* Although the Access database engine does support some ANSI 92 SQL, it is not yet fully ANSI92-compliant.</span></span>

<span data-ttu-id="14319-177">1は**Connection**オブジェクトを使用してデータベースを参照します。</span><span class="sxs-lookup"><span data-stu-id="14319-177">1 Uses **Connection** object to reference database.</span></span>

<span data-ttu-id="14319-178">2は、 **Catalog**オブジェクトを使用してデータベースを参照します。</span><span class="sxs-lookup"><span data-stu-id="14319-178">2 Uses **Catalog** object to reference database.</span></span>

<span data-ttu-id="14319-179">3データベースを参照するのには、 **Replica**オブジェクトを使用します。</span><span class="sxs-lookup"><span data-stu-id="14319-179">3 Uses **Replica** object to reference database.</span></span>

<span data-ttu-id="14319-180">4 **JetEngine**オブジェクトを使用してデータベースを参照します。</span><span class="sxs-lookup"><span data-stu-id="14319-180">4 Uses **JetEngine** object to reference database.</span></span>


> [!NOTE]
> <span data-ttu-id="14319-181">DAO とは異なり、ADO および ADOX オブジェクトは、Jet 以外のデータベースでマークされたアクションを実行できます。これらのデータベースのプロバイダーがそのアクションをサポートしている場合に限ります。</span><span class="sxs-lookup"><span data-stu-id="14319-181">Unlike DAO, ADO and ADOX objects can perform the marked actions in databases other than Jet as long as the provider for those databases supports that action.</span></span>


