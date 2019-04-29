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
# <a name="hropenabentrywithprovideruidsupport"></a><span data-ttu-id="a0205-103">HrOpenABEntryWithProviderUIDSupport</span><span class="sxs-lookup"><span data-stu-id="a0205-103">HrOpenABEntryWithProviderUIDSupport</span></span>

  
  
<span data-ttu-id="a0205-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a0205-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a0205-105">hropenabentrywithprovideruid 関数と同じ機能を実行します。ただし、 **hroentryabentrywithprovideruidsupport**関数は、セッションとアドレス帳を使用するのではなく、指定されたサポートオブジェクトを使用してエントリを開きます。 [](hropenabentrywithprovideruid.md)</span><span class="sxs-lookup"><span data-stu-id="a0205-105">Performs the same function as the [HrOpenABEntryWithProviderUID](hropenabentrywithprovideruid.md) function except that the **HrOpenABEntryWithProviderUIDSupport** function opens the entry using the given support object instead of using the session and the address book.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a0205-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="a0205-106">Header file:</span></span>  <br/> |<span data-ttu-id="a0205-107">abhelp .h</span><span class="sxs-lookup"><span data-stu-id="a0205-107">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="a0205-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="a0205-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a0205-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a0205-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a0205-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="a0205-110">Called by:</span></span>  <br/> |<span data-ttu-id="a0205-111">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="a0205-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="a0205-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a0205-112">Parameters</span></span>

 <span data-ttu-id="a0205-113">_pEmsabpUID_</span><span class="sxs-lookup"><span data-stu-id="a0205-113">_pEmsabpUID_</span></span>
  
> <span data-ttu-id="a0205-114">順番この関数がエントリ識別子の詳細を表示するために使用する Exchange アドレス帳プロバイダーを識別する_emsabpUID_パラメーターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="a0205-114">[in] A pointer to an  _emsabpUID_ parameter that identifies the Exchange address book provider that this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="a0205-115">入力されたエントリ識別子が Exchange アドレス帳プロバイダーのエントリ識別子ではない場合、このパラメーターは無視され、関数呼び出しは[IAddrBook::D etails](iaddrbook-details.md)と同じように動作します。</span><span class="sxs-lookup"><span data-stu-id="a0205-115">If the incoming entry identifier is not an Exchange address book provider entry identifier, this parameter is ignored and the function call acts exactly like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="a0205-116">このパラメーターが NULL またはゼロ MAPIUID の場合は、この関数も[IAddrBook::D etails](iaddrbook-details.md)と同じように動作します。</span><span class="sxs-lookup"><span data-stu-id="a0205-116">If this parameter is NULL or a zero MAPIUID, this function also acts exactly like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="a0205-117">_lpsup_</span><span class="sxs-lookup"><span data-stu-id="a0205-117">_lpSup_</span></span>
  
> 
    
 <span data-ttu-id="a0205-118">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="a0205-118">_cbEntryID_</span></span>
  
> <span data-ttu-id="a0205-119">順番_lな tryid_パラメーターで指定されたエントリ id のバイト数。</span><span class="sxs-lookup"><span data-stu-id="a0205-119">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="a0205-120">_lて tryid_</span><span class="sxs-lookup"><span data-stu-id="a0205-120">_lpEntryID_</span></span>
  
> <span data-ttu-id="a0205-121">順番開くアドレス帳のエントリを表すエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a0205-121">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="a0205-122">_lpinterface_</span><span class="sxs-lookup"><span data-stu-id="a0205-122">_lpInterface_</span></span>
  
> <span data-ttu-id="a0205-123">順番開いているエントリへのアクセスに使用するインターフェイスのインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a0205-123">[in] A pointer to the interface identifier (IID) of the interface to be used to access the open entry.</span></span> <span data-ttu-id="a0205-124">NULL を渡すと、オブジェクトの標準インターフェイスが返されます。</span><span class="sxs-lookup"><span data-stu-id="a0205-124">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="a0205-125">メッセージングユーザーの場合、標準インターフェイスは[imailuser: imapiprop](imailuserimapiprop.md)です。</span><span class="sxs-lookup"><span data-stu-id="a0205-125">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="a0205-126">配布リストの場合、これは[idistlist: IMAPIContainer](idistlistimapicontainer.md)で、コンテナーの場合は[IABContainer: IMAPIContainer](iabcontainerimapicontainer.md)です。</span><span class="sxs-lookup"><span data-stu-id="a0205-126">For distribution lists it is [IDistList : IMAPIContainer](idistlistimapicontainer.md), and for containers it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="a0205-127">呼び出し元は、 _lpinterface_を適切な標準インターフェイスまたは継承階層内のインターフェイスに設定できます。</span><span class="sxs-lookup"><span data-stu-id="a0205-127">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="a0205-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a0205-128">_ulFlags_</span></span>
  
> <span data-ttu-id="a0205-129">順番_lpszbuttontext_パラメーターのテキストの種類を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="a0205-129">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="a0205-130">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="a0205-130">The following flags can be set:</span></span> 
    
<span data-ttu-id="a0205-131">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="a0205-131">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="a0205-132">住所に変更が実際に加えられた場合に、詳細が TRUE を返すことを示します。それ以外の場合、詳細は FALSE を返します。</span><span class="sxs-lookup"><span data-stu-id="a0205-132">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="a0205-133">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="a0205-133">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="a0205-134">[共通アドレス] ダイアログボックスのモーダルバージョンが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a0205-134">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="a0205-135">このフラグは、DIALOG_SDI とは相互に排他的です。</span><span class="sxs-lookup"><span data-stu-id="a0205-135">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="a0205-136">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="a0205-136">DIALOG_SDI</span></span>
  
> <span data-ttu-id="a0205-137">[共通アドレス] ダイアログボックスのモードレスバージョンが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a0205-137">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="a0205-138">このフラグは、DIALOG_MODAL とは相互に排他的です。</span><span class="sxs-lookup"><span data-stu-id="a0205-138">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="a0205-139">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a0205-139">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="a0205-140">渡された文字列は Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="a0205-140">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="a0205-141">MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="a0205-141">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="a0205-142">_lpulobjtype_</span><span class="sxs-lookup"><span data-stu-id="a0205-142">_lpulObjType_</span></span>
  
> <span data-ttu-id="a0205-143">読み上げ開かれた項目の種類へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a0205-143">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="a0205-144">_lppunk_</span><span class="sxs-lookup"><span data-stu-id="a0205-144">_lppUnk_</span></span>
  
> <span data-ttu-id="a0205-145">読み上げ開かれたエントリのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="a0205-145">[out] A pointer to a pointer of the opened entry.</span></span>
    

