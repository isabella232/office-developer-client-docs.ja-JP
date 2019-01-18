---
title: EndOfRecordset イベント (ADO)
TOCTitle: EndOfRecordset event (ADO)
ms:assetid: 8995b851-dff6-2525-1d62-a2cfb4f95393
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249603(v=office.15)
ms:contentKeyID: 48546167
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 48e0eb25b443175013a144fafaa433df12c2cc9c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721361"
---
# <a name="endofrecordset-event-ado"></a>EndOfRecordset イベント (ADO)

**適用されます**Access 2013、Office 2013。

**EndOfRecordset** イベントは、 [Recordset](recordset-object-ado.md) の末尾を越える行に移動しようとすると呼び出されます。

## <a name="syntax"></a>構文

EndOfRecordset*fMoreData*、 *adStatus*、 *pRecordset*

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*fMoreData* |A**バリアント\_BOOL**値をバリアント型に設定\_true の場合、複数の行は、**レコード セット**に追加されていることを示します。|
|*adStatus* |[EventStatusEnum](eventstatusenum.md)。 **EndOfRecordset** が呼び出されたとき、イベントを発生させた操作が成功した場合、このパラメーターは **adStatusOK** に設定されます。 イベントを発生させた操作の取り消しをこのイベントが要求できない場合、このパラメーターは **adStatusCantDeny** に設定されます。<br/><br/>**EndOfRecordset** から制御が戻る前に後続の通知が行われるのを防ぐには、このパラメーターを **adStatusUnwantedEvent** に設定します。|
|*pRecordset* | **Recordset** オブジェクト。このイベントが発生した **Recordset** オブジェクトです。|

## <a name="remarks"></a>解説

**EndOfRecordset** イベントは、 [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) 操作が失敗した場合に発生することがあります。

このイベント ハンドラーは、たとえば **MoveNext** を呼び出して、 **Recordset** オブジェクトの末尾を越えて移動しようとすると呼び出されます。 ただし、このイベントの中で、データベースからさらにレコードを取得し、それらを **Recordset** の末尾に追加することもできます。 その場合は、 *fMoreData*をバリアント型に設定\_true に設定し、 **EndOfRecordset**からの戻り値です。 その後で **MoveNext** を再度呼び出して、新たに取得したレコードにアクセスします。

