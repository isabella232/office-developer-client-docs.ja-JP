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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 1cfd4afbda5892e96a1d74ca56f4a6d1f98e2268
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800720"
---
# <a name="imapisupportcreateoneoff"></a><span data-ttu-id="a44c3-103">IMAPISupport::CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="a44c3-103">IMAPISupport::CreateOneOff</span></span>

  
  
<span data-ttu-id="a44c3-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a44c3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a44c3-105">一時アドレスのエントリ id を作成します。</span><span class="sxs-lookup"><span data-stu-id="a44c3-105">Creates an entry identifier for a one-off address.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="a44c3-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a44c3-106">Parameters</span></span>

 <span data-ttu-id="a44c3-107">_lpszName_</span><span class="sxs-lookup"><span data-stu-id="a44c3-107">_lpszName_</span></span>
  
> <span data-ttu-id="a44c3-108">[in]**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) は、受信者の表示名へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a44c3-108">[in] A pointer to the display name of the recipient the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span> <span data-ttu-id="a44c3-109">_LpszName_パラメーターは、NULL にすることができます。</span><span class="sxs-lookup"><span data-stu-id="a44c3-109">The  _lpszName_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="a44c3-110">_lpszAdrType_</span><span class="sxs-lookup"><span data-stu-id="a44c3-110">_lpszAdrType_</span></span>
  
> <span data-ttu-id="a44c3-111">[in]受信者のアドレスの種類 (FAX、SMTP、X500 など) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a44c3-111">[in] A pointer to the address type (such as FAX, SMTP, or X500) of the recipient.</span></span> <span data-ttu-id="a44c3-112">_LpszAdrType_パラメーターは、NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="a44c3-112">The  _lpszAdrType_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="a44c3-113">_lpszAddress_</span><span class="sxs-lookup"><span data-stu-id="a44c3-113">_lpszAddress_</span></span>
  
> <span data-ttu-id="a44c3-114">[in]受信者のメッセージのアドレスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="a44c3-114">[in] A pointer to the messaging address of the recipient.</span></span> <span data-ttu-id="a44c3-115">_LpszAddress_パラメーターは、NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="a44c3-115">The  _lpszAddress_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="a44c3-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a44c3-116">_ulFlags_</span></span>
  
> <span data-ttu-id="a44c3-117">[in]1 回限りの受信者に影響を与えるフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="a44c3-117">[in] A bitmask of flags that affects the one-off recipient.</span></span> <span data-ttu-id="a44c3-118">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="a44c3-118">The following flags can be set:</span></span>
    
<span data-ttu-id="a44c3-119">MAPI_SEND_NO_RICH_INFO</span><span class="sxs-lookup"><span data-stu-id="a44c3-119">MAPI_SEND_NO_RICH_INFO</span></span> 
  
> <span data-ttu-id="a44c3-120">受信者には、コンテンツの書式設定されたメッセージを処理できません。</span><span class="sxs-lookup"><span data-stu-id="a44c3-120">The recipient cannot handle formatted message content.</span></span> <span data-ttu-id="a44c3-121">MAPI_SEND_NO_RICH_INFO を設定すると、MAPI では受信者の**PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) のプロパティを FALSE に設定します。</span><span class="sxs-lookup"><span data-stu-id="a44c3-121">If MAPI_SEND_NO_RICH_INFO is set, MAPI sets the recipient's **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) property to FALSE.</span></span> <span data-ttu-id="a44c3-122">MAPI_SEND_NO_RICH_INFO が設定されていない場合は、MAPI は_lpszAddress_で指定された受信者のメッセージのアドレスがインターネット アドレスを解釈しない限り、TRUE にこのプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="a44c3-122">If MAPI_SEND_NO_RICH_INFO is not set, MAPI sets this property to TRUE unless the recipient's messaging address pointed to by  _lpszAddress_ is interpreted to be an Internet address.</span></span> <span data-ttu-id="a44c3-123">この例では、MAPI は、 **PR_SEND_RICH_INFO**を FALSE に設定します。</span><span class="sxs-lookup"><span data-stu-id="a44c3-123">In this case, MAPI sets **PR_SEND_RICH_INFO** to FALSE.</span></span> 
    
<span data-ttu-id="a44c3-124">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a44c3-124">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="a44c3-125">表示名、アドレスの種類、およびアドレスは、Unicode 形式では。</span><span class="sxs-lookup"><span data-stu-id="a44c3-125">The display name, address type, and address are in Unicode format.</span></span> <span data-ttu-id="a44c3-126">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式でこれらの文字列です。</span><span class="sxs-lookup"><span data-stu-id="a44c3-126">If the MAPI_UNICODE flag is not set, these strings are in ANSI format.</span></span>
    
 <span data-ttu-id="a44c3-127">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="a44c3-127">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="a44c3-128">[out]_LppEntryID_パラメーターで指定されたエントリの識別子のバイト数のカウントへのポインター。</span><span class="sxs-lookup"><span data-stu-id="a44c3-128">[out] A pointer to the count of bytes in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="a44c3-129">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="a44c3-129">_lppEntryID_</span></span>
  
> <span data-ttu-id="a44c3-130">[out]1 回限りの受信者のエントリの識別子へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="a44c3-130">[out] A pointer to a pointer to the entry identifier for the one-off recipient.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a44c3-131">�߂�l</span><span class="sxs-lookup"><span data-stu-id="a44c3-131">Return value</span></span>

<span data-ttu-id="a44c3-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="a44c3-132">S_OK</span></span> 
  
> <span data-ttu-id="a44c3-133">一時エントリ id が正常に作成されました。</span><span class="sxs-lookup"><span data-stu-id="a44c3-133">The one-off entry identifier was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a44c3-134">注釈</span><span class="sxs-lookup"><span data-stu-id="a44c3-134">Remarks</span></span>

<span data-ttu-id="a44c3-135">サービス プロバイダーのサポートのすべてのオブジェクトの**IMAPISupport::CreateOneOff**メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="a44c3-135">The **IMAPISupport::CreateOneOff** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="a44c3-136">サービス プロバイダーでは、一時受信者 (現在ロードされているアドレス帳プロバイダーのいずれかから任意のコンテナーに属していない受信者) のエントリ id を作成するのには**CreateOneOff**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a44c3-136">Service providers call **CreateOneOff** to create an entry identifier for a one-off recipient (a recipient that does not belong to any of the containers from any of the currently loaded address book providers).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a44c3-137">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="a44c3-137">Notes to callers</span></span>

<span data-ttu-id="a44c3-138">**CreateOneOff**によって返されるエントリの識別子を使用してが完了したら、 [MAPIFreeBuffer](mapifreebuffer.md)関数を使用してエントリの識別子の割り当てられたメモリを解放します。</span><span class="sxs-lookup"><span data-stu-id="a44c3-138">When you are finished using the entry identifier returned by **CreateOneOff**, free the memory allocated for the entry identifier by using the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="notes-to-transport-providers"></a><span data-ttu-id="a44c3-139">トランスポート プロバイダーへのメモ</span><span class="sxs-lookup"><span data-stu-id="a44c3-139">Notes to Transport Providers</span></span>

<span data-ttu-id="a44c3-140">トランスポート ニュートラル カプセル化形式 (TNEF) をサポートし、 **PR_SEND_RICH_INFO**プロパティの値を使用して、メッセージを転送する場合は、TNEF を使用するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="a44c3-140">Support the Transport Neutral Encapsulation Format (TNEF) and use the value of the **PR_SEND_RICH_INFO** property to determine whether to use TNEF when you transport a message.</span></span> <span data-ttu-id="a44c3-141">TNEF をサポートしていないまたはしないメッセージを送信する次の形式で要求されたときに、フォーム ベースのクライアントまたはユーザー設定の MAPI プロパティを必要とするクライアントの問題がある場合ができます。</span><span class="sxs-lookup"><span data-stu-id="a44c3-141">Not supporting TNEF or not sending a message in this format when it is requested can be a problem for form-based clients or clients that require custom MAPI properties.</span></span> <span data-ttu-id="a44c3-142">TNEF は、通常、送信するカスタム メッセージ クラス用のカスタム プロパティに使用するためです。</span><span class="sxs-lookup"><span data-stu-id="a44c3-142">This is because TNEF is typically used to send custom properties for custom message classes.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a44c3-143">関連項目</span><span class="sxs-lookup"><span data-stu-id="a44c3-143">See also</span></span>



[<span data-ttu-id="a44c3-144">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="a44c3-144">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="a44c3-145">PidTagDisplayName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a44c3-145">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)
  
[<span data-ttu-id="a44c3-146">PidTagSendRichInfo 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a44c3-146">PidTagSendRichInfo Canonical Property</span></span>](pidtagsendrichinfo-canonical-property.md)
  
[<span data-ttu-id="a44c3-147">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="a44c3-147">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

