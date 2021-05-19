---
title: 進行状況インジケーターの実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3a062a88-e87e-4c0c-944e-544a8f080930
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 6972c960705c336aa6ff96d81b48ccbd490a22ee
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435097"
---
# <a name="implementing-a-progress-indicator"></a><span data-ttu-id="51ecb-103">進行状況インジケーターの実装</span><span class="sxs-lookup"><span data-stu-id="51ecb-103">Implementing a Progress Indicator</span></span>

  
  
<span data-ttu-id="51ecb-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="51ecb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="51ecb-105">クライアントによって開始される操作の多くは、かなりの時間を必要とします。</span><span class="sxs-lookup"><span data-stu-id="51ecb-105">Many of the operations initiated by clients take a significant amount of time.</span></span> <span data-ttu-id="51ecb-106">これらの潜在的に長い操作に対する入力パラメーターの 1 つは [、IMAPIProgress : IUnknown](imapiprogressiunknown.md) インターフェイスを実装するオブジェクトである進行状況オブジェクトへのポインターです。</span><span class="sxs-lookup"><span data-stu-id="51ecb-106">One of the input parameters to these potentially lengthy operations is a pointer to a progress object — an object that implements the [IMAPIProgress : IUnknown](imapiprogressiunknown.md) interface.</span></span> <span data-ttu-id="51ecb-107">Progress オブジェクトは進行状況インジケーターの外観と表示を制御し、クライアントと MAPI によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="51ecb-107">Progress objects control the appearance and display of progress indicators and are implemented by clients and by MAPI.</span></span> <span data-ttu-id="51ecb-108">進行状況オブジェクトを実装するかどうかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="51ecb-108">You can choose whether or not to implement a progress object.</span></span> <span data-ttu-id="51ecb-109">MAPI 実装は、実装を提供しない場合にサービス プロバイダーが使用できます。</span><span class="sxs-lookup"><span data-stu-id="51ecb-109">The MAPI implementation is available for service providers to use if you elect not to supply an implementation.</span></span> 
  
<span data-ttu-id="51ecb-110">Progress オブジェクトは、次のデータを操作します。</span><span class="sxs-lookup"><span data-stu-id="51ecb-110">Progress objects work with the following pieces of data:</span></span>
  
- <span data-ttu-id="51ecb-111">[IMAPIProgress::P rogress](imapiprogress-progress.md)メソッドが呼び出される場合のグローバル最小値は _、ulValue_ パラメーターの値以下にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="51ecb-111">A global minimum value which, when your [IMAPIProgress::Progress](imapiprogress-progress.md) method is called, should be less than or equal to the value of the  _ulValue_ parameter.</span></span> <span data-ttu-id="51ecb-112">操作の開始時に  _、ulValue_ はこの最小値と等しくなります。</span><span class="sxs-lookup"><span data-stu-id="51ecb-112">At the beginning of the operation,  _ulValue_ will be equal to this minimum value.</span></span> 
    
- <span data-ttu-id="51ecb-113">**IMAPIProgress::P rogress** メソッドが呼び出される場合のグローバル最大値は _、ulValue_ パラメーター以上にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="51ecb-113">A global maximum value which, when your **IMAPIProgress::Progress** method is called, should be greater than or equal to the  _ulValue_ parameter.</span></span> <span data-ttu-id="51ecb-114">操作の最後に  _、ulValue_ はこの最大値と等しくなります。</span><span class="sxs-lookup"><span data-stu-id="51ecb-114">At the end of the operation,  _ulValue_ will be equal to this maximum value.</span></span> 
    
- <span data-ttu-id="51ecb-115">進行状況が上位レベルまたは下位レベルのアイテムに対応するかどうかを示すフラグ値。</span><span class="sxs-lookup"><span data-stu-id="51ecb-115">A flags value which indicates whether the progress corresponds to a top or lower level item.</span></span>
    
- <span data-ttu-id="51ecb-116">操作の進行状況の現在のレベルを示す値。</span><span class="sxs-lookup"><span data-stu-id="51ecb-116">A value that indicates the current level of progress for the operation.</span></span>
    
- <span data-ttu-id="51ecb-117">合計に対する現在処理されているアイテムの数。</span><span class="sxs-lookup"><span data-stu-id="51ecb-117">The number of the currently processed items relative to the total.</span></span>
    
- <span data-ttu-id="51ecb-118">操作中に処理されるアイテムの総数。</span><span class="sxs-lookup"><span data-stu-id="51ecb-118">The total number of items to be processed during the operation.</span></span>
    
<span data-ttu-id="51ecb-119">最小値と最大値は、操作の開始と終了を数値形式で表します。</span><span class="sxs-lookup"><span data-stu-id="51ecb-119">The minimum and maximum values represent the beginning and end of the operation in numeric form.</span></span> <span data-ttu-id="51ecb-120">最初の最小値には 1、初期最大値には 1000 を使用し [、IMAPIProgress::GetMin](imapiprogress-getmin.md) メソッドと [IMAPIProgress::GetMax](imapiprogress-getmax.md) メソッドのサービス プロバイダーにこれらの値を渡します。</span><span class="sxs-lookup"><span data-stu-id="51ecb-120">Use 1 for the initial minimum value and 1000 for the initial maximum value, passing these values to service providers in the [IMAPIProgress::GetMin](imapiprogress-getmin.md) and [IMAPIProgress::GetMax](imapiprogress-getmax.md) methods.</span></span> <span data-ttu-id="51ecb-121">サービス プロバイダーは [、IMAPIProgress::SetLimits を呼び出す際に、これらの値をリセットします](imapiprogress-setlimits.md)。</span><span class="sxs-lookup"><span data-stu-id="51ecb-121">Service providers reset these values when they call [IMAPIProgress::SetLimits](imapiprogress-setlimits.md).</span></span> 
  
<span data-ttu-id="51ecb-122">flags 値は、サービス プロバイダーが他の値を設定する方法を決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="51ecb-122">The flags value is used by service providers to determine how they should set the other values.</span></span> <span data-ttu-id="51ecb-123">フラグ値を初期化してMAPI_TOP_LEVEL **SetLimits** を呼び出してサービス プロバイダーがリセットするまで **GetFlags** の実装でこの値を返します。</span><span class="sxs-lookup"><span data-stu-id="51ecb-123">Initialize the flags value to MAPI_TOP_LEVEL and return this value in your implementation of **GetFlags** until the service provider resets it by calling **SetLimits**.</span></span> 
  
<span data-ttu-id="51ecb-124">**SetLimits** メソッドの実装では、各パラメーターのローカル コピー _(lpulMin、lpulMax、lpulFlags)_ を _保存します_。 </span><span class="sxs-lookup"><span data-stu-id="51ecb-124">In your implementation of the **SetLimits** method, save local copies of each of the parameters:  _lpulMin_,  _lpulMax_, and  _lpulFlags_.</span></span> <span data-ttu-id="51ecb-125">これらの値は、サービス プロバイダーが GetMin メソッド **、GetMax** メソッド、または **GetFlags** メソッドを呼び出す場合にすぐに使用できる必要があります。 </span><span class="sxs-lookup"><span data-stu-id="51ecb-125">These values should be readily available when a service provider calls your **GetMin**, **GetMax**, or **GetFlags** methods.</span></span> 
  
<span data-ttu-id="51ecb-126">進行状況インジケーターの表示を更新するために、サービス プロバイダーは **IMAPIProgress::P rogress** メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="51ecb-126">To update the display of the progress indicator, service providers call your **IMAPIProgress::Progress** method.</span></span> <span data-ttu-id="51ecb-127">このメソッドには、値、カウント、および合計の 3 つのパラメーターがあります。</span><span class="sxs-lookup"><span data-stu-id="51ecb-127">There are three parameters to this method: a value, a count, and a total.</span></span> <span data-ttu-id="51ecb-128">進行状況インジケーターを表示するには、最初のパラメーター  _ulValue_ を使用します。</span><span class="sxs-lookup"><span data-stu-id="51ecb-128">Use the first parameter,  _ulValue_, to display the progress indicator.</span></span> <span data-ttu-id="51ecb-129">_ulValue_ パラメーターは進行状況インジケーターであり、操作の開始時にのみグローバル _ulMin_ に、操作の完了時にのみグローバル _ulMax_ に等しくなります。</span><span class="sxs-lookup"><span data-stu-id="51ecb-129">The  _ulValue_ parameter is the progress indicator and will be equal to global  _ulMin_ only at the very beginning of the operation and equal to global  _ulMax_ only at the completion of the operation.</span></span> 
  
<span data-ttu-id="51ecb-130">2 番目と 3 番目のパラメーター  _ulCount_ と  _ulTotal_(使用可能な場合) を使用して、"10 から 5 アイテムが完了しました" などのオプションのメッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="51ecb-130">Use the second and third parameters,  _ulCount_ and  _ulTotal_, if available, to display an optional message such as "5 items completed out of 10."</span></span> <span data-ttu-id="51ecb-131">2 番目と 3 番目のパラメーターが 0 に設定されている場合は、進行状況インジケーターを視覚的に変更するかどうかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="51ecb-131">If the second and third parameters are set to 0, you can choose whether or not to visually change the progress indicator.</span></span> <span data-ttu-id="51ecb-132">一部のサービス プロバイダーは、親オブジェクトに対して進行状況を監視するサブオブジェクトを処理している場合に、これらのパラメーターを 0 に設定します。</span><span class="sxs-lookup"><span data-stu-id="51ecb-132">Some service providers set these parameters to zeroes to indicate that they are processing a subobject whose progress is monitored relative to a parent object.</span></span> <span data-ttu-id="51ecb-133">このような場合は、親オブジェクトが進行状況を報告した場合にのみ表示を変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="51ecb-133">In this situation, it makes sense to change the display only when the parent object reports progress.</span></span> <span data-ttu-id="51ecb-134">一部のサービス プロバイダーは、これらのパラメーターに対して毎回 0 を渡します。</span><span class="sxs-lookup"><span data-stu-id="51ecb-134">Some service providers pass zeroes for these parameters every time.</span></span> 
  

