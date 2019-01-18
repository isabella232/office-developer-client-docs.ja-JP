---
title: Cellset オブジェクト (ADO MD)
TOCTitle: Cellset object (ADO MD)
ms:assetid: 28d4b3b9-f907-9ec0-00e1-9666c887cdf0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249047(v=office.15)
ms:contentKeyID: 48543869
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c8cb75ad7277386cfe81b2edcffa234498318444
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702188"
---
# <a name="cellset-object-ado-md"></a><span data-ttu-id="c54b3-102">Cellset オブジェクト (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="c54b3-102">Cellset object (ADO MD)</span></span>

<span data-ttu-id="c54b3-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="c54b3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c54b3-p101">多次元クエリの結果を表します。キューブまたは他のセルセットから選択されたセルのコレクションになります。</span><span class="sxs-lookup"><span data-stu-id="c54b3-p101">Represents the results of a multidimensional query. It is a collection of cells selected from cubes or other cellsets.</span></span>

## <a name="remarks"></a><span data-ttu-id="c54b3-106">解説</span><span class="sxs-lookup"><span data-stu-id="c54b3-106">Remarks</span></span>

<span data-ttu-id="c54b3-p102">**Cellset** 内のデータは、直接の配列のようなアクセス方法を使用して取得できます。特定のメンバーに "ドリル ダウン" してそのメンバーに関するデータを取得できます。たとえば、次のコードは、cst というセルセットの最初の軸の最初の位置の最初のメンバーのキャプションを返します。</span><span class="sxs-lookup"><span data-stu-id="c54b3-p102">Data within a **Cellset** is retrieved using direct, array-like access. You can "drill down" to a specific member to obtain data about that member. For example, the following code returns the caption of the first member in the first position on the first axis of a cellset named cst:</span></span>

`cst.Axes(0).Positions(0).Members(0).Caption`

<span data-ttu-id="c54b3-p103">セルセットには現在のセルの概念はありませんが、代わりに [Item](item-property-ado-md-cellset.md) プロパティを使用して、セルセットの特定の [Cell](cell-object-ado-md.md) オブジェクトを取得できます。取得するセルは、 **Item** プロパティの引数によって指定します。セルの一意の序数値を指定できます。セルセットの各軸上の位置番号を使用してセルを取得することもできます。セルの取得方法の詳細については、 [Item](item-property-ado-md-cellset.md) プロパティを参照してください。</span><span class="sxs-lookup"><span data-stu-id="c54b3-p103">There is no notion of a current cell within a cellset. Instead, the [Item](item-property-ado-md-cellset.md) property retrieves a specific [Cell](cell-object-ado-md.md) object from the cellset. The arguments of the **Item** property determine which cell is retrieved. You can specify the unique ordinal value of a cell. You can also retrieve cells by using their position numbers along each axis of the cellset. For more information about retrieving cells, see the [Item](item-property-ado-md-cellset.md) property.</span></span>

<span data-ttu-id="c54b3-116">**Cellset** オブジェクトのコレクション、メソッド、およびプロパティを使用すると、次の操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="c54b3-116">With the collections, methods, and properties of a **Cellset** object, you can do the following:</span></span>

  - <span data-ttu-id="c54b3-117">**Cellset** オブジェクトの [ActiveConnection](activeconnection-property-ado-md.md) プロパティを使用して、開いている接続をそのオブジェクトに関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="c54b3-117">Associate an open connection with a **Cellset** object by setting its [ActiveConnection](activeconnection-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="c54b3-118">[Open](open-method-ado-md.md) メソッドを使用して、多次元クエリを実行して結果を取得します。</span><span class="sxs-lookup"><span data-stu-id="c54b3-118">Execute and retrieve the results of a multidimensional query with the [Open](open-method-ado-md.md) method.</span></span>

  - <span data-ttu-id="c54b3-119">**Item** プロパティを使用して、 **Cellset** から [Cell](item-property-ado-md-cellset.md) を取得します。</span><span class="sxs-lookup"><span data-stu-id="c54b3-119">Retrieve a **Cell** from the **Cellset** with the [Item](item-property-ado-md-cellset.md) property.</span></span>

  - <span data-ttu-id="c54b3-120">[Axes](axis-object-ado-md.md) コレクションを使用して、 **Cellset** を定義する [Axis](axes-collection-ado-md.md) オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="c54b3-120">Return the [Axis](axis-object-ado-md.md) objects that define the **Cellset** with the [Axes](axes-collection-ado-md.md) collection.</span></span>

  - <span data-ttu-id="c54b3-121">**FilterAxis** プロパティを使用して、 [Cellset](filteraxis-property-ado-md.md) 内のデータをフィルター処理するための次元に関する情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="c54b3-121">Retrieve information about the dimensions used to filter the data in the **Cellset** with the [FilterAxis](filteraxis-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="c54b3-122">**Source** プロパティを使用して、 [Cellset](source-property-ado-md.md) を定義するためのクエリを返すか、または指定します。</span><span class="sxs-lookup"><span data-stu-id="c54b3-122">Return or specify the query used to define the **Cellset** with the [Source](source-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="c54b3-123">**State** プロパティを使用して、 [Cellset](state-property-ado-md.md) の現在の状態 (開いている、閉じている、実行中、または接続中) を返します。</span><span class="sxs-lookup"><span data-stu-id="c54b3-123">Return the current state of the **Cellset** (open, closed, executing, or connecting) with the [State](state-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="c54b3-124">**Close** メソッドを使用して、 [Cellset](close-method-ado-md.md) を開くか、または閉じます。</span><span class="sxs-lookup"><span data-stu-id="c54b3-124">Close an open **Cellset** with the [Close](close-method-ado-md.md) method.</span></span>

  - <span data-ttu-id="c54b3-125">標準の ADO **Properties** コレクションを使用して、 [Cellset](properties-collection-ado.md) に関するプロバイダー固有の情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="c54b3-125">Retrieve provider-specific information about the **Cellset** with the standard ADO [Properties](properties-collection-ado.md) collection.</span></span>

