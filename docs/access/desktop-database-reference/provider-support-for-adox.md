---
title: ADOX のプロバイダー サポート
TOCTitle: Provider support for ADOX
ms:assetid: 32ea3236-d69f-df94-1685-d8791aeb9e0f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249100(v=office.15)
ms:contentKeyID: 48544091
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a92ffe9b4b713518330d9dbfd9979d904a5abe8e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703511"
---
# <a name="provider-support-for-adox"></a><span data-ttu-id="ae1b5-102">ADOX のプロバイダー サポート</span><span class="sxs-lookup"><span data-stu-id="ae1b5-102">Provider support for ADOX</span></span>


<span data-ttu-id="ae1b5-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="ae1b5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ae1b5-p101">使用している OLE DB データ プロバイダーによっては、ADOX の特定の機能がサポートされていないことがあります。[Microsoft OLE DB Provider for Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md) の場合、ADOX は完全にサポートされています。 [Microsoft OLE DB Provider for SQL Server](microsoft-ole-db-provider-for-sql-server.md)、[Microsoft OLE DB Provider for ODBC](microsoft-ole-db-provider-for-odbc.md)、または [Microsoft OLE DB Provider for Oracle](microsoft-ole-db-provider-for-oracle.md) でサポートされていない機能の一覧を以下に示します。ADOX は、その他の Microsoft OLE DB プロバイダーではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="ae1b5-p101">Certain features of ADOX are unsupported, depending upon your OLE DB data provider. ADOX is fully supported with the [OLE DB Provider for Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md). The unsupported features with the [Microsoft OLE DB Provider for SQL Server](microsoft-ole-db-provider-for-sql-server.md), the [Microsoft OLE DB Provider for ODBC](microsoft-ole-db-provider-for-odbc.md), or the [Microsoft OLE DB Provider for Oracle](microsoft-ole-db-provider-for-oracle.md) are listed below. ADOX is not supported by any other Microsoft OLE DB providers.</span></span>

## <a name="microsoft-ole-db-provider-for-sql-server"></a><span data-ttu-id="ae1b5-108">Microsoft OLE DB Provider for SQL Server</span><span class="sxs-lookup"><span data-stu-id="ae1b5-108">Microsoft OLE DB Provider for SQL Server</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ae1b5-109">オブジェクトまたはコレクション</span><span class="sxs-lookup"><span data-stu-id="ae1b5-109">Object or Collection</span></span></p></th>
<th><p><span data-ttu-id="ae1b5-110">使用制限</span><span class="sxs-lookup"><span data-stu-id="ae1b5-110">Usage Restriction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ae1b5-111"><strong>Catalog</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="ae1b5-111"><strong>Catalog</strong> object</span></span></p></td>
<td><p><span data-ttu-id="ae1b5-112"><strong>Create</strong> メソッドはサポートされません。</span><span class="sxs-lookup"><span data-stu-id="ae1b5-112">The <strong>Create</strong> method is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae1b5-113"><strong>Tables</strong> コレクション</span><span class="sxs-lookup"><span data-stu-id="ae1b5-113"><strong>Tables</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="ae1b5-114">オブジェクトの作成前はプロパティ値の取得および設定が可能で、既存のオプジェクトを参照する場合は値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="ae1b5-114">Properties are read/write prior to object creation, and read-only when referencing an existing object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae1b5-115"><strong>Views</strong> コレクション</span><span class="sxs-lookup"><span data-stu-id="ae1b5-115"><strong>Views</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="ae1b5-116"><strong>Views</strong> はサポートされません。</span><span class="sxs-lookup"><span data-stu-id="ae1b5-116"><strong>Views</strong> is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae1b5-117"><strong>プロシージャ</strong>のコレクション</span><span class="sxs-lookup"><span data-stu-id="ae1b5-117"><strong>Procedures</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="ae1b5-118"><strong>Append</strong> メソッドおよび <strong>Delete</strong> メソッドはサポートされません。</span><span class="sxs-lookup"><span data-stu-id="ae1b5-118">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae1b5-119"><strong>プロシージャ</strong>オブジェクト</span><span class="sxs-lookup"><span data-stu-id="ae1b5-119"><strong>Procedure</strong> object</span></span></p></td>
<td><p><span data-ttu-id="ae1b5-120"><strong>Command</strong> プロパティはサポートされません。</span><span class="sxs-lookup"><span data-stu-id="ae1b5-120">The <strong>Command</strong> property is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae1b5-121"><strong>Keys</strong>コレクション</span><span class="sxs-lookup"><span data-stu-id="ae1b5-121"><strong>Keys</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="ae1b5-122"><strong>Append</strong> メソッドおよび <strong>Delete</strong> メソッドはサポートされません。</span><span class="sxs-lookup"><span data-stu-id="ae1b5-122">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae1b5-123"><strong>Users</strong>コレクション</span><span class="sxs-lookup"><span data-stu-id="ae1b5-123"><strong>Users</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="ae1b5-124"><strong>Users</strong> はサポートされません。</span><span class="sxs-lookup"><span data-stu-id="ae1b5-124"><strong>Users</strong> is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae1b5-125"><strong>グループ</strong>コレクション</span><span class="sxs-lookup"><span data-stu-id="ae1b5-125"><strong>Groups</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="ae1b5-126"><strong>Groups</strong> はサポートされません。</span><span class="sxs-lookup"><span data-stu-id="ae1b5-126"><strong>Groups</strong> is not supported.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="microsoft-ole-db-provider-for-odbc"></a><span data-ttu-id="ae1b5-127">Microsoft OLE DB Provider for ODBC</span><span class="sxs-lookup"><span data-stu-id="ae1b5-127">Microsoft OLE DB Provider for ODBC</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ae1b5-128">オブジェクトまたはコレクション</span><span class="sxs-lookup"><span data-stu-id="ae1b5-128">Object or Collection</span></span></p></th>
<th><p><span data-ttu-id="ae1b5-129">使用制限</span><span class="sxs-lookup"><span data-stu-id="ae1b5-129">Usage Restriction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ae1b5-130"><strong>Catalog</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="ae1b5-130"><strong>Catalog</strong> object</span></span></p></td>
<td><p><span data-ttu-id="ae1b5-131"><strong>Create</strong> メソッドはサポートされません。</span><span class="sxs-lookup"><span data-stu-id="ae1b5-131">The <strong>Create</strong> method is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae1b5-132"><strong>テーブル</strong>コレクション</span><span class="sxs-lookup"><span data-stu-id="ae1b5-132"><strong>Tables</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="ae1b5-133"><strong>Append</strong> メソッドおよび <strong>Delete</strong> メソッドはサポートされません。
</span><span class="sxs-lookup"><span data-stu-id="ae1b5-133">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span> <span data-ttu-id="ae1b5-134">オブジェクトの作成前はプロパティ値の取得および設定が可能で、既存のオプジェクトを参照する場合は値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="ae1b5-134">Properties are read/write prior to object creation, and read-only when referencing an existing object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae1b5-135"><strong>Procedures</strong> コレクション</span><span class="sxs-lookup"><span data-stu-id="ae1b5-135"><strong>Procedures</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="ae1b5-136"><strong>Append</strong> メソッドおよび <strong>Delete</strong> メソッドはサポートされません。</span><span class="sxs-lookup"><span data-stu-id="ae1b5-136">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae1b5-137"><strong>プロシージャ</strong>オブジェクト</span><span class="sxs-lookup"><span data-stu-id="ae1b5-137"><strong>Procedure</strong> object</span></span></p></td>
<td><p><span data-ttu-id="ae1b5-138"><strong>Command</strong> プロパティはサポートされません。</span><span class="sxs-lookup"><span data-stu-id="ae1b5-138">The <strong>Command</strong> property is not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae1b5-139"><strong>インデックス</strong>コレクション</span><span class="sxs-lookup"><span data-stu-id="ae1b5-139"><strong>Indexes</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="ae1b5-140"><strong>Append</strong> メソッドおよび <strong>Delete</strong> メソッドはサポートされません。</span><span class="sxs-lookup"><span data-stu-id="ae1b5-140">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae1b5-141"><strong>Keys</strong>コレクション</span><span class="sxs-lookup"><span data-stu-id="ae1b5-141"><strong>Keys</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="ae1b5-142"><strong>Append</strong> メソッドおよび <strong>Delete</strong> メソッドはサポートされません。</span><span class="sxs-lookup"><span data-stu-id="ae1b5-142">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae1b5-143"><strong>Users</strong>コレクション</span><span class="sxs-lookup"><span data-stu-id="ae1b5-143"><strong>Users</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="ae1b5-144"><strong>Users</strong> はサポートされません。</span><span class="sxs-lookup"><span data-stu-id="ae1b5-144"><strong>Users</strong> is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae1b5-145"><strong>グループ</strong>コレクション</span><span class="sxs-lookup"><span data-stu-id="ae1b5-145"><strong>Groups</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="ae1b5-146"><strong>Groups</strong> はサポートされません。</span><span class="sxs-lookup"><span data-stu-id="ae1b5-146"><strong>Groups</strong> is not supported.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="microsoft-ole-db-provider-for-oracle"></a><span data-ttu-id="ae1b5-147">Microsoft OLE DB Provider for Oracle</span><span class="sxs-lookup"><span data-stu-id="ae1b5-147">Microsoft OLE DB Provider for Oracle</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ae1b5-148">オブジェクトまたはコレクション</span><span class="sxs-lookup"><span data-stu-id="ae1b5-148">Object or Collection</span></span></p></th>
<th><p><span data-ttu-id="ae1b5-149">使用制限</span><span class="sxs-lookup"><span data-stu-id="ae1b5-149">Usage Restriction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ae1b5-150"><strong>Catalog</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="ae1b5-150"><strong>Catalog</strong> object</span></span></p></td>
<td><p><span data-ttu-id="ae1b5-151"><strong>Create</strong> メソッドはサポートされません。</span><span class="sxs-lookup"><span data-stu-id="ae1b5-151">The <strong>Create</strong> method is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae1b5-152"><strong>テーブル</strong>コレクション</span><span class="sxs-lookup"><span data-stu-id="ae1b5-152"><strong>Tables</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="ae1b5-153"><strong>Append</strong> メソッドおよび <strong>Delete</strong> メソッドはサポートされません。
</span><span class="sxs-lookup"><span data-stu-id="ae1b5-153">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span> <span data-ttu-id="ae1b5-154">オブジェクトの作成前はプロパティ値の取得および設定が可能で、既存のオプジェクトを参照する場合は値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="ae1b5-154">Properties are read/write prior to object creation, and read-only when referencing an existing object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae1b5-155"><strong>Views</strong> コレクション</span><span class="sxs-lookup"><span data-stu-id="ae1b5-155"><strong>Views</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="ae1b5-156"><strong>Append</strong> メソッドおよび <strong>Delete</strong> メソッドはサポートされません。</span><span class="sxs-lookup"><span data-stu-id="ae1b5-156">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae1b5-157"><strong>ビュー</strong>オブジェクト</span><span class="sxs-lookup"><span data-stu-id="ae1b5-157"><strong>View</strong> object</span></span></p></td>
<td><p><span data-ttu-id="ae1b5-158"><strong>Command</strong> プロパティはサポートされません。</span><span class="sxs-lookup"><span data-stu-id="ae1b5-158">The <strong>Command</strong> property is not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae1b5-159"><strong>Procedures</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="ae1b5-159"><strong>Procedures</strong> object</span></span></p></td>
<td><p><span data-ttu-id="ae1b5-160"><strong>Append</strong> メソッドおよび <strong>Delete</strong> メソッドはサポートされません。</span><span class="sxs-lookup"><span data-stu-id="ae1b5-160">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae1b5-161"><strong>プロシージャ</strong>オブジェクト</span><span class="sxs-lookup"><span data-stu-id="ae1b5-161"><strong>Procedure</strong> object</span></span></p></td>
<td><p><span data-ttu-id="ae1b5-162"><strong>Command</strong> プロパティはサポートされません。</span><span class="sxs-lookup"><span data-stu-id="ae1b5-162">The <strong>Command</strong> property is not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae1b5-163"><strong>インデックス</strong>コレクション</span><span class="sxs-lookup"><span data-stu-id="ae1b5-163"><strong>Indexes</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="ae1b5-164"><strong>Append</strong> メソッドおよび <strong>Delete</strong> メソッドはサポートされません。</span><span class="sxs-lookup"><span data-stu-id="ae1b5-164">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae1b5-165"><strong>Keys</strong>コレクション</span><span class="sxs-lookup"><span data-stu-id="ae1b5-165"><strong>Keys</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="ae1b5-166"><strong>Append</strong> メソッドおよび <strong>Delete</strong> メソッドはサポートされません。</span><span class="sxs-lookup"><span data-stu-id="ae1b5-166">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae1b5-167"><strong>Users</strong>コレクション</span><span class="sxs-lookup"><span data-stu-id="ae1b5-167"><strong>Users</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="ae1b5-168"><strong>Users</strong> はサポートされません。</span><span class="sxs-lookup"><span data-stu-id="ae1b5-168"><strong>Users</strong> is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae1b5-169"><strong>グループ</strong>コレクション</span><span class="sxs-lookup"><span data-stu-id="ae1b5-169"><strong>Groups</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="ae1b5-170"><strong>Groups</strong> はサポートされません。</span><span class="sxs-lookup"><span data-stu-id="ae1b5-170"><strong>Groups</strong> is not supported.</span></span></p></td>
</tr>
</tbody>
</table>

