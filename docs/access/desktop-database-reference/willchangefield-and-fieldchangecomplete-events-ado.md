---
title: changefield イベントと FieldChangeComplete イベント (ADO)
TOCTitle: WillChangeField and FieldChangeComplete events (ADO)
ms:assetid: bc4455a6-2925-33dc-d04f-8ea570e5e370
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249904(v=office.15)
ms:contentKeyID: 48547407
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0fd952cc09f410752f3eb7b5963059f8d6ee7c2c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302486"
---
# <a name="willchangefield-and-fieldchangecomplete-events-ado"></a><span data-ttu-id="ab962-102">changefield イベントと FieldChangeComplete イベント (ADO)</span><span class="sxs-lookup"><span data-stu-id="ab962-102">WillChangeField and FieldChangeComplete events (ADO)</span></span>

<span data-ttu-id="ab962-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="ab962-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ab962-p101">**WillChangeField** イベントは、保留中の操作で [Recordset](field-object-ado.md) 内の 1 つ以上の [Field](recordset-object-ado.md) オブジェクトの値が変更される前に呼び出されます。 **FieldChangeComplete** イベントは、1 つ以上の **Field** オブジェクトの値が変更された後に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ab962-p101">The **WillChangeField** event is called before a pending operation changes the value of one or more [Field](field-object-ado.md) objects in the [Recordset](recordset-object-ado.md). The **FieldChangeComplete** event is called after the value of one or more **Field** objects has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab962-106">構文</span><span class="sxs-lookup"><span data-stu-id="ab962-106">Syntax</span></span>

<span data-ttu-id="ab962-107">changefield*cfields*、 *fields*、 *adstatus*、 *precordset*</span><span class="sxs-lookup"><span data-stu-id="ab962-107">WillChangeField*cFields*, *Fields*, *adStatus*, *pRecordset*</span></span>

<span data-ttu-id="ab962-108">FieldChangeComplete*cfields*、 *fields*、 \*\*、 *adstatus*、 *precordset*</span><span class="sxs-lookup"><span data-stu-id="ab962-108">FieldChangeComplete*cFields*, *Fields*, *pError*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="ab962-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ab962-109">Parameters</span></span>

|<span data-ttu-id="ab962-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ab962-110">Parameter</span></span>|<span data-ttu-id="ab962-111">説明</span><span class="sxs-lookup"><span data-stu-id="ab962-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="ab962-112">*cfields*</span><span class="sxs-lookup"><span data-stu-id="ab962-112">*cFields*</span></span> |<span data-ttu-id="ab962-113">*Fields* 内の **Field** オブジェクトの数を表す長整数型 (**Long**) の値です。</span><span class="sxs-lookup"><span data-stu-id="ab962-113">A **Long** that indicates the number of **Field** objects in *Fields*.</span></span>|
|<span data-ttu-id="ab962-114">*フィールド*</span><span class="sxs-lookup"><span data-stu-id="ab962-114">*Fields*</span></span> |<span data-ttu-id="ab962-115">**WillChangeField** の場合、*Fields* パラメーターは、元の値と共に **Field** オブジェクトが格納されたバリアント型 (**Variant**) の配列です。</span><span class="sxs-lookup"><span data-stu-id="ab962-115">For **WillChangeField**, the *Fields* parameter is an array of **Variants** that contains **Field** objects with the original values.</span></span> <br/><br/><span data-ttu-id="ab962-116">**FieldChangeComplete** の場合、*Fields* パラメーターは、変更後の値と共に **Field** オブジェクトが格納されたバリアント型 (**Variant**) の配列です。</span><span class="sxs-lookup"><span data-stu-id="ab962-116">For **FieldChangeComplete**, the *Fields* parameter is an array of **Variants** that contains **Field** objects with the changed values.</span></span>|
|<span data-ttu-id="ab962-117">*の場合*</span><span class="sxs-lookup"><span data-stu-id="ab962-117">*pError*</span></span> |<span data-ttu-id="ab962-p102">[Error](error-object-ado.md) オブジェクトです。 *adStatus* の値が **adStatusErrorsOccurred** の場合は、発生したエラーを示します。それ以外の場合は設定されません。</span><span class="sxs-lookup"><span data-stu-id="ab962-p102">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of *adStatus* is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>|
|<span data-ttu-id="ab962-120">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="ab962-120">*adStatus*</span></span> |<span data-ttu-id="ab962-121">[eventstatusenum](eventstatusenum.md)。</span><span class="sxs-lookup"><span data-stu-id="ab962-121">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="ab962-122">**WillChangeField** が呼び出されたとき、イベントを発生させた操作が成功した場合、このパラメーターは **adStatusOK** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="ab962-122">When **WillChangeField** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful.</span></span> <span data-ttu-id="ab962-123">保留中の操作の取り消しをこのイベントが要求できない場合、このパラメーターは **adStatusCantDeny** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="ab962-123">It is set to **adStatusCantDeny** if this event cannot request cancellation of the pending operation.</span></span> <br/><br/><span data-ttu-id="ab962-124">**FieldChangeComplete** が呼び出されたとき、このパラメーターは、イベントを発生させた操作が成功した場合は **adStatusOK** 、失敗した場合は **adStatusErrorsOccurred** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="ab962-124">When **FieldChangeComplete** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful, or to **adStatusErrorsOccurred** if the operation failed.</span></span> <br/><br/><span data-ttu-id="ab962-125">**WillChangeField** から制御が戻る前に保留中の操作の取り消しを要求する場合は、このパラメーターを **adStatusCancel** に設定します。</span><span class="sxs-lookup"><span data-stu-id="ab962-125">Before **WillChangeField** returns, set this parameter to **adStatusCancel** to request cancellation of the pending operation.</span></span> <br/><br/><span data-ttu-id="ab962-126">**FieldChangeComplete** から制御が戻る前に後続の通知が行われるのを防ぐには、このパラメーターを **adStatusUnwantedEvent** に設定します。</span><span class="sxs-lookup"><span data-stu-id="ab962-126">Before **FieldChangeComplete** returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>|
|<span data-ttu-id="ab962-127">*precordset*</span><span class="sxs-lookup"><span data-stu-id="ab962-127">*pRecordset*</span></span> |<span data-ttu-id="ab962-p104">**Recordset** オブジェクト。このイベントが発生した **Recordset** オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="ab962-p104">A **Recordset** object. The **Recordset** for which this event occurred.</span></span>|

## <a name="remarks"></a><span data-ttu-id="ab962-130">注釈</span><span class="sxs-lookup"><span data-stu-id="ab962-130">Remarks</span></span>

<span data-ttu-id="ab962-131">**WillChangeField** イベントまたは **FieldChangeComplete** イベントは、[Value](value-property-ado.md) プロパティを設定し、フィールドと値配列パラメーターを指定して [Update](update-method-ado.md) メソッドを呼び出したときに発生します。</span><span class="sxs-lookup"><span data-stu-id="ab962-131">A **WillChangeField** or **FieldChangeComplete** event may occur when setting the [Value](value-property-ado.md) property and calling the [Update](update-method-ado.md) method with field and value array parameters.</span></span>

