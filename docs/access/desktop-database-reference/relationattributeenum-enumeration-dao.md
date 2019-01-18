---
title: RelationAttributeEnum 列挙型 (DAO)
TOCTitle: RelationAttributeEnum Enumeration
ms:assetid: ce8d0696-66d7-052f-1313-64baee3442ed
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834499(v=office.15)
ms:contentKeyID: 48547787
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: dbb8ca2e1a63154f17bd814a26fe79ed405765cb
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711120"
---
# <a name="relationattributeenum-enumeration-dao"></a><span data-ttu-id="3fda8-102">RelationAttributeEnum 列挙型 (DAO)</span><span class="sxs-lookup"><span data-stu-id="3fda8-102">RelationAttributeEnum enumeration (DAO)</span></span>


<span data-ttu-id="3fda8-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="3fda8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3fda8-104">" **Attributes**/属性" プロパティで、 **Relation** オブジェクトの属性を特定するために使用します。</span><span class="sxs-lookup"><span data-stu-id="3fda8-104">Used with the **Attributes** property to determine attributes of a **Relation** object.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3fda8-105">名前</span><span class="sxs-lookup"><span data-stu-id="3fda8-105">Name</span></span></p></th>
<th><p><span data-ttu-id="3fda8-106">値</span><span class="sxs-lookup"><span data-stu-id="3fda8-106">Value</span></span></p></th>
<th><p><span data-ttu-id="3fda8-107">説明</span><span class="sxs-lookup"><span data-stu-id="3fda8-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3fda8-108">dbRelationDeleteCascade</span><span class="sxs-lookup"><span data-stu-id="3fda8-108">dbRelationDeleteCascade</span></span></p></td>
<td><p><span data-ttu-id="3fda8-109">4096</span><span class="sxs-lookup"><span data-stu-id="3fda8-109">4096</span></span></p></td>
<td><p><span data-ttu-id="3fda8-110">削除が連鎖的に行われます。</span><span class="sxs-lookup"><span data-stu-id="3fda8-110">Deletions cascade</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fda8-111">dbRelationDontEnforce</span><span class="sxs-lookup"><span data-stu-id="3fda8-111">dbRelationDontEnforce</span></span></p></td>
<td><p><span data-ttu-id="3fda8-112">2</span><span class="sxs-lookup"><span data-stu-id="3fda8-112">2</span></span></p></td>
<td><p><span data-ttu-id="3fda8-113">リレーションシップは適用されません (参照整合性なし)。</span><span class="sxs-lookup"><span data-stu-id="3fda8-113">Relationship not enforced (no referential integrity)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fda8-114">dbRelationInherited</span><span class="sxs-lookup"><span data-stu-id="3fda8-114">dbRelationInherited</span></span></p></td>
<td><p><span data-ttu-id="3fda8-115">4</span><span class="sxs-lookup"><span data-stu-id="3fda8-115">4</span></span></p></td>
<td><p><span data-ttu-id="3fda8-116">リレーションシップは 2 つのリンク テーブルを含むデータベース内に存在します。</span><span class="sxs-lookup"><span data-stu-id="3fda8-116">Relationship exists in the database containing the two linked tables</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fda8-117">dbRelationLeft</span><span class="sxs-lookup"><span data-stu-id="3fda8-117">dbRelationLeft</span></span></p></td>
<td><p><span data-ttu-id="3fda8-118">16777216</span><span class="sxs-lookup"><span data-stu-id="3fda8-118">16777216</span></span></p></td>
<td><p><span data-ttu-id="3fda8-p101">Microsoft Access のみ有効。デザイン ビューで、左結合を既定の結合の種類として表示します。</span><span class="sxs-lookup"><span data-stu-id="3fda8-p101">Microsoft Access only. In Design view, display a LEFT JOIN as the default join type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fda8-121">dbRelationRight</span><span class="sxs-lookup"><span data-stu-id="3fda8-121">dbRelationRight</span></span></p></td>
<td><p><span data-ttu-id="3fda8-122">33554432</span><span class="sxs-lookup"><span data-stu-id="3fda8-122">33554432</span></span></p></td>
<td><p><span data-ttu-id="3fda8-p102">Microsoft Access のみ有効。デザイン ビューで、右結合を既定の結合の種類として表示します。</span><span class="sxs-lookup"><span data-stu-id="3fda8-p102">Microsoft Access only. In Design view, display a RIGHT JOIN as the default join type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fda8-125">dbRelationUnique</span><span class="sxs-lookup"><span data-stu-id="3fda8-125">dbRelationUnique</span></span></p></td>
<td><p><span data-ttu-id="3fda8-126">1</span><span class="sxs-lookup"><span data-stu-id="3fda8-126">1</span></span></p></td>
<td><p><span data-ttu-id="3fda8-127">一対一リレーションシップ。</span><span class="sxs-lookup"><span data-stu-id="3fda8-127">One-to-one relationship</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fda8-128">これら</span><span class="sxs-lookup"><span data-stu-id="3fda8-128">dbRelationUpdateCascade</span></span></p></td>
<td><p><span data-ttu-id="3fda8-129">256</span><span class="sxs-lookup"><span data-stu-id="3fda8-129">256</span></span></p></td>
<td><p><span data-ttu-id="3fda8-130">更新が連鎖的に行われます。</span><span class="sxs-lookup"><span data-stu-id="3fda8-130">Updates cascade</span></span></p></td>
</tr>
</tbody>
</table>

