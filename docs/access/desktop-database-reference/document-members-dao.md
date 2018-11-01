---
title: Document メンバー (DAO)
TOCTitle: Document Members
ms:assetid: 8de770e6-e4d1-372a-3ef8-8539c921b41f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197365(v=office.15)
ms:contentKeyID: 48546270
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2ae19e30aa2a2f60f606f2380712815732eac932
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871368"
---
# <a name="document-members-dao"></a><span data-ttu-id="b33fa-102">Document メンバー (DAO)</span><span class="sxs-lookup"><span data-stu-id="b33fa-102">Document Members (DAO)</span></span>


<span data-ttu-id="b33fa-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="b33fa-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b33fa-p101">Document オブジェクトには、オブジェクトの 1 つのインスタンスの情報があります。オブジェクトは、データベース、保存されたテーブル、クエリ、またはリレーションシップのいずれかです (Microsoft Access データベース エンジン データベースのみ)。</span><span class="sxs-lookup"><span data-stu-id="b33fa-p101">A Document object includes information about one instance of an object. The object can be a database, saved table, query, or relationship (Microsoft Access database engine databases only).</span></span>

## <a name="methods"></a><span data-ttu-id="b33fa-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="b33fa-106">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b33fa-107">名前</span><span class="sxs-lookup"><span data-stu-id="b33fa-107">Name</span></span></p></th>
<th><p><span data-ttu-id="b33fa-108">説明</span><span class="sxs-lookup"><span data-stu-id="b33fa-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b33fa-109"><strong><a href="document-createproperty-method-dao.md">CreateProperty</a></strong></span><span class="sxs-lookup"><span data-stu-id="b33fa-109"><strong><a href="document-createproperty-method-dao.md">CreateProperty</a></strong></span></span></p></td>
<td><p><span data-ttu-id="b33fa-110">新しいユーザー定義の <strong><a href="property-object-dao.md">Property</a></strong> オブジェクトを作成します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="b33fa-110">Creates a new user-defined <strong><a href="property-object-dao.md">Property</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="b33fa-111">プロパティ</span><span class="sxs-lookup"><span data-stu-id="b33fa-111">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b33fa-112">名前</span><span class="sxs-lookup"><span data-stu-id="b33fa-112">Name</span></span></p></th>
<th><p><span data-ttu-id="b33fa-113">説明</span><span class="sxs-lookup"><span data-stu-id="b33fa-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b33fa-114"><strong><a href="document-container-property-dao.md">コンテナー</a></strong></span><span class="sxs-lookup"><span data-stu-id="b33fa-114"><strong><a href="document-container-property-dao.md">Container</a></strong></span></span></p></td>
<td><p><span data-ttu-id="b33fa-p102"><a href="container-object-dao.md">Document</a> オブジェクトが属する <strong><strong>Container</strong></strong> オブジェクトの名前を返します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="b33fa-p102">Returns the name of the <strong><a href="container-object-dao.md">Container</a></strong> object to which a <strong>Document</strong> object belongs (Microsoft Access workspaces only). .</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b33fa-117"><strong><a href="document-datecreated-property-dao.md">DateCreated</a></strong></span><span class="sxs-lookup"><span data-stu-id="b33fa-117"><strong><a href="document-datecreated-property-dao.md">DateCreated</a></strong></span></span></p></td>
<td><p><span data-ttu-id="b33fa-p103">オブジェクトが作成された日時を返します。値の取得のみ可能です。バリアント型 ( <strong>Variant</strong>) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="b33fa-p103">Returns the date and time that an object was created. Read-only <strong>Variant</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b33fa-120"><strong><a href="document-lastupdated-property-dao.md">LastUpdated</a></strong></span><span class="sxs-lookup"><span data-stu-id="b33fa-120"><strong><a href="document-lastupdated-property-dao.md">LastUpdated</a></strong></span></span></p></td>
<td><p><span data-ttu-id="b33fa-p104">オブジェクトを最後に変更した日付および時刻を取得します。値の取得のみ可能です。バリアント型 ( <strong>Variant</strong> ) の値を使用します。  </span><span class="sxs-lookup"><span data-stu-id="b33fa-p104">Returns the date and time of the most recent change made to an object. Read-only <strong>Variant</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b33fa-123"><strong><a href="document-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="b33fa-123"><strong><a href="document-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="b33fa-p105">指定したオブジェクトの名前を取得します。値の取得のみ可能です。文字列型 ( <strong>String</strong>) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="b33fa-p105">Returns the name of the specified object. Read-only <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b33fa-126"><strong><a href="document-properties-property-dao.md">Properties</a></strong></span><span class="sxs-lookup"><span data-stu-id="b33fa-126"><strong><a href="document-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="b33fa-p106">指定したオブジェクトの <strong><a href="properties-collection-dao.md">Properties</a></strong> コレクションを取得します。値の取得のみ可能です。  </span><span class="sxs-lookup"><span data-stu-id="b33fa-p106">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object. Read-only.</span></span></p></td>
</tr>
</tbody>
</table>

