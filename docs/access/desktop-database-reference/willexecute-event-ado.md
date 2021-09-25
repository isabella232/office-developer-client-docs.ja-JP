---
title: WillExecute イベント (ADO)
TOCTitle: WillExecute event (ADO)
ms:assetid: 9f516bfd-246d-9817-4ca3-64598ab466f7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249732(v=office.15)
ms:contentKeyID: 48546686
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 4d911b46800c0b7b9a45b3697088a4c29c86ec3d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59585047"
---
# <a name="willexecute-event-ado"></a>WillExecute イベント (ADO)

**適用先:** Access 2013、Office 2013

**WillExecute** イベントは、保留中のコマンドが接続に対して実行される直前に呼び出されます。

## <a name="syntax"></a>構文

WillExecute *Source*, *CursorType*, *LockType*, *Options*, *adStatus*, *pCommand*, *pRecordset*, *pConnection*

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*Source* |SQL コマンドまたはストアド プロシージャ名が格納された文字列型 ( **String** ) の値です。|
|*CursorType* |開く対象の [Recordset](cursortypeenum.md) のカーソルの種類が格納された **CursorTypeEnum** です。 このパラメーターを使用すると、Recordset Open 操作中にカーソルを任意の **種類に**[変更](open-method-ado-recordset.md)できます。 *CursorType* は、他の操作には無効です。|
|*LockType* |開く対象の [Recordset](locktypeenum.md) のロックの種類が格納された **LockTypeEnum** です。 このパラメーターを使用すると、 **Recordset** の **Open** 操作中にロックを任意の種類に変更できます。 *LockType* は、他の操作には無効です。|
|*Options* |コマンドを実行するとき、または **Recordset** を開くときに使われるオプションを示す長整数型 ( **Long** ) の値です。|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). このイベントから制御が戻る前に後続の通知が行われるのを防ぐには、このパラメーターを **adStatusUnwantedEvent** に設定し、このイベントを発生させた操作の取り消しを要求するには、このパラメーターを **adStatusCancel** に設定します。|
|*pCommand* |このイベント通知が適用される [Command](command-object-ado.md) オブジェクトです。|
|*pRecordset* |このイベント通知が適用される [Recordset](recordset-object-ado.md) オブジェクトです。|
|*pConnection* |このイベント通知が適用される [Connection](connection-object-ado.md) オブジェクトです。|

## <a name="remarks"></a>注釈

**WillExecute** イベントは、**Connection.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) メソッド、**Command.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) メソッド、または **Recordset.**[Open](open-method-ado-recordset.md) メソッドによって発生します。*pConnection* パラメーターには、常に **Connection** オブジェクトに対する有効な参照が格納されます。イベントの原因が **Connection.Execute** の場合、*pRecordset* パラメーターと *pCommand* パラメーターは **Nothing** に設定されます。イベントの原因が **Recordset.Open** の場合、*pRecordset* パラメーターは **Recordset** オブジェクトを参照し、*pCommand* パラメーターは **Nothing** に設定されます。イベントの原因が **Command.Execute** の場合、*pCommand* パラメーターは **Command** オブジェクトを参照し、*pRecordset* パラメーターは **Nothing** に設定されます。

**WillExecute** では、保留中の実行パラメーターを調べたり、編集したりできます。このイベントは、保留中のコマンドを取り消す要求を返すこともあります。

