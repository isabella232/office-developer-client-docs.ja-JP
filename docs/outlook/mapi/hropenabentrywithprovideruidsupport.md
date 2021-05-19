---
title: HrOpenABEntryWithProviderUIDSupport
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1fafc810-7cf3-4c8c-bf21-055ae34da690
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: da40e240b60fa42c48185600b74c6162a966e6f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409546"
---
# <a name="hropenabentrywithprovideruidsupport"></a><span data-ttu-id="00ed1-103">HrOpenABEntryWithProviderUIDSupport</span><span class="sxs-lookup"><span data-stu-id="00ed1-103">HrOpenABEntryWithProviderUIDSupport</span></span>

  
  
<span data-ttu-id="00ed1-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="00ed1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="00ed1-105">[HrOpenABEntryWithProviderUID](hropenabentrywithprovideruid.md)関数と同じ関数を実行しますが **、HrOpenABEntryWithProviderUIDSupport** 関数は、セッションとアドレス帳を使用する代わりに、指定されたサポート オブジェクトを使用してエントリを開きます。</span><span class="sxs-lookup"><span data-stu-id="00ed1-105">Performs the same function as the [HrOpenABEntryWithProviderUID](hropenabentrywithprovideruid.md) function except that the **HrOpenABEntryWithProviderUIDSupport** function opens the entry using the given support object instead of using the session and the address book.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="00ed1-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="00ed1-106">Header file:</span></span>  <br/> |<span data-ttu-id="00ed1-107">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="00ed1-107">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="00ed1-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="00ed1-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="00ed1-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="00ed1-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="00ed1-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="00ed1-110">Called by:</span></span>  <br/> |<span data-ttu-id="00ed1-111">クライアント アプリケーションとサービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="00ed1-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrOpenABEntryWithProviderUIDSupport(
  const MAPIUID *pEmsabpUID,
  LPMAPISUP lpSup,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="00ed1-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="00ed1-112">Parameters</span></span>

 <span data-ttu-id="00ed1-113">_pEmsabpUID_</span><span class="sxs-lookup"><span data-stu-id="00ed1-113">_pEmsabpUID_</span></span>
  
> <span data-ttu-id="00ed1-114">[in]この関数がエントリ識別子の詳細を表示するために使用するExchangeアドレス帳プロバイダーを識別する _emsabpUID_ パラメーターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="00ed1-114">[in] A pointer to an  _emsabpUID_ parameter that identifies the Exchange address book provider that this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="00ed1-115">受信エントリ識別子が Exchange アドレス帳プロバイダーエントリ識別子ではない場合、このパラメーターは無視され、関数呼び出しは[IAddrBook::D](iaddrbook-details.md)とまったく同じ動作をします。</span><span class="sxs-lookup"><span data-stu-id="00ed1-115">If the incoming entry identifier is not an Exchange address book provider entry identifier, this parameter is ignored and the function call acts exactly like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="00ed1-116">このパラメーターが NULL または 0 の MAPIUID の場合、この関数は [IAddrBook::D同様に動作します](iaddrbook-details.md)。</span><span class="sxs-lookup"><span data-stu-id="00ed1-116">If this parameter is NULL or a zero MAPIUID, this function also acts exactly like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="00ed1-117">_lpSup_</span><span class="sxs-lookup"><span data-stu-id="00ed1-117">_lpSup_</span></span>
  
> 
    
 <span data-ttu-id="00ed1-118">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="00ed1-118">_cbEntryID_</span></span>
  
> <span data-ttu-id="00ed1-119">[in]  _lpEntryID_ パラメーターで指定されたエントリ識別子のバイト 数。</span><span class="sxs-lookup"><span data-stu-id="00ed1-119">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="00ed1-120">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="00ed1-120">_lpEntryID_</span></span>
  
> <span data-ttu-id="00ed1-121">[in]開くアドレス帳エントリを表すエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="00ed1-121">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="00ed1-122">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="00ed1-122">_lpInterface_</span></span>
  
> <span data-ttu-id="00ed1-123">[in]開いているエントリへのアクセスに使用するインターフェイスのインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="00ed1-123">[in] A pointer to the interface identifier (IID) of the interface to be used to access the open entry.</span></span> <span data-ttu-id="00ed1-124">NULL を渡す場合は、オブジェクトの標準インターフェイスを返します。</span><span class="sxs-lookup"><span data-stu-id="00ed1-124">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="00ed1-125">メッセージング ユーザーの場合、標準インターフェイスは [IMailUser : IMAPIProp です](imailuserimapiprop.md)。</span><span class="sxs-lookup"><span data-stu-id="00ed1-125">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="00ed1-126">配布リストの場合は [、IDistList : IMAPIContainer](idistlistimapicontainer.md)であり、コンテナーの場合は [IABContainer : IMAPIContainer です](iabcontainerimapicontainer.md)。</span><span class="sxs-lookup"><span data-stu-id="00ed1-126">For distribution lists it is [IDistList : IMAPIContainer](idistlistimapicontainer.md), and for containers it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="00ed1-127">呼び出し元は  _、lpInterface を_ 適切な標準インターフェイスまたは継承階層内のインターフェイスに設定できます。</span><span class="sxs-lookup"><span data-stu-id="00ed1-127">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="00ed1-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="00ed1-128">_ulFlags_</span></span>
  
> <span data-ttu-id="00ed1-129">[in]  _lpszButtonText_ パラメーターのテキストの種類を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="00ed1-129">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="00ed1-130">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="00ed1-130">The following flags can be set:</span></span> 
    
<span data-ttu-id="00ed1-131">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="00ed1-131">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="00ed1-132">アドレスに実際に変更が加えた場合、Details は TRUE を返します。それ以外の場合、Details は FALSE を返します。</span><span class="sxs-lookup"><span data-stu-id="00ed1-132">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="00ed1-133">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="00ed1-133">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="00ed1-134">[共通アドレス] ダイアログ ボックスのモーダル バージョンを表示します。</span><span class="sxs-lookup"><span data-stu-id="00ed1-134">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="00ed1-135">このフラグは、このフラグと相互にDIALOG_SDI。</span><span class="sxs-lookup"><span data-stu-id="00ed1-135">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="00ed1-136">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="00ed1-136">DIALOG_SDI</span></span>
  
> <span data-ttu-id="00ed1-137">[共通アドレス] ダイアログ ボックスのモードレス バージョンを表示します。</span><span class="sxs-lookup"><span data-stu-id="00ed1-137">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="00ed1-138">このフラグは、他のフラグと相互DIALOG_MODAL。</span><span class="sxs-lookup"><span data-stu-id="00ed1-138">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="00ed1-139">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="00ed1-139">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="00ed1-140">渡された文字列は Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="00ed1-140">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="00ed1-141">このフラグMAPI_UNICODE設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="00ed1-141">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="00ed1-142">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="00ed1-142">_lpulObjType_</span></span>
  
> <span data-ttu-id="00ed1-143">[out]開いたエントリの種類へのポインター。</span><span class="sxs-lookup"><span data-stu-id="00ed1-143">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="00ed1-144">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="00ed1-144">_lppUnk_</span></span>
  
> <span data-ttu-id="00ed1-145">[out]開いたエントリのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="00ed1-145">[out] A pointer to a pointer of the opened entry.</span></span>
    

