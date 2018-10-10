---
title: BeginTransComplete、CommitTransComplete、RollbackTransComplete イベント (ADO)
TOCTitle: BeginTransComplete, CommitTransComplete, and RollbackTransComplete Events (ADO)
ms:assetid: 9d0ae38e-530a-7a89-a344-f3ab401c2e35
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249713(v=office.15)
ms:contentKeyID: 48546615
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 216f5a92ea4095d78b8df2b196a1607e40ae58d1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479550"
---
# <a name="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado"></a><span data-ttu-id="50001-102">BeginTransComplete イベント、CommitTransComplete イベント、および RollbackTransComplete イベント (ADO)</span><span class="sxs-lookup"><span data-stu-id="50001-102">BeginTransComplete, CommitTransComplete, and RollbackTransComplete Events (ADO)</span></span>


<span data-ttu-id="50001-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="50001-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="50001-104">これらのイベントは、[Connection](connection-object-ado.md) オブジェクトに対する関連付けられた操作の実行の終了後に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="50001-104">These events will be called after the associated operation on the [Connection](connection-object-ado.md) object finishes executing.</span></span>

  - <span data-ttu-id="50001-105">**BeginTransComplete** は、 [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) の操作が終了した後に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="50001-105">**BeginTransComplete** is called after the [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) operation.</span></span>

  - <span data-ttu-id="50001-106">**CommitTransComplete** は、 [CommitTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) の操作が終了した後に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="50001-106">**CommitTransComplete** is called after the [CommitTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) operation.</span></span>

  - <span data-ttu-id="50001-107">**RollbackTransComplete** は、 [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) の操作が終了した後に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="50001-107">**RollbackTransComplete** is called after the [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="50001-108">構文</span><span class="sxs-lookup"><span data-stu-id="50001-108">Syntax</span></span>

<span data-ttu-id="50001-109">BeginTransComplete*TransactionLevel*、 *pError*、 *adStatus* *pConnection*</span><span class="sxs-lookup"><span data-stu-id="50001-109">BeginTransComplete*TransactionLevel*, *pError*, *adStatus*, *pConnection*</span></span>

<span data-ttu-id="50001-110">CommitTransComplete*pError*、 *adStatus*、 *pConnection*</span><span class="sxs-lookup"><span data-stu-id="50001-110">CommitTransComplete*pError*, *adStatus*, *pConnection*</span></span>

<span data-ttu-id="50001-111">RollbackTransComplete*pError*、 *adStatus*、 *pConnection*</span><span class="sxs-lookup"><span data-stu-id="50001-111">RollbackTransComplete*pError*, *adStatus*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="50001-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50001-112">Parameters</span></span>

  - <span data-ttu-id="50001-113">*TransactionLevel*</span><span class="sxs-lookup"><span data-stu-id="50001-113">*TransactionLevel*</span></span>

  - <span data-ttu-id="50001-114">長整数型 ( **Long** ) の値であり、このイベントを発生させた **BeginTrans** の新規トランザクション レベルが格納されます。</span><span class="sxs-lookup"><span data-stu-id="50001-114">A **Long** value that contains the new transaction level of the **BeginTrans** that caused this event.</span></span>

  - <span data-ttu-id="50001-115">*pError*</span><span class="sxs-lookup"><span data-stu-id="50001-115">*pError*</span></span>

  - <span data-ttu-id="50001-p101">[Error](error-object-ado.md) オブジェクトです。EventStatusEnum の値が **adStatusErrorsOccurred** の場合は、発生したエラーを示します。それ以外の場合は設定されません。</span><span class="sxs-lookup"><span data-stu-id="50001-p101">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of EventStatusEnum is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>

  - <span data-ttu-id="50001-118">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="50001-118">*adStatus*</span></span>

  - [<span data-ttu-id="50001-119">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="50001-119">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="50001-120">このパラメーターを **adStatusUnwantedEvent** に設定すると、これらのイベントから制御が戻る前に後続の通知が行われるのを防ぐことができます。</span><span class="sxs-lookup"><span data-stu-id="50001-120">These events can prevent subsequent notifications by setting this parameter to **adStatusUnwantedEvent** before the event returns.</span></span>

  - <span data-ttu-id="50001-121">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="50001-121">*pConnection*</span></span>

  - <span data-ttu-id="50001-122">このイベントが発生した **Connection** オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="50001-122">The **Connection** object for which this event occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="50001-123">解説</span><span class="sxs-lookup"><span data-stu-id="50001-123">Remarks</span></span>

<span data-ttu-id="50001-p102">Visual C++ では、複数の **Connection** が同じイベント処理メソッドを共有できます。メソッドは返された **Connection** オブジェクトを使って、どのオブジェクトがイベントを発生させたかを判別します。</span><span class="sxs-lookup"><span data-stu-id="50001-p102">In Visual C++, multiple **Connections** can share the same event handling method. The method uses the returned **Connection** object to determine which object caused the event.</span></span>

<span data-ttu-id="50001-p103">[Attributes](attributes-property-ado.md) プロパティを **adXactCommitRetaining** または **adXactAbortRetaining** に設定した場合、トランザクションをコミットまたはロールバックした後に、新規トランザクションが開始されます。 **BeginTransComplete** イベントを使うと、最初のトランザクション開始イベント以外のイベントが無視されます。</span><span class="sxs-lookup"><span data-stu-id="50001-p103">If the [Attributes](attributes-property-ado.md) property is set to **adXactCommitRetaining** or **adXactAbortRetaining**, a new transaction starts after committing or rolling back a transaction. Use the **BeginTransComplete** event to ignore all but the first transaction start event.</span></span>

