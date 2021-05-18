---
title: 進行状況インジケーターを表示する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 20f5ad5a-b700-4fb5-9658-f71da5a06a12
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 7b0ce0ab75ffdce045ccde5bf6ea8a7da046f463
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408027"
---
# <a name="display-a-progress-indicator"></a><span data-ttu-id="06a24-103">進行状況インジケーターを表示する</span><span class="sxs-lookup"><span data-stu-id="06a24-103">Display a progress indicator</span></span>
 
<span data-ttu-id="06a24-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="06a24-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="06a24-105">進行状況インジケーターを表示するには [、IMAPIProgress::GetFlags](imapiprogress-getflags.md) を呼び出して、現在のフラグ設定を取得します。</span><span class="sxs-lookup"><span data-stu-id="06a24-105">To display a progress indicator, call [IMAPIProgress::GetFlags](imapiprogress-getflags.md) to retrieve the current flags setting.</span></span> 
  
<span data-ttu-id="06a24-106">このフラグMAPI_TOP_LEVEL設定されている場合は、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="06a24-106">If the MAPI_TOP_LEVEL flag is set, complete the following steps:</span></span>
  
1. <span data-ttu-id="06a24-107">操作で処理するアイテムの総数に等しい変数を設定します。</span><span class="sxs-lookup"><span data-stu-id="06a24-107">Set a variable equal to the total number of items to process in the operation.</span></span> <span data-ttu-id="06a24-108">たとえば、フォルダーの内容をコピーする場合、この値はフォルダー内のサブフォルダーの数とメッセージの数と等しくなります。</span><span class="sxs-lookup"><span data-stu-id="06a24-108">For example, if you are copying the contents of a folder, this value will be equal to the number of the subfolders in the folder plus the number of messages.</span></span> 
    
2. <span data-ttu-id="06a24-109">変数を項目数で割った値を 1000 に設定します。</span><span class="sxs-lookup"><span data-stu-id="06a24-109">Set a variable equal to 1000 divided by the number of items.</span></span> 
    
3. <span data-ttu-id="06a24-110">サブオブジェクトの進行状況を表示する場合は、progress オブジェクトの [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) メソッドを呼び出し、3 つのパラメーターに次の値を渡します。</span><span class="sxs-lookup"><span data-stu-id="06a24-110">If you are showing progress for subobjects, call the progress object's [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) method and pass the following values for the three parameters:</span></span> 
    
   - <span data-ttu-id="06a24-111">_lpulMin パラメーターを_ 0 に設定します。</span><span class="sxs-lookup"><span data-stu-id="06a24-111">Set the  _lpulMin_ parameter to 0.</span></span> 
    
   - <span data-ttu-id="06a24-112">_lpulMax パラメーターを_ 1000 に設定します。</span><span class="sxs-lookup"><span data-stu-id="06a24-112">Set the  _lpulMax_ parameter to 1000.</span></span> 
    
   - <span data-ttu-id="06a24-113">_lpulFlags_ パラメーターを次の値MAPI_TOP_LEVEL。</span><span class="sxs-lookup"><span data-stu-id="06a24-113">Set the  _lpulFlags_ parameter to MAPI_TOP_LEVEL.</span></span> 
    
4. <span data-ttu-id="06a24-114">処理するオブジェクトごとに、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="06a24-114">For each object to be processed, complete the following steps:</span></span>
    
   1. <span data-ttu-id="06a24-115">**IMAPIProgress::SetLimits** を呼び出し、3 つのパラメーターに次の値を渡します。</span><span class="sxs-lookup"><span data-stu-id="06a24-115">Call **IMAPIProgress::SetLimits** and pass the following values for the three parameters:</span></span> 
      
     - <span data-ttu-id="06a24-116">手順 2 の変数セットに  _lpulMin_ パラメーターを設定し、現在の項目から 1 を引いた値を乗算します。</span><span class="sxs-lookup"><span data-stu-id="06a24-116">Set the  _lpulMin_ parameter to the variable set in step 2 multiplied by the current item minus 1.</span></span> 
      
     - <span data-ttu-id="06a24-117">_lpulMax パラメーターを_、手順 2 の変数セットに現在のオブジェクトを掛けた値に設定します。</span><span class="sxs-lookup"><span data-stu-id="06a24-117">Set the  _lpulMax_ parameter to the variable set in step 2 multiplied by the current object.</span></span> 
      
     - <span data-ttu-id="06a24-118">_lpulFlags パラメーターを_ 0 に設定します。</span><span class="sxs-lookup"><span data-stu-id="06a24-118">Set the  _lpulFlags_ parameter to 0.</span></span> 
      
   2. <span data-ttu-id="06a24-119">このオブジェクトに対して実行する必要がある処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="06a24-119">Perform whatever processing should be done on this object.</span></span> <span data-ttu-id="06a24-120">これがサブオブジェクトであり、サブオブジェクトに進行状況を表示する場合は  _、lpProgress_ パラメーターの progress オブジェクトへのポインターをメソッドに渡します。</span><span class="sxs-lookup"><span data-stu-id="06a24-120">If this is a subobject and you want to display progress on subobjects, pass a pointer to the progress object in the  _lpProgress_ parameter to the method.</span></span> 
      
   3. <span data-ttu-id="06a24-121">[IMAPIProgress::P rogress を](imapiprogress-progress.md)呼び出し、3 つのパラメーターに対して次の値を渡します。</span><span class="sxs-lookup"><span data-stu-id="06a24-121">Call [IMAPIProgress::Progress](imapiprogress-progress.md) and pass the following values for the three parameters:</span></span> 
      
     - <span data-ttu-id="06a24-122">手順 2 で設定した変数に、現在のオブジェクトを乗算して  _、ulValue_ パラメーターを設定します。</span><span class="sxs-lookup"><span data-stu-id="06a24-122">Set the  _ulValue_ parameter to the variable set in step 2 multiplied by the current object.</span></span> 
      
     - <span data-ttu-id="06a24-123">_ulCount パラメーターを_ 現在のオブジェクトに設定します。</span><span class="sxs-lookup"><span data-stu-id="06a24-123">Set the  _ulCount_ parameter to the current object.</span></span> 
      
     - <span data-ttu-id="06a24-124">_ulTotal パラメーターを_、手順 1 の変数セット 、オブジェクトの総数に設定します。</span><span class="sxs-lookup"><span data-stu-id="06a24-124">Set the  _ulTotal_ parameter to the variable set in step 1, the total number of objects.</span></span> 
    
<span data-ttu-id="06a24-125">このフラグMAPI_TOP_LEVEL設定されていない場合は、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="06a24-125">If the MAPI_TOP_LEVEL flag is not set, complete the following steps:</span></span>
  
1. <span data-ttu-id="06a24-126">進行状況オブジェクトの [IMAPIProgress::GetMin](imapiprogress-getmin.md) メソッドを呼び出して、表示の最小値を取得します。</span><span class="sxs-lookup"><span data-stu-id="06a24-126">Call the progress object's [IMAPIProgress::GetMin](imapiprogress-getmin.md) method to retrieve the minimum value for the display.</span></span> 
    
2. <span data-ttu-id="06a24-127">[IMAPIProgress::GetMax](imapiprogress-getmax.md)を呼び出して、表示の最大値を取得します。</span><span class="sxs-lookup"><span data-stu-id="06a24-127">Call [IMAPIProgress::GetMax](imapiprogress-getmax.md) to retrieve the maximum value for the display.</span></span> 
    
3. <span data-ttu-id="06a24-128">処理するオブジェクトの総数に等しい変数を設定します。</span><span class="sxs-lookup"><span data-stu-id="06a24-128">Set a variable equal to the total number of objects to be processed.</span></span> 
    
4. <span data-ttu-id="06a24-129">最大値から最小値を減算し、オブジェクトの総数で割った結果と等しい変数を設定します。</span><span class="sxs-lookup"><span data-stu-id="06a24-129">Set a variable equal to the result of subtracting the minimum value from the maximum value and then dividing by the total number of objects.</span></span>
    
5. <span data-ttu-id="06a24-130">処理するオブジェクトごとに、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="06a24-130">For each object to be processed, complete the following steps:</span></span>
    
   1. <span data-ttu-id="06a24-131">プロバイダーがサブオブジェクトの進行状況を表示している場合は **、IMAPIProgress::SetLimits** を呼び出し、3 つのパラメーターに次の値を渡します。</span><span class="sxs-lookup"><span data-stu-id="06a24-131">If your provider is showing progress for subobjects, call **IMAPIProgress::SetLimits** and pass the following values for the three parameters:</span></span> 
      
     - <span data-ttu-id="06a24-132">_lpulMin パラメーターに_、手順 4 で設定した変数に現在の項目から 1 を掛けた最小値を設定します。</span><span class="sxs-lookup"><span data-stu-id="06a24-132">Set the  _lpulMin_ parameter to the minimum value plus the current item minus 1 multiplied by the variable set in step 4.</span></span> 
      
     - <span data-ttu-id="06a24-133">_lpulMax パラメーターに_、手順 4 で設定した変数を乗算した現在の単位を加えた最小値を設定します。</span><span class="sxs-lookup"><span data-stu-id="06a24-133">Set the  _lpulMax_ parameter to the minimum value plus the current unit multiplied by the variable set in step 4.</span></span> 
      
     - <span data-ttu-id="06a24-134">_lpulFlags パラメーターを_ 0 に設定します。</span><span class="sxs-lookup"><span data-stu-id="06a24-134">Set the  _lpulFlags_ parameter to 0.</span></span> 
      
   2. <span data-ttu-id="06a24-135">このオブジェクトに対して実行する必要がある処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="06a24-135">Perform whatever processing should be done on this object.</span></span> <span data-ttu-id="06a24-136">オブジェクトがサブオブジェクトで、プロバイダーがサブオブジェクトの進行状況を表示する場合は  _、lpProgress_ パラメーターの progress オブジェクトへのポインターをメソッドに渡します。</span><span class="sxs-lookup"><span data-stu-id="06a24-136">If the object is a subobject, and your provider displays progress for subobjects, pass a pointer to the progress object in the  _lpProgress_ parameter to the method.</span></span> 
      
   3. <span data-ttu-id="06a24-137">[IMAPIProgress::P rogress を](imapiprogress-progress.md)呼び出し、3 つのパラメーターに対して次の値を渡します。</span><span class="sxs-lookup"><span data-stu-id="06a24-137">Call [IMAPIProgress::Progress](imapiprogress-progress.md) and pass the following values for the three parameters:</span></span> 
      
     - <span data-ttu-id="06a24-138">手順 2  _で現在_ のオブジェクトを乗算して、ulValue パラメーターを変数セットに設定します。</span><span class="sxs-lookup"><span data-stu-id="06a24-138">Set the  _ulValue_ parameter to variable set in step 2 multiplied by the current object.</span></span> 
      
     - <span data-ttu-id="06a24-139">_ulCount パラメーターを_ 0 に設定します。</span><span class="sxs-lookup"><span data-stu-id="06a24-139">Set the  _ulCount_ parameter to 0.</span></span> 
      
     - <span data-ttu-id="06a24-140">_ulTotal パラメーターを_ 0 に設定します。</span><span class="sxs-lookup"><span data-stu-id="06a24-140">Set the  _ulTotal_ parameter to 0.</span></span> 
    
<span data-ttu-id="06a24-141">次のコード例は、5 つのサブフォルダーを含むフォルダーの内容をコピーする操作のすべてのレベルで進行状況を表示するために必要なロジックを示しています。</span><span class="sxs-lookup"><span data-stu-id="06a24-141">The following code example illustrates the logic required to show progress at all levels of an operation that copies the contents of a folder that contains five subfolders.</span></span> 
  
```cpp
lpProgress->GetFlags (lpulFlags);
ulFlags = *lpulFlags;
/* The folder in charge of the display. It contains 5 subfolders. */
if (ulFlags & MAPI_TOP_LEVEL)
{
    ulItems = 5                         // 5 subfolders in this folder
    ulScale = (ulMax / ulItems)         // 200 because ulMax = 1000
    lpProgress->SetLimits(0, ulMax, MAPI_TOP_LEVEL)
    for (i = 1; i <= ulItems; i++)      // for each subfolder to copy
    {
        lpProgress->SetLimits( (i - 1) * ulScale, i * ulScale, 0)
        CopyOneFolder(lpFolder(i), lpProgress)
        lpProgress->Progress( i * ulScale, i, ulItems)
    }
}
else
/* One of the subfolders to be copied. It contains 3 messages. */
{
    lpProgress->GetMin(&ulMin);
    lpProgress->GetMax(&ulMax);
    ulItems = 3;
    ulDelta = (ulMax - ulMin) / ulItems;
    for (i = 1; i <= ulItems; i++)
    {
        lpProgress->SetLimits(ulMin + (i - 1) * ulDelta,
                              ulMin + i * ulDelta, 0)
        CopyOneFolder(lpFolder(i), lpProgress)
        /* Pass 0 for ulCount and ulTotal because this is not the */
        /* top-level display, and that information is unavailable  */
        lpProgress->Progress( i * ulDelta, 0, 0)
    }
}
 
```

## <a name="see-also"></a><span data-ttu-id="06a24-142">関連項目</span><span class="sxs-lookup"><span data-stu-id="06a24-142">See also</span></span>

- [<span data-ttu-id="06a24-143">MAPI 進行状況インジケーター</span><span class="sxs-lookup"><span data-stu-id="06a24-143">MAPI Progress Indicators</span></span>](mapi-progress-indicators.md)

