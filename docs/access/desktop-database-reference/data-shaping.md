---
title: データ シェイプ (デスクトップ データベース参照のアクセス)
TOCTitle: Data shaping
ms:assetid: 650571cc-6874-2cdb-dd76-0804d1cc4e38
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249390(v=office.15)
ms:contentKeyID: 48545305
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 96a5d7ad82c7cb9182f95b428ff17c9df60c47b3
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947099"
---
# <a name="data-shaping"></a><span data-ttu-id="6bcfb-102">データ シェイプ</span><span class="sxs-lookup"><span data-stu-id="6bcfb-102">Data shaping</span></span>

<span data-ttu-id="6bcfb-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="6bcfb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6bcfb-104">データ シェイプにより、シェイプされた **Recordset** の列や、列によって表されるエンティティ間の関連付け、および **Recordset** にデータを入力するときの方法を定義できるようになります。</span><span class="sxs-lookup"><span data-stu-id="6bcfb-104">Data shaping enables you to define the columns of a shaped **Recordset**, the relationships between the entities represented by the columns, and the manner in which the **Recordset** is populated with data.</span></span>

<span data-ttu-id="6bcfb-105">シェイプされた **Recordset** の列には、Microsoft SQL Server などのデータ プロバイダーからのデータ、他の **Recordset** への参照、 **Recordset** の 1 つの行での計算から導き出される値、 **Recordset** 全体にわたる 1 つの列に対する操作から導き出される値などを含めることができます。また、新規に作成された空の列も含めることができます。</span><span class="sxs-lookup"><span data-stu-id="6bcfb-105">Columns of a shaped **Recordset** may contain data from a data provider such as Microsoft SQL Server, references to another **Recordset**, values derived from a calculation on a single row of a **Recordset**, values derived from an operation over a column of an entire **Recordset**; or they may be a newly fabricated, empty column.</span></span>

<span data-ttu-id="6bcfb-106">別の**レコード セット**への参照が含まれる列の値を取得するとき、ADO は実際の**レコード セット**は参照によって表される自動的に返します。</span><span class="sxs-lookup"><span data-stu-id="6bcfb-106">When you retrieve the value of a column that contains a reference to another **Recordset**, ADO automatically returns the actual **Recordset** represented by the reference.</span></span> <span data-ttu-id="6bcfb-107">別の**レコード セット**が含まれている**レコード セット**は、階層レコード セットと呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="6bcfb-107">A **Recordset** that contains another **Recordset** is called a hierarchical recordset.</span></span> <span data-ttu-id="6bcfb-108">階層レコード セットの*親*を含んでいるし、*子*が含まれているレコード セットを*親と子*の関係が発生します。</span><span class="sxs-lookup"><span data-stu-id="6bcfb-108">Hierarchical recordsets exhibit a *parent-child* relationship, in which the *parent* is the containing recordset and the *child* is the contained recordset.</span></span> <span data-ttu-id="6bcfb-109">*章*と呼ばれる子のサブセットへの参照を実際には、**レコード セット**への参照です。</span><span class="sxs-lookup"><span data-stu-id="6bcfb-109">The reference to a **Recordset** is actually a reference to a subset of the child, called a *chapter*.</span></span> <span data-ttu-id="6bcfb-110">1 つの親は、複数の子**レコード セット**を参照することができません。</span><span class="sxs-lookup"><span data-stu-id="6bcfb-110">A single parent may reference more than one child **Recordset**.</span></span>

<span data-ttu-id="6bcfb-p102">Shape コマンド構文によって、シェイプされた **Recordset** をプログラムで作成できます。その後、プログラムから、または適切なビジュアル コントロールによって、 **Recordset** のコンポーネントにアクセスできます。シェイプ コマンドは、他の ADO コマンド テキストと同じように発行されます。</span><span class="sxs-lookup"><span data-stu-id="6bcfb-p102">The shape command syntax enables you to programmatically create a shaped **Recordset**. You can then access the components of the **Recordset** programmatically or through an appropriate visual control. A shape command is issued like any other ADO command text.</span></span>

<span data-ttu-id="6bcfb-p103">Shape コマンド構文を使用して、階層 **Recordset** オブジェクトを 2 つの方法で作成できます。1 つは、子 **Recordset** を親 **Recordset** に追加する方法です。親と子には、少なくとも 1 つの共通の列が必要です。この共通の列では、親の行の列値と、子のすべての行の列値が同じです。</span><span class="sxs-lookup"><span data-stu-id="6bcfb-p103">You can make hierarchical **Recordset** objects in two ways with the shape command syntax. The first appends a child **Recordset** to a parent **Recordset**. The parent and child typically have at least one column in common: the value of the column in a row of the parent is the same as the value of the column in all rows of the child.</span></span>

<span data-ttu-id="6bcfb-p104">もう 1 つは、子 **Recordset** から親 **Recordset** を生成する方法です。子 **Recordset** のレコードは通常、BY 句 を使用してグループ化され、1 つの行が、子の各グループの親 **Recordset** に追加されます。BY 句を省略した場合、子 **Recordset** は単一のグループを形成し、親 **Recordset** には 1 つの行が含まれます。これは、子 **Recordset** 全体の "総計" 集計を計算する場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="6bcfb-p104">The second way generates a parent **Recordset** from a child **Recordset**. The records in the child **Recordset** are grouped, typically using the BY clause, and one row is added to the parent **Recordset** for each resulting group in the child. If the BY clause is omitted, the child **Recordset** will form a single group and the parent **Recordset** will contain exactly one row. This is useful for computing "grand total" aggregates over the entire child **Recordset**.</span></span>

<span data-ttu-id="6bcfb-p105">親 **Recordset** は、どのように形成されているかには関係なく、子 **Recordset** への関連付けに使用されるチャプター列が含まれます。必要に応じて、親 **Recordset** は、子の行の集計 (SUM、MIN、MAX など) を含む列を持つことができます。親と子の **Recordset** はいずれも、 **Recordset** の行の式を含む列、および、初期状態が空である新しい列を持つことができます。</span><span class="sxs-lookup"><span data-stu-id="6bcfb-p105">Regardless of which way the parent **Recordset** is formed, it will contain a chapter column that is used to relate it to a child **Recordset**. If you wish, the parent **Recordset** may also have columns that contain aggregates (SUM, MIN, MAX, and so on) over the child rows. Both the parent and the child **Recordset** may have columns which contain an expression on the row in the **Recordset**, as well as columns which are new and initially empty.</span></span>

<span data-ttu-id="6bcfb-124">階層 **Recordset** オブジェクトは、任意の深さまで入れ子にできます (つまり、子 **Recordset** オブジェクトの子 **Recordset** オブジェクトをさらに作成する操作を繰り返し実行できます)。</span><span class="sxs-lookup"><span data-stu-id="6bcfb-124">You can nest hierarchical **Recordset** objects to any depth (that is, create child **Recordset** objects of child **Recordset** objects, and so on).</span></span>

<span data-ttu-id="6bcfb-125">シェイプされた **Recordset** の **Recordset** コンポーネントには、プログラムから、または適切なビジュアル コンポーネントによってアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="6bcfb-125">You can access the **Recordset** components of the shaped **Recordset** programmatically or through an appropriate visual control.</span></span>

<span data-ttu-id="6bcfb-126">シェイプ コマンドおよびその結果生成される階層の例については、「Using the Data Shaping Service for OLE DB: A Closer Look」 (英語) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6bcfb-126">For examples of shape commands and their resulting hierarchies, see Using the Data Shaping Service for OLE DB: A Closer Look.</span></span>

<span data-ttu-id="6bcfb-127">このセクションには、次のトピックが含まれています。</span><span class="sxs-lookup"><span data-stu-id="6bcfb-127">This section includes the following topics:</span></span>

- [<span data-ttu-id="6bcfb-128">リシェイプ</span><span class="sxs-lookup"><span data-stu-id="6bcfb-128">Reshaping</span></span>](reshaping.md)
- [<span data-ttu-id="6bcfb-129">孫の集計</span><span class="sxs-lookup"><span data-stu-id="6bcfb-129">Grandchild aggregates</span></span>](grandchild-aggregates.md)
- [<span data-ttu-id="6bcfb-130">計算の間にあるコマンドを使用してパラメーター化されたコマンド</span><span class="sxs-lookup"><span data-stu-id="6bcfb-130">Parameterized commands with intervening COMPUTE commands</span></span>](parameterized-commands-with-intervening-compute-commands.md)
- [<span data-ttu-id="6bcfb-131">階層レコード セットを永続化します。</span><span class="sxs-lookup"><span data-stu-id="6bcfb-131">Persisting hierarchical Recordsets</span></span>](persisting-hierarchical-recordsets.md)