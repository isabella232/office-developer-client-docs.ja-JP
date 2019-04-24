---
title: infomessage イベント (ADO)
TOCTitle: InfoMessage event (ADO)
ms:assetid: 5d4f487f-96c8-4cf6-60ab-583510d3096f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249328(v=office.15)
ms:contentKeyID: 48545109
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 879d8e7b3733937687671a164f86dbb273cf7533
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291443"
---
# <a name="infomessage-event-ado"></a>infomessage イベント (ADO)

**適用先:** Access 2013、Office 2013

**InfoMessage** イベントは、**ConnectionEvent** 操作時に警告が発生するたびに呼び出されます。

## <a name="syntax"></a>構文

infomessage** のメッセージの設定、 *adstatus*、 *pconnection*

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*の場合* |[Error](error-object-ado.md) オブジェクトです。このパラメーターには、返されたすべてのエラーが格納されます。複数のエラーが返される場合、 **Errors** コレクションを列挙してエラーを確認してください。|
|*adStatus* |[eventstatusenum](eventstatusenum.md)。 このイベントから制御が戻る前に後続の通知が行われるのを防ぐには、このパラメーターを **adStatusUnwantedEvent** に設定します。|
|*pconnection* |[Connection](connection-object-ado.md) オブジェクトです。警告が発生した接続です。たとえば、 **Connection** オブジェクトを開いたり、 [Connection](command-object-ado.md) で **Command** コマンドを実行したときに、警告が発生する可能性があります。|

