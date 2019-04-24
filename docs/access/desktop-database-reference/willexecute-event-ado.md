---
title: イベントを実行するイベント (ADO)
TOCTitle: WillExecute event (ADO)
ms:assetid: 9f516bfd-246d-9817-4ca3-64598ab466f7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249732(v=office.15)
ms:contentKeyID: 48546686
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7fe15604d0160afcbde5fdf02eaa6a7831da874b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302758"
---
# <a name="willexecute-event-ado"></a>イベントを実行するイベント (ADO)

**適用先:** Access 2013、Office 2013

**WillExecute** イベントは、保留中のコマンドが接続に対して実行される直前に呼び出されます。

## <a name="syntax"></a>構文

*Source*、 *CursorType*、 *LockType*、 *Options*、 *adstatus*、 *pcommand*、 *pcommand*、 *pcommand*を実行します。

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*Source* |SQL コマンドまたはストアド プロシージャ名が格納された文字列型 ( **String** ) の値です。|
|*CursorType* |開く対象の [Recordset](cursortypeenum.md) のカーソルの種類が格納された **CursorTypeEnum** です。 このパラメーターを使用すると、 **Recordset**の[開い](open-method-ado-recordset.md)ている操作中にカーソルを任意の種類に変更できます。 *CursorType* は、他の操作には無効です。|
|*LockType* |開く対象の [Recordset](locktypeenum.md) のロックの種類が格納された **LockTypeEnum** です。 このパラメーターを使用すると、 **Recordset** の **Open** 操作中にロックを任意の種類に変更できます。 *LockType* は、他の操作には無効です。|
|*Options* |コマンドを実行するとき、または **Recordset** を開くときに使われるオプションを示す長整数型 ( **Long** ) の値です。|
|*adStatus* |[eventstatusenum](eventstatusenum.md)。 このイベントから制御が戻る前に後続の通知が行われるのを防ぐには、このパラメーターを **adStatusUnwantedEvent** に設定し、このイベントを発生させた操作の取り消しを要求するには、このパラメーターを **adStatusCancel** に設定します。|
|*ある* |このイベント通知が適用される [Command](command-object-ado.md) オブジェクトです。|
|*precordset* |このイベント通知が適用される [Recordset](recordset-object-ado.md) オブジェクトです。|
|*pconnection* |このイベント通知が適用される [Connection](connection-object-ado.md) オブジェクトです。|

## <a name="remarks"></a>注釈

**WillExecute** イベントは、**Connection.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) メソッド、**Command.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) メソッド、または **Recordset.**[Open](open-method-ado-recordset.md) メソッドによって発生します。*pConnection* パラメーターには、常に **Connection** オブジェクトに対する有効な参照が格納されます。イベントの原因が **Connection.Execute** の場合、*pRecordset* パラメーターと *pCommand* パラメーターは **Nothing** に設定されます。イベントの原因が **Recordset.Open** の場合、*pRecordset* パラメーターは **Recordset** オブジェクトを参照し、*pCommand* パラメーターは **Nothing** に設定されます。イベントの原因が **Command.Execute** の場合、*pCommand* パラメーターは **Command** オブジェクトを参照し、*pRecordset* パラメーターは **Nothing** に設定されます。

**WillExecute** では、保留中の実行パラメーターを調べたり、編集したりできます。このイベントは、保留中のコマンドを取り消す要求を返すこともあります。

