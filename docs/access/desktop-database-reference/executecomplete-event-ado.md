---
title: ExecuteComplete イベント (ADO)
TOCTitle: ExecuteComplete event (ADO)
ms:assetid: 47317d97-e373-32f4-9438-2dff46b8d367
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249219(v=office.15)
ms:contentKeyID: 48544589
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8a094968e70ace5e6cba1df184bf0ba57c2d7789
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293225"
---
# <a name="executecomplete-event-ado"></a>ExecuteComplete イベント (ADO)

**適用先:** Access 2013、Office 2013

**ExecuteComplete** イベントは、コマンドが実行を終了した後に呼び出されます。

## <a name="syntax"></a>構文

ExecuteComplete*RecordsAffected*、 **、 *adstatus*、 *pcommand*、 *pcommand*、 *pcommand*

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*RecordsAffected* |コマンドによって影響を受けるレコードの数を表す長整数型 ( **Long** ) の値です。|
|*の場合* |[Error](error-object-ado.md) オブジェクトです。 **adStatus** の値が **adStatusErrorsOccurred** の場合は、発生したエラーを示します。それ以外の場合は設定されません。|
|*adStatus* |[eventstatusenum](eventstatusenum.md)。 このイベントから制御が戻る前に後続の通知が行われるのを防ぐには、このパラメーターを **adStatusUnwantedEvent** に設定します。|
|*ある* |実行された [Command](command-object-ado.md) オブジェクトです。明示的に **Command** を作成せずに **Connection.Execute** または **Recordset.Open** を呼び出しても **Command** オブジェクトが格納されます (この場合、 **Command** オブジェクトは ADO によって内部的に作成されます)。|
|*precordset* |実行されたコマンドの結果の [Recordset](recordset-object-ado.md) オブジェクトです。この **Recordset** は空の場合もあります。この Recordset オブジェクトは、このイベント ハンドラーから破棄しないでください。破棄した場合には、ADO が存在しないオブジェクトにアクセスしようとしたときにアクセス違反が発生します。|
|*pconnection* |[Connection](connection-object-ado.md) オブジェクトです。操作を実行したときの接続です。|

## <a name="remarks"></a>注釈

**ExecuteComplete** イベントは、**Connection.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection)、**Command.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command)、**Recordset.**[Open](open-method-ado-recordset.md)、**Recordset.**[Requery](requery-method-ado.md)、または **Recordset.**[NextRecordset](nextrecordset-method-ado.md) の各メソッドにより発生します。

