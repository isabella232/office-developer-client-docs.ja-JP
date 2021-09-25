---
title: FetchComplete イベント (ADO)
TOCTitle: FetchComplete event (ADO)
ms:assetid: 4863d5b5-7d77-bdef-c511-f85c9e6dec9d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249224(v=office.15)
ms:contentKeyID: 48544621
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: f8c5d775610270ffe2b31a352ac595d5f86008a3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59558367"
---
# <a name="fetchcomplete-event-ado"></a>FetchComplete イベント (ADO)

**適用先:** Access 2013、Office 2013

**FetchComplete** イベントは、長い非同期操作ですべてのレコードが [Recordset](recordset-object-ado.md) に取得された後に呼び出されます。

## <a name="syntax"></a>構文

FetchComplete *pError*, *adStatus*, *pRecordset*

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*pError* |[Error](error-object-ado.md) オブジェクトです。 **adStatus** の値が **adStatusErrorsOccurred** の場合は、発生したエラーを示します。それ以外の場合は設定されません。|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). このイベントから制御が戻る前に後続の通知が行われるのを防ぐには、このパラメーターを **adStatusUnwantedEvent** に設定します。|
|*pRecordset* |**Recordset** オブジェクト。レコードを取得したオブジェクトです。|

## <a name="remarks"></a>注釈

Microsoft Visual Basic で **FetchComplete** を使用するには、Visual Basic 6.0 以降が必要です。

