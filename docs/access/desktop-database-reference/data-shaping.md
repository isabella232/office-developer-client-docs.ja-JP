---
title: データ シェイプ (デスクトップ データベース参照のアクセス)
TOCTitle: Data shaping
ms:assetid: 650571cc-6874-2cdb-dd76-0804d1cc4e38
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249390(v=office.15)
ms:contentKeyID: 48545305
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ad507ac8c963f1d6ead7bc3bf444e694d83f90e3
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716811"
---
# <a name="data-shaping"></a>データ シェイプ

**適用されます**Access 2013、Office 2013。

データ シェイプにより、シェイプされた **Recordset** の列や、列によって表されるエンティティ間の関連付け、および **Recordset** にデータを入力するときの方法を定義できるようになります。

シェイプされた **Recordset** の列には、Microsoft SQL Server などのデータ プロバイダーからのデータ、他の **Recordset** への参照、 **Recordset** の 1 つの行での計算から導き出される値、 **Recordset** 全体にわたる 1 つの列に対する操作から導き出される値などを含めることができます。また、新規に作成された空の列も含めることができます。

別の**レコード セット**への参照が含まれる列の値を取得するとき、ADO は実際の**レコード セット**は参照によって表される自動的に返します。 別の**レコード セット**が含まれている**レコード セット**は、階層レコード セットと呼ばれます。 階層レコード セットの*親*を含んでいるし、*子*が含まれているレコード セットを*親と子*の関係が発生します。 *章*と呼ばれる子のサブセットへの参照を実際には、**レコード セット**への参照です。 1 つの親は、複数の子**レコード セット**を参照することができません。

Shape コマンド構文によって、シェイプされた **Recordset** をプログラムで作成できます。その後、プログラムから、または適切なビジュアル コントロールによって、 **Recordset** のコンポーネントにアクセスできます。シェイプ コマンドは、他の ADO コマンド テキストと同じように発行されます。

Shape コマンド構文を使用して、階層 **Recordset** オブジェクトを 2 つの方法で作成できます。1 つは、子 **Recordset** を親 **Recordset** に追加する方法です。親と子には、少なくとも 1 つの共通の列が必要です。この共通の列では、親の行の列値と、子のすべての行の列値が同じです。

もう 1 つは、子 **Recordset** から親 **Recordset** を生成する方法です。子 **Recordset** のレコードは通常、BY 句 を使用してグループ化され、1 つの行が、子の各グループの親 **Recordset** に追加されます。BY 句を省略した場合、子 **Recordset** は単一のグループを形成し、親 **Recordset** には 1 つの行が含まれます。これは、子 **Recordset** 全体の "総計" 集計を計算する場合に便利です。

親 **Recordset** は、どのように形成されているかには関係なく、子 **Recordset** への関連付けに使用されるチャプター列が含まれます。必要に応じて、親 **Recordset** は、子の行の集計 (SUM、MIN、MAX など) を含む列を持つことができます。親と子の **Recordset** はいずれも、 **Recordset** の行の式を含む列、および、初期状態が空である新しい列を持つことができます。

階層 **Recordset** オブジェクトは、任意の深さまで入れ子にできます (つまり、子 **Recordset** オブジェクトの子 **Recordset** オブジェクトをさらに作成する操作を繰り返し実行できます)。

シェイプされた **Recordset** の **Recordset** コンポーネントには、プログラムから、または適切なビジュアル コンポーネントによってアクセスできます。

シェイプ コマンドおよびその結果生成される階層の例については、「Using the Data Shaping Service for OLE DB: A Closer Look」 (英語) を参照してください。

このセクションには、次のトピックが含まれています。

- [リシェイプ](reshaping.md)
- [孫の集計](grandchild-aggregates.md)
- [COMPUTE 句の挿入によってパラメーター化されたコマンド](parameterized-commands-with-intervening-compute-commands.md)
- [階層レコード セットを永続化します。](persisting-hierarchical-recordsets.md)
