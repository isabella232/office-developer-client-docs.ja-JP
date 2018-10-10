---
title: メソッドをオフするには、ActiveX データ オブジェクト (ADO)
TOCTitle: Clear Method (ADO)
ms:assetid: 5d51f42c-147b-1fcf-d05b-123e5714ecb7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249329(v=office.15)
ms:contentKeyID: 48545110
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1fdaaf7ebccdb88bf3bb098f91fa51b939bb8082
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478287"
---
# <a name="clear-method-ado"></a>Clear メソッド (ADO)


**適用されます**Access 2013 |。Office 2013

**Errors** コレクションからすべての **Error** オブジェクトを削除します。

## <a name="syntax"></a>構文

*エラー*です。クリア

## <a name="remarks"></a>解説

**Errors** コレクションの [Clear](errors-collection-ado.md) メソッドは、コレクションから既存のすべての [Error](error-object-ado.md) オブジェクトを削除する場合に使用します。エラーが発生すると、 **Errors** コレクションは自動的にクリアされ、新しいエラーに基づく **Error** オブジェクトが格納されます。

プロパティとメソッドの中には、 **Errors** コレクションの **Error** オブジェクトとして警告を返しても、プログラムの実行を停止しないものがあります。 [Recordset](resync-method-ado.md) オブジェクトで [Resync](updatebatch-method-ado.md) メソッド、 [UpdateBatch](cancelbatch-method-ado.md) メソッド、または [CancelBatch](recordset-object-ado.md) メソッドを呼び出す前、 [Connection](open-method-ado-connection.md) オブジェクトで [Open](connection-object-ado.md) メソッドを呼び出す前、または [Recordset](filter-property-ado.md) オブジェクトで **Filter** プロパティを設定する前に、 **Errors** コレクションで **Clear** メソッドを呼び出す必要があります。これにより、 [Errors](count-property-ado.md) コレクションの **Count** プロパティを読み取り、返された警告を調べることができます。

