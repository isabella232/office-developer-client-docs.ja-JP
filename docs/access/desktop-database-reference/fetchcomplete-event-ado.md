---
title: FetchComplete イベント (ADO)
TOCTitle: FetchComplete event (ADO)
ms:assetid: 4863d5b5-7d77-bdef-c511-f85c9e6dec9d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249224(v=office.15)
ms:contentKeyID: 48544621
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ed0f93fc8b58d94675377b3263ba60fb692a9a4e
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949493"
---
# <a name="fetchcomplete-event-ado"></a><span data-ttu-id="2dd42-102">FetchComplete イベント (ADO)</span><span class="sxs-lookup"><span data-stu-id="2dd42-102">FetchComplete event (ADO)</span></span>

<span data-ttu-id="2dd42-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="2dd42-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2dd42-104">**FetchComplete** イベントは、長い非同期操作ですべてのレコードが [Recordset](recordset-object-ado.md) に取得された後に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="2dd42-104">The **FetchComplete** event is called after all the records in a lengthy asynchronous operation have been retrieved into the [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2dd42-105">構文</span><span class="sxs-lookup"><span data-stu-id="2dd42-105">Syntax</span></span>

<span data-ttu-id="2dd42-106">FetchComplete*pError*、 *adStatus*、 *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="2dd42-106">FetchComplete*pError*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="2dd42-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2dd42-107">Parameters</span></span>

|<span data-ttu-id="2dd42-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2dd42-108">Parameter</span></span>|<span data-ttu-id="2dd42-109">説明</span><span class="sxs-lookup"><span data-stu-id="2dd42-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="2dd42-110">*pError*</span><span class="sxs-lookup"><span data-stu-id="2dd42-110">*pError*</span></span> |<span data-ttu-id="2dd42-p101">[Error](error-object-ado.md) オブジェクトです。 **adStatus** の値が **adStatusErrorsOccurred** の場合は、発生したエラーを示します。それ以外の場合は設定されません。</span><span class="sxs-lookup"><span data-stu-id="2dd42-p101">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of **adStatus** is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>|
|<span data-ttu-id="2dd42-113">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="2dd42-113">*adStatus*</span></span> |<span data-ttu-id="2dd42-114">[EventStatusEnum](eventstatusenum.md)。</span><span class="sxs-lookup"><span data-stu-id="2dd42-114">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="2dd42-115">このイベントから制御が戻る前に後続の通知が行われるのを防ぐには、このパラメーターを **adStatusUnwantedEvent** に設定します。</span><span class="sxs-lookup"><span data-stu-id="2dd42-115">Before this event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>|
|<span data-ttu-id="2dd42-116">*pRecordset*</span><span class="sxs-lookup"><span data-stu-id="2dd42-116">*pRecordset*</span></span> |<span data-ttu-id="2dd42-p103">**Recordset** オブジェクト。レコードを取得したオブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="2dd42-p103">A **Recordset** object. The object for which the records were retrieved.</span></span>|

## <a name="remarks"></a><span data-ttu-id="2dd42-119">解説</span><span class="sxs-lookup"><span data-stu-id="2dd42-119">Remarks</span></span>

<span data-ttu-id="2dd42-120">Microsoft Visual Basic で **FetchComplete** を使用するには、Visual Basic 6.0 以降が必要です。</span><span class="sxs-lookup"><span data-stu-id="2dd42-120">To use **FetchComplete** with Microsoft Visual Basic, Visual Basic 6.0 or later is required.</span></span>

