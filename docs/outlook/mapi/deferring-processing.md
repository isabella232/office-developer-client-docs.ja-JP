---
title: 処理を保留します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a791b95f-56ad-493a-9ba5-fb4c7dd80e89
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 8f26fc6a51c3abdb4d4d009183fa8263ce97b261
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799881"
---
# <a name="deferring-processing"></a><span data-ttu-id="32649-103">処理を保留します。</span><span class="sxs-lookup"><span data-stu-id="32649-103">Deferring Processing</span></span>

  
  
<span data-ttu-id="32649-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="32649-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="32649-105">メソッドの呼び出しを可能な限りに MAPI_DEFERRED_ERRORS フラグを渡します。</span><span class="sxs-lookup"><span data-stu-id="32649-105">Pass the MAPI_DEFERRED_ERRORS flag to method calls as much as possible.</span></span> <span data-ttu-id="32649-106">MAPI メソッドの呼び出しの多くは、一度に複数のタスクを実行することができます設定したり、不要になった結果を得るまでか、要求されたタスクを延期するのにはプロバイダーの原因と、このフラグを受け入れるように最適化されています。</span><span class="sxs-lookup"><span data-stu-id="32649-106">Many of the MAPI method calls have been optimized to accept this flag, causing the provider to either postpone the requested task until multiple tasks can be performed at once or you can wait no longer for the results.</span></span>
  
<span data-ttu-id="32649-107">などの場合はフォルダーを開くには、 [IMsgStore::OpenEntry](imsgstore-openentry.md)に MAPI_DEFERRED_ERRORS を渡すと、フォルダー、および使用可能なリモート呼び出しの開始延期できるようにフォルダーの**GetHierarchyTable**または**の呼び出しなどの別の呼び出しを行うまでGetProps**方法です。</span><span class="sxs-lookup"><span data-stu-id="32649-107">For example, if you pass MAPI_DEFERRED_ERRORS to [IMsgStore::OpenEntry](imsgstore-openentry.md) to open a folder, the opening of the folder and a possible remote call can be postponed until you make another call such as a call to the folder's **GetHierarchyTable** or **GetProps** methods.</span></span> <span data-ttu-id="32649-108">**GetProps**と**GetHierarchyTable**の両方はすぐに実行する必要があるタスク、サービス ・ プロバイダーからデータを返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="32649-108">Both **GetHierarchyTable** and **GetProps** require the return of data from the service provider, a task that must be performed immediately.</span></span> 
  
<span data-ttu-id="32649-109">処理を延期するのには別の方法は、呼び出しを行うことないだけがです。</span><span class="sxs-lookup"><span data-stu-id="32649-109">Another way to defer processing is simply not to make a call.</span></span> <span data-ttu-id="32649-110">把握しているユーザーを使用して、ユーザーがリソースや処理時間の浪費を得ることが、呼び出しを行う方が良い場合を指定できます。</span><span class="sxs-lookup"><span data-stu-id="32649-110">By being aware of the user and when the user can perceive a drain on resources or processing time, you can determine when it makes sense to make calls.</span></span> <span data-ttu-id="32649-111">どちらかですると、ユーザーが気付くことはありませんの呼び出しを行うかを設定していないすべてのパフォーマンスを向上させる機会があります。</span><span class="sxs-lookup"><span data-stu-id="32649-111">There is an opportunity to improve performance by making calls either at a time when the user will not notice or by not making them at all.</span></span>
  
<span data-ttu-id="32649-112">たとえば、多数のメッセージを移動するメッセージ ・ ストアから 1 秒あたりの 1 つ以上の通知を受信するときは、状況を検討します。</span><span class="sxs-lookup"><span data-stu-id="32649-112">For example, consider the situation when you are receiving more than one notification per second from a message store that is moving a great number of messages.</span></span> <span data-ttu-id="32649-113">操作の完了の割合を示す進行状況のインジケーターが表示されます。</span><span class="sxs-lookup"><span data-stu-id="32649-113">A progress indicator is displayed to indicate the percentage of the operation's completion.</span></span> <span data-ttu-id="32649-114">ユーザー一般認識は、ありませんこの操作は数秒が経過するまでに時間がかかることを。</span><span class="sxs-lookup"><span data-stu-id="32649-114">Users typically will not perceive this operation to be slow until a few seconds have passed.</span></span> <span data-ttu-id="32649-115">したがって、プログレス インジケーターを更新する場合は、変更しないでください、最低 4 秒間の移動操作を開始した後まで。</span><span class="sxs-lookup"><span data-stu-id="32649-115">Therefore, if you are updating the progress indicator, do not make any changes until at least four seconds after the initiation of the move operation.</span></span> <span data-ttu-id="32649-116">操作が高速にしたときの一般的なケースで時間の節約、操作が低速にすると適切なタイミングでユーザーに通知します。</span><span class="sxs-lookup"><span data-stu-id="32649-116">This will save time in the common cases when the operation is fast and inform users in a timely manner when the operation is slow.</span></span>
  

