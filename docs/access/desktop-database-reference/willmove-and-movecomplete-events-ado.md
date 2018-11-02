---
title: WillMove イベントと MoveComplete イベント (ADO)
TOCTitle: WillMove and MoveComplete events (ADO)
ms:assetid: fe7eb823-b388-6b3d-1ae9-056018032ef5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250307(v=office.15)
ms:contentKeyID: 48548937
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5388601f1ac88e281a6abc5cfe1e644bdeebef28
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923568"
---
# <a name="willmove-and-movecomplete-events-ado"></a>WillMove イベントと MoveComplete イベント (ADO)


**適用されます**Access 2013、Office 2013。

**WillMove** イベントは、保留中の操作で [Recordset](recordset-object-ado.md) 内の現在の位置が変更される前に呼び出されます。 **MoveComplete** イベントは、 **Recordset** 内の現在の位置が変更された後に呼び出されます。

## <a name="syntax"></a>構文

WillMove*adReason*、 *adStatus*、 *pRecordset*

MoveComplete*adReason*、 *pError*、 *adStatus*、 *pRecordset*

## <a name="parameters"></a>パラメーター

  - *adReason*

  - このイベントの原因を示す [EventReasonEnum](eventreasonenum.md) 値です。値は **adRsnMoveFirst** 、 **adRsnMoveLast** 、 **adRsnMoveNext** 、 **adRsnMovePrevious** 、 **adRsnMove** 、または **adRsnRequery** です。

  - *pError*

  - [Error](error-object-ado.md) オブジェクトです。 *adStatus* の値が **adStatusErrorsOccurred** の場合は、発生したエラーを示します。それ以外の場合は設定されません。

  - *adStatus*

  - [EventStatusEnum](eventstatusenum.md)
    
    **WillMove** が呼び出されたとき、イベントを発生させた操作が成功した場合、このパラメーターは **adStatusOK** に設定されます。保留中の操作の取り消しをこのイベントが要求できない場合、このパラメーターは **adStatusCantDeny** に設定されます。
    
    **MoveComplete** が呼び出されたとき、このパラメーターは、イベントを発生させた操作が成功した場合は **adStatusOK** 、失敗した場合は **adStatusErrorsOccurred** に設定されます。
    
    **WillMove** から制御が戻る前に、保留中の操作の取り消しを要求するには、このパラメーターを **adStatusCancel** に設定し、後続の通知が行われないようにするには、このパラメーターを adStatusUnwantedEvent に設定します。
    
    **MoveComplete** から制御が戻る前に後続の通知が行われるのを防ぐには、このパラメーターを **adStatusUnwantedEvent** に設定します。

  - *pRecordset*

  - [Recordset](recordset-object-ado.md) オブジェクト。このイベントが発生した **Recordset** オブジェクトです。

## <a name="remarks"></a>解説

**WillMove** イベントまたは **MoveComplete** イベントは、 **Recordset** の [Open](open-method-ado-recordset.md)、[Move](move-method-ado.md)、[MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)、[MoveLast](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)、[MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)、[MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)、[AddNew](addnew-method-ado.md)、および [Requery](requery-method-ado.md) の各操作によって発生します。これらのイベントは、 [Filter](filter-property-ado.md)、[Index](index-property-ado.md)、[Bookmark](bookmark-property-ado.md)、[AbsolutePage](absolutepage-property-ado.md)、および [AbsolutePosition](absoluteposition-property-ado.md) の各プロパティに基づいて発生します。これらのイベントは、子 **Recordset** に **Recordset** イベントが関連付けられているときに親 **Recordset** が移動した場合にも発生します。

adReason パラメーターを含むすべてのイベントのイベント通知を完全に停止するには、考えられる adReason 値ごとに **adStatus** パラメーターを **adStatusUnwantedEvent** に設定する必要があります。

