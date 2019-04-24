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
# <a name="willmove-and-movecomplete-events-ado"></a><span data-ttu-id="b6fde-102">イベントの移動と MoveComplete (ADO)</span><span class="sxs-lookup"><span data-stu-id="b6fde-102">WillMove and MoveComplete events (ADO)</span></span>

<span data-ttu-id="b6fde-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="b6fde-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b6fde-p101">**WillMove** イベントは、保留中の操作で [Recordset](recordset-object-ado.md) 内の現在の位置が変更される前に呼び出されます。 **MoveComplete** イベントは、 **Recordset** 内の現在の位置が変更された後に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="b6fde-p101">The **WillMove** event is called before a pending operation changes the current position in the [Recordset](recordset-object-ado.md). The **MoveComplete** event is called after the current position in the **Recordset** changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6fde-106">構文</span><span class="sxs-lookup"><span data-stu-id="b6fde-106">Syntax</span></span>

<span data-ttu-id="b6fde-107">移動*adReason*、 *adstatus*、 *precordset*</span><span class="sxs-lookup"><span data-stu-id="b6fde-107">WillMove*adReason*, *adStatus*, *pRecordset*</span></span>

<span data-ttu-id="b6fde-108">MoveComplete*adReason*、 \*\*、 *adstatus*、 *precordset*</span><span class="sxs-lookup"><span data-stu-id="b6fde-108">MoveComplete*adReason*, *pError*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="b6fde-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b6fde-109">Parameters</span></span>

|<span data-ttu-id="b6fde-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b6fde-110">Parameter</span></span>|<span data-ttu-id="b6fde-111">説明</span><span class="sxs-lookup"><span data-stu-id="b6fde-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="b6fde-112">*adReason*</span><span class="sxs-lookup"><span data-stu-id="b6fde-112">*adReason*</span></span> |<span data-ttu-id="b6fde-p102">このイベントの原因を示す [EventReasonEnum](eventreasonenum.md) 値です。値は **adRsnMoveFirst** 、 **adRsnMoveLast** 、 **adRsnMoveNext** 、 **adRsnMovePrevious** 、 **adRsnMove** 、または **adRsnRequery** です。</span><span class="sxs-lookup"><span data-stu-id="b6fde-p102">An [EventReasonEnum](eventreasonenum.md) value that specifies the reason for this event. Its value can be **adRsnMoveFirst**, **adRsnMoveLast**, **adRsnMoveNext**, **adRsnMovePrevious**, **adRsnMove**, or **adRsnRequery**.</span></span>|
|<span data-ttu-id="b6fde-115">*の場合*</span><span class="sxs-lookup"><span data-stu-id="b6fde-115">*pError*</span></span> |<span data-ttu-id="b6fde-p103">[Error](error-object-ado.md) オブジェクトです。 *adStatus* の値が **adStatusErrorsOccurred** の場合は、発生したエラーを示します。それ以外の場合は設定されません。</span><span class="sxs-lookup"><span data-stu-id="b6fde-p103">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of *adStatus* is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>|
|<span data-ttu-id="b6fde-118">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="b6fde-118">*adStatus*</span></span> |<span data-ttu-id="b6fde-119">[eventstatusenum](eventstatusenum.md)。</span><span class="sxs-lookup"><span data-stu-id="b6fde-119">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="b6fde-120">**WillMove** が呼び出されたとき、イベントを発生させた操作が成功した場合、このパラメーターは **adStatusOK** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="b6fde-120">When **WillMove** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful.</span></span> <span data-ttu-id="b6fde-121">保留中の操作の取り消しをこのイベントが要求できない場合、このパラメーターは **adStatusCantDeny** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="b6fde-121">It is set to **adStatusCantDeny** if this event cannot request cancellation of the pending operation.</span></span> <br/><br/><span data-ttu-id="b6fde-122">**MoveComplete** が呼び出されたとき、このパラメーターは、イベントを発生させた操作が成功した場合は **adStatusOK** 、失敗した場合は **adStatusErrorsOccurred** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="b6fde-122">When **MoveComplete** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful, or to **adStatusErrorsOccurred** if the operation failed.</span></span> <br/><br/><span data-ttu-id="b6fde-123">**WillMove** から制御が戻る前に、保留中の操作の取り消しを要求するには、このパラメーターを **adStatusCancel** に設定し、後続の通知が行われないようにするには、このパラメーターを adStatusUnwantedEvent に設定します。</span><span class="sxs-lookup"><span data-stu-id="b6fde-123">Before **WillMove** returns, set this parameter to **adStatusCancel** to request cancellation of the pending operation or set this parameter to adStatusUnwantedEvent to prevent subsequent notications.</span></span> <br/><br/><span data-ttu-id="b6fde-124">**MoveComplete** から制御が戻る前に後続の通知が行われるのを防ぐには、このパラメーターを **adStatusUnwantedEvent** に設定します。</span><span class="sxs-lookup"><span data-stu-id="b6fde-124">Before **MoveComplete** returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>|
|<span data-ttu-id="b6fde-125">*precordset*</span><span class="sxs-lookup"><span data-stu-id="b6fde-125">*pRecordset*</span></span> |<span data-ttu-id="b6fde-p105">[Recordset](recordset-object-ado.md) オブジェクト。このイベントが発生した **Recordset** オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="b6fde-p105">A [Recordset](recordset-object-ado.md) object. The **Recordset** for which this event occurred.</span></span>|

## <a name="remarks"></a><span data-ttu-id="b6fde-128">注釈</span><span class="sxs-lookup"><span data-stu-id="b6fde-128">Remarks</span></span>

<span data-ttu-id="b6fde-129">次\*\*\*\* の**Recordset**の操作によって、 **MoveComplete**イベントが発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="b6fde-129">A **WillMove** or **MoveComplete** event may occur due to the following **Recordset** operations:</span></span>

- [<span data-ttu-id="b6fde-130">Open</span><span class="sxs-lookup"><span data-stu-id="b6fde-130">Open</span></span>](open-method-ado-recordset.md)
- [<span data-ttu-id="b6fde-131">Move</span><span class="sxs-lookup"><span data-stu-id="b6fde-131">Move</span></span>](move-method-ado.md)
- [<span data-ttu-id="b6fde-132">MoveFirst</span><span class="sxs-lookup"><span data-stu-id="b6fde-132">MoveFirst</span></span>](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)
- [<span data-ttu-id="b6fde-133">MoveLast</span><span class="sxs-lookup"><span data-stu-id="b6fde-133">MoveLast</span></span>](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)
- [<span data-ttu-id="b6fde-134">MoveNext</span><span class="sxs-lookup"><span data-stu-id="b6fde-134">MoveNext</span></span>](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) 
- [<span data-ttu-id="b6fde-135">MovePrevious</span><span class="sxs-lookup"><span data-stu-id="b6fde-135">MovePrevious</span></span>](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)
- [<span data-ttu-id="b6fde-136">AddNew</span><span class="sxs-lookup"><span data-stu-id="b6fde-136">AddNew</span></span>](addnew-method-ado.md)
- [<span data-ttu-id="b6fde-137">Requery</span><span class="sxs-lookup"><span data-stu-id="b6fde-137">Requery</span></span>](requery-method-ado.md)

<span data-ttu-id="b6fde-138">これらのイベントは、次のプロパティによって発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b6fde-138">These events may occur because of the following properties:</span></span>

- [<span data-ttu-id="b6fde-139">Filter</span><span class="sxs-lookup"><span data-stu-id="b6fde-139">Filter</span></span>](filter-property-ado.md)
- [<span data-ttu-id="b6fde-140">インデックス</span><span class="sxs-lookup"><span data-stu-id="b6fde-140">Index</span></span>](index-property-ado.md)
- [<span data-ttu-id="b6fde-141">Bookmark</span><span class="sxs-lookup"><span data-stu-id="b6fde-141">Bookmark</span></span>](bookmark-property-ado.md)
- [<span data-ttu-id="b6fde-142">AbsolutePage</span><span class="sxs-lookup"><span data-stu-id="b6fde-142">AbsolutePage</span></span>](absolutepage-property-ado.md)
- [<span data-ttu-id="b6fde-143">AbsolutePosition</span><span class="sxs-lookup"><span data-stu-id="b6fde-143">AbsolutePosition</span></span>](absoluteposition-property-ado.md)

<span data-ttu-id="b6fde-144">これらのイベントは、子 **Recordset** に **Recordset** イベントが関連付けられているときに親 **Recordset** が移動した場合にも発生します。</span><span class="sxs-lookup"><span data-stu-id="b6fde-144">These events also occur if a child **Recordset** has **Recordset** events connected and the parent **Recordset** is moved.</span></span>

<span data-ttu-id="b6fde-145">*adReason* パラメーターを含むすべてのイベントのイベント通知を完全に停止するには、考えられる **adReason** 値ごとに *adStatus* パラメーターを *adStatusUnwantedEvent* に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b6fde-145">You must set the *adStatus* parameter to **adStatusUnwantedEvent** for each possible *adReason* value in order to completely stop event notification for any event that includes an *adReason* parameter.</span></span>

