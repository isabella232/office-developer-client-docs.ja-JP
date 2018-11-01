---
title: 多次元スキーマおよびデータの概要
TOCTitle: Overview of Multidimensional Schemas and Data
ms:assetid: a963e993-b7bf-eeb4-ecd5-d6fe43cf4bb5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249784(v=office.15)
ms:contentKeyID: 48546923
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 376d80bc79af772cfd09b6f5b8759321ed4431ee
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887168"
---
# <a name="overview-of-multidimensional-schemas-and-data"></a><span data-ttu-id="fd079-102">多次元スキーマおよびデータの概要</span><span class="sxs-lookup"><span data-stu-id="fd079-102">Overview of Multidimensional Schemas and Data</span></span>


<span data-ttu-id="fd079-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="fd079-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="understanding-multidimensional-schemas"></a><span data-ttu-id="fd079-104">多次元スキーマについて</span><span class="sxs-lookup"><span data-stu-id="fd079-104">Understanding Multidimensional Schemas</span></span>

<span data-ttu-id="fd079-105">ADO MD の中心的なメタデータ オブジェクトは、構造化された関連する次元、階層、レベル、およびメンバーで構成される*キューブ*です。</span><span class="sxs-lookup"><span data-stu-id="fd079-105">The central metadata object in ADO MD is the *cube*, which consists of a structured set of related dimensions, hierarchies, levels, and members.</span></span>

<span data-ttu-id="fd079-106">*ディメンション*は、ビジネス エンティティから派生する多次元データベースからのデータの独立したカテゴリです。</span><span class="sxs-lookup"><span data-stu-id="fd079-106">A *dimension* is an independent category of data from your multidimensional database, derived from your business entities.</span></span> <span data-ttu-id="fd079-107">次元には、一般にデータベースのメジャーのクエリの抽出条件として使用するアイテムが含まれます。</span><span class="sxs-lookup"><span data-stu-id="fd079-107">A dimension typically contains items to be used as query criteria for the measures of the database.</span></span>

<span data-ttu-id="fd079-108">*階層*は、ディメンションの集計パスです。</span><span class="sxs-lookup"><span data-stu-id="fd079-108">A *hierarchy* is a path of aggregation of a dimension.</span></span> <span data-ttu-id="fd079-109">次元には、複数レベルの粒度があり、そこには親子関係 があります。</span><span class="sxs-lookup"><span data-stu-id="fd079-109">A dimension may have multiple levels of granularity, which have parent-child relationships.</span></span> <span data-ttu-id="fd079-110">階層によって、レベル間の関係が定義されます。</span><span class="sxs-lookup"><span data-stu-id="fd079-110">A hierarchy defines how these levels are related.</span></span>

<span data-ttu-id="fd079-111">*レベル*は、階層内の集計の手順です。</span><span class="sxs-lookup"><span data-stu-id="fd079-111">A *level* is a step of aggregation in a hierarchy.</span></span> <span data-ttu-id="fd079-112">複数の情報のレイヤーを含む次元では、各レイヤーがレベルになります。</span><span class="sxs-lookup"><span data-stu-id="fd079-112">For dimensions with multiple layers of information, each layer is a level.</span></span>

<span data-ttu-id="fd079-113">*メンバー*は、ディメンション内のデータ アイテムです。</span><span class="sxs-lookup"><span data-stu-id="fd079-113">A *member* is a data item in a dimension.</span></span> <span data-ttu-id="fd079-114">一般に、メンバーを使用してキャプションを作成したり、データベースのメジャーを記述します。</span><span class="sxs-lookup"><span data-stu-id="fd079-114">Typically, you create a caption or describe a measure of the database using members.</span></span>

<span data-ttu-id="fd079-p105">キューブは ADO MD の [CubeDef](cubedef-object-ado-md.md) のオブジェクトによって表されます。次元、階層、レベル、およびメンバーも、対応する ADO MD のオブジェクト ( [Dimension](dimension-object-ado-md.md)、[Hierarchy](hierarchy-object-ado-md.md)、[Level](level-object-ado-md.md)、および [Member](member-object-ado-md.md)) によって表されます。</span><span class="sxs-lookup"><span data-stu-id="fd079-p105">Cubes are represented by [CubeDef](cubedef-object-ado-md.md) objects in ADO MD. Dimensions, hierarchies, levels, and members are also represented by their corresponding ADO MD objects: [Dimension](dimension-object-ado-md.md), [Hierarchy](hierarchy-object-ado-md.md), [Level](level-object-ado-md.md), and [Member](member-object-ado-md.md).</span></span>

## <a name="dimensions"></a><span data-ttu-id="fd079-117">次元</span><span class="sxs-lookup"><span data-stu-id="fd079-117">Dimensions</span></span>

<span data-ttu-id="fd079-p106">キューブの次元は、各自のビジネス エンティティおよびデータベースでモデル化するデータの種類に依存します。各次元は、一般にデータを選択するための独立したエントリ ポイントまたはメカニズムです。</span><span class="sxs-lookup"><span data-stu-id="fd079-p106">The dimensions of a cube depend on your business entities and types of data to be modeled in the database. Typically, each dimension is an independent entry point or mechanism for selecting data.</span></span>

<span data-ttu-id="fd079-p107">たとえば、Salesperson、Geography、Time、Products、および Measures の 5 つの次元で構成される売上データを含むキューブがあるとします。Measures 次元には実際の売上データ値が含まれ、他の次元は売上データ値を分類してグループ化する方法を表します。</span><span class="sxs-lookup"><span data-stu-id="fd079-p107">For example, a cube containing sales data has the following five dimensions: Salesperson, Geography, Time, Products, and Measures. The Measures dimension contains actual sales data values, while the other dimensions represent ways to categorize and group the sales data values.</span></span>

<span data-ttu-id="fd079-122">Geography 次元には、以下の一連のメンバーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="fd079-122">The Geography dimension has the following set of members:</span></span>

```text
 
{All, North America, Europe, Canada, USA, UK, Germany, Canada-West, 
Canada-East, USA-NW, USA-SW, USA-NE, USA-SE, England, Scotland,  
Wales,Ireland, Germany-North, Germany-South, Ottawa, Toronto,  
Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston,  
Shreveport, Miami, Boston, New York, London, Dover, Glasgow,  
Edinburgh, Cardiff, Pembroke, Belfast, Berlin,  
Hamburg, Munich, Stuttgart} 
```

## <a name="hierarchies"></a><span data-ttu-id="fd079-123">階層</span><span class="sxs-lookup"><span data-stu-id="fd079-123">Hierarchies</span></span>

<span data-ttu-id="fd079-p108">階層によって、次元のレベルを "まとめる" またはグループ化する方法を定義します。次元には、複数の階層を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="fd079-p108">Hierarchies define the ways in which the levels of a dimension can be "rolled up" or grouped. A dimension can have more than one hierarchy.</span></span>

## <a name="levels"></a><span data-ttu-id="fd079-126">レベル</span><span class="sxs-lookup"><span data-stu-id="fd079-126">Levels</span></span>

<span data-ttu-id="fd079-127">上の図で示されている Geography 次元の例の各ボックスは、階層内のレベルを表します。</span><span class="sxs-lookup"><span data-stu-id="fd079-127">In the example Geography dimension pictured in the previous figure, each box represents a level in the hierarchy.</span></span>

<span data-ttu-id="fd079-128">各レベルには、以下のメンバーがあります。</span><span class="sxs-lookup"><span data-stu-id="fd079-128">Each level has a set of members, as follows:</span></span>

  - <span data-ttu-id="fd079-129">The World = {All}
</span><span class="sxs-lookup"><span data-stu-id="fd079-129">The World = {All}</span></span>

  - <span data-ttu-id="fd079-130">Continents = {North America, Europe}
</span><span class="sxs-lookup"><span data-stu-id="fd079-130">Continents = {North America, Europe}</span></span>

  - <span data-ttu-id="fd079-131">Countries = {Canada, USA, UK, Germany}
</span><span class="sxs-lookup"><span data-stu-id="fd079-131">Countries = {Canada, USA, UK, Germany}</span></span>

  - <span data-ttu-id="fd079-132">Regions = {Canada-East, Canada-West, USA-NE, USA-NW, USA-SE, USA-SW, England, Ireland, Scotland, Wales, Germany-North, Germany-South}
</span><span class="sxs-lookup"><span data-stu-id="fd079-132">Regions = {Canada-East, Canada-West, USA-NE, USA-NW, USA-SE, USA-SW, England, Ireland, Scotland, Wales, Germany-North, Germany-South}</span></span>

  - <span data-ttu-id="fd079-133">Cities = {Ottawa, Toronto, Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston, Shreveport, Miami, Boston, New York, London, Dover, Glasgow, Edinburgh, Cardiff, Pembroke, Belfast, Berlin, Hamburg, Munich, Stuttgart}
</span><span class="sxs-lookup"><span data-stu-id="fd079-133">Cities = {Ottawa, Toronto, Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston, Shreveport, Miami, Boston, New York, London, Dover, Glasgow, Edinburgh, Cardiff, Pembroke, Belfast, Berlin, Hamburg, Munich, Stuttgart}</span></span>

## <a name="members"></a><span data-ttu-id="fd079-134">メンバー</span><span class="sxs-lookup"><span data-stu-id="fd079-134">Members</span></span>

<span data-ttu-id="fd079-p109">階層のリーフ レベルのメンバーに子はなく、ルート レベルのメンバーに親はありません。他のすべてのメンバーには、少なくとも 1 つの親と 1 つの子があります。たとえば、Geography 次元の階層ツリーを部分的にスキャンすると、以下の親子関係が生成されます。</span><span class="sxs-lookup"><span data-stu-id="fd079-p109">Members at the leaf level of a hierarchy have no children, and members at the root level have no parent. All other members have at least one parent and at least one child. For example, a partial traversal of the hierarchy tree in the Geography dimension yields the following parent-child relationships:</span></span>

  - <span data-ttu-id="fd079-138">{すべて}(親の){ヨーロッパ、北アメリカ。</span><span class="sxs-lookup"><span data-stu-id="fd079-138">{All} (parent of) {Europe, North America}</span></span>

  - <span data-ttu-id="fd079-139">{(北アメリカ)。(親の){カナダ、アメリカ合衆国}</span><span class="sxs-lookup"><span data-stu-id="fd079-139">{North America} (parent of) {Canada, USA}</span></span>

  - <span data-ttu-id="fd079-140">{アメリカ合衆国}(親の){NE ではアメリカ合衆国、アメリカ合衆国の NW、アメリカ合衆国 SE (米国)-SW}</span><span class="sxs-lookup"><span data-stu-id="fd079-140">{USA} (parent of) {USA-NE, USA-NW, USA-SE, USA-SW}</span></span>

  - <span data-ttu-id="fd079-141">{アメリカ合衆国の NW}(親の){ボイシ、シアトル。</span><span class="sxs-lookup"><span data-stu-id="fd079-141">{USA-NW} (parent of) {Boise, Seattle}</span></span>

<span data-ttu-id="fd079-142">メンバーは各次元で 1 つ以上の階層に統合できます。</span><span class="sxs-lookup"><span data-stu-id="fd079-142">Members can be consolidated along one or more hierarchies per dimension.</span></span>

<span data-ttu-id="fd079-p110">この例は、Year-Week 階層の Week レベルのメンバーは Year-Quarter 階層のどのレベルにも表示されないという、もう 1 つの特性も示しています。つまり、階層に次元のすべてのメンバーを含める必要はありません。</span><span class="sxs-lookup"><span data-stu-id="fd079-p110">This example also illustrates another characteristic: Some members of the Week level of the Year-Week hierarchy do not appear in any level of the Year-Quarter hierarchy. Thus, a hierarchy need not include all members of a dimension.</span></span>

## <a name="understanding-multidimensional-schemas"></a><span data-ttu-id="fd079-145">多次元スキーマについて</span><span class="sxs-lookup"><span data-stu-id="fd079-145">Understanding Multidimensional Schemas</span></span>

<span data-ttu-id="fd079-146">ADO MD の中心的なメタデータ オブジェクトは、構造化された関連する次元、階層、レベル、およびメンバーで構成される*キューブ*です。</span><span class="sxs-lookup"><span data-stu-id="fd079-146">The central metadata object in ADO MD is the *cube*, which consists of a structured set of related dimensions, hierarchies, levels, and members.</span></span>

<span data-ttu-id="fd079-147">*ディメンション*は、ビジネス エンティティから派生する多次元データベースからのデータの独立したカテゴリです。</span><span class="sxs-lookup"><span data-stu-id="fd079-147">A *dimension* is an independent category of data from your multidimensional database, derived from your business entities.</span></span> <span data-ttu-id="fd079-148">次元には、一般にデータベースのメジャーのクエリの抽出条件として使用するアイテムが含まれます。</span><span class="sxs-lookup"><span data-stu-id="fd079-148">A dimension typically contains items to be used as query criteria for the measures of the database.</span></span>

<span data-ttu-id="fd079-149">*階層*は、ディメンションの集計パスです。</span><span class="sxs-lookup"><span data-stu-id="fd079-149">A *hierarchy* is a path of aggregation of a dimension.</span></span> <span data-ttu-id="fd079-150">次元には、複数レベルの粒度があり、そこには親子関係 があります。</span><span class="sxs-lookup"><span data-stu-id="fd079-150">A dimension may have multiple levels of granularity, which have parent-child relationships.</span></span> <span data-ttu-id="fd079-151">階層によって、レベル間の関係が定義されます。</span><span class="sxs-lookup"><span data-stu-id="fd079-151">A hierarchy defines how these levels are related.</span></span>

<span data-ttu-id="fd079-152">*レベル*は、階層内の集計の手順です。</span><span class="sxs-lookup"><span data-stu-id="fd079-152">A *level* is a step of aggregation in a hierarchy.</span></span> <span data-ttu-id="fd079-153">複数の情報のレイヤーを含む次元では、各レイヤーがレベルになります。</span><span class="sxs-lookup"><span data-stu-id="fd079-153">For dimensions with multiple layers of information, each layer is a level.</span></span>

<span data-ttu-id="fd079-154">*メンバー*は、ディメンション内のデータ アイテムです。</span><span class="sxs-lookup"><span data-stu-id="fd079-154">A *member* is a data item in a dimension.</span></span> <span data-ttu-id="fd079-155">一般に、メンバーを使用してキャプションを作成したり、データベースのメジャーを記述します。</span><span class="sxs-lookup"><span data-stu-id="fd079-155">Typically, you create a caption or describe a measure of the database using members.</span></span>

<span data-ttu-id="fd079-p115">キューブは ADO MD の [CubeDef](cubedef-object-ado-md.md) のオブジェクトによって表されます。次元、階層、レベル、およびメンバーも、対応する ADO MD のオブジェクト ( [Dimension](dimension-object-ado-md.md)、[Hierarchy](hierarchy-object-ado-md.md)、[Level](level-object-ado-md.md)、および [Member](member-object-ado-md.md)) によって表されます。</span><span class="sxs-lookup"><span data-stu-id="fd079-p115">Cubes are represented by [CubeDef](cubedef-object-ado-md.md) objects in ADO MD. Dimensions, hierarchies, levels, and members are also represented by their corresponding ADO MD objects: [Dimension](dimension-object-ado-md.md), [Hierarchy](hierarchy-object-ado-md.md), [Level](level-object-ado-md.md), and [Member](member-object-ado-md.md).</span></span>

## <a name="dimensions"></a><span data-ttu-id="fd079-158">次元</span><span class="sxs-lookup"><span data-stu-id="fd079-158">Dimensions</span></span>

<span data-ttu-id="fd079-p116">キューブの次元は、各自のビジネス エンティティおよびデータベースでモデル化するデータの種類に依存します。各次元は、一般にデータを選択するための独立したエントリ ポイントまたはメカニズムです。</span><span class="sxs-lookup"><span data-stu-id="fd079-p116">The dimensions of a cube depend on your business entities and types of data to be modeled in the database. Typically, each dimension is an independent entry point or mechanism for selecting data.</span></span>

<span data-ttu-id="fd079-p117">たとえば、Salesperson、Geography、Time、Products、および Measures の 5 つの次元で構成される売上データを含むキューブがあるとします。Measures 次元には実際の売上データ値が含まれ、他の次元は売上データ値を分類してグループ化する方法を表します。</span><span class="sxs-lookup"><span data-stu-id="fd079-p117">For example, a cube containing sales data has the following five dimensions: Salesperson, Geography, Time, Products, and Measures. The Measures dimension contains actual sales data values, while the other dimensions represent ways to categorize and group the sales data values.</span></span>

<span data-ttu-id="fd079-163">Geography 次元には、以下の一連のメンバーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="fd079-163">The Geography dimension has the following set of members:</span></span>

```text 
 
{All, North America, Europe, Canada, USA, UK, Germany, Canada-West, 
Canada-East, USA-NW, USA-SW, USA-NE, USA-SE, England, Scotland,  
Wales,Ireland, Germany-North, Germany-South, Ottawa, Toronto,  
Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston,  
Shreveport, Miami, Boston, New York, London, Dover, Glasgow,  
Edinburgh, Cardiff, Pembroke, Belfast, Berlin,  
Hamburg, Munich, Stuttgart} 
```

## <a name="hierarchies"></a><span data-ttu-id="fd079-164">階層</span><span class="sxs-lookup"><span data-stu-id="fd079-164">Hierarchies</span></span>

<span data-ttu-id="fd079-p118">階層によって、次元のレベルを "まとめる" またはグループ化する方法を定義します。次元には、複数の階層を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="fd079-p118">Hierarchies define the ways in which the levels of a dimension can be "rolled up" or grouped. A dimension can have more than one hierarchy.</span></span>

## <a name="levels"></a><span data-ttu-id="fd079-167">レベル</span><span class="sxs-lookup"><span data-stu-id="fd079-167">Levels</span></span>

<span data-ttu-id="fd079-168">上の図で示されている Geography 次元の例の各ボックスは、階層内のレベルを表します。</span><span class="sxs-lookup"><span data-stu-id="fd079-168">In the example Geography dimension pictured in the previous figure, each box represents a level in the hierarchy.</span></span>

<span data-ttu-id="fd079-169">各レベルには、以下のメンバーがあります。</span><span class="sxs-lookup"><span data-stu-id="fd079-169">Each level has a set of members, as follows:</span></span>

- <span data-ttu-id="fd079-170">The World = {All}
</span><span class="sxs-lookup"><span data-stu-id="fd079-170">The World = {All}</span></span>

- <span data-ttu-id="fd079-171">Continents = {North America, Europe}
</span><span class="sxs-lookup"><span data-stu-id="fd079-171">Continents = {North America, Europe}</span></span>

- <span data-ttu-id="fd079-172">Countries = {Canada, USA, UK, Germany}
</span><span class="sxs-lookup"><span data-stu-id="fd079-172">Countries = {Canada, USA, UK, Germany}</span></span>

- <span data-ttu-id="fd079-173">Regions = {Canada-East, Canada-West, USA-NE, USA-NW, USA-SE, USA-SW, England, Ireland, Scotland, Wales, Germany-North, Germany-South}
</span><span class="sxs-lookup"><span data-stu-id="fd079-173">Regions = {Canada-East, Canada-West, USA-NE, USA-NW, USA-SE, USA-SW, England, Ireland, Scotland, Wales, Germany-North, Germany-South}</span></span>

- <span data-ttu-id="fd079-174">Cities = {Ottawa, Toronto, Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston, Shreveport, Miami, Boston, New York, London, Dover, Glasgow, Edinburgh, Cardiff, Pembroke, Belfast, Berlin, Hamburg, Munich, Stuttgart}
</span><span class="sxs-lookup"><span data-stu-id="fd079-174">Cities = {Ottawa, Toronto, Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston, Shreveport, Miami, Boston, New York, London, Dover, Glasgow, Edinburgh, Cardiff, Pembroke, Belfast, Berlin, Hamburg, Munich, Stuttgart}</span></span>

## <a name="members"></a><span data-ttu-id="fd079-175">メンバー</span><span class="sxs-lookup"><span data-stu-id="fd079-175">Members</span></span>

<span data-ttu-id="fd079-p119">階層のリーフ レベルのメンバーに子はなく、ルート レベルのメンバーに親はありません。他のすべてのメンバーには、少なくとも 1 つの親と 1 つの子があります。たとえば、Geography 次元の階層ツリーを部分的にスキャンすると、以下の親子関係が生成されます。</span><span class="sxs-lookup"><span data-stu-id="fd079-p119">Members at the leaf level of a hierarchy have no children, and members at the root level have no parent. All other members have at least one parent and at least one child. For example, a partial traversal of the hierarchy tree in the Geography dimension yields the following parent-child relationships:</span></span>

- <span data-ttu-id="fd079-179">{すべて}(親の){ヨーロッパ、北アメリカ。</span><span class="sxs-lookup"><span data-stu-id="fd079-179">{All} (parent of) {Europe, North America}</span></span>

- <span data-ttu-id="fd079-180">{(北アメリカ)。(親の){カナダ、アメリカ合衆国}</span><span class="sxs-lookup"><span data-stu-id="fd079-180">{North America} (parent of) {Canada, USA}</span></span>

- <span data-ttu-id="fd079-181">{アメリカ合衆国}(親の){NE ではアメリカ合衆国、アメリカ合衆国の NW、アメリカ合衆国 SE (米国)-SW}</span><span class="sxs-lookup"><span data-stu-id="fd079-181">{USA} (parent of) {USA-NE, USA-NW, USA-SE, USA-SW}</span></span>

- <span data-ttu-id="fd079-182">{アメリカ合衆国の NW}(親の){ボイシ、シアトル。</span><span class="sxs-lookup"><span data-stu-id="fd079-182">{USA-NW} (parent of) {Boise, Seattle}</span></span>

<span data-ttu-id="fd079-183">メンバーは各次元で 1 つ以上の階層に統合できます。</span><span class="sxs-lookup"><span data-stu-id="fd079-183">Members can be consolidated along one or more hierarchies per dimension.</span></span>

<span data-ttu-id="fd079-p120">この例は、Year-Week 階層の Week レベルのメンバーは Year-Quarter 階層のどのレベルにも表示されないという、もう 1 つの特性も示しています。つまり、階層に次元のすべてのメンバーを含める必要はありません。</span><span class="sxs-lookup"><span data-stu-id="fd079-p120">This example also illustrates another characteristic: Some members of the Week level of the Year-Week hierarchy do not appear in any level of the Year-Quarter hierarchy. Thus, a hierarchy need not include all members of a dimension.</span></span>

