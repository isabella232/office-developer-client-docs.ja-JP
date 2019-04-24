---
title: fetchprogress イベント (ADO)
TOCTitle: FetchProgress event (ADO)
ms:assetid: 09145d9a-ea5e-b41c-6c54-33ec83e642a9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248828(v=office.15)
ms:contentKeyID: 48543114
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d863f51e7836acdc577ecd720df77114ed66f067
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293183"
---
# <a name="fetchprogress-event-ado"></a>fetchprogress イベント (ADO)

**適用先:** Access 2013、Office 2013

非同期操作が長く続く場合、現在までに [Recordset](recordset-object-ado.md) に取得された行数を報告するために **FetchProgress** イベントが定期的に呼び出されます。

## <a name="syntax"></a>構文

fetchprogress** の進行状況、 *maxprogress*、 *adstatus*、 *precordset*

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*Progress* |フェッチ操作によって、現在までに取得したレコード数を表す長整数型 ( **Long** ) の値です。|
|*maxprogress* |取得する予定の最大レコード数を表す長整数型 ( **Long** ) の値です。|
|*adStatus* |[EventStatusEnum](eventstatusenum.md) 状態値です。|
|*precordset* |レコードの取得先のオブジェクトである **Recordset** オブジェクトです。|

## <a name="remarks"></a>注釈

子 **Recordset** を指定して **FetchProgress** を使用する場合、*Progress* パラメーターと *MaxProgress* パラメーターの値は、基になる [Cursor Service](microsoft-cursor-service-for-ole-db-ado-service-component.md) 行セットから派生します。戻り値は、基になる行セットの全レコード数であり、現在のチャプターのレコード数だけではありません。

> [!NOTE]
> [!メモ] Microsoft Visual Basic で **FetchProgress** を使用するには、Visual Basic 6.0 以降が必要です。


