---
title: RelationAttributeEnum 列挙 (DAO)
TOCTitle: RelationAttributeEnum Enumeration
ms:assetid: ce8d0696-66d7-052f-1313-64baee3442ed
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834499(v=office.15)
ms:contentKeyID: 48547787
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4c4d7a2b622e382461bcf1b4171a5aa85f036854
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478942"
---
# <a name="relationattributeenum-enumeration-dao"></a><span data-ttu-id="e6af9-102">RelationAttributeEnum 列挙 (DAO)</span><span class="sxs-lookup"><span data-stu-id="e6af9-102">RelationAttributeEnum Enumeration (DAO)</span></span>


<span data-ttu-id="e6af9-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="e6af9-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e6af9-104">" **Attributes**/属性" プロパティで、 **Relation** オブジェクトの属性を特定するために使用します。</span><span class="sxs-lookup"><span data-stu-id="e6af9-104">Used with the **Attributes** property to determine attributes of a **Relation** object.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e6af9-105">名前</span><span class="sxs-lookup"><span data-stu-id="e6af9-105">Name</span></span></p></th>
<th><p><span data-ttu-id="e6af9-106">値</span><span class="sxs-lookup"><span data-stu-id="e6af9-106">Value</span></span></p></th>
<th><p><span data-ttu-id="e6af9-107">説明</span><span class="sxs-lookup"><span data-stu-id="e6af9-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e6af9-108">dbRelationDeleteCascade</span><span class="sxs-lookup"><span data-stu-id="e6af9-108">dbRelationDeleteCascade</span></span></p></td>
<td><p><span data-ttu-id="e6af9-109">4096</span><span class="sxs-lookup"><span data-stu-id="e6af9-109">4096</span></span></p></td>
<td><p><span data-ttu-id="e6af9-110">削除が連鎖的に行われます。</span><span class="sxs-lookup"><span data-stu-id="e6af9-110">Deletions cascade</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6af9-111">dbRelationDontEnforce</span><span class="sxs-lookup"><span data-stu-id="e6af9-111">dbRelationDontEnforce</span></span></p></td>
<td><p><span data-ttu-id="e6af9-112">2</span><span class="sxs-lookup"><span data-stu-id="e6af9-112">2</span></span></p></td>
<td><p><span data-ttu-id="e6af9-113">リレーションシップは適用されません (参照整合性なし)。</span><span class="sxs-lookup"><span data-stu-id="e6af9-113">Relationship not enforced (no referential integrity)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6af9-114">dbRelationInherited</span><span class="sxs-lookup"><span data-stu-id="e6af9-114">dbRelationInherited</span></span></p></td>
<td><p><span data-ttu-id="e6af9-115">4</span><span class="sxs-lookup"><span data-stu-id="e6af9-115">4</span></span></p></td>
<td><p><span data-ttu-id="e6af9-116">リレーションシップは 2 つのリンク テーブルを含むデータベース内に存在します。</span><span class="sxs-lookup"><span data-stu-id="e6af9-116">Relationship exists in the database containing the two linked tables</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6af9-117">dbRelationLeft</span><span class="sxs-lookup"><span data-stu-id="e6af9-117">dbRelationLeft</span></span></p></td>
<td><p><span data-ttu-id="e6af9-118">16777216</span><span class="sxs-lookup"><span data-stu-id="e6af9-118">16777216</span></span></p></td>
<td><p><span data-ttu-id="e6af9-p101">Microsoft Access のみ有効。デザイン ビューで、左結合を既定の結合の種類として表示します。</span><span class="sxs-lookup"><span data-stu-id="e6af9-p101">Microsoft Access only. In Design view, display a LEFT JOIN as the default join type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6af9-121">dbRelationRight</span><span class="sxs-lookup"><span data-stu-id="e6af9-121">dbRelationRight</span></span></p></td>
<td><p><span data-ttu-id="e6af9-122">33554432</span><span class="sxs-lookup"><span data-stu-id="e6af9-122">33554432</span></span></p></td>
<td><p><span data-ttu-id="e6af9-p102">Microsoft Access のみ有効。デザイン ビューで、右結合を既定の結合の種類として表示します。</span><span class="sxs-lookup"><span data-stu-id="e6af9-p102">Microsoft Access only. In Design view, display a RIGHT JOIN as the default join type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6af9-125">dbRelationUnique</span><span class="sxs-lookup"><span data-stu-id="e6af9-125">dbRelationUnique</span></span></p></td>
<td><p><span data-ttu-id="e6af9-126">1</span><span class="sxs-lookup"><span data-stu-id="e6af9-126">1</span></span></p></td>
<td><p><span data-ttu-id="e6af9-127">一対一リレーションシップ。</span><span class="sxs-lookup"><span data-stu-id="e6af9-127">One-to-one relationship</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6af9-128">これら</span><span class="sxs-lookup"><span data-stu-id="e6af9-128">dbRelationUpdateCascade</span></span></p></td>
<td><p><span data-ttu-id="e6af9-129">256</span><span class="sxs-lookup"><span data-stu-id="e6af9-129">256</span></span></p></td>
<td><p><span data-ttu-id="e6af9-130">更新が連鎖的に行われます。</span><span class="sxs-lookup"><span data-stu-id="e6af9-130">Updates cascade</span></span></p></td>
</tr>
</tbody>
</table>

