---
title: ActiveX データ オブジェクトを使う
TOCTitle: Use ActiveX Data Objects
description: Access には、保守、および Visual Basic を使用して、Access データベースとその関連データの管理、作成時に使用する 3 つのオブジェクト モデルが用意されています。
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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28719226"
---
# <a name="use-activex-data-objects"></a><span data-ttu-id="5c347-103">ActiveX データ オブジェクトを使う</span><span class="sxs-lookup"><span data-stu-id="5c347-103">Use ActiveX Data Objects</span></span>

<span data-ttu-id="5c347-104">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="5c347-104">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5c347-105">Access には、保守、および Visual Basic を使用して、Access データベースとその関連データの管理、作成時に使用する 3 つのオブジェクト モデルが用意されています。</span><span class="sxs-lookup"><span data-stu-id="5c347-105">Microsoft Access provides three object models to use in the creation, maintaining, and managing of your Access databases and their related data by using Visual Basic.</span></span>

## <a name="microsoft-activex-data-objects-ado"></a><span data-ttu-id="5c347-106">ADO (ActiveX データ オブジェクト)</span><span class="sxs-lookup"><span data-stu-id="5c347-106">Microsoft ActiveX Data Objects (ADO)</span></span>

<span data-ttu-id="5c347-107">ADO には、指定されたデータソースからレコードを作成、保守、および削除するために必要なオブジェクトが含まれてます。</span><span class="sxs-lookup"><span data-stu-id="5c347-107">ADO contains the objects needed to create, maintain, and delete records in a given datasource.</span></span>

## <a name="microsoft-ado-ext-for-ddl-and-security-adox"></a><span data-ttu-id="5c347-108">DDL とセキュリティ (ADOX) の ADO の拡張</span><span class="sxs-lookup"><span data-stu-id="5c347-108">Microsoft ADO ext. for DDL and security (ADOX)</span></span>

<span data-ttu-id="5c347-109">ADOX には、新しいデータベースを作成するために必要なデータ定義言語 (DDL) オブジェクト、およびセキュリティを管理するために必要なオブジェクトだけでなく内にあるオブジェクトが用意されています。</span><span class="sxs-lookup"><span data-stu-id="5c347-109">ADOX provides the Data Definition Language (DDL) objects needed to create a new database and its contained objects in addition to the objects needed to manage security.</span></span>

### <a name="microsoft-jet-and-replication-objects-25-library-jro"></a><span data-ttu-id="5c347-110">Microsoft Jet とレプリケーション オブジェクト 2.5 ライブラリ (JRO)</span><span class="sxs-lookup"><span data-stu-id="5c347-110">Microsoft Jet and Replication Objects 2.5 library (JRO)</span></span>

<span data-ttu-id="5c347-111">ADO オブジェクトは、Microsoft Jet データベースの他の多くのデータベースを操作するに設計されて、ため jet 固有の機能に分かれています。</span><span class="sxs-lookup"><span data-stu-id="5c347-111">Because ADO objects were designed to work with many databases in addition to Microsoft Jet databases, functionality specific to Jet was broken out into the JRO library.</span></span>

<span data-ttu-id="5c347-112">次の表は、各機能を DAO と比較したものです。</span><span class="sxs-lookup"><span data-stu-id="5c347-112">The following table lists the functionality provided by each compared to DAO.</span></span>

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
<th><p><span data-ttu-id="5c347-113">機能</span><span class="sxs-lookup"><span data-stu-id="5c347-113">Functionality</span></span></p></th>
<th><p><span data-ttu-id="5c347-114">DAO</span><span class="sxs-lookup"><span data-stu-id="5c347-114">DAO</span></span></p></th>
<th><p><span data-ttu-id="5c347-115">ADO1</span><span class="sxs-lookup"><span data-stu-id="5c347-115">ADO1</span></span></p></th>
<th><p><span data-ttu-id="5c347-116">ADOX2</span><span class="sxs-lookup"><span data-stu-id="5c347-116">ADOX2</span></span></p></th>
<th><p><span data-ttu-id="5c347-117">JRO</span><span class="sxs-lookup"><span data-stu-id="5c347-117">JRO</span></span><br />
<span data-ttu-id="5c347-118">(Mdb のみ)</span><span class="sxs-lookup"><span data-stu-id="5c347-118">(MDBs only)</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5c347-119">レコード セットを作成します。</span><span class="sxs-lookup"><span data-stu-id="5c347-119">Create Recordsets.</span></span></p></td>
<td><p><span data-ttu-id="5c347-120">X</span><span class="sxs-lookup"><span data-stu-id="5c347-120">X</span></span></p></td>
<td><p><span data-ttu-id="5c347-121">X</span><span class="sxs-lookup"><span data-stu-id="5c347-121">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c347-122">スタートアップ プロパティを編集します。</span><span class="sxs-lookup"><span data-stu-id="5c347-122">Edit Startup properties.</span></span></p></td>
<td><p><span data-ttu-id="5c347-123">X</span><span class="sxs-lookup"><span data-stu-id="5c347-123">X</span></span></p></td>
<td><p><span data-ttu-id="5c347-124">X\*\*</span><span class="sxs-lookup"><span data-stu-id="5c347-124">X\*\*</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c347-125">ANSI92 のサポート \* \* sql.\* パッケージ</span><span class="sxs-lookup"><span data-stu-id="5c347-125">Support ANSI92 SQL.\*\*\*</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="5c347-126">X</span><span class="sxs-lookup"><span data-stu-id="5c347-126">X</span></span></p></td>
<td><p><span data-ttu-id="5c347-127">X</span><span class="sxs-lookup"><span data-stu-id="5c347-127">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c347-128">テーブルを作成します。</span><span class="sxs-lookup"><span data-stu-id="5c347-128">Create tables.</span></span></p></td>
<td><p><span data-ttu-id="5c347-129">X</span><span class="sxs-lookup"><span data-stu-id="5c347-129">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="5c347-130">X</span><span class="sxs-lookup"><span data-stu-id="5c347-130">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c347-131">新しいデータベースを作成します。</span><span class="sxs-lookup"><span data-stu-id="5c347-131">Create new database.</span></span></p></td>
<td><p><span data-ttu-id="5c347-132">X</span><span class="sxs-lookup"><span data-stu-id="5c347-132">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="5c347-133">X\*</span><span class="sxs-lookup"><span data-stu-id="5c347-133">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c347-134">既存のテーブルのプロパティを編集します。</span><span class="sxs-lookup"><span data-stu-id="5c347-134">Edit existing table properties.</span></span></p></td>
<td><p><span data-ttu-id="5c347-135">X</span><span class="sxs-lookup"><span data-stu-id="5c347-135">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="5c347-136">X</span><span class="sxs-lookup"><span data-stu-id="5c347-136">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c347-137">テーブル間のリレーションシップを作成します。</span><span class="sxs-lookup"><span data-stu-id="5c347-137">Create table relationships.</span></span></p></td>
<td><p><span data-ttu-id="5c347-138">X</span><span class="sxs-lookup"><span data-stu-id="5c347-138">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="5c347-139">X\*</span><span class="sxs-lookup"><span data-stu-id="5c347-139">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c347-140">セキュリティの設定を編集します。</span><span class="sxs-lookup"><span data-stu-id="5c347-140">Edit security settings.</span></span></p></td>
<td><p><span data-ttu-id="5c347-141">X</span><span class="sxs-lookup"><span data-stu-id="5c347-141">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="5c347-142">X\*</span><span class="sxs-lookup"><span data-stu-id="5c347-142">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c347-143">列のデータの圧縮の属性をサポートします。</span><span class="sxs-lookup"><span data-stu-id="5c347-143">Support for Compression attribute for column data.</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="5c347-144">X</span><span class="sxs-lookup"><span data-stu-id="5c347-144">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c347-145">格納された基本 SQL クエリまたはビューを編集します。</span><span class="sxs-lookup"><span data-stu-id="5c347-145">Edit stored, basic SQL queries or views.</span></span></p></td>
<td><p><span data-ttu-id="5c347-146">X</span><span class="sxs-lookup"><span data-stu-id="5c347-146">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="5c347-147">X\*</span><span class="sxs-lookup"><span data-stu-id="5c347-147">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c347-148">コードでのみアクセス可能なパーマネント クエリの作成</span><span class="sxs-lookup"><span data-stu-id="5c347-148">Create permanent queries that are accessible only through code.</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="5c347-149">X\*</span><span class="sxs-lookup"><span data-stu-id="5c347-149">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c347-150">コンテナー/UI およびコードでアクセス可能なクエリの作成</span><span class="sxs-lookup"><span data-stu-id="5c347-150">Create queries accessible through database container/UI and code.</span></span></p></td>
<td><p><span data-ttu-id="5c347-151">X</span><span class="sxs-lookup"><span data-stu-id="5c347-151">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c347-152">データベースの最適化/エンコードします。</span><span class="sxs-lookup"><span data-stu-id="5c347-152">Compact/encode database.</span></span></p></td>
<td><p><span data-ttu-id="5c347-153">X</span><span class="sxs-lookup"><span data-stu-id="5c347-153">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="5c347-154">X4</span><span class="sxs-lookup"><span data-stu-id="5c347-154">X4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c347-155">キャッシュを更新します。</span><span class="sxs-lookup"><span data-stu-id="5c347-155">Refresh cache.</span></span></p></td>
<td><p><span data-ttu-id="5c347-156">X</span><span class="sxs-lookup"><span data-stu-id="5c347-156">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="5c347-157">X</span><span class="sxs-lookup"><span data-stu-id="5c347-157">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c347-158">データベースをレプリケート可能にします。</span><span class="sxs-lookup"><span data-stu-id="5c347-158">Make database replicable.</span></span></p></td>
<td><p><span data-ttu-id="5c347-159">X</span><span class="sxs-lookup"><span data-stu-id="5c347-159">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="5c347-160">X3</span><span class="sxs-lookup"><span data-stu-id="5c347-160">X3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c347-161">データベースのレプリカを作成します。</span><span class="sxs-lookup"><span data-stu-id="5c347-161">Make database replicas.</span></span></p></td>
<td><p><span data-ttu-id="5c347-162">X</span><span class="sxs-lookup"><span data-stu-id="5c347-162">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="5c347-163">X3</span><span class="sxs-lookup"><span data-stu-id="5c347-163">X3</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c347-164">レプリカを同期します。</span><span class="sxs-lookup"><span data-stu-id="5c347-164">Synchronize replicas.</span></span></p></td>
<td><p><span data-ttu-id="5c347-165">X</span><span class="sxs-lookup"><span data-stu-id="5c347-165">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="5c347-166">X3</span><span class="sxs-lookup"><span data-stu-id="5c347-166">X3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c347-167">データベースのプロパティを編集します。</span><span class="sxs-lookup"><span data-stu-id="5c347-167">Edit database properties.</span></span></p></td>
<td><p><span data-ttu-id="5c347-168">X</span><span class="sxs-lookup"><span data-stu-id="5c347-168">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c347-169">カスタム データベース プロパティを作成します。</span><span class="sxs-lookup"><span data-stu-id="5c347-169">Create custom database properties.</span></span></p></td>
<td><p><span data-ttu-id="5c347-170">X</span><span class="sxs-lookup"><span data-stu-id="5c347-170">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c347-171">テーブルの列のプロパティを編集します。</span><span class="sxs-lookup"><span data-stu-id="5c347-171">Edit table column properties.</span></span></p></td>
<td><p><span data-ttu-id="5c347-172">X</span><span class="sxs-lookup"><span data-stu-id="5c347-172">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5c347-p101">\* Microsoft Access データベースを操作するときのみ使用できます。SQL プロバイダーの将来のバージョンでは、この機能は Microsoft Access プロジェクト (.adp) で提供される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="5c347-p101">\* Only available when working with Microsoft Access databases. Future versions of the SQL Provider may provide this functionality in Microsoft Access projects (.adp).</span></span>

<span data-ttu-id="5c347-175">\*\* Access プロジェクトを操作するときのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="5c347-175">\*\* Only available when working with Access projects.</span></span>

<span data-ttu-id="5c347-176">\*\*\*Access データベース エンジンは、いくつかの ANSI 92 SQL をサポートして、その準拠ではありませんまだ完全に ANSI92 です。</span><span class="sxs-lookup"><span data-stu-id="5c347-176">\*\*\* Although the Access database engine does support some ANSI 92 SQL, it is not yet fully ANSI92-compliant.</span></span>

<span data-ttu-id="5c347-177">リファレンス ・ データベースを使用して**接続**オブジェクトを 1 です。</span><span class="sxs-lookup"><span data-stu-id="5c347-177">1 Uses **Connection** object to reference database.</span></span>

<span data-ttu-id="5c347-178">2 は**カタログ**データベースにオブジェクトを参照します。</span><span class="sxs-lookup"><span data-stu-id="5c347-178">2 Uses **Catalog** object to reference database.</span></span>

<span data-ttu-id="5c347-179">3 使用**レプリカ**データベースにオブジェクトを参照します。</span><span class="sxs-lookup"><span data-stu-id="5c347-179">3 Uses **Replica** object to reference database.</span></span>

<span data-ttu-id="5c347-180">4 使用**JetEngine**データベースにオブジェクトを参照します。</span><span class="sxs-lookup"><span data-stu-id="5c347-180">4 Uses **JetEngine** object to reference database.</span></span>


> [!NOTE]
> <span data-ttu-id="5c347-181">DAO とは異なり ADO および ADOX オブジェクトはこれらのデータベース用のプロバイダーは、そのアクションをサポートしている限り、Jet 以外のデータベースにマークされたアクションを実行できます。</span><span class="sxs-lookup"><span data-stu-id="5c347-181">Unlike DAO, ADO and ADOX objects can perform the marked actions in databases other than Jet as long as the provider for those databases supports that action.</span></span>


