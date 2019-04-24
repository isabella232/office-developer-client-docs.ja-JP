---
title: 一般的な Shape コマンド
TOCTitle: Shape commands in general
ms:assetid: ad555aa7-bc64-b495-a98d-e927061a5809
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249814(v=office.15)
ms:contentKeyID: 48547039
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 399836158084f07b30b06a9fb099da74527d0cb0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308653"
---
# <a name="shape-commands-in-general"></a>一般的な Shape コマンド

**適用先:** Access 2013、Office 2013

データ シェイプでは、シェイプされる **Recordset** の列、列で表されるエンティティ間の関係、および **Recordset** にデータを設定する方法を定義することができます。

シェイプされる **Recordset** は、以下のような種類の列で構成されます。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>列の種類</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>data</p></td>
<td><p>データ プロバイダー、テーブル、または既にシェイプされている <strong>Recordset</strong> に対してクエリ コマンドが返す <strong>Recordset</strong> のフィールド。</p></td>
</tr>
<tr class="even">
<td><p>チャプター</p></td>
<td><p><em>チャプター</em>と呼ばれる別の<strong>Recordset</strong>への参照。 チャプター列を使用すると、親がチャプター列<strong></strong>を含む<strong>レコードセット</strong>であり、<em>子</em>がチャプターで表される recordset である場合に、<em>親と子</em>のリレーションシップを定義できるようになります。 <em></em></p></td>
</tr>
<tr class="odd">
<td><p>統計</p></td>
<td><p>列の値は、子<strong>Recordset</strong>のすべての行または1つの列に対して<em>集計関数</em>を実行することによって導出されます。 (次のトピック、<a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">集計関数、CALC 関数、および NEW キーワード</a>の集計関数を参照してください)。</p></td>
</tr>
<tr class="even">
<td><p>演算式</p></td>
<td><p>列の値は、<strong>Recordset</strong> の同じ行にある複数の列に対して Visual Basic for Applications の式を実行することで算出されます。式は、CALC 関数への引数です (次のトピック「<a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">集計関数、CALC 関数、および NEW キーワード</a>」および「<a href="visual-basic-for-applications-functions.md">Visual Basic for Applications の関数</a>」の演算式を参照)。</p></td>
</tr>
<tr class="odd">
<td><p>新機能</p></td>
<td><p>後でデータを入力できるように空の状態で作成されるフィールド。この列は、NEW キーワードで定義されます (次のトピック「<a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">集計関数、CALC 関数、および NEW キーワード</a>」の NEW キーワードを参照)。</p></td>
</tr>
</tbody>
</table>


shape コマンドには、 **Recordset** オブジェクトを返す基のデータ プロバイダーに対してクエリ コマンドを指定するための句を含めることができます。クエリの構文は、基になるデータ プロバイダーの要件によって異なります。ADO では特定のクエリ言語を使用する必要はありませんが、通常は Structured Query Language (SQL) を使用します。

SQL の JOIN 句を使用して 2 つのテーブルを関連付けることはできますが、階層 **Recordset** を使用すると、さらに効率的に情報を表すことができます。JOIN で作成された **Recordset** の各行には、1 つのテーブルからの情報が冗長的に繰り返し格納されます。階層 **Recordset** では、複数の子 **Recordset** オブジェクトのそれぞれに対して、ただ 1 つの親 **Recordset** が存在します。

shape コマンドは、 **Recordset** オブジェクトによって、または [Command](commandtext-property-ado.md) オブジェクトの [CommandText](command-object-ado.md) プロパティを設定して [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) メソッドを呼び出すことによって、発行することができます。

shape コマンドはネストできます。つまり、*parent-command* または *child-command* 自体を別の shape コマンドにすることができます。

shape プロバイダーは、ユーザーが **adUseServer** のカーソル位置を指定した場合でも、常にクライアント カーソルを返します。

階層 **Recordset** の移動については、「 [階層 Recordset 内の行にアクセスする](accessing-rows-in-a-hierarchical-recordset.md)」を参照してください。

shape コマンドの厳密な構文については、「[正式な Shape 文法](formal-shape-grammar.md)」を参照してください。

## <a name="see-also"></a>関連項目

- [基になるデータ プロバイダーにコマンドを発行する](issuing-commands-to-the-underlying-data-provider.md)

