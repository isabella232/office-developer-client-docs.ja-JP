---
title: ActiveX データ オブジェクトを使用します。
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
ms.openlocfilehash: d7e8e7e6abeea9cca86c928760eddb990517a207
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887510"
---
# <a name="use-activex-data-objects"></a><span data-ttu-id="5af98-103">ActiveX データ オブジェクトを使用します。</span><span class="sxs-lookup"><span data-stu-id="5af98-103">Use ActiveX Data Objects</span></span>

<span data-ttu-id="5af98-104">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="5af98-104">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5af98-105">Access には、保守、および Visual Basic を使用して、Access データベースとその関連データの管理、作成時に使用する 3 つのオブジェクト モデルが用意されています。</span><span class="sxs-lookup"><span data-stu-id="5af98-105">Microsoft Access provides three object models to use in the creation, maintaining, and managing of your Access databases and their related data by using Visual Basic.</span></span>

## <a name="microsoft-activex-data-objects-ado"></a><span data-ttu-id="5af98-106">ADO (ActiveX データ オブジェクト)</span><span class="sxs-lookup"><span data-stu-id="5af98-106">Microsoft ActiveX Data Objects (ADO)</span></span>

<span data-ttu-id="5af98-107">ADO には、指定されたデータソースからレコードを作成、保守、および削除するために必要なオブジェクトが含まれてます。</span><span class="sxs-lookup"><span data-stu-id="5af98-107">ADO contains the objects needed to create, maintain, and delete records in a given datasource.</span></span>

## <a name="microsoft-ado-ext-for-ddl-and-security-adox"></a><span data-ttu-id="5af98-108">DDL とセキュリティ (ADOX) の ADO の拡張</span><span class="sxs-lookup"><span data-stu-id="5af98-108">Microsoft ADO ext. for DDL and security (ADOX)</span></span>

<span data-ttu-id="5af98-109">ADOX には、新しいデータベースを作成するために必要なデータ定義言語 (DDL) オブジェクト、およびセキュリティを管理するために必要なオブジェクトだけでなく内にあるオブジェクトが用意されています。</span><span class="sxs-lookup"><span data-stu-id="5af98-109">ADOX provides the Data Definition Language (DDL) objects needed to create a new database and its contained objects in addition to the objects needed to manage security.</span></span>

### <a name="microsoft-jet-and-replication-objects-25-library-jro"></a><span data-ttu-id="5af98-110">Microsoft Jet とレプリケーション オブジェクト 2.5 ライブラリ (JRO)</span><span class="sxs-lookup"><span data-stu-id="5af98-110">Microsoft Jet and Replication Objects 2.5 library (JRO)</span></span>

<span data-ttu-id="5af98-111">ADO オブジェクトは、Microsoft Jet データベースの他の多くのデータベースを操作するに設計されて、ため jet 固有の機能に分かれています。</span><span class="sxs-lookup"><span data-stu-id="5af98-111">Because ADO objects were designed to work with many databases in addition to Microsoft Jet databases, functionality specific to Jet was broken out into the JRO library.</span></span>

<span data-ttu-id="5af98-112">次の表は、各機能を DAO と比較したものです。</span><span class="sxs-lookup"><span data-stu-id="5af98-112">The following table lists the functionality provided by each compared to DAO.</span></span>

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
<th><p><span data-ttu-id="5af98-113">機能</span><span class="sxs-lookup"><span data-stu-id="5af98-113">Functionality</span></span></p></th>
<th><p><span data-ttu-id="5af98-114">DAO</span><span class="sxs-lookup"><span data-stu-id="5af98-114">DAO</span></span></p></th>
<th><p><span data-ttu-id="5af98-115">ADO1</span><span class="sxs-lookup"><span data-stu-id="5af98-115">ADO1</span></span></p></th>
<th><p><span data-ttu-id="5af98-116">ADOX2</span><span class="sxs-lookup"><span data-stu-id="5af98-116">ADOX2</span></span></p></th>
<th><p><span data-ttu-id="5af98-117">JRO</span><span class="sxs-lookup"><span data-stu-id="5af98-117">JRO</span></span><br />
<span data-ttu-id="5af98-118">(Mdb のみ)</span><span class="sxs-lookup"><span data-stu-id="5af98-118">(MDBs only)</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5af98-119">レコード セットを作成します。</span><span class="sxs-lookup"><span data-stu-id="5af98-119">Create Recordsets.</span></span></p></td>
<td><p><span data-ttu-id="5af98-120">X</span><span class="sxs-lookup"><span data-stu-id="5af98-120">X</span></span></p></td>
<td><p><span data-ttu-id="5af98-121">X</span><span class="sxs-lookup"><span data-stu-id="5af98-121">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5af98-122">スタートアップ プロパティを編集します。</span><span class="sxs-lookup"><span data-stu-id="5af98-122">Edit Startup properties.</span></span></p></td>
<td><p><span data-ttu-id="5af98-123">X</span><span class="sxs-lookup"><span data-stu-id="5af98-123">X</span></span></p></td>
<td><p><span data-ttu-id="5af98-124">X\*\*</span><span class="sxs-lookup"><span data-stu-id="5af98-124">X\*\*</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5af98-125">ANSI92 のサポート \* \* sql.\* パッケージ</span><span class="sxs-lookup"><span data-stu-id="5af98-125">Support ANSI92 SQL.\*\*\*</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="5af98-126">X</span><span class="sxs-lookup"><span data-stu-id="5af98-126">X</span></span></p></td>
<td><p><span data-ttu-id="5af98-127">X</span><span class="sxs-lookup"><span data-stu-id="5af98-127">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5af98-128">テーブルを作成します。</span><span class="sxs-lookup"><span data-stu-id="5af98-128">Create tables.</span></span></p></td>
<td><p><span data-ttu-id="5af98-129">X</span><span class="sxs-lookup"><span data-stu-id="5af98-129">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="5af98-130">X</span><span class="sxs-lookup"><span data-stu-id="5af98-130">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5af98-131">新しいデータベースを作成します。</span><span class="sxs-lookup"><span data-stu-id="5af98-131">Create new database.</span></span></p></td>
<td><p><span data-ttu-id="5af98-132">X</span><span class="sxs-lookup"><span data-stu-id="5af98-132">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="5af98-133">X\*</span><span class="sxs-lookup"><span data-stu-id="5af98-133">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5af98-134">既存のテーブルのプロパティを編集します。</span><span class="sxs-lookup"><span data-stu-id="5af98-134">Edit existing table properties.</span></span></p></td>
<td><p><span data-ttu-id="5af98-135">X</span><span class="sxs-lookup"><span data-stu-id="5af98-135">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="5af98-136">X</span><span class="sxs-lookup"><span data-stu-id="5af98-136">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5af98-137">テーブル間のリレーションシップを作成します。</span><span class="sxs-lookup"><span data-stu-id="5af98-137">Create table relationships.</span></span></p></td>
<td><p><span data-ttu-id="5af98-138">X</span><span class="sxs-lookup"><span data-stu-id="5af98-138">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="5af98-139">X\*</span><span class="sxs-lookup"><span data-stu-id="5af98-139">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5af98-140">セキュリティの設定を編集します。</span><span class="sxs-lookup"><span data-stu-id="5af98-140">Edit security settings.</span></span></p></td>
<td><p><span data-ttu-id="5af98-141">X</span><span class="sxs-lookup"><span data-stu-id="5af98-141">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="5af98-142">X\*</span><span class="sxs-lookup"><span data-stu-id="5af98-142">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5af98-143">列のデータの圧縮の属性をサポートします。</span><span class="sxs-lookup"><span data-stu-id="5af98-143">Support for Compression attribute for column data.</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="5af98-144">X</span><span class="sxs-lookup"><span data-stu-id="5af98-144">X</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5af98-145">格納された基本 SQL クエリまたはビューを編集します。</span><span class="sxs-lookup"><span data-stu-id="5af98-145">Edit stored, basic SQL queries or views.</span></span></p></td>
<td><p><span data-ttu-id="5af98-146">X</span><span class="sxs-lookup"><span data-stu-id="5af98-146">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="5af98-147">X\*</span><span class="sxs-lookup"><span data-stu-id="5af98-147">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5af98-148">コードでのみアクセス可能なパーマネント クエリの作成</span><span class="sxs-lookup"><span data-stu-id="5af98-148">Create permanent queries that are accessible only through code.</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="5af98-149">X\*</span><span class="sxs-lookup"><span data-stu-id="5af98-149">X\*</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5af98-150">コンテナー/UI およびコードでアクセス可能なクエリの作成</span><span class="sxs-lookup"><span data-stu-id="5af98-150">Create queries accessible through database container/UI and code.</span></span></p></td>
<td><p><span data-ttu-id="5af98-151">X</span><span class="sxs-lookup"><span data-stu-id="5af98-151">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5af98-152">データベースの最適化/エンコードします。</span><span class="sxs-lookup"><span data-stu-id="5af98-152">Compact/encode database.</span></span></p></td>
<td><p><span data-ttu-id="5af98-153">X</span><span class="sxs-lookup"><span data-stu-id="5af98-153">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="5af98-154">X4</span><span class="sxs-lookup"><span data-stu-id="5af98-154">X4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5af98-155">キャッシュを更新します。</span><span class="sxs-lookup"><span data-stu-id="5af98-155">Refresh cache.</span></span></p></td>
<td><p><span data-ttu-id="5af98-156">X</span><span class="sxs-lookup"><span data-stu-id="5af98-156">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="5af98-157">X</span><span class="sxs-lookup"><span data-stu-id="5af98-157">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5af98-158">データベースをレプリケート可能にします。</span><span class="sxs-lookup"><span data-stu-id="5af98-158">Make database replicable.</span></span></p></td>
<td><p><span data-ttu-id="5af98-159">X</span><span class="sxs-lookup"><span data-stu-id="5af98-159">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="5af98-160">X3</span><span class="sxs-lookup"><span data-stu-id="5af98-160">X3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5af98-161">データベースのレプリカを作成します。</span><span class="sxs-lookup"><span data-stu-id="5af98-161">Make database replicas.</span></span></p></td>
<td><p><span data-ttu-id="5af98-162">X</span><span class="sxs-lookup"><span data-stu-id="5af98-162">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="5af98-163">X3</span><span class="sxs-lookup"><span data-stu-id="5af98-163">X3</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5af98-164">レプリカを同期します。</span><span class="sxs-lookup"><span data-stu-id="5af98-164">Synchronize replicas.</span></span></p></td>
<td><p><span data-ttu-id="5af98-165">X</span><span class="sxs-lookup"><span data-stu-id="5af98-165">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="5af98-166">X3</span><span class="sxs-lookup"><span data-stu-id="5af98-166">X3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5af98-167">データベースのプロパティを編集します。</span><span class="sxs-lookup"><span data-stu-id="5af98-167">Edit database properties.</span></span></p></td>
<td><p><span data-ttu-id="5af98-168">X</span><span class="sxs-lookup"><span data-stu-id="5af98-168">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5af98-169">カスタム データベース プロパティを作成します。</span><span class="sxs-lookup"><span data-stu-id="5af98-169">Create custom database properties.</span></span></p></td>
<td><p><span data-ttu-id="5af98-170">X</span><span class="sxs-lookup"><span data-stu-id="5af98-170">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5af98-171">テーブルの列のプロパティを編集します。</span><span class="sxs-lookup"><span data-stu-id="5af98-171">Edit table column properties.</span></span></p></td>
<td><p><span data-ttu-id="5af98-172">X</span><span class="sxs-lookup"><span data-stu-id="5af98-172">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5af98-p101">\* Microsoft Access データベースを操作するときのみ使用できます。SQL プロバイダーの将来のバージョンでは、この機能は Microsoft Access プロジェクト (.adp) で提供される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="5af98-p101">\* Only available when working with Microsoft Access databases. Future versions of the SQL Provider may provide this functionality in Microsoft Access projects (.adp).</span></span>

<span data-ttu-id="5af98-175">\*\* Access プロジェクトを操作するときのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="5af98-175">\*\* Only available when working with Access projects.</span></span>

<span data-ttu-id="5af98-176">\*\*\*Access データベース エンジンは、いくつかの ANSI 92 SQL をサポートして、その準拠ではありませんまだ完全に ANSI92 です。</span><span class="sxs-lookup"><span data-stu-id="5af98-176">\*\*\* Although the Access database engine does support some ANSI 92 SQL, it is not yet fully ANSI92-compliant.</span></span>

<span data-ttu-id="5af98-177">リファレンス ・ データベースを使用して**接続**オブジェクトを 1 です。</span><span class="sxs-lookup"><span data-stu-id="5af98-177">1 Uses **Connection** object to reference database.</span></span>

<span data-ttu-id="5af98-178">2 は**カタログ**データベースにオブジェクトを参照します。</span><span class="sxs-lookup"><span data-stu-id="5af98-178">2 Uses **Catalog** object to reference database.</span></span>

<span data-ttu-id="5af98-179">3 使用**レプリカ**データベースにオブジェクトを参照します。</span><span class="sxs-lookup"><span data-stu-id="5af98-179">3 Uses **Replica** object to reference database.</span></span>

<span data-ttu-id="5af98-180">4 使用**JetEngine**データベースにオブジェクトを参照します。</span><span class="sxs-lookup"><span data-stu-id="5af98-180">4 Uses **JetEngine** object to reference database.</span></span>


> [!NOTE]
> <span data-ttu-id="5af98-181">DAO とは異なり ADO および ADOX オブジェクトはこれらのデータベース用のプロバイダーは、そのアクションをサポートしている限り、Jet 以外のデータベースにマークされたアクションを実行できます。</span><span class="sxs-lookup"><span data-stu-id="5af98-181">Unlike DAO, ADO and ADOX objects can perform the marked actions in databases other than Jet as long as the provider for those databases supports that action.</span></span>


