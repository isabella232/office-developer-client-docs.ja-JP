---
title: HrDoABDetailsWithExchangeContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b4e7fed2-88e4-4e14-90b6-913a1b7e338a
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: cb6138072cd5dedc528168d4056041661c40fd06
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800298"
---
# <a name="hrdoabdetailswithexchangecontext"></a><span data-ttu-id="d9e78-103">HrDoABDetailsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="d9e78-103">HrDoABDetailsWithExchangeContext</span></span>

  
  
<span data-ttu-id="d9e78-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d9e78-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d9e78-105">**OpenEntry**メソッドが必要な Exchange のアドレス帳プロバイダーで開かれているようにします。</span><span class="sxs-lookup"><span data-stu-id="d9e78-105">Ensures that the **OpenEntry** method is opened by the expected Exchange address book provider.</span></span> <span data-ttu-id="d9e78-106">この関数は、 [IAddrBook::Details](iaddrbook-details.md)と同様に動作しますが、 _pEmsmdbUID_パラメーターで指定された Exchange のアドレス帳を使用して**エントリ Id**を表示します。</span><span class="sxs-lookup"><span data-stu-id="d9e78-106">This function works similarly to [IAddrBook::Details](iaddrbook-details.md), but opens the **entryID** using the Exchange address book identified by the  _pEmsmdbUID_ parameter.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d9e78-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="d9e78-107">Header file:</span></span>  <br/> |<span data-ttu-id="d9e78-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="d9e78-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="d9e78-109">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="d9e78-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="d9e78-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="d9e78-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="d9e78-111">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d9e78-111">Called by:</span></span>  <br/> |<span data-ttu-id="d9e78-112">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="d9e78-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrOpenABEntryWithExchangeContext(
  LPMAPISESSION   pmsess,
  const MAPIUID  *pEmsmdbUID,
  LPADRBOOK pAddrBook,
  ULONG_PTR FAR * lpulUIParam,
  LPFNDISMISS lpfnDismiss,
  LPVOID lpvDismissContext,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPENTRYID lpEntryID,
  LPFNBUTTON lpfButtonCallback,
  LPVOID lpvButtonContext,
  LPSTR lpszButtonText,
  ULONG ulFlags,
);
```

## <a name="parameters"></a><span data-ttu-id="d9e78-113">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9e78-113">Parameters</span></span>

 <span data-ttu-id="d9e78-114">_pmsess_</span><span class="sxs-lookup"><span data-stu-id="d9e78-114">_pmsess_</span></span>
  
> <span data-ttu-id="d9e78-115">**IMAPISession**にログオンします。</span><span class="sxs-lookup"><span data-stu-id="d9e78-115">The logged on **IMAPISession**.</span></span> <span data-ttu-id="d9e78-116">NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="d9e78-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="d9e78-117">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="d9e78-117">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="d9e78-118">開くには、エントリの識別子、関数で使用される Exchange アドレス帳プロバイダーが含まれている Exchange サービスを識別する**emsmdbUID**へのポインター。</span><span class="sxs-lookup"><span data-stu-id="d9e78-118">A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange address book provider that is used by the function to open the entry identifier.</span></span> <span data-ttu-id="d9e78-119">受信のエントリ id が Exchange アドレス帳プロバイダー エントリ識別子でない場合は、このパラメーターは無視され、関数は、[アドレス帳コンテナー](iaddrbook-openentry.md)のように動作します。</span><span class="sxs-lookup"><span data-stu-id="d9e78-119">If the incoming entry identifier is not an Exchange address book provider entry identifier, this parameter is ignored and the function behaves like [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span> <span data-ttu-id="d9e78-120">このパラメーターが NULL またはゼロの**MAPIUID**の場合は、この関数は、[アドレス帳コンテナー](iaddrbook-openentry.md)と同じようにも機能します。</span><span class="sxs-lookup"><span data-stu-id="d9e78-120">If this parameter is NULL or a zero **MAPIUID**, this function also acts exactly like [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span> 
    
 <span data-ttu-id="d9e78-121">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="d9e78-121">_pAddrBook_</span></span>
  
> <span data-ttu-id="d9e78-122">[in]アドレス帳のエントリ id を開くために使用します。</span><span class="sxs-lookup"><span data-stu-id="d9e78-122">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="d9e78-123">NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="d9e78-123">It cannot be NULL.</span></span>
    
 <span data-ttu-id="d9e78-124">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="d9e78-124">_lpulUIParam_</span></span>
  
> <span data-ttu-id="d9e78-125">[out]ダイアログ ボックスの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="d9e78-125">[out] A handle to the parent window for the dialog box.</span></span>
    
 <span data-ttu-id="d9e78-126">_lpfnDismiss_</span><span class="sxs-lookup"><span data-stu-id="d9e78-126">_lpfnDismiss_</span></span>
  
> <span data-ttu-id="d9e78-127">[in]**DISMISSMODELESS**のプロトタイプでは関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="d9e78-127">[in] A pointer to a function based on the **DISMISSMODELESS** prototype, or NULL.</span></span> <span data-ttu-id="d9e78-128">このメンバーは、DIALOG_SDI フラグが設定されている中で示されるように、モードレス ダイアログ ボックスのバージョンにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="d9e78-128">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="d9e78-129">MAPI 関数を呼び出す**DISMISSMODELESS**ユーザーが、アドレスのモードレス ダイアログ ボックスを閉じるときの詳細] ダイアログ ボックスがアクティブではないことを呼び出しているクライアントに通知します。</span><span class="sxs-lookup"><span data-stu-id="d9e78-129">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client that is calling Details that the dialog box is no longer active.</span></span> 
    
 <span data-ttu-id="d9e78-130">_lpvDismissContext_</span><span class="sxs-lookup"><span data-stu-id="d9e78-130">_lpvDismissContext_</span></span>
  
> <span data-ttu-id="d9e78-131">[in]_LpfnDismiss_パラメーターが指す、 **DISMISSMODELESS**関数に渡すコンテキスト情報へのポインターです。</span><span class="sxs-lookup"><span data-stu-id="d9e78-131">[in] A pointer to context information to pass to the **DISMISSMODELESS** function pointed to by the  _lpfnDismiss_ parameter.</span></span> <span data-ttu-id="d9e78-132">このパラメーターは、 _ulFlags_パラメーターに**DIALOG_SDI**フラグを含めることで、モードレス ダイアログ ボックスのバージョンにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="d9e78-132">This parameter applies only to the modeless version of the dialog box by including the **DIALOG_SDI** flag in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="d9e78-133">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="d9e78-133">_cbEntryID_</span></span>
  
> <span data-ttu-id="d9e78-134">[in]_LpEntryID_パラメーターで指定されたエントリの識別子のバイト数です。</span><span class="sxs-lookup"><span data-stu-id="d9e78-134">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="d9e78-135">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="d9e78-135">_lpEntryID_</span></span>
  
> <span data-ttu-id="d9e78-136">[in]開くにはアドレス帳のエントリを表すエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="d9e78-136">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="d9e78-137">_lpfButtonCallback_</span><span class="sxs-lookup"><span data-stu-id="d9e78-137">_lpfButtonCallback_</span></span>
  
> <span data-ttu-id="d9e78-138">[in]**LPFNBUTTON**関数のプロトタイプでは関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="d9e78-138">[in] A pointer to a function based on the **LPFNBUTTON** function prototype.</span></span> <span data-ttu-id="d9e78-139">**LPFNBUTTON**関数では、[詳細情報] ダイアログ ボックスにボタンを追加します。</span><span class="sxs-lookup"><span data-stu-id="d9e78-139">An **LPFNBUTTON** function adds a button to the details dialog box.</span></span> 
    
 <span data-ttu-id="d9e78-140">_lpvButtonContext_</span><span class="sxs-lookup"><span data-stu-id="d9e78-140">_lpvButtonContext_</span></span>
  
> <span data-ttu-id="d9e78-141">[in]_LpfButtonCallback_パラメーターで指定された関数のパラメーターとして使用されていたデータへのポインター。</span><span class="sxs-lookup"><span data-stu-id="d9e78-141">[in] A pointer to data that was used as a parameter for the function specified by the  _lpfButtonCallback_ parameter.</span></span> 
    
 <span data-ttu-id="d9e78-142">_lpszButtonText_</span><span class="sxs-lookup"><span data-stu-id="d9e78-142">_lpszButtonText_</span></span>
  
> <span data-ttu-id="d9e78-143">[in]そのボタンは拡張可能な場合、[追加] ボタンに適用するテキストを含む文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="d9e78-143">[in] A pointer to a string that contains text to be applied to the added button, if that button is extensible.</span></span> <span data-ttu-id="d9e78-144">拡張ボタンが不要な場合、 _lpszButtonText_パラメーターは NULL である必要があります。</span><span class="sxs-lookup"><span data-stu-id="d9e78-144">The  _lpszButtonText_ parameter should be NULL when an extensible button is not needed.</span></span> 
    
 <span data-ttu-id="d9e78-145">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d9e78-145">_ulFlags_</span></span>
  
> <span data-ttu-id="d9e78-146">[in]_LpszButtonText_パラメーターのテキストの種類を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="d9e78-146">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="d9e78-147">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="d9e78-147">The following flags can be set:</span></span> 
    
<span data-ttu-id="d9e78-148">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="d9e78-148">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="d9e78-149">詳細は TRUE を返す場合は、アドレスに変更を加えた実際にことを示します。それ以外の場合、詳細は、FALSE を返します。</span><span class="sxs-lookup"><span data-stu-id="d9e78-149">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="d9e78-150">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="d9e78-150">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="d9e78-151">共通のアドレス] ダイアログ ボックスのモーダル バージョンが表示されます。</span><span class="sxs-lookup"><span data-stu-id="d9e78-151">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="d9e78-152">このフラグは、DIALOG_SDI と相互に排他的です。</span><span class="sxs-lookup"><span data-stu-id="d9e78-152">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="d9e78-153">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="d9e78-153">DIALOG_SDI</span></span>
  
> <span data-ttu-id="d9e78-154">モードレスのバージョンの共通のアドレス] ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="d9e78-154">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="d9e78-155">このフラグは、DIALOG_MODAL と相互に排他的です。</span><span class="sxs-lookup"><span data-stu-id="d9e78-155">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="d9e78-156">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d9e78-156">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="d9e78-157">渡された文字列は、Unicode 形式では。</span><span class="sxs-lookup"><span data-stu-id="d9e78-157">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="d9e78-158">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。</span><span class="sxs-lookup"><span data-stu-id="d9e78-158">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    

