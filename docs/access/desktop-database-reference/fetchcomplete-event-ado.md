---
title: fetchcomplete イベント (ADO)
TOCTitle: FetchComplete event (ADO)
ms:assetid: 4863d5b5-7d77-bdef-c511-f85c9e6dec9d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249224(v=office.15)
ms:contentKeyID: 48544621
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f4c1cb1379d1faec39fd44fa8273fba4aadca548
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293190"
---
# <a name="fetchcomplete-event-ado"></a>fetchcomplete イベント (ADO)

**適用先:** Access 2013、Office 2013

**FetchComplete** イベントは、長い非同期操作ですべてのレコードが [Recordset](recordset-object-ado.md) に取得された後に呼び出されます。

## <a name="syntax"></a>構文

fetchcomplete** の*状態、adstatus*、 *precordset*

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*の場合* |[Error](error-object-ado.md) オブジェクトです。 **adStatus** の値が **adStatusErrorsOccurred** の場合は、発生したエラーを示します。それ以外の場合は設定されません。|
|*adStatus* |[eventstatusenum](eventstatusenum.md)。 このイベントから制御が戻る前に後続の通知が行われるのを防ぐには、このパラメーターを **adStatusUnwantedEvent** に設定します。|
|*precordset* |**Recordset** オブジェクト。レコードを取得したオブジェクトです。|

## <a name="remarks"></a>注釈

Microsoft Visual Basic で **FetchComplete** を使用するには、Visual Basic 6.0 以降が必要です。

