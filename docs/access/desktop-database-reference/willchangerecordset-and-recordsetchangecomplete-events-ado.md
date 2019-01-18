---
title: WillChangeRecordset イベントと RecordsetChangeComplete イベント (ADO)
TOCTitle: WillChangeRecordset and RecordsetChangeComplete events (ADO)
ms:assetid: 2cec4cf9-a4e9-c386-5202-04e86f4cf8ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249068(v=office.15)
ms:contentKeyID: 48543963
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: bfb304f41ada88e1b0546aaa4a54240b931017cd
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701515"
---
# <a name="willchangerecordset-and-recordsetchangecomplete-events-ado"></a><span data-ttu-id="8b9bf-102">WillChangeRecordset イベントと RecordsetChangeComplete イベント (ADO)</span><span class="sxs-lookup"><span data-stu-id="8b9bf-102">WillChangeRecordset and RecordsetChangeComplete events (ADO)</span></span>

<span data-ttu-id="8b9bf-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="8b9bf-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8b9bf-p101">**WillChangeRecordset** イベントは、保留中の操作で [Recordset](recordset-object-ado.md) が変更される前に呼び出されます。 **RecordsetChangeComplete** イベントは、 **Recordset** が変更された後に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="8b9bf-p101">The **WillChangeRecordset** event is called before a pending operation changes the [Recordset](recordset-object-ado.md). The **RecordsetChangeComplete** event is called after the **Recordset** has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b9bf-106">構文</span><span class="sxs-lookup"><span data-stu-id="8b9bf-106">Syntax</span></span>

<span data-ttu-id="8b9bf-107">WillChangeRecordset*adReason*、 *adStatus*、 *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="8b9bf-107">WillChangeRecordset*adReason*, *adStatus*, *pRecordset*</span></span>

<span data-ttu-id="8b9bf-108">RecordsetChangeComplete*adReason*、 *pError*、 *adStatus*、 *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="8b9bf-108">RecordsetChangeComplete*adReason*, *pError*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="8b9bf-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8b9bf-109">Parameters</span></span>

|<span data-ttu-id="8b9bf-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8b9bf-110">Parameter</span></span>|<span data-ttu-id="8b9bf-111">説明</span><span class="sxs-lookup"><span data-stu-id="8b9bf-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="8b9bf-112">*adReason*</span><span class="sxs-lookup"><span data-stu-id="8b9bf-112">*adReason*</span></span> |<span data-ttu-id="8b9bf-p102">このイベントの原因を示す [EventReasonEnum](eventreasonenum.md) 値です。値は **adRsnRequery** 、 **adRsnResynch** 、 **adRsnClose** 、 **adRsnOpen** です。</span><span class="sxs-lookup"><span data-stu-id="8b9bf-p102">An [EventReasonEnum](eventreasonenum.md) value that specifies the reason for this event. Its value can be **adRsnRequery**, **adRsnResynch**, **adRsnClose**, **adRsnOpen**.</span></span>|
|<span data-ttu-id="8b9bf-115">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="8b9bf-115">*adStatus*</span></span> |<span data-ttu-id="8b9bf-116">[EventStatusEnum](eventstatusenum.md)。</span><span class="sxs-lookup"><span data-stu-id="8b9bf-116">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="8b9bf-117">**WillChangeRecordset** が呼び出されたとき、イベントを発生させた操作が成功した場合、このパラメーターは **adStatusOK** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="8b9bf-117">When **WillChangeRecordset** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful.</span></span> <span data-ttu-id="8b9bf-118">保留中の操作の取り消しをこのイベントが要求できない場合、このパラメーターは **adStatusCantDeny** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="8b9bf-118">It is set to **adStatusCantDeny** if this event cannot request cancellation of the pending operation.</span></span> <br/><br/><span data-ttu-id="8b9bf-119">**RecordsetChangeComplete** が呼び出されたとき、このパラメーターは、イベントを発生させた操作が成功した場合は **adStatusOK** 、操作が失敗した場合は **adStatusErrorsOccurred** 、以前に受け付けた **WillChangeRecordset** イベントに関連付けられた操作が取り消された場合は **adStatusCancel** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="8b9bf-119">When **RecordsetChangeComplete** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful, **adStatusErrorsOccurred** if the operation failed, or **adStatusCancel** if the operation associated with the previously accepted **WillChangeRecordset** event has been canceled.</span></span> <br/><br/><span data-ttu-id="8b9bf-120">**WillChangeRecordset** から制御が戻る前に、保留中の操作の取り消しを要求するには、このパラメーターを **adStatusCancel** に設定し、後続の通知が行われないようにするには、このパラメーターを adStatusUnwantedEvent に設定します。</span><span class="sxs-lookup"><span data-stu-id="8b9bf-120">Before **WillChangeRecordset** returns, set this parameter to **adStatusCancel** to request cancellation of the pending operation or set this parameter to adStatusUnwantedEvent to prevent subsequent notifications.</span></span> <br/><br/><span data-ttu-id="8b9bf-121">**WillChangeRecordset** または **RecordsetChangeComplete** から制御が戻る前に後続の通知が行われないようにするには、このパラメーターを **adStatusUnwantedEvent** に設定します。</span><span class="sxs-lookup"><span data-stu-id="8b9bf-121">Before **WillChangeRecordset** or **RecordsetChangeComplete** returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>|
|<span data-ttu-id="8b9bf-122">*pError*</span><span class="sxs-lookup"><span data-stu-id="8b9bf-122">*pError*</span></span> |<span data-ttu-id="8b9bf-p104">[Error](error-object-ado.md) オブジェクトです。 *adStatus* の値が **adStatusErrorsOccurred** の場合は、発生したエラーを示します。それ以外の場合は設定されません。</span><span class="sxs-lookup"><span data-stu-id="8b9bf-p104">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of *adStatus* is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>|
|<span data-ttu-id="8b9bf-125">*pRecordset*</span><span class="sxs-lookup"><span data-stu-id="8b9bf-125">*pRecordset*</span></span> |<span data-ttu-id="8b9bf-p105">**Recordset** オブジェクト。このイベントが発生した **Recordset** オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="8b9bf-p105">A **Recordset** object. The **Recordset** for which this event occurred.</span></span>|

## <a name="remarks"></a><span data-ttu-id="8b9bf-128">解説</span><span class="sxs-lookup"><span data-stu-id="8b9bf-128">Remarks</span></span>

<span data-ttu-id="8b9bf-129">**WillChangeRecordset**または**RecordsetChangeComplete**イベントは、**レコード セット**の[クエリを再実行](requery-method-ado.md)] または [[開く](open-method-ado-recordset.md)メソッドのため発生します。</span><span class="sxs-lookup"><span data-stu-id="8b9bf-129">A **WillChangeRecordset** or **RecordsetChangeComplete** event may occur due to the **Recordset** [Requery](requery-method-ado.md) or [Open](open-method-ado-recordset.md) methods.</span></span>

<span data-ttu-id="8b9bf-p106">プロバイダーがブックマークをサポートしていない場合、プロバイダーから新しい行が取得されるたびに **RecordsetChange** イベントの通知が発生します。このイベントの発生頻度は、 **RecordsetCacheSize** プロパティによって決まります。</span><span class="sxs-lookup"><span data-stu-id="8b9bf-p106">If the provider does not support bookmarks, a **RecordsetChange** event notification occurs each time new rows are retrieved from the provider. The frequency of this event depends on the **RecordsetCacheSize** property.</span></span>

<span data-ttu-id="8b9bf-132">**adReason** パラメーターを含むすべてのイベントのイベント通知を完全に停止するには、考えられる **adReason** 値ごとに **adStatus** パラメーターを **adStatusUnwantedEvent** に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b9bf-132">You must set the **adStatus** parameter to **adStatusUnwantedEvent** for each possible **adReason** value in order to completely stop event notification for any event that includes an **adReason** parameter.</span></span>

