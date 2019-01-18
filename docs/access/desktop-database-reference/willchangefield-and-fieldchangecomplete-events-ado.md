---
title: WillChangeField イベントと FieldChangeComplete イベント (ADO)
TOCTitle: WillChangeField and FieldChangeComplete events (ADO)
ms:assetid: bc4455a6-2925-33dc-d04f-8ea570e5e370
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249904(v=office.15)
ms:contentKeyID: 48547407
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0fd952cc09f410752f3eb7b5963059f8d6ee7c2c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700186"
---
# <a name="willchangefield-and-fieldchangecomplete-events-ado"></a>WillChangeField イベントと FieldChangeComplete イベント (ADO)

**適用されます**Access 2013、Office 2013。

**WillChangeField** イベントは、保留中の操作で [Recordset](field-object-ado.md) 内の 1 つ以上の [Field](recordset-object-ado.md) オブジェクトの値が変更される前に呼び出されます。 **FieldChangeComplete** イベントは、1 つ以上の **Field** オブジェクトの値が変更された後に呼び出されます。

## <a name="syntax"></a>構文

WillChangeField*cFields*、*フィールド*、 *adStatus*、 *pRecordset*

FieldChangeComplete*cFields*、*フィールド*、 *pError*、 *adStatus*、 *pRecordset*

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*cFields* |*Fields* 内の **Field** オブジェクトの数を表す長整数型 (**Long**) の値です。|
|*フィールド* |**WillChangeField**の場合は、*フィールド*のパラメーターは元の値を持つ**フィールド**オブジェクトを格納する**バリアント**の配列です。 <br/><br/>**FieldChangeComplete**の場合、*フィールド*・ パラメーターの値が変更された**フィールド**のオブジェクトを含む**バリアント**の配列です。|
|*pError* |[Error](error-object-ado.md) オブジェクトです。 *adStatus* の値が **adStatusErrorsOccurred** の場合は、発生したエラーを示します。それ以外の場合は設定されません。|
|*adStatus* |[EventStatusEnum](eventstatusenum.md)。 **WillChangeField** が呼び出されたとき、イベントを発生させた操作が成功した場合、このパラメーターは **adStatusOK** に設定されます。 保留中の操作の取り消しをこのイベントが要求できない場合、このパラメーターは **adStatusCantDeny** に設定されます。 <br/><br/>**FieldChangeComplete** が呼び出されたとき、このパラメーターは、イベントを発生させた操作が成功した場合は **adStatusOK** 、失敗した場合は **adStatusErrorsOccurred** に設定されます。 <br/><br/>**WillChangeField** から制御が戻る前に保留中の操作の取り消しを要求する場合は、このパラメーターを **adStatusCancel** に設定します。 <br/><br/>**FieldChangeComplete** から制御が戻る前に後続の通知が行われるのを防ぐには、このパラメーターを **adStatusUnwantedEvent** に設定します。|
|*pRecordset* |**Recordset** オブジェクト。このイベントが発生した **Recordset** オブジェクトです。|

## <a name="remarks"></a>解説

**WillChangeField** イベントまたは **FieldChangeComplete** イベントは、 [Value](value-property-ado.md) プロパティを設定し、フィールドと値配列パラメーターを指定して [Update](update-method-ado.md) メソッドを呼び出したときに発生します。

