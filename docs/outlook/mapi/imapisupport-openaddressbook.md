---
title: IMAPISupportOpenAddressBook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.OpenAddressBook
api_type:
- COM
ms.assetid: d8da8be1-3efe-410a-bcce-49e522602d80
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 47a62b331ff9f1c96576d42797ebb23ed61cd362
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416882"
---
# <a name="imapisupportopenaddressbook"></a><span data-ttu-id="162fc-103">IMAPISupport::OpenAddressBook</span><span class="sxs-lookup"><span data-stu-id="162fc-103">IMAPISupport::OpenAddressBook</span></span>

  
  
<span data-ttu-id="162fc-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="162fc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="162fc-105">アドレス帳へのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="162fc-105">Provides access to the address book.</span></span>
  
```cpp
HRESULT OpenAddressBook(
LPCIID lpInterface,
ULONG ulFlags,
LPADRBOOK FAR * lppAdrBook
);
```

## <a name="parameters"></a><span data-ttu-id="162fc-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="162fc-106">Parameters</span></span>

 <span data-ttu-id="162fc-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="162fc-107">_lpInterface_</span></span>
  
> <span data-ttu-id="162fc-108">[in]アドレス帳へのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="162fc-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the address book.</span></span> <span data-ttu-id="162fc-109">有効な値は NULL で、標準のアドレス帳インターフェイス [IAddrBook](iaddrbookimapiprop.md)を示し、IID_IAddrBook。</span><span class="sxs-lookup"><span data-stu-id="162fc-109">Valid values are NULL, which indicates the standard address book interface [IAddrBook](iaddrbookimapiprop.md), and IID_IAddrBook.</span></span>
    
 <span data-ttu-id="162fc-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="162fc-110">_ulFlags_</span></span>
  
> <span data-ttu-id="162fc-111">予約済み。は 0 である必要があります。</span><span class="sxs-lookup"><span data-stu-id="162fc-111">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="162fc-112">_lppAdrBook_</span><span class="sxs-lookup"><span data-stu-id="162fc-112">_lppAdrBook_</span></span>
  
> <span data-ttu-id="162fc-113">[out]アドレス帳へのポインターを指すポインター。</span><span class="sxs-lookup"><span data-stu-id="162fc-113">[out] A pointer to a pointer to the address book.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="162fc-114">戻り値</span><span class="sxs-lookup"><span data-stu-id="162fc-114">Return value</span></span>

<span data-ttu-id="162fc-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="162fc-115">S_OK</span></span> 
  
> <span data-ttu-id="162fc-116">アドレス帳へのアクセスが提供された。</span><span class="sxs-lookup"><span data-stu-id="162fc-116">Access to the address book was provided.</span></span>
    
<span data-ttu-id="162fc-117">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="162fc-117">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="162fc-118">呼び出しは成功しましたが、1 つ以上のアドレス帳プロバイダーを読み込む必要がありました。</span><span class="sxs-lookup"><span data-stu-id="162fc-118">The call succeeded, but one or more address book providers could not be loaded.</span></span> <span data-ttu-id="162fc-119">この警告が返されると、呼び出しは正常に処理されます。</span><span class="sxs-lookup"><span data-stu-id="162fc-119">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="162fc-120">この警告をテストするには、次のマクロ **HR_FAILED** します。</span><span class="sxs-lookup"><span data-stu-id="162fc-120">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="162fc-121">詳細については、「Using [Macros for Error Handling 」を参照してください](using-macros-for-error-handling.md)。</span><span class="sxs-lookup"><span data-stu-id="162fc-121">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="162fc-122">注釈</span><span class="sxs-lookup"><span data-stu-id="162fc-122">Remarks</span></span>

<span data-ttu-id="162fc-123">**IMAPISupport::OpenAddressBook** メソッドは、すべてのサービス プロバイダー サポート オブジェクトに実装されます。</span><span class="sxs-lookup"><span data-stu-id="162fc-123">The **IMAPISupport::OpenAddressBook** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="162fc-124">サービス プロバイダー (通常は緊密に結合されたメッセージ ストアとトランスポート プロバイダー) は、アドレス帳へのアクセスを取得するために **OpenAddressBook** を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="162fc-124">Service providers, typically tightly coupled message store and transport providers, call **OpenAddressBook** to get access to the address book.</span></span> <span data-ttu-id="162fc-125">返される **IAddrBook** ポインターは、アドレス帳コンテナーの開き方、メッセージング ユーザーの検索、アドレスダイアログ ボックスの表示など、さまざまなアドレス帳タスクに使用できます。</span><span class="sxs-lookup"><span data-stu-id="162fc-125">The returned **IAddrBook** pointer can be used for a variety of address book tasks, including opening address book containers, finding messaging users, and displaying address dialog boxes.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="162fc-126">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="162fc-126">Notes to callers</span></span>

 <span data-ttu-id="162fc-127">**OpenAddressBook** は、現在MAPI_W_ERRORS_RETURNED 1 つ以上のアドレス帳プロバイダーを読み込めない場合に、そのアドレス帳を返します。</span><span class="sxs-lookup"><span data-stu-id="162fc-127">**OpenAddressBook** can return MAPI_W_ERRORS_RETURNED if it cannot load one or more of the address book providers in the current profile.</span></span> <span data-ttu-id="162fc-128">この値は警告であり、呼び出しは成功として扱う必要があります。</span><span class="sxs-lookup"><span data-stu-id="162fc-128">This value is a warning and you should treat the call as successful.</span></span> <span data-ttu-id="162fc-129">すべてのアドレス帳プロバイダーが読み込めなくても **、OpenAddressBook** は引き続き成功し _、lppAdrBook_ パラメーターに MAPI_W_ERRORS_RETURNED と **IAddrBook** ポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="162fc-129">Even if all of the address book providers failed to load, **OpenAddressBook** still succeeds, returning MAPI_W_ERRORS_RETURNED and an **IAddrBook** pointer in the  _lppAdrBook_ parameter.</span></span> <span data-ttu-id="162fc-130">**OpenAddressBook は** 常に有効な **IAddrBook** ポインターを返すので、使用が終了したら解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="162fc-130">Because **OpenAddressBook** always returns a valid **IAddrBook** pointer, you must release it when you are finished using it.</span></span> 
  
<span data-ttu-id="162fc-131">1 つ以上のアドレス帳プロバイダーの読み込みに失敗した場合は [、IMAPISupport::GetLastError](imapisupport-getlasterror.md) を呼び出して、読み込みなかったプロバイダーに関する情報を含む [MAPIERROR](mapierror.md) 構造を取得します。</span><span class="sxs-lookup"><span data-stu-id="162fc-131">If one or more address book providers failed to load, call [IMAPISupport::GetLastError](imapisupport-getlasterror.md) to obtain a [MAPIERROR](mapierror.md) structure that contains information about the providers that did not load.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="162fc-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="162fc-132">See also</span></span>



[<span data-ttu-id="162fc-133">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="162fc-133">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)
  
[<span data-ttu-id="162fc-134">IMAPISession::OpenAddressBook</span><span class="sxs-lookup"><span data-stu-id="162fc-134">IMAPISession::OpenAddressBook</span></span>](imapisession-openaddressbook.md)
  
[<span data-ttu-id="162fc-135">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="162fc-135">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

