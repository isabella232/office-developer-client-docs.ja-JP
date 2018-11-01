---
title: FetchComplete イベント (ADO)
TOCTitle: FetchComplete Event (ADO)
ms:assetid: 4863d5b5-7d77-bdef-c511-f85c9e6dec9d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249224(v=office.15)
ms:contentKeyID: 48544621
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e4b72bb3e05b4ef05358a80faffaa0ee4ce08a80
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882400"
---
# <a name="fetchcomplete-event-ado"></a><span data-ttu-id="979eb-102">FetchComplete イベント (ADO)</span><span class="sxs-lookup"><span data-stu-id="979eb-102">FetchComplete Event (ADO)</span></span>


<span data-ttu-id="979eb-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="979eb-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="979eb-104">**FetchComplete** イベントは、長い非同期操作ですべてのレコードが [Recordset](recordset-object-ado.md) に取得された後に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="979eb-104">The **FetchComplete** event is called after all the records in a lengthy asynchronous operation have been retrieved into the [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="979eb-105">構文</span><span class="sxs-lookup"><span data-stu-id="979eb-105">Syntax</span></span>

<span data-ttu-id="979eb-106">FetchComplete*pError*、 *adStatus*、 *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="979eb-106">FetchComplete*pError*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="979eb-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="979eb-107">Parameters</span></span>

  - <span data-ttu-id="979eb-108">*pError*</span><span class="sxs-lookup"><span data-stu-id="979eb-108">*pError*</span></span>

  - <span data-ttu-id="979eb-p101">[Error](error-object-ado.md) オブジェクトです。 **adStatus** の値が **adStatusErrorsOccurred** の場合は、発生したエラーを示します。それ以外の場合は設定されません。</span><span class="sxs-lookup"><span data-stu-id="979eb-p101">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of **adStatus** is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>

  - <span data-ttu-id="979eb-111">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="979eb-111">*adStatus*</span></span>

  - [<span data-ttu-id="979eb-112">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="979eb-112">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="979eb-113">このイベントから制御が戻る前に後続の通知が行われるのを防ぐには、このパラメーターを **adStatusUnwantedEvent** に設定します。</span><span class="sxs-lookup"><span data-stu-id="979eb-113">Before this event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>

  - <span data-ttu-id="979eb-114">*pRecordset*</span><span class="sxs-lookup"><span data-stu-id="979eb-114">*pRecordset*</span></span>

  - <span data-ttu-id="979eb-p102">**Recordset** オブジェクト。レコードを取得したオブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="979eb-p102">A **Recordset** object. The object for which the records were retrieved.</span></span>

## <a name="remarks"></a><span data-ttu-id="979eb-117">解説</span><span class="sxs-lookup"><span data-stu-id="979eb-117">Remarks</span></span>

<span data-ttu-id="979eb-118">Microsoft Visual Basic で **FetchComplete** を使用するには、Visual Basic 6.0 以降が必要です。</span><span class="sxs-lookup"><span data-stu-id="979eb-118">To use **FetchComplete** with Microsoft Visual Basic, Visual Basic 6.0 or later is required.</span></span>

