---
title: InfoMessage イベント (ADO)
TOCTitle: InfoMessage event (ADO)
ms:assetid: 5d4f487f-96c8-4cf6-60ab-583510d3096f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249328(v=office.15)
ms:contentKeyID: 48545109
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 3a629511b87a182d659cba74de537edd15d27b5d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631966"
---
# <a name="infomessage-event-ado"></a>InfoMessage イベント (ADO)

**適用先**: Access 2013、Office 2013

**InfoMessage** イベントは、**ConnectionEvent** 操作時に警告が発生するたびに呼び出されます。

## <a name="syntax"></a>構文

InfoMessage *pError*、 *adStatus*、 *pConnection*

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*pError* |[Error](error-object-ado.md) オブジェクトです。このパラメーターには、返されたすべてのエラーが格納されます。複数のエラーが返される場合、 **Errors** コレクションを列挙してエラーを確認してください。|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). このイベントから制御が戻る前に後続の通知が行われるのを防ぐには、このパラメーターを **adStatusUnwantedEvent** に設定します。|
|*pConnection* |[Connection](connection-object-ado.md) オブジェクトです。警告が発生した接続です。たとえば、 **Connection** オブジェクトを開いたり、 [Connection](command-object-ado.md) で **Command** コマンドを実行したときに、警告が発生する可能性があります。|

