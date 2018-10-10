---
title: ActiveX データ オブジェクト (ADO) メソッドを閉じる
TOCTitle: Close Method (ADO)
ms:assetid: 26a7cced-ebeb-70be-f5de-96a35711bc37
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249029(v=office.15)
ms:contentKeyID: 48543818
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6623af069ddbf74dc94fa173160003711779cc8a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477382"
---
# <a name="close-method-ado"></a>Close メソッド (ADO)


**適用されます**Access 2013 |。Office 2013

開いているオブジェクトおよびそれに関連するすべてのオブジェクトを閉じます。

## <a name="syntax"></a>構文

*object*.Close

## <a name="remarks"></a>備考

**Close** メソッドは、 [Connection](connection-object-ado.md) オブジェクト、 [Record](record-object-ado.md) オブジェクト、 [Recordset](recordset-object-ado.md) オブジェクト、または [Stream](stream-object-ado.md) オブジェクトを閉じて、関連するすべてのシステム リソースを解放する場合に使用します。 オブジェクトを閉じてもメモリからは削除されず、プロパティ設定を変更してもう一度開くことができます。 メモリからオブジェクトを完全に排除するには、オブジェクトを閉じた後、オブジェクト変数に*Nothing* (Visual Basic) でを設定します。

**Connection**

**Close** メソッドを使用して **Connection** オブジェクトを閉じると、その接続に関連するアクティブな **Recordset** オブジェクトもすべて閉じます。閉じた [Connection](command-object-ado.md) オブジェクトに関連する **Command** オブジェクトはそのまま維持されますが、 **Connection** オブジェクトとの関連はなくなります。つまり、 [ActiveConnection](activeconnection-property-ado.md) プロパティは **Nothing** に設定されます。また、 **Command** オブジェクトの [Parameters](parameters-collection-ado.md) コレクション内のプロバイダー定義のパラメーターはすべてクリアされます。

後で [Open](open-method-ado-connection.md) メソッドを呼び出して、同じデータ ソースまたは別のデータ ソースへの接続を再度確立することができます。 **Connection** オブジェクトが閉じている間に、データ ソースに対する開いた接続を必要とするメソッドを呼び出すと、エラーが発生します。

接続上に開いた **Recordset** オブジェクトがある状態で **Connection** オブジェクトを閉じると、すべての **Recordset** オブジェクトの保留中の変更がすべてロールバックされます。トランザクションの処理中に **Close** メソッドを呼び出して明示的に **Connection** オブジェクトを閉じると、エラーが発生します。トランザクションの処理中に **Connection** オブジェクトが適用範囲を外れると、トランザクションは自動的にロールバックされます。

**Recordset、Record、および Stream**

**Close** メソッドを使用して **Recordset** オブジェクト、 **Record** オブジェクト、または **Stream** オブジェクトを閉じると、関連するデータ、およびデータに対するそのオブジェクトからの排他アクセスが、すべて解放されます。後で [Open](open-method-ado-recordset.md) メソッドを呼び出し、同じ属性で、または属性を変更して、オブジェクトを再度開くことができます。

**Recordset** オブジェクトが閉じている間に、有効なカーソルを必要とするメソッドを呼び出すと、エラーが発生します。

即時更新モードで編集を行っているときに **Close** メソッドを呼び出すと、エラーが発生します。 [Update](update-method-ado.md) メソッドまたは [CancelUpdate](cancelupdate-method-ado.md) メソッドを先に呼び出す必要があります。バッチ更新モードの実行中に **Recordset** オブジェクトを閉じると、最後に [UpdateBatch](updatebatch-method-ado.md) を呼び出した後で行われた変更がすべて失われます。

[Clone](clone-method-ado.md) メソッドを使用して、開いている **Recordset** オブジェクトの複製を作成した場合、元のオブジェクトまたはいずれかの複製を閉じても、他の複製には影響しません。

