---
title: '第 9 章: データ シェイプ'
TOCTitle: 'Chapter 9: Data Shaping'
ms:assetid: f66a319f-1b3d-c4a3-50b3-af1a47540832
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250253(v=office.15)
ms:contentKeyID: 48548739
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4636c853f58557b30474b78d902131329084a1a2
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863886"
---
# <a name="chapter-9-data-shaping"></a><span data-ttu-id="34309-102">第 9 章: データ シェイプ</span><span class="sxs-lookup"><span data-stu-id="34309-102">Chapter 9: Data Shaping</span></span>


<span data-ttu-id="34309-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="34309-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="34309-104">*データ シェイプ*は、データ ソースのクエリを実行し、2 つまたは複数の論理エンティティ (階層) の間の親子リレーションシップを表す[レコード セット](recordset-object-ado.md)を返す方法を提供します。</span><span class="sxs-lookup"><span data-stu-id="34309-104">*Data shaping* provides a way to query a data source and return a [Recordset](recordset-object-ado.md) that represents a parent-child relationship between two or more logical entities (a hierarchy).</span></span> <span data-ttu-id="34309-105">階層関係の典型的な例は、顧客と注文です。</span><span class="sxs-lookup"><span data-stu-id="34309-105">A classic example of a hierarchical relationship is customers and orders.</span></span> <span data-ttu-id="34309-106">データベース内のすべての顧客の 0 個以上の注文が存在することができます。</span><span class="sxs-lookup"><span data-stu-id="34309-106">For every customer in a database, there can be zero or more orders.</span></span> <span data-ttu-id="34309-107">正規の SQL には、JOIN 構文を使用してデータを取得するための手段が用意されていますが、これは、非効率的で扱いにくいため、指定された親子関係に対して返された各レコード内で冗長な親データが繰り返されます。</span><span class="sxs-lookup"><span data-stu-id="34309-107">Regular SQL provides a means of retrieving the data using JOIN syntax, but this can be inefficient and unwieldy because redundant parent data is repeated in each record returned for a given parent-child relationship.</span></span> <span data-ttu-id="34309-108">データ シェイプと、子**レコード セット**JOIN の冗長性を回避することで複数の子レコードの親**レコード セット**内の 1 つの親レコードを関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="34309-108">Data shaping can relate a single parent record in the parent **Recordset** to multiple child records in the child **Recordset**, avoiding the redundancy of a JOIN.</span></span> <span data-ttu-id="34309-109">ほとんどの人より自然で、1 つの**レコード セット**の結合モデルよりも操作が容易に親と子・複数の**Recordset**プログラミング モデルを検索します。</span><span class="sxs-lookup"><span data-stu-id="34309-109">Most people find the parent-child multiple **Recordset** programming model more natural and easier to work with than the single **Recordset** JOIN model.</span></span>

<span data-ttu-id="34309-p102">データ シェイプの構文には、他の機能もあります。親および子 **Recordset** のフィールドを記述する際に NEW キーワードを使用すると、基になるデータ ソースなしで新しい **Recordset** オブジェクトを作成することができます。この新しい **Recordset** オブジェクトには、データを入力し、永続的に保存することができます。また、開発者は、子フィールドでさまざまな計算や集計 (たとえば、SUM、AVG、および MAX) を実行できます。さらにデータ シェイプでは、子のレコードをグループ化して、親に、子の各グループに対応する 1 つの行を置くことで、子の **Recordset** から親の **Recordset** を作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="34309-p102">The data shaping syntax also provides other capabilities. Developers can create new **Recordset** objects without an underlying data source by using the NEW keyword to describe the fields of the parent and child **Recordsets**. The new **Recordset** object can be populated with data and persistently stored. Developers can also perform various calculations or aggregations (for example, SUM, AVG, and MAX) on child fields. Data shaping can also create a parent **Recordset** from a child **Recordset** by grouping records in the child and placing one row in the parent for each group in the child.</span></span>

<span data-ttu-id="34309-115">データ シェイプの詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="34309-115">See the following topics to learn more about data shaping:</span></span>

- [<span data-ttu-id="34309-116">データ シェイプに必要なプロバイダー</span><span class="sxs-lookup"><span data-stu-id="34309-116">Required Providers for Data Shaping</span></span>](required-providers-for-data-shaping.md)

- [<span data-ttu-id="34309-117">Shape Compute 句</span><span class="sxs-lookup"><span data-stu-id="34309-117">Shape Compute Clause</span></span>](shape-compute-clause.md)

- [<span data-ttu-id="34309-118">階層レコードセットを作成する</span><span class="sxs-lookup"><span data-stu-id="34309-118">Fabricating Hierarchical Recordsets</span></span>](fabricating-hierarchical-recordsets.md)

- [<span data-ttu-id="34309-119">階層 Recordset 内の行にアクセスする</span><span class="sxs-lookup"><span data-stu-id="34309-119">Accessing Rows in a Hierarchical Recordset</span></span>](accessing-rows-in-a-hierarchical-recordset.md)

- [<span data-ttu-id="34309-120">正式な Shape 文法</span><span class="sxs-lookup"><span data-stu-id="34309-120">Formal Shape Grammar</span></span>](formal-shape-grammar.md)

- [<span data-ttu-id="34309-121">Visual Basic for Applications の関数</span><span class="sxs-lookup"><span data-stu-id="34309-121">Visual Basic for Applications functions</span></span>](visual-basic-for-applications-functions.md)

- [<span data-ttu-id="34309-122">Shape Append 句 (ADO)</span><span class="sxs-lookup"><span data-stu-id="34309-122">Shape Append Clause (ADO)</span></span>](shape-append-clause.md)

- [<span data-ttu-id="34309-123">データ シェイプ (ADO)</span><span class="sxs-lookup"><span data-stu-id="34309-123">Data Shaping (ADO)</span></span>](data-shaping.md)

- [<span data-ttu-id="34309-124">一般的な Shape コマンド (ADO)</span><span class="sxs-lookup"><span data-stu-id="34309-124">Shape Commands in General (ADO)</span></span>](shape-commands-in-general.md)

