---
title: Clear メソッド - ActiveX データ オブジェクト (ADO)
TOCTitle: Clear method (ADO)
ms:assetid: 5d51f42c-147b-1fcf-d05b-123e5714ecb7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249329(v=office.15)
ms:contentKeyID: 48545110
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 893b896df4b3655bb401f1e0446d371017ed0819
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59612352"
---
# <a name="clear-method-ado"></a>Clear メソッド (ADO)


**適用先**: Access 2013、Office 2013

**Errors** コレクションからすべての **Error** オブジェクトを削除します。

## <a name="syntax"></a>構文

*エラー*。クリア

## <a name="remarks"></a>注釈

**Errors** コレクションの [Clear](errors-collection-ado.md) メソッドは、コレクションから既存のすべての [Error](error-object-ado.md) オブジェクトを削除する場合に使用します。エラーが発生すると、 **Errors** コレクションは自動的にクリアされ、新しいエラーに基づく **Error** オブジェクトが格納されます。

プロパティとメソッドの中には、 **Errors** コレクションの **Error** オブジェクトとして警告を返しても、プログラムの実行を停止しないものがあります。 [Recordset](resync-method-ado.md) オブジェクトで [Resync](updatebatch-method-ado.md) メソッド、 [UpdateBatch](cancelbatch-method-ado.md) メソッド、または [CancelBatch](recordset-object-ado.md) メソッドを呼び出す前、 [Connection](open-method-ado-connection.md) オブジェクトで [Open](connection-object-ado.md) メソッドを呼び出す前、または [Recordset](filter-property-ado.md) オブジェクトで **Filter** プロパティを設定する前に、 **Errors** コレクションで **Clear** メソッドを呼び出す必要があります。これにより、 [Errors](count-property-ado.md) コレクションの **Count** プロパティを読み取り、返された警告を調べることができます。

