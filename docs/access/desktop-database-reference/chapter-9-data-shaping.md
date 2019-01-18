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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721555"
---
# <a name="chapter-9-data-shaping"></a>第 9 章: データ シェイプ

**適用されます**Access 2013、Office 2013。

*データ シェイプ*は、データ ソースのクエリを実行し、2 つまたは複数の論理エンティティ (階層) の間の親子リレーションシップを表す[レコード セット](recordset-object-ado.md)を返す方法を提供します。 

階層関係の典型的な例は、顧客と注文です。 データベース内のすべての顧客の 0 個以上の注文が存在することができます。 正規の SQL には、JOIN 構文を使用してデータを取得するための手段が用意されていますが、これは、非効率的で扱いにくいため、指定された親子関係に対して返された各レコード内で冗長な親データが繰り返されます。 データ シェイプと、子**レコード セット**JOIN の冗長性を回避することで複数の子レコードの親**レコード セット**内の 1 つの親レコードを関連付けることができます。 ほとんどの人より自然で、1 つの**レコード セット**の結合モデルよりも操作が容易に親と子・複数の**Recordset**プログラミング モデルを検索します。

データ シェイプの構文には、他の機能もあります。親および子 **Recordset** のフィールドを記述する際に NEW キーワードを使用すると、基になるデータ ソースなしで新しい **Recordset** オブジェクトを作成することができます。この新しい **Recordset** オブジェクトには、データを入力し、永続的に保存することができます。また、開発者は、子フィールドでさまざまな計算や集計 (たとえば、SUM、AVG、および MAX) を実行できます。さらにデータ シェイプでは、子のレコードをグループ化して、親に、子の各グループに対応する 1 つの行を置くことで、子の **Recordset** から親の **Recordset** を作成することもできます。

データ シェイプの詳細については、次のトピックを参照してください。

- [データ シェイプに必要なプロバイダー](required-providers-for-data-shaping.md)
- [Shape COMPUTE 句](shape-compute-clause.md)
- [階層レコードセットの生成](fabricating-hierarchical-recordsets.md)
- [階層レコードセット内の行へのアクセス](accessing-rows-in-a-hierarchical-recordset.md)
- [図形の正式な文法](formal-shape-grammar.md)
- [Visual Basic for Applications の関数](visual-basic-for-applications-functions.md)
- [Shape Append 句 (ADO)](shape-append-clause.md)
- [データ シェイプ (ADO)](data-shaping.md)
- [図形コマンド (ADO) では一般に](shape-commands-in-general.md)

