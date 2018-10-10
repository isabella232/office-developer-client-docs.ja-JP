---
title: WillChangeRecordset イベントと RecordsetChangeComplete イベント (ADO)
TOCTitle: WillChangeRecordset and RecordsetChangeComplete Events (ADO)
ms:assetid: 2cec4cf9-a4e9-c386-5202-04e86f4cf8ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249068(v=office.15)
ms:contentKeyID: 48543963
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7f9126005d8f11f859a3f45cbfec08e6612b59ac
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477206"
---
# <a name="willchangerecordset-and-recordsetchangecomplete-events-ado"></a>WillChangeRecordset イベントと RecordsetChangeComplete イベント (ADO)


**適用されます**Access 2013 |。Office 2013


**WillChangeRecordset** イベントは、保留中の操作で [Recordset](recordset-object-ado.md) が変更される前に呼び出されます。 **RecordsetChangeComplete** イベントは、 **Recordset** が変更された後に呼び出されます。

## <a name="syntax"></a>構文

WillChangeRecordset*adReason*、 *adStatus*、 *pRecordset*

RecordsetChangeComplete*adReason*、 *pError*、 *adStatus*、 *pRecordset*

## <a name="parameters"></a>パラメーター

  - *adReason*

  - このイベントの原因を示す [EventReasonEnum](eventreasonenum.md) 値です。値は **adRsnRequery** 、 **adRsnResynch** 、 **adRsnClose** 、 **adRsnOpen** です。

  - *adStatus*

  - [EventStatusEnum](eventstatusenum.md)
    
    **WillChangeRecordset** が呼び出されたとき、イベントを発生させた操作が成功した場合、このパラメーターは **adStatusOK** に設定されます。保留中の操作の取り消しをこのイベントが要求できない場合、このパラメーターは **adStatusCantDeny** に設定されます。
    
    **RecordsetChangeComplete** が呼び出されたとき、このパラメーターは、イベントを発生させた操作が成功した場合は **adStatusOK** 、操作が失敗した場合は **adStatusErrorsOccurred** 、以前に受け付けた **WillChangeRecordset** イベントに関連付けられた操作が取り消された場合は **adStatusCancel** に設定されます。
    
    **WillChangeRecordset** から制御が戻る前に、保留中の操作の取り消しを要求するには、このパラメーターを **adStatusCancel** に設定し、後続の通知が行われないようにするには、このパラメーターを adStatusUnwantedEvent に設定します。
    
    **WillChangeRecordset** または **RecordsetChangeComplete** から制御が戻る前に後続の通知が行われないようにするには、このパラメーターを **adStatusUnwantedEvent** に設定します。

  - *pError*

  - [Error](error-object-ado.md) オブジェクトです。 *adStatus* の値が **adStatusErrorsOccurred** の場合は、発生したエラーを示します。それ以外の場合は設定されません。

  - *pRecordset*

  - **Recordset** オブジェクト。このイベントが発生した **Recordset** オブジェクトです。

## <a name="remarks"></a>解説

**WillChangeRecordset**または**RecordsetChangeComplete**イベントは、**レコード セット**の[クエリを再実行](requery-method-ado.md)] または [[開く](open-method-ado-recordset.md)メソッドのため発生します。

プロバイダーがブックマークをサポートしていない場合、プロバイダーから新しい行が取得されるたびに **RecordsetChange** イベントの通知が発生します。このイベントの発生頻度は、 **RecordsetCacheSize** プロパティによって決まります。

**adReason** パラメーターを含むすべてのイベントのイベント通知を完全に停止するには、考えられる **adReason** 値ごとに **adStatus** パラメーターを **adStatusUnwantedEvent** に設定する必要があります。

