---
title: ExecuteComplete イベント (ADO)
TOCTitle: ExecuteComplete Event (ADO)
ms:assetid: 47317d97-e373-32f4-9438-2dff46b8d367
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249219(v=office.15)
ms:contentKeyID: 48544589
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 231cfcf42cead3074996870971488dadb60583ae
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/17/2018
ms.locfileid: "25605423"
---
# <a name="executecomplete-event-ado"></a>ExecuteComplete イベント (ADO)


**適用されます**Access 2013 |。Office 2013



**ExecuteComplete** イベントは、コマンドが実行を終了した後に呼び出されます。

## <a name="syntax"></a>構文

ExecuteComplete*RecordsAffected*、 *pError*、 *adStatus*、 *pCommand*、 *pRecordset*、 *pConnection*

## <a name="parameters"></a>パラメーター

  - *RecordsAffected*

  - コマンドによって影響を受けるレコードの数を表す長整数型 ( **Long** ) の値です。

  - *pError*

  - [Error](error-object-ado.md) オブジェクトです。 **adStatus** の値が **adStatusErrorsOccurred** の場合は、発生したエラーを示します。それ以外の場合は設定されません。

  - *adStatus*

  - [EventStatusEnum](eventstatusenum.md)
    
    このイベントから制御が戻る前に後続の通知が行われるのを防ぐには、このパラメーターを **adStatusUnwantedEvent** に設定します。

  - *pCommand*

  - 実行された [Command](command-object-ado.md) オブジェクトです。明示的に **Command** を作成せずに **Connection.Execute** または **Recordset.Open** を呼び出しても **Command** オブジェクトが格納されます (この場合、 **Command** オブジェクトは ADO によって内部的に作成されます)。

  - *pRecordset*

  - 実行されたコマンドの結果の [Recordset](recordset-object-ado.md) オブジェクトです。この **Recordset** は空の場合もあります。この Recordset オブジェクトは、このイベント ハンドラーから破棄しないでください。破棄した場合には、ADO が存在しないオブジェクトにアクセスしようとしたときにアクセス違反が発生します。

  - *pConnection*

  - [Connection](connection-object-ado.md) オブジェクトです。操作を実行したときの接続です。

## <a name="remarks"></a>解説

<<<<<<< ヘッドのために**ExecuteComplete**イベントが発生する可能性があります、**接続します**。[実行](https://msdn.microsoft.com/library/jj249832\(v=office.15\))するには、**コマンドです**。[実行](https://msdn.microsoft.com/library/jj248785\(v=office.15\))するには、**レコード セット**。[開く](open-method-ado-recordset.md)、**レコード セット**。[クエリを再実行](requery-method-ado.md)、または**レコード セット**。[NextRecordset](nextrecordset-method-ado.md)メソッドです。
=== 理由のため、 **ExecuteComplete**イベントが発生する可能性があります、**接続します**。[実行](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection)するには、**コマンドです**。[実行](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command)するには、**レコード セット**。[開く](open-method-ado-recordset.md)、**レコード セット**。[クエリを再実行](requery-method-ado.md)、または**レコード セット**。[NextRecordset](nextrecordset-method-ado.md)メソッドです。
>>>>>>> master

