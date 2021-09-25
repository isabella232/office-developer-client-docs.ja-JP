---
title: データ シェーピング (Access デスクトップ データベースリファレンス)
TOCTitle: Data shaping
ms:assetid: 650571cc-6874-2cdb-dd76-0804d1cc4e38
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249390(v=office.15)
ms:contentKeyID: 48545305
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: abf6d5cd03addcbd658e6ae02b1dc139dd6b8824
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59594364"
---
# <a name="data-shaping"></a>データ シェイプ

**適用先**: Access 2013、Office 2013

データ シェイプにより、シェイプされた **Recordset** の列や、列によって表されるエンティティ間の関連付け、および **Recordset** にデータを入力するときの方法を定義できるようになります。

シェイプされた **Recordset** の列には、Microsoft SQL Server などのデータ プロバイダーからのデータ、他の **Recordset** への参照、 **Recordset** の 1 つの行での計算から導き出される値、 **Recordset** 全体にわたる 1 つの列に対する操作から導き出される値などを含めることができます。また、新規に作成された空の列も含めることができます。

When you retrieve the value of a column that contains a reference to another **Recordset**, ADO automatically returns the actual **Recordset** represented by the reference. A **Recordset** that contains another **Recordset** is called a hierarchical recordset. 階層レコードセットは、親が含まれているレコードセットであり、子が含まれているレコードセットである親子関係を示します。  **Recordset** への参照は、実際にはチャプターと呼ばれる子のサブセットへの *参照です*。 A single parent may reference more than one child **Recordset**.

Shape コマンド構文によって、シェイプされた **Recordset** をプログラムで作成できます。その後、プログラムから、または適切なビジュアル コントロールによって、 **Recordset** のコンポーネントにアクセスできます。シェイプ コマンドは、他の ADO コマンド テキストと同じように発行されます。

Shape コマンド構文を使用して、階層 **Recordset** オブジェクトを 2 つの方法で作成できます。1 つは、子 **Recordset** を親 **Recordset** に追加する方法です。親と子には、少なくとも 1 つの共通の列が必要です。この共通の列では、親の行の列値と、子のすべての行の列値が同じです。

もう 1 つは、子 **Recordset** から親 **Recordset** を生成する方法です。子 **Recordset** のレコードは通常、BY 句 を使用してグループ化され、1 つの行が、子の各グループの親 **Recordset** に追加されます。BY 句を省略した場合、子 **Recordset** は単一のグループを形成し、親 **Recordset** には 1 つの行が含まれます。これは、子 **Recordset** 全体の "総計" 集計を計算する場合に便利です。

親 **Recordset** は、どのように形成されているかには関係なく、子 **Recordset** への関連付けに使用されるチャプター列が含まれます。必要に応じて、親 **Recordset** は、子の行の集計 (SUM、MIN、MAX など) を含む列を持つことができます。親と子の **Recordset** はいずれも、 **Recordset** の行の式を含む列、および、初期状態が空である新しい列を持つことができます。

階層 **Recordset** オブジェクトは、任意の深さまで入れ子にできます (つまり、子 **Recordset** オブジェクトの子 **Recordset** オブジェクトをさらに作成する操作を繰り返し実行できます)。

シェイプされた **Recordset** の **Recordset** コンポーネントには、プログラムから、または適切なビジュアル コンポーネントによってアクセスできます。

シェイプ コマンドおよびその結果生成される階層の例については、「Using the Data Shaping Service for OLE DB: A Closer Look」 (英語) を参照してください。

このセクションでは、以下のトピックについて説明します。

- [リシェイプ](reshaping.md)
- [孫の集計](grandchild-aggregates.md)
- [COMPUTE 句の挿入によってパラメーター化されたコマンド](parameterized-commands-with-intervening-compute-commands.md)
- [階層レコードセットの永続化](persisting-hierarchical-recordsets.md)
