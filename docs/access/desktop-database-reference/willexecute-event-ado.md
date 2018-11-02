---
title: WillExecute イベント (ADO)
TOCTitle: WillExecute event (ADO)
ms:assetid: 9f516bfd-246d-9817-4ca3-64598ab466f7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249732(v=office.15)
ms:contentKeyID: 48546686
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5e4025645e5f8b12325ba20497ca6ef2b70175df
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919452"
---
# <a name="willexecute-event-ado"></a><span data-ttu-id="a7421-102">WillExecute イベント (ADO)</span><span class="sxs-lookup"><span data-stu-id="a7421-102">WillExecute event (ADO)</span></span>


<span data-ttu-id="a7421-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="a7421-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="a7421-104">**WillExecute** イベントは、保留中のコマンドが接続に対して実行される直前に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="a7421-104">The **WillExecute** event is called just before a pending command executes on a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7421-105">構文</span><span class="sxs-lookup"><span data-stu-id="a7421-105">Syntax</span></span>

<span data-ttu-id="a7421-106">アクティビ ティー*ソース*、 *CursorType*、 *LockType*、*オプション*、 *adStatus*、 *pCommand*、 *pRecordset*、 *pConnection*</span><span class="sxs-lookup"><span data-stu-id="a7421-106">WillExecute*Source*, *CursorType*, *LockType*, *Options*, *adStatus*, *pCommand*, *pRecordset*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="a7421-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a7421-107">Parameters</span></span>

  - <span data-ttu-id="a7421-108">*Source*</span><span class="sxs-lookup"><span data-stu-id="a7421-108">*Source*</span></span>

  - <span data-ttu-id="a7421-109">SQL コマンドまたはストアド プロシージャ名が格納された文字列型 ( **String** ) の値です。</span><span class="sxs-lookup"><span data-stu-id="a7421-109">A **String** that contains an SQL command or a stored procedure name.</span></span>

  - <span data-ttu-id="a7421-110">*カーソル。*</span><span class="sxs-lookup"><span data-stu-id="a7421-110">*CursorType*</span></span>

  - <span data-ttu-id="a7421-111">開く対象の [Recordset](cursortypeenum.md) のカーソルの種類が格納された **CursorTypeEnum** です。</span><span class="sxs-lookup"><span data-stu-id="a7421-111">A [CursorTypeEnum](cursortypeenum.md) that contains the type of cursor for the **Recordset** that will be opened.</span></span> <span data-ttu-id="a7421-112">このパラメーターを使用、**レコード セット**を[開く](open-method-ado-recordset.md)操作中にカーソルを任意の種類に変更できます。</span><span class="sxs-lookup"><span data-stu-id="a7421-112">With this parameter, you can change the cursor to any type during a **Recordset** [Open](open-method-ado-recordset.md) operation.</span></span> <span data-ttu-id="a7421-113">*CursorType*は、他の操作の無視されます。</span><span class="sxs-lookup"><span data-stu-id="a7421-113">*CursorType* will be ignored for any other operation.</span></span>

  - <span data-ttu-id="a7421-114">*ロック。*</span><span class="sxs-lookup"><span data-stu-id="a7421-114">*LockType*</span></span>

  - <span data-ttu-id="a7421-115">開く対象の [Recordset](locktypeenum.md) のロックの種類が格納された **LockTypeEnum** です。</span><span class="sxs-lookup"><span data-stu-id="a7421-115">A [LockTypeEnum](locktypeenum.md) that contains the lock type for the **Recordset** that will be opened.</span></span> <span data-ttu-id="a7421-116">このパラメーターを使用すると、 **Recordset** の **Open** 操作中にロックを任意の種類に変更できます。</span><span class="sxs-lookup"><span data-stu-id="a7421-116">With this parameter, you can change the lock to any type during a **Recordset** **Open** operation.</span></span> <span data-ttu-id="a7421-117">*LockType*は、他のすべての操作に対しては無視されます。</span><span class="sxs-lookup"><span data-stu-id="a7421-117">*LockType* will be ignored for any other operation.</span></span>

  - <span data-ttu-id="a7421-118">*Options*</span><span class="sxs-lookup"><span data-stu-id="a7421-118">*Options*</span></span>

  - <span data-ttu-id="a7421-119">コマンドを実行するとき、または **Recordset** を開くときに使われるオプションを示す長整数型 ( **Long** ) の値です。</span><span class="sxs-lookup"><span data-stu-id="a7421-119">A **Long** value that indicates options that can be used to execute the command or open the **Recordset**.</span></span>

  - <span data-ttu-id="a7421-120">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="a7421-120">*adStatus*</span></span>

  - [<span data-ttu-id="a7421-121">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="a7421-121">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="a7421-122">このイベントから制御が戻る前に後続の通知が行われるのを防ぐには、このパラメーターを **adStatusUnwantedEvent** に設定し、このイベントを発生させた操作の取り消しを要求するには、このパラメーターを **adStatusCancel** に設定します。</span><span class="sxs-lookup"><span data-stu-id="a7421-122">Before this event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications, or **adStatusCancel** to request cancellation of the operation that caused this event.</span></span>

  - <span data-ttu-id="a7421-123">*pCommand*</span><span class="sxs-lookup"><span data-stu-id="a7421-123">*pCommand*</span></span>

  - <span data-ttu-id="a7421-124">このイベント通知が適用される [Command](command-object-ado.md) オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="a7421-124">The [Command](command-object-ado.md) object for which this event notification applies.</span></span>

  - <span data-ttu-id="a7421-125">*pRecordset*</span><span class="sxs-lookup"><span data-stu-id="a7421-125">*pRecordset*</span></span>

  - <span data-ttu-id="a7421-126">このイベント通知が適用される [Recordset](recordset-object-ado.md) オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="a7421-126">The [Recordset](recordset-object-ado.md) object for which this event notification applies.</span></span>

  - <span data-ttu-id="a7421-127">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="a7421-127">*pConnection*</span></span>

  - <span data-ttu-id="a7421-128">このイベント通知が適用される [Connection](connection-object-ado.md) オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="a7421-128">The [Connection](connection-object-ado.md) object for which this event notification applies.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7421-129">解説</span><span class="sxs-lookup"><span data-stu-id="a7421-129">Remarks</span></span>

<span data-ttu-id="a7421-130">**アクティビ ティー**イベント発生の理由のため、**接続します**。[実行](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection)するには、**コマンドです**。[実行](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command)、または**レコード セット**。[Open](open-method-ado-recordset.md)メソッド*pConnection*パラメーターは、有効なオブジェクトへの参照、**接続**を常に含む必要があります。</span><span class="sxs-lookup"><span data-stu-id="a7421-130">A **WillExecute** event may occur due to a **Connection.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection), **Command.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command), or **Recordset.**[Open](open-method-ado-recordset.md) method The *pConnection* parameter should always contain a valid reference to a **Connection** object.</span></span> <span data-ttu-id="a7421-131">**Connection.Execute**のためのイベントの場合、 *pRecordset*と*pCommand*パラメーターが**Nothing**に設定します。</span><span class="sxs-lookup"><span data-stu-id="a7421-131">If the event is due to **Connection.Execute**, the *pRecordset* and *pCommand* parameters are set to **Nothing**.</span></span> <span data-ttu-id="a7421-132">**Recordset.Open**のためのイベントの場合は、 *pRecordset*パラメーターが**レコード セット**オブジェクトを参照し、 *pCommand*パラメーターは**Nothing**に設定します。</span><span class="sxs-lookup"><span data-stu-id="a7421-132">If the event is due to **Recordset.Open**, the *pRecordset* parameter will reference the **Recordset** object and the *pCommand* parameter is set to **Nothing**.</span></span> <span data-ttu-id="a7421-133">**Command.Execute**のためのイベントの場合は、 *pCommand*パラメーターは、**コマンド**オブジェクトを参照し、 *pRecordset*パラメーターは**Nothing**に設定します。</span><span class="sxs-lookup"><span data-stu-id="a7421-133">If the event is due to **Command.Execute**, the *pCommand* parameter will reference the **Command** object and the *pRecordset* parameter is set to **Nothing**.</span></span>

<span data-ttu-id="a7421-p104">**WillExecute** では、保留中の実行パラメーターを調べたり、編集したりできます。このイベントは、保留中のコマンドを取り消す要求を返すこともあります。</span><span class="sxs-lookup"><span data-stu-id="a7421-p104">**WillExecute** allows you to examine and modify the pending execution parameters. This event may return a request that the pending command be canceled.</span></span>

