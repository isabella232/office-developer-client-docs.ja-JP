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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332852"
---
# <a name="implementing-a-progress-indicator"></a><span data-ttu-id="e6148-103">進行状況インジケーターの実装</span><span class="sxs-lookup"><span data-stu-id="e6148-103">Implementing a Progress Indicator</span></span>

  
  
<span data-ttu-id="e6148-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e6148-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e6148-105">クライアントによって開始される操作の多くには、かなりの時間がかかります。</span><span class="sxs-lookup"><span data-stu-id="e6148-105">Many of the operations initiated by clients take a significant amount of time.</span></span> <span data-ttu-id="e6148-106">このような長い時間がかかる可能性のある操作への入力パラメーターの1つは、progress オブジェクトへのポインターです。これは、 [imapiprogress: IUnknown](imapiprogressiunknown.md)インターフェイスを実装するオブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="e6148-106">One of the input parameters to these potentially lengthy operations is a pointer to a progress object — an object that implements the [IMAPIProgress : IUnknown](imapiprogressiunknown.md) interface.</span></span> <span data-ttu-id="e6148-107">progress オブジェクトは、進行状況インジケーターの表示と表示を制御し、クライアントと MAPI で実装されます。</span><span class="sxs-lookup"><span data-stu-id="e6148-107">Progress objects control the appearance and display of progress indicators and are implemented by clients and by MAPI.</span></span> <span data-ttu-id="e6148-108">progress オブジェクトを実装するかどうかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="e6148-108">You can choose whether or not to implement a progress object.</span></span> <span data-ttu-id="e6148-109">実装を提供しない場合は、サービスプロバイダーが MAPI 実装を使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="e6148-109">The MAPI implementation is available for service providers to use if you elect not to supply an implementation.</span></span> 
  
<span data-ttu-id="e6148-110">Progress オブジェクトは、次のデータを使用して機能します。</span><span class="sxs-lookup"><span data-stu-id="e6148-110">Progress objects work with the following pieces of data:</span></span>
  
- <span data-ttu-id="e6148-111">[imapiprogress::P rogress](imapiprogress-progress.md)メソッドが呼び出されたときに、 _ulvalue_パラメーターの値以下である必要がある、グローバルな最小値。</span><span class="sxs-lookup"><span data-stu-id="e6148-111">A global minimum value which, when your [IMAPIProgress::Progress](imapiprogress-progress.md) method is called, should be less than or equal to the value of the  _ulValue_ parameter.</span></span> <span data-ttu-id="e6148-112">操作の開始時に、 _ulvalue_はこの最小値と等しくなります。</span><span class="sxs-lookup"><span data-stu-id="e6148-112">At the beginning of the operation,  _ulValue_ will be equal to this minimum value.</span></span> 
    
- <span data-ttu-id="e6148-113">**imapiprogress::P rogress**メソッドが呼び出されるときに、 _ulvalue_パラメーター以上である必要があるグローバル最大値。</span><span class="sxs-lookup"><span data-stu-id="e6148-113">A global maximum value which, when your **IMAPIProgress::Progress** method is called, should be greater than or equal to the  _ulValue_ parameter.</span></span> <span data-ttu-id="e6148-114">操作の終了時に、 _ulvalue_はこの最大値と等しくなります。</span><span class="sxs-lookup"><span data-stu-id="e6148-114">At the end of the operation,  _ulValue_ will be equal to this maximum value.</span></span> 
    
- <span data-ttu-id="e6148-115">進捗状況が上位または下位レベルのアイテムに対応するかどうかを示すフラグ値。</span><span class="sxs-lookup"><span data-stu-id="e6148-115">A flags value which indicates whether the progress corresponds to a top or lower level item.</span></span>
    
- <span data-ttu-id="e6148-116">操作の現在の進行状況レベルを示す値。</span><span class="sxs-lookup"><span data-stu-id="e6148-116">A value that indicates the current level of progress for the operation.</span></span>
    
- <span data-ttu-id="e6148-117">現在処理されているアイテムの総数を基準としたアイテムの数。</span><span class="sxs-lookup"><span data-stu-id="e6148-117">The number of the currently processed items relative to the total.</span></span>
    
- <span data-ttu-id="e6148-118">操作中に処理されるアイテムの合計数。</span><span class="sxs-lookup"><span data-stu-id="e6148-118">The total number of items to be processed during the operation.</span></span>
    
<span data-ttu-id="e6148-119">最小値と最大値は、操作の開始と終了を数値形式で表します。</span><span class="sxs-lookup"><span data-stu-id="e6148-119">The minimum and maximum values represent the beginning and end of the operation in numeric form.</span></span> <span data-ttu-id="e6148-120">最初の最小値には1、最大値には1000を使用します。これらの値は、 [imapiprogress:: getmin](imapiprogress-getmin.md)および[imapiprogress:: getmin](imapiprogress-getmax.md)メソッドのサービスプロバイダーに渡されます。</span><span class="sxs-lookup"><span data-stu-id="e6148-120">Use 1 for the initial minimum value and 1000 for the initial maximum value, passing these values to service providers in the [IMAPIProgress::GetMin](imapiprogress-getmin.md) and [IMAPIProgress::GetMax](imapiprogress-getmax.md) methods.</span></span> <span data-ttu-id="e6148-121">サービスプロバイダー[は、imapiprogress:: setlimits](imapiprogress-setlimits.md)を呼び出したときに、これらの値をリセットします。</span><span class="sxs-lookup"><span data-stu-id="e6148-121">Service providers reset these values when they call [IMAPIProgress::SetLimits](imapiprogress-setlimits.md).</span></span> 
  
<span data-ttu-id="e6148-122">flags 値は、サービスプロバイダーが他の値をどのように設定するかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="e6148-122">The flags value is used by service providers to determine how they should set the other values.</span></span> <span data-ttu-id="e6148-123">flags 値を MAPI_TOP_LEVEL に初期化し、 **getflags**の実装で、 **setlimits**を呼び出してサービスプロバイダーがリセットするまでこの値を返します。</span><span class="sxs-lookup"><span data-stu-id="e6148-123">Initialize the flags value to MAPI_TOP_LEVEL and return this value in your implementation of **GetFlags** until the service provider resets it by calling **SetLimits**.</span></span> 
  
<span data-ttu-id="e6148-124">**setlimits**メソッドの実装では、各パラメーターのローカルコピーを_lルー min_、 _l出 max_、lアウトの各_フラグ_で保存します。</span><span class="sxs-lookup"><span data-stu-id="e6148-124">In your implementation of the **SetLimits** method, save local copies of each of the parameters:  _lpulMin_,  _lpulMax_, and  _lpulFlags_.</span></span> <span data-ttu-id="e6148-125">これらの値は、サービスプロバイダーが**getmin**、 **getmin**、または**getmin**メソッドを呼び出すときにすぐに使用できるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e6148-125">These values should be readily available when a service provider calls your **GetMin**, **GetMax**, or **GetFlags** methods.</span></span> 
  
<span data-ttu-id="e6148-126">進行状況インジケーターの表示を更新するために、サービスプロバイダーは imapiprogress を呼び出します。 **:P rogress** method。</span><span class="sxs-lookup"><span data-stu-id="e6148-126">To update the display of the progress indicator, service providers call your **IMAPIProgress::Progress** method.</span></span> <span data-ttu-id="e6148-127">このメソッドには、値、数、合計という3つのパラメーターがあります。</span><span class="sxs-lookup"><span data-stu-id="e6148-127">There are three parameters to this method: a value, a count, and a total.</span></span> <span data-ttu-id="e6148-128">最初のパラメーター _ulvalue_を使用して進行状況インジケーターを表示します。</span><span class="sxs-lookup"><span data-stu-id="e6148-128">Use the first parameter,  _ulValue_, to display the progress indicator.</span></span> <span data-ttu-id="e6148-129">_ulvalue_パラメーターは進行状況インジケーターで、操作の開始時にグローバル_ulvalue_のみになり、操作が完了したときにのみグローバル_ulvalue_に等しくなります。</span><span class="sxs-lookup"><span data-stu-id="e6148-129">The  _ulValue_ parameter is the progress indicator and will be equal to global  _ulMin_ only at the very beginning of the operation and equal to global  _ulMax_ only at the completion of the operation.</span></span> 
  
<span data-ttu-id="e6148-130">2番目および3番目のパラメーター [ _ulcount_ ] および [ _ulcount_] を使用して、"5 個のアイテムが完了しました" のようなオプションのメッセージを表示します (使用可能な場合)。</span><span class="sxs-lookup"><span data-stu-id="e6148-130">Use the second and third parameters,  _ulCount_ and  _ulTotal_, if available, to display an optional message such as "5 items completed out of 10."</span></span> <span data-ttu-id="e6148-131">2番目と3番目のパラメーターが0に設定されている場合は、進行状況インジケーターを視覚的に変更するかどうかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="e6148-131">If the second and third parameters are set to 0, you can choose whether or not to visually change the progress indicator.</span></span> <span data-ttu-id="e6148-132">一部のサービスプロバイダーでは、このパラメーターを0に設定して、進行状況が親オブジェクトに対して監視されているサブオブジェクトを処理していることを示します。</span><span class="sxs-lookup"><span data-stu-id="e6148-132">Some service providers set these parameters to zeroes to indicate that they are processing a subobject whose progress is monitored relative to a parent object.</span></span> <span data-ttu-id="e6148-133">このような状況では、親オブジェクトが進捗状況を報告する場合にのみ、表示を変更することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="e6148-133">In this situation, it makes sense to change the display only when the parent object reports progress.</span></span> <span data-ttu-id="e6148-134">一部のサービスプロバイダーでは、これらのパラメーターに対して常に0が渡されます。</span><span class="sxs-lookup"><span data-stu-id="e6148-134">Some service providers pass zeroes for these parameters every time.</span></span> 
  

