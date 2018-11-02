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
# <a name="willmove-and-movecomplete-events-ado"></a><span data-ttu-id="3ba8e-102">WillMove イベントと MoveComplete イベント (ADO)</span><span class="sxs-lookup"><span data-stu-id="3ba8e-102">WillMove and MoveComplete events (ADO)</span></span>


<span data-ttu-id="3ba8e-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="3ba8e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3ba8e-p101">**WillMove** イベントは、保留中の操作で [Recordset](recordset-object-ado.md) 内の現在の位置が変更される前に呼び出されます。 **MoveComplete** イベントは、 **Recordset** 内の現在の位置が変更された後に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="3ba8e-p101">The **WillMove** event is called before a pending operation changes the current position in the [Recordset](recordset-object-ado.md). The **MoveComplete** event is called after the current position in the **Recordset** changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ba8e-106">構文</span><span class="sxs-lookup"><span data-stu-id="3ba8e-106">Syntax</span></span>

<span data-ttu-id="3ba8e-107">WillMove*adReason*、 *adStatus*、 *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="3ba8e-107">WillMove*adReason*, *adStatus*, *pRecordset*</span></span>

<span data-ttu-id="3ba8e-108">MoveComplete*adReason*、 *pError*、 *adStatus*、 *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="3ba8e-108">MoveComplete*adReason*, *pError*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="3ba8e-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="3ba8e-109">Parameters</span></span>

  - <span data-ttu-id="3ba8e-110">*adReason*</span><span class="sxs-lookup"><span data-stu-id="3ba8e-110">*adReason*</span></span>

  - <span data-ttu-id="3ba8e-p102">このイベントの原因を示す [EventReasonEnum](eventreasonenum.md) 値です。値は **adRsnMoveFirst** 、 **adRsnMoveLast** 、 **adRsnMoveNext** 、 **adRsnMovePrevious** 、 **adRsnMove** 、または **adRsnRequery** です。</span><span class="sxs-lookup"><span data-stu-id="3ba8e-p102">An [EventReasonEnum](eventreasonenum.md) value that specifies the reason for this event. Its value can be **adRsnMoveFirst**, **adRsnMoveLast**, **adRsnMoveNext**, **adRsnMovePrevious**, **adRsnMove**, or **adRsnRequery**.</span></span>

  - <span data-ttu-id="3ba8e-113">*pError*</span><span class="sxs-lookup"><span data-stu-id="3ba8e-113">*pError*</span></span>

  - <span data-ttu-id="3ba8e-p103">[Error](error-object-ado.md) オブジェクトです。 *adStatus* の値が **adStatusErrorsOccurred** の場合は、発生したエラーを示します。それ以外の場合は設定されません。</span><span class="sxs-lookup"><span data-stu-id="3ba8e-p103">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of *adStatus* is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>

  - <span data-ttu-id="3ba8e-116">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="3ba8e-116">*adStatus*</span></span>

  - [<span data-ttu-id="3ba8e-117">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="3ba8e-117">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="3ba8e-p104">**WillMove** が呼び出されたとき、イベントを発生させた操作が成功した場合、このパラメーターは **adStatusOK** に設定されます。保留中の操作の取り消しをこのイベントが要求できない場合、このパラメーターは **adStatusCantDeny** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="3ba8e-p104">When **WillMove** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful. It is set to **adStatusCantDeny** if this event cannot request cancellation of the pending operation.</span></span>
    
    <span data-ttu-id="3ba8e-120">**MoveComplete** が呼び出されたとき、このパラメーターは、イベントを発生させた操作が成功した場合は **adStatusOK** 、失敗した場合は **adStatusErrorsOccurred** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="3ba8e-120">When **MoveComplete** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful, or to **adStatusErrorsOccurred** if the operation failed.</span></span>
    
    <span data-ttu-id="3ba8e-121">**WillMove** から制御が戻る前に、保留中の操作の取り消しを要求するには、このパラメーターを **adStatusCancel** に設定し、後続の通知が行われないようにするには、このパラメーターを adStatusUnwantedEvent に設定します。</span><span class="sxs-lookup"><span data-stu-id="3ba8e-121">Before **WillMove** returns, set this parameter to **adStatusCancel** to request cancellation of the pending operation or set this parameter to adStatusUnwantedEvent to prevent subsequent notications.</span></span>
    
    <span data-ttu-id="3ba8e-122">**MoveComplete** から制御が戻る前に後続の通知が行われるのを防ぐには、このパラメーターを **adStatusUnwantedEvent** に設定します。</span><span class="sxs-lookup"><span data-stu-id="3ba8e-122">Before **MoveComplete** returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>

  - <span data-ttu-id="3ba8e-123">*pRecordset*</span><span class="sxs-lookup"><span data-stu-id="3ba8e-123">*pRecordset*</span></span>

  - <span data-ttu-id="3ba8e-p105">[Recordset](recordset-object-ado.md) オブジェクト。このイベントが発生した **Recordset** オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="3ba8e-p105">A [Recordset](recordset-object-ado.md) object. The **Recordset** for which this event occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ba8e-126">解説</span><span class="sxs-lookup"><span data-stu-id="3ba8e-126">Remarks</span></span>

<span data-ttu-id="3ba8e-p106">**WillMove** イベントまたは **MoveComplete** イベントは、 **Recordset** の [Open](open-method-ado-recordset.md)、[Move](move-method-ado.md)、[MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)、[MoveLast](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)、[MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)、[MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)、[AddNew](addnew-method-ado.md)、および [Requery](requery-method-ado.md) の各操作によって発生します。これらのイベントは、 [Filter](filter-property-ado.md)、[Index](index-property-ado.md)、[Bookmark](bookmark-property-ado.md)、[AbsolutePage](absolutepage-property-ado.md)、および [AbsolutePosition](absoluteposition-property-ado.md) の各プロパティに基づいて発生します。これらのイベントは、子 **Recordset** に **Recordset** イベントが関連付けられているときに親 **Recordset** が移動した場合にも発生します。</span><span class="sxs-lookup"><span data-stu-id="3ba8e-p106">A **WillMove** or **MoveComplete** event may occur due to the following **Recordset** operations: [Open](open-method-ado-recordset.md), [Move](move-method-ado.md), [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), [MoveLast](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), [MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), [AddNew](addnew-method-ado.md), and [Requery](requery-method-ado.md). These events may occur because of the following properties: [Filter](filter-property-ado.md), [Index](index-property-ado.md), [Bookmark](bookmark-property-ado.md), [AbsolutePage](absolutepage-property-ado.md), and [AbsolutePosition](absoluteposition-property-ado.md). These events also occur if a child **Recordset** has **Recordset** events connected and the parent **Recordset** is moved.</span></span>

<span data-ttu-id="3ba8e-130">adReason パラメーターを含むすべてのイベントのイベント通知を完全に停止するには、考えられる adReason 値ごとに **adStatus** パラメーターを **adStatusUnwantedEvent** に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3ba8e-130">You must set the **adStatus** parameter to **adStatusUnwantedEvent** for each possible adReason value in order to completely stop event notification for any event that includes an adReason parameter.</span></span>

