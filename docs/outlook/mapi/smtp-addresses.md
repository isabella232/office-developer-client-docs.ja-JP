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
# <a name="smtp-addresses"></a><span data-ttu-id="9ae25-103">SMTP アドレス</span><span class="sxs-lookup"><span data-stu-id="9ae25-103">SMTP Addresses</span></span>

  
  
<span data-ttu-id="9ae25-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9ae25-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9ae25-105">SMTP 電子メールアドレスの形式は、RFC 822 で定義されています。</span><span class="sxs-lookup"><span data-stu-id="9ae25-105">The format of SMTP email addresses is defined in RFC 822.</span></span> <span data-ttu-id="9ae25-106">MAPI コンポーネントは、その標準に準拠する任意のアドレスを処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9ae25-106">MAPI components should handle any address that complies with that standard.</span></span> <span data-ttu-id="9ae25-107">ただし、次のような特定の形式の RFC 822 アドレスは、MAPI アドレスを最適にエンコードします。</span><span class="sxs-lookup"><span data-stu-id="9ae25-107">However, there is a particular form of RFC 822 address that best encodes MAPI addresses:</span></span>
  
 <span data-ttu-id="9ae25-108">_表示名_**\<** _電子メールアドレス_**\>**</span><span class="sxs-lookup"><span data-stu-id="9ae25-108">_display-name_ **\<** _email-address_ **\>**</span></span>
  
<span data-ttu-id="9ae25-109">山かっこは、リテラルとして含まれています。</span><span class="sxs-lookup"><span data-stu-id="9ae25-109">The angle brackets are included as literals.</span></span> <span data-ttu-id="9ae25-110">空白は表示名によく見られます。引用符で囲む必要はありません。</span><span class="sxs-lookup"><span data-stu-id="9ae25-110">Blanks are common in display names; they need not be quoted.</span></span> <span data-ttu-id="9ae25-111">一般的な住所は、RFC 1521 の coauthors のいずれかに属している次のようになります。</span><span class="sxs-lookup"><span data-stu-id="9ae25-111">A typical address might look like this one, which belongs to one of the coauthors of RFC 1521:</span></span>
  
<span data-ttu-id="9ae25-112">Nathaniel Borenstein \<nsb@bellcore.com\></span><span class="sxs-lookup"><span data-stu-id="9ae25-112">Nathaniel Borenstein \<nsb@bellcore.com\></span></span>
  
<span data-ttu-id="9ae25-113">\<または @ などの SMTP アドレスで特別な意味を持つ文字が表示名に含まれている場合は、表示名全体を二重引用符で囲む必要があります。</span><span class="sxs-lookup"><span data-stu-id="9ae25-113">If the display name contains characters that have special meaning in SMTP addresses, such as \< or @, the entire display name should be enclosed in double quotes.</span></span> <span data-ttu-id="9ae25-114">送信メールで、電子メールアドレスと表示名の長さの合計が255文字を超えている場合は、表示名を削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9ae25-114">On outbound mail, if the total length of the email address plus display name exceeds 255 characters, the display name should be dropped.</span></span>
  
<span data-ttu-id="9ae25-115">次に示すように、SMTP アドレスを MAPI プロパティにマップします。</span><span class="sxs-lookup"><span data-stu-id="9ae25-115">The parts of an SMTP address map into MAPI properties as follows:</span></span>
  
|<span data-ttu-id="9ae25-116">**SMTP アドレスコンポーネント**</span><span class="sxs-lookup"><span data-stu-id="9ae25-116">**SMTP address component**</span></span>|<span data-ttu-id="9ae25-117">**MAPI プロパティ**</span><span class="sxs-lookup"><span data-stu-id="9ae25-117">**MAPI property**</span></span>|
|:-----|:-----|
| <span data-ttu-id="9ae25-118">すべての受信者の_表示名_</span><span class="sxs-lookup"><span data-stu-id="9ae25-118">_display-name_ for all recipients</span></span>  <br/> |<span data-ttu-id="9ae25-119">**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9ae25-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |
| <span data-ttu-id="9ae25-120">From フィールドの_表示名_</span><span class="sxs-lookup"><span data-stu-id="9ae25-120">_display-name_ for From field</span></span>  <br/> |<span data-ttu-id="9ae25-121">**PR_SENDER_NAME**([PidTagSenderName](pidtagsendername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9ae25-121">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span></span>  <br/> |
| <span data-ttu-id="9ae25-122">送信者フィールドの_表示名_</span><span class="sxs-lookup"><span data-stu-id="9ae25-122">_display-name_ for Sender field</span></span>  <br/> |<span data-ttu-id="9ae25-123">**PR_SENT_REPRESENTING_NAME**([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9ae25-123">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span></span>  <br/> |
| <span data-ttu-id="9ae25-124">_電子メールアドレス_</span><span class="sxs-lookup"><span data-stu-id="9ae25-124">_email-address_</span></span> <br/> |<span data-ttu-id="9ae25-125">**PR_EMAIL_ADDRESS**([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9ae25-125">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="9ae25-126">暗黙的、常に "SMTP"</span><span class="sxs-lookup"><span data-stu-id="9ae25-126">implicit, always "SMTP"</span></span>  <br/> |<span data-ttu-id="9ae25-127">**PR_ADDRTYPE**([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9ae25-127">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>  <br/> |
   
<span data-ttu-id="9ae25-128">受信メールのアドレスの表示名がない場合は、代わりにメールアドレス全体を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9ae25-128">If there is no display name for an address on inbound mail, the entire email address should be used instead.</span></span> <span data-ttu-id="9ae25-129">アドレスの種類は、常に SMTP です。</span><span class="sxs-lookup"><span data-stu-id="9ae25-129">The address type is always SMTP.</span></span>
  
<span data-ttu-id="9ae25-130">受信者のプロパティは、MAPI メッセージの受信者テーブルから取得されます。sender プロパティは、メッセージ自体から取得されます。</span><span class="sxs-lookup"><span data-stu-id="9ae25-130">Recipient properties are taken from the MAPI message's recipient table; sender properties are taken from the message itself.</span></span>
  

