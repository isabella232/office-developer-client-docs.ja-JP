---
title: フォームの状態
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dfc9fbf1-90d4-4756-92d9-032ac56a9c50
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 969aca6fd37f237a607df36cc58f249828449e27
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800126"
---
# <a name="form-states"></a><span data-ttu-id="6853d-103">フォームの状態</span><span class="sxs-lookup"><span data-stu-id="6853d-103">Form states</span></span>

<span data-ttu-id="6853d-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6853d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6853d-105">フォーム オブジェクトは、それらにどのようなメソッドが呼び出された、およびそれらのメソッドを実行する際にエラーが発生しているかどうかによって、5 つの異なる状態のいずれかで指定できます。</span><span class="sxs-lookup"><span data-stu-id="6853d-105">Form objects can be in one of five distinct states, depending on what methods have been called in them and whether any errors have occurred in performing those methods.</span></span> <span data-ttu-id="6853d-106">状態は次のトピックで説明します。</span><span class="sxs-lookup"><span data-stu-id="6853d-106">The states are described in the following topics:</span></span>
  
- [<span data-ttu-id="6853d-107">Uninitialized 状態</span><span class="sxs-lookup"><span data-stu-id="6853d-107">Uninitialized State</span></span>](uninitialized-state.md)
    
- [<span data-ttu-id="6853d-108">Normal 状態</span><span class="sxs-lookup"><span data-stu-id="6853d-108">Normal State</span></span>](normal-state.md)
    
- [<span data-ttu-id="6853d-109">NoScribble 状態</span><span class="sxs-lookup"><span data-stu-id="6853d-109">NoScribble State</span></span>](noscribble-state.md)
    
- [<span data-ttu-id="6853d-110">HandsOffAfterSave 状態</span><span class="sxs-lookup"><span data-stu-id="6853d-110">HandsOffAfterSave State</span></span>](handsoffaftersave-state.md)
    
- [<span data-ttu-id="6853d-111">HandsOffFromNormal 状態</span><span class="sxs-lookup"><span data-stu-id="6853d-111">HandsOffFromNormal State</span></span>](handsofffromnormal-state.md)
    
<span data-ttu-id="6853d-112">状態は、主に、フォーム オブジェクト内のデータの状態に関連します。</span><span class="sxs-lookup"><span data-stu-id="6853d-112">The states primarily relate to the status of the data in the form object.</span></span> <span data-ttu-id="6853d-113">さまざまな状態では、フォーム オブジェクトは、データ、および、どの時点では、フォームでデータを保存する際に変更を許可する必要があるかどうかを保存するには、データが必要かどうかを反映します。</span><span class="sxs-lookup"><span data-stu-id="6853d-113">The different states reflect whether the data needs to be saved, whether the form object should allow modifications to the data, and what point in the process of saving the data the form is in.</span></span> <span data-ttu-id="6853d-114">ように、フォームの状態およびそれらの間の遷移がある他の操作、フォームのサーバーの実装の[IPersistMessage: IUnknown](ipersistmessageiunknown.md)よりも、他のメソッドのインターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="6853d-114">As such, the form states and transitions between them have more to do with your form server's implementation of [IPersistMessage : IUnknown](ipersistmessageiunknown.md) interface methods than any other.</span></span> <span data-ttu-id="6853d-115">これらの状態の知識は、フォーム サーバーを実装する必要があります、MAPI フォーム インターフェイスの適切な実装に非常に便利です。</span><span class="sxs-lookup"><span data-stu-id="6853d-115">Knowledge of these states is very useful for proper implementation of the MAPI form interfaces that your form server must implement.</span></span> 
  
<span data-ttu-id="6853d-116">このセクションのトピックでは、他の状態への遷移が発生するを許可する操作と、さまざまな状態について説明します。</span><span class="sxs-lookup"><span data-stu-id="6853d-116">The topics in this section describe the various states, along with the allowed actions that cause transitions to other states.</span></span> <span data-ttu-id="6853d-117">トピックに記載されていないすべての遷移を指定することはできません。</span><span class="sxs-lookup"><span data-stu-id="6853d-117">Any transitions not listed in the topics are not allowed.</span></span> <span data-ttu-id="6853d-118">場合は、フォーム オブジェクトでは、[許可しない] の切り替えを行うための状態の間、メッセージング クライアントが予想され、クライアント、またはフォーム オブジェクトの予期しない動作が発生する可能性がありますの方法では動作しません。</span><span class="sxs-lookup"><span data-stu-id="6853d-118">If your form objects make disallowed transitions between states, they will not behave in the ways that messaging clients expect and could cause unpredictable client or form object behavior.</span></span>
  
> [!NOTE]
> <span data-ttu-id="6853d-119">いくつかの状態の遷移は、以前の状態からの情報に依存します。</span><span class="sxs-lookup"><span data-stu-id="6853d-119">Some state transitions depend on information from previous states.</span></span> <span data-ttu-id="6853d-120">フォーム サーバーは、後の状態の変更を容易にするメッセージのプロパティの値が変更されたかどうかを示すためには、そのフォーム オブジェクトにフラグを実装する可能性が高い必要があります。</span><span class="sxs-lookup"><span data-stu-id="6853d-120">Your form server will most likely have to implement a flag in its form objects to indicate whether the values of the message's properties have been changed to facilitate later state changes.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6853d-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="6853d-121">See also</span></span>

- [<span data-ttu-id="6853d-122">MAPI フォーム サーバーの開発</span><span class="sxs-lookup"><span data-stu-id="6853d-122">Developing MAPI Form Servers</span></span>](developing-mapi-form-servers.md)

