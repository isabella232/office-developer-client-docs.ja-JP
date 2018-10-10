---
title: '9 章: データ シェイプ'
TOCTitle: 'Chapter 9: Data Shaping'
ms:assetid: f66a319f-1b3d-c4a3-50b3-af1a47540832
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250253(v=office.15)
ms:contentKeyID: 48548739
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8217be1004ea8304501e7d32908b8af269873b7a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478729"
---
# <a name="chapter-9-data-shaping"></a><span data-ttu-id="fae0b-102">9 章: データ シェイプ</span><span class="sxs-lookup"><span data-stu-id="fae0b-102">Chapter 9: Data Shaping</span></span>


<span data-ttu-id="fae0b-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="fae0b-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="fae0b-104">*データ シェイプ*は、データ ソースのクエリを実行し、2 つまたは複数の論理エンティティ (階層) の間の親子リレーションシップを表す[レコード セット](recordset-object-ado.md)を返す方法を提供します。</span><span class="sxs-lookup"><span data-stu-id="fae0b-104">*Data shaping* provides a way to query a data source and return a [Recordset](recordset-object-ado.md) that represents a parent-child relationship between two or more logical entities (a hierarchy).</span></span> <span data-ttu-id="fae0b-105">階層関係の典型的な例は、顧客と注文です。</span><span class="sxs-lookup"><span data-stu-id="fae0b-105">A classic example of a hierarchical relationship is customers and orders.</span></span> <span data-ttu-id="fae0b-106">データベース内のすべての顧客の 0 個以上の注文が存在することができます。</span><span class="sxs-lookup"><span data-stu-id="fae0b-106">For every customer in a database, there can be zero or more orders.</span></span> <span data-ttu-id="fae0b-107">正規の SQL には、JOIN 構文を使用してデータを取得するための手段が用意されていますが、これは、非効率的で扱いにくいため、指定された親子関係に対して返された各レコード内で冗長な親データが繰り返されます。</span><span class="sxs-lookup"><span data-stu-id="fae0b-107">Regular SQL provides a means of retrieving the data using JOIN syntax, but this can be inefficient and unwieldy because redundant parent data is repeated in each record returned for a given parent-child relationship.</span></span> <span data-ttu-id="fae0b-108">データ シェイプと、子**レコード セット**JOIN の冗長性を回避することで複数の子レコードの親**レコード セット**内の 1 つの親レコードを関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="fae0b-108">Data shaping can relate a single parent record in the parent **Recordset** to multiple child records in the child **Recordset**, avoiding the redundancy of a JOIN.</span></span> <span data-ttu-id="fae0b-109">ほとんどの人より自然で、1 つの**レコード セット**の結合モデルよりも操作が容易に親と子・複数の**Recordset**プログラミング モデルを検索します。</span><span class="sxs-lookup"><span data-stu-id="fae0b-109">Most people find the parent-child multiple **Recordset** programming model more natural and easier to work with than the single **Recordset** JOIN model.</span></span>

<span data-ttu-id="fae0b-p102">データ シェイプの構文には、他の機能もあります。親および子 **Recordset** のフィールドを記述する際に NEW キーワードを使用すると、基になるデータ ソースなしで新しい **Recordset** オブジェクトを作成することができます。この新しい **Recordset** オブジェクトには、データを入力し、永続的に保存することができます。また、開発者は、子フィールドでさまざまな計算や集計 (たとえば、SUM、AVG、および MAX) を実行できます。さらにデータ シェイプでは、子のレコードをグループ化して、親に、子の各グループに対応する 1 つの行を置くことで、子の **Recordset** から親の **Recordset** を作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="fae0b-p102">The data shaping syntax also provides other capabilities. Developers can create new **Recordset** objects without an underlying data source by using the NEW keyword to describe the fields of the parent and child **Recordsets**. The new **Recordset** object can be populated with data and persistently stored. Developers can also perform various calculations or aggregations (for example, SUM, AVG, and MAX) on child fields. Data shaping can also create a parent **Recordset** from a child **Recordset** by grouping records in the child and placing one row in the parent for each group in the child.</span></span>

<span data-ttu-id="fae0b-115">データ シェイプの詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="fae0b-115">See the following topics to learn more about data shaping:</span></span>

  - [<span data-ttu-id="fae0b-116">データ シェイプの概要</span><span class="sxs-lookup"><span data-stu-id="fae0b-116">Data Shaping Summary</span></span>](data-shaping-summary.md)

  - [<span data-ttu-id="fae0b-117">データ シェイプに必要なプロバイダー</span><span class="sxs-lookup"><span data-stu-id="fae0b-117">Required Providers for Data Shaping</span></span>](required-providers-for-data-shaping.md)

  - [<span data-ttu-id="fae0b-118">一般的な Shape コマンド</span><span class="sxs-lookup"><span data-stu-id="fae0b-118">Shape Commands in General</span></span>](shape-commands-in-general.md)

  - [<span data-ttu-id="fae0b-119">Shape Append 句</span><span class="sxs-lookup"><span data-stu-id="fae0b-119">Shape APPEND Clause</span></span>](shape-append-clause.md)

  - [<span data-ttu-id="fae0b-120">Shape Compute 句</span><span class="sxs-lookup"><span data-stu-id="fae0b-120">Shape COMPUTE Clause</span></span>](shape-compute-clause.md)

  - [<span data-ttu-id="fae0b-121">階層レコードセットを製造する</span><span class="sxs-lookup"><span data-stu-id="fae0b-121">Fabricating Hierarchical Recordsets</span></span>](fabricating-hierarchical-recordsets.md)

  - [<span data-ttu-id="fae0b-122">階層 Recordset 内の行にアクセスする</span><span class="sxs-lookup"><span data-stu-id="fae0b-122">Accessing Rows in a Hierarchical Recordset</span></span>](accessing-rows-in-a-hierarchical-recordset.md)

  - [<span data-ttu-id="fae0b-123">正式な Shape 文法</span><span class="sxs-lookup"><span data-stu-id="fae0b-123">Formal Shape Grammar</span></span>](formal-shape-grammar.md)

  - [<span data-ttu-id="fae0b-124">Visual Basic for Applications の関数</span><span class="sxs-lookup"><span data-stu-id="fae0b-124">Visual Basic for Applications Functions</span></span>](visual-basic-for-applications-functions.md)

