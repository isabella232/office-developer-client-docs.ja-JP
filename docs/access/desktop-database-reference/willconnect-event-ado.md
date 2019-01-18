---
title: WillConnect イベント (ADO)
TOCTitle: WillConnect event (ADO)
ms:assetid: 8b0e9955-4e7a-7af8-ce6c-7a4ba569a5bb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249611(v=office.15)
ms:contentKeyID: 48546208
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6e62a01d274752b33f7bf3f6f4af6171e7efb16b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703434"
---
# <a name="willconnect-event-ado"></a>WillConnect イベント (ADO)

**適用されます**Access 2013、Office 2013。

**WillConnect** イベントは、接続が開始される前に呼び出されます。

## <a name="syntax"></a>構文

WillConnect*接続文字列*、*ユーザー Id*、*パスワード*、*オプション*、 *adStatus* *pConnection*

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*ConnectionString* |保留中の接続の接続情報が格納された文字列型 ( **String** ) の値です。|
|*UserID* |保留中の接続のユーザー名が格納された文字列型 ( **String** ) の値です。|
|*Password* |保留中の接続のパスワードが格納された文字列型 ( **String** ) の値です。|
|*Options* |プロバイダーが *ConnectionString* を評価する方法を示す長整数型 (**Long**) の値です。オプションは **adAsyncOpen** のみ指定できます。|
|*adStatus* |[EventStatusEnum](eventstatusenum.md)。 このイベントが呼び出されたとき、既定では、このパラメーターは **adStatusOK** に設定されます。 保留中の操作の取り消しをイベントが要求できない場合、このパラメーターは **adStatusCantDeny** に設定されます。<br/><br/>このイベントから制御が戻る前に後続の通知が行われるのを防ぐには、このパラメーターを **adStatusUnwantedEvent** に設定します。この通知の取り消しを実行する接続操作を要求するには、このパラメーターを **adStatusCancel** に設定します。|
|*pConnection* |このイベント通知が適用される [Connection](connection-object-ado.md) オブジェクト。 **WillConnect** イベント ハンドラーで **Connection** のパラメーターが変更されても、 **Connection** には影響はありません。|

## <a name="remarks"></a>解説

**WillConnect** を呼び出したとき、*ConnectionString*、*UserID*、*Password*、および *Options* の各パラメーターの値は、このイベント (保留中の接続) を発生させた操作によって設定され、イベントから制御が戻る前に変更できます。**WillConnect** では、保留中の接続を取り消す要求を返す場合もあります。

このイベントがキャンセルされると、 **ConnectComplete**が**adStatusErrorsOccurred**に設定、 *adStatus*パラメーターで呼び出されます。

