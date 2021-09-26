---
title: '第 9 章: データ シェイプ'
TOCTitle: 'Chapter 9: Data shaping'
ms:assetid: f66a319f-1b3d-c4a3-50b3-af1a47540832
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250253(v=office.15)
ms:contentKeyID: 48548739
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 31016a76c68e6cddd58dd1e876f52ca298374890
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59622516"
---
# <a name="chapter-9-data-shaping"></a>第 9 章: データ シェイプ

**適用先**: Access 2013、Office 2013

*データ シェーピング* は、データ ソースを照会し、2 つ以上の論理エンティティ (階層) 間の親子関係を表す [Recordset](recordset-object-ado.md) を返す方法を提供します。 

A classic example of a hierarchical relationship is customers and orders. For every customer in a database, there can be zero or more orders. Regular SQL provides a means of retrieving the data using JOIN syntax, but this can be inefficient and unwieldy because redundant parent data is repeated in each record returned for a given parent-child relationship. Data shaping can relate a single parent record in the parent **Recordset** to multiple child records in the child **Recordset**, avoiding the redundancy of a JOIN. Most people find the parent-child multiple **Recordset** programming model more natural and easier to work with than the single **Recordset** JOIN model.

データ シェイプの構文には、他の機能もあります。親および子 **Recordset** のフィールドを記述する際に NEW キーワードを使用すると、基になるデータ ソースなしで新しい **Recordset** オブジェクトを作成することができます。この新しい **Recordset** オブジェクトには、データを入力し、永続的に保存することができます。また、開発者は、子フィールドでさまざまな計算や集計 (たとえば、SUM、AVG、および MAX) を実行できます。さらにデータ シェイプでは、子のレコードをグループ化して、親に、子の各グループに対応する 1 つの行を置くことで、子の **Recordset** から親の **Recordset** を作成することもできます。

データ シェイプの詳細については、次のトピックを参照してください。

- [データ シェイプに必要なプロバイダー](required-providers-for-data-shaping.md)
- [Shape COMPUTE 句](shape-compute-clause.md)
- [階層レコードセットの生成](fabricating-hierarchical-recordsets.md)
- [階層レコードセット内の行へのアクセス](accessing-rows-in-a-hierarchical-recordset.md)
- [正式な Shape 文法](formal-shape-grammar.md)
- [Visual Basic for Applications の関数](visual-basic-for-applications-functions.md)
- [Shape Append 句 (ADO)](shape-append-clause.md)
- [データ シェーピング (ADO)](data-shaping.md)
- [Shape コマンド全般 (ADO)](shape-commands-in-general.md)

