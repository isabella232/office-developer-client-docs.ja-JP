---
title: イベントの移動と MoveComplete (ADO)
TOCTitle: WillMove and MoveComplete events (ADO)
ms:assetid: fe7eb823-b388-6b3d-1ae9-056018032ef5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250307(v=office.15)
ms:contentKeyID: 48548937
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e663e18a13803097d490e0e315d139e6e15400da
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306056"
---
# <a name="willmove-and-movecomplete-events-ado"></a>イベントの移動と MoveComplete (ADO)

**適用先:** Access 2013、Office 2013

**WillMove** イベントは、保留中の操作で [Recordset](recordset-object-ado.md) 内の現在の位置が変更される前に呼び出されます。 **MoveComplete** イベントは、 **Recordset** 内の現在の位置が変更された後に呼び出されます。

## <a name="syntax"></a>構文

移動*adReason*、 *adstatus*、 *precordset*

MoveComplete*adReason*、 **、 *adstatus*、 *precordset*

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*adReason* |このイベントの原因を示す [EventReasonEnum](eventreasonenum.md) 値です。値は **adRsnMoveFirst** 、 **adRsnMoveLast** 、 **adRsnMoveNext** 、 **adRsnMovePrevious** 、 **adRsnMove** 、または **adRsnRequery** です。|
|*の場合* |[Error](error-object-ado.md) オブジェクトです。 *adStatus* の値が **adStatusErrorsOccurred** の場合は、発生したエラーを示します。それ以外の場合は設定されません。|
|*adStatus* |[eventstatusenum](eventstatusenum.md)。 **WillMove** が呼び出されたとき、イベントを発生させた操作が成功した場合、このパラメーターは **adStatusOK** に設定されます。 保留中の操作の取り消しをこのイベントが要求できない場合、このパラメーターは **adStatusCantDeny** に設定されます。 <br/><br/>**MoveComplete** が呼び出されたとき、このパラメーターは、イベントを発生させた操作が成功した場合は **adStatusOK** 、失敗した場合は **adStatusErrorsOccurred** に設定されます。 <br/><br/>**WillMove** から制御が戻る前に、保留中の操作の取り消しを要求するには、このパラメーターを **adStatusCancel** に設定し、後続の通知が行われないようにするには、このパラメーターを adStatusUnwantedEvent に設定します。 <br/><br/>**MoveComplete** から制御が戻る前に後続の通知が行われるのを防ぐには、このパラメーターを **adStatusUnwantedEvent** に設定します。|
|*precordset* |[Recordset](recordset-object-ado.md) オブジェクト。このイベントが発生した **Recordset** オブジェクトです。|

## <a name="remarks"></a>注釈

次**** の**Recordset**の操作によって、 **MoveComplete**イベントが発生することがあります。

- [Open](open-method-ado-recordset.md)
- [Move](move-method-ado.md)
- [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)
- [MoveLast](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)
- [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) 
- [MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)
- [AddNew](addnew-method-ado.md)
- [Requery](requery-method-ado.md)

これらのイベントは、次のプロパティによって発生する可能性があります。

- [Filter](filter-property-ado.md)
- [インデックス](index-property-ado.md)
- [Bookmark](bookmark-property-ado.md)
- [AbsolutePage](absolutepage-property-ado.md)
- [AbsolutePosition](absoluteposition-property-ado.md)

これらのイベントは、子 **Recordset** に **Recordset** イベントが関連付けられているときに親 **Recordset** が移動した場合にも発生します。

*adReason* パラメーターを含むすべてのイベントのイベント通知を完全に停止するには、考えられる **adReason** 値ごとに *adStatus* パラメーターを *adStatusUnwantedEvent* に設定する必要があります。

