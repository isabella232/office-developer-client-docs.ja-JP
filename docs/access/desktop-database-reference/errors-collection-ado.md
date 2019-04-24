---
title: Errors コレクション (ADO)
TOCTitle: Errors collection (ADO)
ms:assetid: 76c234b8-7fec-11c5-275e-864d5d880ee7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249486(v=office.15)
ms:contentKeyID: 48545706
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: db9fa4fccc4f3d13849f34c157f2ea07cc3f171d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293428"
---
# <a name="errors-collection-ado"></a>Errors コレクション (ADO)


**適用先:** Access 2013、Office 2013

プロバイダー関連の 1 つのエラーに対応して発生するすべての [Error](error-object-ado.md) オブジェクトを格納します。

## <a name="remarks"></a>注釈

ADO オブジェクトに関係するすべての操作では、1 つ以上のプロバイダー エラーが発生する場合があります。エラーが発生するたびに、1 つ以上の **Error** オブジェクトが **Connection** オブジェクトの [Errors](connection-object-ado.md) コレクションに追加される可能性があります。別の ADO 操作でエラーが発生すると、 **Errors** コレクションがクリアされ、 **Error** オブジェクトの新しいセットが **Errors** コレクションに配置される可能性があります。

各 **Error** オブジェクトは、ADO エラーではなく特定のプロバイダー エラーを表します。ADO エラーは、実行時の例外処理メカニズムに公開されます。たとえば、Microsoft Visual Basic の場合、ADO 固有のエラーが発生すると、 [onError](onerror-event-rds.md) イベントが実行され、そのエラーが **Err** オブジェクトに追加されます。

エラーが発生しない ADO 操作は、 **Errors** コレクションには影響を与えません。 [Errors](clear-method-ado.md) コレクションを手動でクリアするには、 **Clear** メソッドを使用します。

**Errors** コレクション内の **Error** オブジェクトのセットは、1 つのステートメントに対応して発生するすべてのエラーを記述します。 **Errors** コレクションの特定のエラーを列挙すると、エラー処理ルーチンでは、エラーの原因と発生源をより正確に特定し、適切な回復手順を実行できます。

プロパティとメソッドの中には、 **Errors** コレクションの **Error** オブジェクトとして警告を返しても、プログラムの実行を停止しないものがあります。 [Recordset](resync-method-ado.md) オブジェクトで [Resync](updatebatch-method-ado.md) メソッド、 [UpdateBatch](cancelbatch-method-ado.md) メソッド、または [CancelBatch](recordset-object-ado.md) メソッドを呼び出す前、 [Connection](open-method-ado-connection.md) オブジェクトで **Open** メソッドを呼び出す前、または [Recordset](filter-property-ado.md) オブジェクトで **Filter** プロパティを設定する前に、 **Errors** コレクションで **Clear** メソッドを呼び出す必要があります。これにより、 [Errors](count-property-ado.md) コレクションの **Count** プロパティを読み取り、返された警告を調べることができます。


> [!NOTE]
> [!メモ] 1 つの ADO 操作で複数のエラーが発生する場合の詳細については、 **Error** オブジェクトのトピックを参照してください。


