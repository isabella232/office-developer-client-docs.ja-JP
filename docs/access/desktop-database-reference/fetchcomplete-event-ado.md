---
title: FetchComplete イベント (ADO)
TOCTitle: FetchComplete event (ADO)
ms:assetid: 4863d5b5-7d77-bdef-c511-f85c9e6dec9d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249224(v=office.15)
ms:contentKeyID: 48544621
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: edb2eefd36aea9f037ea4ad6afc51e0da18b76db
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945636"
---
# <a name="fetchcomplete-event-ado"></a>FetchComplete イベント (ADO)


**適用されます**Access 2013、Office 2013。


**FetchComplete** イベントは、長い非同期操作ですべてのレコードが [Recordset](recordset-object-ado.md) に取得された後に呼び出されます。

## <a name="syntax"></a>構文

FetchComplete*pError*、 *adStatus*、 *pRecordset*

## <a name="parameters"></a>パラメーター

- *pError*

  - [Error](error-object-ado.md) オブジェクトです。 **adStatus** の値が **adStatusErrorsOccurred** の場合は、発生したエラーを示します。それ以外の場合は設定されません。

- *adStatus*

  - [EventStatusEnum](eventstatusenum.md)
    
    このイベントから制御が戻る前に後続の通知が行われるのを防ぐには、このパラメーターを **adStatusUnwantedEvent** に設定します。

- *pRecordset*

  - **Recordset** オブジェクト。レコードを取得したオブジェクトです。

## <a name="remarks"></a>解説

Microsoft Visual Basic で **FetchComplete** を使用するには、Visual Basic 6.0 以降が必要です。

