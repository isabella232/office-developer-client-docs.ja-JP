---
title: IAddrBookDetails
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.Details
api_type:
- COM
ms.assetid: 4eee4382-98c3-4714-8920-8d72edef00b8
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 5fbd20a6b5d5598b8fa51f9c369eefac9a1ea2e9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424680"
---
# <a name="iaddrbookdetails"></a><span data-ttu-id="ac31b-103">IAddrBook::Details</span><span class="sxs-lookup"><span data-stu-id="ac31b-103">IAddrBook::Details</span></span>

  
  
<span data-ttu-id="ac31b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ac31b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ac31b-105">特定のアドレス帳エントリに関する詳細を表示するダイアログ ボックスを表示します。</span><span class="sxs-lookup"><span data-stu-id="ac31b-105">Displays a dialog box that shows details about a particular address book entry.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="ac31b-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ac31b-106">Parameters</span></span>

 <span data-ttu-id="ac31b-107">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="ac31b-107">_lpulUIParam_</span></span>
  
> <span data-ttu-id="ac31b-108">[in]ダイアログ ボックスの親ウィンドウのハンドルへのポインター。</span><span class="sxs-lookup"><span data-stu-id="ac31b-108">[in] A pointer to a handle of the parent window for the dialog box.</span></span>
    
 <span data-ttu-id="ac31b-109">_lpfnDismiss_</span><span class="sxs-lookup"><span data-stu-id="ac31b-109">_lpfnDismiss_</span></span>
  
> <span data-ttu-id="ac31b-110">[in] [DISMISSMODELESS](dismissmodeless.md) プロトタイプまたは NULL に基づく関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ac31b-110">[in] A pointer to a function based on the [DISMISSMODELESS](dismissmodeless.md) prototype, or NULL.</span></span> <span data-ttu-id="ac31b-111">このメンバーは、設定されているオプション フラグで示されているモードレス DIALOG_SDIダイアログ ボックスにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="ac31b-111">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="ac31b-112">MAPI は、ユーザーがモードレス アドレス ダイアログ ボックスを閉じ、ダイアログ ボックスがアクティブでなくなった詳細を呼び出しているクライアントに通知するときに **DISMISSMODELESS** 関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ac31b-112">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client that is calling **Details** that the dialog box is no longer active.</span></span> 
    
 <span data-ttu-id="ac31b-113">_lpvDismissContext_</span><span class="sxs-lookup"><span data-stu-id="ac31b-113">_lpvDismissContext_</span></span>
  
> <span data-ttu-id="ac31b-114">[in]_lpfnDismiss_ パラメーターが指す **DISMISSMODELESS** 関数に渡すコンテキスト情報へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ac31b-114">[in] A pointer to context information to pass to the **DISMISSMODELESS** function pointed to by the  _lpfnDismiss_ parameter.</span></span> <span data-ttu-id="ac31b-115">このパラメーターは  _、ulFlags_ パラメーターに DIALOG_SDIフラグを含めて、ダイアログ ボックスのモードレス バージョンにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="ac31b-115">This parameter applies only to the modeless version of the dialog box, by including the DIALOG_SDI flag in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="ac31b-116">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="ac31b-116">_cbEntryID_</span></span>
  
> <span data-ttu-id="ac31b-117">[in]  _lpEntryID_ パラメーターが指すエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="ac31b-117">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="ac31b-118">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="ac31b-118">_lpEntryID_</span></span>
  
> <span data-ttu-id="ac31b-119">[in]詳細が表示されるエントリのエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ac31b-119">[in] A pointer to the entry identifier for the entry for which details are displayed.</span></span>
    
 <span data-ttu-id="ac31b-120">_lpfButtonCallback_</span><span class="sxs-lookup"><span data-stu-id="ac31b-120">_lpfButtonCallback_</span></span>
  
> <span data-ttu-id="ac31b-121">[in] [LPFNBUTTON 関数プロトタイプに基づく関数への](lpfnbutton.md) ポインター。</span><span class="sxs-lookup"><span data-stu-id="ac31b-121">[in] A pointer to a function based on the [LPFNBUTTON](lpfnbutton.md) function prototype.</span></span> <span data-ttu-id="ac31b-122">**LPFNBUTTON 関数は**、詳細ダイアログ ボックスにボタンを追加します。</span><span class="sxs-lookup"><span data-stu-id="ac31b-122">An **LPFNBUTTON** function adds a button to the details dialog box.</span></span> 
    
 <span data-ttu-id="ac31b-123">_lpvButtonContext_</span><span class="sxs-lookup"><span data-stu-id="ac31b-123">_lpvButtonContext_</span></span>
  
> <span data-ttu-id="ac31b-124">[in]  _lpfButtonCallback_ パラメーターで指定された関数のパラメーターとして使用されたデータへのポインター。</span><span class="sxs-lookup"><span data-stu-id="ac31b-124">[in] A pointer to data that was used as a parameter for the function specified by the  _lpfButtonCallback_ parameter.</span></span> 
    
 <span data-ttu-id="ac31b-125">_lpszButtonText_</span><span class="sxs-lookup"><span data-stu-id="ac31b-125">_lpszButtonText_</span></span>
  
> <span data-ttu-id="ac31b-126">[in]追加されたボタンに適用するテキストを含む文字列へのポインター (そのボタンが拡張可能な場合)。</span><span class="sxs-lookup"><span data-stu-id="ac31b-126">[in] A pointer to a string that contains text to be applied to the added button, if that button is extensible.</span></span> <span data-ttu-id="ac31b-127">_拡張可能ボタンが必要ない場合、lpszButtonText_ パラメーターは NULL である必要があります。</span><span class="sxs-lookup"><span data-stu-id="ac31b-127">The  _lpszButtonText_ parameter should be NULL if you do not need an extensible button.</span></span> 
    
 <span data-ttu-id="ac31b-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ac31b-128">_ulFlags_</span></span>
  
> <span data-ttu-id="ac31b-129">[in]  _lpszButtonText_ パラメーターのテキストの種類を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="ac31b-129">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="ac31b-130">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="ac31b-130">The following flags can be set:</span></span> 
    
<span data-ttu-id="ac31b-131">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="ac31b-131">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="ac31b-132">Details が **アドレスに** 実際にS_OK変更された場合に、そのアドレスを返します。それ以外の場合 **、Details** はS_FALSE。</span><span class="sxs-lookup"><span data-stu-id="ac31b-132">Indicates that **Details** returns S_OK if changes are actually made to the address; otherwise, **Details** returns S_FALSE.</span></span> 
    
<span data-ttu-id="ac31b-133">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="ac31b-133">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="ac31b-134">[共通アドレス] ダイアログ ボックスのモーダル バージョンを表示します。これは、常にクライアント以外のクライアントOutlookされます。</span><span class="sxs-lookup"><span data-stu-id="ac31b-134">Display the modal version of the common address dialog box, which is always shown in non-Outlook clients.</span></span> <span data-ttu-id="ac31b-135">このフラグは、このフラグと相互にDIALOG_SDI。</span><span class="sxs-lookup"><span data-stu-id="ac31b-135">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="ac31b-136">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="ac31b-136">DIALOG_SDI</span></span>
  
>  <span data-ttu-id="ac31b-137">[共通アドレス] ダイアログ ボックスのモードレス バージョンを表示します。</span><span class="sxs-lookup"><span data-stu-id="ac31b-137">Display the modeless version of the common address dialog box.</span></span> <span data-ttu-id="ac31b-138">このフラグは、クライアント以外のクライアントOutlookされます。</span><span class="sxs-lookup"><span data-stu-id="ac31b-138">This flag is ignored for non-Outlook clients.</span></span> 
    
<span data-ttu-id="ac31b-139">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ac31b-139">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="ac31b-140">渡された文字列は Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="ac31b-140">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="ac31b-141">このフラグMAPI_UNICODE設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="ac31b-141">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ac31b-142">戻り値</span><span class="sxs-lookup"><span data-stu-id="ac31b-142">Return value</span></span>

<span data-ttu-id="ac31b-143">S_OK</span><span class="sxs-lookup"><span data-stu-id="ac31b-143">S_OK</span></span> 
  
> <span data-ttu-id="ac31b-144">アドレス帳エントリの詳細ダイアログ ボックスが正常に表示されました。</span><span class="sxs-lookup"><span data-stu-id="ac31b-144">The details dialog box was successfully displayed for the address book entry.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ac31b-145">注釈</span><span class="sxs-lookup"><span data-stu-id="ac31b-145">Remarks</span></span>

<span data-ttu-id="ac31b-146">クライアント アプリケーションは Details メソッド **を呼び** 出して、アドレス帳内の特定のエントリに関する詳細を示すダイアログ ボックスを表示します。</span><span class="sxs-lookup"><span data-stu-id="ac31b-146">Client applications call the **Details** method to display a dialog box that provides details about a particular entry in the address book.</span></span> <span data-ttu-id="ac31b-147">_lpfButtonCallback_ パラメーター _、lpvButtonContext_ パラメーター、_および lpszButtonText_ パラメーターを使用して、クライアント定義ボタンをダイアログ ボックスに追加できます。</span><span class="sxs-lookup"><span data-stu-id="ac31b-147">You can use the  _lpfButtonCallback_,  _lpvButtonContext_, and  _lpszButtonText_ parameters to add a client-defined button to the dialog box.</span></span> <span data-ttu-id="ac31b-148">ボタンをクリックすると、MAPI は  _lpfButtonCallback_ が指すコールバック関数を呼び出し、ボタンのエントリ識別子と  _lpvButtonContext_ のデータの両方を渡します。</span><span class="sxs-lookup"><span data-stu-id="ac31b-148">When the button is clicked, MAPI calls the callback function pointed to by  _lpfButtonCallback_, passing both the entry identifier of the button and the data in  _lpvButtonContext_.</span></span> <span data-ttu-id="ac31b-149">拡張可能ボタンが必要ない場合  _、lpszButtonText_ は NULL である必要があります。</span><span class="sxs-lookup"><span data-stu-id="ac31b-149">If you do not need an extensible button,  _lpszButtonText_ should be NULL.</span></span> 
  
 <span data-ttu-id="ac31b-150">**詳細は** Unicode 文字文字列をサポートします。Unicode 文字列は、詳細ダイアログ ボックスに表示される前に、マルチバイト文字文字列 (MBCS) 形式に変換されます。</span><span class="sxs-lookup"><span data-stu-id="ac31b-150">**Details** supports Unicode character strings; Unicode strings are converted to the multibyte character string (MBCS) format before they are displayed in the details dialog box.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ac31b-151">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="ac31b-151">MFCMAPI reference</span></span>

<span data-ttu-id="ac31b-152">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ac31b-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ac31b-153">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="ac31b-153">**File**</span></span>|<span data-ttu-id="ac31b-154">**関数**</span><span class="sxs-lookup"><span data-stu-id="ac31b-154">**Function**</span></span>|<span data-ttu-id="ac31b-155">**コメント**</span><span class="sxs-lookup"><span data-stu-id="ac31b-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ac31b-156">BaseDialog.cpp</span><span class="sxs-lookup"><span data-stu-id="ac31b-156">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="ac31b-157">CBaseDialog::OnOpenEntryID</span><span class="sxs-lookup"><span data-stu-id="ac31b-157">CBaseDialog::OnOpenEntryID</span></span>  <br/> |<span data-ttu-id="ac31b-158">MFCMAPI は Details メソッド **を** 使用して、アドレス帳エントリの詳細を示すダイアログ ボックスを表示します。</span><span class="sxs-lookup"><span data-stu-id="ac31b-158">MFCMAPI uses the **Details** method to display a dialog box that shows the details for an address book entry.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ac31b-159">関連項目</span><span class="sxs-lookup"><span data-stu-id="ac31b-159">See also</span></span>



[<span data-ttu-id="ac31b-160">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="ac31b-160">ADRPARM</span></span>](adrparm.md)
  
[<span data-ttu-id="ac31b-161">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="ac31b-161">IAddrBook::Address</span></span>](iaddrbook-address.md)
  
[<span data-ttu-id="ac31b-162">LPFNBUTTON</span><span class="sxs-lookup"><span data-stu-id="ac31b-162">LPFNBUTTON</span></span>](lpfnbutton.md)
  
[<span data-ttu-id="ac31b-163">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="ac31b-163">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


<span data-ttu-id="ac31b-164">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="ac31b-164">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

