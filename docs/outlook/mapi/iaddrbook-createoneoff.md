---
title: IAddrBookCreateOneOff
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
# <a name="iaddrbookcreateoneoff"></a><span data-ttu-id="09b3f-103">IAddrBook::CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="09b3f-103">IAddrBook::CreateOneOff</span></span>

  
  
<span data-ttu-id="09b3f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="09b3f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="09b3f-105">1 回のアドレスのエントリ識別子を作成します。</span><span class="sxs-lookup"><span data-stu-id="09b3f-105">Creates an entry identifier for a one-off address.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="09b3f-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="09b3f-106">Parameters</span></span>

 <span data-ttu-id="09b3f-107">_lpszName_</span><span class="sxs-lookup"><span data-stu-id="09b3f-107">_lpszName_</span></span>
  
> <span data-ttu-id="09b3f-108">[in]受信者のプロパティ[(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)プロパティPR_DISPLAY_NAMEへのポインター。 </span><span class="sxs-lookup"><span data-stu-id="09b3f-108">[in] A pointer to the value of the recipient's **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span> <span data-ttu-id="09b3f-109">_lpszName パラメーター_ には NULL を指定できます。</span><span class="sxs-lookup"><span data-stu-id="09b3f-109">The  _lpszName_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="09b3f-110">_lpszAdrType_</span><span class="sxs-lookup"><span data-stu-id="09b3f-110">_lpszAdrType_</span></span>
  
> <span data-ttu-id="09b3f-111">[in]FAX や SMTP などの受信者のアドレスの種類へのポインター。</span><span class="sxs-lookup"><span data-stu-id="09b3f-111">[in] A pointer to the address type of the recipient, such as FAX or SMTP.</span></span> <span data-ttu-id="09b3f-112">_lpszAdrType パラメーター_ を NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="09b3f-112">The  _lpszAdrType_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="09b3f-113">_lpszAddress_</span><span class="sxs-lookup"><span data-stu-id="09b3f-113">_lpszAddress_</span></span>
  
> <span data-ttu-id="09b3f-114">[in]受信者のアドレスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="09b3f-114">[in] A pointer to the address of the recipient.</span></span> <span data-ttu-id="09b3f-115">_lpszAddress パラメーター_ は NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="09b3f-115">The  _lpszAddress_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="09b3f-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="09b3f-116">_ulFlags_</span></span>
  
> <span data-ttu-id="09b3f-117">[in]1 回の受信者に影響を与えるフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="09b3f-117">[in] A bitmask of flags that affects the one-off recipient.</span></span> <span data-ttu-id="09b3f-118">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="09b3f-118">The following flags can be set:</span></span>
    
<span data-ttu-id="09b3f-119">MAPI_SEND_NO_RICH_INFO</span><span class="sxs-lookup"><span data-stu-id="09b3f-119">MAPI_SEND_NO_RICH_INFO</span></span> 
  
> <span data-ttu-id="09b3f-120">受信者は、書式設定されたメッセージ コンテンツを処理できません。</span><span class="sxs-lookup"><span data-stu-id="09b3f-120">The recipient cannot handle formatted message content.</span></span> <span data-ttu-id="09b3f-121">このMAPI_SEND_NO_RICH_INFO設定されている場合、MAPI は受信者のPR_SEND_RICH_INFO **(** [PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) プロパティを FALSE に設定します。</span><span class="sxs-lookup"><span data-stu-id="09b3f-121">If MAPI_SEND_NO_RICH_INFO is set, MAPI sets the recipient's **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) property to FALSE.</span></span> <span data-ttu-id="09b3f-122">このMAPI_SEND_NO_RICH_INFO設定されていない場合  _、LPszAddress_ が指す受信者のメッセージング アドレスがインターネット アドレスと解釈されない限り、MAPI はこのプロパティを TRUE に設定します。</span><span class="sxs-lookup"><span data-stu-id="09b3f-122">If MAPI_SEND_NO_RICH_INFO is not set, MAPI sets this property to TRUE unless the recipient's messaging address pointed to by  _lpszAddress_ is interpreted to be an Internet address.</span></span> <span data-ttu-id="09b3f-123">この場合、MAPI は、この値 **PR_SEND_RICH_INFO** FALSE に設定します。</span><span class="sxs-lookup"><span data-stu-id="09b3f-123">In this case, MAPI sets **PR_SEND_RICH_INFO** to FALSE.</span></span> 
    
<span data-ttu-id="09b3f-124">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="09b3f-124">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="09b3f-125">表示名、アドレスの種類、およびアドレスは Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="09b3f-125">The display name, address type, and address are in Unicode format.</span></span> <span data-ttu-id="09b3f-126">このフラグMAPI_UNICODE設定されていない場合、これらの文字列は ANSI 形式です。</span><span class="sxs-lookup"><span data-stu-id="09b3f-126">If the MAPI_UNICODE flag is not set, these strings are in ANSI format.</span></span>
    
 <span data-ttu-id="09b3f-127">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="09b3f-127">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="09b3f-128">[out]  _lppEntryID_ パラメーターが指すエントリ識別子内のバイト 数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="09b3f-128">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="09b3f-129">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="09b3f-129">_lppEntryID_</span></span>
  
> <span data-ttu-id="09b3f-130">[out]1 回の受信者のエントリ識別子へのポインターを指すポインター。</span><span class="sxs-lookup"><span data-stu-id="09b3f-130">[out] A pointer to a pointer to the entry identifier for the one-off recipient.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="09b3f-131">戻り値</span><span class="sxs-lookup"><span data-stu-id="09b3f-131">Return value</span></span>

<span data-ttu-id="09b3f-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="09b3f-132">S_OK</span></span> 
  
> <span data-ttu-id="09b3f-133">1 回のエントリ識別子が正常に作成されました。</span><span class="sxs-lookup"><span data-stu-id="09b3f-133">The one-off entry identifier was created successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="09b3f-134">注釈</span><span class="sxs-lookup"><span data-stu-id="09b3f-134">Remarks</span></span>

<span data-ttu-id="09b3f-135">クライアントは **CreateOneOff** メソッドを呼び出して、現在読み込まれているアドレス帳プロバイダーのコンテナーに属していない受信者である 1 回の受信者のエントリ識別子を作成します。</span><span class="sxs-lookup"><span data-stu-id="09b3f-135">Clients call the **CreateOneOff** method to create an entry identifier for a one-off recipient — a recipient that does not belong to any of the containers from any of the currently loaded address book providers.</span></span> <span data-ttu-id="09b3f-136">1 回の受信者は、セッションのアクティブなアドレス帳プロバイダーの 1 つでサポートされる任意の種類のアドレスを持つ可能性があります。</span><span class="sxs-lookup"><span data-stu-id="09b3f-136">One-off recipients can have any kind of address that is supported by one of the active address book providers for the session.</span></span> 
  
<span data-ttu-id="09b3f-137">一時受信者は、通常、特定のアドレスの種類のテンプレートを使用して作成されます。</span><span class="sxs-lookup"><span data-stu-id="09b3f-137">One-off recipients are typically created with a template for their particular address type.</span></span> <span data-ttu-id="09b3f-138">アドレスの種類をサポートするアドレス帳プロバイダーは、テンプレートを提供します。</span><span class="sxs-lookup"><span data-stu-id="09b3f-138">The address book provider that supports the address type supplies the template.</span></span> <span data-ttu-id="09b3f-139">クライアント アプリケーションのユーザーは、関連する情報をテンプレートに入力します。</span><span class="sxs-lookup"><span data-stu-id="09b3f-139">A user of a client application enters the relevant information into the template.</span></span>
  
<span data-ttu-id="09b3f-140">MAPI では、CreateOneOff の表示名、アドレスの種類、およびアドレス パラメーターの Unicode 文字 **文字列がサポートされています**。</span><span class="sxs-lookup"><span data-stu-id="09b3f-140">MAPI supports Unicode character strings for the display name, address type, and address parameters of **CreateOneOff**.</span></span>
  
<span data-ttu-id="09b3f-141">[MAPI_SEND_NO_RICH_INFO] フラグは、リッチ テキスト形式 (RTF) の書式設定されたテキストを各メッセージと共に送信するかどうかを制御します。</span><span class="sxs-lookup"><span data-stu-id="09b3f-141">The MAPI_SEND_NO_RICH_INFO flag controls whether formatted text in Rich Text Format (RTF) is sent along with each message.</span></span> <span data-ttu-id="09b3f-142">トランスポート ニュートラル カプセル化形式 (TNEF) (書式設定されたテキストの送信に使用される形式) は、受信者が PR_SEND_RICH_INFO プロパティを設定する方法に関係なく、ほとんどのトランスポート **プロバイダーによって送信** されます。</span><span class="sxs-lookup"><span data-stu-id="09b3f-142">The Transport Neutral Encapsulation Format (TNEF) — a format that is used for transmitting formatted text — is sent by most transport providers, regardless of how the recipient sets its **PR_SEND_RICH_INFO** property.</span></span> <span data-ttu-id="09b3f-143">これは、対人メッセージを処理するメッセージング クライアントの問題ではありません。</span><span class="sxs-lookup"><span data-stu-id="09b3f-143">This is not an issue for messaging clients that work with interpersonal messages.</span></span> <span data-ttu-id="09b3f-144">ただし、TNEF は通常、カスタム メッセージ クラスのカスタム プロパティを送信するために使用するため、サポートしない場合は、カスタム MAPI プロパティを必要とするフォーム ベースのクライアントまたはクライアントに問題が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="09b3f-144">However, because TNEF is typically used to send custom properties for custom message classes, not supporting it can be a problem for form-based clients or clients that require custom MAPI properties.</span></span> <span data-ttu-id="09b3f-145">詳細については [、「TNEF を使用したメッセージの送信」を参照してください](sending-messages-with-tnef.md)。</span><span class="sxs-lookup"><span data-stu-id="09b3f-145">For more information, see [Sending Messages with TNEF](sending-messages-with-tnef.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="09b3f-146">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="09b3f-146">MFCMAPI reference</span></span>

<span data-ttu-id="09b3f-147">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="09b3f-147">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="09b3f-148">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="09b3f-148">**File**</span></span>|<span data-ttu-id="09b3f-149">**関数**</span><span class="sxs-lookup"><span data-stu-id="09b3f-149">**Function**</span></span>|<span data-ttu-id="09b3f-150">**コメント**</span><span class="sxs-lookup"><span data-stu-id="09b3f-150">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="09b3f-151">Mapiabfunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="09b3f-151">Mapiabfunctions.cpp</span></span>  <br/> |<span data-ttu-id="09b3f-152">AddOneOffAddress</span><span class="sxs-lookup"><span data-stu-id="09b3f-152">AddOneOffAddress</span></span>  <br/> |<span data-ttu-id="09b3f-153">MFCMAPI は **CreateOneOff** メソッドを使用して、アドレス帳に含めされていないアドレスのエントリ ID を作成します。</span><span class="sxs-lookup"><span data-stu-id="09b3f-153">MFCMAPI uses the **CreateOneOff** method to create an entry ID for an address that is not found in any address book.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="09b3f-154">関連項目</span><span class="sxs-lookup"><span data-stu-id="09b3f-154">See also</span></span>



[<span data-ttu-id="09b3f-155">IMAPISupport::CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="09b3f-155">IMAPISupport::CreateOneOff</span></span>](imapisupport-createoneoff.md)
  
[<span data-ttu-id="09b3f-156">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="09b3f-156">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


<span data-ttu-id="09b3f-157">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="09b3f-157">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

