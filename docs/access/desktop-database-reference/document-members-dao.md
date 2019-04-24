---
title: Document メンバー (DAO)
TOCTitle: Document Members
ms:assetid: 8de770e6-e4d1-372a-3ef8-8539c921b41f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197365(v=office.15)
ms:contentKeyID: 48546270
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cd50ec72113b0615849ff6b8b2e8d73c0e61c3ce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293792"
---
# <a name="document-members-dao"></a><span data-ttu-id="9eb3d-102">Document メンバー (DAO)</span><span class="sxs-lookup"><span data-stu-id="9eb3d-102">Document members (DAO)</span></span>


<span data-ttu-id="9eb3d-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="9eb3d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9eb3d-p101">Document オブジェクトには、オブジェクトの 1 つのインスタンスの情報があります。オブジェクトは、データベース、保存されたテーブル、クエリ、またはリレーションシップのいずれかです (Microsoft Access データベース エンジン データベースのみ)。</span><span class="sxs-lookup"><span data-stu-id="9eb3d-p101">A Document object includes information about one instance of an object. The object can be a database, saved table, query, or relationship (Microsoft Access database engine databases only).</span></span>

## <a name="methods"></a><span data-ttu-id="9eb3d-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="9eb3d-106">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9eb3d-107">名前</span><span class="sxs-lookup"><span data-stu-id="9eb3d-107">Name</span></span></p></th>
<th><p><span data-ttu-id="9eb3d-108">説明</span><span class="sxs-lookup"><span data-stu-id="9eb3d-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9eb3d-109"><strong><a href="document-createproperty-method-dao.md">CreateProperty</a></strong></span><span class="sxs-lookup"><span data-stu-id="9eb3d-109"><strong><a href="document-createproperty-method-dao.md">CreateProperty</a></strong></span></span></p></td>
<td><p><span data-ttu-id="9eb3d-110">新しいユーザー定義の <strong><a href="property-object-dao.md">Property</a></strong> オブジェクトを作成します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="9eb3d-110">Creates a new user-defined <strong><a href="property-object-dao.md">Property</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="9eb3d-111">プロパティ</span><span class="sxs-lookup"><span data-stu-id="9eb3d-111">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9eb3d-112">名前</span><span class="sxs-lookup"><span data-stu-id="9eb3d-112">Name</span></span></p></th>
<th><p><span data-ttu-id="9eb3d-113">説明</span><span class="sxs-lookup"><span data-stu-id="9eb3d-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9eb3d-114"><strong><a href="document-container-property-dao.md">Container</a></strong></span><span class="sxs-lookup"><span data-stu-id="9eb3d-114"><strong><a href="document-container-property-dao.md">Container</a></strong></span></span></p></td>
<td><p><span data-ttu-id="9eb3d-115"><strong>Document</strong>オブジェクトが属する<strong><a href="container-object-dao.md">コンテナー</a></strong>オブジェクトの名前を返します (Microsoft access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="9eb3d-115">Returns the name of the <strong><a href="container-object-dao.md">Container</a></strong> object to which a <strong>Document</strong> object belongs (Microsoft Access workspaces only).</span></span> <span data-ttu-id="9eb3d-116">.</span><span class="sxs-lookup"><span data-stu-id="9eb3d-116"></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9eb3d-117"><strong><a href="document-datecreated-property-dao.md">DateCreated</a></strong></span><span class="sxs-lookup"><span data-stu-id="9eb3d-117"><strong><a href="document-datecreated-property-dao.md">DateCreated</a></strong></span></span></p></td>
<td><p><span data-ttu-id="9eb3d-118">オブジェクトが作成された日付と時刻を返します。</span><span class="sxs-lookup"><span data-stu-id="9eb3d-118">Returns the date and time that an object was created.</span></span> <span data-ttu-id="9eb3d-119">読み取り専用 <strong>バリアント</strong> です。</span><span class="sxs-lookup"><span data-stu-id="9eb3d-119">Read-only <strong>Variant</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9eb3d-120"><strong><a href="document-lastupdated-property-dao.md">LastUpdated</a></strong></span><span class="sxs-lookup"><span data-stu-id="9eb3d-120"><strong><a href="document-lastupdated-property-dao.md">LastUpdated</a></strong></span></span></p></td>
<td><p><span data-ttu-id="9eb3d-p104">オブジェクトを最後に変更した日付および時刻を取得します。値の取得のみ可能です。バリアント型 ( <strong>Variant</strong> ) の値を使用します。  </span><span class="sxs-lookup"><span data-stu-id="9eb3d-p104">Returns the date and time of the most recent change made to an object. Read-only <strong>Variant</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9eb3d-123"><strong><a href="document-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="9eb3d-123"><strong><a href="document-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="9eb3d-124">指定したオブジェクトの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="9eb3d-124">Returns the name of the specified object.</span></span> <span data-ttu-id="9eb3d-125">読み取り専用 <strong>文字列</strong> です。</span><span class="sxs-lookup"><span data-stu-id="9eb3d-125">Read-only <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9eb3d-126"><strong><a href="document-properties-property-dao.md">Properties</a></strong></span><span class="sxs-lookup"><span data-stu-id="9eb3d-126"><strong><a href="document-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="9eb3d-p106">指定したオブジェクトの <strong><a href="properties-collection-dao.md">Properties</a></strong> コレクションを取得します。値の取得のみ可能です。  </span><span class="sxs-lookup"><span data-stu-id="9eb3d-p106">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object. Read-only.</span></span></p></td>
</tr>
</tbody>
</table>

