---
title: IMAPISupportCreateOneOff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.CreateOneOff
api_type:
- COM
ms.assetid: ee57d6e0-9de0-4427-97ce-371c1c01f3de
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 9571d51e01c2d58d9b8a9a913ba2c210ae0bd44d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411996"
---
# <a name="imapisupportcreateoneoff"></a><span data-ttu-id="2ced7-103">IMAPISupport::CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="2ced7-103">IMAPISupport::CreateOneOff</span></span>

  
  
<span data-ttu-id="2ced7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2ced7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2ced7-105">1 回のアドレスのエントリ識別子を作成します。</span><span class="sxs-lookup"><span data-stu-id="2ced7-105">Creates an entry identifier for a one-off address.</span></span>
  
```cpp
HRESULT CreateOneOff(
  LPSTR lpszName,
  LPSTR lpszAdrType,
  LPSTR lpszAddress,
  ULONG ulFlags,
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="2ced7-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2ced7-106">Parameters</span></span>

 <span data-ttu-id="2ced7-107">_lpszName_</span><span class="sxs-lookup"><span data-stu-id="2ced7-107">_lpszName_</span></span>
  
> <span data-ttu-id="2ced7-108">[in]受信者 [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)**プロパティPR_DISPLAY_NAME表示** 名へのポインター。</span><span class="sxs-lookup"><span data-stu-id="2ced7-108">[in] A pointer to the display name of the recipient the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span> <span data-ttu-id="2ced7-109">_lpszName パラメーター_ には NULL を指定できます。</span><span class="sxs-lookup"><span data-stu-id="2ced7-109">The  _lpszName_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="2ced7-110">_lpszAdrType_</span><span class="sxs-lookup"><span data-stu-id="2ced7-110">_lpszAdrType_</span></span>
  
> <span data-ttu-id="2ced7-111">[in]受信者のアドレスの種類 (FAX、SMTP、X500 など) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="2ced7-111">[in] A pointer to the address type (such as FAX, SMTP, or X500) of the recipient.</span></span> <span data-ttu-id="2ced7-112">_lpszAdrType パラメーター_ を NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="2ced7-112">The  _lpszAdrType_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="2ced7-113">_lpszAddress_</span><span class="sxs-lookup"><span data-stu-id="2ced7-113">_lpszAddress_</span></span>
  
> <span data-ttu-id="2ced7-114">[in]受信者のメッセージング アドレスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="2ced7-114">[in] A pointer to the messaging address of the recipient.</span></span> <span data-ttu-id="2ced7-115">_lpszAddress パラメーター_ は NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="2ced7-115">The  _lpszAddress_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="2ced7-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2ced7-116">_ulFlags_</span></span>
  
> <span data-ttu-id="2ced7-117">[in]1 回の受信者に影響を与えるフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="2ced7-117">[in] A bitmask of flags that affects the one-off recipient.</span></span> <span data-ttu-id="2ced7-118">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="2ced7-118">The following flags can be set:</span></span>
    
<span data-ttu-id="2ced7-119">MAPI_SEND_NO_RICH_INFO</span><span class="sxs-lookup"><span data-stu-id="2ced7-119">MAPI_SEND_NO_RICH_INFO</span></span> 
  
> <span data-ttu-id="2ced7-120">受信者は、書式設定されたメッセージ コンテンツを処理できません。</span><span class="sxs-lookup"><span data-stu-id="2ced7-120">The recipient cannot handle formatted message content.</span></span> <span data-ttu-id="2ced7-121">このMAPI_SEND_NO_RICH_INFO設定されている場合、MAPI は受信者のPR_SEND_RICH_INFO **(** [PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) プロパティを FALSE に設定します。</span><span class="sxs-lookup"><span data-stu-id="2ced7-121">If MAPI_SEND_NO_RICH_INFO is set, MAPI sets the recipient's **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) property to FALSE.</span></span> <span data-ttu-id="2ced7-122">このMAPI_SEND_NO_RICH_INFO設定されていない場合  _、LPszAddress_ が指す受信者のメッセージング アドレスがインターネット アドレスと解釈されない限り、MAPI はこのプロパティを TRUE に設定します。</span><span class="sxs-lookup"><span data-stu-id="2ced7-122">If MAPI_SEND_NO_RICH_INFO is not set, MAPI sets this property to TRUE unless the recipient's messaging address pointed to by  _lpszAddress_ is interpreted to be an Internet address.</span></span> <span data-ttu-id="2ced7-123">この場合、MAPI は、この値 **PR_SEND_RICH_INFO** FALSE に設定します。</span><span class="sxs-lookup"><span data-stu-id="2ced7-123">In this case, MAPI sets **PR_SEND_RICH_INFO** to FALSE.</span></span> 
    
<span data-ttu-id="2ced7-124">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2ced7-124">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="2ced7-125">表示名、アドレスの種類、およびアドレスは Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="2ced7-125">The display name, address type, and address are in Unicode format.</span></span> <span data-ttu-id="2ced7-126">このフラグMAPI_UNICODE設定されていない場合、これらの文字列は ANSI 形式です。</span><span class="sxs-lookup"><span data-stu-id="2ced7-126">If the MAPI_UNICODE flag is not set, these strings are in ANSI format.</span></span>
    
 <span data-ttu-id="2ced7-127">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="2ced7-127">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="2ced7-128">[out]  _lppEntryID_ パラメーターが指すエントリ識別子内のバイト数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="2ced7-128">[out] A pointer to the count of bytes in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="2ced7-129">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="2ced7-129">_lppEntryID_</span></span>
  
> <span data-ttu-id="2ced7-130">[out]1 回の受信者のエントリ識別子へのポインターを指すポインター。</span><span class="sxs-lookup"><span data-stu-id="2ced7-130">[out] A pointer to a pointer to the entry identifier for the one-off recipient.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2ced7-131">戻り値</span><span class="sxs-lookup"><span data-stu-id="2ced7-131">Return value</span></span>

<span data-ttu-id="2ced7-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="2ced7-132">S_OK</span></span> 
  
> <span data-ttu-id="2ced7-133">1 回のエントリ識別子が正常に作成されました。</span><span class="sxs-lookup"><span data-stu-id="2ced7-133">The one-off entry identifier was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2ced7-134">注釈</span><span class="sxs-lookup"><span data-stu-id="2ced7-134">Remarks</span></span>

<span data-ttu-id="2ced7-135">**IMAPISupport::CreateOneOff** メソッドは、すべてのサービス プロバイダー サポート オブジェクトに実装されます。</span><span class="sxs-lookup"><span data-stu-id="2ced7-135">The **IMAPISupport::CreateOneOff** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="2ced7-136">サービス プロバイダーは **CreateOneOff** を呼び出して、1 回の受信者 (現在読み込まれているアドレス帳プロバイダーのコンテナーに属していない受信者) のエントリ識別子を作成します。</span><span class="sxs-lookup"><span data-stu-id="2ced7-136">Service providers call **CreateOneOff** to create an entry identifier for a one-off recipient (a recipient that does not belong to any of the containers from any of the currently loaded address book providers).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="2ced7-137">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="2ced7-137">Notes to callers</span></span>

<span data-ttu-id="2ced7-138">**CreateOneOff** によって返されるエントリ識別子の使用が完了したら [、MAPIFreeBuffer](mapifreebuffer.md)関数を使用してエントリ識別子に割り当てられたメモリを解放します。</span><span class="sxs-lookup"><span data-stu-id="2ced7-138">When you are finished using the entry identifier returned by **CreateOneOff**, free the memory allocated for the entry identifier by using the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="notes-to-transport-providers"></a><span data-ttu-id="2ced7-139">トランスポート プロバイダーへのメモ</span><span class="sxs-lookup"><span data-stu-id="2ced7-139">Notes to Transport Providers</span></span>

<span data-ttu-id="2ced7-140">トランスポート ニュートラル カプセル化形式 (TNEF) をサポートし **、PR_SEND_RICH_INFO** プロパティの値を使用して、メッセージを転送するときに TNEF を使用するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="2ced7-140">Support the Transport Neutral Encapsulation Format (TNEF) and use the value of the **PR_SEND_RICH_INFO** property to determine whether to use TNEF when you transport a message.</span></span> <span data-ttu-id="2ced7-141">TNEF をサポートしていない、または要求された場合にこの形式でメッセージを送信しない場合は、カスタム MAPI プロパティを必要とするフォーム ベースのクライアントまたはクライアントに問題が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="2ced7-141">Not supporting TNEF or not sending a message in this format when it is requested can be a problem for form-based clients or clients that require custom MAPI properties.</span></span> <span data-ttu-id="2ced7-142">これは、TNEF は通常、カスタム メッセージ クラスのカスタム プロパティを送信するために使用されるためです。</span><span class="sxs-lookup"><span data-stu-id="2ced7-142">This is because TNEF is typically used to send custom properties for custom message classes.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2ced7-143">関連項目</span><span class="sxs-lookup"><span data-stu-id="2ced7-143">See also</span></span>



[<span data-ttu-id="2ced7-144">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="2ced7-144">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="2ced7-145">PidTagDisplayName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2ced7-145">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)
  
[<span data-ttu-id="2ced7-146">PidTagSendRichInfo 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2ced7-146">PidTagSendRichInfo Canonical Property</span></span>](pidtagsendrichinfo-canonical-property.md)
  
[<span data-ttu-id="2ced7-147">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="2ced7-147">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

