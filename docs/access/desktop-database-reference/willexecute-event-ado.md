---
title: WillExecute イベント (ADO)
TOCTitle: WillExecute event (ADO)
ms:assetid: 9f516bfd-246d-9817-4ca3-64598ab466f7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249732(v=office.15)
ms:contentKeyID: 48546686
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7fe15604d0160afcbde5fdf02eaa6a7831da874b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718568"
---
# <a name="willexecute-event-ado"></a><span data-ttu-id="3bfab-102">WillExecute イベント (ADO)</span><span class="sxs-lookup"><span data-stu-id="3bfab-102">WillExecute event (ADO)</span></span>

<span data-ttu-id="3bfab-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="3bfab-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3bfab-104">**WillExecute** イベントは、保留中のコマンドが接続に対して実行される直前に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="3bfab-104">The **WillExecute** event is called just before a pending command executes on a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bfab-105">構文</span><span class="sxs-lookup"><span data-stu-id="3bfab-105">Syntax</span></span>

<span data-ttu-id="3bfab-106">アクティビ ティー*ソース*、 *CursorType*、 *LockType*、*オプション*、 *adStatus*、 *pCommand*、 *pRecordset*、 *pConnection*</span><span class="sxs-lookup"><span data-stu-id="3bfab-106">WillExecute*Source*, *CursorType*, *LockType*, *Options*, *adStatus*, *pCommand*, *pRecordset*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="3bfab-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="3bfab-107">Parameters</span></span>

|<span data-ttu-id="3bfab-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="3bfab-108">Parameter</span></span>|<span data-ttu-id="3bfab-109">説明</span><span class="sxs-lookup"><span data-stu-id="3bfab-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="3bfab-110">*Source*</span><span class="sxs-lookup"><span data-stu-id="3bfab-110">*Source*</span></span> |<span data-ttu-id="3bfab-111">SQL コマンドまたはストアド プロシージャ名が格納された文字列型 ( **String** ) の値です。</span><span class="sxs-lookup"><span data-stu-id="3bfab-111">A **String** that contains an SQL command or a stored procedure name.</span></span>|
|<span data-ttu-id="3bfab-112">*カーソル。*</span><span class="sxs-lookup"><span data-stu-id="3bfab-112">*CursorType*</span></span> |<span data-ttu-id="3bfab-113">開く対象の [Recordset](cursortypeenum.md) のカーソルの種類が格納された **CursorTypeEnum** です。</span><span class="sxs-lookup"><span data-stu-id="3bfab-113">A [CursorTypeEnum](cursortypeenum.md) that contains the type of cursor for the **Recordset** that will be opened.</span></span> <span data-ttu-id="3bfab-114">このパラメーターを使用、**レコード セット**を[開く](open-method-ado-recordset.md)操作中にカーソルを任意の種類に変更できます。</span><span class="sxs-lookup"><span data-stu-id="3bfab-114">With this parameter, you can change the cursor to any type during a **Recordset** [Open](open-method-ado-recordset.md) operation.</span></span> <span data-ttu-id="3bfab-115">*CursorType*は、他の操作の無視されます。</span><span class="sxs-lookup"><span data-stu-id="3bfab-115">*CursorType* will be ignored for any other operation.</span></span>|
|<span data-ttu-id="3bfab-116">*ロック。*</span><span class="sxs-lookup"><span data-stu-id="3bfab-116">*LockType*</span></span> |<span data-ttu-id="3bfab-117">開く対象の [Recordset](locktypeenum.md) のロックの種類が格納された **LockTypeEnum** です。</span><span class="sxs-lookup"><span data-stu-id="3bfab-117">A [LockTypeEnum](locktypeenum.md) that contains the lock type for the **Recordset** that will be opened.</span></span> <span data-ttu-id="3bfab-118">このパラメーターを使用すると、 **Recordset** の **Open** 操作中にロックを任意の種類に変更できます。</span><span class="sxs-lookup"><span data-stu-id="3bfab-118">With this parameter, you can change the lock to any type during a **Recordset** **Open** operation.</span></span> <span data-ttu-id="3bfab-119">*LockType*は、他のすべての操作に対しては無視されます。</span><span class="sxs-lookup"><span data-stu-id="3bfab-119">*LockType* will be ignored for any other operation.</span></span>|
|<span data-ttu-id="3bfab-120">*Options*</span><span class="sxs-lookup"><span data-stu-id="3bfab-120">*Options*</span></span> |<span data-ttu-id="3bfab-121">コマンドを実行するとき、または **Recordset** を開くときに使われるオプションを示す長整数型 ( **Long** ) の値です。</span><span class="sxs-lookup"><span data-stu-id="3bfab-121">A **Long** value that indicates options that can be used to execute the command or open the **Recordset**.</span></span>|
|<span data-ttu-id="3bfab-122">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="3bfab-122">*adStatus*</span></span> |<span data-ttu-id="3bfab-123">[EventStatusEnum](eventstatusenum.md)。</span><span class="sxs-lookup"><span data-stu-id="3bfab-123">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="3bfab-124">このイベントから制御が戻る前に後続の通知が行われるのを防ぐには、このパラメーターを **adStatusUnwantedEvent** に設定し、このイベントを発生させた操作の取り消しを要求するには、このパラメーターを **adStatusCancel** に設定します。</span><span class="sxs-lookup"><span data-stu-id="3bfab-124">Before this event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications, or **adStatusCancel** to request cancellation of the operation that caused this event.</span></span>|
|<span data-ttu-id="3bfab-125">*pCommand*</span><span class="sxs-lookup"><span data-stu-id="3bfab-125">*pCommand*</span></span> |<span data-ttu-id="3bfab-126">このイベント通知が適用される [Command](command-object-ado.md) オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="3bfab-126">The [Command](command-object-ado.md) object for which this event notification applies.</span></span>|
|<span data-ttu-id="3bfab-127">*pRecordset*</span><span class="sxs-lookup"><span data-stu-id="3bfab-127">*pRecordset*</span></span> |<span data-ttu-id="3bfab-128">このイベント通知が適用される [Recordset](recordset-object-ado.md) オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="3bfab-128">The [Recordset](recordset-object-ado.md) object for which this event notification applies.</span></span>|
|<span data-ttu-id="3bfab-129">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="3bfab-129">*pConnection*</span></span> |<span data-ttu-id="3bfab-130">このイベント通知が適用される [Connection](connection-object-ado.md) オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="3bfab-130">The [Connection](connection-object-ado.md) object for which this event notification applies.</span></span>|

## <a name="remarks"></a><span data-ttu-id="3bfab-131">解説</span><span class="sxs-lookup"><span data-stu-id="3bfab-131">Remarks</span></span>

<span data-ttu-id="3bfab-132">**アクティビ ティー**イベント発生の理由のため、**接続します**。[実行](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection)するには、**コマンドです**。[実行](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command)、または**レコード セット**。[Open](open-method-ado-recordset.md)メソッド*pConnection*パラメーターは、有効なオブジェクトへの参照、**接続**を常に含む必要があります。</span><span class="sxs-lookup"><span data-stu-id="3bfab-132">A **WillExecute** event may occur due to a **Connection.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection), **Command.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command), or **Recordset.**[Open](open-method-ado-recordset.md) method The *pConnection* parameter should always contain a valid reference to a **Connection** object.</span></span> <span data-ttu-id="3bfab-133">**Connection.Execute**のためのイベントの場合、 *pRecordset*と*pCommand*パラメーターが**Nothing**に設定します。</span><span class="sxs-lookup"><span data-stu-id="3bfab-133">If the event is due to **Connection.Execute**, the *pRecordset* and *pCommand* parameters are set to **Nothing**.</span></span> <span data-ttu-id="3bfab-134">**Recordset.Open**のためのイベントの場合は、 *pRecordset*パラメーターが**レコード セット**オブジェクトを参照し、 *pCommand*パラメーターは**Nothing**に設定します。</span><span class="sxs-lookup"><span data-stu-id="3bfab-134">If the event is due to **Recordset.Open**, the *pRecordset* parameter will reference the **Recordset** object and the *pCommand* parameter is set to **Nothing**.</span></span> <span data-ttu-id="3bfab-135">**Command.Execute**のためのイベントの場合は、 *pCommand*パラメーターは、**コマンド**オブジェクトを参照し、 *pRecordset*パラメーターは**Nothing**に設定します。</span><span class="sxs-lookup"><span data-stu-id="3bfab-135">If the event is due to **Command.Execute**, the *pCommand* parameter will reference the **Command** object and the *pRecordset* parameter is set to **Nothing**.</span></span>

<span data-ttu-id="3bfab-p105">**WillExecute** では、保留中の実行パラメーターを調べたり、編集したりできます。このイベントは、保留中のコマンドを取り消す要求を返すこともあります。</span><span class="sxs-lookup"><span data-stu-id="3bfab-p105">**WillExecute** allows you to examine and modify the pending execution parameters. This event may return a request that the pending command be canceled.</span></span>

