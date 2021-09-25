---
title: ExecuteComplete イベント (ADO)
TOCTitle: ExecuteComplete event (ADO)
ms:assetid: 47317d97-e373-32f4-9438-2dff46b8d367
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249219(v=office.15)
ms:contentKeyID: 48544589
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: f451d61b228d85abb16f5d5e08e0fdd40b1c2d55
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59597346"
---
# <a name="executecomplete-event-ado"></a>ExecuteComplete イベント (ADO)

**適用先**: Access 2013、Office 2013

**ExecuteComplete** イベントは、コマンドが実行を終了した後に呼び出されます。

## <a name="syntax"></a>構文

ExecuteComplete *RecordsAffected*, *pError*, *adStatus*, *pCommand*, *pRecordset*, *pConnection*

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*RecordsAffected* |コマンドによって影響を受けるレコードの数を表す長整数型 ( **Long** ) の値です。|
|*pError* |[Error](error-object-ado.md) オブジェクトです。 **adStatus** の値が **adStatusErrorsOccurred** の場合は、発生したエラーを示します。それ以外の場合は設定されません。|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). このイベントから制御が戻る前に後続の通知が行われるのを防ぐには、このパラメーターを **adStatusUnwantedEvent** に設定します。|
|*pCommand* |実行された [Command](command-object-ado.md) オブジェクトです。明示的に **Command** を作成せずに **Connection.Execute** または **Recordset.Open** を呼び出しても **Command** オブジェクトが格納されます (この場合、 **Command** オブジェクトは ADO によって内部的に作成されます)。|
|*pRecordset* |実行されたコマンドの結果の [Recordset](recordset-object-ado.md) オブジェクトです。この **Recordset** は空の場合もあります。この Recordset オブジェクトは、このイベント ハンドラーから破棄しないでください。破棄した場合には、ADO が存在しないオブジェクトにアクセスしようとしたときにアクセス違反が発生します。|
|*pConnection* |[Connection](connection-object-ado.md) オブジェクトです。操作を実行したときの接続です。|

## <a name="remarks"></a>注釈

**ExecuteComplete** イベントは、**Connection.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection)、**Command.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command)、**Recordset.**[Open](open-method-ado-recordset.md)、**Recordset.**[Requery](requery-method-ado.md)、または **Recordset.**[NextRecordset](nextrecordset-method-ado.md) の各メソッドにより発生します。

