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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429167"
---
# <a name="form-states"></a><span data-ttu-id="c56c4-103">フォームの状態</span><span class="sxs-lookup"><span data-stu-id="c56c4-103">Form states</span></span>

<span data-ttu-id="c56c4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c56c4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c56c4-105">フォーム オブジェクトは、呼び出されたメソッドと、それらのメソッドの実行でエラーが発生したかどうかに応じて、5 つの異なる状態の 1 つになります。</span><span class="sxs-lookup"><span data-stu-id="c56c4-105">Form objects can be in one of five distinct states, depending on what methods have been called in them and whether any errors have occurred in performing those methods.</span></span> <span data-ttu-id="c56c4-106">状態については、次のトピックで説明します。</span><span class="sxs-lookup"><span data-stu-id="c56c4-106">The states are described in the following topics:</span></span>
  
- [<span data-ttu-id="c56c4-107">初期化されていない状態</span><span class="sxs-lookup"><span data-stu-id="c56c4-107">Uninitialized State</span></span>](uninitialized-state.md)
    
- [<span data-ttu-id="c56c4-108">標準状態</span><span class="sxs-lookup"><span data-stu-id="c56c4-108">Normal State</span></span>](normal-state.md)
    
- [<span data-ttu-id="c56c4-109">NoScribble 状態</span><span class="sxs-lookup"><span data-stu-id="c56c4-109">NoScribble State</span></span>](noscribble-state.md)
    
- [<span data-ttu-id="c56c4-110">HandsOffAfterSave 状態</span><span class="sxs-lookup"><span data-stu-id="c56c4-110">HandsOffAfterSave State</span></span>](handsoffaftersave-state.md)
    
- [<span data-ttu-id="c56c4-111">HandsOffFromNormal State</span><span class="sxs-lookup"><span data-stu-id="c56c4-111">HandsOffFromNormal State</span></span>](handsofffromnormal-state.md)
    
<span data-ttu-id="c56c4-112">状態は、主にフォーム オブジェクト内のデータの状態に関連します。</span><span class="sxs-lookup"><span data-stu-id="c56c4-112">The states primarily relate to the status of the data in the form object.</span></span> <span data-ttu-id="c56c4-113">異なる状態は、データを保存する必要があるかどうか、フォーム オブジェクトがデータの変更を許可するかどうか、およびフォームが含まれるデータを保存する過程のポイントを反映します。</span><span class="sxs-lookup"><span data-stu-id="c56c4-113">The different states reflect whether the data needs to be saved, whether the form object should allow modifications to the data, and what point in the process of saving the data the form is in.</span></span> <span data-ttu-id="c56c4-114">そのため、フォームの状態と切り替えは、フォーム サーバーの [IPersistMessage : IUnknown](ipersistmessageiunknown.md) インターフェイス メソッドの実装と他の方法よりも関係があります。</span><span class="sxs-lookup"><span data-stu-id="c56c4-114">As such, the form states and transitions between them have more to do with your form server's implementation of [IPersistMessage : IUnknown](ipersistmessageiunknown.md) interface methods than any other.</span></span> <span data-ttu-id="c56c4-115">これらの状態に関する知識は、フォーム サーバーが実装する必要がある MAPI フォーム インターフェイスを適切に実装する場合に非常に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="c56c4-115">Knowledge of these states is very useful for proper implementation of the MAPI form interfaces that your form server must implement.</span></span> 
  
<span data-ttu-id="c56c4-116">このセクションのトピックでは、さまざまな状態と、他の状態への移行を引き起こす許可されるアクションについて説明します。</span><span class="sxs-lookup"><span data-stu-id="c56c4-116">The topics in this section describe the various states, along with the allowed actions that cause transitions to other states.</span></span> <span data-ttu-id="c56c4-117">トピックに記載されていない遷移は許可されません。</span><span class="sxs-lookup"><span data-stu-id="c56c4-117">Any transitions not listed in the topics are not allowed.</span></span> <span data-ttu-id="c56c4-118">フォーム オブジェクトが状態間の移行を許可しない場合、メッセージング クライアントが期待する方法では動作し、予期しないクライアントまたはフォーム オブジェクトの動作を引き起こす可能性があります。</span><span class="sxs-lookup"><span data-stu-id="c56c4-118">If your form objects make disallowed transitions between states, they will not behave in the ways that messaging clients expect and could cause unpredictable client or form object behavior.</span></span>
  
> [!NOTE]
> <span data-ttu-id="c56c4-119">一部の状態遷移は、以前の状態からの情報に依存します。</span><span class="sxs-lookup"><span data-stu-id="c56c4-119">Some state transitions depend on information from previous states.</span></span> <span data-ttu-id="c56c4-120">フォーム サーバーは、メッセージのプロパティの値が変更されたかどうかを示すために、フォーム オブジェクトにフラグを実装して、後で状態を変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c56c4-120">Your form server will most likely have to implement a flag in its form objects to indicate whether the values of the message's properties have been changed to facilitate later state changes.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c56c4-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="c56c4-121">See also</span></span>

- [<span data-ttu-id="c56c4-122">MAPI フォーム サーバーの開発</span><span class="sxs-lookup"><span data-stu-id="c56c4-122">Developing MAPI Form Servers</span></span>](developing-mapi-form-servers.md)

