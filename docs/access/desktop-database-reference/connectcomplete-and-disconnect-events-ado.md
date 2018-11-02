---
title: ConnectComplete イベントと Disconnect イベント (ADO)
TOCTitle: ConnectComplete and Disconnect events (ADO)
ms:assetid: 8ecb080b-7fc9-7565-25bd-bd57b983750d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249629(v=office.15)
ms:contentKeyID: 48546293
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3ab98e270fd52d656bf722c7f666afbe22d5ea44
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926305"
---
# <a name="connectcomplete-and-disconnect-events-ado"></a>ConnectComplete イベントと Disconnect イベント (ADO)


**適用されます**Access 2013、Office 2013。

**ConnectComplete**イベントは、接続が*開始*した後に呼び出されます。 **切断**イベントは、接続が*終了*した後に呼び出されます。

## <a name="syntax"></a>構文

ConnectComplete*pError*、 *adStatus*、 *pConnection*

*AdStatus*、 *pConnection*を切断します。

## <a name="parameters"></a>パラメーター

  - *pError*

  - [Error](error-object-ado.md) オブジェクトです。 *adStatus* の値が **adStatusErrorsOccurred** の場合は、発生したエラーを示します。それ以外の場合は設定されません。

  - *adStatus*

  - [EventStatusEnum](eventstatusenum.md)
    
    **WillConnect** イベントが保留中の接続の取り消しを要求しているときに **ConnectComplete** が呼び出されると、このパラメーターは **adStatusCancel** に設定されます。
    
    いずれかのイベントから制御が戻る前に後続の通知が行われるのを防ぐには、このパラメーターを **adStatusUnwantedEvent** に設定します。ただし、 [Connection](connection-object-ado.md) をいったん閉じてから再び開くと、これらのイベントが再度発生します。

  - *pConnection*

  - このイベントが適用される **Connection** オブジェクト。

