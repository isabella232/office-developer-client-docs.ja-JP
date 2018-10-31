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
# <a name="chapter-9-data-shaping"></a>第 9 章: データ シェイプ


**適用されます**Access 2013 |。Office 2013

*データ シェイプ*は、データ ソースのクエリを実行し、2 つまたは複数の論理エンティティ (階層) の間の親子リレーションシップを表す[レコード セット](recordset-object-ado.md)を返す方法を提供します。 階層関係の典型的な例は、顧客と注文です。 データベース内のすべての顧客の 0 個以上の注文が存在することができます。 正規の SQL には、JOIN 構文を使用してデータを取得するための手段が用意されていますが、これは、非効率的で扱いにくいため、指定された親子関係に対して返された各レコード内で冗長な親データが繰り返されます。 データ シェイプと、子**レコード セット**JOIN の冗長性を回避することで複数の子レコードの親**レコード セット**内の 1 つの親レコードを関連付けることができます。 ほとんどの人より自然で、1 つの**レコード セット**の結合モデルよりも操作が容易に親と子・複数の**Recordset**プログラミング モデルを検索します。

データ シェイプの構文には、他の機能もあります。親および子 **Recordset** のフィールドを記述する際に NEW キーワードを使用すると、基になるデータ ソースなしで新しい **Recordset** オブジェクトを作成することができます。この新しい **Recordset** オブジェクトには、データを入力し、永続的に保存することができます。また、開発者は、子フィールドでさまざまな計算や集計 (たとえば、SUM、AVG、および MAX) を実行できます。さらにデータ シェイプでは、子のレコードをグループ化して、親に、子の各グループに対応する 1 つの行を置くことで、子の **Recordset** から親の **Recordset** を作成することもできます。

データ シェイプの詳細については、次のトピックを参照してください。

- [データ シェイプに必要なプロバイダー](required-providers-for-data-shaping.md)

- [Shape Compute 句](shape-compute-clause.md)

- [階層レコードセットを作成する](fabricating-hierarchical-recordsets.md)

- [階層 Recordset 内の行にアクセスする](accessing-rows-in-a-hierarchical-recordset.md)

- [正式な Shape 文法](formal-shape-grammar.md)

- [Visual Basic for Applications の関数](visual-basic-for-applications-functions.md)

- [Shape Append 句 (ADO)](shape-append-clause.md)

- [データ シェイプ (ADO)](data-shaping.md)

- [一般的な Shape コマンド (ADO)](shape-commands-in-general.md)

