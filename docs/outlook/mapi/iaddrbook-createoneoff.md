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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: fefd81a7d6cdfda24df93ec928cd3305cb8ef8be
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800375"
---
# <a name="iaddrbookcreateoneoff"></a><span data-ttu-id="bf92f-103">IAddrBook::CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="bf92f-103">IAddrBook::CreateOneOff</span></span>

  
  
<span data-ttu-id="bf92f-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bf92f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bf92f-105">一時アドレスのエントリ id を作成します。</span><span class="sxs-lookup"><span data-stu-id="bf92f-105">Creates an entry identifier for a one-off address.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="bf92f-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bf92f-106">Parameters</span></span>

 <span data-ttu-id="bf92f-107">_lpszName_</span><span class="sxs-lookup"><span data-stu-id="bf92f-107">_lpszName_</span></span>
  
> <span data-ttu-id="bf92f-108">[in]受信者の**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) のプロパティの値へのポインター。</span><span class="sxs-lookup"><span data-stu-id="bf92f-108">[in] A pointer to the value of the recipient's **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span> <span data-ttu-id="bf92f-109">_LpszName_パラメーターは、NULL にすることができます。</span><span class="sxs-lookup"><span data-stu-id="bf92f-109">The  _lpszName_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="bf92f-110">_lpszAdrType_</span><span class="sxs-lookup"><span data-stu-id="bf92f-110">_lpszAdrType_</span></span>
  
> <span data-ttu-id="bf92f-111">[in]FAX または SMTP など、受信者のアドレスの種類へのポインター。</span><span class="sxs-lookup"><span data-stu-id="bf92f-111">[in] A pointer to the address type of the recipient, such as FAX or SMTP.</span></span> <span data-ttu-id="bf92f-112">_LpszAdrType_パラメーターは、NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="bf92f-112">The  _lpszAdrType_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="bf92f-113">_lpszAddress_</span><span class="sxs-lookup"><span data-stu-id="bf92f-113">_lpszAddress_</span></span>
  
> <span data-ttu-id="bf92f-114">[in]受信者のアドレスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="bf92f-114">[in] A pointer to the address of the recipient.</span></span> <span data-ttu-id="bf92f-115">_LpszAddress_パラメーターは、NULL にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="bf92f-115">The  _lpszAddress_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="bf92f-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="bf92f-116">_ulFlags_</span></span>
  
> <span data-ttu-id="bf92f-117">[in]1 回限りの受信者に影響を与えるフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="bf92f-117">[in] A bitmask of flags that affects the one-off recipient.</span></span> <span data-ttu-id="bf92f-118">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="bf92f-118">The following flags can be set:</span></span>
    
<span data-ttu-id="bf92f-119">MAPI_SEND_NO_RICH_INFO</span><span class="sxs-lookup"><span data-stu-id="bf92f-119">MAPI_SEND_NO_RICH_INFO</span></span> 
  
> <span data-ttu-id="bf92f-120">受信者には、コンテンツの書式設定されたメッセージを処理できません。</span><span class="sxs-lookup"><span data-stu-id="bf92f-120">The recipient cannot handle formatted message content.</span></span> <span data-ttu-id="bf92f-121">MAPI_SEND_NO_RICH_INFO を設定すると、MAPI では受信者の**PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) のプロパティを FALSE に設定します。</span><span class="sxs-lookup"><span data-stu-id="bf92f-121">If MAPI_SEND_NO_RICH_INFO is set, MAPI sets the recipient's **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) property to FALSE.</span></span> <span data-ttu-id="bf92f-122">MAPI_SEND_NO_RICH_INFO が設定されていない場合は、MAPI は_lpszAddress_で指定された受信者のメッセージのアドレスがインターネット アドレスを解釈しない限り、TRUE にこのプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="bf92f-122">If MAPI_SEND_NO_RICH_INFO is not set, MAPI sets this property to TRUE unless the recipient's messaging address pointed to by  _lpszAddress_ is interpreted to be an Internet address.</span></span> <span data-ttu-id="bf92f-123">この例では、MAPI は、 **PR_SEND_RICH_INFO**を FALSE に設定します。</span><span class="sxs-lookup"><span data-stu-id="bf92f-123">In this case, MAPI sets **PR_SEND_RICH_INFO** to FALSE.</span></span> 
    
<span data-ttu-id="bf92f-124">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="bf92f-124">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="bf92f-125">表示名、アドレスの種類、およびアドレスは、Unicode 形式では。</span><span class="sxs-lookup"><span data-stu-id="bf92f-125">The display name, address type, and address are in Unicode format.</span></span> <span data-ttu-id="bf92f-126">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式でこれらの文字列です。</span><span class="sxs-lookup"><span data-stu-id="bf92f-126">If the MAPI_UNICODE flag is not set, these strings are in ANSI format.</span></span>
    
 <span data-ttu-id="bf92f-127">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="bf92f-127">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="bf92f-128">[out]_LppEntryID_パラメーターで指定されたエントリの識別子のバイト数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="bf92f-128">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="bf92f-129">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="bf92f-129">_lppEntryID_</span></span>
  
> <span data-ttu-id="bf92f-130">[out]1 回限りの受信者のエントリの識別子へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="bf92f-130">[out] A pointer to a pointer to the entry identifier for the one-off recipient.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bf92f-131">�߂�l</span><span class="sxs-lookup"><span data-stu-id="bf92f-131">Return value</span></span>

<span data-ttu-id="bf92f-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="bf92f-132">S_OK</span></span> 
  
> <span data-ttu-id="bf92f-133">一時エントリ id が正常に作成されました。</span><span class="sxs-lookup"><span data-stu-id="bf92f-133">The one-off entry identifier was created successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bf92f-134">注釈</span><span class="sxs-lookup"><span data-stu-id="bf92f-134">Remarks</span></span>

<span data-ttu-id="bf92f-135">クライアントが 1 回限りの受信者のエントリ id を作成する**CreateOneOff**メソッドを呼び出して、現在読み込まれているアドレス帳プロバイダーのいずれかから任意のコンテナーに属していない受信者です。</span><span class="sxs-lookup"><span data-stu-id="bf92f-135">Clients call the **CreateOneOff** method to create an entry identifier for a one-off recipient — a recipient that does not belong to any of the containers from any of the currently loaded address book providers.</span></span> <span data-ttu-id="bf92f-136">一時受信者は、セッションのすべての種類のアクティブなアドレス帳のプロバイダーの 1 つによってサポートされているアドレスを持つことができます。</span><span class="sxs-lookup"><span data-stu-id="bf92f-136">One-off recipients can have any kind of address that is supported by one of the active address book providers for the session.</span></span> 
  
<span data-ttu-id="bf92f-137">一時受信者は通常、特定のアドレスの種類のテンプレートを使用して作成されます。</span><span class="sxs-lookup"><span data-stu-id="bf92f-137">One-off recipients are typically created with a template for their particular address type.</span></span> <span data-ttu-id="bf92f-138">アドレスの種類をサポートしているアドレス帳プロバイダーには、テンプレートが用意されています。</span><span class="sxs-lookup"><span data-stu-id="bf92f-138">The address book provider that supports the address type supplies the template.</span></span> <span data-ttu-id="bf92f-139">クライアント アプリケーションのユーザーは、テンプレートに関連する情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="bf92f-139">A user of a client application enters the relevant information into the template.</span></span>
  
<span data-ttu-id="bf92f-140">MAPI では、表示名、アドレスの種類、および**CreateOneOff**のアドレス パラメーターの文字の Unicode 文字列をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="bf92f-140">MAPI supports Unicode character strings for the display name, address type, and address parameters of **CreateOneOff**.</span></span>
  
<span data-ttu-id="bf92f-141">MAPI_SEND_NO_RICH_INFO フラグは、書式付きのテキストをリッチ テキスト形式 (RTF) では各メッセージと送信かどうかを制御します。</span><span class="sxs-lookup"><span data-stu-id="bf92f-141">The MAPI_SEND_NO_RICH_INFO flag controls whether formatted text in Rich Text Format (RTF) is sent along with each message.</span></span> <span data-ttu-id="bf92f-142">トランスポート ニュートラル カプセル化形式 (TNEF): 書式設定されたテキスト形式の送信に使用される-は、受信者が、 **PR_SEND_RICH_INFO**プロパティを設定する方法に関係なく、ほとんどのトランスポート プロバイダーによって送信されます。</span><span class="sxs-lookup"><span data-stu-id="bf92f-142">The Transport Neutral Encapsulation Format (TNEF) — a format that is used for transmitting formatted text — is sent by most transport providers, regardless of how the recipient sets its **PR_SEND_RICH_INFO** property.</span></span> <span data-ttu-id="bf92f-143">個人間のメッセージを処理するクライアントのメッセージングの問題ではありません。</span><span class="sxs-lookup"><span data-stu-id="bf92f-143">This is not an issue for messaging clients that work with interpersonal messages.</span></span> <span data-ttu-id="bf92f-144">ただし、通常は TNEF を送信するカスタム メッセージ クラス用のカスタム プロパティを使用、それをサポートしていないことがありますフォーム ベースのクライアントまたはユーザー設定の MAPI プロパティを必要とするクライアントの問題。</span><span class="sxs-lookup"><span data-stu-id="bf92f-144">However, because TNEF is typically used to send custom properties for custom message classes, not supporting it can be a problem for form-based clients or clients that require custom MAPI properties.</span></span> <span data-ttu-id="bf92f-145">詳細については、 [TNEF をメッセージの送信](sending-messages-with-tnef.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bf92f-145">For more information, see [Sending Messages with TNEF](sending-messages-with-tnef.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="bf92f-146">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="bf92f-146">MFCMAPI reference</span></span>

<span data-ttu-id="bf92f-147">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="bf92f-147">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="bf92f-148">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="bf92f-148">**File**</span></span>|<span data-ttu-id="bf92f-149">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="bf92f-149">**Function**</span></span>|<span data-ttu-id="bf92f-150">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="bf92f-150">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bf92f-151">Mapiabfunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="bf92f-151">Mapiabfunctions.cpp</span></span>  <br/> |<span data-ttu-id="bf92f-152">AddOneOffAddress</span><span class="sxs-lookup"><span data-stu-id="bf92f-152">AddOneOffAddress</span></span>  <br/> |<span data-ttu-id="bf92f-153">MFCMAPI では、 **CreateOneOff**メソッドを使用して、任意のアドレス帳に含まれていないアドレスのエントリ ID を作成します。</span><span class="sxs-lookup"><span data-stu-id="bf92f-153">MFCMAPI uses the **CreateOneOff** method to create an entry ID for an address that is not found in any address book.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bf92f-154">関連項目</span><span class="sxs-lookup"><span data-stu-id="bf92f-154">See also</span></span>



[<span data-ttu-id="bf92f-155">IMAPISupport::CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="bf92f-155">IMAPISupport::CreateOneOff</span></span>](imapisupport-createoneoff.md)
  
[<span data-ttu-id="bf92f-156">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="bf92f-156">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


<span data-ttu-id="bf92f-157">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="bf92f-157">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

