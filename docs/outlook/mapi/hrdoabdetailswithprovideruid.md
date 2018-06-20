---
title: HrDoABDetailsWithProviderUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 27741887-8405-49ed-b080-613613faf91b
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: fada57c45602f0a0b07276034101fa23a7525f5b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800285"
---
# <a name="hrdoabdetailswithprovideruid"></a><span data-ttu-id="9259a-103">HrDoABDetailsWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="9259a-103">HrDoABDetailsWithProviderUID</span></span>

  
  
<span data-ttu-id="9259a-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9259a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9259a-105">**OpenEntry**メソッドが必要な Exchange のアドレス帳プロバイダーで開かれているようにします。</span><span class="sxs-lookup"><span data-stu-id="9259a-105">Ensures that the **OpenEntry** method is opened by the expected Exchange address book provider.</span></span> <span data-ttu-id="9259a-106">この関数は、 [IAddrBook::Details](iaddrbook-details.md)と同様に動作しますが、 _pEmsabpUID_で識別される、Exchange アドレス帳を使用して**エントリ Id**を表示します。</span><span class="sxs-lookup"><span data-stu-id="9259a-106">This function works similarly to [IAddrBook::Details](iaddrbook-details.md) but opens **entryID** using the Exchange address book identified by  _pEmsabpUID_.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9259a-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="9259a-107">Header file:</span></span>  <br/> |<span data-ttu-id="9259a-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="9259a-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="9259a-109">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="9259a-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="9259a-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="9259a-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="9259a-111">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="9259a-111">Called by:</span></span>  <br/> |<span data-ttu-id="9259a-112">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="9259a-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="9259a-113">Parameters</span><span class="sxs-lookup"><span data-stu-id="9259a-113">Parameters</span></span>

 <span data-ttu-id="9259a-114">_pEmsabpUID_</span><span class="sxs-lookup"><span data-stu-id="9259a-114">_pEmsabpUID_</span></span>
  
> <span data-ttu-id="9259a-115">[in]Exchange アドレス帳プロバイダーを識別する_emsabpUID_へのポインターのエントリ id の詳細を表示するのにはこの関数を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9259a-115">[in] A pointer to an  _emsabpUID_ that identifies the Exchange address book provider this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="9259a-116">受信のエントリ id が Exchange アドレス帳プロバイダー エントリ識別子ではない場合は、このパラメーターは無視され、 [IAddrBook::Details](iaddrbook-details.md)関数の呼び出しの動作とまったく同じです。</span><span class="sxs-lookup"><span data-stu-id="9259a-116">If the incoming entry identifier is not an Exchange address book provider entry identifier, this parameter is ignored and the function call acts exactly like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="9259a-117">このパラメーターが NULL またはゼロの MAPIUID の場合は、この関数はまた[IAddrBook::Details](iaddrbook-details.md)と同様に機能します。</span><span class="sxs-lookup"><span data-stu-id="9259a-117">If this parameter is NULL or a zero MAPIUID, this function also acts exactly like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="9259a-118">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="9259a-118">_pAddrBook_</span></span>
  
> <span data-ttu-id="9259a-119">[in]アドレス帳のエントリ id を開くために使用します。</span><span class="sxs-lookup"><span data-stu-id="9259a-119">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="9259a-120">NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="9259a-120">It cannot be NULL.</span></span>
    
 <span data-ttu-id="9259a-121">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="9259a-121">_lpulUIParam_</span></span>
  
> <span data-ttu-id="9259a-122">[out]ダイアログ ボックスの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="9259a-122">[out] A handle to the parent window for the dialog box.</span></span>
    
 <span data-ttu-id="9259a-123">_lpfnDismiss_</span><span class="sxs-lookup"><span data-stu-id="9259a-123">_lpfnDismiss_</span></span>
  
> <span data-ttu-id="9259a-124">[in]**DISMISSMODELESS**のプロトタイプでは関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="9259a-124">[in] A pointer to a function based on the **DISMISSMODELESS** prototype, or NULL.</span></span> <span data-ttu-id="9259a-125">このメンバーは、DIALOG_SDI フラグが設定されている中で示されるように、モードレス ダイアログ ボックスのバージョンにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="9259a-125">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="9259a-126">MAPI 関数を呼び出す**DISMISSMODELESS**ユーザーが、アドレスのモードレス ダイアログ ボックスを閉じるときの詳細] ダイアログ ボックスがアクティブではないことを呼び出しているクライアントに通知します。</span><span class="sxs-lookup"><span data-stu-id="9259a-126">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client that is calling Details that the dialog box is no longer active.</span></span> 
    
 <span data-ttu-id="9259a-127">_lpvDismissContext_</span><span class="sxs-lookup"><span data-stu-id="9259a-127">_lpvDismissContext_</span></span>
  
> <span data-ttu-id="9259a-128">[in]_LpfnDismiss_パラメーターが指す、 **DISMISSMODELESS**関数に渡すコンテキスト情報へのポインターです。</span><span class="sxs-lookup"><span data-stu-id="9259a-128">[in] A pointer to context information to pass to the **DISMISSMODELESS** function pointed to by the  _lpfnDismiss_ parameter.</span></span> <span data-ttu-id="9259a-129">このパラメーターは、 _ulFlags_パラメーターに**DIALOG_SDI**フラグを含めることで、モードレス ダイアログ ボックスのバージョンにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="9259a-129">This parameter applies only to the modeless version of the dialog box by including the **DIALOG_SDI** flag in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="9259a-130">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="9259a-130">_cbEntryID_</span></span>
  
> <span data-ttu-id="9259a-131">[in]_LpEntryID_パラメーターで指定されたエントリの識別子のバイト数です。</span><span class="sxs-lookup"><span data-stu-id="9259a-131">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="9259a-132">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="9259a-132">_lpEntryID_</span></span>
  
> <span data-ttu-id="9259a-133">[in]開くにはアドレス帳のエントリを表すエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="9259a-133">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="9259a-134">_lpfButtonCallback_</span><span class="sxs-lookup"><span data-stu-id="9259a-134">_lpfButtonCallback_</span></span>
  
> <span data-ttu-id="9259a-135">[in]**LPFNBUTTON**関数のプロトタイプでは関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="9259a-135">[in] A pointer to a function based on the **LPFNBUTTON** function prototype.</span></span> <span data-ttu-id="9259a-136">**LPFNBUTTON**関数では、[詳細情報] ダイアログ ボックスにボタンを追加します。</span><span class="sxs-lookup"><span data-stu-id="9259a-136">An **LPFNBUTTON** function adds a button to the details dialog box.</span></span> 
    
 <span data-ttu-id="9259a-137">_lpvButtonContext_</span><span class="sxs-lookup"><span data-stu-id="9259a-137">_lpvButtonContext_</span></span>
  
> <span data-ttu-id="9259a-138">[in]_LpfButtonCallback_パラメーターで指定された関数のパラメーターとして使用されていたデータへのポインター。</span><span class="sxs-lookup"><span data-stu-id="9259a-138">[in] A pointer to data that was used as a parameter for the function specified by the  _lpfButtonCallback_ parameter.</span></span> 
    
 <span data-ttu-id="9259a-139">_lpszButtonText_</span><span class="sxs-lookup"><span data-stu-id="9259a-139">_lpszButtonText_</span></span>
  
> <span data-ttu-id="9259a-140">[in]そのボタンは拡張可能な場合、[追加] ボタンに適用するテキストを含む文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="9259a-140">[in] A pointer to a string that contains text to be applied to the added button, if that button is extensible.</span></span> <span data-ttu-id="9259a-141">拡張ボタンが不要な場合、 _lpszButtonText_パラメーターは NULL である必要があります。</span><span class="sxs-lookup"><span data-stu-id="9259a-141">The  _lpszButtonText_ parameter should be NULL when an extensible button is not needed.</span></span> 
    
 <span data-ttu-id="9259a-142">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9259a-142">_ulFlags_</span></span>
  
> <span data-ttu-id="9259a-143">[in]_LpszButtonText_パラメーターのテキストの種類を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="9259a-143">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="9259a-144">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="9259a-144">The following flags can be set:</span></span> 
    
<span data-ttu-id="9259a-145">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="9259a-145">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="9259a-146">詳細は TRUE を返す場合は、アドレスに変更を加えた実際にことを示します。それ以外の場合、詳細は、FALSE を返します。</span><span class="sxs-lookup"><span data-stu-id="9259a-146">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="9259a-147">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="9259a-147">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="9259a-148">共通のアドレス] ダイアログ ボックスのモーダル バージョンが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9259a-148">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="9259a-149">このフラグは、DIALOG_SDI と相互に排他的です。</span><span class="sxs-lookup"><span data-stu-id="9259a-149">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="9259a-150">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="9259a-150">DIALOG_SDI</span></span>
  
> <span data-ttu-id="9259a-151">モードレスのバージョンの共通のアドレス] ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9259a-151">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="9259a-152">このフラグは、DIALOG_MODAL と相互に排他的です。</span><span class="sxs-lookup"><span data-stu-id="9259a-152">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="9259a-153">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9259a-153">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="9259a-154">渡された文字列は、Unicode 形式では。</span><span class="sxs-lookup"><span data-stu-id="9259a-154">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="9259a-155">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。</span><span class="sxs-lookup"><span data-stu-id="9259a-155">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    

