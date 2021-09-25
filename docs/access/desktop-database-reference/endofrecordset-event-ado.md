---
title: EndOfRecordset イベント (ADO)
TOCTitle: EndOfRecordset event (ADO)
ms:assetid: 8995b851-dff6-2525-1d62-a2cfb4f95393
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249603(v=office.15)
ms:contentKeyID: 48546167
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 336dd8f5dce734e7b820f8bf78f113d122d90444
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602753"
---
# <a name="endofrecordset-event-ado"></a>EndOfRecordset イベント (ADO)

**適用先**: Access 2013、Office 2013

**EndOfRecordset** イベントは、[Recordset](recordset-object-ado.md) の末尾を越える行に移動しようとすると呼び出されます。

## <a name="syntax"></a>構文

EndOfRecordset *fMoreData*, *adStatus*, *pRecordset*

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*fMoreData* |**VARIANT \_ TRUE に設定されている** 場合は、Recordset に追加された行が多く含まれます \_ 。 |
|*adStatus* |[EventStatusEnum](eventstatusenum.md). **EndOfRecordset** が呼び出されたとき、イベントを発生させた操作が成功した場合、このパラメーターは **adStatusOK** に設定されます。 イベントを発生させた操作の取り消しをこのイベントが要求できない場合、このパラメーターは **adStatusCantDeny** に設定されます。<br/><br/>**EndOfRecordset** から制御が戻る前に後続の通知が行われるのを防ぐには、このパラメーターを **adStatusUnwantedEvent** に設定します。|
|*pRecordset* | **Recordset** オブジェクト。このイベントが発生した **Recordset** オブジェクトです。|

## <a name="remarks"></a>注釈

**EndOfRecordset** イベントは、 [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) 操作が失敗した場合に発生することがあります。

このイベント ハンドラーは、たとえば **MoveNext** を呼び出して、 **Recordset** オブジェクトの末尾を越えて移動しようとすると呼び出されます。 ただし、このイベントの中で、データベースからさらにレコードを取得し、それらを **Recordset** の末尾に追加することもできます。 その場合は *、fMoreData を* VARIANT TRUE に設定 \_ し **、EndOfRecordset から返します**。 その後で **MoveNext** を再度呼び出して、新たに取得したレコードにアクセスします。

