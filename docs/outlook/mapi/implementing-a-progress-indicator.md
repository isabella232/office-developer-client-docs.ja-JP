---
title: 進行状況のインジケーターを実装します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3a062a88-e87e-4c0c-944e-544a8f080930
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 767b8723d9a544a31ee5c4bbc1d6186a15387b44
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800915"
---
# <a name="implementing-a-progress-indicator"></a><span data-ttu-id="7ce3f-103">進行状況のインジケーターを実装します。</span><span class="sxs-lookup"><span data-stu-id="7ce3f-103">Implementing a Progress Indicator</span></span>

  
  
<span data-ttu-id="7ce3f-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7ce3f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7ce3f-105">多くのクライアントによって開始された操作により、かなりの時間がかかります。</span><span class="sxs-lookup"><span data-stu-id="7ce3f-105">Many of the operations initiated by clients take a significant amount of time.</span></span> <span data-ttu-id="7ce3f-106">進行中のオブジェクトへのポインターは、これらの可能性のある時間のかかる操作への入力パラメーターの 1 つ-を実装するオブジェクトの[IMAPIProgress: IUnknown](imapiprogressiunknown.md)インタ フェースです。</span><span class="sxs-lookup"><span data-stu-id="7ce3f-106">One of the input parameters to these potentially lengthy operations is a pointer to a progress object — an object that implements the [IMAPIProgress : IUnknown](imapiprogressiunknown.md) interface.</span></span> <span data-ttu-id="7ce3f-107">進行状況オブジェクトでは、進行状況インジケーターの表示と外観を制御してと MAPI クライアントによって実装されます。</span><span class="sxs-lookup"><span data-stu-id="7ce3f-107">Progress objects control the appearance and display of progress indicators and are implemented by clients and by MAPI.</span></span> <span data-ttu-id="7ce3f-108">進行中のオブジェクトを実装するかどうかを選択することができます。</span><span class="sxs-lookup"><span data-stu-id="7ce3f-108">You can choose whether or not to implement a progress object.</span></span> <span data-ttu-id="7ce3f-109">MAPI 実装は、実装を提供するように選択する場合に使用するサービス プロバイダーを使用できます。</span><span class="sxs-lookup"><span data-stu-id="7ce3f-109">The MAPI implementation is available for service providers to use if you elect not to supply an implementation.</span></span> 
  
<span data-ttu-id="7ce3f-110">進行中のオブジェクトは、次のどのデータを扱います。</span><span class="sxs-lookup"><span data-stu-id="7ce3f-110">Progress objects work with the following pieces of data:</span></span>
  
- <span data-ttu-id="7ce3f-111">グローバル最小値、 [IMAPIProgress::Progress](imapiprogress-progress.md)メソッドが呼び出されるは、 _ulValue_パラメーターの値以下である必要があります。</span><span class="sxs-lookup"><span data-stu-id="7ce3f-111">A global minimum value which, when your [IMAPIProgress::Progress](imapiprogress-progress.md) method is called, should be less than or equal to the value of the  _ulValue_ parameter.</span></span> <span data-ttu-id="7ce3f-112">操作の先頭には、 _ulValue_をこの最小値と等しくなります。</span><span class="sxs-lookup"><span data-stu-id="7ce3f-112">At the beginning of the operation,  _ulValue_ will be equal to this minimum value.</span></span> 
    
- <span data-ttu-id="7ce3f-113">**IMAPIProgress::Progress**メソッドが呼び出されると、必要があります以上の_ulValue_パラメーターに値をグローバルな最大値です。</span><span class="sxs-lookup"><span data-stu-id="7ce3f-113">A global maximum value which, when your **IMAPIProgress::Progress** method is called, should be greater than or equal to the  _ulValue_ parameter.</span></span> <span data-ttu-id="7ce3f-114">操作の最後に、 _ulValue_がこの最大値に等しくなります。</span><span class="sxs-lookup"><span data-stu-id="7ce3f-114">At the end of the operation,  _ulValue_ will be equal to this maximum value.</span></span> 
    
- <span data-ttu-id="7ce3f-115">フラグは、上に進行状況が対応しているかどうかを示す値または項目レベルを下げます。</span><span class="sxs-lookup"><span data-stu-id="7ce3f-115">A flags value which indicates whether the progress corresponds to a top or lower level item.</span></span>
    
- <span data-ttu-id="7ce3f-116">操作の進行中の現在のレベルを示す値。</span><span class="sxs-lookup"><span data-stu-id="7ce3f-116">A value that indicates the current level of progress for the operation.</span></span>
    
- <span data-ttu-id="7ce3f-117">合計を基準にして現在処理されたアイテムの数です。</span><span class="sxs-lookup"><span data-stu-id="7ce3f-117">The number of the currently processed items relative to the total.</span></span>
    
- <span data-ttu-id="7ce3f-118">操作中に処理する品目の合計数です。</span><span class="sxs-lookup"><span data-stu-id="7ce3f-118">The total number of items to be processed during the operation.</span></span>
    
<span data-ttu-id="7ce3f-119">最小値と最大値は、先頭と末尾の数値形式での操作を表します。</span><span class="sxs-lookup"><span data-stu-id="7ce3f-119">The minimum and maximum values represent the beginning and end of the operation in numeric form.</span></span> <span data-ttu-id="7ce3f-120">初期の最小値と、 [IMAPIProgress::GetMin](imapiprogress-getmin.md)メソッドと[IMAPIProgress::GetMax](imapiprogress-getmax.md)メソッドのサービス プロバイダーにこれらの値を渡すこと、初期の最大値の 1000 の 1 を使用します。</span><span class="sxs-lookup"><span data-stu-id="7ce3f-120">Use 1 for the initial minimum value and 1000 for the initial maximum value, passing these values to service providers in the [IMAPIProgress::GetMin](imapiprogress-getmin.md) and [IMAPIProgress::GetMax](imapiprogress-getmax.md) methods.</span></span> <span data-ttu-id="7ce3f-121">サービス プロバイダーは、 [IMAPIProgress::SetLimits](imapiprogress-setlimits.md)を呼び出すときに、これらの値をリセットします。</span><span class="sxs-lookup"><span data-stu-id="7ce3f-121">Service providers reset these values when they call [IMAPIProgress::SetLimits](imapiprogress-setlimits.md).</span></span> 
  
<span data-ttu-id="7ce3f-122">フラグ値は、他の値を設定する必要がある方法を決定するのには、サービス プロバイダーによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="7ce3f-122">The flags value is used by service providers to determine how they should set the other values.</span></span> <span data-ttu-id="7ce3f-123">MAPI_TOP_LEVEL するフラグ値を初期化し、 **SetLimits**を呼び出すことにより、サービス プロバイダーがリセットするまで、 **GetFlags**の実装では、この値を返します。</span><span class="sxs-lookup"><span data-stu-id="7ce3f-123">Initialize the flags value to MAPI_TOP_LEVEL and return this value in your implementation of **GetFlags** until the service provider resets it by calling **SetLimits**.</span></span> 
  
<span data-ttu-id="7ce3f-124">**SetLimits**メソッドの実装で、各パラメーターのローカル コピーを保存します: _lpulMin_、 _lpulMax_、および_lpulFlags_。</span><span class="sxs-lookup"><span data-stu-id="7ce3f-124">In your implementation of the **SetLimits** method, save local copies of each of the parameters:  _lpulMin_,  _lpulMax_, and  _lpulFlags_.</span></span> <span data-ttu-id="7ce3f-125">これらの値は、サービス プロバイダーは、 **GetMin**、 **GetMax**、または**GetFlags**メソッドを呼び出すと、すぐに利用できることがあります。</span><span class="sxs-lookup"><span data-stu-id="7ce3f-125">These values should be readily available when a service provider calls your **GetMin**, **GetMax**, or **GetFlags** methods.</span></span> 
  
<span data-ttu-id="7ce3f-126">進行状況インジケーターの表示を更新するには、サービス プロバイダーは、 **IMAPIProgress::Progress**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="7ce3f-126">To update the display of the progress indicator, service providers call your **IMAPIProgress::Progress** method.</span></span> <span data-ttu-id="7ce3f-127">このメソッドを次の 3 つのパラメーター: 値、カウント、および合計。</span><span class="sxs-lookup"><span data-stu-id="7ce3f-127">There are three parameters to this method: a value, a count, and a total.</span></span> <span data-ttu-id="7ce3f-128">進行状況インジケーターを表示するには、最初のパラメーターでは、 _ulValue_を使用します。</span><span class="sxs-lookup"><span data-stu-id="7ce3f-128">Use the first parameter,  _ulValue_, to display the progress indicator.</span></span> <span data-ttu-id="7ce3f-129">_UlValue_パラメーターでは、進行状況のインジケーターし、 _ulMin_グローバル操作の先頭に、かつ、操作の完了時にのみグローバルの_ulMax_と同じになります。</span><span class="sxs-lookup"><span data-stu-id="7ce3f-129">The  _ulValue_ parameter is the progress indicator and will be equal to global  _ulMin_ only at the very beginning of the operation and equal to global  _ulMax_ only at the completion of the operation.</span></span> 
  
<span data-ttu-id="7ce3f-130">「5 アイテム 10 個が完了した」などのオプションのメッセージを表示するのには、利用可能な場合は、2 番目と 3 番目のパラメーター、 _ulCount_ _ulTotal_を使用してください。</span><span class="sxs-lookup"><span data-stu-id="7ce3f-130">Use the second and third parameters,  _ulCount_ and  _ulTotal_, if available, to display an optional message such as "5 items completed out of 10."</span></span> <span data-ttu-id="7ce3f-131">2 番目と 3 番目のパラメーターを 0 に設定されている場合は、進行状況を視覚的に変更するかどうかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="7ce3f-131">If the second and third parameters are set to 0, you can choose whether or not to visually change the progress indicator.</span></span> <span data-ttu-id="7ce3f-132">サービス プロバイダーによっては、サブオブジェクトの進行状況は、親オブジェクトを基準にして処理することを示すためにゼロにこれらのパラメーターを設定します。</span><span class="sxs-lookup"><span data-stu-id="7ce3f-132">Some service providers set these parameters to zeroes to indicate that they are processing a subobject whose progress is monitored relative to a parent object.</span></span> <span data-ttu-id="7ce3f-133">このような状況は、親オブジェクトの進行状況を報告する場合にのみ、表示を変更します。</span><span class="sxs-lookup"><span data-stu-id="7ce3f-133">In this situation, it makes sense to change the display only when the parent object reports progress.</span></span> <span data-ttu-id="7ce3f-134">サービス プロバイダーによっては、毎回これらのパラメーターに 0 を渡します。</span><span class="sxs-lookup"><span data-stu-id="7ce3f-134">Some service providers pass zeroes for these parameters every time.</span></span> 
  

