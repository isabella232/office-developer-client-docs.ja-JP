---
title: ConnectComplete イベントと Disconnect イベント (ADO)
TOCTitle: ConnectComplete and Disconnect events (ADO)
ms:assetid: 8ecb080b-7fc9-7565-25bd-bd57b983750d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249629(v=office.15)
ms:contentKeyID: 48546293
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3ab98e270fd52d656bf722c7f666afbe22d5ea44
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926305"
---
# <a name="connectcomplete-and-disconnect-events-ado"></a><span data-ttu-id="ba352-102">ConnectComplete イベントと Disconnect イベント (ADO)</span><span class="sxs-lookup"><span data-stu-id="ba352-102">ConnectComplete and Disconnect events (ADO)</span></span>


<span data-ttu-id="ba352-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="ba352-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ba352-104">**ConnectComplete**イベントは、接続が*開始*した後に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ba352-104">The **ConnectComplete** event is called after a connection *starts*.</span></span> <span data-ttu-id="ba352-105">**切断**イベントは、接続が*終了*した後に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ba352-105">The **Disconnect** event is called after a connection *ends*.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba352-106">構文</span><span class="sxs-lookup"><span data-stu-id="ba352-106">Syntax</span></span>

<span data-ttu-id="ba352-107">ConnectComplete*pError*、 *adStatus*、 *pConnection*</span><span class="sxs-lookup"><span data-stu-id="ba352-107">ConnectComplete*pError*, *adStatus*, *pConnection*</span></span>

<span data-ttu-id="ba352-108">*AdStatus*、 *pConnection*を切断します。</span><span class="sxs-lookup"><span data-stu-id="ba352-108">Disconnect*adStatus*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="ba352-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ba352-109">Parameters</span></span>

  - <span data-ttu-id="ba352-110">*pError*</span><span class="sxs-lookup"><span data-stu-id="ba352-110">*pError*</span></span>

  - <span data-ttu-id="ba352-p102">[Error](error-object-ado.md) オブジェクトです。 *adStatus* の値が **adStatusErrorsOccurred** の場合は、発生したエラーを示します。それ以外の場合は設定されません。</span><span class="sxs-lookup"><span data-stu-id="ba352-p102">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of *adStatus* is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>

  - <span data-ttu-id="ba352-113">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="ba352-113">*adStatus*</span></span>

  - [<span data-ttu-id="ba352-114">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="ba352-114">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="ba352-115">**WillConnect** イベントが保留中の接続の取り消しを要求しているときに **ConnectComplete** が呼び出されると、このパラメーターは **adStatusCancel** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="ba352-115">When **ConnectComplete** is called, this parameter is set to **adStatusCancel** if a **WillConnect** event has requested cancellation of the pending connection.</span></span>
    
    <span data-ttu-id="ba352-p103">いずれかのイベントから制御が戻る前に後続の通知が行われるのを防ぐには、このパラメーターを **adStatusUnwantedEvent** に設定します。ただし、 [Connection](connection-object-ado.md) をいったん閉じてから再び開くと、これらのイベントが再度発生します。</span><span class="sxs-lookup"><span data-stu-id="ba352-p103">Before either event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications. However, closing and reopening the [Connection](connection-object-ado.md) causes these events to occur again.</span></span>

  - <span data-ttu-id="ba352-118">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="ba352-118">*pConnection*</span></span>

  - <span data-ttu-id="ba352-119">このイベントが適用される **Connection** オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="ba352-119">The **Connection** object for which this event applies.</span></span>

