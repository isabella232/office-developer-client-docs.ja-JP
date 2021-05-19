---
title: HrDoABDetailsWithExchangeContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b4e7fed2-88e4-4e14-90b6-913a1b7e338a
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 353a663071a9f23f0d2330169d3ac7747e047c2b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421369"
---
# <a name="hrdoabdetailswithexchangecontext"></a><span data-ttu-id="e512b-103">HrDoABDetailsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="e512b-103">HrDoABDetailsWithExchangeContext</span></span>

  
  
<span data-ttu-id="e512b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e512b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e512b-105">**OpenEntry** メソッドが、予想されるアドレス帳プロバイダーによって開Exchange確認します。</span><span class="sxs-lookup"><span data-stu-id="e512b-105">Ensures that the **OpenEntry** method is opened by the expected Exchange address book provider.</span></span> <span data-ttu-id="e512b-106">この関数は [IAddrBook::D etails](iaddrbook-details.md)と同様に動作しますが _、pEmsmdbUID_ パラメーターで識別される Exchange アドレス帳を使用して **entryID** を開きます。</span><span class="sxs-lookup"><span data-stu-id="e512b-106">This function works similarly to [IAddrBook::Details](iaddrbook-details.md), but opens the **entryID** using the Exchange address book identified by the  _pEmsmdbUID_ parameter.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e512b-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="e512b-107">Header file:</span></span>  <br/> |<span data-ttu-id="e512b-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="e512b-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="e512b-109">実装元:</span><span class="sxs-lookup"><span data-stu-id="e512b-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="e512b-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="e512b-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="e512b-111">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="e512b-111">Called by:</span></span>  <br/> |<span data-ttu-id="e512b-112">クライアント アプリケーションとサービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="e512b-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="e512b-113">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e512b-113">Parameters</span></span>

 <span data-ttu-id="e512b-114">_pmsess_</span><span class="sxs-lookup"><span data-stu-id="e512b-114">_pmsess_</span></span>
  
> <span data-ttu-id="e512b-115">ログオンしている **IMAPISession**。</span><span class="sxs-lookup"><span data-stu-id="e512b-115">The logged on **IMAPISession**.</span></span> <span data-ttu-id="e512b-116">NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="e512b-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="e512b-117">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="e512b-117">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="e512b-118">エントリ識別子を開く関数で使用される Exchange アドレス帳プロバイダーを含む Exchange Service を識別する **emsmdbUID** へのポインター。</span><span class="sxs-lookup"><span data-stu-id="e512b-118">A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange address book provider that is used by the function to open the entry identifier.</span></span> <span data-ttu-id="e512b-119">受信エントリ識別子がアドレス帳プロバイダー Exchange識別子ではない場合、このパラメーターは無視され、関数は[IAddrBook::OpenEntry のように動作します](iaddrbook-openentry.md)。</span><span class="sxs-lookup"><span data-stu-id="e512b-119">If the incoming entry identifier is not an Exchange address book provider entry identifier, this parameter is ignored and the function behaves like [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span> <span data-ttu-id="e512b-120">このパラメーターが NULL または 0 **の MAPIUID** の場合、この関数は [IAddrBook::OpenEntry とまったく同じ動作をします](iaddrbook-openentry.md)。</span><span class="sxs-lookup"><span data-stu-id="e512b-120">If this parameter is NULL or a zero **MAPIUID**, this function also acts exactly like [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span> 
    
 <span data-ttu-id="e512b-121">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="e512b-121">_pAddrBook_</span></span>
  
> <span data-ttu-id="e512b-122">[in]エントリ識別子を開くのに使用するアドレス帳。</span><span class="sxs-lookup"><span data-stu-id="e512b-122">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="e512b-123">NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="e512b-123">It cannot be NULL.</span></span>
    
 <span data-ttu-id="e512b-124">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="e512b-124">_lpulUIParam_</span></span>
  
> <span data-ttu-id="e512b-125">[out]ダイアログ ボックスの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="e512b-125">[out] A handle to the parent window for the dialog box.</span></span>
    
 <span data-ttu-id="e512b-126">_lpfnDismiss_</span><span class="sxs-lookup"><span data-stu-id="e512b-126">_lpfnDismiss_</span></span>
  
> <span data-ttu-id="e512b-127">[in] **DISMISSMODELESS** プロトタイプまたは NULL に基づく関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="e512b-127">[in] A pointer to a function based on the **DISMISSMODELESS** prototype, or NULL.</span></span> <span data-ttu-id="e512b-128">このメンバーは、設定されているオプション フラグで示されているモードレス DIALOG_SDIダイアログ ボックスにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="e512b-128">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="e512b-129">MAPI は、ユーザーがモードレス アドレス ダイアログ ボックスを閉じ、ダイアログ ボックスがアクティブでなくなった詳細を呼び出しているクライアントに通知するときに **DISMISSMODELESS** 関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e512b-129">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client that is calling Details that the dialog box is no longer active.</span></span> 
    
 <span data-ttu-id="e512b-130">_lpvDismissContext_</span><span class="sxs-lookup"><span data-stu-id="e512b-130">_lpvDismissContext_</span></span>
  
> <span data-ttu-id="e512b-131">[in]_lpfnDismiss_ パラメーターが指す **DISMISSMODELESS** 関数に渡すコンテキスト情報へのポインター。</span><span class="sxs-lookup"><span data-stu-id="e512b-131">[in] A pointer to context information to pass to the **DISMISSMODELESS** function pointed to by the  _lpfnDismiss_ parameter.</span></span> <span data-ttu-id="e512b-132">このパラメーターは _、ulFlags_ パラメーターに DIALOG_SDIを含めて、ダイアログ ボックス **のモードレス** バージョンにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="e512b-132">This parameter applies only to the modeless version of the dialog box by including the **DIALOG_SDI** flag in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="e512b-133">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="e512b-133">_cbEntryID_</span></span>
  
> <span data-ttu-id="e512b-134">[in]  _lpEntryID_ パラメーターで指定されたエントリ識別子のバイト 数。</span><span class="sxs-lookup"><span data-stu-id="e512b-134">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="e512b-135">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="e512b-135">_lpEntryID_</span></span>
  
> <span data-ttu-id="e512b-136">[in]開くアドレス帳エントリを表すエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="e512b-136">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="e512b-137">_lpfButtonCallback_</span><span class="sxs-lookup"><span data-stu-id="e512b-137">_lpfButtonCallback_</span></span>
  
> <span data-ttu-id="e512b-138">[in] **LPFNBUTTON 関数プロトタイプに基づく関数への** ポインター。</span><span class="sxs-lookup"><span data-stu-id="e512b-138">[in] A pointer to a function based on the **LPFNBUTTON** function prototype.</span></span> <span data-ttu-id="e512b-139">**LPFNBUTTON 関数は**、詳細ダイアログ ボックスにボタンを追加します。</span><span class="sxs-lookup"><span data-stu-id="e512b-139">An **LPFNBUTTON** function adds a button to the details dialog box.</span></span> 
    
 <span data-ttu-id="e512b-140">_lpvButtonContext_</span><span class="sxs-lookup"><span data-stu-id="e512b-140">_lpvButtonContext_</span></span>
  
> <span data-ttu-id="e512b-141">[in]  _lpfButtonCallback_ パラメーターで指定された関数のパラメーターとして使用されたデータへのポインター。</span><span class="sxs-lookup"><span data-stu-id="e512b-141">[in] A pointer to data that was used as a parameter for the function specified by the  _lpfButtonCallback_ parameter.</span></span> 
    
 <span data-ttu-id="e512b-142">_lpszButtonText_</span><span class="sxs-lookup"><span data-stu-id="e512b-142">_lpszButtonText_</span></span>
  
> <span data-ttu-id="e512b-143">[in]追加されたボタンに適用するテキストを含む文字列へのポインター (そのボタンが拡張可能な場合)。</span><span class="sxs-lookup"><span data-stu-id="e512b-143">[in] A pointer to a string that contains text to be applied to the added button, if that button is extensible.</span></span> <span data-ttu-id="e512b-144">_拡張可能ボタンが不要な場合、lpszButtonText_ パラメーターは NULL である必要があります。</span><span class="sxs-lookup"><span data-stu-id="e512b-144">The  _lpszButtonText_ parameter should be NULL when an extensible button is not needed.</span></span> 
    
 <span data-ttu-id="e512b-145">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e512b-145">_ulFlags_</span></span>
  
> <span data-ttu-id="e512b-146">[in]  _lpszButtonText_ パラメーターのテキストの種類を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="e512b-146">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="e512b-147">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="e512b-147">The following flags can be set:</span></span> 
    
<span data-ttu-id="e512b-148">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="e512b-148">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="e512b-149">アドレスに実際に変更が加えた場合、Details は TRUE を返します。それ以外の場合、Details は FALSE を返します。</span><span class="sxs-lookup"><span data-stu-id="e512b-149">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="e512b-150">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="e512b-150">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="e512b-151">[共通アドレス] ダイアログ ボックスのモーダル バージョンを表示します。</span><span class="sxs-lookup"><span data-stu-id="e512b-151">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="e512b-152">このフラグは、このフラグと相互にDIALOG_SDI。</span><span class="sxs-lookup"><span data-stu-id="e512b-152">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="e512b-153">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="e512b-153">DIALOG_SDI</span></span>
  
> <span data-ttu-id="e512b-154">[共通アドレス] ダイアログ ボックスのモードレス バージョンを表示します。</span><span class="sxs-lookup"><span data-stu-id="e512b-154">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="e512b-155">このフラグは、他のフラグと相互DIALOG_MODAL。</span><span class="sxs-lookup"><span data-stu-id="e512b-155">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="e512b-156">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e512b-156">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="e512b-157">渡された文字列は Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="e512b-157">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="e512b-158">このフラグMAPI_UNICODE設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="e512b-158">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    

