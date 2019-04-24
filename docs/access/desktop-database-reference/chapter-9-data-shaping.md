---
title: '第 9 章: データ シェイプ'
TOCTitle: 'Chapter 9: Data shaping'
ms:assetid: f66a319f-1b3d-c4a3-50b3-af1a47540832
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250253(v=office.15)
ms:contentKeyID: 48548739
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 43ad9d5e989bc1c6f4a54fb4882cfe3c3e357fd1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296424"
---
# <a name="chapter-9-data-shaping"></a><span data-ttu-id="0d31a-102">第 9 章: データ シェイプ</span><span class="sxs-lookup"><span data-stu-id="0d31a-102">Chapter 9: Data shaping</span></span>

<span data-ttu-id="0d31a-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="0d31a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0d31a-104">*データシェイプ*では、データソースに対してクエリを実行し、2つ以上の論理エンティティ (階層) 間の親子関係を表す[Recordset](recordset-object-ado.md)を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="0d31a-104">*Data shaping* provides a way to query a data source and return a [Recordset](recordset-object-ado.md) that represents a parent-child relationship between two or more logical entities (a hierarchy).</span></span> 

<span data-ttu-id="0d31a-105">A classic example of a hierarchical relationship is customers and orders.</span><span class="sxs-lookup"><span data-stu-id="0d31a-105">A classic example of a hierarchical relationship is customers and orders.</span></span> <span data-ttu-id="0d31a-106">For every customer in a database, there can be zero or more orders.</span><span class="sxs-lookup"><span data-stu-id="0d31a-106">For every customer in a database, there can be zero or more orders.</span></span> <span data-ttu-id="0d31a-107">Regular SQL provides a means of retrieving the data using JOIN syntax, but this can be inefficient and unwieldy because redundant parent data is repeated in each record returned for a given parent-child relationship.</span><span class="sxs-lookup"><span data-stu-id="0d31a-107">Regular SQL provides a means of retrieving the data using JOIN syntax, but this can be inefficient and unwieldy because redundant parent data is repeated in each record returned for a given parent-child relationship.</span></span> <span data-ttu-id="0d31a-108">Data shaping can relate a single parent record in the parent **Recordset** to multiple child records in the child **Recordset**, avoiding the redundancy of a JOIN.</span><span class="sxs-lookup"><span data-stu-id="0d31a-108">Data shaping can relate a single parent record in the parent **Recordset** to multiple child records in the child **Recordset**, avoiding the redundancy of a JOIN.</span></span> <span data-ttu-id="0d31a-109">Most people find the parent-child multiple **Recordset** programming model more natural and easier to work with than the single **Recordset** JOIN model.</span><span class="sxs-lookup"><span data-stu-id="0d31a-109">Most people find the parent-child multiple **Recordset** programming model more natural and easier to work with than the single **Recordset** JOIN model.</span></span>

<span data-ttu-id="0d31a-p102">データ シェイプの構文には、他の機能もあります。親および子 **Recordset** のフィールドを記述する際に NEW キーワードを使用すると、基になるデータ ソースなしで新しい **Recordset** オブジェクトを作成することができます。この新しい **Recordset** オブジェクトには、データを入力し、永続的に保存することができます。また、開発者は、子フィールドでさまざまな計算や集計 (たとえば、SUM、AVG、および MAX) を実行できます。さらにデータ シェイプでは、子のレコードをグループ化して、親に、子の各グループに対応する 1 つの行を置くことで、子の **Recordset** から親の **Recordset** を作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="0d31a-p102">The data shaping syntax also provides other capabilities. Developers can create new **Recordset** objects without an underlying data source by using the NEW keyword to describe the fields of the parent and child **Recordsets**. The new **Recordset** object can be populated with data and persistently stored. Developers can also perform various calculations or aggregations (for example, SUM, AVG, and MAX) on child fields. Data shaping can also create a parent **Recordset** from a child **Recordset** by grouping records in the child and placing one row in the parent for each group in the child.</span></span>

<span data-ttu-id="0d31a-115">データ シェイプの詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="0d31a-115">See the following topics to learn more about data shaping:</span></span>

- [<span data-ttu-id="0d31a-116">データ シェイプに必要なプロバイダー</span><span class="sxs-lookup"><span data-stu-id="0d31a-116">Required providers for data shaping</span></span>](required-providers-for-data-shaping.md)
- [<span data-ttu-id="0d31a-117">Shape COMPUTE 句</span><span class="sxs-lookup"><span data-stu-id="0d31a-117">Shape Compute clause</span></span>](shape-compute-clause.md)
- [<span data-ttu-id="0d31a-118">階層レコードセットの生成</span><span class="sxs-lookup"><span data-stu-id="0d31a-118">Fabricating hierarchical Recordsets</span></span>](fabricating-hierarchical-recordsets.md)
- [<span data-ttu-id="0d31a-119">階層レコードセット内の行へのアクセス</span><span class="sxs-lookup"><span data-stu-id="0d31a-119">Accessing rows in a hierarchical Recordset</span></span>](accessing-rows-in-a-hierarchical-recordset.md)
- [<span data-ttu-id="0d31a-120">正式な Shape 文法</span><span class="sxs-lookup"><span data-stu-id="0d31a-120">Formal shape grammar</span></span>](formal-shape-grammar.md)
- [<span data-ttu-id="0d31a-121">Visual Basic for Applications の関数</span><span class="sxs-lookup"><span data-stu-id="0d31a-121">Visual Basic for Applications functions</span></span>](visual-basic-for-applications-functions.md)
- [<span data-ttu-id="0d31a-122">Shape Append 句 (ADO)</span><span class="sxs-lookup"><span data-stu-id="0d31a-122">Shape Append clause (ADO)</span></span>](shape-append-clause.md)
- [<span data-ttu-id="0d31a-123">データシェイプ (ADO)</span><span class="sxs-lookup"><span data-stu-id="0d31a-123">Data shaping (ADO)</span></span>](data-shaping.md)
- [<span data-ttu-id="0d31a-124">一般的な Shape コマンド (ADO)</span><span class="sxs-lookup"><span data-stu-id="0d31a-124">Shape commands in general (ADO)</span></span>](shape-commands-in-general.md)

