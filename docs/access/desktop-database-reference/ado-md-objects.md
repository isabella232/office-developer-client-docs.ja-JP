---
title: ADO MD オブジェクト (デスクトップ データベース参照のアクセス)
TOCTitle: ADO MD Objects
ms:assetid: 13501e44-70b6-1036-a8b7-c276f187e4f4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248907(v=office.15)
ms:contentKeyID: 48543366
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e09676b222e7199b7f2f9f7520ebf3d5436f9a3c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875134"
---
# <a name="ado-md-objects"></a><span data-ttu-id="75ea6-102">ADO MD のオブジェクト</span><span class="sxs-lookup"><span data-stu-id="75ea6-102">ADO MD Objects</span></span>


<span data-ttu-id="75ea6-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="75ea6-103">**Applies to**: Access 2013, Office 2013</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="75ea6-104"><a href="axis-object-ado-md.md">軸</a></span><span class="sxs-lookup"><span data-stu-id="75ea6-104"><a href="axis-object-ado-md.md">Axis</a></span></span></p></td>
<td><p><span data-ttu-id="75ea6-105">1 つ以上の次元の選択されたメンバーを含む、セルセットの位置またはフィルターの軸を表します。</span><span class="sxs-lookup"><span data-stu-id="75ea6-105">Represents a positional or filter axis of a cellset, containing selected members of one or more dimensions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75ea6-106"><a href="catalog-object-ado-md.md">カタログ</a></span><span class="sxs-lookup"><span data-stu-id="75ea6-106"><a href="catalog-object-ado-md.md">Catalog</a></span></span></p></td>
<td><p><span data-ttu-id="75ea6-107">多次元データ プロバイダー (MDP) に固有の多次元スキーマ情報 (つまり、キューブおよび基になる次元、階層、レベル、およびメンバー) が含まれます。</span><span class="sxs-lookup"><span data-stu-id="75ea6-107">Contains multidimensional schema information (that is, cubes and underlying dimensions, hierarchies, levels, and members) specific to a multidimensional data provider (MDP).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75ea6-108"><a href="cell-object-ado-md.md">Cell</a></span><span class="sxs-lookup"><span data-stu-id="75ea6-108"><a href="cell-object-ado-md.md">Cell</a></span></span></p></td>
<td><p><span data-ttu-id="75ea6-109">セルセットに含まれる、座標軸の交点のデータを表します。</span><span class="sxs-lookup"><span data-stu-id="75ea6-109">Represents the data at the intersection of axis coordinates, contained in a cellset.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75ea6-110"><a href="cellset-object-ado-md.md">セルセット</a></span><span class="sxs-lookup"><span data-stu-id="75ea6-110"><a href="cellset-object-ado-md.md">Cellset</a></span></span></p></td>
<td><p><span data-ttu-id="75ea6-p101">多次元クエリの結果を表します。キューブまたは他のセルセットから選択されたセルのコレクションになります。</span><span class="sxs-lookup"><span data-stu-id="75ea6-p101">Represents the results of a multidimensional query. It is a collection of cells selected from cubes or other cellsets.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75ea6-113"><a href="cubedef-object-ado-md.md">CubeDef</a></span><span class="sxs-lookup"><span data-stu-id="75ea6-113"><a href="cubedef-object-ado-md.md">CubeDef</a></span></span></p></td>
<td><p><span data-ttu-id="75ea6-114">関連する次元のセットを含む、多次元スキーマからのキューブを表します。</span><span class="sxs-lookup"><span data-stu-id="75ea6-114">Represents a cube from a multidimensional schema, containing a set of related dimensions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75ea6-115"><a href="dimension-object-ado-md.md">ディメンション</a></span><span class="sxs-lookup"><span data-stu-id="75ea6-115"><a href="dimension-object-ado-md.md">Dimension</a></span></span></p></td>
<td><p><span data-ttu-id="75ea6-116">1 つ以上のメンバーの階層を含む、多次元キューブの次元の 1 つを表します。</span><span class="sxs-lookup"><span data-stu-id="75ea6-116">Represents one of the dimensions of a multidimensional cube, containing one or more hierarchies of members.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75ea6-117"><a href="hierarchy-object-ado-md.md">階層</a></span><span class="sxs-lookup"><span data-stu-id="75ea6-117"><a href="hierarchy-object-ado-md.md">Hierarchy</a></span></span></p></td>
<td><p><span data-ttu-id="75ea6-118">いずれかのように、ディメンションのメンバーを集約することを表すまたは&quot;ロール アップします。&quot;ディメンションは 1 つまたは複数の階層ごとに集約できます。</span><span class="sxs-lookup"><span data-stu-id="75ea6-118">Represents one way in which the members of a dimension can be aggregated or &quot;rolled up.&quot; A dimension can be aggregated along one or more hierarchies.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75ea6-119"><a href="level-object-ado-md.md">Level</a></span><span class="sxs-lookup"><span data-stu-id="75ea6-119"><a href="level-object-ado-md.md">Level</a></span></span></p></td>
<td><p><span data-ttu-id="75ea6-120">階層内で同じランクを持つメンバーのセットが含まれます。</span><span class="sxs-lookup"><span data-stu-id="75ea6-120">Contains a set of members, each of which has the same rank within a hierarchy.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75ea6-121"><a href="member-object-ado-md.md">メンバー</a></span><span class="sxs-lookup"><span data-stu-id="75ea6-121"><a href="member-object-ado-md.md">Member</a></span></span></p></td>
<td><p><span data-ttu-id="75ea6-122">キューブ内のレベルのメンバー、レベルのメンバーの子、またはセルセットの軸に沿ったメンバーの位置を表します。</span><span class="sxs-lookup"><span data-stu-id="75ea6-122">Represents a member of a level in a cube, the children of a member of a level, or a member of a position along an axis of a cellset.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75ea6-123"><a href="position-object-ado-md.md">Position</a></span><span class="sxs-lookup"><span data-stu-id="75ea6-123"><a href="position-object-ado-md.md">Position</a></span></span></p></td>
<td><p><span data-ttu-id="75ea6-124">軸に沿った位置を定義する、異なる次元の 1 つ以上のメンバーのセットを表します。</span><span class="sxs-lookup"><span data-stu-id="75ea6-124">Represents a set of one or more members of different dimensions that defines a point along an axis.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="75ea6-125">また、 **Catalog** オブジェクトは、標準の ADO ライブラリに含まれる ADO **Connection** オブジェクトに接続されます。</span><span class="sxs-lookup"><span data-stu-id="75ea6-125">Also, the **Catalog** object is connected to an ADO **Connection** object, which is included with the standard ADO library:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="75ea6-126">オブジェクト</span><span class="sxs-lookup"><span data-stu-id="75ea6-126">Object</span></span></p></th>
<th><p><span data-ttu-id="75ea6-127">説明</span><span class="sxs-lookup"><span data-stu-id="75ea6-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="75ea6-128"><a href="connection-object-ado.md">Connection</a></span><span class="sxs-lookup"><span data-stu-id="75ea6-128"><a href="connection-object-ado.md">Connection</a></span></span></p></td>
<td><p><span data-ttu-id="75ea6-129">データ ソースに対して開かれている接続を表します。</span><span class="sxs-lookup"><span data-stu-id="75ea6-129">Represents an open connection to a data source.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="75ea6-p102">ADO MD オブジェクトの多くは、対応するコレクションに格納できます。たとえば、[CubeDef](cubedef-object-ado-md.md) オブジェクトは [Catalog](cubedefs-collection-ado-md.md) オブジェクトの **CubeDefs** コレクションに格納できます。詳細については、「 [ADO MD コレクション](ado-md-collections.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="75ea6-p102">Many ADO MD objects can be contained in a corresponding collection. For example, a [CubeDef](cubedef-object-ado-md.md) object can be contained in a [CubeDefs](cubedefs-collection-ado-md.md) collection of a **Catalog**. For more information, see [ADO MD Collections](ado-md-collections.md).</span></span>

