---
title: 多次元データの使用
TOCTitle: Working with multidimensional data
ms:assetid: a0c9ac73-04da-cfdd-8787-15c8a53ff819
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249740(v=office.15)
ms:contentKeyID: 48546717
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 67b22219fdbbec8bf518b7be0fabd9a6adfbcf7f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726072"
---
# <a name="working-with-multidimensional-data"></a><span data-ttu-id="0878a-102">多次元データの使用</span><span class="sxs-lookup"><span data-stu-id="0878a-102">Working with multidimensional data</span></span>

<span data-ttu-id="0878a-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="0878a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0878a-104">*セルセット*は、多次元データのクエリの結果です。</span><span class="sxs-lookup"><span data-stu-id="0878a-104">A *cellset* is the result of a query on multidimensional data.</span></span> <span data-ttu-id="0878a-105">軸、通常 4 つ以内の軸と通常 2 つまたは 3 つのコレクションで構成されています。</span><span class="sxs-lookup"><span data-stu-id="0878a-105">It consists of a collection of axes, usually no more than four axes and typically only two or three.</span></span> <span data-ttu-id="0878a-106">*軸*は、検索またはキューブ内の特定の値をフィルター処理に使用される 1 つまたは複数のディメンションのメンバーのコレクションです。</span><span class="sxs-lookup"><span data-stu-id="0878a-106">An *axis* is a collection of members from one or more dimensions, which is used to locate or filter specific values in a cube.</span></span>

<span data-ttu-id="0878a-107">*位置*は、軸に沿ったポイントです。</span><span class="sxs-lookup"><span data-stu-id="0878a-107">A *position* is a point along an axis.</span></span> <span data-ttu-id="0878a-108">1 つのディメンションで構成される軸の位置は、ディメンション メンバーのサブセットです。</span><span class="sxs-lookup"><span data-stu-id="0878a-108">For an axis consisting of a single dimension, these positions are a subset of the dimension members.</span></span> <span data-ttu-id="0878a-109">軸は、複数のディメンションから構成されている場合、各位置は*その軸に沿った方向の次元の数が* *n*の部分から構成される複合エンティティには、</span><span class="sxs-lookup"><span data-stu-id="0878a-109">If an axis consists of more than one dimension, then each position is a compound entity, which has *n* parts where *n* is the number of dimensions oriented along that axis.</span></span> <span data-ttu-id="0878a-110">位置の各部分は、1 つの構成要素であるディメンションのメンバーです。</span><span class="sxs-lookup"><span data-stu-id="0878a-110">Each part of the position is a member from one constituent dimension.</span></span>

<span data-ttu-id="0878a-p103">たとえば、売上データを含むキューブの Geography 次元と Product 次元がセルセットの x 軸に沿っている場合、この軸上の位置には、"USA" メンバーと "Computers" メンバーが含まれます。この例で、x 軸に沿った位置を決定するには、各次元のメンバーが軸に沿っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="0878a-p103">For example, if the Geography and Product dimensions from a cube containing sales data are oriented along the x-axis of a cellset, a position along this axis may contain the members "USA" and "Computers." In this example, determining a position along the x-axis requires that members from each dimension are oriented along the axis.</span></span>

<span data-ttu-id="0878a-113">*セル*は、軸座標の交点にあるオブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="0878a-113">A *cell* is an object positioned at the intersection of axis coordinates.</span></span> <span data-ttu-id="0878a-114">各セルには、データ自体、フォーマット済み文字列 (表示可能形式のセル データ)、セルの序数値などの複数の関連情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="0878a-114">Each cell has multiple pieces of information associated with it, including the data itself, a formatted string (the displayable form of cell data), and the cell ordinal value.</span></span> <span data-ttu-id="0878a-115">各セルは、セルセットで一意の序数値です。</span><span class="sxs-lookup"><span data-stu-id="0878a-115">(Each cell is a unique ordinal value in the cellset.</span></span> <span data-ttu-id="0878a-116">セルセットの最初のセルの序数値はゼロで、8 列あるセルセットの 2 行目の一番左のセルの序数値は 8 です。</span><span class="sxs-lookup"><span data-stu-id="0878a-116">The ordinal value of the first cell in the cellset is zero, while the leftmost cell in the second row of a cellset with eight columns would have an ordinal value of eight.)</span></span>

<span data-ttu-id="0878a-117">たとえば、キューブに以下の 6 つの次元があるとします。このキューブのスキーマは、「[多次元スキーマおよびデータの概要](overview-of-multidimensional-schemas-and-data.md)」の例と多少異なることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="0878a-117">For example, a cube has the following six dimensions (note that this cube schema differs slightly from the example given in [Overview of Multidimensional Schemas and Data](overview-of-multidimensional-schemas-and-data.md)):</span></span>

- <span data-ttu-id="0878a-118">Salesperson</span><span class="sxs-lookup"><span data-stu-id="0878a-118">Salesperson</span></span>
- <span data-ttu-id="0878a-119">Geography (地理的な階層) - Continents、Countries、States など</span><span class="sxs-lookup"><span data-stu-id="0878a-119">Geography (natural hierarchy) — Continents, Countries, States, and so on</span></span>
- <span data-ttu-id="0878a-120">Quarters - Quarters、Months、Days</span><span class="sxs-lookup"><span data-stu-id="0878a-120">Quarters — Quarters, Months, Days</span></span>
- <span data-ttu-id="0878a-121">Years</span><span class="sxs-lookup"><span data-stu-id="0878a-121">Years</span></span>
- <span data-ttu-id="0878a-122">Measures - Sales、PercentChange、BudgetedSales</span><span class="sxs-lookup"><span data-stu-id="0878a-122">Measures — Sales, PercentChange, BudgetedSales</span></span>
- <span data-ttu-id="0878a-123">Products</span><span class="sxs-lookup"><span data-stu-id="0878a-123">Products</span></span>

> [!NOTE]
> <span data-ttu-id="0878a-124">[!メモ] この例のセル値は軸位置の序数の整列されたペアとして表示でき、最初の桁は x 軸の位置を表し、2 桁目が Y 軸の位置を表します。</span><span class="sxs-lookup"><span data-stu-id="0878a-124">The cell values in the example can be viewed as ordered pairs of axis position ordinals where the first digit represents the x-axis position and the second digit the y-axis position.</span></span>

<span data-ttu-id="0878a-125">このセルセットの特性は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="0878a-125">The characteristics of this cellset are as follows:</span></span>

- <span data-ttu-id="0878a-126">軸の次元: Quarters、Salesperson、Geography</span><span class="sxs-lookup"><span data-stu-id="0878a-126">Axis dimensions: Quarters, Salesperson, Geography</span></span>

- <span data-ttu-id="0878a-127">フィルター次元: Measures、Years、Products</span><span class="sxs-lookup"><span data-stu-id="0878a-127">Filter dimensions: Measures, Years, Products</span></span>

- <span data-ttu-id="0878a-128">2 つの軸: COLUMN (x または Axis 0) と ROW (y または Axis 1)</span><span class="sxs-lookup"><span data-stu-id="0878a-128">Two axes: COLUMN (x, or Axis 0) and ROW (y, or Axis 1)</span></span>

- <span data-ttu-id="0878a-129">x 軸: ネストされた 2 つの次元 (Salesperson と Geography)</span><span class="sxs-lookup"><span data-stu-id="0878a-129">x-axis: two nested dimensions, Salesperson and Geography</span></span>

- <span data-ttu-id="0878a-130">y 軸: Quarters 次元</span><span class="sxs-lookup"><span data-stu-id="0878a-130">y-axis: Quarters dimension</span></span>

<span data-ttu-id="0878a-p105">x 軸には、Salesperson と Geography という 2 つの次元があります。Geography からは、Seattle、Boston、USA-South、および Japan の 4 つのメンバーが選択されます。Salesperson からは、Valentine と Nash という 2 つのメンバーが選択されます。これによって、この軸には合計 8 つの位置が生成されます (8 = 4 \*2)。</span><span class="sxs-lookup"><span data-stu-id="0878a-p105">The x-axis has two nested dimensions: Salesperson and Geography. From Geography, four members are selected: Seattle, Boston, USA-South, and Japan. Two members are selected from Salesperson: Valentine and Nash. This yields a total of eight positions on this axis (8 = 4\*2).</span></span>

<span data-ttu-id="0878a-135">各座標は、Salesperson 次元と Geography 次元から 1 つずつの 2 つのメンバーを持つ位置として表されます。</span><span class="sxs-lookup"><span data-stu-id="0878a-135">Each coordinate is represented as a position with two members — one from the Salesperson dimension and another from the Geography dimension:</span></span>

```vb 
 
(Valentine, Seattle), (Valentine, Boston), (Valentine, USA_North), 
(Valentine, Japan), (Nash, Seattle), (Nash, Boston), (Nash, USA_North), 
(Nash, Japan) 
```

<span data-ttu-id="0878a-136">Y 軸の次元は 1 つだけで、以下の 8 つの位置があります。</span><span class="sxs-lookup"><span data-stu-id="0878a-136">The y-axis has only one dimension, containing the following eight positions:</span></span>

```vb 
 
Jan, Feb, Mar, Qtr2, Qtr3, Oct, Nov, Dec 
```

<span data-ttu-id="0878a-137">セルセット、セル、軸、および位置は、すべて ADO MD の対応するオブジェクトによって表されます ([Cellset](cellset-object-ado-md.md)、[Cell](cell-object-ado-md.md)、[Axis](axis-object-ado-md.md)、および [Position](position-object-ado-md.md))。</span><span class="sxs-lookup"><span data-stu-id="0878a-137">Cellsets, cells, axes, and positions are all represented in ADO MD by corresponding objects: [Cellset](cellset-object-ado-md.md), [Cell](cell-object-ado-md.md), [Axis](axis-object-ado-md.md), and [Position](position-object-ado-md.md).</span></span>

