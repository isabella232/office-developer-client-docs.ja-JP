---
title: 一時エントリ識別子
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 741d21ae-f14a-4b7f-80aa-91d0f0ff3f34
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: abe52cb45e13e6713d28fffe379e245e2483bffa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279694"
---
# <a name="one-off-entry-identifiers"></a><span data-ttu-id="eaadd-103">一時エントリ識別子</span><span class="sxs-lookup"><span data-stu-id="eaadd-103">One-off entry identifiers</span></span>
  
<span data-ttu-id="eaadd-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eaadd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eaadd-105">**IAddrBook:: createoneoff**メソッドと、ゲートウェイコンポーネントなどの mapi サブシステムにアクセスできないコンポーネントによって、1回限りのエントリ識別子が mapi によって作成されます。</span><span class="sxs-lookup"><span data-stu-id="eaadd-105">One-off entry identifiers are created by MAPI in the **IAddrBook::CreateOneOff** method and by components that do not have access to the MAPI subsystem, such as gateway components.</span></span> <span data-ttu-id="eaadd-106">�ڍׂɂ��ẮA [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md)��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="eaadd-106">For more information, see [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md).</span></span> <span data-ttu-id="eaadd-107">次の図は、1回限りのエントリ識別子の形式を示しています。</span><span class="sxs-lookup"><span data-stu-id="eaadd-107">The following illustration shows the format of a one-off entry identifier.</span></span>
  
<span data-ttu-id="eaadd-108">**一時エントリ識別子の形式**</span><span class="sxs-lookup"><span data-stu-id="eaadd-108">**One-off entry identifier format**</span></span>
  
<span data-ttu-id="eaadd-109">![1 回限りのエントリ識別子形式](media/amapi_69.gif "1 回限りのエントリ識別子形式")</span><span class="sxs-lookup"><span data-stu-id="eaadd-109">![One-off entry identifier format](media/amapi_69.gif "One-off entry identifier format")</span></span>
  
<span data-ttu-id="eaadd-110">最初のフィールドは、カスタム受信者を表すエントリ id を識別する特別な[MAPIUID](mapiuid.md)構造です。</span><span class="sxs-lookup"><span data-stu-id="eaadd-110">The first field is a special [MAPIUID](mapiuid.md) structure that identifies the entry identifier as representing a custom recipient.</span></span> <span data-ttu-id="eaadd-111">この**MAPIUID**構造は、定数 MAPI_ONE_OFF_UID に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="eaadd-111">This **MAPIUID** structure must be set to the constant MAPI_ONE_OFF_UID.</span></span> <span data-ttu-id="eaadd-112">MAPI_ONE_OFF_UID は、ヘッダーファイル mapidefs.h で定義されています。H.</span><span class="sxs-lookup"><span data-stu-id="eaadd-112">MAPI_ONE_OFF_UID is defined in the header file MAPIDEFS.H.</span></span> 
  
<span data-ttu-id="eaadd-113">version および flags フィールドは、Intel バイトオーダーでの16ビットの単語です。</span><span class="sxs-lookup"><span data-stu-id="eaadd-113">The version and flags fields are 16-bit words in Intel byte order.</span></span> <span data-ttu-id="eaadd-114">バージョンフィールドは0に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="eaadd-114">The version field must be set to zero.</span></span> <span data-ttu-id="eaadd-115">flags フィールドには、次の値を設定できます。</span><span class="sxs-lookup"><span data-stu-id="eaadd-115">The flags field can be set to the following values:</span></span>
  
<span data-ttu-id="eaadd-116">MAPI_ONE_OFF_NO_RICH_INFO</span><span class="sxs-lookup"><span data-stu-id="eaadd-116">MAPI_ONE_OFF_NO_RICH_INFO</span></span>
  
<span data-ttu-id="eaadd-117">MAPI_ONE_OFF_UNICODE</span><span class="sxs-lookup"><span data-stu-id="eaadd-117">MAPI_ONE_OFF_UNICODE</span></span>
  
<span data-ttu-id="eaadd-118">MAPI_ONE_OFF_NO_RICH_INFO フラグは、受信者がトランスポートニュートラルカプセル化形式 (TNEF) でメッセージコンテンツを受信できないように設定されています。</span><span class="sxs-lookup"><span data-stu-id="eaadd-118">The MAPI_ONE_OFF_NO_RICH_INFO flag is set if a recipient should not receive message content in the Transport Neutral Encapsulation Format (TNEF).</span></span> <span data-ttu-id="eaadd-119">このフラグは、MAPI_SEND_NO_RICH_INFO が[IAddrBook:: createoneoff](iaddrbook-createoneoff.md)メソッドに渡されたときに設定されます。</span><span class="sxs-lookup"><span data-stu-id="eaadd-119">This flag is set when MAPI_SEND_NO_RICH_INFO is passed to [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) method.</span></span> 
  
<span data-ttu-id="eaadd-120">表示名と電子メールアドレスが UNICODE 文字列の場合は、MAPI_ONE_OFF_UNICODE フラグが設定されます。</span><span class="sxs-lookup"><span data-stu-id="eaadd-120">The MAPI_ONE_OFF_UNICODE flag is set if the display name and email address are Unicode strings.</span></span> <span data-ttu-id="eaadd-121">このフラグは、MAPI_UNICODE が**IAddrBook:: createoneoff**に渡されたときに設定されます。</span><span class="sxs-lookup"><span data-stu-id="eaadd-121">This flag is set when the MAPI_UNICODE is passed to **IAddrBook::CreateOneOff**.</span></span> <span data-ttu-id="eaadd-122">MAPI_UNICODE フラグが**createoneoff**に渡されていない場合、MAPI では、表示名と電子メールアドレスの文字列がワークステーションの現在の ANSI 文字セットに含まれていると見なされます。</span><span class="sxs-lookup"><span data-stu-id="eaadd-122">When the MAPI_UNICODE flag is not passed to **CreateOneOff**, MAPI assumes that the display name and email address strings are in the workstation's current ANSI character set.</span></span> <span data-ttu-id="eaadd-123">ANSI 文字列は、コードページがエントリ識別子でエンコードされていないために、異なる文字セットを使用してプラットフォーム間で送信されるメッセージでは、通常は適切に機能しません。</span><span class="sxs-lookup"><span data-stu-id="eaadd-123">ANSI strings generally do not work well in messages that are sent between platforms using different character sets because the code page is not encoded in the entry identifier.</span></span> <span data-ttu-id="eaadd-124">このような非互換性の問題から保護するために、多くのアドレスの種類は、複数の文字セットで共通の文字に制限されています。</span><span class="sxs-lookup"><span data-stu-id="eaadd-124">To protect against this potential incompatibility, many address types are limited to only those characters that are common across multiple character sets.</span></span> <span data-ttu-id="eaadd-125">ただし、文字セットとプラットフォームの互換性を確保するために、クライアントはメッセージ内の文字列に Unicode を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="eaadd-125">However, to ensure character set and platform compatibility, clients should use Unicode for the character strings in their messages.</span></span>
  
<span data-ttu-id="eaadd-126">表示名は、受信者の**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティ、および**IAddrBook:: createoneoff**に渡された_lpszname_パラメーターに対応する、null で終わる文字列です。</span><span class="sxs-lookup"><span data-stu-id="eaadd-126">The display name is a null-terminated string that corresponds to the recipient's **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property and to the  _lpszName_ parameter passed to **IAddrBook::CreateOneOff**.</span></span> <span data-ttu-id="eaadd-127">MAPI_ONE_OFF_UNICODE フラグが設定されている場合、文字セットが Unicode で、クリアされている場合は ANSI になります。</span><span class="sxs-lookup"><span data-stu-id="eaadd-127">The character set is Unicode if the MAPI_ONE_OFF_UNICODE flag is set and ANSI if it is clear.</span></span> 
  
<span data-ttu-id="eaadd-128">アドレスの種類は、受信者の**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) プロパティ、および**IAddrBook:: createoneoff**に渡された_lpszadrtype_パラメーターに対応する、null で終わる文字列です。</span><span class="sxs-lookup"><span data-stu-id="eaadd-128">The address type is a null-terminated string that corresponds to the recipient's **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) property and to the  _lpszAdrType_ parameter passed to **IAddrBook::CreateOneOff**.</span></span> 
  
<span data-ttu-id="eaadd-129">電子メールアドレスは、受信者の**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) プロパティ、および**IAddrBook:: createoneoff**に渡された_lpszaddress_パラメーターに対応する、null で終了する文字列です。</span><span class="sxs-lookup"><span data-stu-id="eaadd-129">The email address is a null-terminated string that corresponds to the recipient's **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) property and to the  _lpszAddress_ parameter passed to **IAddrBook::CreateOneOff**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="eaadd-130">1回限りのエントリ識別子の構造には、パディングはありません。バイトは上記で示したとおりにパックされ、エントリ識別子の長さには、電子メールアドレスの終端の null 文字を超えるバイトを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="eaadd-130">There is no padding in one-off entry identifier structures; the bytes are packed exactly as indicated above and the entry identifier length should not include any bytes beyond the terminating null character of the email address.</span></span> 
  
<span data-ttu-id="eaadd-131">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) および**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) プロパティの値を生成する必要があるのは、1回限りのエントリ識別子を手動で作成するクライアントとアドレス帳プロバイダーです。</span><span class="sxs-lookup"><span data-stu-id="eaadd-131">Clients and address book providers that manually construct one-off entry identifiers might also need to generate values for the **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) and **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) properties.</span></span> <span data-ttu-id="eaadd-132">record キーは、エントリ識別子と同じです。</span><span class="sxs-lookup"><span data-stu-id="eaadd-132">The record key is identical to the entry identifier.</span></span> <span data-ttu-id="eaadd-133">検索キーは、次の順序で各フィールドを連結することによって形成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="eaadd-133">The search key should be formed by concatenating the following fields in the following order:</span></span>
  
1. <span data-ttu-id="eaadd-134">住所の種類を大文字に変換します。</span><span class="sxs-lookup"><span data-stu-id="eaadd-134">The address type, converted to uppercase characters.</span></span>
    
2. <span data-ttu-id="eaadd-135">コロン (:)</span><span class="sxs-lookup"><span data-stu-id="eaadd-135">A colon (:).</span></span>
    
3. <span data-ttu-id="eaadd-136">電子メールアドレス。大文字に変換されます。</span><span class="sxs-lookup"><span data-stu-id="eaadd-136">The email address, converted to uppercase characters.</span></span>
    
4. <span data-ttu-id="eaadd-137">終端の null 文字。</span><span class="sxs-lookup"><span data-stu-id="eaadd-137">A terminating null character.</span></span>
    
<span data-ttu-id="eaadd-138">検索キーを生成するときに、文字セット変換を行わないでください。</span><span class="sxs-lookup"><span data-stu-id="eaadd-138">No character set conversion must be done when generating the search key.</span></span>
  

