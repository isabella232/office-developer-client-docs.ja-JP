---
title: HrDoABDetailsWithProviderUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 27741887-8405-49ed-b080-613613faf91b
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 47cf87fce0af3b866018bf03a34a05ea42cef82c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426682"
---
# <a name="hrdoabdetailswithprovideruid"></a><span data-ttu-id="2293c-103">HrDoABDetailsWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="2293c-103">HrDoABDetailsWithProviderUID</span></span>

  
  
<span data-ttu-id="2293c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2293c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2293c-105">必要な Exchange アドレス帳プロバイダーが**openentry**メソッドを開いていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="2293c-105">Ensures that the **OpenEntry** method is opened by the expected Exchange address book provider.</span></span> <span data-ttu-id="2293c-106">この関数は[IAddrBook::D etails](iaddrbook-details.md)と同様に動作しますが、 _pEmsabpUID_で識別される Exchange アドレス帳を使用して**entryID**を開きます。</span><span class="sxs-lookup"><span data-stu-id="2293c-106">This function works similarly to [IAddrBook::Details](iaddrbook-details.md) but opens **entryID** using the Exchange address book identified by  _pEmsabpUID_.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2293c-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="2293c-107">Header file:</span></span>  <br/> |<span data-ttu-id="2293c-108">abhelp .h</span><span class="sxs-lookup"><span data-stu-id="2293c-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="2293c-109">実装元:</span><span class="sxs-lookup"><span data-stu-id="2293c-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="2293c-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="2293c-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="2293c-111">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="2293c-111">Called by:</span></span>  <br/> |<span data-ttu-id="2293c-112">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="2293c-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrDoABDetailsWithProviderUID(
  const MAPIUID   *pEmsabpUID,
  LPADRBOOK        pAddrBook,
  ULONG_PTR FAR *  lpulUIParam,
  LPFNDISMISS      lpfnDismiss,
  LPVOID           lpvDismissContext,
  ULONG            cbEntryID,
  LPENTRYID        lpEntryID,
  LPFNBUTTON       lpfButtonCallback,
  LPVOID           lpvButtonContext,
  LPSTR           lpszButtonText,
  ULONG            ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="2293c-113">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2293c-113">Parameters</span></span>

 <span data-ttu-id="2293c-114">_pEmsabpUID_</span><span class="sxs-lookup"><span data-stu-id="2293c-114">_pEmsabpUID_</span></span>
  
> <span data-ttu-id="2293c-115">順番この関数がエントリ識別子の詳細を表示するために使用する Exchange アドレス帳プロバイダーを識別する_emsabpUID_へのポインター。</span><span class="sxs-lookup"><span data-stu-id="2293c-115">[in] A pointer to an  _emsabpUID_ that identifies the Exchange address book provider this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="2293c-116">入力されたエントリ識別子が Exchange アドレス帳プロバイダーのエントリ識別子ではない場合、このパラメーターは無視され、関数呼び出しは[IAddrBook::D etails](iaddrbook-details.md)と同じように動作します。</span><span class="sxs-lookup"><span data-stu-id="2293c-116">If the incoming entry identifier is not an Exchange address book provider entry identifier, this parameter is ignored and the function call acts exactly like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="2293c-117">このパラメーターが NULL またはゼロ MAPIUID の場合は、この関数も[IAddrBook::D etails](iaddrbook-details.md)と同じように動作します。</span><span class="sxs-lookup"><span data-stu-id="2293c-117">If this parameter is NULL or a zero MAPIUID, this function also acts exactly like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="2293c-118">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="2293c-118">_pAddrBook_</span></span>
  
> <span data-ttu-id="2293c-119">順番エントリ識別子を開くために使用されるアドレス帳。</span><span class="sxs-lookup"><span data-stu-id="2293c-119">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="2293c-120">NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="2293c-120">It cannot be NULL.</span></span>
    
 <span data-ttu-id="2293c-121">_l出 uiparam_</span><span class="sxs-lookup"><span data-stu-id="2293c-121">_lpulUIParam_</span></span>
  
> <span data-ttu-id="2293c-122">読み上げダイアログボックスの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="2293c-122">[out] A handle to the parent window for the dialog box.</span></span>
    
 <span data-ttu-id="2293c-123">_lpfnDismiss_</span><span class="sxs-lookup"><span data-stu-id="2293c-123">_lpfnDismiss_</span></span>
  
> <span data-ttu-id="2293c-124">順番**DISMISSMODELESS**プロトタイプに基づく関数へのポインター、または NULL。</span><span class="sxs-lookup"><span data-stu-id="2293c-124">[in] A pointer to a function based on the **DISMISSMODELESS** prototype, or NULL.</span></span> <span data-ttu-id="2293c-125">このメンバーは、DIALOG_SDI フラグが設定されている場合のように、ダイアログボックスのモードレスバージョンにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="2293c-125">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="2293c-126">MAPI は、ユーザーがモードレスアドレスダイアログボックスを閉じたときに、そのダイアログボックスがアクティブでなくなったことを示す詳細を呼び出していることをクライアントに通知する**DISMISSMODELESS**関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="2293c-126">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client that is calling Details that the dialog box is no longer active.</span></span> 
    
 <span data-ttu-id="2293c-127">_lpvDismissContext_</span><span class="sxs-lookup"><span data-stu-id="2293c-127">_lpvDismissContext_</span></span>
  
> <span data-ttu-id="2293c-128">順番_lpfnDismiss_パラメーターが指す**DISMISSMODELESS**関数に渡すコンテキスト情報へのポインター。</span><span class="sxs-lookup"><span data-stu-id="2293c-128">[in] A pointer to context information to pass to the **DISMISSMODELESS** function pointed to by the  _lpfnDismiss_ parameter.</span></span> <span data-ttu-id="2293c-129">このパラメーターは、 **DIALOG_SDI**フラグを_ulflags_パラメーターに含めることによって、ダイアログボックスのモードレスバージョンにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="2293c-129">This parameter applies only to the modeless version of the dialog box by including the **DIALOG_SDI** flag in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="2293c-130">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="2293c-130">_cbEntryID_</span></span>
  
> <span data-ttu-id="2293c-131">順番_lな tryid_パラメーターで指定されたエントリ id のバイト数。</span><span class="sxs-lookup"><span data-stu-id="2293c-131">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="2293c-132">_lて tryid_</span><span class="sxs-lookup"><span data-stu-id="2293c-132">_lpEntryID_</span></span>
  
> <span data-ttu-id="2293c-133">順番開くアドレス帳のエントリを表すエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="2293c-133">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="2293c-134">_lpfbuttoncallback_</span><span class="sxs-lookup"><span data-stu-id="2293c-134">_lpfButtonCallback_</span></span>
  
> <span data-ttu-id="2293c-135">順番**LPFNBUTTON**関数プロトタイプに基づく関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="2293c-135">[in] A pointer to a function based on the **LPFNBUTTON** function prototype.</span></span> <span data-ttu-id="2293c-136">**LPFNBUTTON**関数は、[詳細] ダイアログボックスにボタンを追加します。</span><span class="sxs-lookup"><span data-stu-id="2293c-136">An **LPFNBUTTON** function adds a button to the details dialog box.</span></span> 
    
 <span data-ttu-id="2293c-137">_lpvbuttoncontext_</span><span class="sxs-lookup"><span data-stu-id="2293c-137">_lpvButtonContext_</span></span>
  
> <span data-ttu-id="2293c-138">順番_lpfbuttoncallback_パラメーターで指定された関数のパラメーターとして使用されたデータへのポインター。</span><span class="sxs-lookup"><span data-stu-id="2293c-138">[in] A pointer to data that was used as a parameter for the function specified by the  _lpfButtonCallback_ parameter.</span></span> 
    
 <span data-ttu-id="2293c-139">_lpszbuttontext_</span><span class="sxs-lookup"><span data-stu-id="2293c-139">_lpszButtonText_</span></span>
  
> <span data-ttu-id="2293c-140">順番追加されたボタンに適用されるテキストを含む文字列へのポインター。ボタンが拡張可能な場合です。</span><span class="sxs-lookup"><span data-stu-id="2293c-140">[in] A pointer to a string that contains text to be applied to the added button, if that button is extensible.</span></span> <span data-ttu-id="2293c-141">拡張ボタンを必要としない場合は、 _lpszbuttontext_パラメーターを NULL に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2293c-141">The  _lpszButtonText_ parameter should be NULL when an extensible button is not needed.</span></span> 
    
 <span data-ttu-id="2293c-142">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2293c-142">_ulFlags_</span></span>
  
> <span data-ttu-id="2293c-143">順番_lpszbuttontext_パラメーターのテキストの種類を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="2293c-143">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="2293c-144">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="2293c-144">The following flags can be set:</span></span> 
    
<span data-ttu-id="2293c-145">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="2293c-145">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="2293c-146">住所に変更が実際に加えられた場合に、詳細が TRUE を返すことを示します。それ以外の場合、詳細は FALSE を返します。</span><span class="sxs-lookup"><span data-stu-id="2293c-146">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="2293c-147">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="2293c-147">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="2293c-148">[共通アドレス] ダイアログボックスのモーダルバージョンが表示されます。</span><span class="sxs-lookup"><span data-stu-id="2293c-148">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="2293c-149">このフラグは、DIALOG_SDI とは相互に排他的です。</span><span class="sxs-lookup"><span data-stu-id="2293c-149">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="2293c-150">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="2293c-150">DIALOG_SDI</span></span>
  
> <span data-ttu-id="2293c-151">[共通アドレス] ダイアログボックスのモードレスバージョンが表示されます。</span><span class="sxs-lookup"><span data-stu-id="2293c-151">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="2293c-152">このフラグは、DIALOG_MODAL とは相互に排他的です。</span><span class="sxs-lookup"><span data-stu-id="2293c-152">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="2293c-153">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2293c-153">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="2293c-154">渡された文字列は Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="2293c-154">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="2293c-155">MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="2293c-155">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    

