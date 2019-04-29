---
title: 処理の延期
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a791b95f-56ad-493a-9ba5-fb4c7dd80e89
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2d3fbf8f7a725f121579066001715fb0bc6beba0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430932"
---
# <a name="deferring-processing"></a><span data-ttu-id="dd6fb-103">処理の延期</span><span class="sxs-lookup"><span data-stu-id="dd6fb-103">Deferring Processing</span></span>

  
  
<span data-ttu-id="dd6fb-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dd6fb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dd6fb-105">MAPI_DEFERRED_ERRORS フラグをメソッド呼び出しに可能な限り渡します。</span><span class="sxs-lookup"><span data-stu-id="dd6fb-105">Pass the MAPI_DEFERRED_ERRORS flag to method calls as much as possible.</span></span> <span data-ttu-id="dd6fb-106">多くの MAPI メソッド呼び出しは、このフラグを受け入れるように最適化されているため、プロバイダーは、一度に複数のタスクを実行できるようになるか、または結果を待つことができなくなるまで、要求されたタスクを延期することができます。</span><span class="sxs-lookup"><span data-stu-id="dd6fb-106">Many of the MAPI method calls have been optimized to accept this flag, causing the provider to either postpone the requested task until multiple tasks can be performed at once or you can wait no longer for the results.</span></span>
  
<span data-ttu-id="dd6fb-107">たとえば、MAPI_DEFERRED_ERRORS を[IMsgStore:: openentry](imsgstore-openentry.md)に渡してフォルダーを開くと、フォルダーを開く操作とリモート呼び出しを延期することができます。そのためには、フォルダーの**GetHierarchyTable**の呼び出し、または**その他の呼び出しを実行する必要があります。GetProps**メソッド</span><span class="sxs-lookup"><span data-stu-id="dd6fb-107">For example, if you pass MAPI_DEFERRED_ERRORS to [IMsgStore::OpenEntry](imsgstore-openentry.md) to open a folder, the opening of the folder and a possible remote call can be postponed until you make another call such as a call to the folder's **GetHierarchyTable** or **GetProps** methods.</span></span> <span data-ttu-id="dd6fb-108">**GetHierarchyTable**と**GetProps**の両方に、サービスプロバイダーからのデータを返す必要があります。タスクは、すぐに実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dd6fb-108">Both **GetHierarchyTable** and **GetProps** require the return of data from the service provider, a task that must be performed immediately.</span></span> 
  
<span data-ttu-id="dd6fb-109">処理を延期する別の方法は、単に通話を行わないことです。</span><span class="sxs-lookup"><span data-stu-id="dd6fb-109">Another way to defer processing is simply not to make a call.</span></span> <span data-ttu-id="dd6fb-110">ユーザーを認識し、ユーザーがリソースのドレインや処理時間を感じられる場合は、どのような場合に呼び出しを行うのが妥当かを判断できます。</span><span class="sxs-lookup"><span data-stu-id="dd6fb-110">By being aware of the user and when the user can perceive a drain on resources or processing time, you can determine when it makes sense to make calls.</span></span> <span data-ttu-id="dd6fb-111">ユーザーが気付かないときに、または一度に呼び出しを行うことによって、パフォーマンスを向上させる機会があります。</span><span class="sxs-lookup"><span data-stu-id="dd6fb-111">There is an opportunity to improve performance by making calls either at a time when the user will not notice or by not making them at all.</span></span>
  
<span data-ttu-id="dd6fb-112">たとえば、非常に多くのメッセージを移動しているメッセージストアから1秒間に複数の通知を受信する場合の状況を考えてみます。</span><span class="sxs-lookup"><span data-stu-id="dd6fb-112">For example, consider the situation when you are receiving more than one notification per second from a message store that is moving a great number of messages.</span></span> <span data-ttu-id="dd6fb-113">操作の完了率を示す進行状況インジケーターが表示されます。</span><span class="sxs-lookup"><span data-stu-id="dd6fb-113">A progress indicator is displayed to indicate the percentage of the operation's completion.</span></span> <span data-ttu-id="dd6fb-114">通常、ユーザーは数秒間経過するまで、この操作が遅くなることを感じることはありません。</span><span class="sxs-lookup"><span data-stu-id="dd6fb-114">Users typically will not perceive this operation to be slow until a few seconds have passed.</span></span> <span data-ttu-id="dd6fb-115">そのため、進行状況インジケーターを更新している場合は、移動操作の開始後、少なくとも4秒後に変更を加えないでください。</span><span class="sxs-lookup"><span data-stu-id="dd6fb-115">Therefore, if you are updating the progress indicator, do not make any changes until at least four seconds after the initiation of the move operation.</span></span> <span data-ttu-id="dd6fb-116">これにより、操作が高速な場合の一般的なケースで時間が節約され、操作が遅くなるときにユーザーにタイムリーに通知されます。</span><span class="sxs-lookup"><span data-stu-id="dd6fb-116">This will save time in the common cases when the operation is fast and inform users in a timely manner when the operation is slow.</span></span>
  

