---
title: は changerecord イベントと RecordChangeComplete イベント (ADO) を行います。
TOCTitle: WillChangeRecord and RecordChangeComplete events (ADO)
ms:assetid: b21229b2-74e6-0798-95bf-0252f041831c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249851(v=office.15)
ms:contentKeyID: 48547162
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0113a7b22d0bba8e843ce9583e93eef848f872a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32305986"
---
# <a name="willchangerecord-and-recordchangecomplete-events-ado"></a>は changerecord イベントと RecordChangeComplete イベント (ADO) を行います。

**適用先:** Access 2013、Office 2013

**WillChangeRecord** イベントは、 [Recordset](recordset-object-ado.md) の 1 つ以上のレコード (行) が変更される前に呼び出されます。 **RecordChangeComplete** イベントは、1 つ以上のレコードが変更された後に呼び出されます。

## <a name="syntax"></a>構文

/changerecord*adReason*、 *crecords*、 *adstatus*、 *precordset*

RecordChangeComplete*adReason*、 *crecords*、 **、 *adstatus*、 *precordset*

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*adReason* |このイベントの原因を示す [EventReasonEnum](eventreasonenum.md) 値です。値は **adRsnAddNew** 、 **adRsnDelete** 、 **adRsnUpdate** 、 **adRsnUndoUpdate** 、 **adRsnUndoAddNew** 、 **adRsnUndoDelete** 、または **adRsnFirstChange** です。|
|*crecords* |変更される (影響を受ける) レコードの数を示す長整数型 ( **Long** ) の値です。|
|*の場合* |[Error](error-object-ado.md) オブジェクトです。 *adStatus* の値が **adStatusErrorsOccurred** の場合は、発生したエラーを示します。それ以外の場合は設定されません。|
|*adStatus* |[eventstatusenum](eventstatusenum.md)。 **WillChangeRecord** が呼び出されたとき、イベントを発生させた操作が成功した場合、このパラメーターは **adStatusOK** に設定されます。 保留中の操作の取り消しをこのイベントが要求できない場合、このパラメーターは **adStatusCantDeny** に設定されます。 <br/><br/>**RecordChangeComplete** が呼び出されたとき、このパラメーターは、イベントを発生させた操作が成功した場合は **adStatusOK** 、失敗した場合は **adStatusErrorsOccurred** に設定されます。 <br/><br/>**WillChangeRecord** から制御が戻る前に、このイベントを発生させた操作の取り消しを要求するには、このパラメーターを **adStatusCancel** に設定し、後続の通知が行われないようにするには、このパラメーターを adStatusUnwantedEvent に設定します。 <br/><br/>**RecordChangeComplete** から制御が戻る前に後続の通知が行われるのを防ぐには、このパラメーターを **adStatusUnwantedEvent** に設定します。|
|*precordset* |**Recordset** オブジェクト。このイベントが発生した **Recordset** オブジェクトです。|

## <a name="remarks"></a>注釈

**WillChangeRecord** イベントまたは **RecordChangeComplete** イベントは、 **Recordset** の [Update](update-method-ado.md)、[Delete](delete-method-ado-recordset.md)、[CancelUpdate](cancelupdate-method-ado.md)、[AddNew](addnew-method-ado.md)、[UpdateBatch](updatebatch-method-ado.md)、および [CancelBatch](cancelbatch-method-ado.md) の各操作によって、行のフィールドが最初に変更されたときに発生します。 **Recordset** [CursorType](cursortype-property-ado.md)の値は、イベントを発生させる操作を決定します。

イベントの**** 発生時に、 **Recordset** [Filter](filter-property-ado.md)プロパティは**adFilterAffectedRecords**に設定されます。 イベント処理中は、このプロパティを変更できません。

adReason パラメーターを含むすべてのイベントのイベント通知を完全に停止するには、考えられる adReason 値ごとに adStatus パラメーターを adStatusUnwantedEvent に設定する必要があります。

