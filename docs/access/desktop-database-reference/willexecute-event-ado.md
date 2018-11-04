---
title: WillExecute イベント (ADO)
TOCTitle: WillExecute event (ADO)
ms:assetid: 9f516bfd-246d-9817-4ca3-64598ab466f7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249732(v=office.15)
ms:contentKeyID: 48546686
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2ea43f565199f346287abf8fd134dec494d37cf5
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949972"
---
# <a name="willexecute-event-ado"></a>WillExecute イベント (ADO)

**適用されます**Access 2013、Office 2013。

**WillExecute** イベントは、保留中のコマンドが接続に対して実行される直前に呼び出されます。

## <a name="syntax"></a>構文

アクティビ ティー*ソース*、 *CursorType*、 *LockType*、*オプション*、 *adStatus*、 *pCommand*、 *pRecordset*、 *pConnection*

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*Source* |SQL コマンドまたはストアド プロシージャ名が格納された文字列型 ( **String** ) の値です。|
|*カーソル。* |開く対象の [Recordset](cursortypeenum.md) のカーソルの種類が格納された **CursorTypeEnum** です。 このパラメーターを使用、**レコード セット**を[開く](open-method-ado-recordset.md)操作中にカーソルを任意の種類に変更できます。 *CursorType*は、他の操作の無視されます。|
|*ロック。* |開く対象の [Recordset](locktypeenum.md) のロックの種類が格納された **LockTypeEnum** です。 このパラメーターを使用すると、 **Recordset** の **Open** 操作中にロックを任意の種類に変更できます。 *LockType*は、他のすべての操作に対しては無視されます。|
|*Options* |コマンドを実行するとき、または **Recordset** を開くときに使われるオプションを示す長整数型 ( **Long** ) の値です。|
|*adStatus* |[EventStatusEnum](eventstatusenum.md)。 このイベントから制御が戻る前に後続の通知が行われるのを防ぐには、このパラメーターを **adStatusUnwantedEvent** に設定し、このイベントを発生させた操作の取り消しを要求するには、このパラメーターを **adStatusCancel** に設定します。|
|*pCommand* |このイベント通知が適用される [Command](command-object-ado.md) オブジェクトです。|
|*pRecordset* |このイベント通知が適用される [Recordset](recordset-object-ado.md) オブジェクトです。|
|*pConnection* |このイベント通知が適用される [Connection](connection-object-ado.md) オブジェクトです。|

## <a name="remarks"></a>解説

**アクティビ ティー**イベント発生の理由のため、**接続します**。[実行](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection)するには、**コマンドです**。[実行](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command)、または**レコード セット**。[Open](open-method-ado-recordset.md)メソッド*pConnection*パラメーターは、有効なオブジェクトへの参照、**接続**を常に含む必要があります。 **Connection.Execute**のためのイベントの場合、 *pRecordset*と*pCommand*パラメーターが**Nothing**に設定します。 **Recordset.Open**のためのイベントの場合は、 *pRecordset*パラメーターが**レコード セット**オブジェクトを参照し、 *pCommand*パラメーターは**Nothing**に設定します。 **Command.Execute**のためのイベントの場合は、 *pCommand*パラメーターは、**コマンド**オブジェクトを参照し、 *pRecordset*パラメーターは**Nothing**に設定します。

**WillExecute** では、保留中の実行パラメーターを調べたり、編集したりできます。このイベントは、保留中のコマンドを取り消す要求を返すこともあります。

