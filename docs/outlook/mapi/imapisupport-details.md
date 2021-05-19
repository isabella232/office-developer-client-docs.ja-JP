---
title: IMAPISupportDetails
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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426780"
---
# <a name="imapisupportdetails"></a><span data-ttu-id="74a9f-103">IMAPISupport::Details</span><span class="sxs-lookup"><span data-stu-id="74a9f-103">IMAPISupport::Details</span></span>

  
  
<span data-ttu-id="74a9f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="74a9f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="74a9f-105">特定のアドレス帳エントリに関する詳細を表示するダイアログ ボックスを表示します。</span><span class="sxs-lookup"><span data-stu-id="74a9f-105">Displays a dialog box that shows details about a particular address book entry.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="74a9f-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74a9f-106">Parameters</span></span>

 <span data-ttu-id="74a9f-107">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="74a9f-107">_lpulUIParam_</span></span>
  
> <span data-ttu-id="74a9f-108">[out]返されるダイアログ ボックスの親ウィンドウへのハンドルへのポインター。</span><span class="sxs-lookup"><span data-stu-id="74a9f-108">[out] A pointer to the handle to the parent window of the returned dialog box.</span></span>
    
 <span data-ttu-id="74a9f-109">_lpfnDismiss_</span><span class="sxs-lookup"><span data-stu-id="74a9f-109">_lpfnDismiss_</span></span>
  
> <span data-ttu-id="74a9f-110">[in] [DISMISSMODELESS](dismissmodeless.md) プロトタイプまたは NULL に基づく関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="74a9f-110">[in] A pointer to a function based on the [DISMISSMODELESS](dismissmodeless.md) prototype, or NULL.</span></span> <span data-ttu-id="74a9f-111">このメンバーは、設定されているオプション フラグで示されているモードレス DIALOG_SDIダイアログ ボックスにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="74a9f-111">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="74a9f-112">MAPI は、ユーザーがモードレス アドレス ダイアログ ボックスを閉じ **、IMAPISupport::D** ダイアログ ボックスがアクティブでなくなったことを示すクライアントに通知するときに **、DISMISSMODELESS** 関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="74a9f-112">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client that is calling **IMAPISupport::Details** that the dialog box is no longer active.</span></span> 
    
 <span data-ttu-id="74a9f-113">_lpvDismissContext_</span><span class="sxs-lookup"><span data-stu-id="74a9f-113">_lpvDismissContext_</span></span>
  
> <span data-ttu-id="74a9f-114">[in]_lpfnDismiss_ パラメーターが指す **DISMISSMODELESS** 関数に渡すコンテキスト情報へのポインター。</span><span class="sxs-lookup"><span data-stu-id="74a9f-114">[in] A pointer to context information to pass to the **DISMISSMODELESS** function pointed to by the  _lpfnDismiss_ parameter.</span></span> <span data-ttu-id="74a9f-115">このパラメーターは  _、ulFlags_ パラメーターに DIALOG_SDIフラグを含めて、ダイアログ ボックスのモードレス バージョンにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="74a9f-115">This parameter applies only to the modeless version of the dialog box, by including the DIALOG_SDI flag in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="74a9f-116">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="74a9f-116">_cbEntryID_</span></span>
  
> <span data-ttu-id="74a9f-117">[in]  _lpEntryID_ パラメーターが指すエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="74a9f-117">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="74a9f-118">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="74a9f-118">_lpEntryID_</span></span>
  
> <span data-ttu-id="74a9f-119">[in]詳細が表示されるエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="74a9f-119">[in] A pointer to the entry identifier for which details are displayed.</span></span>
    
 <span data-ttu-id="74a9f-120">_lpfButtonCallback_</span><span class="sxs-lookup"><span data-stu-id="74a9f-120">_lpfButtonCallback_</span></span>
  
> <span data-ttu-id="74a9f-121">[in] [LPFNBUTTON 関数プロトタイプに基づく関数への](lpfnbutton.md) ポインター。</span><span class="sxs-lookup"><span data-stu-id="74a9f-121">[in] A pointer to a function based on the [LPFNBUTTON](lpfnbutton.md) function prototype.</span></span> <span data-ttu-id="74a9f-122">**LPFNBUTTON 関数は**、詳細ダイアログ ボックスにボタンを追加します。</span><span class="sxs-lookup"><span data-stu-id="74a9f-122">An **LPFNBUTTON** function adds a button to the details dialog box.</span></span> 
    
 <span data-ttu-id="74a9f-123">_lpvButtonContext_</span><span class="sxs-lookup"><span data-stu-id="74a9f-123">_lpvButtonContext_</span></span>
  
> <span data-ttu-id="74a9f-124">[in]  _lpfButtonCallback_ パラメーターで指定された関数のパラメーターとして使用されるデータへのポインター。</span><span class="sxs-lookup"><span data-stu-id="74a9f-124">[in] A pointer to data used as a parameter for the function specified by the  _lpfButtonCallback_ parameter.</span></span> 
    
 <span data-ttu-id="74a9f-125">_lpszButtonText_</span><span class="sxs-lookup"><span data-stu-id="74a9f-125">_lpszButtonText_</span></span>
  
> <span data-ttu-id="74a9f-126">[in]そのボタンが拡張可能な場合、追加されたボタンに適用されるテキストを含む文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="74a9f-126">[in] A pointer to a string that contains text to be applied to the added button if that button is extensible.</span></span> <span data-ttu-id="74a9f-127">_拡張可能なボタンが必要ない場合、lpszButtonText_ パラメーターは NULL である必要があります。</span><span class="sxs-lookup"><span data-stu-id="74a9f-127">The  _lpszButtonText_ parameter should be NULL if an extensible button is not needed.</span></span> 
    
 <span data-ttu-id="74a9f-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="74a9f-128">_ulFlags_</span></span>
  
> <span data-ttu-id="74a9f-129">[in]  _lpszButtonText_ パラメーターのテキストの種類を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="74a9f-129">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="74a9f-130">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="74a9f-130">The following flag can be set:</span></span> 
    
<span data-ttu-id="74a9f-131">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="74a9f-131">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="74a9f-132">[共通アドレス] ダイアログ ボックスのモーダル バージョンを表示します。</span><span class="sxs-lookup"><span data-stu-id="74a9f-132">Display the modal version of the common address dialog box.</span></span> <span data-ttu-id="74a9f-133">このフラグは、このフラグと相互にDIALOG_SDI。</span><span class="sxs-lookup"><span data-stu-id="74a9f-133">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="74a9f-134">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="74a9f-134">DIALOG_SDI</span></span>
  
>  <span data-ttu-id="74a9f-135">[共通アドレス] ダイアログ ボックスのモードレス バージョンを表示します。</span><span class="sxs-lookup"><span data-stu-id="74a9f-135">Display the modeless version of the common address dialog box.</span></span> <span data-ttu-id="74a9f-136">このフラグは、他のフラグと相互DIALOG_MODAL。</span><span class="sxs-lookup"><span data-stu-id="74a9f-136">This flag is mutually exclusive with DIALOG_MODAL.</span></span> 
    
<span data-ttu-id="74a9f-137">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="74a9f-137">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="74a9f-138">渡された文字列は Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="74a9f-138">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="74a9f-139">このフラグMAPI_UNICODE設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="74a9f-139">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="74a9f-140">戻り値</span><span class="sxs-lookup"><span data-stu-id="74a9f-140">Return value</span></span>

<span data-ttu-id="74a9f-141">S_OK</span><span class="sxs-lookup"><span data-stu-id="74a9f-141">S_OK</span></span> 
  
> <span data-ttu-id="74a9f-142">アドレス帳エントリの詳細ダイアログ ボックスが正常に表示されました。</span><span class="sxs-lookup"><span data-stu-id="74a9f-142">The details dialog box was successfully displayed for the address book entry.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="74a9f-143">注釈</span><span class="sxs-lookup"><span data-stu-id="74a9f-143">Remarks</span></span>

<span data-ttu-id="74a9f-144">**IMAPISupport::D etails** メソッドは、アドレス帳プロバイダーのサポート オブジェクトに実装されます。</span><span class="sxs-lookup"><span data-stu-id="74a9f-144">The **IMAPISupport::Details** method is implemented for address book provider support objects.</span></span> <span data-ttu-id="74a9f-145">アドレス帳プロバイダーは、詳細を **呼** び出して、アドレス帳内の特定のエントリの詳細を示すダイアログ ボックスを表示します。</span><span class="sxs-lookup"><span data-stu-id="74a9f-145">Address book providers call **Details** to display a dialog box that gives details on a particular entry in the address book.</span></span> <span data-ttu-id="74a9f-146">_lpfButtonCallback_ パラメーター _、lpvButtonContext_ パラメーター、_および lpszButtonText_ パラメーターを使用して、ダイアログ ボックスにクライアント定義ボタンを追加できます。</span><span class="sxs-lookup"><span data-stu-id="74a9f-146">The  _lpfButtonCallback_,  _lpvButtonContext_, and  _lpszButtonText_ parameters can be used to add a client-defined button to the dialog box.</span></span> <span data-ttu-id="74a9f-147">ボタンをクリックすると、MAPI は  _lpfButtonCallback_ が指すコールバック関数を呼び出し、ボタンのエントリ識別子と  _lpvButtonContext_ のデータの両方を渡します。</span><span class="sxs-lookup"><span data-stu-id="74a9f-147">When the button is clicked, MAPI calls the callback function pointed to by  _lpfButtonCallback_, passing both the entry identifier of the button and the data in  _lpvButtonContext_.</span></span> <span data-ttu-id="74a9f-148">拡張可能なボタンが必要ない場合  _、lpszButtonText_ は NULL である必要があります。</span><span class="sxs-lookup"><span data-stu-id="74a9f-148">If an extensible button is not needed,  _lpszButtonText_ should be NULL.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="74a9f-149">関連項目</span><span class="sxs-lookup"><span data-stu-id="74a9f-149">See also</span></span>



[<span data-ttu-id="74a9f-150">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="74a9f-150">ADRPARM</span></span>](adrparm.md)
  
[<span data-ttu-id="74a9f-151">IMAPISupport::Address</span><span class="sxs-lookup"><span data-stu-id="74a9f-151">IMAPISupport::Address</span></span>](imapisupport-address.md)
  
[<span data-ttu-id="74a9f-152">LPFNBUTTON</span><span class="sxs-lookup"><span data-stu-id="74a9f-152">LPFNBUTTON</span></span>](lpfnbutton.md)
  
[<span data-ttu-id="74a9f-153">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="74a9f-153">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

