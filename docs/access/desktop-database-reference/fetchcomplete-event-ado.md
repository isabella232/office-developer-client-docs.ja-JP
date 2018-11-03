---
title: FetchComplete イベント (ADO)
TOCTitle: FetchComplete event (ADO)
ms:assetid: 4863d5b5-7d77-bdef-c511-f85c9e6dec9d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249224(v=office.15)
ms:contentKeyID: 48544621
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: edb2eefd36aea9f037ea4ad6afc51e0da18b76db
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945636"
---
# <a name="fetchcomplete-event-ado"></a><span data-ttu-id="c2418-102">FetchComplete イベント (ADO)</span><span class="sxs-lookup"><span data-stu-id="c2418-102">FetchComplete event (ADO)</span></span>


<span data-ttu-id="c2418-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="c2418-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="c2418-104">**FetchComplete** イベントは、長い非同期操作ですべてのレコードが [Recordset](recordset-object-ado.md) に取得された後に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="c2418-104">The **FetchComplete** event is called after all the records in a lengthy asynchronous operation have been retrieved into the [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c2418-105">構文</span><span class="sxs-lookup"><span data-stu-id="c2418-105">Syntax</span></span>

<span data-ttu-id="c2418-106">FetchComplete*pError*、 *adStatus*、 *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="c2418-106">FetchComplete*pError*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="c2418-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c2418-107">Parameters</span></span>

- <span data-ttu-id="c2418-108">*pError*</span><span class="sxs-lookup"><span data-stu-id="c2418-108">*pError*</span></span>

  - <span data-ttu-id="c2418-p101">[Error](error-object-ado.md) オブジェクトです。 **adStatus** の値が **adStatusErrorsOccurred** の場合は、発生したエラーを示します。それ以外の場合は設定されません。</span><span class="sxs-lookup"><span data-stu-id="c2418-p101">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of **adStatus** is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>

- <span data-ttu-id="c2418-111">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="c2418-111">*adStatus*</span></span>

  - [<span data-ttu-id="c2418-112">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="c2418-112">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="c2418-113">このイベントから制御が戻る前に後続の通知が行われるのを防ぐには、このパラメーターを **adStatusUnwantedEvent** に設定します。</span><span class="sxs-lookup"><span data-stu-id="c2418-113">Before this event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>

- <span data-ttu-id="c2418-114">*pRecordset*</span><span class="sxs-lookup"><span data-stu-id="c2418-114">*pRecordset*</span></span>

  - <span data-ttu-id="c2418-p102">**Recordset** オブジェクト。レコードを取得したオブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="c2418-p102">A **Recordset** object. The object for which the records were retrieved.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2418-117">解説</span><span class="sxs-lookup"><span data-stu-id="c2418-117">Remarks</span></span>

<span data-ttu-id="c2418-118">Microsoft Visual Basic で **FetchComplete** を使用するには、Visual Basic 6.0 以降が必要です。</span><span class="sxs-lookup"><span data-stu-id="c2418-118">To use **FetchComplete** with Microsoft Visual Basic, Visual Basic 6.0 or later is required.</span></span>

