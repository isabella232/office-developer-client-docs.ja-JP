---
title: ConnectComplete イベントと Disconnect イベント (ADO)
TOCTitle: ConnectComplete and Disconnect Events (ADO)
ms:assetid: 8ecb080b-7fc9-7565-25bd-bd57b983750d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249629(v=office.15)
ms:contentKeyID: 48546293
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 731879abf181f64c24b1012e45ea23435f965574
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478858"
---
# <a name="connectcomplete-and-disconnect-events-ado"></a><span data-ttu-id="fe6dd-102">ConnectComplete イベントと Disconnect イベント (ADO)</span><span class="sxs-lookup"><span data-stu-id="fe6dd-102">ConnectComplete and Disconnect Events (ADO)</span></span>


<span data-ttu-id="fe6dd-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="fe6dd-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="fe6dd-104">**ConnectComplete**イベントは、接続が*開始*した後に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="fe6dd-104">The **ConnectComplete** event is called after a connection *starts*.</span></span> <span data-ttu-id="fe6dd-105">**切断**イベントは、接続が*終了*した後に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="fe6dd-105">The **Disconnect** event is called after a connection *ends*.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe6dd-106">構文</span><span class="sxs-lookup"><span data-stu-id="fe6dd-106">Syntax</span></span>

<span data-ttu-id="fe6dd-107">ConnectComplete*pError*、 *adStatus*、 *pConnection*</span><span class="sxs-lookup"><span data-stu-id="fe6dd-107">ConnectComplete*pError*, *adStatus*, *pConnection*</span></span>

<span data-ttu-id="fe6dd-108">*AdStatus*、 *pConnection*を切断します。</span><span class="sxs-lookup"><span data-stu-id="fe6dd-108">Disconnect*adStatus*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="fe6dd-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="fe6dd-109">Parameters</span></span>

  - <span data-ttu-id="fe6dd-110">*pError*</span><span class="sxs-lookup"><span data-stu-id="fe6dd-110">*pError*</span></span>

  - <span data-ttu-id="fe6dd-p102">[Error](error-object-ado.md) オブジェクトです。 *adStatus* の値が **adStatusErrorsOccurred** の場合は、発生したエラーを示します。それ以外の場合は設定されません。</span><span class="sxs-lookup"><span data-stu-id="fe6dd-p102">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of *adStatus* is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>

  - <span data-ttu-id="fe6dd-113">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="fe6dd-113">*adStatus*</span></span>

  - [<span data-ttu-id="fe6dd-114">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="fe6dd-114">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="fe6dd-115">**WillConnect** イベントが保留中の接続の取り消しを要求しているときに **ConnectComplete** が呼び出されると、このパラメーターは **adStatusCancel** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="fe6dd-115">When **ConnectComplete** is called, this parameter is set to **adStatusCancel** if a **WillConnect** event has requested cancellation of the pending connection.</span></span>
    
    <span data-ttu-id="fe6dd-p103">いずれかのイベントから制御が戻る前に後続の通知が行われるのを防ぐには、このパラメーターを **adStatusUnwantedEvent** に設定します。ただし、 [Connection](connection-object-ado.md) をいったん閉じてから再び開くと、これらのイベントが再度発生します。</span><span class="sxs-lookup"><span data-stu-id="fe6dd-p103">Before either event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications. However, closing and reopening the [Connection](connection-object-ado.md) causes these events to occur again.</span></span>

  - <span data-ttu-id="fe6dd-118">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="fe6dd-118">*pConnection*</span></span>

  - <span data-ttu-id="fe6dd-119">このイベントが適用される **Connection** オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="fe6dd-119">The **Connection** object for which this event applies.</span></span>
