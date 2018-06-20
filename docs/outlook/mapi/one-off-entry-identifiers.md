---
title: 一時エントリ id
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 741d21ae-f14a-4b7f-80aa-91d0f0ff3f34
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 1335de3c1decf6c594f0148fbbf055061d7ce7e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801670"
---
# <a name="one-off-entry-identifiers"></a><span data-ttu-id="b8c8b-103">一時エントリ id</span><span class="sxs-lookup"><span data-stu-id="b8c8b-103">One-off entry identifiers</span></span>
  
<span data-ttu-id="b8c8b-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b8c8b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b8c8b-105">一時エントリ id は、 **IAddrBook::CreateOneOff**メソッドでは、MAPI とゲートウェイ ・ コンポーネントなど、MAPI サブシステムへのアクセス権を持たないコンポーネントによって作成されます。</span><span class="sxs-lookup"><span data-stu-id="b8c8b-105">One-off entry identifiers are created by MAPI in the **IAddrBook::CreateOneOff** method and by components that do not have access to the MAPI subsystem, such as gateway components.</span></span> <span data-ttu-id="b8c8b-106">�ڍׂɂ��ẮA [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md)��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="b8c8b-106">For more information, see [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md).</span></span> <span data-ttu-id="b8c8b-107">一時エントリ id の形式を次の図に示します。</span><span class="sxs-lookup"><span data-stu-id="b8c8b-107">The following illustration shows the format of a one-off entry identifier.</span></span>
  
<span data-ttu-id="b8c8b-108">**一時エントリの識別子の形式**</span><span class="sxs-lookup"><span data-stu-id="b8c8b-108">**One-off entry identifier format**</span></span>
  
<span data-ttu-id="b8c8b-109">![一時エントリの識別子の形式](media/amapi_69.gif "一時エントリの識別子の形式")</span><span class="sxs-lookup"><span data-stu-id="b8c8b-109">![One-off entry identifier format](media/amapi_69.gif "One-off entry identifier format")</span></span>
  
<span data-ttu-id="b8c8b-110">最初のフィールドは、カスタム受信者を表すものとしてのエントリ id を識別する特殊な[MAPIUID](mapiuid.md)構造です。</span><span class="sxs-lookup"><span data-stu-id="b8c8b-110">The first field is a special [MAPIUID](mapiuid.md) structure that identifies the entry identifier as representing a custom recipient.</span></span> <span data-ttu-id="b8c8b-111">この**MAPIUID**の構造体は、定数 MAPI_ONE_OFF_UID を設定しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="b8c8b-111">This **MAPIUID** structure must be set to the constant MAPI_ONE_OFF_UID.</span></span> <span data-ttu-id="b8c8b-112">MAPI_ONE_OFF_UID は、MAPIDEFS ヘッダー ファイルで定義されます。H.</span><span class="sxs-lookup"><span data-stu-id="b8c8b-112">MAPI_ONE_OFF_UID is defined in the header file MAPIDEFS.H.</span></span> 
  
<span data-ttu-id="b8c8b-113">バージョンとフラグ フィールドには、Intel のバイト順の 16 ビット ワードです。</span><span class="sxs-lookup"><span data-stu-id="b8c8b-113">The version and flags fields are 16-bit words in Intel byte order.</span></span> <span data-ttu-id="b8c8b-114">バージョン フィールドはゼロに設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b8c8b-114">The version field must be set to zero.</span></span> <span data-ttu-id="b8c8b-115">フラグ フィールドは、次の値に設定できます。</span><span class="sxs-lookup"><span data-stu-id="b8c8b-115">The flags field can be set to the following values:</span></span>
  
<span data-ttu-id="b8c8b-116">MAPI_ONE_OFF_NO_RICH_INFO</span><span class="sxs-lookup"><span data-stu-id="b8c8b-116">MAPI_ONE_OFF_NO_RICH_INFO</span></span>
  
<span data-ttu-id="b8c8b-117">MAPI_ONE_OFF_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b8c8b-117">MAPI_ONE_OFF_UNICODE</span></span>
  
<span data-ttu-id="b8c8b-118">受信者が表示されなくなりますメッセージの内容で、トランスポート ニュートラル カプセル化形式 (TNEF) 場合、MAPI_ONE_OFF_NO_RICH_INFO フラグが設定されています。</span><span class="sxs-lookup"><span data-stu-id="b8c8b-118">The MAPI_ONE_OFF_NO_RICH_INFO flag is set if a recipient should not receive message content in the Transport Neutral Encapsulation Format (TNEF).</span></span> <span data-ttu-id="b8c8b-119">MAPI_SEND_NO_RICH_INFO は、 [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md)メソッドに渡されるとき、このフラグが設定されています。</span><span class="sxs-lookup"><span data-stu-id="b8c8b-119">This flag is set when MAPI_SEND_NO_RICH_INFO is passed to [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) method.</span></span> 
  
<span data-ttu-id="b8c8b-120">表示名と電子メール アドレスが Unicode 文字列である場合、MAPI_ONE_OFF_UNICODE フラグが設定されています。</span><span class="sxs-lookup"><span data-stu-id="b8c8b-120">The MAPI_ONE_OFF_UNICODE flag is set if the display name and email address are Unicode strings.</span></span> <span data-ttu-id="b8c8b-121">MAPI_UNICODE が**IAddrBook::CreateOneOff**に渡された場合、このフラグが設定されています。</span><span class="sxs-lookup"><span data-stu-id="b8c8b-121">This flag is set when the MAPI_UNICODE is passed to **IAddrBook::CreateOneOff**.</span></span> <span data-ttu-id="b8c8b-122">**CreateOneOff**に MAPI_UNICODE フラグが渡されない、MAPI では、ワークステーションの現在の ANSI 文字セットでは、表示名と電子メール アドレスの文字列を想定しています。</span><span class="sxs-lookup"><span data-stu-id="b8c8b-122">When the MAPI_UNICODE flag is not passed to **CreateOneOff**, MAPI assumes that the display name and email address strings are in the workstation's current ANSI character set.</span></span> <span data-ttu-id="b8c8b-123">ANSI 文字列は、一般にエントリの識別子のコード ページがエンコードされていませんので、別の文字セットを使用してプラットフォーム間で送信されるメッセージでは動作しません。</span><span class="sxs-lookup"><span data-stu-id="b8c8b-123">ANSI strings generally do not work well in messages that are sent between platforms using different character sets because the code page is not encoded in the entry identifier.</span></span> <span data-ttu-id="b8c8b-124">この潜在的な互換性の問題を防ぐには、多くのアドレスの種類は、複数の文字セットに共通の文字だけに制限されます。</span><span class="sxs-lookup"><span data-stu-id="b8c8b-124">To protect against this potential incompatibility, many address types are limited to only those characters that are common across multiple character sets.</span></span> <span data-ttu-id="b8c8b-125">ただし、文字セットとプラットフォームの互換性を確保するのにはクライアントする必要があります Unicode を使用、メッセージ内の文字の文字列です。</span><span class="sxs-lookup"><span data-stu-id="b8c8b-125">However, to ensure character set and platform compatibility, clients should use Unicode for the character strings in their messages.</span></span>
  
<span data-ttu-id="b8c8b-126">表示名は、受信者の**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) のプロパティを**IAddrBook::CreateOneOff**に渡される_lpszName_パラメーターに対応する null で終わる文字列です。</span><span class="sxs-lookup"><span data-stu-id="b8c8b-126">The display name is a null-terminated string that corresponds to the recipient's **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property and to the  _lpszName_ parameter passed to **IAddrBook::CreateOneOff**.</span></span> <span data-ttu-id="b8c8b-127">明らかな場合、MAPI_ONE_OFF_UNICODE フラグが設定されたと ANSI の場合、文字セット、ユニコードです。</span><span class="sxs-lookup"><span data-stu-id="b8c8b-127">The character set is Unicode if the MAPI_ONE_OFF_UNICODE flag is set and ANSI if it is clear.</span></span> 
  
<span data-ttu-id="b8c8b-128">アドレスの種類は、受信者の**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) のプロパティを**IAddrBook::CreateOneOff**に渡される_lpszAdrType_パラメーターに対応する null で終わる文字列です。</span><span class="sxs-lookup"><span data-stu-id="b8c8b-128">The address type is a null-terminated string that corresponds to the recipient's **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) property and to the  _lpszAdrType_ parameter passed to **IAddrBook::CreateOneOff**.</span></span> 
  
<span data-ttu-id="b8c8b-129">電子メール アドレスは、受信者の**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) のプロパティを**IAddrBook::CreateOneOff**に渡される_lpszAddress_パラメーターに対応する null で終わる文字列です。</span><span class="sxs-lookup"><span data-stu-id="b8c8b-129">The email address is a null-terminated string that corresponds to the recipient's **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) property and to the  _lpszAddress_ parameter passed to **IAddrBook::CreateOneOff**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="b8c8b-130">1 回限りのエントリの識別子構造体です。バイトの上に示されるとおりに梱包し、エントリの識別子の長さは、電子メール アドレスの末尾の null 文字を超える任意のバイト数を含めないようにします。</span><span class="sxs-lookup"><span data-stu-id="b8c8b-130">There is no padding in one-off entry identifier structures; the bytes are packed exactly as indicated above and the entry identifier length should not include any bytes beyond the terminating null character of the email address.</span></span> 
  
<span data-ttu-id="b8c8b-131">クライアントと一時エントリ id を手動で作成したアドレス帳プロバイダーは、 **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) と**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) のプロパティの値を生成する必要もあります。</span><span class="sxs-lookup"><span data-stu-id="b8c8b-131">Clients and address book providers that manually construct one-off entry identifiers might also need to generate values for the **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) and **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) properties.</span></span> <span data-ttu-id="b8c8b-132">レコード キーは、エントリの識別子と同じです。</span><span class="sxs-lookup"><span data-stu-id="b8c8b-132">The record key is identical to the entry identifier.</span></span> <span data-ttu-id="b8c8b-133">検索キーは、次の順序で次のフィールドを連結することにより形成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b8c8b-133">The search key should be formed by concatenating the following fields in the following order:</span></span>
  
1. <span data-ttu-id="b8c8b-134">アドレスの種類、文字の大文字に変換します。</span><span class="sxs-lookup"><span data-stu-id="b8c8b-134">The address type, converted to uppercase characters.</span></span>
    
2. <span data-ttu-id="b8c8b-135">コロン (:)。</span><span class="sxs-lookup"><span data-stu-id="b8c8b-135">A colon (:).</span></span>
    
3. <span data-ttu-id="b8c8b-136">電子メールのアドレスは、大文字に変換されます。</span><span class="sxs-lookup"><span data-stu-id="b8c8b-136">The email address, converted to uppercase characters.</span></span>
    
4. <span data-ttu-id="b8c8b-137">終端の null 文字です。</span><span class="sxs-lookup"><span data-stu-id="b8c8b-137">A terminating null character.</span></span>
    
<span data-ttu-id="b8c8b-138">文字セット変換する必要がありますを完了できません、検索キーを生成するとき。</span><span class="sxs-lookup"><span data-stu-id="b8c8b-138">No character set conversion must be done when generating the search key.</span></span>
  

