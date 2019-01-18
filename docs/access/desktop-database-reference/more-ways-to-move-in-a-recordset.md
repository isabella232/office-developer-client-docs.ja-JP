---
title: レコードセットでのその他の移動方法
TOCTitle: More ways to move in a Recordset
ms:assetid: ae49b20e-0050-c44b-67e9-7e39de5098c4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249822(v=office.15)
ms:contentKeyID: 48547067
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2d10a493aac39934a047c6fa311233fd6c9fac4e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710574"
---
# <a name="more-ways-to-move-in-a-recordset"></a>レコードセットでのその他の移動方法

**適用されます**Access 2013、Office 2013。

**MoveFirst、MoveLast、MoveNext、および MovePrevious** の 4 つのメソッドを使用すると、 [Recordset](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) 内を移動またはスクロールできます (前方スクロール カーソルでは使用できないメソッドもあります)。

**MoveFirst** は、現在のレコードの位置を **Recordset** 内の最初のレコードに変更します。 **MoveLast** は、現在のレコードの位置を **Recordset** 内の最後のレコードに変更します。 **MoveFirst** または **MoveLast** を使用するには、 **Recordset** オブジェクトがブックマークまたは後方スクロール カーソルの移動をサポートしている必要があります。それ以外の場合にメソッドを呼び出すと、エラーが発生します。

**MoveNext** は、現在のレコードの位置を 1 つ進めます。最後のレコードで **MoveNext** を呼び出すと、 **EOF** が **True** に設定されます。 **MovePrevious** は、現在のレコードの位置を 1 つ戻します。最初のレコードで **MovePrevious** を呼び出すと、 **BOF** が **True** に設定されます。次に示すように、これらのメソッドを使用するときには、 **EOF** プロパティと **BOF** プロパティを調べ、 **Recordset** のいずれかの端を超えたときには、カーソルを有効な現在のレコードの位置に戻します。

```vb
. . . 
oRs.MoveNext 
If oRs.EOF Then oRs.MoveLast 
. . . 
```

**MovePrevious** メソッドの場合は、次のようになります。

```vb
. . . 
oRs.MovePrevious 
If oRs.BOF Then oRs.MoveFirst 
. . . 
```

フィルター処理または並べ替えが行われた **Recordset** で現在のレコードのデータを変更すると、その位置も変更されることがあります。 その場合、 **MoveNext** メソッドは正常に動作しますが、その位置が、元の位置からではなく、変更後の位置から 1 つ前に移動されることに注意する必要があります。 たとえば、レコードが並べ替えられた**レコード セット**の末尾に移動するように、現在のレコードのデータを変更することは、 **MoveNext**の呼び出し元が得られる ADO では、**の最後のレコードより後に位置する現在のレコードを設定レコード セット**(**EOF** = **場合は True**)。

**Recordset** オブジェクトのさまざまな Move メソッドの動作は、 **Recordset** 内のデータによってある程度異なります。 **Recordset** に追加された新規レコードは、最初はデータ ソースで定義され、新規レコードのデータに暗黙的または明示的に依存する特定の順序で追加されます。たとえば、 **Recordset** を設定するクエリで並べ替えまたは結合を実行すると、 **Recordset** 内の該当する位置に新規レコードが挿入されます。 **Recordset** の作成時に順序が明示的に指定されていない場合、データ ソースの実装を変更すると、返される行の順序が予期せずに変更されることがあります。さらに、 **Recordset** の並べ替え、フィルター、および編集機能は順序にも影響し、表示されるレコードセットの行にも影響する可能性があります。

したがって、 **MoveNext** 、 **MovePrevious** 、 **MoveFirst** 、 **MoveLast** 、および **Move** の各メソッドはすべて、同じ **Recordset** で行われるその他の操作に影響されることがあります。ADO は明示的に移動されるまで現在の位置を維持しようとしますが、途中で変更すると、その後の移動の結果を考えるのが難しくなります。たとえば、 **MoveFirst** を呼び出して、並べ替えられた **Recordset** の最初の行に移動し、並べ替えの順序を昇順から降順に変更すると、同じ行が表示されていますが、それは **Recordset** の最後の行になっています。 **MoveFirst** を使用すると、別の行 (変更後の最初の行) に移動します。

別の例として、 **Recordset** の途中にある特定の行で、 **Delete** を呼び出してから **MoveNext** を呼び出すと、削除されたレコードのすぐ次のレコードが表示されます。そこで **MovePrevious** を呼び出すと、削除されたレコードは、 **Recordset** のアクティブなメンバーシップとして数えられなくなるため、現在のレコードは、削除したレコードの前のレコードになります。

現在のレコードを基準にして相対的に移動するメソッド (**MovePrevious**、**MoveNext**、および **Move**) について、現在のレコードでデータを変更した場合の移動の形式を、すべてのプロバイダーで一貫して定義するのはたいへん困難です。たとえば、並べ替えおよびフィルター処理が行われた **Recordset** で、現在のレコードがその他のすべてのレコードより前になるようにデータを変更したが、変更したデータがフィルターに一致しなくなった場合、**MoveNext** 操作による移動先は予期できません。レコードの編集、追加、または削除中にデータを変更する場合は、**Recordset** 内を相対的に移動する方が、**MoveFirst** や **MoveLast** を使用して絶対的に移動するよりも危険です。主キーまたは ID は値が変わらないため、並べ替えおよびフィルターは、これらの値に基づいて行ってください。

