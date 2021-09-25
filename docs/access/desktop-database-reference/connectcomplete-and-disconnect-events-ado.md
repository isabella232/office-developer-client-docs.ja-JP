---
title: ConnectComplete イベントと Disconnect イベント (ADO)
TOCTitle: ConnectComplete and Disconnect events (ADO)
ms:assetid: 8ecb080b-7fc9-7565-25bd-bd57b983750d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249629(v=office.15)
ms:contentKeyID: 48546293
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: d46da971ed9cb59c83b91fbb12e2588c40685f47
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602830"
---
# <a name="connectcomplete-and-disconnect-events-ado"></a>ConnectComplete イベントと Disconnect イベント (ADO)

**適用先**: Access 2013、Office 2013

**ConnectComplete イベントは**、接続の開始後に呼び出 *されます*。 Disconnect **イベントは** 、接続が終了した後に呼び *出されます*。

## <a name="syntax"></a>構文

ConnectComplete *pError*, *adStatus*, *pConnection*

*adStatus* *、pConnection を切断する*

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*pError* |[Error](error-object-ado.md) オブジェクトです。 *adStatus* の値が **adStatusErrorsOccurred** の場合は、発生したエラーを示します。それ以外の場合は設定されません。|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). **WillConnect** イベントが保留中の接続の取り消しを要求しているときに **ConnectComplete** が呼び出されると、このパラメーターは **adStatusCancel** に設定されます。<br/><br/>いずれかのイベントから制御が戻る前に後続の通知が行われるのを防ぐには、このパラメーターを **adStatusUnwantedEvent** に設定します。ただし、 [Connection](connection-object-ado.md) をいったん閉じてから再び開くと、これらのイベントが再度発生します。|
|*pConnection* |このイベントが適用される **Connection** オブジェクト。|

