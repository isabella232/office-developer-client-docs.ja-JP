---
title: プロバイダー ADOX のサポート
TOCTitle: Provider support for ADOX
ms:assetid: 32ea3236-d69f-df94-1685-d8791aeb9e0f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249100(v=office.15)
ms:contentKeyID: 48544091
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bdd9ca9a2274f03f1592f73c3da5a6837101fda2
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947827"
---
# <a name="provider-support-for-adox"></a><span data-ttu-id="4adfa-102">プロバイダー ADOX のサポート</span><span class="sxs-lookup"><span data-stu-id="4adfa-102">Provider support for ADOX</span></span>


<span data-ttu-id="4adfa-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="4adfa-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4adfa-p101">使用している OLE DB データ プロバイダーによっては、ADOX の特定の機能がサポートされていないことがあります。[Microsoft OLE DB Provider for Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md) の場合、ADOX は完全にサポートされています。 [Microsoft OLE DB Provider for SQL Server](microsoft-ole-db-provider-for-sql-server.md)、[Microsoft OLE DB Provider for ODBC](microsoft-ole-db-provider-for-odbc.md)、または [Microsoft OLE DB Provider for Oracle](microsoft-ole-db-provider-for-oracle.md) でサポートされていない機能の一覧を以下に示します。ADOX は、その他の Microsoft OLE DB プロバイダーではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="4adfa-p101">Certain features of ADOX are unsupported, depending upon your OLE DB data provider. ADOX is fully supported with the [OLE DB Provider for Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md). The unsupported features with the [Microsoft OLE DB Provider for SQL Server](microsoft-ole-db-provider-for-sql-server.md), the [Microsoft OLE DB Provider for ODBC](microsoft-ole-db-provider-for-odbc.md), or the [Microsoft OLE DB Provider for Oracle](microsoft-ole-db-provider-for-oracle.md) are listed below. ADOX is not supported by any other Microsoft OLE DB providers.</span></span>

## <a name="microsoft-ole-db-provider-for-sql-server"></a><span data-ttu-id="4adfa-108">Microsoft OLE DB Provider for SQL Server</span><span class="sxs-lookup"><span data-stu-id="4adfa-108">Microsoft OLE DB Provider for SQL Server</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4adfa-109">オブジェクトまたはコレクション</span><span class="sxs-lookup"><span data-stu-id="4adfa-109">Object or Collection</span></span></p></th>
<th><p><span data-ttu-id="4adfa-110">使用制限</span><span class="sxs-lookup"><span data-stu-id="4adfa-110">Usage Restriction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4adfa-111"><strong>Catalog</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="4adfa-111"><strong>Catalog</strong> object</span></span></p></td>
<td><p><span data-ttu-id="4adfa-112"><strong>Create</strong> メソッドはサポートされません。</span><span class="sxs-lookup"><span data-stu-id="4adfa-112">The <strong>Create</strong> method is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4adfa-113"><strong>Tables</strong> コレクション</span><span class="sxs-lookup"><span data-stu-id="4adfa-113"><strong>Tables</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="4adfa-114">オブジェクトの作成前はプロパティ値の取得および設定が可能で、既存のオプジェクトを参照する場合は値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="4adfa-114">Properties are read/write prior to object creation, and read-only when referencing an existing object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4adfa-115"><strong>Views</strong> コレクション</span><span class="sxs-lookup"><span data-stu-id="4adfa-115"><strong>Views</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="4adfa-116"><strong>Views</strong> はサポートされません。</span><span class="sxs-lookup"><span data-stu-id="4adfa-116"><strong>Views</strong> is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4adfa-117"><strong>プロシージャ</strong>のコレクション</span><span class="sxs-lookup"><span data-stu-id="4adfa-117"><strong>Procedures</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="4adfa-118"><strong>Append</strong> メソッドおよび <strong>Delete</strong> メソッドはサポートされません。</span><span class="sxs-lookup"><span data-stu-id="4adfa-118">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4adfa-119"><strong>Procedure</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="4adfa-119"><strong>Procedure</strong> object</span></span></p></td>
<td><p><span data-ttu-id="4adfa-120"><strong>Command</strong> プロパティはサポートされません。</span><span class="sxs-lookup"><span data-stu-id="4adfa-120">The <strong>Command</strong> property is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4adfa-121"><strong>Keys</strong>コレクション</span><span class="sxs-lookup"><span data-stu-id="4adfa-121"><strong>Keys</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="4adfa-122"><strong>Append</strong> メソッドおよび <strong>Delete</strong> メソッドはサポートされません。</span><span class="sxs-lookup"><span data-stu-id="4adfa-122">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4adfa-123"><strong>Users</strong>コレクション</span><span class="sxs-lookup"><span data-stu-id="4adfa-123"><strong>Users</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="4adfa-124"><strong>Users</strong> はサポートされません。</span><span class="sxs-lookup"><span data-stu-id="4adfa-124"><strong>Users</strong> is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4adfa-125"><strong>グループ</strong>コレクション</span><span class="sxs-lookup"><span data-stu-id="4adfa-125"><strong>Groups</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="4adfa-126"><strong>Groups</strong> はサポートされません。</span><span class="sxs-lookup"><span data-stu-id="4adfa-126"><strong>Groups</strong> is not supported.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="microsoft-ole-db-provider-for-odbc"></a><span data-ttu-id="4adfa-127">Microsoft OLE DB Provider for ODBC</span><span class="sxs-lookup"><span data-stu-id="4adfa-127">Microsoft OLE DB Provider for ODBC</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4adfa-128">オブジェクトまたはコレクション</span><span class="sxs-lookup"><span data-stu-id="4adfa-128">Object or Collection</span></span></p></th>
<th><p><span data-ttu-id="4adfa-129">使用制限</span><span class="sxs-lookup"><span data-stu-id="4adfa-129">Usage Restriction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4adfa-130"><strong>Catalog</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="4adfa-130"><strong>Catalog</strong> object</span></span></p></td>
<td><p><span data-ttu-id="4adfa-131"><strong>Create</strong> メソッドはサポートされません。</span><span class="sxs-lookup"><span data-stu-id="4adfa-131">The <strong>Create</strong> method is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4adfa-132"><strong>テーブル</strong>コレクション</span><span class="sxs-lookup"><span data-stu-id="4adfa-132"><strong>Tables</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="4adfa-133"><strong>Append</strong> メソッドおよび <strong>Delete</strong> メソッドはサポートされません。
</span><span class="sxs-lookup"><span data-stu-id="4adfa-133">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span> <span data-ttu-id="4adfa-134">オブジェクトの作成前はプロパティ値の取得および設定が可能で、既存のオプジェクトを参照する場合は値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="4adfa-134">Properties are read/write prior to object creation, and read-only when referencing an existing object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4adfa-135"><strong>Procedures</strong> コレクション</span><span class="sxs-lookup"><span data-stu-id="4adfa-135"><strong>Procedures</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="4adfa-136"><strong>Append</strong> メソッドおよび <strong>Delete</strong> メソッドはサポートされません。</span><span class="sxs-lookup"><span data-stu-id="4adfa-136">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4adfa-137"><strong>Procedure</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="4adfa-137"><strong>Procedure</strong> object</span></span></p></td>
<td><p><span data-ttu-id="4adfa-138"><strong>Command</strong> プロパティはサポートされません。</span><span class="sxs-lookup"><span data-stu-id="4adfa-138">The <strong>Command</strong> property is not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4adfa-139"><strong>インデックス</strong>コレクション</span><span class="sxs-lookup"><span data-stu-id="4adfa-139"><strong>Indexes</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="4adfa-140"><strong>Append</strong> メソッドおよび <strong>Delete</strong> メソッドはサポートされません。</span><span class="sxs-lookup"><span data-stu-id="4adfa-140">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4adfa-141"><strong>Keys</strong>コレクション</span><span class="sxs-lookup"><span data-stu-id="4adfa-141"><strong>Keys</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="4adfa-142"><strong>Append</strong> メソッドおよび <strong>Delete</strong> メソッドはサポートされません。</span><span class="sxs-lookup"><span data-stu-id="4adfa-142">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4adfa-143"><strong>Users</strong>コレクション</span><span class="sxs-lookup"><span data-stu-id="4adfa-143"><strong>Users</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="4adfa-144"><strong>Users</strong> はサポートされません。</span><span class="sxs-lookup"><span data-stu-id="4adfa-144"><strong>Users</strong> is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4adfa-145"><strong>グループ</strong>コレクション</span><span class="sxs-lookup"><span data-stu-id="4adfa-145"><strong>Groups</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="4adfa-146"><strong>Groups</strong> はサポートされません。</span><span class="sxs-lookup"><span data-stu-id="4adfa-146"><strong>Groups</strong> is not supported.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="microsoft-ole-db-provider-for-oracle"></a><span data-ttu-id="4adfa-147">Microsoft OLE DB Provider for Oracle</span><span class="sxs-lookup"><span data-stu-id="4adfa-147">Microsoft OLE DB Provider for Oracle</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4adfa-148">オブジェクトまたはコレクション</span><span class="sxs-lookup"><span data-stu-id="4adfa-148">Object or Collection</span></span></p></th>
<th><p><span data-ttu-id="4adfa-149">使用制限</span><span class="sxs-lookup"><span data-stu-id="4adfa-149">Usage Restriction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4adfa-150"><strong>Catalog</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="4adfa-150"><strong>Catalog</strong> object</span></span></p></td>
<td><p><span data-ttu-id="4adfa-151"><strong>Create</strong> メソッドはサポートされません。</span><span class="sxs-lookup"><span data-stu-id="4adfa-151">The <strong>Create</strong> method is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4adfa-152"><strong>テーブル</strong>コレクション</span><span class="sxs-lookup"><span data-stu-id="4adfa-152"><strong>Tables</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="4adfa-153"><strong>Append</strong> メソッドおよび <strong>Delete</strong> メソッドはサポートされません。
</span><span class="sxs-lookup"><span data-stu-id="4adfa-153">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span> <span data-ttu-id="4adfa-154">オブジェクトの作成前はプロパティ値の取得および設定が可能で、既存のオプジェクトを参照する場合は値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="4adfa-154">Properties are read/write prior to object creation, and read-only when referencing an existing object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4adfa-155"><strong>Views</strong> コレクション</span><span class="sxs-lookup"><span data-stu-id="4adfa-155"><strong>Views</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="4adfa-156"><strong>Append</strong> メソッドおよび <strong>Delete</strong> メソッドはサポートされません。</span><span class="sxs-lookup"><span data-stu-id="4adfa-156">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4adfa-157"><strong>ビュー</strong>オブジェクト</span><span class="sxs-lookup"><span data-stu-id="4adfa-157"><strong>View</strong> object</span></span></p></td>
<td><p><span data-ttu-id="4adfa-158"><strong>Command</strong> プロパティはサポートされません。</span><span class="sxs-lookup"><span data-stu-id="4adfa-158">The <strong>Command</strong> property is not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4adfa-159"><strong>Procedures</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="4adfa-159"><strong>Procedures</strong> object</span></span></p></td>
<td><p><span data-ttu-id="4adfa-160"><strong>Append</strong> メソッドおよび <strong>Delete</strong> メソッドはサポートされません。</span><span class="sxs-lookup"><span data-stu-id="4adfa-160">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4adfa-161"><strong>Procedure</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="4adfa-161"><strong>Procedure</strong> object</span></span></p></td>
<td><p><span data-ttu-id="4adfa-162"><strong>Command</strong> プロパティはサポートされません。</span><span class="sxs-lookup"><span data-stu-id="4adfa-162">The <strong>Command</strong> property is not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4adfa-163"><strong>インデックス</strong>コレクション</span><span class="sxs-lookup"><span data-stu-id="4adfa-163"><strong>Indexes</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="4adfa-164"><strong>Append</strong> メソッドおよび <strong>Delete</strong> メソッドはサポートされません。</span><span class="sxs-lookup"><span data-stu-id="4adfa-164">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4adfa-165"><strong>Keys</strong>コレクション</span><span class="sxs-lookup"><span data-stu-id="4adfa-165"><strong>Keys</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="4adfa-166"><strong>Append</strong> メソッドおよび <strong>Delete</strong> メソッドはサポートされません。</span><span class="sxs-lookup"><span data-stu-id="4adfa-166">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4adfa-167"><strong>Users</strong>コレクション</span><span class="sxs-lookup"><span data-stu-id="4adfa-167"><strong>Users</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="4adfa-168"><strong>Users</strong> はサポートされません。</span><span class="sxs-lookup"><span data-stu-id="4adfa-168"><strong>Users</strong> is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4adfa-169"><strong>グループ</strong>コレクション</span><span class="sxs-lookup"><span data-stu-id="4adfa-169"><strong>Groups</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="4adfa-170"><strong>Groups</strong> はサポートされません。</span><span class="sxs-lookup"><span data-stu-id="4adfa-170"><strong>Groups</strong> is not supported.</span></span></p></td>
</tr>
</tbody>
</table>

