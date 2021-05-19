---
title: SMTP アドレス
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 42015740-a94f-4628-bf32-b7fc2fdb9ff6
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: fb4402100891df8b27c8d26900a4acd05f4183e3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419626"
---
# <a name="smtp-addresses"></a><span data-ttu-id="08145-103">SMTP アドレス</span><span class="sxs-lookup"><span data-stu-id="08145-103">SMTP Addresses</span></span>

  
  
<span data-ttu-id="08145-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="08145-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="08145-105">SMTP 電子メール アドレスの形式は RFC 822 で定義されています。</span><span class="sxs-lookup"><span data-stu-id="08145-105">The format of SMTP email addresses is defined in RFC 822.</span></span> <span data-ttu-id="08145-106">MAPI コンポーネントは、その標準に準拠するアドレスを処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="08145-106">MAPI components should handle any address that complies with that standard.</span></span> <span data-ttu-id="08145-107">ただし、MAPI アドレスを最適にエンコードする RFC 822 アドレスの特定の形式があります。</span><span class="sxs-lookup"><span data-stu-id="08145-107">However, there is a particular form of RFC 822 address that best encodes MAPI addresses:</span></span>
  
 <span data-ttu-id="08145-108">_表示名_ **\<**_電子メール アドレス_**\>**</span><span class="sxs-lookup"><span data-stu-id="08145-108">_display-name_ **\<** _email-address_ **\>**</span></span>
  
<span data-ttu-id="08145-109">角かっこはリテラルとして含まれます。</span><span class="sxs-lookup"><span data-stu-id="08145-109">The angle brackets are included as literals.</span></span> <span data-ttu-id="08145-110">空白は、表示名で一般的です。引用符で囲む必要はない。</span><span class="sxs-lookup"><span data-stu-id="08145-110">Blanks are common in display names; they need not be quoted.</span></span> <span data-ttu-id="08145-111">一般的なアドレスは、RFC 1521 の共同編集者の 1 つに属する次のように見える場合があります。</span><span class="sxs-lookup"><span data-stu-id="08145-111">A typical address might look like this one, which belongs to one of the coauthors of RFC 1521:</span></span>
  
<span data-ttu-id="08145-112">ナサニエル・ボレンシュタイン nsb@bellcore.com \<\></span><span class="sxs-lookup"><span data-stu-id="08145-112">Nathaniel Borenstein \<nsb@bellcore.com\></span></span>
  
<span data-ttu-id="08145-113">表示名に SMTP アドレス (@など) に特別な意味を持つ文字が含まれている場合は、表示名全体を二重引用符 \< で囲む必要があります。</span><span class="sxs-lookup"><span data-stu-id="08145-113">If the display name contains characters that have special meaning in SMTP addresses, such as \< or @, the entire display name should be enclosed in double quotes.</span></span> <span data-ttu-id="08145-114">送信メールでは、電子メール アドレスと表示名の合計長が 255 文字を超える場合は、表示名を削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="08145-114">On outbound mail, if the total length of the email address plus display name exceeds 255 characters, the display name should be dropped.</span></span>
  
<span data-ttu-id="08145-115">SMTP アドレスの各部分は、次のように MAPI プロパティにマップされます。</span><span class="sxs-lookup"><span data-stu-id="08145-115">The parts of an SMTP address map into MAPI properties as follows:</span></span>
  
|<span data-ttu-id="08145-116">**SMTP アドレス コンポーネント**</span><span class="sxs-lookup"><span data-stu-id="08145-116">**SMTP address component**</span></span>|<span data-ttu-id="08145-117">**MAPI プロパティ**</span><span class="sxs-lookup"><span data-stu-id="08145-117">**MAPI property**</span></span>|
|:-----|:-----|
| <span data-ttu-id="08145-118">_すべての受信者の_ 表示名</span><span class="sxs-lookup"><span data-stu-id="08145-118">_display-name_ for all recipients</span></span>  <br/> |<span data-ttu-id="08145-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="08145-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |
| <span data-ttu-id="08145-120">_[From] フィールド_ の表示名</span><span class="sxs-lookup"><span data-stu-id="08145-120">_display-name_ for From field</span></span>  <br/> |<span data-ttu-id="08145-121">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="08145-121">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span></span>  <br/> |
| <span data-ttu-id="08145-122">_送信者フィールドの_ 表示名</span><span class="sxs-lookup"><span data-stu-id="08145-122">_display-name_ for Sender field</span></span>  <br/> |<span data-ttu-id="08145-123">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="08145-123">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span></span>  <br/> |
| <span data-ttu-id="08145-124">_電子メール アドレス_</span><span class="sxs-lookup"><span data-stu-id="08145-124">_email-address_</span></span> <br/> |<span data-ttu-id="08145-125">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="08145-125">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="08145-126">暗黙的、常に "SMTP"</span><span class="sxs-lookup"><span data-stu-id="08145-126">implicit, always "SMTP"</span></span>  <br/> |<span data-ttu-id="08145-127">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="08145-127">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>  <br/> |
   
<span data-ttu-id="08145-128">受信メールにアドレスの表示名がない場合は、代わりに電子メール アドレス全体を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="08145-128">If there is no display name for an address on inbound mail, the entire email address should be used instead.</span></span> <span data-ttu-id="08145-129">アドレスの種類は常に SMTP です。</span><span class="sxs-lookup"><span data-stu-id="08145-129">The address type is always SMTP.</span></span>
  
<span data-ttu-id="08145-130">受信者のプロパティは、MAPI メッセージの受信者テーブルから取られます。sender プロパティは、メッセージ自体から取られます。</span><span class="sxs-lookup"><span data-stu-id="08145-130">Recipient properties are taken from the MAPI message's recipient table; sender properties are taken from the message itself.</span></span>
  

