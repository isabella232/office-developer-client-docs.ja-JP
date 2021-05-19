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
# <a name="hrdoabdetailswithprovideruid"></a><span data-ttu-id="a1365-103">HrDoABDetailsWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="a1365-103">HrDoABDetailsWithProviderUID</span></span>

  
  
<span data-ttu-id="a1365-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a1365-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a1365-105">**OpenEntry** メソッドが、予想されるアドレス帳プロバイダーによって開Exchange確認します。</span><span class="sxs-lookup"><span data-stu-id="a1365-105">Ensures that the **OpenEntry** method is opened by the expected Exchange address book provider.</span></span> <span data-ttu-id="a1365-106">この関数は [IAddrBook::D etails](iaddrbook-details.md)と同様に動作しますが _、pEmsabpUID_ で識別される Exchange アドレス帳を使用して **entryID** を開きます。</span><span class="sxs-lookup"><span data-stu-id="a1365-106">This function works similarly to [IAddrBook::Details](iaddrbook-details.md) but opens **entryID** using the Exchange address book identified by  _pEmsabpUID_.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a1365-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="a1365-107">Header file:</span></span>  <br/> |<span data-ttu-id="a1365-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="a1365-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="a1365-109">実装元:</span><span class="sxs-lookup"><span data-stu-id="a1365-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="a1365-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="a1365-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="a1365-111">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="a1365-111">Called by:</span></span>  <br/> |<span data-ttu-id="a1365-112">クライアント アプリケーションとサービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="a1365-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="a1365-113">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a1365-113">Parameters</span></span>

 <span data-ttu-id="a1365-114">_pEmsabpUID_</span><span class="sxs-lookup"><span data-stu-id="a1365-114">_pEmsabpUID_</span></span>
  
> <span data-ttu-id="a1365-115">[in]この関数は、エントリ識別子の詳細を表示するためにExchangeアドレス帳プロバイダーを識別する _emsabpUID_ へのポインターです。</span><span class="sxs-lookup"><span data-stu-id="a1365-115">[in] A pointer to an  _emsabpUID_ that identifies the Exchange address book provider this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="a1365-116">受信エントリ識別子が Exchange アドレス帳プロバイダーエントリ識別子ではない場合、このパラメーターは無視され、関数呼び出しは[IAddrBook::D](iaddrbook-details.md)とまったく同じ動作をします。</span><span class="sxs-lookup"><span data-stu-id="a1365-116">If the incoming entry identifier is not an Exchange address book provider entry identifier, this parameter is ignored and the function call acts exactly like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="a1365-117">このパラメーターが NULL または 0 の MAPIUID の場合、この関数は [IAddrBook::D同様に動作します](iaddrbook-details.md)。</span><span class="sxs-lookup"><span data-stu-id="a1365-117">If this parameter is NULL or a zero MAPIUID, this function also acts exactly like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="a1365-118">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="a1365-118">_pAddrBook_</span></span>
  
> <span data-ttu-id="a1365-119">[in]エントリ識別子を開くのに使用するアドレス帳。</span><span class="sxs-lookup"><span data-stu-id="a1365-119">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="a1365-120">NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="a1365-120">It cannot be NULL.</span></span>
    
 <span data-ttu-id="a1365-121">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="a1365-121">_lpulUIParam_</span></span>
  
> <span data-ttu-id="a1365-122">[out]ダイアログ ボックスの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="a1365-122">[out] A handle to the parent window for the dialog box.</span></span>
    
 <span data-ttu-id="a1365-123">_lpfnDismiss_</span><span class="sxs-lookup"><span data-stu-id="a1365-123">_lpfnDismiss_</span></span>
  
> <span data-ttu-id="a1365-124">[in] **DISMISSMODELESS** プロトタイプまたは NULL に基づく関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a1365-124">[in] A pointer to a function based on the **DISMISSMODELESS** prototype, or NULL.</span></span> <span data-ttu-id="a1365-125">このメンバーは、設定されているオプション フラグで示されているモードレス DIALOG_SDIダイアログ ボックスにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="a1365-125">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="a1365-126">MAPI は、ユーザーがモードレス アドレス ダイアログ ボックスを閉じ、ダイアログ ボックスがアクティブでなくなった詳細を呼び出しているクライアントに通知するときに **DISMISSMODELESS** 関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a1365-126">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client that is calling Details that the dialog box is no longer active.</span></span> 
    
 <span data-ttu-id="a1365-127">_lpvDismissContext_</span><span class="sxs-lookup"><span data-stu-id="a1365-127">_lpvDismissContext_</span></span>
  
> <span data-ttu-id="a1365-128">[in]_lpfnDismiss_ パラメーターが指す **DISMISSMODELESS** 関数に渡すコンテキスト情報へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a1365-128">[in] A pointer to context information to pass to the **DISMISSMODELESS** function pointed to by the  _lpfnDismiss_ parameter.</span></span> <span data-ttu-id="a1365-129">このパラメーターは _、ulFlags_ パラメーターに DIALOG_SDIを含めて、ダイアログ ボックス **のモードレス** バージョンにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="a1365-129">This parameter applies only to the modeless version of the dialog box by including the **DIALOG_SDI** flag in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="a1365-130">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="a1365-130">_cbEntryID_</span></span>
  
> <span data-ttu-id="a1365-131">[in]  _lpEntryID_ パラメーターで指定されたエントリ識別子のバイト 数。</span><span class="sxs-lookup"><span data-stu-id="a1365-131">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="a1365-132">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="a1365-132">_lpEntryID_</span></span>
  
> <span data-ttu-id="a1365-133">[in]開くアドレス帳エントリを表すエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a1365-133">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="a1365-134">_lpfButtonCallback_</span><span class="sxs-lookup"><span data-stu-id="a1365-134">_lpfButtonCallback_</span></span>
  
> <span data-ttu-id="a1365-135">[in] **LPFNBUTTON 関数プロトタイプに基づく関数への** ポインター。</span><span class="sxs-lookup"><span data-stu-id="a1365-135">[in] A pointer to a function based on the **LPFNBUTTON** function prototype.</span></span> <span data-ttu-id="a1365-136">**LPFNBUTTON 関数は**、詳細ダイアログ ボックスにボタンを追加します。</span><span class="sxs-lookup"><span data-stu-id="a1365-136">An **LPFNBUTTON** function adds a button to the details dialog box.</span></span> 
    
 <span data-ttu-id="a1365-137">_lpvButtonContext_</span><span class="sxs-lookup"><span data-stu-id="a1365-137">_lpvButtonContext_</span></span>
  
> <span data-ttu-id="a1365-138">[in]  _lpfButtonCallback_ パラメーターで指定された関数のパラメーターとして使用されたデータへのポインター。</span><span class="sxs-lookup"><span data-stu-id="a1365-138">[in] A pointer to data that was used as a parameter for the function specified by the  _lpfButtonCallback_ parameter.</span></span> 
    
 <span data-ttu-id="a1365-139">_lpszButtonText_</span><span class="sxs-lookup"><span data-stu-id="a1365-139">_lpszButtonText_</span></span>
  
> <span data-ttu-id="a1365-140">[in]追加されたボタンに適用するテキストを含む文字列へのポインター (そのボタンが拡張可能な場合)。</span><span class="sxs-lookup"><span data-stu-id="a1365-140">[in] A pointer to a string that contains text to be applied to the added button, if that button is extensible.</span></span> <span data-ttu-id="a1365-141">_拡張可能ボタンが不要な場合、lpszButtonText_ パラメーターは NULL である必要があります。</span><span class="sxs-lookup"><span data-stu-id="a1365-141">The  _lpszButtonText_ parameter should be NULL when an extensible button is not needed.</span></span> 
    
 <span data-ttu-id="a1365-142">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a1365-142">_ulFlags_</span></span>
  
> <span data-ttu-id="a1365-143">[in]  _lpszButtonText_ パラメーターのテキストの種類を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="a1365-143">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="a1365-144">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="a1365-144">The following flags can be set:</span></span> 
    
<span data-ttu-id="a1365-145">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="a1365-145">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="a1365-146">アドレスに実際に変更が加えた場合、Details は TRUE を返します。それ以外の場合、Details は FALSE を返します。</span><span class="sxs-lookup"><span data-stu-id="a1365-146">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="a1365-147">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="a1365-147">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="a1365-148">[共通アドレス] ダイアログ ボックスのモーダル バージョンを表示します。</span><span class="sxs-lookup"><span data-stu-id="a1365-148">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="a1365-149">このフラグは、このフラグと相互にDIALOG_SDI。</span><span class="sxs-lookup"><span data-stu-id="a1365-149">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="a1365-150">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="a1365-150">DIALOG_SDI</span></span>
  
> <span data-ttu-id="a1365-151">[共通アドレス] ダイアログ ボックスのモードレス バージョンを表示します。</span><span class="sxs-lookup"><span data-stu-id="a1365-151">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="a1365-152">このフラグは、他のフラグと相互DIALOG_MODAL。</span><span class="sxs-lookup"><span data-stu-id="a1365-152">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="a1365-153">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a1365-153">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="a1365-154">渡された文字列は Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="a1365-154">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="a1365-155">このフラグMAPI_UNICODE設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="a1365-155">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    

