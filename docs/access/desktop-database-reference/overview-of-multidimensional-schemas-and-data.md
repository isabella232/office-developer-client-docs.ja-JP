---
title: 多次元スキーマおよびデータの概要
TOCTitle: Overview of multidimensional schemas and data
ms:assetid: a963e993-b7bf-eeb4-ecd5-d6fe43cf4bb5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249784(v=office.15)
ms:contentKeyID: 48546923
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2ce7366437028ed1e745c596c38b2c0314acefd2
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945895"
---
# <a name="overview-of-multidimensional-schemas-and-data"></a><span data-ttu-id="e3e9e-102">多次元スキーマおよびデータの概要</span><span class="sxs-lookup"><span data-stu-id="e3e9e-102">Overview of multidimensional schemas and data</span></span>

<span data-ttu-id="e3e9e-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="understanding-multidimensional-schemas"></a><span data-ttu-id="e3e9e-104">多次元スキーマについて</span><span class="sxs-lookup"><span data-stu-id="e3e9e-104">Understanding Multidimensional Schemas</span></span>

<span data-ttu-id="e3e9e-105">ADO MD の中心的なメタデータ オブジェクトは、構造化された関連する次元、階層、レベル、およびメンバーで構成される*キューブ*です。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-105">The central metadata object in ADO MD is the *cube*, which consists of a structured set of related dimensions, hierarchies, levels, and members.</span></span>

<span data-ttu-id="e3e9e-106">*ディメンション*は、ビジネス エンティティから派生する多次元データベースからのデータの独立したカテゴリです。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-106">A *dimension* is an independent category of data from your multidimensional database, derived from your business entities.</span></span> <span data-ttu-id="e3e9e-107">次元には、一般にデータベースのメジャーのクエリの抽出条件として使用するアイテムが含まれます。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-107">A dimension typically contains items to be used as query criteria for the measures of the database.</span></span>

<span data-ttu-id="e3e9e-108">*階層*は、ディメンションの集計パスです。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-108">A *hierarchy* is a path of aggregation of a dimension.</span></span> <span data-ttu-id="e3e9e-109">次元には、複数レベルの粒度があり、そこには親子関係 があります。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-109">A dimension may have multiple levels of granularity, which have parent-child relationships.</span></span> <span data-ttu-id="e3e9e-110">階層によって、レベル間の関係が定義されます。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-110">A hierarchy defines how these levels are related.</span></span>

<span data-ttu-id="e3e9e-111">*レベル*は、階層内の集計の手順です。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-111">A *level* is a step of aggregation in a hierarchy.</span></span> <span data-ttu-id="e3e9e-112">複数の情報のレイヤーを含む次元では、各レイヤーがレベルになります。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-112">For dimensions with multiple layers of information, each layer is a level.</span></span>

<span data-ttu-id="e3e9e-113">*メンバー*は、ディメンション内のデータ アイテムです。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-113">A *member* is a data item in a dimension.</span></span> <span data-ttu-id="e3e9e-114">一般に、メンバーを使用してキャプションを作成したり、データベースのメジャーを記述します。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-114">Typically, you create a caption or describe a measure of the database using members.</span></span>

<span data-ttu-id="e3e9e-p105">キューブは ADO MD の [CubeDef](cubedef-object-ado-md.md) のオブジェクトによって表されます。次元、階層、レベル、およびメンバーも、対応する ADO MD のオブジェクト ( [Dimension](dimension-object-ado-md.md)、[Hierarchy](hierarchy-object-ado-md.md)、[Level](level-object-ado-md.md)、および [Member](member-object-ado-md.md)) によって表されます。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-p105">Cubes are represented by [CubeDef](cubedef-object-ado-md.md) objects in ADO MD. Dimensions, hierarchies, levels, and members are also represented by their corresponding ADO MD objects: [Dimension](dimension-object-ado-md.md), [Hierarchy](hierarchy-object-ado-md.md), [Level](level-object-ado-md.md), and [Member](member-object-ado-md.md).</span></span>

## <a name="dimensions"></a><span data-ttu-id="e3e9e-117">次元</span><span class="sxs-lookup"><span data-stu-id="e3e9e-117">Dimensions</span></span>

<span data-ttu-id="e3e9e-p106">キューブの次元は、各自のビジネス エンティティおよびデータベースでモデル化するデータの種類に依存します。各次元は、一般にデータを選択するための独立したエントリ ポイントまたはメカニズムです。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-p106">The dimensions of a cube depend on your business entities and types of data to be modeled in the database. Typically, each dimension is an independent entry point or mechanism for selecting data.</span></span>

<span data-ttu-id="e3e9e-p107">たとえば、Salesperson、Geography、Time、Products、および Measures の 5 つの次元で構成される売上データを含むキューブがあるとします。Measures 次元には実際の売上データ値が含まれ、他の次元は売上データ値を分類してグループ化する方法を表します。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-p107">For example, a cube containing sales data has the following five dimensions: Salesperson, Geography, Time, Products, and Measures. The Measures dimension contains actual sales data values, while the other dimensions represent ways to categorize and group the sales data values.</span></span>

<span data-ttu-id="e3e9e-122">Geography 次元には、以下の一連のメンバーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-122">The Geography dimension has the following set of members:</span></span>

```text
 
{All, North America, Europe, Canada, USA, UK, Germany, Canada-West, 
Canada-East, USA-NW, USA-SW, USA-NE, USA-SE, England, Scotland,  
Wales,Ireland, Germany-North, Germany-South, Ottawa, Toronto,  
Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston,  
Shreveport, Miami, Boston, New York, London, Dover, Glasgow,  
Edinburgh, Cardiff, Pembroke, Belfast, Berlin,  
Hamburg, Munich, Stuttgart} 
```

## <a name="hierarchies"></a><span data-ttu-id="e3e9e-123">階層</span><span class="sxs-lookup"><span data-stu-id="e3e9e-123">Hierarchies</span></span>

<span data-ttu-id="e3e9e-p108">階層によって、次元のレベルを "まとめる" またはグループ化する方法を定義します。次元には、複数の階層を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-p108">Hierarchies define the ways in which the levels of a dimension can be "rolled up" or grouped. A dimension can have more than one hierarchy.</span></span>

## <a name="levels"></a><span data-ttu-id="e3e9e-126">レベル</span><span class="sxs-lookup"><span data-stu-id="e3e9e-126">Levels</span></span>

<span data-ttu-id="e3e9e-127">上の図で示されている Geography 次元の例の各ボックスは、階層内のレベルを表します。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-127">In the example Geography dimension pictured in the previous figure, each box represents a level in the hierarchy.</span></span>

<span data-ttu-id="e3e9e-128">各レベルには、以下のメンバーがあります。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-128">Each level has a set of members, as follows:</span></span>

  - <span data-ttu-id="e3e9e-129">The World = {All}
</span><span class="sxs-lookup"><span data-stu-id="e3e9e-129">The World = {All}</span></span>

  - <span data-ttu-id="e3e9e-130">Continents = {North America, Europe}
</span><span class="sxs-lookup"><span data-stu-id="e3e9e-130">Continents = {North America, Europe}</span></span>

  - <span data-ttu-id="e3e9e-131">Countries = {Canada, USA, UK, Germany}
</span><span class="sxs-lookup"><span data-stu-id="e3e9e-131">Countries = {Canada, USA, UK, Germany}</span></span>

  - <span data-ttu-id="e3e9e-132">Regions = {Canada-East, Canada-West, USA-NE, USA-NW, USA-SE, USA-SW, England, Ireland, Scotland, Wales, Germany-North, Germany-South}
</span><span class="sxs-lookup"><span data-stu-id="e3e9e-132">Regions = {Canada-East, Canada-West, USA-NE, USA-NW, USA-SE, USA-SW, England, Ireland, Scotland, Wales, Germany-North, Germany-South}</span></span>

  - <span data-ttu-id="e3e9e-133">Cities = {Ottawa, Toronto, Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston, Shreveport, Miami, Boston, New York, London, Dover, Glasgow, Edinburgh, Cardiff, Pembroke, Belfast, Berlin, Hamburg, Munich, Stuttgart}
</span><span class="sxs-lookup"><span data-stu-id="e3e9e-133">Cities = {Ottawa, Toronto, Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston, Shreveport, Miami, Boston, New York, London, Dover, Glasgow, Edinburgh, Cardiff, Pembroke, Belfast, Berlin, Hamburg, Munich, Stuttgart}</span></span>

## <a name="members"></a><span data-ttu-id="e3e9e-134">メンバー</span><span class="sxs-lookup"><span data-stu-id="e3e9e-134">Members</span></span>

<span data-ttu-id="e3e9e-p109">階層のリーフ レベルのメンバーに子はなく、ルート レベルのメンバーに親はありません。他のすべてのメンバーには、少なくとも 1 つの親と 1 つの子があります。たとえば、Geography 次元の階層ツリーを部分的にスキャンすると、以下の親子関係が生成されます。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-p109">Members at the leaf level of a hierarchy have no children, and members at the root level have no parent. All other members have at least one parent and at least one child. For example, a partial traversal of the hierarchy tree in the Geography dimension yields the following parent-child relationships:</span></span>

- <span data-ttu-id="e3e9e-138">{すべて}(親の){ヨーロッパ、北アメリカ。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-138">{All} (parent of) {Europe, North America}</span></span>
- <span data-ttu-id="e3e9e-139">{(北アメリカ)。(親の){カナダ、アメリカ合衆国}</span><span class="sxs-lookup"><span data-stu-id="e3e9e-139">{North America} (parent of) {Canada, USA}</span></span>
- <span data-ttu-id="e3e9e-140">{アメリカ合衆国}(親の){NE ではアメリカ合衆国、アメリカ合衆国の NW、アメリカ合衆国 SE (米国)-SW}</span><span class="sxs-lookup"><span data-stu-id="e3e9e-140">{USA} (parent of) {USA-NE, USA-NW, USA-SE, USA-SW}</span></span>
- <span data-ttu-id="e3e9e-141">{アメリカ合衆国の NW}(親の){ボイシ、シアトル。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-141">{USA-NW} (parent of) {Boise, Seattle}</span></span>

<span data-ttu-id="e3e9e-142">メンバーは各次元で 1 つ以上の階層に統合できます。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-142">Members can be consolidated along one or more hierarchies per dimension.</span></span>

<span data-ttu-id="e3e9e-143">この例では、別の特性も示しています。 年週階層の週レベルの一部のメンバーは、4 分の 1 年の階層のどのレベルには表示されません。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-143">This example also illustrates another characteristic: some members of the Week level of the Year-Week hierarchy do not appear in any level of the Year-Quarter hierarchy.</span></span> <span data-ttu-id="e3e9e-144">つまり、階層に次元のすべてのメンバーを含める必要はありません。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-144">Thus, a hierarchy need not include all members of a dimension.</span></span>

## <a name="understanding-multidimensional-schemas"></a><span data-ttu-id="e3e9e-145">多次元スキーマについて</span><span class="sxs-lookup"><span data-stu-id="e3e9e-145">Understanding Multidimensional Schemas</span></span>

<span data-ttu-id="e3e9e-146">ADO MD の中心的なメタデータ オブジェクトは、構造化された関連する次元、階層、レベル、およびメンバーで構成される*キューブ*です。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-146">The central metadata object in ADO MD is the *cube*, which consists of a structured set of related dimensions, hierarchies, levels, and members.</span></span>

<span data-ttu-id="e3e9e-147">*ディメンション*は、ビジネス エンティティから派生する多次元データベースからのデータの独立したカテゴリです。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-147">A *dimension* is an independent category of data from your multidimensional database, derived from your business entities.</span></span> <span data-ttu-id="e3e9e-148">次元には、一般にデータベースのメジャーのクエリの抽出条件として使用するアイテムが含まれます。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-148">A dimension typically contains items to be used as query criteria for the measures of the database.</span></span>

<span data-ttu-id="e3e9e-149">*階層*は、ディメンションの集計パスです。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-149">A *hierarchy* is a path of aggregation of a dimension.</span></span> <span data-ttu-id="e3e9e-150">次元には、複数レベルの粒度があり、そこには親子関係 があります。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-150">A dimension may have multiple levels of granularity, which have parent-child relationships.</span></span> <span data-ttu-id="e3e9e-151">階層によって、レベル間の関係が定義されます。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-151">A hierarchy defines how these levels are related.</span></span>

<span data-ttu-id="e3e9e-152">*レベル*は、階層内の集計の手順です。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-152">A *level* is a step of aggregation in a hierarchy.</span></span> <span data-ttu-id="e3e9e-153">複数の情報のレイヤーを含む次元では、各レイヤーがレベルになります。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-153">For dimensions with multiple layers of information, each layer is a level.</span></span>

<span data-ttu-id="e3e9e-154">*メンバー*は、ディメンション内のデータ アイテムです。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-154">A *member* is a data item in a dimension.</span></span> <span data-ttu-id="e3e9e-155">一般に、メンバーを使用してキャプションを作成したり、データベースのメジャーを記述します。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-155">Typically, you create a caption or describe a measure of the database using members.</span></span>

<span data-ttu-id="e3e9e-p115">キューブは ADO MD の [CubeDef](cubedef-object-ado-md.md) のオブジェクトによって表されます。次元、階層、レベル、およびメンバーも、対応する ADO MD のオブジェクト ( [Dimension](dimension-object-ado-md.md)、[Hierarchy](hierarchy-object-ado-md.md)、[Level](level-object-ado-md.md)、および [Member](member-object-ado-md.md)) によって表されます。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-p115">Cubes are represented by [CubeDef](cubedef-object-ado-md.md) objects in ADO MD. Dimensions, hierarchies, levels, and members are also represented by their corresponding ADO MD objects: [Dimension](dimension-object-ado-md.md), [Hierarchy](hierarchy-object-ado-md.md), [Level](level-object-ado-md.md), and [Member](member-object-ado-md.md).</span></span>

## <a name="dimensions"></a><span data-ttu-id="e3e9e-158">次元</span><span class="sxs-lookup"><span data-stu-id="e3e9e-158">Dimensions</span></span>

<span data-ttu-id="e3e9e-p116">キューブの次元は、各自のビジネス エンティティおよびデータベースでモデル化するデータの種類に依存します。各次元は、一般にデータを選択するための独立したエントリ ポイントまたはメカニズムです。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-p116">The dimensions of a cube depend on your business entities and types of data to be modeled in the database. Typically, each dimension is an independent entry point or mechanism for selecting data.</span></span>

<span data-ttu-id="e3e9e-p117">たとえば、Salesperson、Geography、Time、Products、および Measures の 5 つの次元で構成される売上データを含むキューブがあるとします。Measures 次元には実際の売上データ値が含まれ、他の次元は売上データ値を分類してグループ化する方法を表します。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-p117">For example, a cube containing sales data has the following five dimensions: Salesperson, Geography, Time, Products, and Measures. The Measures dimension contains actual sales data values, while the other dimensions represent ways to categorize and group the sales data values.</span></span>

<span data-ttu-id="e3e9e-163">Geography 次元には、以下の一連のメンバーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-163">The Geography dimension has the following set of members:</span></span>

```text 
 
{All, North America, Europe, Canada, USA, UK, Germany, Canada-West, 
Canada-East, USA-NW, USA-SW, USA-NE, USA-SE, England, Scotland,  
Wales,Ireland, Germany-North, Germany-South, Ottawa, Toronto,  
Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston,  
Shreveport, Miami, Boston, New York, London, Dover, Glasgow,  
Edinburgh, Cardiff, Pembroke, Belfast, Berlin,  
Hamburg, Munich, Stuttgart} 
```

## <a name="hierarchies"></a><span data-ttu-id="e3e9e-164">階層</span><span class="sxs-lookup"><span data-stu-id="e3e9e-164">Hierarchies</span></span>

<span data-ttu-id="e3e9e-p118">階層によって、次元のレベルを "まとめる" またはグループ化する方法を定義します。次元には、複数の階層を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-p118">Hierarchies define the ways in which the levels of a dimension can be "rolled up" or grouped. A dimension can have more than one hierarchy.</span></span>

## <a name="levels"></a><span data-ttu-id="e3e9e-167">レベル</span><span class="sxs-lookup"><span data-stu-id="e3e9e-167">Levels</span></span>

<span data-ttu-id="e3e9e-168">上の図で示されている Geography 次元の例の各ボックスは、階層内のレベルを表します。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-168">In the example Geography dimension pictured in the previous figure, each box represents a level in the hierarchy.</span></span>

<span data-ttu-id="e3e9e-169">各レベルには、以下のメンバーがあります。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-169">Each level has a set of members, as follows:</span></span>

- <span data-ttu-id="e3e9e-170">The World = {All}
</span><span class="sxs-lookup"><span data-stu-id="e3e9e-170">The World = {All}</span></span>

- <span data-ttu-id="e3e9e-171">Continents = {North America, Europe}
</span><span class="sxs-lookup"><span data-stu-id="e3e9e-171">Continents = {North America, Europe}</span></span>

- <span data-ttu-id="e3e9e-172">Countries = {Canada, USA, UK, Germany}
</span><span class="sxs-lookup"><span data-stu-id="e3e9e-172">Countries = {Canada, USA, UK, Germany}</span></span>

- <span data-ttu-id="e3e9e-173">Regions = {Canada-East, Canada-West, USA-NE, USA-NW, USA-SE, USA-SW, England, Ireland, Scotland, Wales, Germany-North, Germany-South}
</span><span class="sxs-lookup"><span data-stu-id="e3e9e-173">Regions = {Canada-East, Canada-West, USA-NE, USA-NW, USA-SE, USA-SW, England, Ireland, Scotland, Wales, Germany-North, Germany-South}</span></span>

- <span data-ttu-id="e3e9e-174">Cities = {Ottawa, Toronto, Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston, Shreveport, Miami, Boston, New York, London, Dover, Glasgow, Edinburgh, Cardiff, Pembroke, Belfast, Berlin, Hamburg, Munich, Stuttgart}
</span><span class="sxs-lookup"><span data-stu-id="e3e9e-174">Cities = {Ottawa, Toronto, Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston, Shreveport, Miami, Boston, New York, London, Dover, Glasgow, Edinburgh, Cardiff, Pembroke, Belfast, Berlin, Hamburg, Munich, Stuttgart}</span></span>

## <a name="members"></a><span data-ttu-id="e3e9e-175">メンバー</span><span class="sxs-lookup"><span data-stu-id="e3e9e-175">Members</span></span>

<span data-ttu-id="e3e9e-p119">階層のリーフ レベルのメンバーに子はなく、ルート レベルのメンバーに親はありません。他のすべてのメンバーには、少なくとも 1 つの親と 1 つの子があります。たとえば、Geography 次元の階層ツリーを部分的にスキャンすると、以下の親子関係が生成されます。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-p119">Members at the leaf level of a hierarchy have no children, and members at the root level have no parent. All other members have at least one parent and at least one child. For example, a partial traversal of the hierarchy tree in the Geography dimension yields the following parent-child relationships:</span></span>

- <span data-ttu-id="e3e9e-179">{すべて}(親の){ヨーロッパ、北アメリカ。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-179">{All} (parent of) {Europe, North America}</span></span>

- <span data-ttu-id="e3e9e-180">{(北アメリカ)。(親の){カナダ、アメリカ合衆国}</span><span class="sxs-lookup"><span data-stu-id="e3e9e-180">{North America} (parent of) {Canada, USA}</span></span>

- <span data-ttu-id="e3e9e-181">{アメリカ合衆国}(親の){NE ではアメリカ合衆国、アメリカ合衆国の NW、アメリカ合衆国 SE (米国)-SW}</span><span class="sxs-lookup"><span data-stu-id="e3e9e-181">{USA} (parent of) {USA-NE, USA-NW, USA-SE, USA-SW}</span></span>

- <span data-ttu-id="e3e9e-182">{アメリカ合衆国の NW}(親の){ボイシ、シアトル。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-182">{USA-NW} (parent of) {Boise, Seattle}</span></span>

<span data-ttu-id="e3e9e-183">メンバーは各次元で 1 つ以上の階層に統合できます。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-183">Members can be consolidated along one or more hierarchies per dimension.</span></span>

<span data-ttu-id="e3e9e-184">この例では、別の特性も示しています。 年週階層の週レベルの一部のメンバーは、4 分の 1 年の階層のどのレベルには表示されません。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-184">This example also illustrates another characteristic: some members of the Week level of the Year-Week hierarchy do not appear in any level of the Year-Quarter hierarchy.</span></span> <span data-ttu-id="e3e9e-185">つまり、階層に次元のすべてのメンバーを含める必要はありません。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-185">Thus, a hierarchy need not include all members of a dimension.</span></span>

