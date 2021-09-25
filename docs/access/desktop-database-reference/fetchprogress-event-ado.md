---
title: FetchProgress イベント (ADO)
TOCTitle: FetchProgress event (ADO)
ms:assetid: 09145d9a-ea5e-b41c-6c54-33ec83e642a9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248828(v=office.15)
ms:contentKeyID: 48543114
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 32aca282a3ef79ad5e29614445559a653034528a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602674"
---
# <a name="fetchprogress-event-ado"></a>FetchProgress イベント (ADO)

**適用先**: Access 2013、Office 2013

非同期操作が長く続く場合、現在までに [Recordset](recordset-object-ado.md) に取得された行数を報告するために **FetchProgress** イベントが定期的に呼び出されます。

## <a name="syntax"></a>構文

FetchProgress *Progress*, *MaxProgress*, *adStatus*, *pRecordset*

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*Progress* |フェッチ操作によって、現在までに取得したレコード数を表す長整数型 ( **Long** ) の値です。|
|*MaxProgress* |取得する予定の最大レコード数を表す長整数型 ( **Long** ) の値です。|
|*adStatus* |[EventStatusEnum](eventstatusenum.md) 状態値です。|
|*pRecordset* |レコードの取得先のオブジェクトである **Recordset** オブジェクトです。|

## <a name="remarks"></a>注釈

子 **Recordset** を指定して **FetchProgress** を使用する場合、*Progress* パラメーターと *MaxProgress* パラメーターの値は、基になる [Cursor Service](microsoft-cursor-service-for-ole-db-ado-service-component.md) 行セットから派生します。戻り値は、基になる行セットの全レコード数であり、現在のチャプターのレコード数だけではありません。

> [!NOTE]
> [!メモ] Microsoft Visual Basic で **FetchProgress** を使用するには、Visual Basic 6.0 以降が必要です。


