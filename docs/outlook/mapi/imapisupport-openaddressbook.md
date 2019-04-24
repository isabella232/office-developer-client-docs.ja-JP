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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329030"
---
# <a name="imapisupportopenaddressbook"></a><span data-ttu-id="04eb7-103">IMAPISupport::OpenAddressBook</span><span class="sxs-lookup"><span data-stu-id="04eb7-103">IMAPISupport::OpenAddressBook</span></span>

  
  
<span data-ttu-id="04eb7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="04eb7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="04eb7-105">アドレス帳へのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="04eb7-105">Provides access to the address book.</span></span>
  
```cpp
HRESULT OpenAddressBook(
LPCIID lpInterface,
ULONG ulFlags,
LPADRBOOK FAR * lppAdrBook
);
```

## <a name="parameters"></a><span data-ttu-id="04eb7-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="04eb7-106">Parameters</span></span>

 <span data-ttu-id="04eb7-107">_lpinterface_</span><span class="sxs-lookup"><span data-stu-id="04eb7-107">_lpInterface_</span></span>
  
> <span data-ttu-id="04eb7-108">順番アドレス帳へのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="04eb7-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the address book.</span></span> <span data-ttu-id="04eb7-109">有効な値は NULL で、標準のアドレス帳インターフェイス[IAddrBook](iaddrbookimapiprop.md)および IID_IAddrBook を示します。</span><span class="sxs-lookup"><span data-stu-id="04eb7-109">Valid values are NULL, which indicates the standard address book interface [IAddrBook](iaddrbookimapiprop.md), and IID_IAddrBook.</span></span>
    
 <span data-ttu-id="04eb7-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="04eb7-110">_ulFlags_</span></span>
  
> <span data-ttu-id="04eb7-111">予約語0である必要があります。</span><span class="sxs-lookup"><span data-stu-id="04eb7-111">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="04eb7-112">_lppadrbook_</span><span class="sxs-lookup"><span data-stu-id="04eb7-112">_lppAdrBook_</span></span>
  
> <span data-ttu-id="04eb7-113">読み上げアドレス帳へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="04eb7-113">[out] A pointer to a pointer to the address book.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="04eb7-114">戻り値</span><span class="sxs-lookup"><span data-stu-id="04eb7-114">Return value</span></span>

<span data-ttu-id="04eb7-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="04eb7-115">S_OK</span></span> 
  
> <span data-ttu-id="04eb7-116">アドレス帳へのアクセスが提供されました。</span><span class="sxs-lookup"><span data-stu-id="04eb7-116">Access to the address book was provided.</span></span>
    
<span data-ttu-id="04eb7-117">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="04eb7-117">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="04eb7-118">呼び出しは成功しましたが、1つ以上のアドレス帳プロバイダーを読み込めませんでした。</span><span class="sxs-lookup"><span data-stu-id="04eb7-118">The call succeeded, but one or more address book providers could not be loaded.</span></span> <span data-ttu-id="04eb7-119">この警告が返された場合、呼び出しは正常に処理されます。</span><span class="sxs-lookup"><span data-stu-id="04eb7-119">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="04eb7-120">この警告をテストするには、 **HR_FAILED**マクロを使用します。</span><span class="sxs-lookup"><span data-stu-id="04eb7-120">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="04eb7-121">詳細については、「[エラー処理にマクロを使用する](using-macros-for-error-handling.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="04eb7-121">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="04eb7-122">解説</span><span class="sxs-lookup"><span data-stu-id="04eb7-122">Remarks</span></span>

<span data-ttu-id="04eb7-123">**imapisupport:: OpenAddressBook**メソッドは、すべてのサービスプロバイダーサポートオブジェクトに実装されています。</span><span class="sxs-lookup"><span data-stu-id="04eb7-123">The **IMAPISupport::OpenAddressBook** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="04eb7-124">サービスプロバイダは通常、メッセージストアとトランスポートプロバイダーを密結合し、 **OpenAddressBook**を呼び出してアドレス帳へのアクセス権を取得します。</span><span class="sxs-lookup"><span data-stu-id="04eb7-124">Service providers, typically tightly coupled message store and transport providers, call **OpenAddressBook** to get access to the address book.</span></span> <span data-ttu-id="04eb7-125">返される**IAddrBook**ポインターは、アドレス帳コンテナーを開く、メッセージングユーザーを検索する、アドレスダイアログボックスを表示するなど、さまざまなアドレス帳タスクに使用できます。</span><span class="sxs-lookup"><span data-stu-id="04eb7-125">The returned **IAddrBook** pointer can be used for a variety of address book tasks, including opening address book containers, finding messaging users, and displaying address dialog boxes.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="04eb7-126">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="04eb7-126">Notes to callers</span></span>

 <span data-ttu-id="04eb7-127">**OpenAddressBook**は、現在のプロファイルにアドレス帳プロバイダーの1つ以上を読み込むことができない場合、MAPI_W_ERRORS_RETURNED を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="04eb7-127">**OpenAddressBook** can return MAPI_W_ERRORS_RETURNED if it cannot load one or more of the address book providers in the current profile.</span></span> <span data-ttu-id="04eb7-128">この値は警告で、呼び出しを成功として扱う必要があります。</span><span class="sxs-lookup"><span data-stu-id="04eb7-128">This value is a warning and you should treat the call as successful.</span></span> <span data-ttu-id="04eb7-129">すべてのアドレス帳プロバイダーが読み込まれなかった場合でも、 **OpenAddressBook**は成功し、 _lppadrbook_パラメーターで MAPI_W_ERRORS_RETURNED と**IAddrBook**ポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="04eb7-129">Even if all of the address book providers failed to load, **OpenAddressBook** still succeeds, returning MAPI_W_ERRORS_RETURNED and an **IAddrBook** pointer in the  _lppAdrBook_ parameter.</span></span> <span data-ttu-id="04eb7-130">**OpenAddressBook**は常に有効な**IAddrBook**ポインターを返すため、これを使用し終えたら解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="04eb7-130">Because **OpenAddressBook** always returns a valid **IAddrBook** pointer, you must release it when you are finished using it.</span></span> 
  
<span data-ttu-id="04eb7-131">1つ以上のアドレス帳プロバイダーが読み込みに失敗した場合は、 [imapisupport:: GetLastError](imapisupport-getlasterror.md)を呼び出して、読み込まれていないプロバイダーに関する情報を含む[MAPIERROR](mapierror.md)構造を取得します。</span><span class="sxs-lookup"><span data-stu-id="04eb7-131">If one or more address book providers failed to load, call [IMAPISupport::GetLastError](imapisupport-getlasterror.md) to obtain a [MAPIERROR](mapierror.md) structure that contains information about the providers that did not load.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="04eb7-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="04eb7-132">See also</span></span>



[<span data-ttu-id="04eb7-133">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="04eb7-133">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)
  
[<span data-ttu-id="04eb7-134">IMAPISession::OpenAddressBook</span><span class="sxs-lookup"><span data-stu-id="04eb7-134">IMAPISession::OpenAddressBook</span></span>](imapisession-openaddressbook.md)
  
[<span data-ttu-id="04eb7-135">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="04eb7-135">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

