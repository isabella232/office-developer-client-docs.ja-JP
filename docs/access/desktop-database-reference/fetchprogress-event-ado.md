---
title: FetchProgress イベント (ADO)
TOCTitle: FetchProgress Event (ADO)
ms:assetid: 09145d9a-ea5e-b41c-6c54-33ec83e642a9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248828(v=office.15)
ms:contentKeyID: 48543114
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a898ad02d551e0c4de02597761ccd3076fc5eb77
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862280"
---
# <a name="fetchprogress-event-ado"></a>FetchProgress イベント (ADO)


**適用されます**Access 2013 |。Office 2013


非同期操作が長く続く場合、現在までに **Recordset** に取得された行数を報告するために [FetchProgress](recordset-object-ado.md) イベントが定期的に呼び出されます。

## <a name="syntax"></a>構文

FetchProgress*の進行状況*、 *MaxProgress*、 *adStatus*、 *pRecordset*

## <a name="parameters"></a>パラメーター

  - *Progress*

  - フェッチ操作によって、現在までに取得したレコード数を表す長整数型 ( **Long** ) の値です。

  - *MaxProgress*

  - 取得する予定の最大レコード数を表す長整数型 ( **Long** ) の値です。

  - *adStatus*

  - [EventStatusEnum](eventstatusenum.md) 状態値です。

  - *pRecordset*

  - レコードの取得先のオブジェクトである **Recordset** オブジェクトです。

## <a name="remarks"></a>解説

**FetchProgress**を使用して、子**レコード セット**に、場合は、*進捗状況*と*MaxProgress*パラメーターの値が基になる[カーソル サービス](microsoft-cursor-service-for-ole-db-ado-service-component.md)の行セットから派生したことに注意してください。 戻り値は、基になる行セットの全レコード数であり、現在のチャプターのレコード数だけではありません。


> [!NOTE]
> [!メモ] Microsoft Visual Basic で **FetchProgress** を使用するには、Visual Basic 6.0 以降が必要です。


