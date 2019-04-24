---
title: connectcomplete イベントと Disconnect イベント (ADO)
TOCTitle: ConnectComplete and Disconnect events (ADO)
ms:assetid: 8ecb080b-7fc9-7565-25bd-bd57b983750d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249629(v=office.15)
ms:contentKeyID: 48546293
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e1e1d4487eb113c25e25ce6b9de051e33a4536b3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295990"
---
# <a name="connectcomplete-and-disconnect-events-ado"></a><span data-ttu-id="deeb7-102">connectcomplete イベントと Disconnect イベント (ADO)</span><span class="sxs-lookup"><span data-stu-id="deeb7-102">ConnectComplete and Disconnect events (ADO)</span></span>

<span data-ttu-id="deeb7-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="deeb7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="deeb7-104">**connectcomplete**イベントは、接続が*開始*された後に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="deeb7-104">The **ConnectComplete** event is called after a connection *starts*.</span></span> <span data-ttu-id="deeb7-105">**Disconnect**イベントは、接続が*終了*した後に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="deeb7-105">The **Disconnect** event is called after a connection *ends*.</span></span>

## <a name="syntax"></a><span data-ttu-id="deeb7-106">構文</span><span class="sxs-lookup"><span data-stu-id="deeb7-106">Syntax</span></span>

<span data-ttu-id="deeb7-107">connectcomplete\*\* の手順、 *adstatus*、 *pconnection*</span><span class="sxs-lookup"><span data-stu-id="deeb7-107">ConnectComplete*pError*, *adStatus*, *pConnection*</span></span>

<span data-ttu-id="deeb7-108">*adstatus*、 *pconnection*の切断</span><span class="sxs-lookup"><span data-stu-id="deeb7-108">Disconnect*adStatus*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="deeb7-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="deeb7-109">Parameters</span></span>

|<span data-ttu-id="deeb7-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="deeb7-110">Parameter</span></span>|<span data-ttu-id="deeb7-111">説明</span><span class="sxs-lookup"><span data-stu-id="deeb7-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="deeb7-112">*の場合*</span><span class="sxs-lookup"><span data-stu-id="deeb7-112">*pError*</span></span> |<span data-ttu-id="deeb7-p102">[Error](error-object-ado.md) オブジェクトです。 *adStatus* の値が **adStatusErrorsOccurred** の場合は、発生したエラーを示します。それ以外の場合は設定されません。</span><span class="sxs-lookup"><span data-stu-id="deeb7-p102">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of *adStatus* is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>|
|<span data-ttu-id="deeb7-115">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="deeb7-115">*adStatus*</span></span> |<span data-ttu-id="deeb7-116">[eventstatusenum](eventstatusenum.md)。</span><span class="sxs-lookup"><span data-stu-id="deeb7-116">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="deeb7-117">**WillConnect** イベントが保留中の接続の取り消しを要求しているときに **ConnectComplete** が呼び出されると、このパラメーターは **adStatusCancel** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="deeb7-117">When **ConnectComplete** is called, this parameter is set to **adStatusCancel** if a **WillConnect** event has requested cancellation of the pending connection.</span></span><br/><br/><span data-ttu-id="deeb7-p104">いずれかのイベントから制御が戻る前に後続の通知が行われるのを防ぐには、このパラメーターを **adStatusUnwantedEvent** に設定します。ただし、 [Connection](connection-object-ado.md) をいったん閉じてから再び開くと、これらのイベントが再度発生します。</span><span class="sxs-lookup"><span data-stu-id="deeb7-p104">Before either event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications. However, closing and reopening the [Connection](connection-object-ado.md) causes these events to occur again.</span></span>|
|<span data-ttu-id="deeb7-120">*pconnection*</span><span class="sxs-lookup"><span data-stu-id="deeb7-120">*pConnection*</span></span> |<span data-ttu-id="deeb7-121">このイベントが適用される **Connection** オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="deeb7-121">The **Connection** object for which this event applies.</span></span>|

