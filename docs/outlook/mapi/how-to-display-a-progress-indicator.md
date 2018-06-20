---
title: 進行状況インジケーターを表示します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 20f5ad5a-b700-4fb5-9658-f71da5a06a12
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 3c4c553a000dab233eb208c1222cc427c97b1e70
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800228"
---
# <a name="display-a-progress-indicator"></a><span data-ttu-id="7efdd-103">進行状況インジケーターを表示します。</span><span class="sxs-lookup"><span data-stu-id="7efdd-103">Display a progress indicator</span></span>
 
<span data-ttu-id="7efdd-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7efdd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7efdd-105">進行状況インジケーターを表示するには、現在のフラグの設定を取得するために[IMAPIProgress::GetFlags](imapiprogress-getflags.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="7efdd-105">To display a progress indicator, call [IMAPIProgress::GetFlags](imapiprogress-getflags.md) to retrieve the current flags setting.</span></span> 
  
<span data-ttu-id="7efdd-106">MAPI_TOP_LEVEL フラグが設定されている場合は、次の手順に行います。</span><span class="sxs-lookup"><span data-stu-id="7efdd-106">If the MAPI_TOP_LEVEL flag is set, complete the following steps:</span></span>
  
1. <span data-ttu-id="7efdd-107">操作で処理する項目の合計数を変数に格納に設定します。</span><span class="sxs-lookup"><span data-stu-id="7efdd-107">Set a variable equal to the total number of items to process in the operation.</span></span> <span data-ttu-id="7efdd-108">たとえば、フォルダーの内容をコピーする場合この値は、フォルダー内のサブフォルダーの数とメッセージの数と等しいのようになります。</span><span class="sxs-lookup"><span data-stu-id="7efdd-108">For example, if you are copying the contents of a folder, this value will be equal to the number of the subfolders in the folder plus the number of messages.</span></span> 
    
2. <span data-ttu-id="7efdd-109">1000 の項目の数で割った値を変数に格納を設定します。</span><span class="sxs-lookup"><span data-stu-id="7efdd-109">Set a variable equal to 1000 divided by the number of items.</span></span> 
    
3. <span data-ttu-id="7efdd-110">サブオブジェクトの進行状況を表示する場合、進行中のオブジェクトの[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)メソッドを呼び出すし、次の 3 つのパラメーターの値を渡します。</span><span class="sxs-lookup"><span data-stu-id="7efdd-110">If you are showing progress for subobjects, call the progress object's [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) method and pass the following values for the three parameters:</span></span> 
    
   - <span data-ttu-id="7efdd-111">_LpulMin_パラメーターを 0 に設定します。</span><span class="sxs-lookup"><span data-stu-id="7efdd-111">Set the  _lpulMin_ parameter to 0.</span></span> 
    
   - <span data-ttu-id="7efdd-112">_LpulMax_パラメーターを 1000 に設定します。</span><span class="sxs-lookup"><span data-stu-id="7efdd-112">Set the  _lpulMax_ parameter to 1000.</span></span> 
    
   - <span data-ttu-id="7efdd-113">_LpulFlags_パラメーターを MAPI_TOP_LEVEL に設定します。</span><span class="sxs-lookup"><span data-stu-id="7efdd-113">Set the  _lpulFlags_ parameter to MAPI_TOP_LEVEL.</span></span> 
    
4. <span data-ttu-id="7efdd-114">各オブジェクトを処理するには、次の手順を行います。</span><span class="sxs-lookup"><span data-stu-id="7efdd-114">For each object to be processed, complete the following steps:</span></span>
    
   1. <span data-ttu-id="7efdd-115">**IMAPIProgress::SetLimits**を呼び出すし、次の 3 つのパラメーターの値を渡します。</span><span class="sxs-lookup"><span data-stu-id="7efdd-115">Call **IMAPIProgress::SetLimits** and pass the following values for the three parameters:</span></span> 
      
     - <span data-ttu-id="7efdd-116">変数から 1 を引いた現在の項目を掛けた値 2 の手順で設定するには、 _lpulMin_パラメーターを設定します。</span><span class="sxs-lookup"><span data-stu-id="7efdd-116">Set the  _lpulMin_ parameter to the variable set in step 2 multiplied by the current item minus 1.</span></span> 
      
     - <span data-ttu-id="7efdd-117">手順 2 の現在のオブジェクトを掛けた値に設定する変数には、 _lpulMax_パラメーターを設定します。</span><span class="sxs-lookup"><span data-stu-id="7efdd-117">Set the  _lpulMax_ parameter to the variable set in step 2 multiplied by the current object.</span></span> 
      
     - <span data-ttu-id="7efdd-118">_LpulFlags_パラメーターを 0 に設定します。</span><span class="sxs-lookup"><span data-stu-id="7efdd-118">Set the  _lpulFlags_ parameter to 0.</span></span> 
      
   2. <span data-ttu-id="7efdd-119">このオブジェクトに対するすべての処理を行う必要がありますを実行します。</span><span class="sxs-lookup"><span data-stu-id="7efdd-119">Perform whatever processing should be done on this object.</span></span> <span data-ttu-id="7efdd-120">サブオブジェクト、サブオブジェクトの進行状況を表示する場合、メソッドの_lpProgress_パラメーターで進行中のオブジェクトへのポインターを渡します。</span><span class="sxs-lookup"><span data-stu-id="7efdd-120">If this is a subobject and you want to display progress on subobjects, pass a pointer to the progress object in the  _lpProgress_ parameter to the method.</span></span> 
      
   3. <span data-ttu-id="7efdd-121">[IMAPIProgress::Progress](imapiprogress-progress.md)を呼び出すし、次の 3 つのパラメーターの値を渡します。</span><span class="sxs-lookup"><span data-stu-id="7efdd-121">Call [IMAPIProgress::Progress](imapiprogress-progress.md) and pass the following values for the three parameters:</span></span> 
      
     - <span data-ttu-id="7efdd-122">手順 2 の現在のオブジェクトを掛けた値に設定する変数には、 _ulValue_パラメーターを設定します。</span><span class="sxs-lookup"><span data-stu-id="7efdd-122">Set the  _ulValue_ parameter to the variable set in step 2 multiplied by the current object.</span></span> 
      
     - <span data-ttu-id="7efdd-123">現在のオブジェクトには、 _ulCount_パラメーターを設定します。</span><span class="sxs-lookup"><span data-stu-id="7efdd-123">Set the  _ulCount_ parameter to the current object.</span></span> 
      
     - <span data-ttu-id="7efdd-124">手順 1 のオブジェクトの合計数を設定する変数には、 _ulTotal_パラメーターを設定します。</span><span class="sxs-lookup"><span data-stu-id="7efdd-124">Set the  _ulTotal_ parameter to the variable set in step 1, the total number of objects.</span></span> 
    
<span data-ttu-id="7efdd-125">MAPI_TOP_LEVEL フラグが設定されていない場合は、次の手順に行います。</span><span class="sxs-lookup"><span data-stu-id="7efdd-125">If the MAPI_TOP_LEVEL flag is not set, complete the following steps:</span></span>
  
1. <span data-ttu-id="7efdd-126">表示の最小値を取得するために、実行中のオブジェクトの[IMAPIProgress::GetMin](imapiprogress-getmin.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="7efdd-126">Call the progress object's [IMAPIProgress::GetMin](imapiprogress-getmin.md) method to retrieve the minimum value for the display.</span></span> 
    
2. <span data-ttu-id="7efdd-127">表示の最大値を取得するために[IMAPIProgress::GetMax](imapiprogress-getmax.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="7efdd-127">Call [IMAPIProgress::GetMax](imapiprogress-getmax.md) to retrieve the maximum value for the display.</span></span> 
    
3. <span data-ttu-id="7efdd-128">変数に格納を処理するオブジェクトの合計数に設定します。</span><span class="sxs-lookup"><span data-stu-id="7efdd-128">Set a variable equal to the total number of objects to be processed.</span></span> 
    
4. <span data-ttu-id="7efdd-129">最大値から最小値を減算し、オブジェクトの合計数で除算して結果を変数に格納を設定します。</span><span class="sxs-lookup"><span data-stu-id="7efdd-129">Set a variable equal to the result of subtracting the minimum value from the maximum value and then dividing by the total number of objects.</span></span>
    
5. <span data-ttu-id="7efdd-130">各オブジェクトを処理するには、次の手順を行います。</span><span class="sxs-lookup"><span data-stu-id="7efdd-130">For each object to be processed, complete the following steps:</span></span>
    
   1. <span data-ttu-id="7efdd-131">プロバイダーには、サブオブジェクトの進行状況が表示されている場合**IMAPIProgress::SetLimits**を呼び出すし、次の 3 つのパラメーターの値を渡します。</span><span class="sxs-lookup"><span data-stu-id="7efdd-131">If your provider is showing progress for subobjects, call **IMAPIProgress::SetLimits** and pass the following values for the three parameters:</span></span> 
      
     - <span data-ttu-id="7efdd-132">_LpulMin_パラメーターを設定すると、最小値は、手順 4 で設定する変数を乗算した値 1 を引いた数値です。</span><span class="sxs-lookup"><span data-stu-id="7efdd-132">Set the  _lpulMin_ parameter to the minimum value plus the current item minus 1 multiplied by the variable set in step 4.</span></span> 
      
     - <span data-ttu-id="7efdd-133">_LpulMax_パラメーターを設定すると、最小値と現在の単位を手順 4 で設定する変数を乗算します。</span><span class="sxs-lookup"><span data-stu-id="7efdd-133">Set the  _lpulMax_ parameter to the minimum value plus the current unit multiplied by the variable set in step 4.</span></span> 
      
     - <span data-ttu-id="7efdd-134">_LpulFlags_パラメーターを 0 に設定します。</span><span class="sxs-lookup"><span data-stu-id="7efdd-134">Set the  _lpulFlags_ parameter to 0.</span></span> 
      
   2. <span data-ttu-id="7efdd-135">このオブジェクトに対するすべての処理を行う必要がありますを実行します。</span><span class="sxs-lookup"><span data-stu-id="7efdd-135">Perform whatever processing should be done on this object.</span></span> <span data-ttu-id="7efdd-136">オブジェクトには、サブオブジェクトと、プロバイダーには、下位オブジェクトの進行状況が表示されます、メソッドの_lpProgress_パラメーターで進行中のオブジェクトにポインターを渡します。</span><span class="sxs-lookup"><span data-stu-id="7efdd-136">If the object is a subobject, and your provider displays progress for subobjects, pass a pointer to the progress object in the  _lpProgress_ parameter to the method.</span></span> 
      
   3. <span data-ttu-id="7efdd-137">[IMAPIProgress::Progress](imapiprogress-progress.md)を呼び出すし、次の 3 つのパラメーターの値を渡します。</span><span class="sxs-lookup"><span data-stu-id="7efdd-137">Call [IMAPIProgress::Progress](imapiprogress-progress.md) and pass the following values for the three parameters:</span></span> 
      
     - <span data-ttu-id="7efdd-138">_UlValue_パラメーターを手順 2 の現在のオブジェクトを掛けた値に設定された変数に設定します。</span><span class="sxs-lookup"><span data-stu-id="7efdd-138">Set the  _ulValue_ parameter to variable set in step 2 multiplied by the current object.</span></span> 
      
     - <span data-ttu-id="7efdd-139">_UlCount_パラメーターを 0 に設定します。</span><span class="sxs-lookup"><span data-stu-id="7efdd-139">Set the  _ulCount_ parameter to 0.</span></span> 
      
     - <span data-ttu-id="7efdd-140">_UlTotal_パラメーターを 0 に設定します。</span><span class="sxs-lookup"><span data-stu-id="7efdd-140">Set the  _ulTotal_ parameter to 0.</span></span> 
    
<span data-ttu-id="7efdd-141">次のコード例は、5 つのサブフォルダーを含むフォルダーの内容をコピーする操作のすべてのレベルで進行状況を表示するために必要なロジックを示しています。</span><span class="sxs-lookup"><span data-stu-id="7efdd-141">The following code example illustrates the logic required to show progress at all levels of an operation that copies the contents of a folder that contains five subfolders.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="7efdd-142">関連項目</span><span class="sxs-lookup"><span data-stu-id="7efdd-142">See also</span></span>

- [<span data-ttu-id="7efdd-143">MAPI の進捗状況</span><span class="sxs-lookup"><span data-stu-id="7efdd-143">MAPI Progress Indicators</span></span>](mapi-progress-indicators.md)

