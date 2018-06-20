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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 9923813d821e2b34497e3b498c19ce22ceda2eb0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800728"
---
# <a name="imapisupportdetails"></a><span data-ttu-id="fbece-103">IMAPISupport::Details</span><span class="sxs-lookup"><span data-stu-id="fbece-103">IMAPISupport::Details</span></span>

  
  
<span data-ttu-id="fbece-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fbece-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fbece-105">特定のアドレス帳のエントリに関する詳細情報を表示するダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="fbece-105">Displays a dialog box that shows details about a particular address book entry.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="fbece-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="fbece-106">Parameters</span></span>

 <span data-ttu-id="fbece-107">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="fbece-107">_lpulUIParam_</span></span>
  
> <span data-ttu-id="fbece-108">[out]返されたダイアログ ボックスの親ウィンドウへのハンドルへのポインター。</span><span class="sxs-lookup"><span data-stu-id="fbece-108">[out] A pointer to the handle to the parent window of the returned dialog box.</span></span>
    
 <span data-ttu-id="fbece-109">_lpfnDismiss_</span><span class="sxs-lookup"><span data-stu-id="fbece-109">_lpfnDismiss_</span></span>
  
> <span data-ttu-id="fbece-110">[in][DISMISSMODELESS](dismissmodeless.md)のプロトタイプでは関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="fbece-110">[in] A pointer to a function based on the [DISMISSMODELESS](dismissmodeless.md) prototype, or NULL.</span></span> <span data-ttu-id="fbece-111">このメンバーは、DIALOG_SDI フラグが設定されている中で示されるように、モードレス ダイアログ ボックスのバージョンにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="fbece-111">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="fbece-112">MAPI 関数を呼び出す**DISMISSMODELESS**ユーザーが、アドレスのモードレス ダイアログ ボックスを閉じると、 **IMAPISupport::Details**ダイアログ ボックスがアクティブではないことを呼び出しているクライアントに通知します。</span><span class="sxs-lookup"><span data-stu-id="fbece-112">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client that is calling **IMAPISupport::Details** that the dialog box is no longer active.</span></span> 
    
 <span data-ttu-id="fbece-113">_lpvDismissContext_</span><span class="sxs-lookup"><span data-stu-id="fbece-113">_lpvDismissContext_</span></span>
  
> <span data-ttu-id="fbece-114">[in]_LpfnDismiss_パラメーターが指す、 **DISMISSMODELESS**関数に渡すコンテキスト情報へのポインターです。</span><span class="sxs-lookup"><span data-stu-id="fbece-114">[in] A pointer to context information to pass to the **DISMISSMODELESS** function pointed to by the  _lpfnDismiss_ parameter.</span></span> <span data-ttu-id="fbece-115">このパラメーターは、 _ulFlags_パラメーターに DIALOG_SDI フラグを含めることで、モードレス ダイアログ ボックスのバージョンにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="fbece-115">This parameter applies only to the modeless version of the dialog box, by including the DIALOG_SDI flag in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="fbece-116">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="fbece-116">_cbEntryID_</span></span>
  
> <span data-ttu-id="fbece-117">[in]_LpEntryID_パラメーターで指定されたエントリの識別子のバイト数です。</span><span class="sxs-lookup"><span data-stu-id="fbece-117">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="fbece-118">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="fbece-118">_lpEntryID_</span></span>
  
> <span data-ttu-id="fbece-119">[in]詳細情報が表示されているエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="fbece-119">[in] A pointer to the entry identifier for which details are displayed.</span></span>
    
 <span data-ttu-id="fbece-120">_lpfButtonCallback_</span><span class="sxs-lookup"><span data-stu-id="fbece-120">_lpfButtonCallback_</span></span>
  
> <span data-ttu-id="fbece-121">[in][LPFNBUTTON](lpfnbutton.md)関数のプロトタイプでは関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="fbece-121">[in] A pointer to a function based on the [LPFNBUTTON](lpfnbutton.md) function prototype.</span></span> <span data-ttu-id="fbece-122">**LPFNBUTTON**関数では、[詳細情報] ダイアログ ボックスにボタンを追加します。</span><span class="sxs-lookup"><span data-stu-id="fbece-122">An **LPFNBUTTON** function adds a button to the details dialog box.</span></span> 
    
 <span data-ttu-id="fbece-123">_lpvButtonContext_</span><span class="sxs-lookup"><span data-stu-id="fbece-123">_lpvButtonContext_</span></span>
  
> <span data-ttu-id="fbece-124">[in]_LpfButtonCallback_パラメーターで指定された関数のパラメーターとして使用するデータへのポインター。</span><span class="sxs-lookup"><span data-stu-id="fbece-124">[in] A pointer to data used as a parameter for the function specified by the  _lpfButtonCallback_ parameter.</span></span> 
    
 <span data-ttu-id="fbece-125">_lpszButtonText_</span><span class="sxs-lookup"><span data-stu-id="fbece-125">_lpszButtonText_</span></span>
  
> <span data-ttu-id="fbece-126">[in]そのボタンは拡張可能な場合は、[追加] ボタンに適用するテキストを含む文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="fbece-126">[in] A pointer to a string that contains text to be applied to the added button if that button is extensible.</span></span> <span data-ttu-id="fbece-127">_LpszButtonText_パラメーターは、拡張ボタンは、必要でない場合、NULL にすることがあります。</span><span class="sxs-lookup"><span data-stu-id="fbece-127">The  _lpszButtonText_ parameter should be NULL if an extensible button is not needed.</span></span> 
    
 <span data-ttu-id="fbece-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="fbece-128">_ulFlags_</span></span>
  
> <span data-ttu-id="fbece-129">[in]_LpszButtonText_パラメーターのテキストの種類を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="fbece-129">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="fbece-130">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="fbece-130">The following flag can be set:</span></span> 
    
<span data-ttu-id="fbece-131">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="fbece-131">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="fbece-132">共通のアドレス] ダイアログ ボックスのモーダル バージョンを表示します。</span><span class="sxs-lookup"><span data-stu-id="fbece-132">Display the modal version of the common address dialog box.</span></span> <span data-ttu-id="fbece-133">このフラグは、DIALOG_SDI と相互に排他的です。</span><span class="sxs-lookup"><span data-stu-id="fbece-133">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="fbece-134">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="fbece-134">DIALOG_SDI</span></span>
  
>  <span data-ttu-id="fbece-135">モードレスのバージョンの共通のアドレス] ダイアログ ボックスを表示します。</span><span class="sxs-lookup"><span data-stu-id="fbece-135">Display the modeless version of the common address dialog box.</span></span> <span data-ttu-id="fbece-136">このフラグは、DIALOG_MODAL と相互に排他的です。</span><span class="sxs-lookup"><span data-stu-id="fbece-136">This flag is mutually exclusive with DIALOG_MODAL.</span></span> 
    
<span data-ttu-id="fbece-137">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="fbece-137">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="fbece-138">渡された文字列は、Unicode 形式では。</span><span class="sxs-lookup"><span data-stu-id="fbece-138">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="fbece-139">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。</span><span class="sxs-lookup"><span data-stu-id="fbece-139">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fbece-140">�߂�l</span><span class="sxs-lookup"><span data-stu-id="fbece-140">Return value</span></span>

<span data-ttu-id="fbece-141">S_OK</span><span class="sxs-lookup"><span data-stu-id="fbece-141">S_OK</span></span> 
  
> <span data-ttu-id="fbece-142">詳細] ダイアログ ボックスは、アドレス帳のエントリを正常に表示されました。</span><span class="sxs-lookup"><span data-stu-id="fbece-142">The details dialog box was successfully displayed for the address book entry.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fbece-143">備考</span><span class="sxs-lookup"><span data-stu-id="fbece-143">Remarks</span></span>

<span data-ttu-id="fbece-144">アドレス帳プロバイダーのサポート オブジェクトの**IMAPISupport::Details**メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="fbece-144">The **IMAPISupport::Details** method is implemented for address book provider support objects.</span></span> <span data-ttu-id="fbece-145">アドレス帳プロバイダーは、アドレス帳の特定のエントリについて説明するダイアログ ボックスを表示する**詳細情報**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="fbece-145">Address book providers call **Details** to display a dialog box that gives details on a particular entry in the address book.</span></span> <span data-ttu-id="fbece-146">ボタンを追加する、クライアントの定義] ダイアログ ボックスには、 _lpfButtonCallback_、 _lpvButtonContext_、および_lpszButtonText_パラメーターを使用できます。</span><span class="sxs-lookup"><span data-stu-id="fbece-146">The  _lpfButtonCallback_,  _lpvButtonContext_, and  _lpszButtonText_ parameters can be used to add a client-defined button to the dialog box.</span></span> <span data-ttu-id="fbece-147">ボタンがクリックされると、MAPI は、 _lpvButtonContext_のボタンとデータの両方のエントリ id を渡すこと_lpfButtonCallback_で指定されたコールバック関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="fbece-147">When the button is clicked, MAPI calls the callback function pointed to by  _lpfButtonCallback_, passing both the entry identifier of the button and the data in  _lpvButtonContext_.</span></span> <span data-ttu-id="fbece-148">拡張ボタンが必要でない場合_lpszButtonText_は NULL である必要があります。</span><span class="sxs-lookup"><span data-stu-id="fbece-148">If an extensible button is not needed,  _lpszButtonText_ should be NULL.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fbece-149">関連項目</span><span class="sxs-lookup"><span data-stu-id="fbece-149">See also</span></span>



[<span data-ttu-id="fbece-150">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="fbece-150">ADRPARM</span></span>](adrparm.md)
  
[<span data-ttu-id="fbece-151">IMAPISupport::Address</span><span class="sxs-lookup"><span data-stu-id="fbece-151">IMAPISupport::Address</span></span>](imapisupport-address.md)
  
[<span data-ttu-id="fbece-152">LPFNBUTTON</span><span class="sxs-lookup"><span data-stu-id="fbece-152">LPFNBUTTON</span></span>](lpfnbutton.md)
  
[<span data-ttu-id="fbece-153">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="fbece-153">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

