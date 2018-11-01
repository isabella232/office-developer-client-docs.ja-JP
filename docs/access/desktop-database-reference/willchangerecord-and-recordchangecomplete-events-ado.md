---
title: WillChangeRecord イベントと RecordChangeComplete イベント (ADO)
TOCTitle: WillChangeRecord and RecordChangeComplete Events (ADO)
ms:assetid: b21229b2-74e6-0798-95bf-0252f041831c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249851(v=office.15)
ms:contentKeyID: 48547162
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 895a80cf4810088b5f18f4a9416e7eadc54a004f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878130"
---
# <a name="willchangerecord-and-recordchangecomplete-events-ado"></a>WillChangeRecord イベントと RecordChangeComplete イベント (ADO)


**適用されます**Access 2013、Office 2013。


**WillChangeRecord** イベントは、 [Recordset](recordset-object-ado.md) の 1 つ以上のレコード (行) が変更される前に呼び出されます。 **RecordChangeComplete** イベントは、1 つ以上のレコードが変更された後に呼び出されます。

## <a name="syntax"></a>構文

WillChangeRecord*adReason*、 *cRecords*、 *adStatus*、 *pRecordset*

RecordChangeComplete*adReason*、 *cRecords*、 *pError*、 *adStatus*、 *pRecordset*

## <a name="parameters"></a>パラメーター

  - *adReason*

  - このイベントの原因を示す [EventReasonEnum](eventreasonenum.md) 値です。値は **adRsnAddNew** 、 **adRsnDelete** 、 **adRsnUpdate** 、 **adRsnUndoUpdate** 、 **adRsnUndoAddNew** 、 **adRsnUndoDelete** 、または **adRsnFirstChange** です。

  - *cRecords*

  - 変更される (影響を受ける) レコードの数を示す長整数型 ( **Long** ) の値です。

  - *pError*

  - [Error](error-object-ado.md) オブジェクトです。 *adStatus* の値が **adStatusErrorsOccurred** の場合は、発生したエラーを示します。それ以外の場合は設定されません。

  - *adStatus*

  - [EventStatusEnum](eventstatusenum.md)
    
    **WillChangeRecord** が呼び出されたとき、イベントを発生させた操作が成功した場合、このパラメーターは **adStatusOK** に設定されます。保留中の操作の取り消しをこのイベントが要求できない場合、このパラメーターは **adStatusCantDeny** に設定されます。
    
    **RecordChangeComplete** が呼び出されたとき、このパラメーターは、イベントを発生させた操作が成功した場合は **adStatusOK** 、失敗した場合は **adStatusErrorsOccurred** に設定されます。
    
    **WillChangeRecord** から制御が戻る前に、このイベントを発生させた操作の取り消しを要求するには、このパラメーターを **adStatusCancel** に設定し、後続の通知が行われないようにするには、このパラメーターを adStatusUnwantedEvent に設定します。
    
    **RecordChangeComplete** から制御が戻る前に後続の通知が行われるのを防ぐには、このパラメーターを **adStatusUnwantedEvent** に設定します。

  - *pRecordset*

  - **Recordset** オブジェクト。このイベントが発生した **Recordset** オブジェクトです。

## <a name="remarks"></a>解説

**WillChangeRecord** イベントまたは **RecordChangeComplete** イベントは、 **Recordset** の [Update](update-method-ado.md)、[Delete](delete-method-ado-recordset.md)、[CancelUpdate](cancelupdate-method-ado.md)、[AddNew](addnew-method-ado.md)、[UpdateBatch](updatebatch-method-ado.md)、および [CancelBatch](cancelbatch-method-ado.md) の各操作によって、行のフィールドが最初に変更されたときに発生します。 **Recordset**の[CursorType](cursortype-property-ado.md)の値は、どのような操作が発生するイベントが発生するを決定します。

**WillChangeRecord**イベントの実行中には、**レコード セット**の[Filter](filter-property-ado.md)プロパティは**adFilterAffectedRecords**に設定されます。 イベント処理中は、このプロパティを変更できません。

adReason パラメーターを含むすべてのイベントのイベント通知を完全に停止するには、考えられる adReason 値ごとに adStatus パラメーターを adStatusUnwantedEvent に設定する必要があります。

