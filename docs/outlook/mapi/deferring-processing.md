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
# <a name="deferring-processing"></a><span data-ttu-id="f1965-103">処理の延期</span><span class="sxs-lookup"><span data-stu-id="f1965-103">Deferring Processing</span></span>

  
  
<span data-ttu-id="f1965-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f1965-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f1965-105">メソッド呼び出MAPI_DEFERRED_ERRORS可能な限り、このフラグを渡します。</span><span class="sxs-lookup"><span data-stu-id="f1965-105">Pass the MAPI_DEFERRED_ERRORS flag to method calls as much as possible.</span></span> <span data-ttu-id="f1965-106">MAPI メソッドの呼び出しの多くは、このフラグを受け入れするために最適化されています。これにより、プロバイダーは、複数のタスクを一度に実行するか、結果を待てなくなるまで、要求されたタスクを延期します。</span><span class="sxs-lookup"><span data-stu-id="f1965-106">Many of the MAPI method calls have been optimized to accept this flag, causing the provider to either postpone the requested task until multiple tasks can be performed at once or you can wait no longer for the results.</span></span>
  
<span data-ttu-id="f1965-107">たとえば、MAPI_DEFERRED_ERRORS を [IMsgStore::OpenEntry](imsgstore-openentry.md) に渡してフォルダーを開く場合、フォルダーの **GetHierarchyTable** メソッドや **GetProps** メソッドへの呼び出しなど、別の呼び出しを行うまで、フォルダーの開始とリモート呼び出しの可能性を延期できます。</span><span class="sxs-lookup"><span data-stu-id="f1965-107">For example, if you pass MAPI_DEFERRED_ERRORS to [IMsgStore::OpenEntry](imsgstore-openentry.md) to open a folder, the opening of the folder and a possible remote call can be postponed until you make another call such as a call to the folder's **GetHierarchyTable** or **GetProps** methods.</span></span> <span data-ttu-id="f1965-108">**GetHierarchyTable と** **GetProps** の両方で、すぐに実行する必要があるタスクであるサービス プロバイダーからのデータの戻り値が必要です。</span><span class="sxs-lookup"><span data-stu-id="f1965-108">Both **GetHierarchyTable** and **GetProps** require the return of data from the service provider, a task that must be performed immediately.</span></span> 
  
<span data-ttu-id="f1965-109">処理を延期するもう 1 つの方法は、単に呼び出しを行うのではありません。</span><span class="sxs-lookup"><span data-stu-id="f1965-109">Another way to defer processing is simply not to make a call.</span></span> <span data-ttu-id="f1965-110">ユーザーを認識し、ユーザーがリソースの消耗や処理時間を感知できる場合は、いつ呼び出しを行うのが理にかなったのか判断できます。</span><span class="sxs-lookup"><span data-stu-id="f1965-110">By being aware of the user and when the user can perceive a drain on resources or processing time, you can determine when it makes sense to make calls.</span></span> <span data-ttu-id="f1965-111">ユーザーが気付かないときや、呼び出しを行ってパフォーマンスを向上させる機会があります。</span><span class="sxs-lookup"><span data-stu-id="f1965-111">There is an opportunity to improve performance by making calls either at a time when the user will not notice or by not making them at all.</span></span>
  
<span data-ttu-id="f1965-112">たとえば、多数のメッセージを移動しているメッセージ ストアから 1 秒に 2 つ以上の通知を受け取る状況を考え出します。</span><span class="sxs-lookup"><span data-stu-id="f1965-112">For example, consider the situation when you are receiving more than one notification per second from a message store that is moving a great number of messages.</span></span> <span data-ttu-id="f1965-113">進行状況インジケーターが表示され、操作の完了率が示されます。</span><span class="sxs-lookup"><span data-stu-id="f1965-113">A progress indicator is displayed to indicate the percentage of the operation's completion.</span></span> <span data-ttu-id="f1965-114">ユーザーは通常、数秒が経過するまで、この操作が遅いと認識されます。</span><span class="sxs-lookup"><span data-stu-id="f1965-114">Users typically will not perceive this operation to be slow until a few seconds have passed.</span></span> <span data-ttu-id="f1965-115">したがって、進行状況インジケーターを更新する場合は、移動操作の開始から少なくとも 4 秒後まで変更を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="f1965-115">Therefore, if you are updating the progress indicator, do not make any changes until at least four seconds after the initiation of the move operation.</span></span> <span data-ttu-id="f1965-116">これにより、操作が高速な場合の一般的なケースの時間が節約され、操作が遅いときにユーザーに迅速に通知します。</span><span class="sxs-lookup"><span data-stu-id="f1965-116">This will save time in the common cases when the operation is fast and inform users in a timely manner when the operation is slow.</span></span>
  

