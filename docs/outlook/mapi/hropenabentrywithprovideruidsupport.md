---
title: HrOpenABEntryWithProviderUIDSupport
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1fafc810-7cf3-4c8c-bf21-055ae34da690
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: bd42fcd34042c2f9579497f164c4a67f6ba97e35
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800338"
---
# <a name="hropenabentrywithprovideruidsupport"></a><span data-ttu-id="95c43-103">HrOpenABEntryWithProviderUIDSupport</span><span class="sxs-lookup"><span data-stu-id="95c43-103">HrOpenABEntryWithProviderUIDSupport</span></span>

  
  
<span data-ttu-id="95c43-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="95c43-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="95c43-105">**HrOpenABEntryWithProviderUIDSupport**関数は、セッションとアドレス帳を使用する代わりに特定のサポート オブジェクトを使用してエントリを開きますが、 [HrOpenABEntryWithProviderUID](hropenabentrywithprovideruid.md)関数と同じ機能を実行します。</span><span class="sxs-lookup"><span data-stu-id="95c43-105">Performs the same function as the [HrOpenABEntryWithProviderUID](hropenabentrywithprovideruid.md) function except that the **HrOpenABEntryWithProviderUIDSupport** function opens the entry using the given support object instead of using the session and the address book.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="95c43-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="95c43-106">Header file:</span></span>  <br/> |<span data-ttu-id="95c43-107">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="95c43-107">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="95c43-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="95c43-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="95c43-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="95c43-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="95c43-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="95c43-110">Called by:</span></span>  <br/> |<span data-ttu-id="95c43-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="95c43-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="95c43-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="95c43-112">Parameters</span></span>

 <span data-ttu-id="95c43-113">_pEmsabpUID_</span><span class="sxs-lookup"><span data-stu-id="95c43-113">_pEmsabpUID_</span></span>
  
> <span data-ttu-id="95c43-114">[in]エントリ id の詳細を表示するのにはこの関数を使用する必要があります Exchange のアドレス帳プロバイダーを識別する_emsabpUID_のパラメーターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="95c43-114">[in] A pointer to an  _emsabpUID_ parameter that identifies the Exchange address book provider that this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="95c43-115">受信のエントリ id が Exchange アドレス帳プロバイダー エントリ識別子ではない場合は、このパラメーターは無視され、 [IAddrBook::Details](iaddrbook-details.md)関数の呼び出しの動作とまったく同じです。</span><span class="sxs-lookup"><span data-stu-id="95c43-115">If the incoming entry identifier is not an Exchange address book provider entry identifier, this parameter is ignored and the function call acts exactly like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="95c43-116">このパラメーターが NULL またはゼロの MAPIUID の場合は、この関数はまた[IAddrBook::Details](iaddrbook-details.md)と同様に機能します。</span><span class="sxs-lookup"><span data-stu-id="95c43-116">If this parameter is NULL or a zero MAPIUID, this function also acts exactly like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="95c43-117">_lpSup_</span><span class="sxs-lookup"><span data-stu-id="95c43-117">_lpSup_</span></span>
  
> 
    
 <span data-ttu-id="95c43-118">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="95c43-118">_cbEntryID_</span></span>
  
> <span data-ttu-id="95c43-119">[in]_LpEntryID_パラメーターで指定されたエントリの識別子のバイト数です。</span><span class="sxs-lookup"><span data-stu-id="95c43-119">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="95c43-120">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="95c43-120">_lpEntryID_</span></span>
  
> <span data-ttu-id="95c43-121">[in]開くにはアドレス帳のエントリを表すエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="95c43-121">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="95c43-122">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="95c43-122">_lpInterface_</span></span>
  
> <span data-ttu-id="95c43-123">[in][Open] エントリにアクセスするために使用するインターフェイスのインターフェイス id (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="95c43-123">[in] A pointer to the interface identifier (IID) of the interface to be used to access the open entry.</span></span> <span data-ttu-id="95c43-124">NULL を渡すことは、標準的なオブジェクトのインターフェイスを返します。</span><span class="sxs-lookup"><span data-stu-id="95c43-124">Passing NULL returns the standard interface of the object.</span></span> <span data-ttu-id="95c43-125">メッセージング ユーザーは、標準のインタ フェースは[IMailUser: IMAPIProp](imailuserimapiprop.md)。</span><span class="sxs-lookup"><span data-stu-id="95c43-125">For messaging users, the standard interface is [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span> <span data-ttu-id="95c43-126">配布リストには、 [IDistList: IMAPIContainer](idistlistimapicontainer.md)とは、コンテナーの[これにより: IMAPIContainer](iabcontainerimapicontainer.md)。</span><span class="sxs-lookup"><span data-stu-id="95c43-126">For distribution lists it is [IDistList : IMAPIContainer](idistlistimapicontainer.md), and for containers it is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="95c43-127">呼び出し元は、適切な標準インターフェイスまたはインターフェイスの継承階層内に_lpInterface_を設定できます。</span><span class="sxs-lookup"><span data-stu-id="95c43-127">Callers can set  _lpInterface_ to the appropriate standard interface or an interface in the inheritance hierarchy.</span></span> 
    
 <span data-ttu-id="95c43-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="95c43-128">_ulFlags_</span></span>
  
> <span data-ttu-id="95c43-129">[in]_LpszButtonText_パラメーターのテキストの種類を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="95c43-129">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="95c43-130">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="95c43-130">The following flags can be set:</span></span> 
    
<span data-ttu-id="95c43-131">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="95c43-131">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="95c43-132">詳細は TRUE を返す場合は、アドレスに変更を加えた実際にことを示します。それ以外の場合、詳細は、FALSE を返します。</span><span class="sxs-lookup"><span data-stu-id="95c43-132">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="95c43-133">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="95c43-133">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="95c43-134">共通のアドレス] ダイアログ ボックスのモーダル バージョンが表示されます。</span><span class="sxs-lookup"><span data-stu-id="95c43-134">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="95c43-135">このフラグは、DIALOG_SDI と相互に排他的です。</span><span class="sxs-lookup"><span data-stu-id="95c43-135">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="95c43-136">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="95c43-136">DIALOG_SDI</span></span>
  
> <span data-ttu-id="95c43-137">モードレスのバージョンの共通のアドレス] ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="95c43-137">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="95c43-138">このフラグは、DIALOG_MODAL と相互に排他的です。</span><span class="sxs-lookup"><span data-stu-id="95c43-138">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="95c43-139">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="95c43-139">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="95c43-140">渡された文字列は、Unicode 形式では。</span><span class="sxs-lookup"><span data-stu-id="95c43-140">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="95c43-141">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。</span><span class="sxs-lookup"><span data-stu-id="95c43-141">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="95c43-142">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="95c43-142">_lpulObjType_</span></span>
  
> <span data-ttu-id="95c43-143">[out]開かれているエントリの種類へのポインター。</span><span class="sxs-lookup"><span data-stu-id="95c43-143">[out] A pointer to the type of the opened entry.</span></span>
    
 <span data-ttu-id="95c43-144">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="95c43-144">_lppUnk_</span></span>
  
> <span data-ttu-id="95c43-145">[out]開かれているエントリのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="95c43-145">[out] A pointer to a pointer of the opened entry.</span></span>
    

