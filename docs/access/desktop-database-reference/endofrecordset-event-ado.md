---
title: EndOfRecordset イベント (ADO)
TOCTitle: EndOfRecordset event (ADO)
ms:assetid: 8995b851-dff6-2525-1d62-a2cfb4f95393
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249603(v=office.15)
ms:contentKeyID: 48546167
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 89ca397c4e95dd6f18de41862e9383f77fe14aa8
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928839"
---
# <a name="endofrecordset-event-ado"></a><span data-ttu-id="89445-102">EndOfRecordset イベント (ADO)</span><span class="sxs-lookup"><span data-stu-id="89445-102">EndOfRecordset event (ADO)</span></span>


<span data-ttu-id="89445-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="89445-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="89445-104">**EndOfRecordset** イベントは、 [Recordset](recordset-object-ado.md) の末尾を越える行に移動しようとすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="89445-104">The **EndOfRecordset** event is called when there is an attempt to move to a row past the end of the [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="89445-105">構文</span><span class="sxs-lookup"><span data-stu-id="89445-105">Syntax</span></span>

<span data-ttu-id="89445-106">EndOfRecordset*fMoreData*、 *adStatus*、 *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="89445-106">EndOfRecordset*fMoreData*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="89445-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="89445-107">Parameters</span></span>

  - <span data-ttu-id="89445-108">*fMoreData*</span><span class="sxs-lookup"><span data-stu-id="89445-108">*fMoreData*</span></span>

  - <span data-ttu-id="89445-109">A**バリアント\_BOOL**値をバリアント型に設定\_true の場合、複数の行は、**レコード セット**に追加されていることを示します。</span><span class="sxs-lookup"><span data-stu-id="89445-109">A **VARIANT\_BOOL** value that, if set to VARIANT\_TRUE, indicates more rows have been added to the **Recordset**.</span></span>

  - <span data-ttu-id="89445-110">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="89445-110">*adStatus*</span></span>

  - [<span data-ttu-id="89445-111">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="89445-111">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="89445-p101">**EndOfRecordset** が呼び出されたとき、イベントを発生させた操作が成功した場合、このパラメーターは **adStatusOK** に設定されます。イベントを発生させた操作の取り消しをこのイベントが要求できない場合、このパラメーターは **adStatusCantDeny** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="89445-p101">When **EndOfRecordset** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful. It is set to **adStatusCantDeny** if this event cannot request cancellation of the operation that caused this event.</span></span>
    
    <span data-ttu-id="89445-114">**EndOfRecordset** から制御が戻る前に後続の通知が行われるのを防ぐには、このパラメーターを **adStatusUnwantedEvent** に設定します。</span><span class="sxs-lookup"><span data-stu-id="89445-114">Before **EndOfRecordset** returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>

  - <span data-ttu-id="89445-115">*pRecordset*</span><span class="sxs-lookup"><span data-stu-id="89445-115">*pRecordset*</span></span>

  - <span data-ttu-id="89445-p102">**Recordset** オブジェクト。このイベントが発生した **Recordset** オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="89445-p102">A **Recordset** object. The **Recordset** for which this event occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="89445-118">解説</span><span class="sxs-lookup"><span data-stu-id="89445-118">Remarks</span></span>

<span data-ttu-id="89445-119">**EndOfRecordset** イベントは、 [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) 操作が失敗した場合に発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="89445-119">An **EndOfRecordset** event may occur if the [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) operation fails.</span></span>

<span data-ttu-id="89445-120">このイベント ハンドラーは、たとえば **MoveNext** を呼び出して、 **Recordset** オブジェクトの末尾を越えて移動しようとすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="89445-120">This event handler is called when an attempt is made to move past the end of the **Recordset** object, perhaps as a result of calling **MoveNext**.</span></span> <span data-ttu-id="89445-121">ただし、このイベントの中で、データベースからさらにレコードを取得し、それらを **Recordset** の末尾に追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="89445-121">However, while in this event, you could retrieve more records from a database and append them to the end of the **Recordset**.</span></span> <span data-ttu-id="89445-122">その場合は、 *fMoreData*をバリアント型に設定\_true に設定し、 **EndOfRecordset**からの戻り値です。</span><span class="sxs-lookup"><span data-stu-id="89445-122">In that case, set *fMoreData* to VARIANT\_TRUE, and return from **EndOfRecordset**.</span></span> <span data-ttu-id="89445-123">その後で **MoveNext** を再度呼び出して、新たに取得したレコードにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="89445-123">Then call **MoveNext** again to access the newly retrieved records.</span></span>

