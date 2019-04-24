---
title: フォームの状態
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dfc9fbf1-90d4-4756-92d9-032ac56a9c50
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 61d20ff7010151a82c53cafc69270e6925796a5c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327518"
---
# <a name="form-states"></a><span data-ttu-id="c3ebd-103">フォームの状態</span><span class="sxs-lookup"><span data-stu-id="c3ebd-103">Form states</span></span>

<span data-ttu-id="c3ebd-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c3ebd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c3ebd-105">フォームオブジェクトは、どのメソッドが呼び出されたか、およびそれらのメソッドの実行時にエラーが発生したかどうかに応じて、5つの異なる状態のいずれかになります。</span><span class="sxs-lookup"><span data-stu-id="c3ebd-105">Form objects can be in one of five distinct states, depending on what methods have been called in them and whether any errors have occurred in performing those methods.</span></span> <span data-ttu-id="c3ebd-106">これらの状態については、以下のトピックで説明します。</span><span class="sxs-lookup"><span data-stu-id="c3ebd-106">The states are described in the following topics:</span></span>
  
- [<span data-ttu-id="c3ebd-107">未初期化状態</span><span class="sxs-lookup"><span data-stu-id="c3ebd-107">Uninitialized State</span></span>](uninitialized-state.md)
    
- [<span data-ttu-id="c3ebd-108">通常の状態</span><span class="sxs-lookup"><span data-stu-id="c3ebd-108">Normal State</span></span>](normal-state.md)
    
- [<span data-ttu-id="c3ebd-109">noscribble 状態</span><span class="sxs-lookup"><span data-stu-id="c3ebd-109">NoScribble State</span></span>](noscribble-state.md)
    
- [<span data-ttu-id="c3ebd-110">保存の状態を処理する</span><span class="sxs-lookup"><span data-stu-id="c3ebd-110">HandsOffAfterSave State</span></span>](handsoffaftersave-state.md)
    
- [<span data-ttu-id="c3ebd-111">標準の状態</span><span class="sxs-lookup"><span data-stu-id="c3ebd-111">HandsOffFromNormal State</span></span>](handsofffromnormal-state.md)
    
<span data-ttu-id="c3ebd-112">状態は、主に form オブジェクト内のデータの状態に関連しています。</span><span class="sxs-lookup"><span data-stu-id="c3ebd-112">The states primarily relate to the status of the data in the form object.</span></span> <span data-ttu-id="c3ebd-113">さまざまな状態は、データを保存する必要があるかどうか、フォームオブジェクトがデータに変更を加えることができるかどうか、およびフォームがどのようなデータを保存するかを表します。</span><span class="sxs-lookup"><span data-stu-id="c3ebd-113">The different states reflect whether the data needs to be saved, whether the form object should allow modifications to the data, and what point in the process of saving the data the form is in.</span></span> <span data-ttu-id="c3ebd-114">そのため、フォームの状態と、それらの間の切り替えは、フォームサーバーの IPersistMessage の実装とは他のものよりも、 [IUnknown](ipersistmessageiunknown.md)インターフェイスメソッドの実装によって大きくなります。</span><span class="sxs-lookup"><span data-stu-id="c3ebd-114">As such, the form states and transitions between them have more to do with your form server's implementation of [IPersistMessage : IUnknown](ipersistmessageiunknown.md) interface methods than any other.</span></span> <span data-ttu-id="c3ebd-115">これらの状態に関する知識は、フォームサーバーで実装する必要がある MAPI フォームインターフェイスを適切に実装するのに非常に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="c3ebd-115">Knowledge of these states is very useful for proper implementation of the MAPI form interfaces that your form server must implement.</span></span> 
  
<span data-ttu-id="c3ebd-116">このセクションのトピックでは、さまざまな状態と、他の状態に遷移する可能性がある許可されるアクションについて説明します。</span><span class="sxs-lookup"><span data-stu-id="c3ebd-116">The topics in this section describe the various states, along with the allowed actions that cause transitions to other states.</span></span> <span data-ttu-id="c3ebd-117">これらのトピックに記載されていない遷移は許可されません。</span><span class="sxs-lookup"><span data-stu-id="c3ebd-117">Any transitions not listed in the topics are not allowed.</span></span> <span data-ttu-id="c3ebd-118">フォームオブジェクトで状態間の移行が許可されない場合は、メッセージングクライアントが予期している方法では動作せず、予期しないクライアントまたはフォームオブジェクトの動作が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="c3ebd-118">If your form objects make disallowed transitions between states, they will not behave in the ways that messaging clients expect and could cause unpredictable client or form object behavior.</span></span>
  
> [!NOTE]
> <span data-ttu-id="c3ebd-119">一部の状態遷移は、以前の状態の情報に依存します。</span><span class="sxs-lookup"><span data-stu-id="c3ebd-119">Some state transitions depend on information from previous states.</span></span> <span data-ttu-id="c3ebd-120">フォームサーバーでは、多くの場合、メッセージのプロパティの値が変更されているかどうかを示すフラグを form オブジェクトに実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c3ebd-120">Your form server will most likely have to implement a flag in its form objects to indicate whether the values of the message's properties have been changed to facilitate later state changes.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c3ebd-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="c3ebd-121">See also</span></span>

- [<span data-ttu-id="c3ebd-122">MAPI フォームサーバーの開発</span><span class="sxs-lookup"><span data-stu-id="c3ebd-122">Developing MAPI Form Servers</span></span>](developing-mapi-form-servers.md)

