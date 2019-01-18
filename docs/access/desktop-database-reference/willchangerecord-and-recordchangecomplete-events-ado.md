---
title: WillChangeRecord イベントと RecordChangeComplete イベント (ADO)
TOCTitle: WillChangeRecord and RecordChangeComplete events (ADO)
ms:assetid: b21229b2-74e6-0798-95bf-0252f041831c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249851(v=office.15)
ms:contentKeyID: 48547162
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0113a7b22d0bba8e843ce9583e93eef848f872a5
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710840"
---
# <a name="willchangerecord-and-recordchangecomplete-events-ado"></a><span data-ttu-id="8cf24-102">WillChangeRecord イベントと RecordChangeComplete イベント (ADO)</span><span class="sxs-lookup"><span data-stu-id="8cf24-102">WillChangeRecord and RecordChangeComplete events (ADO)</span></span>

<span data-ttu-id="8cf24-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="8cf24-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8cf24-p101">**WillChangeRecord** イベントは、 [Recordset](recordset-object-ado.md) の 1 つ以上のレコード (行) が変更される前に呼び出されます。 **RecordChangeComplete** イベントは、1 つ以上のレコードが変更された後に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="8cf24-p101">The **WillChangeRecord** event is called before one or more records (rows) in the [Recordset](recordset-object-ado.md) change. The **RecordChangeComplete** event is called after one or more records change.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cf24-106">構文</span><span class="sxs-lookup"><span data-stu-id="8cf24-106">Syntax</span></span>

<span data-ttu-id="8cf24-107">WillChangeRecord*adReason*、 *cRecords*、 *adStatus*、 *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="8cf24-107">WillChangeRecord*adReason*, *cRecords*, *adStatus*, *pRecordset*</span></span>

<span data-ttu-id="8cf24-108">RecordChangeComplete*adReason*、 *cRecords*、 *pError*、 *adStatus*、 *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="8cf24-108">RecordChangeComplete*adReason*, *cRecords*, *pError*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="8cf24-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8cf24-109">Parameters</span></span>

|<span data-ttu-id="8cf24-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8cf24-110">Parameter</span></span>|<span data-ttu-id="8cf24-111">説明</span><span class="sxs-lookup"><span data-stu-id="8cf24-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="8cf24-112">*adReason*</span><span class="sxs-lookup"><span data-stu-id="8cf24-112">*adReason*</span></span> |<span data-ttu-id="8cf24-p102">このイベントの原因を示す [EventReasonEnum](eventreasonenum.md) 値です。値は **adRsnAddNew** 、 **adRsnDelete** 、 **adRsnUpdate** 、 **adRsnUndoUpdate** 、 **adRsnUndoAddNew** 、 **adRsnUndoDelete** 、または **adRsnFirstChange** です。</span><span class="sxs-lookup"><span data-stu-id="8cf24-p102">An [EventReasonEnum](eventreasonenum.md) value that specifies the reason for this event. Its value can be **adRsnAddNew**, **adRsnDelete**, **adRsnUpdate**, **adRsnUndoUpdate**, **adRsnUndoAddNew**, **adRsnUndoDelete**, or **adRsnFirstChange**.</span></span>|
|<span data-ttu-id="8cf24-115">*cRecords*</span><span class="sxs-lookup"><span data-stu-id="8cf24-115">*cRecords*</span></span> |<span data-ttu-id="8cf24-116">変更される (影響を受ける) レコードの数を示す長整数型 ( **Long** ) の値です。</span><span class="sxs-lookup"><span data-stu-id="8cf24-116">A **Long** value that indicates the number of records changing (affected).</span></span>|
|<span data-ttu-id="8cf24-117">*pError*</span><span class="sxs-lookup"><span data-stu-id="8cf24-117">*pError*</span></span> |<span data-ttu-id="8cf24-p103">[Error](error-object-ado.md) オブジェクトです。 *adStatus* の値が **adStatusErrorsOccurred** の場合は、発生したエラーを示します。それ以外の場合は設定されません。</span><span class="sxs-lookup"><span data-stu-id="8cf24-p103">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of *adStatus* is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>|
|<span data-ttu-id="8cf24-120">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="8cf24-120">*adStatus*</span></span> |<span data-ttu-id="8cf24-121">[EventStatusEnum](eventstatusenum.md)。</span><span class="sxs-lookup"><span data-stu-id="8cf24-121">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="8cf24-122">**WillChangeRecord** が呼び出されたとき、イベントを発生させた操作が成功した場合、このパラメーターは **adStatusOK** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="8cf24-122">When **WillChangeRecord** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful.</span></span> <span data-ttu-id="8cf24-123">保留中の操作の取り消しをこのイベントが要求できない場合、このパラメーターは **adStatusCantDeny** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="8cf24-123">It is set to **adStatusCantDeny** if this event cannot request cancellation of the pending operation.</span></span> <br/><br/><span data-ttu-id="8cf24-124">**RecordChangeComplete** が呼び出されたとき、このパラメーターは、イベントを発生させた操作が成功した場合は **adStatusOK** 、失敗した場合は **adStatusErrorsOccurred** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="8cf24-124">When **RecordChangeComplete** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful, or to **adStatusErrorsOccurred** if the operation failed.</span></span> <br/><br/><span data-ttu-id="8cf24-125">**WillChangeRecord** から制御が戻る前に、このイベントを発生させた操作の取り消しを要求するには、このパラメーターを **adStatusCancel** に設定し、後続の通知が行われないようにするには、このパラメーターを adStatusUnwantedEvent に設定します。</span><span class="sxs-lookup"><span data-stu-id="8cf24-125">Before **WillChangeRecord** returns, set this parameter to **adStatusCancel** to request cancellation of the operation that caused this event or set this parameter to adStatusUnwantedEvent to prevent subsequent notications.</span></span> <br/><br/><span data-ttu-id="8cf24-126">**RecordChangeComplete** から制御が戻る前に後続の通知が行われるのを防ぐには、このパラメーターを **adStatusUnwantedEvent** に設定します。</span><span class="sxs-lookup"><span data-stu-id="8cf24-126">Before **RecordChangeComplete** returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>|
|<span data-ttu-id="8cf24-127">*pRecordset*</span><span class="sxs-lookup"><span data-stu-id="8cf24-127">*pRecordset*</span></span> |<span data-ttu-id="8cf24-p105">**Recordset** オブジェクト。このイベントが発生した **Recordset** オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="8cf24-p105">A **Recordset** object. The **Recordset** for which this event occurred.</span></span>|

## <a name="remarks"></a><span data-ttu-id="8cf24-130">解説</span><span class="sxs-lookup"><span data-stu-id="8cf24-130">Remarks</span></span>

<span data-ttu-id="8cf24-131">**WillChangeRecord** イベントまたは **RecordChangeComplete** イベントは、 **Recordset** の [Update](update-method-ado.md)、[Delete](delete-method-ado-recordset.md)、[CancelUpdate](cancelupdate-method-ado.md)、[AddNew](addnew-method-ado.md)、[UpdateBatch](updatebatch-method-ado.md)、および [CancelBatch](cancelbatch-method-ado.md) の各操作によって、行のフィールドが最初に変更されたときに発生します。</span><span class="sxs-lookup"><span data-stu-id="8cf24-131">A **WillChangeRecord** or **RecordChangeComplete** event may occur for the first changed field in a row due to the following **Recordset** operations: [Update](update-method-ado.md), [Delete](delete-method-ado-recordset.md), [CancelUpdate](cancelupdate-method-ado.md), [AddNew](addnew-method-ado.md), [UpdateBatch](updatebatch-method-ado.md), and [CancelBatch](cancelbatch-method-ado.md).</span></span> <span data-ttu-id="8cf24-132">**Recordset**の[CursorType](cursortype-property-ado.md)の値は、どのような操作が発生するイベントが発生するを決定します。</span><span class="sxs-lookup"><span data-stu-id="8cf24-132">The value of the **Recordset** [CursorType](cursortype-property-ado.md) determines which operations cause the events to occur.</span></span>

<span data-ttu-id="8cf24-133">**WillChangeRecord**イベントの実行中には、**レコード セット**の[Filter](filter-property-ado.md)プロパティは**adFilterAffectedRecords**に設定されます。</span><span class="sxs-lookup"><span data-stu-id="8cf24-133">During the **WillChangeRecord** event, the **Recordset** [Filter](filter-property-ado.md) property is set to **adFilterAffectedRecords**.</span></span> <span data-ttu-id="8cf24-134">イベント処理中は、このプロパティを変更できません。</span><span class="sxs-lookup"><span data-stu-id="8cf24-134">You cannot change this property while processing the event.</span></span>

<span data-ttu-id="8cf24-135">adReason パラメーターを含むすべてのイベントのイベント通知を完全に停止するには、考えられる adReason 値ごとに adStatus パラメーターを adStatusUnwantedEvent に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8cf24-135">You must set the adStatus parameter to adStatusUnwantedEvent for each possible adReason value in order to completely stop event noticiation for any event that includes an adReason parameter.</span></span>

