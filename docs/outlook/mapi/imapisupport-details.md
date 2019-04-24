---
title: imapisupportdetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.Details
api_type:
- COM
ms.assetid: 1a62efa2-dd6b-4acb-a760-defa601c20c9
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: bdc57a6e951e54640fe3c638977c6a5f16986e68
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322359"
---
# <a name="imapisupportdetails"></a><span data-ttu-id="b958f-103">IMAPISupport::Details</span><span class="sxs-lookup"><span data-stu-id="b958f-103">IMAPISupport::Details</span></span>

  
  
<span data-ttu-id="b958f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b958f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b958f-105">特定のアドレス帳エントリの詳細を表示するダイアログボックスを表示します。</span><span class="sxs-lookup"><span data-stu-id="b958f-105">Displays a dialog box that shows details about a particular address book entry.</span></span>
  
```cpp
HRESULT Details(
  ULONG_PTR FAR * lpulUIParam,
  LPFNDISMISS lpfnDismiss,
  LPVOID lpvDismissContext,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPFNBUTTON lpfButtonCallback,
  LPVOID lpvButtonContext,
  LPSTR lpszButtonText,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="b958f-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b958f-106">Parameters</span></span>

 <span data-ttu-id="b958f-107">_l出 uiparam_</span><span class="sxs-lookup"><span data-stu-id="b958f-107">_lpulUIParam_</span></span>
  
> <span data-ttu-id="b958f-108">読み上げ返されたダイアログボックスの親ウィンドウへのハンドルへのポインター。</span><span class="sxs-lookup"><span data-stu-id="b958f-108">[out] A pointer to the handle to the parent window of the returned dialog box.</span></span>
    
 <span data-ttu-id="b958f-109">_lpfnDismiss_</span><span class="sxs-lookup"><span data-stu-id="b958f-109">_lpfnDismiss_</span></span>
  
> <span data-ttu-id="b958f-110">順番[DISMISSMODELESS](dismissmodeless.md)プロトタイプに基づく関数へのポインター、または NULL。</span><span class="sxs-lookup"><span data-stu-id="b958f-110">[in] A pointer to a function based on the [DISMISSMODELESS](dismissmodeless.md) prototype, or NULL.</span></span> <span data-ttu-id="b958f-111">このメンバーは、DIALOG_SDI フラグが設定されている場合のように、ダイアログボックスのモードレスバージョンにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="b958f-111">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="b958f-112">MAPI は、ユーザーがモードレスアドレスダイアログボックスを閉じたときに**DISMISSMODELESS**関数を呼び出し、imapisupport を呼び出していることをクライアントに通知し**ます。 etails**は、このダイアログボックスがアクティブでなくなったことを示します。</span><span class="sxs-lookup"><span data-stu-id="b958f-112">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client that is calling **IMAPISupport::Details** that the dialog box is no longer active.</span></span> 
    
 <span data-ttu-id="b958f-113">_lpvDismissContext_</span><span class="sxs-lookup"><span data-stu-id="b958f-113">_lpvDismissContext_</span></span>
  
> <span data-ttu-id="b958f-114">順番_lpfnDismiss_パラメーターが指す**DISMISSMODELESS**関数に渡すコンテキスト情報へのポインター。</span><span class="sxs-lookup"><span data-stu-id="b958f-114">[in] A pointer to context information to pass to the **DISMISSMODELESS** function pointed to by the  _lpfnDismiss_ parameter.</span></span> <span data-ttu-id="b958f-115">このパラメーターは、DIALOG_SDI フラグを_ulflags_パラメーターに含めることによって、ダイアログボックスのモードレスバージョンにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="b958f-115">This parameter applies only to the modeless version of the dialog box, by including the DIALOG_SDI flag in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="b958f-116">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="b958f-116">_cbEntryID_</span></span>
  
> <span data-ttu-id="b958f-117">順番_lな tryid_パラメーターで指定されたエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="b958f-117">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="b958f-118">_lて tryid_</span><span class="sxs-lookup"><span data-stu-id="b958f-118">_lpEntryID_</span></span>
  
> <span data-ttu-id="b958f-119">順番詳細が表示されるエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="b958f-119">[in] A pointer to the entry identifier for which details are displayed.</span></span>
    
 <span data-ttu-id="b958f-120">_lpfbuttoncallback_</span><span class="sxs-lookup"><span data-stu-id="b958f-120">_lpfButtonCallback_</span></span>
  
> <span data-ttu-id="b958f-121">順番[LPFNBUTTON](lpfnbutton.md)関数プロトタイプに基づく関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="b958f-121">[in] A pointer to a function based on the [LPFNBUTTON](lpfnbutton.md) function prototype.</span></span> <span data-ttu-id="b958f-122">**LPFNBUTTON**関数は、[詳細] ダイアログボックスにボタンを追加します。</span><span class="sxs-lookup"><span data-stu-id="b958f-122">An **LPFNBUTTON** function adds a button to the details dialog box.</span></span> 
    
 <span data-ttu-id="b958f-123">_lpvbuttoncontext_</span><span class="sxs-lookup"><span data-stu-id="b958f-123">_lpvButtonContext_</span></span>
  
> <span data-ttu-id="b958f-124">順番_lpfbuttoncallback_パラメーターで指定された関数のパラメーターとして使用されるデータへのポインター。</span><span class="sxs-lookup"><span data-stu-id="b958f-124">[in] A pointer to data used as a parameter for the function specified by the  _lpfButtonCallback_ parameter.</span></span> 
    
 <span data-ttu-id="b958f-125">_lpszbuttontext_</span><span class="sxs-lookup"><span data-stu-id="b958f-125">_lpszButtonText_</span></span>
  
> <span data-ttu-id="b958f-126">順番追加されたボタンが拡張可能な場合に、そのボタンに適用されるテキストを含む文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="b958f-126">[in] A pointer to a string that contains text to be applied to the added button if that button is extensible.</span></span> <span data-ttu-id="b958f-127">拡張ボタンを必要としない場合は、 _lpszbuttontext_パラメーターを NULL に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b958f-127">The  _lpszButtonText_ parameter should be NULL if an extensible button is not needed.</span></span> 
    
 <span data-ttu-id="b958f-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b958f-128">_ulFlags_</span></span>
  
> <span data-ttu-id="b958f-129">順番_lpszbuttontext_パラメーターのテキストの種類を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="b958f-129">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="b958f-130">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="b958f-130">The following flag can be set:</span></span> 
    
<span data-ttu-id="b958f-131">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="b958f-131">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="b958f-132">[共通アドレス] ダイアログボックスのモーダルバージョンを表示します。</span><span class="sxs-lookup"><span data-stu-id="b958f-132">Display the modal version of the common address dialog box.</span></span> <span data-ttu-id="b958f-133">このフラグは、DIALOG_SDI とは相互に排他的です。</span><span class="sxs-lookup"><span data-stu-id="b958f-133">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="b958f-134">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="b958f-134">DIALOG_SDI</span></span>
  
>  <span data-ttu-id="b958f-135">[共通アドレス] ダイアログボックスのモードレスバージョンを表示します。</span><span class="sxs-lookup"><span data-stu-id="b958f-135">Display the modeless version of the common address dialog box.</span></span> <span data-ttu-id="b958f-136">このフラグは、DIALOG_MODAL とは相互に排他的です。</span><span class="sxs-lookup"><span data-stu-id="b958f-136">This flag is mutually exclusive with DIALOG_MODAL.</span></span> 
    
<span data-ttu-id="b958f-137">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b958f-137">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="b958f-138">渡された文字列は Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="b958f-138">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="b958f-139">MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="b958f-139">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b958f-140">戻り値</span><span class="sxs-lookup"><span data-stu-id="b958f-140">Return value</span></span>

<span data-ttu-id="b958f-141">S_OK</span><span class="sxs-lookup"><span data-stu-id="b958f-141">S_OK</span></span> 
  
> <span data-ttu-id="b958f-142">アドレス帳エントリに対して [詳細] ダイアログボックスが正常に表示されました。</span><span class="sxs-lookup"><span data-stu-id="b958f-142">The details dialog box was successfully displayed for the address book entry.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b958f-143">解説</span><span class="sxs-lookup"><span data-stu-id="b958f-143">Remarks</span></span>

<span data-ttu-id="b958f-144">**imapisupport::D etails**メソッドは、アドレス帳プロバイダーサポートオブジェクトに対して実装されています。</span><span class="sxs-lookup"><span data-stu-id="b958f-144">The **IMAPISupport::Details** method is implemented for address book provider support objects.</span></span> <span data-ttu-id="b958f-145">アドレス帳プロバイダーは、アドレス帳の特定のエントリに関する詳細情報を表示するダイアログボックスを表示するために呼び出す**詳細情報**を提供します。</span><span class="sxs-lookup"><span data-stu-id="b958f-145">Address book providers call **Details** to display a dialog box that gives details on a particular entry in the address book.</span></span> <span data-ttu-id="b958f-146">_lpfbuttoncallback_、 _lpfbuttoncallback_、および_lpszbuttontext_パラメーターを使用して、クライアント定義ボタンをダイアログボックスに追加できます。</span><span class="sxs-lookup"><span data-stu-id="b958f-146">The  _lpfButtonCallback_,  _lpvButtonContext_, and  _lpszButtonText_ parameters can be used to add a client-defined button to the dialog box.</span></span> <span data-ttu-id="b958f-147">ボタンがクリックされると、MAPI は_lpfbuttoncallback_が指すコールバック関数を呼び出し、ボタンのエントリ識別子と_lpfbuttoncallback_のデータの両方を渡します。</span><span class="sxs-lookup"><span data-stu-id="b958f-147">When the button is clicked, MAPI calls the callback function pointed to by  _lpfButtonCallback_, passing both the entry identifier of the button and the data in  _lpvButtonContext_.</span></span> <span data-ttu-id="b958f-148">拡張ボタンが必要ない場合は、 _lpszbuttontext_を NULL にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b958f-148">If an extensible button is not needed,  _lpszButtonText_ should be NULL.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b958f-149">関連項目</span><span class="sxs-lookup"><span data-stu-id="b958f-149">See also</span></span>



[<span data-ttu-id="b958f-150">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="b958f-150">ADRPARM</span></span>](adrparm.md)
  
[<span data-ttu-id="b958f-151">IMAPISupport::Address</span><span class="sxs-lookup"><span data-stu-id="b958f-151">IMAPISupport::Address</span></span>](imapisupport-address.md)
  
[<span data-ttu-id="b958f-152">LPFNBUTTON</span><span class="sxs-lookup"><span data-stu-id="b958f-152">LPFNBUTTON</span></span>](lpfnbutton.md)
  
[<span data-ttu-id="b958f-153">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="b958f-153">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

