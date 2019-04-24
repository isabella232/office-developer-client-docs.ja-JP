---
title: connectcomplete イベントと Disconnect イベント (ADO)
TOCTitle: ConnectComplete and Disconnect events (ADO)
ms:assetid: 8ecb080b-7fc9-7565-25bd-bd57b983750d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249629(v=office.15)
ms:contentKeyID: 48546293
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e1e1d4487eb113c25e25ce6b9de051e33a4536b3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295990"
---
# <a name="connectcomplete-and-disconnect-events-ado"></a>connectcomplete イベントと Disconnect イベント (ADO)

**適用先:** Access 2013、Office 2013

**connectcomplete**イベントは、接続が*開始*された後に呼び出されます。 **Disconnect**イベントは、接続が*終了*した後に呼び出されます。

## <a name="syntax"></a>構文

connectcomplete** の手順、 *adstatus*、 *pconnection*

*adstatus*、 *pconnection*の切断

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*の場合* |[Error](error-object-ado.md) オブジェクトです。 *adStatus* の値が **adStatusErrorsOccurred** の場合は、発生したエラーを示します。それ以外の場合は設定されません。|
|*adStatus* |[eventstatusenum](eventstatusenum.md)。 **WillConnect** イベントが保留中の接続の取り消しを要求しているときに **ConnectComplete** が呼び出されると、このパラメーターは **adStatusCancel** に設定されます。<br/><br/>いずれかのイベントから制御が戻る前に後続の通知が行われるのを防ぐには、このパラメーターを **adStatusUnwantedEvent** に設定します。ただし、 [Connection](connection-object-ado.md) をいったん閉じてから再び開くと、これらのイベントが再度発生します。|
|*pconnection* |このイベントが適用される **Connection** オブジェクト。|

