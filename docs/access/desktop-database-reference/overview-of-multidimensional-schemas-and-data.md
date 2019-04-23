---
title: 多次元スキーマとデータの概要
TOCTitle: Overview of multidimensional schemas and data
ms:assetid: a963e993-b7bf-eeb4-ecd5-d6fe43cf4bb5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249784(v=office.15)
ms:contentKeyID: 48546923
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d65378bf964ad8c6e81a08cb653f09bf00a8431c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288155"
---
# <a name="overview-of-multidimensional-schemas-and-data"></a><span data-ttu-id="ac2c2-102">多次元スキーマとデータの概要</span><span class="sxs-lookup"><span data-stu-id="ac2c2-102">Overview of multidimensional schemas and data</span></span>

<span data-ttu-id="ac2c2-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="ac2c2-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="understanding-multidimensional-schemas"></a><span data-ttu-id="ac2c2-104">多次元スキーマについて</span><span class="sxs-lookup"><span data-stu-id="ac2c2-104">Understanding Multidimensional Schemas</span></span>

<span data-ttu-id="ac2c2-105">ADO MD の中心的なメタデータ オブジェクトは、構造化された関連する次元、階層、レベル、およびメンバーで構成される*キューブ*です。</span><span class="sxs-lookup"><span data-stu-id="ac2c2-105">The central metadata object in ADO MD is the *cube*, which consists of a structured set of related dimensions, hierarchies, levels, and members.</span></span>

<span data-ttu-id="ac2c2-p101">*次元*は、ビジネス エンティティから派生する多次元データベースの独立したデータのカテゴリです。次元には、一般にデータベースのメジャーのクエリの抽出条件として使用するアイテムが含まれます。</span><span class="sxs-lookup"><span data-stu-id="ac2c2-p101">A *dimension* is an independent category of data from your multidimensional database, derived from your business entities. A dimension typically contains items to be used as query criteria for the measures of the database.</span></span>

<span data-ttu-id="ac2c2-p102">*階層*は、次元の集計パスです。次元には、複数レベルの粒度があり、そこには親子関係 があります。階層によって、レベル間の関係が定義されます。</span><span class="sxs-lookup"><span data-stu-id="ac2c2-p102">A *hierarchy* is a path of aggregation of a dimension. A dimension may have multiple levels of granularity, which have parent-child relationships. A hierarchy defines how these levels are related.</span></span>

<span data-ttu-id="ac2c2-111">*レベル*は、階層内の集計の手順です。</span><span class="sxs-lookup"><span data-stu-id="ac2c2-111">A *level* is a step of aggregation in a hierarchy.</span></span> <span data-ttu-id="ac2c2-112">複数の情報のレイヤーを含む次元では、各レイヤーがレベルになります。</span><span class="sxs-lookup"><span data-stu-id="ac2c2-112">For dimensions with multiple layers of information, each layer is a level.</span></span>

<span data-ttu-id="ac2c2-113">*メンバー*は、次元のデータ アイテムです。</span><span class="sxs-lookup"><span data-stu-id="ac2c2-113">A *member* is a data item in a dimension.</span></span> <span data-ttu-id="ac2c2-114">一般に、メンバーを使用してキャプションを作成したり、データベースのメジャーを記述します。</span><span class="sxs-lookup"><span data-stu-id="ac2c2-114">Typically, you create a caption or describe a measure of the database using members.</span></span>

<span data-ttu-id="ac2c2-p105">キューブは ADO MD の [CubeDef](cubedef-object-ado-md.md) のオブジェクトによって表されます。次元、階層、レベル、およびメンバーも、対応する ADO MD のオブジェクト ( [Dimension](dimension-object-ado-md.md)、[Hierarchy](hierarchy-object-ado-md.md)、[Level](level-object-ado-md.md)、および [Member](member-object-ado-md.md)) によって表されます。</span><span class="sxs-lookup"><span data-stu-id="ac2c2-p105">Cubes are represented by [CubeDef](cubedef-object-ado-md.md) objects in ADO MD. Dimensions, hierarchies, levels, and members are also represented by their corresponding ADO MD objects: [Dimension](dimension-object-ado-md.md), [Hierarchy](hierarchy-object-ado-md.md), [Level](level-object-ado-md.md), and [Member](member-object-ado-md.md).</span></span>

## <a name="dimensions"></a><span data-ttu-id="ac2c2-117">Dimensions</span><span class="sxs-lookup"><span data-stu-id="ac2c2-117">Dimensions</span></span>

<span data-ttu-id="ac2c2-p106">キューブの次元は、各自のビジネス エンティティおよびデータベースでモデル化するデータの種類に依存します。各次元は、一般にデータを選択するための独立したエントリ ポイントまたはメカニズムです。</span><span class="sxs-lookup"><span data-stu-id="ac2c2-p106">The dimensions of a cube depend on your business entities and types of data to be modeled in the database. Typically, each dimension is an independent entry point or mechanism for selecting data.</span></span>

<span data-ttu-id="ac2c2-p107">たとえば、Salesperson、Geography、Time、Products、および Measures の 5 つの次元で構成される売上データを含むキューブがあるとします。Measures 次元には実際の売上データ値が含まれ、他の次元は売上データ値を分類してグループ化する方法を表します。</span><span class="sxs-lookup"><span data-stu-id="ac2c2-p107">For example, a cube containing sales data has the following five dimensions: Salesperson, Geography, Time, Products, and Measures. The Measures dimension contains actual sales data values, while the other dimensions represent ways to categorize and group the sales data values.</span></span>

<span data-ttu-id="ac2c2-122">Geography 次元には、以下の一連のメンバーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="ac2c2-122">The Geography dimension has the following set of members:</span></span>

```text
 
{All, North America, Europe, Canada, USA, UK, Germany, Canada-West, 
Canada-East, USA-NW, USA-SW, USA-NE, USA-SE, England, Scotland,  
Wales,Ireland, Germany-North, Germany-South, Ottawa, Toronto,  
Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston,  
Shreveport, Miami, Boston, New York, London, Dover, Glasgow,  
Edinburgh, Cardiff, Pembroke, Belfast, Berlin,  
Hamburg, Munich, Stuttgart} 
```

## <a name="hierarchies"></a><span data-ttu-id="ac2c2-123">Hierarchies</span><span class="sxs-lookup"><span data-stu-id="ac2c2-123">Hierarchies</span></span>

<span data-ttu-id="ac2c2-p108">階層によって、次元のレベルを "まとめる" またはグループ化する方法を定義します。次元には、複数の階層を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="ac2c2-p108">Hierarchies define the ways in which the levels of a dimension can be "rolled up" or grouped. A dimension can have more than one hierarchy.</span></span>

## <a name="levels"></a><span data-ttu-id="ac2c2-126">Levels</span><span class="sxs-lookup"><span data-stu-id="ac2c2-126">Levels</span></span>

<span data-ttu-id="ac2c2-127">上の図で示されている Geography 次元の例の各ボックスは、階層内のレベルを表します。</span><span class="sxs-lookup"><span data-stu-id="ac2c2-127">In the example Geography dimension pictured in the previous figure, each box represents a level in the hierarchy.</span></span>

<span data-ttu-id="ac2c2-128">各レベルには、以下のメンバーがあります。</span><span class="sxs-lookup"><span data-stu-id="ac2c2-128">Each level has a set of members, as follows:</span></span>

  - <span data-ttu-id="ac2c2-129">The World = {All}
</span><span class="sxs-lookup"><span data-stu-id="ac2c2-129">The World = {All}</span></span>

  - <span data-ttu-id="ac2c2-130">大陸: {北アメリカ、ヨーロッパ}</span><span class="sxs-lookup"><span data-stu-id="ac2c2-130">Continents = {North America, Europe}</span></span>

  - <span data-ttu-id="ac2c2-131">国 = {カナダ、米国、英国、ドイツ}</span><span class="sxs-lookup"><span data-stu-id="ac2c2-131">Countries = {Canada, USA, UK, Germany}</span></span>

  - <span data-ttu-id="ac2c2-132">地域 = {カナダ-東、カナダ-西、usa-NE、usa-NW、usa-中南米、usa-SW、英国、アイルランド、スコットランド、ウェールズ、ドイツ-北、ドイツ-南}</span><span class="sxs-lookup"><span data-stu-id="ac2c2-132">Regions = {Canada-East, Canada-West, USA-NE, USA-NW, USA-SE, USA-SW, England, Ireland, Scotland, Wales, Germany-North, Germany-South}</span></span>

  - <span data-ttu-id="ac2c2-133">都市 = {Ottawa, トロント, Vancouver, calgary, シアトル, ボイシ, Los ロサンゼルス, ヒューストン, Shreveport, Miami, ボストン, ニューヨーク,, Dover, Glasgow,, cardiff, Pembroke, ベルギー fast, ベルリン, Hamburg, ミュンヘン, シュトゥットガルト}</span><span class="sxs-lookup"><span data-stu-id="ac2c2-133">Cities = {Ottawa, Toronto, Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston, Shreveport, Miami, Boston, New York, London, Dover, Glasgow, Edinburgh, Cardiff, Pembroke, Belfast, Berlin, Hamburg, Munich, Stuttgart}</span></span>

## <a name="members"></a><span data-ttu-id="ac2c2-134">Members</span><span class="sxs-lookup"><span data-stu-id="ac2c2-134">Members</span></span>

<span data-ttu-id="ac2c2-p109">階層のリーフ レベルのメンバーに子はなく、ルート レベルのメンバーに親はありません。他のすべてのメンバーには、少なくとも 1 つの親と 1 つの子があります。たとえば、Geography 次元の階層ツリーを部分的にスキャンすると、以下の親子関係が生成されます。</span><span class="sxs-lookup"><span data-stu-id="ac2c2-p109">Members at the leaf level of a hierarchy have no children, and members at the root level have no parent. All other members have at least one parent and at least one child. For example, a partial traversal of the hierarchy tree in the Geography dimension yields the following parent-child relationships:</span></span>

- <span data-ttu-id="ac2c2-138">いずれ(の親){ヨーロッパ、北アメリカ}</span><span class="sxs-lookup"><span data-stu-id="ac2c2-138">{All} (parent of) {Europe, North America}</span></span>
- <span data-ttu-id="ac2c2-139">{北アメリカ}(の親){カナダ、USA}</span><span class="sxs-lookup"><span data-stu-id="ac2c2-139">{North America} (parent of) {Canada, USA}</span></span>
- <span data-ttu-id="ac2c2-140">英語(の親){米国-NE、USA-NW、USA-SE、USA-SW}</span><span class="sxs-lookup"><span data-stu-id="ac2c2-140">{USA} (parent of) {USA-NE, USA-NW, USA-SE, USA-SW}</span></span>
- <span data-ttu-id="ac2c2-141">{米国-NW}(の親){ボイシ, シアトル}</span><span class="sxs-lookup"><span data-stu-id="ac2c2-141">{USA-NW} (parent of) {Boise, Seattle}</span></span>

<span data-ttu-id="ac2c2-142">メンバーは各次元で 1 つ以上の階層に統合できます。</span><span class="sxs-lookup"><span data-stu-id="ac2c2-142">Members can be consolidated along one or more hierarchies per dimension.</span></span>

<span data-ttu-id="ac2c2-143">また、この例では、年単位階層の週レベルの一部のメンバーが年四半期の階層のどのレベルにも表示されないということも示しています。</span><span class="sxs-lookup"><span data-stu-id="ac2c2-143">This example also illustrates another characteristic: some members of the Week level of the Year-Week hierarchy do not appear in any level of the Year-Quarter hierarchy.</span></span> <span data-ttu-id="ac2c2-144">つまり、階層に次元のすべてのメンバーを含める必要はありません。</span><span class="sxs-lookup"><span data-stu-id="ac2c2-144">Thus, a hierarchy need not include all members of a dimension.</span></span>

## <a name="understanding-multidimensional-schemas"></a><span data-ttu-id="ac2c2-145">多次元スキーマについて</span><span class="sxs-lookup"><span data-stu-id="ac2c2-145">Understanding Multidimensional Schemas</span></span>

<span data-ttu-id="ac2c2-146">ADO MD の中心的なメタデータ オブジェクトは、構造化された関連する次元、階層、レベル、およびメンバーで構成される*キューブ*です。</span><span class="sxs-lookup"><span data-stu-id="ac2c2-146">The central metadata object in ADO MD is the *cube*, which consists of a structured set of related dimensions, hierarchies, levels, and members.</span></span>

<span data-ttu-id="ac2c2-p111">*次元*は、ビジネス エンティティから派生する多次元データベースの独立したデータのカテゴリです。次元には、一般にデータベースのメジャーのクエリの抽出条件として使用するアイテムが含まれます。</span><span class="sxs-lookup"><span data-stu-id="ac2c2-p111">A *dimension* is an independent category of data from your multidimensional database, derived from your business entities. A dimension typically contains items to be used as query criteria for the measures of the database.</span></span>

<span data-ttu-id="ac2c2-p112">*階層*は、次元の集計パスです。次元には、複数レベルの粒度があり、そこには親子関係 があります。階層によって、レベル間の関係が定義されます。</span><span class="sxs-lookup"><span data-stu-id="ac2c2-p112">A *hierarchy* is a path of aggregation of a dimension. A dimension may have multiple levels of granularity, which have parent-child relationships. A hierarchy defines how these levels are related.</span></span>

<span data-ttu-id="ac2c2-152">*レベル*は、階層内の集計の手順です。</span><span class="sxs-lookup"><span data-stu-id="ac2c2-152">A *level* is a step of aggregation in a hierarchy.</span></span> <span data-ttu-id="ac2c2-153">複数の情報のレイヤーを含む次元では、各レイヤーがレベルになります。</span><span class="sxs-lookup"><span data-stu-id="ac2c2-153">For dimensions with multiple layers of information, each layer is a level.</span></span>

<span data-ttu-id="ac2c2-154">*メンバー*は、次元のデータ アイテムです。</span><span class="sxs-lookup"><span data-stu-id="ac2c2-154">A *member* is a data item in a dimension.</span></span> <span data-ttu-id="ac2c2-155">一般に、メンバーを使用してキャプションを作成したり、データベースのメジャーを記述します。</span><span class="sxs-lookup"><span data-stu-id="ac2c2-155">Typically, you create a caption or describe a measure of the database using members.</span></span>

<span data-ttu-id="ac2c2-p115">キューブは ADO MD の [CubeDef](cubedef-object-ado-md.md) のオブジェクトによって表されます。次元、階層、レベル、およびメンバーも、対応する ADO MD のオブジェクト ( [Dimension](dimension-object-ado-md.md)、[Hierarchy](hierarchy-object-ado-md.md)、[Level](level-object-ado-md.md)、および [Member](member-object-ado-md.md)) によって表されます。</span><span class="sxs-lookup"><span data-stu-id="ac2c2-p115">Cubes are represented by [CubeDef](cubedef-object-ado-md.md) objects in ADO MD. Dimensions, hierarchies, levels, and members are also represented by their corresponding ADO MD objects: [Dimension](dimension-object-ado-md.md), [Hierarchy](hierarchy-object-ado-md.md), [Level](level-object-ado-md.md), and [Member](member-object-ado-md.md).</span></span>

## <a name="dimensions"></a><span data-ttu-id="ac2c2-158">Dimensions</span><span class="sxs-lookup"><span data-stu-id="ac2c2-158">Dimensions</span></span>

<span data-ttu-id="ac2c2-p116">キューブの次元は、各自のビジネス エンティティおよびデータベースでモデル化するデータの種類に依存します。各次元は、一般にデータを選択するための独立したエントリ ポイントまたはメカニズムです。</span><span class="sxs-lookup"><span data-stu-id="ac2c2-p116">The dimensions of a cube depend on your business entities and types of data to be modeled in the database. Typically, each dimension is an independent entry point or mechanism for selecting data.</span></span>

<span data-ttu-id="ac2c2-p117">たとえば、Salesperson、Geography、Time、Products、および Measures の 5 つの次元で構成される売上データを含むキューブがあるとします。Measures 次元には実際の売上データ値が含まれ、他の次元は売上データ値を分類してグループ化する方法を表します。</span><span class="sxs-lookup"><span data-stu-id="ac2c2-p117">For example, a cube containing sales data has the following five dimensions: Salesperson, Geography, Time, Products, and Measures. The Measures dimension contains actual sales data values, while the other dimensions represent ways to categorize and group the sales data values.</span></span>

<span data-ttu-id="ac2c2-163">Geography 次元には、以下の一連のメンバーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="ac2c2-163">The Geography dimension has the following set of members:</span></span>

```text 
 
{All, North America, Europe, Canada, USA, UK, Germany, Canada-West, 
Canada-East, USA-NW, USA-SW, USA-NE, USA-SE, England, Scotland,  
Wales,Ireland, Germany-North, Germany-South, Ottawa, Toronto,  
Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston,  
Shreveport, Miami, Boston, New York, London, Dover, Glasgow,  
Edinburgh, Cardiff, Pembroke, Belfast, Berlin,  
Hamburg, Munich, Stuttgart} 
```

## <a name="hierarchies"></a><span data-ttu-id="ac2c2-164">Hierarchies</span><span class="sxs-lookup"><span data-stu-id="ac2c2-164">Hierarchies</span></span>

<span data-ttu-id="ac2c2-p118">階層によって、次元のレベルを "まとめる" またはグループ化する方法を定義します。次元には、複数の階層を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="ac2c2-p118">Hierarchies define the ways in which the levels of a dimension can be "rolled up" or grouped. A dimension can have more than one hierarchy.</span></span>

## <a name="levels"></a><span data-ttu-id="ac2c2-167">Levels</span><span class="sxs-lookup"><span data-stu-id="ac2c2-167">Levels</span></span>

<span data-ttu-id="ac2c2-168">上の図で示されている Geography 次元の例の各ボックスは、階層内のレベルを表します。</span><span class="sxs-lookup"><span data-stu-id="ac2c2-168">In the example Geography dimension pictured in the previous figure, each box represents a level in the hierarchy.</span></span>

<span data-ttu-id="ac2c2-169">各レベルには、以下のメンバーがあります。</span><span class="sxs-lookup"><span data-stu-id="ac2c2-169">Each level has a set of members, as follows:</span></span>

- <span data-ttu-id="ac2c2-170">The World = {All}
</span><span class="sxs-lookup"><span data-stu-id="ac2c2-170">The World = {All}</span></span>

- <span data-ttu-id="ac2c2-171">大陸: {北アメリカ、ヨーロッパ}</span><span class="sxs-lookup"><span data-stu-id="ac2c2-171">Continents = {North America, Europe}</span></span>

- <span data-ttu-id="ac2c2-172">国 = {カナダ、米国、英国、ドイツ}</span><span class="sxs-lookup"><span data-stu-id="ac2c2-172">Countries = {Canada, USA, UK, Germany}</span></span>

- <span data-ttu-id="ac2c2-173">地域 = {カナダ-東、カナダ-西、usa-NE、usa-NW、usa-中南米、usa-SW、英国、アイルランド、スコットランド、ウェールズ、ドイツ-北、ドイツ-南}</span><span class="sxs-lookup"><span data-stu-id="ac2c2-173">Regions = {Canada-East, Canada-West, USA-NE, USA-NW, USA-SE, USA-SW, England, Ireland, Scotland, Wales, Germany-North, Germany-South}</span></span>

- <span data-ttu-id="ac2c2-174">都市 = {Ottawa, トロント, Vancouver, calgary, シアトル, ボイシ, Los ロサンゼルス, ヒューストン, Shreveport, Miami, ボストン, ニューヨーク,, Dover, Glasgow,, cardiff, Pembroke, ベルギー fast, ベルリン, Hamburg, ミュンヘン, シュトゥットガルト}</span><span class="sxs-lookup"><span data-stu-id="ac2c2-174">Cities = {Ottawa, Toronto, Vancouver, Calgary, Seattle, Boise, Los Angeles, Houston, Shreveport, Miami, Boston, New York, London, Dover, Glasgow, Edinburgh, Cardiff, Pembroke, Belfast, Berlin, Hamburg, Munich, Stuttgart}</span></span>

## <a name="members"></a><span data-ttu-id="ac2c2-175">Members</span><span class="sxs-lookup"><span data-stu-id="ac2c2-175">Members</span></span>

<span data-ttu-id="ac2c2-p119">階層のリーフ レベルのメンバーに子はなく、ルート レベルのメンバーに親はありません。他のすべてのメンバーには、少なくとも 1 つの親と 1 つの子があります。たとえば、Geography 次元の階層ツリーを部分的にスキャンすると、以下の親子関係が生成されます。</span><span class="sxs-lookup"><span data-stu-id="ac2c2-p119">Members at the leaf level of a hierarchy have no children, and members at the root level have no parent. All other members have at least one parent and at least one child. For example, a partial traversal of the hierarchy tree in the Geography dimension yields the following parent-child relationships:</span></span>

- <span data-ttu-id="ac2c2-179">いずれ(の親){ヨーロッパ、北アメリカ}</span><span class="sxs-lookup"><span data-stu-id="ac2c2-179">{All} (parent of) {Europe, North America}</span></span>

- <span data-ttu-id="ac2c2-180">{北アメリカ}(の親){カナダ、USA}</span><span class="sxs-lookup"><span data-stu-id="ac2c2-180">{North America} (parent of) {Canada, USA}</span></span>

- <span data-ttu-id="ac2c2-181">英語(の親){米国-NE、USA-NW、USA-SE、USA-SW}</span><span class="sxs-lookup"><span data-stu-id="ac2c2-181">{USA} (parent of) {USA-NE, USA-NW, USA-SE, USA-SW}</span></span>

- <span data-ttu-id="ac2c2-182">{米国-NW}(の親){ボイシ, シアトル}</span><span class="sxs-lookup"><span data-stu-id="ac2c2-182">{USA-NW} (parent of) {Boise, Seattle}</span></span>

<span data-ttu-id="ac2c2-183">メンバーは各次元で 1 つ以上の階層に統合できます。</span><span class="sxs-lookup"><span data-stu-id="ac2c2-183">Members can be consolidated along one or more hierarchies per dimension.</span></span>

<span data-ttu-id="ac2c2-184">また、この例では、年単位階層の週レベルの一部のメンバーが年四半期の階層のどのレベルにも表示されないということも示しています。</span><span class="sxs-lookup"><span data-stu-id="ac2c2-184">This example also illustrates another characteristic: some members of the Week level of the Year-Week hierarchy do not appear in any level of the Year-Quarter hierarchy.</span></span> <span data-ttu-id="ac2c2-185">つまり、階層に次元のすべてのメンバーを含める必要はありません。</span><span class="sxs-lookup"><span data-stu-id="ac2c2-185">Thus, a hierarchy need not include all members of a dimension.</span></span>

