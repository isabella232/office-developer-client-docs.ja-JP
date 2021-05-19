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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411044"
---
# <a name="one-off-entry-identifiers"></a><span data-ttu-id="f4ec9-103">一時エントリ識別子</span><span class="sxs-lookup"><span data-stu-id="f4ec9-103">One-off entry identifiers</span></span>
  
<span data-ttu-id="f4ec9-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f4ec9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f4ec9-105">1 回限りエントリ識別子は **、IAddrBook::CreateOneOff** メソッドで MAPI によって作成され、ゲートウェイ コンポーネントなどの MAPI サブシステムにアクセスできないコンポーネントによって作成されます。</span><span class="sxs-lookup"><span data-stu-id="f4ec9-105">One-off entry identifiers are created by MAPI in the **IAddrBook::CreateOneOff** method and by components that do not have access to the MAPI subsystem, such as gateway components.</span></span> <span data-ttu-id="f4ec9-106">�ڍׂɂ��ẮA [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md)��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="f4ec9-106">For more information, see [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md).</span></span> <span data-ttu-id="f4ec9-107">次の図は、一時エントリ識別子の形式を示しています。</span><span class="sxs-lookup"><span data-stu-id="f4ec9-107">The following illustration shows the format of a one-off entry identifier.</span></span>
  
<span data-ttu-id="f4ec9-108">**一時エントリ識別子の形式**</span><span class="sxs-lookup"><span data-stu-id="f4ec9-108">**One-off entry identifier format**</span></span>
  
<span data-ttu-id="f4ec9-109">![1 回のエントリ識別子の形式](media/amapi_69.gif "1 回のエントリ識別子の形式")</span><span class="sxs-lookup"><span data-stu-id="f4ec9-109">![One-off entry identifier format](media/amapi_69.gif "One-off entry identifier format")</span></span>
  
<span data-ttu-id="f4ec9-110">最初のフィールドは、カスタム受信者を表すエントリ識別子を識別する特別な [MAPIUID](mapiuid.md) 構造です。</span><span class="sxs-lookup"><span data-stu-id="f4ec9-110">The first field is a special [MAPIUID](mapiuid.md) structure that identifies the entry identifier as representing a custom recipient.</span></span> <span data-ttu-id="f4ec9-111">この **MAPIUID** 構造体は、定数に設定する必要MAPI_ONE_OFF_UID。</span><span class="sxs-lookup"><span data-stu-id="f4ec9-111">This **MAPIUID** structure must be set to the constant MAPI_ONE_OFF_UID.</span></span> <span data-ttu-id="f4ec9-112">MAPI_ONE_OFF_UIDは、ヘッダー ファイル MAPIDEFS.H で定義されます。</span><span class="sxs-lookup"><span data-stu-id="f4ec9-112">MAPI_ONE_OFF_UID is defined in the header file MAPIDEFS.H.</span></span> 
  
<span data-ttu-id="f4ec9-113">バージョンとフラグのフィールドは、Intel のバイト順で 16 ビットの単語です。</span><span class="sxs-lookup"><span data-stu-id="f4ec9-113">The version and flags fields are 16-bit words in Intel byte order.</span></span> <span data-ttu-id="f4ec9-114">バージョン フィールドは 0 に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f4ec9-114">The version field must be set to zero.</span></span> <span data-ttu-id="f4ec9-115">flags フィールドは、次の値に設定できます。</span><span class="sxs-lookup"><span data-stu-id="f4ec9-115">The flags field can be set to the following values:</span></span>
  
<span data-ttu-id="f4ec9-116">MAPI_ONE_OFF_NO_RICH_INFO</span><span class="sxs-lookup"><span data-stu-id="f4ec9-116">MAPI_ONE_OFF_NO_RICH_INFO</span></span>
  
<span data-ttu-id="f4ec9-117">MAPI_ONE_OFF_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f4ec9-117">MAPI_ONE_OFF_UNICODE</span></span>
  
<span data-ttu-id="f4ec9-118">受信者MAPI_ONE_OFF_NO_RICH_INFOトランスポート ニュートラル カプセル化形式 (TNEF) でメッセージ コンテンツを受信しない場合は、このフラグが設定されます。</span><span class="sxs-lookup"><span data-stu-id="f4ec9-118">The MAPI_ONE_OFF_NO_RICH_INFO flag is set if a recipient should not receive message content in the Transport Neutral Encapsulation Format (TNEF).</span></span> <span data-ttu-id="f4ec9-119">このフラグは [、IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) MAPI_SEND_NO_RICH_INFOに渡される場合に設定されます。</span><span class="sxs-lookup"><span data-stu-id="f4ec9-119">This flag is set when MAPI_SEND_NO_RICH_INFO is passed to [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) method.</span></span> 
  
<span data-ttu-id="f4ec9-120">表示MAPI_ONE_OFF_UNICODE、電子メール アドレスが Unicode 文字列の場合は、このフラグが設定されます。</span><span class="sxs-lookup"><span data-stu-id="f4ec9-120">The MAPI_ONE_OFF_UNICODE flag is set if the display name and email address are Unicode strings.</span></span> <span data-ttu-id="f4ec9-121">このフラグは **、IAddrBook::CreateOneOff にMAPI_UNICODEが渡される場合に設定されます**。</span><span class="sxs-lookup"><span data-stu-id="f4ec9-121">This flag is set when the MAPI_UNICODE is passed to **IAddrBook::CreateOneOff**.</span></span> <span data-ttu-id="f4ec9-122">**CreateOneOff** に MAPI_UNICODEフラグが渡されない場合、MAPI は表示名と電子メール アドレス文字列がワークステーションの現在の ANSI 文字セットにあると見なします。</span><span class="sxs-lookup"><span data-stu-id="f4ec9-122">When the MAPI_UNICODE flag is not passed to **CreateOneOff**, MAPI assumes that the display name and email address strings are in the workstation's current ANSI character set.</span></span> <span data-ttu-id="f4ec9-123">ANSI 文字列は、通常、コード ページがエントリ識別子にエンコードされないので、異なる文字セットを使用してプラットフォーム間で送信されるメッセージではうまく動作しません。</span><span class="sxs-lookup"><span data-stu-id="f4ec9-123">ANSI strings generally do not work well in messages that are sent between platforms using different character sets because the code page is not encoded in the entry identifier.</span></span> <span data-ttu-id="f4ec9-124">この潜在的な非互換性から保護するために、多くのアドレスの種類は、複数の文字セットで一般的な文字にのみ制限されます。</span><span class="sxs-lookup"><span data-stu-id="f4ec9-124">To protect against this potential incompatibility, many address types are limited to only those characters that are common across multiple character sets.</span></span> <span data-ttu-id="f4ec9-125">ただし、文字セットとプラットフォームの互換性を確保するために、クライアントはメッセージ内の文字列に Unicode を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f4ec9-125">However, to ensure character set and platform compatibility, clients should use Unicode for the character strings in their messages.</span></span>
  
<span data-ttu-id="f4ec9-126">表示名は、受信者の **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティおよび **IAddrBook::CreateOneOff** に渡される _lpszName_ パラメーターに対応する null で終わる文字列です。</span><span class="sxs-lookup"><span data-stu-id="f4ec9-126">The display name is a null-terminated string that corresponds to the recipient's **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property and to the  _lpszName_ parameter passed to **IAddrBook::CreateOneOff**.</span></span> <span data-ttu-id="f4ec9-127">文字セットが Unicode の場合MAPI_ONE_OFF_UNICODEフラグが設定されている場合、ANSI はクリアです。</span><span class="sxs-lookup"><span data-stu-id="f4ec9-127">The character set is Unicode if the MAPI_ONE_OFF_UNICODE flag is set and ANSI if it is clear.</span></span> 
  
<span data-ttu-id="f4ec9-128">アドレスの種類は、受信者の **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) プロパティおよび **IAddrBook::CreateOneOff** に渡される _lpszAdrType_ パラメーターに対応する null 終端文字列です。</span><span class="sxs-lookup"><span data-stu-id="f4ec9-128">The address type is a null-terminated string that corresponds to the recipient's **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) property and to the  _lpszAdrType_ parameter passed to **IAddrBook::CreateOneOff**.</span></span> 
  
<span data-ttu-id="f4ec9-129">電子メール アドレスは、受信者の PR_EMAIL_ADDRESS ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) プロパティおよび **IAddrBook::CreateOneOff** に渡される _lpszAddress_ パラメーターに対応する null で終わる文字列です。 </span><span class="sxs-lookup"><span data-stu-id="f4ec9-129">The email address is a null-terminated string that corresponds to the recipient's **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) property and to the  _lpszAddress_ parameter passed to **IAddrBook::CreateOneOff**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f4ec9-130">1 回のエントリ識別子構造にパディングはありません。バイトは上で示したとおりにパックされ、エントリ識別子の長さは、電子メール アドレスの終端の null 文字を超えるバイトを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="f4ec9-130">There is no padding in one-off entry identifier structures; the bytes are packed exactly as indicated above and the entry identifier length should not include any bytes beyond the terminating null character of the email address.</span></span> 
  
<span data-ttu-id="f4ec9-131">一時エントリ識別子を手動で作成するクライアントおよびアドレス帳プロバイダーは **、PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) プロパティと PR_SEARCH_KEY ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) プロパティの値を生成する必要があります。 </span><span class="sxs-lookup"><span data-stu-id="f4ec9-131">Clients and address book providers that manually construct one-off entry identifiers might also need to generate values for the **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) and **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) properties.</span></span> <span data-ttu-id="f4ec9-132">レコード キーはエントリ識別子と同じです。</span><span class="sxs-lookup"><span data-stu-id="f4ec9-132">The record key is identical to the entry identifier.</span></span> <span data-ttu-id="f4ec9-133">検索キーは、次のフィールドを次の順序で連結して形成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f4ec9-133">The search key should be formed by concatenating the following fields in the following order:</span></span>
  
1. <span data-ttu-id="f4ec9-134">大文字に変換されたアドレスの種類。</span><span class="sxs-lookup"><span data-stu-id="f4ec9-134">The address type, converted to uppercase characters.</span></span>
    
2. <span data-ttu-id="f4ec9-135">コロン (:)。</span><span class="sxs-lookup"><span data-stu-id="f4ec9-135">A colon (:).</span></span>
    
3. <span data-ttu-id="f4ec9-136">大文字に変換された電子メール アドレス。</span><span class="sxs-lookup"><span data-stu-id="f4ec9-136">The email address, converted to uppercase characters.</span></span>
    
4. <span data-ttu-id="f4ec9-137">終端の null 文字。</span><span class="sxs-lookup"><span data-stu-id="f4ec9-137">A terminating null character.</span></span>
    
<span data-ttu-id="f4ec9-138">検索キーを生成するときに、文字セット変換を実行する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="f4ec9-138">No character set conversion must be done when generating the search key.</span></span>
  

