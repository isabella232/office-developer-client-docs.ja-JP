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
ms.openlocfilehash: 353a663071a9f23f0d2330169d3ac7747e047c2b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347853"
---
# <a name="hrdoabdetailswithexchangecontext"></a><span data-ttu-id="be28c-103">HrDoABDetailsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="be28c-103">HrDoABDetailsWithExchangeContext</span></span>

  
  
<span data-ttu-id="be28c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="be28c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="be28c-105">必要な Exchange アドレス帳プロバイダーが**openentry**メソッドを開いていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="be28c-105">Ensures that the **OpenEntry** method is opened by the expected Exchange address book provider.</span></span> <span data-ttu-id="be28c-106">この関数は[IAddrBook::D etails](iaddrbook-details.md)と同様に動作しますが、 _pEmsmdbUID_パラメーターによって識別される Exchange アドレス帳を使用して**entryID**を開きます。</span><span class="sxs-lookup"><span data-stu-id="be28c-106">This function works similarly to [IAddrBook::Details](iaddrbook-details.md), but opens the **entryID** using the Exchange address book identified by the  _pEmsmdbUID_ parameter.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="be28c-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="be28c-107">Header file:</span></span>  <br/> |<span data-ttu-id="be28c-108">abhelp .h</span><span class="sxs-lookup"><span data-stu-id="be28c-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="be28c-109">実装元:</span><span class="sxs-lookup"><span data-stu-id="be28c-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="be28c-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="be28c-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="be28c-111">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="be28c-111">Called by:</span></span>  <br/> |<span data-ttu-id="be28c-112">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="be28c-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="be28c-113">パラメーター</span><span class="sxs-lookup"><span data-stu-id="be28c-113">Parameters</span></span>

 <span data-ttu-id="be28c-114">_pmsess_</span><span class="sxs-lookup"><span data-stu-id="be28c-114">_pmsess_</span></span>
  
> <span data-ttu-id="be28c-115">ログオンしている**imapisession**。</span><span class="sxs-lookup"><span data-stu-id="be28c-115">The logged on **IMAPISession**.</span></span> <span data-ttu-id="be28c-116">NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="be28c-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="be28c-117">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="be28c-117">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="be28c-118">エントリ id を開くために関数によって使用される exchange アドレス帳プロバイダーを含む exchange サービスを識別する**emsmdbUID**へのポインター。</span><span class="sxs-lookup"><span data-stu-id="be28c-118">A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange address book provider that is used by the function to open the entry identifier.</span></span> <span data-ttu-id="be28c-119">受信エントリ識別子が Exchange アドレス帳プロバイダーエントリ識別子ではない場合、このパラメーターは無視され、関数は[IAddrBook:: openentry](iaddrbook-openentry.md)と同様に動作します。</span><span class="sxs-lookup"><span data-stu-id="be28c-119">If the incoming entry identifier is not an Exchange address book provider entry identifier, this parameter is ignored and the function behaves like [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span> <span data-ttu-id="be28c-120">このパラメーターが NULL またはゼロ**MAPIUID**の場合は、この関数も[IAddrBook:: openentry](iaddrbook-openentry.md)と同じように動作します。</span><span class="sxs-lookup"><span data-stu-id="be28c-120">If this parameter is NULL or a zero **MAPIUID**, this function also acts exactly like [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span> 
    
 <span data-ttu-id="be28c-121">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="be28c-121">_pAddrBook_</span></span>
  
> <span data-ttu-id="be28c-122">順番エントリ識別子を開くために使用されるアドレス帳。</span><span class="sxs-lookup"><span data-stu-id="be28c-122">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="be28c-123">NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="be28c-123">It cannot be NULL.</span></span>
    
 <span data-ttu-id="be28c-124">_l出 uiparam_</span><span class="sxs-lookup"><span data-stu-id="be28c-124">_lpulUIParam_</span></span>
  
> <span data-ttu-id="be28c-125">読み上げダイアログボックスの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="be28c-125">[out] A handle to the parent window for the dialog box.</span></span>
    
 <span data-ttu-id="be28c-126">_lpfnDismiss_</span><span class="sxs-lookup"><span data-stu-id="be28c-126">_lpfnDismiss_</span></span>
  
> <span data-ttu-id="be28c-127">順番**DISMISSMODELESS**プロトタイプに基づく関数へのポインター、または NULL。</span><span class="sxs-lookup"><span data-stu-id="be28c-127">[in] A pointer to a function based on the **DISMISSMODELESS** prototype, or NULL.</span></span> <span data-ttu-id="be28c-128">このメンバーは、DIALOG_SDI フラグが設定されている場合のように、ダイアログボックスのモードレスバージョンにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="be28c-128">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="be28c-129">MAPI は、ユーザーがモードレスアドレスダイアログボックスを閉じたときに、そのダイアログボックスがアクティブでなくなったことを示す詳細を呼び出していることをクライアントに通知する**DISMISSMODELESS**関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="be28c-129">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client that is calling Details that the dialog box is no longer active.</span></span> 
    
 <span data-ttu-id="be28c-130">_lpvDismissContext_</span><span class="sxs-lookup"><span data-stu-id="be28c-130">_lpvDismissContext_</span></span>
  
> <span data-ttu-id="be28c-131">順番_lpfnDismiss_パラメーターが指す**DISMISSMODELESS**関数に渡すコンテキスト情報へのポインター。</span><span class="sxs-lookup"><span data-stu-id="be28c-131">[in] A pointer to context information to pass to the **DISMISSMODELESS** function pointed to by the  _lpfnDismiss_ parameter.</span></span> <span data-ttu-id="be28c-132">このパラメーターは、 **DIALOG_SDI**フラグを_ulflags_パラメーターに含めることによって、ダイアログボックスのモードレスバージョンにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="be28c-132">This parameter applies only to the modeless version of the dialog box by including the **DIALOG_SDI** flag in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="be28c-133">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="be28c-133">_cbEntryID_</span></span>
  
> <span data-ttu-id="be28c-134">順番_lな tryid_パラメーターで指定されたエントリ id のバイト数。</span><span class="sxs-lookup"><span data-stu-id="be28c-134">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="be28c-135">_lて tryid_</span><span class="sxs-lookup"><span data-stu-id="be28c-135">_lpEntryID_</span></span>
  
> <span data-ttu-id="be28c-136">順番開くアドレス帳のエントリを表すエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="be28c-136">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="be28c-137">_lpfbuttoncallback_</span><span class="sxs-lookup"><span data-stu-id="be28c-137">_lpfButtonCallback_</span></span>
  
> <span data-ttu-id="be28c-138">順番**LPFNBUTTON**関数プロトタイプに基づく関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="be28c-138">[in] A pointer to a function based on the **LPFNBUTTON** function prototype.</span></span> <span data-ttu-id="be28c-139">**LPFNBUTTON**関数は、[詳細] ダイアログボックスにボタンを追加します。</span><span class="sxs-lookup"><span data-stu-id="be28c-139">An **LPFNBUTTON** function adds a button to the details dialog box.</span></span> 
    
 <span data-ttu-id="be28c-140">_lpvbuttoncontext_</span><span class="sxs-lookup"><span data-stu-id="be28c-140">_lpvButtonContext_</span></span>
  
> <span data-ttu-id="be28c-141">順番_lpfbuttoncallback_パラメーターで指定された関数のパラメーターとして使用されたデータへのポインター。</span><span class="sxs-lookup"><span data-stu-id="be28c-141">[in] A pointer to data that was used as a parameter for the function specified by the  _lpfButtonCallback_ parameter.</span></span> 
    
 <span data-ttu-id="be28c-142">_lpszbuttontext_</span><span class="sxs-lookup"><span data-stu-id="be28c-142">_lpszButtonText_</span></span>
  
> <span data-ttu-id="be28c-143">順番追加されたボタンに適用されるテキストを含む文字列へのポインター。ボタンが拡張可能な場合です。</span><span class="sxs-lookup"><span data-stu-id="be28c-143">[in] A pointer to a string that contains text to be applied to the added button, if that button is extensible.</span></span> <span data-ttu-id="be28c-144">拡張ボタンを必要としない場合は、 _lpszbuttontext_パラメーターを NULL に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="be28c-144">The  _lpszButtonText_ parameter should be NULL when an extensible button is not needed.</span></span> 
    
 <span data-ttu-id="be28c-145">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="be28c-145">_ulFlags_</span></span>
  
> <span data-ttu-id="be28c-146">順番_lpszbuttontext_パラメーターのテキストの種類を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="be28c-146">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="be28c-147">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="be28c-147">The following flags can be set:</span></span> 
    
<span data-ttu-id="be28c-148">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="be28c-148">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="be28c-149">住所に変更が実際に加えられた場合に、詳細が TRUE を返すことを示します。それ以外の場合、詳細は FALSE を返します。</span><span class="sxs-lookup"><span data-stu-id="be28c-149">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="be28c-150">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="be28c-150">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="be28c-151">[共通アドレス] ダイアログボックスのモーダルバージョンが表示されます。</span><span class="sxs-lookup"><span data-stu-id="be28c-151">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="be28c-152">このフラグは、DIALOG_SDI とは相互に排他的です。</span><span class="sxs-lookup"><span data-stu-id="be28c-152">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="be28c-153">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="be28c-153">DIALOG_SDI</span></span>
  
> <span data-ttu-id="be28c-154">[共通アドレス] ダイアログボックスのモードレスバージョンが表示されます。</span><span class="sxs-lookup"><span data-stu-id="be28c-154">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="be28c-155">このフラグは、DIALOG_MODAL とは相互に排他的です。</span><span class="sxs-lookup"><span data-stu-id="be28c-155">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="be28c-156">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="be28c-156">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="be28c-157">渡された文字列は Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="be28c-157">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="be28c-158">MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="be28c-158">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    

