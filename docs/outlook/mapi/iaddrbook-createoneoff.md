---
title: iaddrbookcreateoneoff
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.CreateOneOff
api_type:
- COM
ms.assetid: bcacfbdf-edff-4810-a985-e6d2c9271901
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 980ac82c6f7fcb5771a6013b3fb033b0bdfd05e0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427382"
---
# <a name="iaddrbookcreateoneoff"></a><span data-ttu-id="ca17a-103">IAddrBook::CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="ca17a-103">IAddrBook::CreateOneOff</span></span>

  
  
<span data-ttu-id="ca17a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ca17a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ca17a-105">1回限りのアドレスのエントリ id を作成します。</span><span class="sxs-lookup"><span data-stu-id="ca17a-105">Creates an entry identifier for a one-off address.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="ca17a-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ca17a-106">Parameters</span></span>

 <span data-ttu-id="ca17a-107">_lpszname_</span><span class="sxs-lookup"><span data-stu-id="ca17a-107">_lpszName_</span></span>
  
> <span data-ttu-id="ca17a-108">順番受信者の**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティの値へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ca17a-108">[in] A pointer to the value of the recipient's **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span> <span data-ttu-id="ca17a-109">_lpszname_パラメーターには NULL を指定できます。</span><span class="sxs-lookup"><span data-stu-id="ca17a-109">The  _lpszName_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="ca17a-110">_lpszadrtype_</span><span class="sxs-lookup"><span data-stu-id="ca17a-110">_lpszAdrType_</span></span>
  
> <span data-ttu-id="ca17a-111">順番FAX、SMTP などの受信者のアドレスの種類へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ca17a-111">[in] A pointer to the address type of the recipient, such as FAX or SMTP.</span></span> <span data-ttu-id="ca17a-112">_lpszadrtype_パラメーターを NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="ca17a-112">The  _lpszAdrType_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="ca17a-113">_lpszaddress_</span><span class="sxs-lookup"><span data-stu-id="ca17a-113">_lpszAddress_</span></span>
  
> <span data-ttu-id="ca17a-114">順番受信者のアドレスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="ca17a-114">[in] A pointer to the address of the recipient.</span></span> <span data-ttu-id="ca17a-115">_lpszaddress_パラメーターを NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="ca17a-115">The  _lpszAddress_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="ca17a-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ca17a-116">_ulFlags_</span></span>
  
> <span data-ttu-id="ca17a-117">順番1回限りの受信者に影響を与えるフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="ca17a-117">[in] A bitmask of flags that affects the one-off recipient.</span></span> <span data-ttu-id="ca17a-118">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="ca17a-118">The following flags can be set:</span></span>
    
<span data-ttu-id="ca17a-119">MAPI_SEND_NO_RICH_INFO</span><span class="sxs-lookup"><span data-stu-id="ca17a-119">MAPI_SEND_NO_RICH_INFO</span></span> 
  
> <span data-ttu-id="ca17a-120">受信者は、書式設定されたメッセージコンテンツを処理できません。</span><span class="sxs-lookup"><span data-stu-id="ca17a-120">The recipient cannot handle formatted message content.</span></span> <span data-ttu-id="ca17a-121">MAPI_SEND_NO_RICH_INFO が設定されている場合、MAPI は受信者の**PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) プロパティを FALSE に設定します。</span><span class="sxs-lookup"><span data-stu-id="ca17a-121">If MAPI_SEND_NO_RICH_INFO is set, MAPI sets the recipient's **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) property to FALSE.</span></span> <span data-ttu-id="ca17a-122">MAPI_SEND_NO_RICH_INFO が設定されていない場合、MAPI は、 _lpszaddress_が指す受信者のメッセージアドレスがインターネットアドレスであると解釈されない限り、このプロパティを TRUE に設定します。</span><span class="sxs-lookup"><span data-stu-id="ca17a-122">If MAPI_SEND_NO_RICH_INFO is not set, MAPI sets this property to TRUE unless the recipient's messaging address pointed to by  _lpszAddress_ is interpreted to be an Internet address.</span></span> <span data-ttu-id="ca17a-123">この場合、MAPI は**PR_SEND_RICH_INFO**を FALSE に設定します。</span><span class="sxs-lookup"><span data-stu-id="ca17a-123">In this case, MAPI sets **PR_SEND_RICH_INFO** to FALSE.</span></span> 
    
<span data-ttu-id="ca17a-124">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ca17a-124">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="ca17a-125">表示名、アドレスの種類、アドレスは、Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="ca17a-125">The display name, address type, and address are in Unicode format.</span></span> <span data-ttu-id="ca17a-126">MAPI_UNICODE フラグが設定されていない場合、これらの文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="ca17a-126">If the MAPI_UNICODE flag is not set, these strings are in ANSI format.</span></span>
    
 <span data-ttu-id="ca17a-127">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="ca17a-127">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="ca17a-128">読み上げ_lppentryid_パラメーターによって指定されたエントリ識別子のバイト数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ca17a-128">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="ca17a-129">_lppentryid_</span><span class="sxs-lookup"><span data-stu-id="ca17a-129">_lppEntryID_</span></span>
  
> <span data-ttu-id="ca17a-130">読み上げ1回限りの受信者のエントリ識別子へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="ca17a-130">[out] A pointer to a pointer to the entry identifier for the one-off recipient.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ca17a-131">戻り値</span><span class="sxs-lookup"><span data-stu-id="ca17a-131">Return value</span></span>

<span data-ttu-id="ca17a-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="ca17a-132">S_OK</span></span> 
  
> <span data-ttu-id="ca17a-133">1回限りのエントリ識別子が正常に作成されました。</span><span class="sxs-lookup"><span data-stu-id="ca17a-133">The one-off entry identifier was created successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ca17a-134">注釈</span><span class="sxs-lookup"><span data-stu-id="ca17a-134">Remarks</span></span>

<span data-ttu-id="ca17a-135">クライアントは**createoneoff**メソッドを呼び出して、1回限りの受信者 (現在読み込まれているアドレス帳プロバイダーのいずれかのコンテナーに属さない受信者) のエントリ id を作成します。</span><span class="sxs-lookup"><span data-stu-id="ca17a-135">Clients call the **CreateOneOff** method to create an entry identifier for a one-off recipient — a recipient that does not belong to any of the containers from any of the currently loaded address book providers.</span></span> <span data-ttu-id="ca17a-136">1回限りの受信者は、セッションの active アドレス帳プロバイダーの1つでサポートされている任意の種類のアドレスを持つことができます。</span><span class="sxs-lookup"><span data-stu-id="ca17a-136">One-off recipients can have any kind of address that is supported by one of the active address book providers for the session.</span></span> 
  
<span data-ttu-id="ca17a-137">通常、1回限りの受信者は、特定のアドレスの種類に対応したテンプレートを使用して作成されます。</span><span class="sxs-lookup"><span data-stu-id="ca17a-137">One-off recipients are typically created with a template for their particular address type.</span></span> <span data-ttu-id="ca17a-138">アドレスの種類をサポートするアドレス帳プロバイダーがテンプレートを提供します。</span><span class="sxs-lookup"><span data-stu-id="ca17a-138">The address book provider that supports the address type supplies the template.</span></span> <span data-ttu-id="ca17a-139">クライアントアプリケーションのユーザーが、テンプレートに関連情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="ca17a-139">A user of a client application enters the relevant information into the template.</span></span>
  
<span data-ttu-id="ca17a-140">MAPI では、表示名、アドレスの種類、および**createoneoff**のアドレスパラメーターに対して Unicode 文字列をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="ca17a-140">MAPI supports Unicode character strings for the display name, address type, and address parameters of **CreateOneOff**.</span></span>
  
<span data-ttu-id="ca17a-141">MAPI_SEND_NO_RICH_INFO フラグは、リッチテキスト形式 (RTF) の書式付きテキストを各メッセージと共に送信するかどうかを制御します。</span><span class="sxs-lookup"><span data-stu-id="ca17a-141">The MAPI_SEND_NO_RICH_INFO flag controls whether formatted text in Rich Text Format (RTF) is sent along with each message.</span></span> <span data-ttu-id="ca17a-142">トランスポートニュートラルカプセル化形式 (TNEF) (書式付きテキストの送信に使用される形式) は、受信者が**PR_SEND_RICH_INFO**プロパティを設定する方法に関係なく、ほとんどのトランスポートプロバイダーによって送信されます。</span><span class="sxs-lookup"><span data-stu-id="ca17a-142">The Transport Neutral Encapsulation Format (TNEF) — a format that is used for transmitting formatted text — is sent by most transport providers, regardless of how the recipient sets its **PR_SEND_RICH_INFO** property.</span></span> <span data-ttu-id="ca17a-143">これは、個人間メッセージを処理するメッセージングクライアントにとっては問題ではありません。</span><span class="sxs-lookup"><span data-stu-id="ca17a-143">This is not an issue for messaging clients that work with interpersonal messages.</span></span> <span data-ttu-id="ca17a-144">ただし、TNEF は通常、カスタムメッセージクラスのカスタムプロパティを送信するために使用されるため、サポートしていません。これは、フォームベースのクライアントまたはカスタム MAPI プロパティを必要とするクライアントにとって問題になる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ca17a-144">However, because TNEF is typically used to send custom properties for custom message classes, not supporting it can be a problem for form-based clients or clients that require custom MAPI properties.</span></span> <span data-ttu-id="ca17a-145">詳細については、「 [TNEF を使用](sending-messages-with-tnef.md)してメッセージを送信する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ca17a-145">For more information, see [Sending Messages with TNEF](sending-messages-with-tnef.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ca17a-146">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="ca17a-146">MFCMAPI reference</span></span>

<span data-ttu-id="ca17a-147">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ca17a-147">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ca17a-148">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="ca17a-148">**File**</span></span>|<span data-ttu-id="ca17a-149">**関数**</span><span class="sxs-lookup"><span data-stu-id="ca17a-149">**Function**</span></span>|<span data-ttu-id="ca17a-150">**コメント**</span><span class="sxs-lookup"><span data-stu-id="ca17a-150">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ca17a-151">Mapiabfunctions</span><span class="sxs-lookup"><span data-stu-id="ca17a-151">Mapiabfunctions.cpp</span></span>  <br/> |<span data-ttu-id="ca17a-152">addoneoffaddress</span><span class="sxs-lookup"><span data-stu-id="ca17a-152">AddOneOffAddress</span></span>  <br/> |<span data-ttu-id="ca17a-153">mfcmapi は、 **createoneoff**メソッドを使用して、アドレス帳に存在しないアドレスのエントリ ID を作成します。</span><span class="sxs-lookup"><span data-stu-id="ca17a-153">MFCMAPI uses the **CreateOneOff** method to create an entry ID for an address that is not found in any address book.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ca17a-154">関連項目</span><span class="sxs-lookup"><span data-stu-id="ca17a-154">See also</span></span>



[<span data-ttu-id="ca17a-155">IMAPISupport::CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="ca17a-155">IMAPISupport::CreateOneOff</span></span>](imapisupport-createoneoff.md)
  
[<span data-ttu-id="ca17a-156">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="ca17a-156">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


<span data-ttu-id="ca17a-157">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="ca17a-157">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

