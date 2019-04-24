---
title: イベントを実行するイベント (ADO)
TOCTitle: WillExecute event (ADO)
ms:assetid: 9f516bfd-246d-9817-4ca3-64598ab466f7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249732(v=office.15)
ms:contentKeyID: 48546686
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7fe15604d0160afcbde5fdf02eaa6a7831da874b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302758"
---
# <a name="willexecute-event-ado"></a><span data-ttu-id="a03a0-102">イベントを実行するイベント (ADO)</span><span class="sxs-lookup"><span data-stu-id="a03a0-102">WillExecute event (ADO)</span></span>

<span data-ttu-id="a03a0-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="a03a0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a03a0-104">**WillExecute** イベントは、保留中のコマンドが接続に対して実行される直前に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="a03a0-104">The **WillExecute** event is called just before a pending command executes on a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="a03a0-105">構文</span><span class="sxs-lookup"><span data-stu-id="a03a0-105">Syntax</span></span>

<span data-ttu-id="a03a0-106">*Source*、 *CursorType*、 *LockType*、 *Options*、 *adstatus*、 *pcommand*、 *pcommand*、 *pcommand*を実行します。</span><span class="sxs-lookup"><span data-stu-id="a03a0-106">WillExecute*Source*, *CursorType*, *LockType*, *Options*, *adStatus*, *pCommand*, *pRecordset*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="a03a0-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a03a0-107">Parameters</span></span>

|<span data-ttu-id="a03a0-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a03a0-108">Parameter</span></span>|<span data-ttu-id="a03a0-109">説明</span><span class="sxs-lookup"><span data-stu-id="a03a0-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="a03a0-110">*Source*</span><span class="sxs-lookup"><span data-stu-id="a03a0-110">*Source*</span></span> |<span data-ttu-id="a03a0-111">SQL コマンドまたはストアド プロシージャ名が格納された文字列型 ( **String** ) の値です。</span><span class="sxs-lookup"><span data-stu-id="a03a0-111">A **String** that contains an SQL command or a stored procedure name.</span></span>|
|<span data-ttu-id="a03a0-112">*CursorType*</span><span class="sxs-lookup"><span data-stu-id="a03a0-112">*CursorType*</span></span> |<span data-ttu-id="a03a0-113">開く対象の [Recordset](cursortypeenum.md) のカーソルの種類が格納された **CursorTypeEnum** です。</span><span class="sxs-lookup"><span data-stu-id="a03a0-113">A [CursorTypeEnum](cursortypeenum.md) that contains the type of cursor for the **Recordset** that will be opened.</span></span> <span data-ttu-id="a03a0-114">このパラメーターを使用すると、 **Recordset**の[開い](open-method-ado-recordset.md)ている操作中にカーソルを任意の種類に変更できます。</span><span class="sxs-lookup"><span data-stu-id="a03a0-114">With this parameter, you can change the cursor to any type during a **Recordset** [Open](open-method-ado-recordset.md) operation.</span></span> <span data-ttu-id="a03a0-115">*CursorType* は、他の操作には無効です。</span><span class="sxs-lookup"><span data-stu-id="a03a0-115">*CursorType* will be ignored for any other operation.</span></span>|
|<span data-ttu-id="a03a0-116">*LockType*</span><span class="sxs-lookup"><span data-stu-id="a03a0-116">*LockType*</span></span> |<span data-ttu-id="a03a0-117">開く対象の [Recordset](locktypeenum.md) のロックの種類が格納された **LockTypeEnum** です。</span><span class="sxs-lookup"><span data-stu-id="a03a0-117">A [LockTypeEnum](locktypeenum.md) that contains the lock type for the **Recordset** that will be opened.</span></span> <span data-ttu-id="a03a0-118">このパラメーターを使用すると、 **Recordset** の **Open** 操作中にロックを任意の種類に変更できます。</span><span class="sxs-lookup"><span data-stu-id="a03a0-118">With this parameter, you can change the lock to any type during a **Recordset** **Open** operation.</span></span> <span data-ttu-id="a03a0-119">*LockType* は、他の操作には無効です。</span><span class="sxs-lookup"><span data-stu-id="a03a0-119">*LockType* will be ignored for any other operation.</span></span>|
|<span data-ttu-id="a03a0-120">*Options*</span><span class="sxs-lookup"><span data-stu-id="a03a0-120">*Options*</span></span> |<span data-ttu-id="a03a0-121">コマンドを実行するとき、または **Recordset** を開くときに使われるオプションを示す長整数型 ( **Long** ) の値です。</span><span class="sxs-lookup"><span data-stu-id="a03a0-121">A **Long** value that indicates options that can be used to execute the command or open the **Recordset**.</span></span>|
|<span data-ttu-id="a03a0-122">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="a03a0-122">*adStatus*</span></span> |<span data-ttu-id="a03a0-123">[eventstatusenum](eventstatusenum.md)。</span><span class="sxs-lookup"><span data-stu-id="a03a0-123">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="a03a0-124">このイベントから制御が戻る前に後続の通知が行われるのを防ぐには、このパラメーターを **adStatusUnwantedEvent** に設定し、このイベントを発生させた操作の取り消しを要求するには、このパラメーターを **adStatusCancel** に設定します。</span><span class="sxs-lookup"><span data-stu-id="a03a0-124">Before this event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications, or **adStatusCancel** to request cancellation of the operation that caused this event.</span></span>|
|<span data-ttu-id="a03a0-125">*ある*</span><span class="sxs-lookup"><span data-stu-id="a03a0-125">*pCommand*</span></span> |<span data-ttu-id="a03a0-126">このイベント通知が適用される [Command](command-object-ado.md) オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="a03a0-126">The [Command](command-object-ado.md) object for which this event notification applies.</span></span>|
|<span data-ttu-id="a03a0-127">*precordset*</span><span class="sxs-lookup"><span data-stu-id="a03a0-127">*pRecordset*</span></span> |<span data-ttu-id="a03a0-128">このイベント通知が適用される [Recordset](recordset-object-ado.md) オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="a03a0-128">The [Recordset](recordset-object-ado.md) object for which this event notification applies.</span></span>|
|<span data-ttu-id="a03a0-129">*pconnection*</span><span class="sxs-lookup"><span data-stu-id="a03a0-129">*pConnection*</span></span> |<span data-ttu-id="a03a0-130">このイベント通知が適用される [Connection](connection-object-ado.md) オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="a03a0-130">The [Connection](connection-object-ado.md) object for which this event notification applies.</span></span>|

## <a name="remarks"></a><span data-ttu-id="a03a0-131">注釈</span><span class="sxs-lookup"><span data-stu-id="a03a0-131">Remarks</span></span>

<span data-ttu-id="a03a0-p104">**WillExecute** イベントは、**Connection.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) メソッド、**Command.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) メソッド、または **Recordset.**[Open](open-method-ado-recordset.md) メソッドによって発生します。*pConnection* パラメーターには、常に **Connection** オブジェクトに対する有効な参照が格納されます。イベントの原因が **Connection.Execute** の場合、*pRecordset* パラメーターと *pCommand* パラメーターは **Nothing** に設定されます。イベントの原因が **Recordset.Open** の場合、*pRecordset* パラメーターは **Recordset** オブジェクトを参照し、*pCommand* パラメーターは **Nothing** に設定されます。イベントの原因が **Command.Execute** の場合、*pCommand* パラメーターは **Command** オブジェクトを参照し、*pRecordset* パラメーターは **Nothing** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="a03a0-p104">A **WillExecute** event may occur due to a **Connection.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection), **Command.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command), or **Recordset.**[Open](open-method-ado-recordset.md) method The *pConnection* parameter should always contain a valid reference to a **Connection** object. If the event is due to **Connection.Execute**, the *pRecordset* and *pCommand* parameters are set to **Nothing**. If the event is due to **Recordset.Open**, the *pRecordset* parameter will reference the **Recordset** object and the *pCommand* parameter is set to **Nothing**. If the event is due to **Command.Execute**, the *pCommand* parameter will reference the **Command** object and the *pRecordset* parameter is set to **Nothing**.</span></span>

<span data-ttu-id="a03a0-p105">**WillExecute** では、保留中の実行パラメーターを調べたり、編集したりできます。このイベントは、保留中のコマンドを取り消す要求を返すこともあります。</span><span class="sxs-lookup"><span data-stu-id="a03a0-p105">**WillExecute** allows you to examine and modify the pending execution parameters. This event may return a request that the pending command be canceled.</span></span>

