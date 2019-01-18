---
title: BeginTransComplete、CommitTransComplete、RollbackTransComplete イベント (ADO)
TOCTitle: BeginTransComplete, CommitTransComplete, and RollbackTransComplete events (ADO)
ms:assetid: 9d0ae38e-530a-7a89-a344-f3ab401c2e35
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249713(v=office.15)
ms:contentKeyID: 48546615
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a6f86e17a44ec0813176a023a02710fded627488
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702895"
---
# <a name="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado"></a><span data-ttu-id="43c46-102">BeginTransComplete イベント、CommitTransComplete イベント、RollbackTransComplete イベント (ADO)</span><span class="sxs-lookup"><span data-stu-id="43c46-102">BeginTransComplete, CommitTransComplete, and RollbackTransComplete events (ADO)</span></span>

<span data-ttu-id="43c46-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="43c46-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="43c46-104">これらのイベントは、[Connection](connection-object-ado.md) オブジェクトに対する関連付けられた操作の実行の終了後に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="43c46-104">These events will be called after the associated operation on the [Connection](connection-object-ado.md) object finishes executing.</span></span>

- <span data-ttu-id="43c46-105">**BeginTransComplete** は、 [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) の操作が終了した後に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="43c46-105">**BeginTransComplete** is called after the [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) operation.</span></span>

- <span data-ttu-id="43c46-106">**CommitTransComplete** は、 [CommitTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) の操作が終了した後に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="43c46-106">**CommitTransComplete** is called after the [CommitTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) operation.</span></span>

- <span data-ttu-id="43c46-107">**RollbackTransComplete** は、 [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) の操作が終了した後に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="43c46-107">**RollbackTransComplete** is called after the [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="43c46-108">構文</span><span class="sxs-lookup"><span data-stu-id="43c46-108">Syntax</span></span>

<span data-ttu-id="43c46-109">BeginTransComplete*TransactionLevel*、 *pError*、 *adStatus* *pConnection*</span><span class="sxs-lookup"><span data-stu-id="43c46-109">BeginTransComplete*TransactionLevel*, *pError*, *adStatus*, *pConnection*</span></span>

<span data-ttu-id="43c46-110">CommitTransComplete*pError*、 *adStatus*、 *pConnection*</span><span class="sxs-lookup"><span data-stu-id="43c46-110">CommitTransComplete*pError*, *adStatus*, *pConnection*</span></span>

<span data-ttu-id="43c46-111">RollbackTransComplete*pError*、 *adStatus*、 *pConnection*</span><span class="sxs-lookup"><span data-stu-id="43c46-111">RollbackTransComplete*pError*, *adStatus*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="43c46-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="43c46-112">Parameters</span></span>

|<span data-ttu-id="43c46-113">パラメーター</span><span class="sxs-lookup"><span data-stu-id="43c46-113">Parameter</span></span>|<span data-ttu-id="43c46-114">説明</span><span class="sxs-lookup"><span data-stu-id="43c46-114">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="43c46-115">*TransactionLevel*</span><span class="sxs-lookup"><span data-stu-id="43c46-115">*TransactionLevel*</span></span> |<span data-ttu-id="43c46-116">長整数型 ( **Long** ) の値であり、このイベントを発生させた **BeginTrans** の新規トランザクション レベルが格納されます。</span><span class="sxs-lookup"><span data-stu-id="43c46-116">A **Long** value that contains the new transaction level of the **BeginTrans** that caused this event.</span></span>|
|<span data-ttu-id="43c46-117">*pError*</span><span class="sxs-lookup"><span data-stu-id="43c46-117">*pError*</span></span> |<span data-ttu-id="43c46-118">[Error](error-object-ado.md) オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="43c46-118">An [Error](error-object-ado.md) object.</span></span> <span data-ttu-id="43c46-119">EventStatusEnum の値が**adStatusErrorsOccurred**の場合に発生したエラーについて説明します。それ以外の場合、設定されていません。</span><span class="sxs-lookup"><span data-stu-id="43c46-119">It describes the error that occurred if the value of EventStatusEnum is **adStatusErrorsOccurred**; otherwise, it is not set.</span></span>|
|<span data-ttu-id="43c46-120">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="43c46-120">*adStatus*</span></span> |<span data-ttu-id="43c46-121">[EventStatusEnum](eventstatusenum.md)。</span><span class="sxs-lookup"><span data-stu-id="43c46-121">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="43c46-122">このパラメーターを **adStatusUnwantedEvent** に設定すると、これらのイベントから制御が戻る前に後続の通知が行われるのを防ぐことができます。</span><span class="sxs-lookup"><span data-stu-id="43c46-122">These events can prevent subsequent notifications by setting this parameter to **adStatusUnwantedEvent** before the event returns.</span></span>|
|<span data-ttu-id="43c46-123">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="43c46-123">*pConnection*</span></span> |<span data-ttu-id="43c46-124">このイベントが発生した **Connection** オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="43c46-124">The **Connection** object for which this event occurred.</span></span>|

## <a name="remarks"></a><span data-ttu-id="43c46-125">解説</span><span class="sxs-lookup"><span data-stu-id="43c46-125">Remarks</span></span>

<span data-ttu-id="43c46-p103">Visual C++ では、複数の **Connection** が同じイベント処理メソッドを共有できます。メソッドは返された **Connection** オブジェクトを使って、どのオブジェクトがイベントを発生させたかを判別します。</span><span class="sxs-lookup"><span data-stu-id="43c46-p103">In Visual C++, multiple **Connections** can share the same event handling method. The method uses the returned **Connection** object to determine which object caused the event.</span></span>

<span data-ttu-id="43c46-p104">[Attributes](attributes-property-ado.md) プロパティを **adXactCommitRetaining** または **adXactAbortRetaining** に設定した場合、トランザクションをコミットまたはロールバックした後に、新規トランザクションが開始されます。 **BeginTransComplete** イベントを使うと、最初のトランザクション開始イベント以外のイベントが無視されます。</span><span class="sxs-lookup"><span data-stu-id="43c46-p104">If the [Attributes](attributes-property-ado.md) property is set to **adXactCommitRetaining** or **adXactAbortRetaining**, a new transaction starts after committing or rolling back a transaction. Use the **BeginTransComplete** event to ignore all but the first transaction start event.</span></span>

