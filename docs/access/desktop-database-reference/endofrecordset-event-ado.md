---
title: endofrecordset イベント (ADO)
TOCTitle: EndOfRecordset event (ADO)
ms:assetid: 8995b851-dff6-2525-1d62-a2cfb4f95393
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249603(v=office.15)
ms:contentKeyID: 48546167
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 48e0eb25b443175013a144fafaa433df12c2cc9c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293561"
---
# <a name="endofrecordset-event-ado"></a><span data-ttu-id="74003-102">endofrecordset イベント (ADO)</span><span class="sxs-lookup"><span data-stu-id="74003-102">EndOfRecordset event (ADO)</span></span>

<span data-ttu-id="74003-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="74003-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="74003-104">**EndOfRecordset** イベントは、[Recordset](recordset-object-ado.md) の末尾を越える行に移動しようとすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="74003-104">The **EndOfRecordset** event is called when there is an attempt to move to a row past the end of the [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="74003-105">構文</span><span class="sxs-lookup"><span data-stu-id="74003-105">Syntax</span></span>

<span data-ttu-id="74003-106">endofrecordset*fsupports データ*、 *adstatus*、 *precordset*</span><span class="sxs-lookup"><span data-stu-id="74003-106">EndOfRecordset*fMoreData*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="74003-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74003-107">Parameters</span></span>

|<span data-ttu-id="74003-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74003-108">Parameter</span></span>|<span data-ttu-id="74003-109">説明</span><span class="sxs-lookup"><span data-stu-id="74003-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="74003-110">*fのデータ*</span><span class="sxs-lookup"><span data-stu-id="74003-110">*fMoreData*</span></span> |<span data-ttu-id="74003-111">バリアント型 (variant) の**\_BOOL**値。 variant\_TRUE に設定すると、 **Recordset**に追加された行が多いことを示します。</span><span class="sxs-lookup"><span data-stu-id="74003-111">A **VARIANT\_BOOL** value that, if set to VARIANT\_TRUE, indicates more rows have been added to the **Recordset**.</span></span>|
|<span data-ttu-id="74003-112">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="74003-112">*adStatus*</span></span> |<span data-ttu-id="74003-113">[eventstatusenum](eventstatusenum.md)。</span><span class="sxs-lookup"><span data-stu-id="74003-113">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="74003-114">**EndOfRecordset** が呼び出されたとき、イベントを発生させた操作が成功した場合、このパラメーターは **adStatusOK** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="74003-114">When **EndOfRecordset** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful.</span></span> <span data-ttu-id="74003-115">イベントを発生させた操作の取り消しをこのイベントが要求できない場合、このパラメーターは **adStatusCantDeny** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="74003-115">It is set to **adStatusCantDeny** if this event cannot request cancellation of the operation that caused this event.</span></span><br/><br/><span data-ttu-id="74003-116">**EndOfRecordset** から制御が戻る前に後続の通知が行われるのを防ぐには、このパラメーターを **adStatusUnwantedEvent** に設定します。</span><span class="sxs-lookup"><span data-stu-id="74003-116">Before **EndOfRecordset** returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>|
|<span data-ttu-id="74003-117">*precordset*</span><span class="sxs-lookup"><span data-stu-id="74003-117">*pRecordset*</span></span> | <span data-ttu-id="74003-p102">**Recordset** オブジェクト。このイベントが発生した **Recordset** オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="74003-p102">A **Recordset** object. The **Recordset** for which this event occurred.</span></span>|

## <a name="remarks"></a><span data-ttu-id="74003-120">注釈</span><span class="sxs-lookup"><span data-stu-id="74003-120">Remarks</span></span>

<span data-ttu-id="74003-121">**EndOfRecordset** イベントは、 [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) 操作が失敗した場合に発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="74003-121">An **EndOfRecordset** event may occur if the [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) operation fails.</span></span>

<span data-ttu-id="74003-122">このイベント ハンドラーは、たとえば **MoveNext** を呼び出して、 **Recordset** オブジェクトの末尾を越えて移動しようとすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="74003-122">This event handler is called when an attempt is made to move past the end of the **Recordset** object, perhaps as a result of calling **MoveNext**.</span></span> <span data-ttu-id="74003-123">ただし、このイベントの中で、データベースからさらにレコードを取得し、それらを **Recordset** の末尾に追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="74003-123">However, while in this event, you could retrieve more records from a database and append them to the end of the **Recordset**.</span></span> <span data-ttu-id="74003-124">その場合は、 *ffar データ*をバリアント型\_の TRUE に設定し、 **endofrecordset**から戻ります。</span><span class="sxs-lookup"><span data-stu-id="74003-124">In that case, set *fMoreData* to VARIANT\_TRUE, and return from **EndOfRecordset**.</span></span> <span data-ttu-id="74003-125">その後で **MoveNext** を再度呼び出して、新たに取得したレコードにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="74003-125">Then call **MoveNext** again to access the newly retrieved records.</span></span>

