---
title: endofrecordset イベント (ADO)
TOCTitle: EndOfRecordset event (ADO)
ms:assetid: 8995b851-dff6-2525-1d62-a2cfb4f95393
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249603(v=office.15)
ms:contentKeyID: 48546167
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 48e0eb25b443175013a144fafaa433df12c2cc9c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293561"
---
# <a name="endofrecordset-event-ado"></a>endofrecordset イベント (ADO)

**適用先:** Access 2013、Office 2013

**EndOfRecordset** イベントは、[Recordset](recordset-object-ado.md) の末尾を越える行に移動しようとすると呼び出されます。

## <a name="syntax"></a>構文

endofrecordset*fsupports データ*、 *adstatus*、 *precordset*

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*fのデータ* |バリアント型 (variant) の**\_BOOL**値。 variant\_TRUE に設定すると、 **Recordset**に追加された行が多いことを示します。|
|*adStatus* |[eventstatusenum](eventstatusenum.md)。 **EndOfRecordset** が呼び出されたとき、イベントを発生させた操作が成功した場合、このパラメーターは **adStatusOK** に設定されます。 イベントを発生させた操作の取り消しをこのイベントが要求できない場合、このパラメーターは **adStatusCantDeny** に設定されます。<br/><br/>**EndOfRecordset** から制御が戻る前に後続の通知が行われるのを防ぐには、このパラメーターを **adStatusUnwantedEvent** に設定します。|
|*precordset* | **Recordset** オブジェクト。このイベントが発生した **Recordset** オブジェクトです。|

## <a name="remarks"></a>注釈

**EndOfRecordset** イベントは、 [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) 操作が失敗した場合に発生することがあります。

このイベント ハンドラーは、たとえば **MoveNext** を呼び出して、 **Recordset** オブジェクトの末尾を越えて移動しようとすると呼び出されます。 ただし、このイベントの中で、データベースからさらにレコードを取得し、それらを **Recordset** の末尾に追加することもできます。 その場合は、 *ffar データ*をバリアント型\_の TRUE に設定し、 **endofrecordset**から戻ります。 その後で **MoveNext** を再度呼び出して、新たに取得したレコードにアクセスします。

