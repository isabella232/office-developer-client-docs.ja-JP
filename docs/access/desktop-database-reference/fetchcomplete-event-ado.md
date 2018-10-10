---
title: FetchComplete イベント (ADO)
TOCTitle: FetchComplete Event (ADO)
ms:assetid: 4863d5b5-7d77-bdef-c511-f85c9e6dec9d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249224(v=office.15)
ms:contentKeyID: 48544621
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 299fec4a831bbde5d3fd2d58e0f76edb2acea0f8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478281"
---
# <a name="fetchcomplete-event-ado"></a>FetchComplete イベント (ADO)


**適用されます**Access 2013 |。Office 2013


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

