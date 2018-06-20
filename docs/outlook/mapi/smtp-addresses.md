---
title: SMTP アドレス
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 42015740-a94f-4628-bf32-b7fc2fdb9ff6
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 9bc77e3226066dc88bbaf4f4efc324825add8919
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803970"
---
# <a name="smtp-addresses"></a><span data-ttu-id="b14f5-103">SMTP アドレス</span><span class="sxs-lookup"><span data-stu-id="b14f5-103">SMTP Addresses</span></span>

  
  
<span data-ttu-id="b14f5-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b14f5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b14f5-105">SMTP 電子メール アドレスの形式は、RFC 822 で定義されます。</span><span class="sxs-lookup"><span data-stu-id="b14f5-105">The format of SMTP email addresses is defined in RFC 822.</span></span> <span data-ttu-id="b14f5-106">MAPI コンポーネントでは、その標準に準拠している任意のアドレスを処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b14f5-106">MAPI components should handle any address that complies with that standard.</span></span> <span data-ttu-id="b14f5-107">ただし、RFC 822 アドレス MAPI アドレスを記述する方式の特定のフォームがあります。</span><span class="sxs-lookup"><span data-stu-id="b14f5-107">However, there is a particular form of RFC 822 address that best encodes MAPI addresses:</span></span>
  
 <span data-ttu-id="b14f5-108">_表示名_**\<** _e メール アドレス_**\>**</span><span class="sxs-lookup"><span data-stu-id="b14f5-108">_display-name_ **\<** _email-address_ **\>**</span></span>
  
<span data-ttu-id="b14f5-109">山かっこでは、リテラル文字列として含まれています。</span><span class="sxs-lookup"><span data-stu-id="b14f5-109">The angle brackets are included as literals.</span></span> <span data-ttu-id="b14f5-110">空白は、共通の表示名です。それらを引用されません必要があります。</span><span class="sxs-lookup"><span data-stu-id="b14f5-110">Blanks are common in display names; they need not be quoted.</span></span> <span data-ttu-id="b14f5-111">一般的なアドレスは、このいずれか、RFC 1521 の共同のいずれかに属するのようになります。</span><span class="sxs-lookup"><span data-stu-id="b14f5-111">A typical address might look like this one, which belongs to one of the coauthors of RFC 1521:</span></span>
  
<span data-ttu-id="b14f5-112">Nathaniel Borenstein \<nsb@bellcore.com\></span><span class="sxs-lookup"><span data-stu-id="b14f5-112">Nathaniel Borenstein \<nsb@bellcore.com\></span></span>
  
<span data-ttu-id="b14f5-113">表示名には、次のように、SMTP アドレスに特別な意味がある文字が含まれている場合\<または @、全体の表示名を二重引用符で囲む必要があります。</span><span class="sxs-lookup"><span data-stu-id="b14f5-113">If the display name contains characters that have special meaning in SMTP addresses, such as \< or @, the entire display name should be enclosed in double quotes.</span></span> <span data-ttu-id="b14f5-114">、送信メールの名が 255 文字を超えるプラスの電子メール アドレスの長さの合計を表示する場合、表示名を削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b14f5-114">On outbound mail, if the total length of the email address plus display name exceeds 255 characters, the display name should be dropped.</span></span>
  
<span data-ttu-id="b14f5-115">SMTP アドレスの部分は、MAPI のプロパティに次のようにマップします。</span><span class="sxs-lookup"><span data-stu-id="b14f5-115">The parts of an SMTP address map into MAPI properties as follows:</span></span>
  
|<span data-ttu-id="b14f5-116">**SMTP アドレスのコンポーネント**</span><span class="sxs-lookup"><span data-stu-id="b14f5-116">**SMTP address component**</span></span>|<span data-ttu-id="b14f5-117">**MAPI プロパティ**</span><span class="sxs-lookup"><span data-stu-id="b14f5-117">**MAPI property**</span></span>|
|:-----|:-----|
| <span data-ttu-id="b14f5-118">すべての受信者の_表示名_</span><span class="sxs-lookup"><span data-stu-id="b14f5-118">_display-name_ for all recipients</span></span>  <br/> |<span data-ttu-id="b14f5-119">**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b14f5-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |
| <span data-ttu-id="b14f5-120">フィールドの_表示名_</span><span class="sxs-lookup"><span data-stu-id="b14f5-120">_display-name_ for From field</span></span>  <br/> |<span data-ttu-id="b14f5-121">**PR_SENDER_NAME**([PidTagSenderName](pidtagsendername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b14f5-121">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span></span>  <br/> |
| <span data-ttu-id="b14f5-122">[送信者] フィールドの_表示名_</span><span class="sxs-lookup"><span data-stu-id="b14f5-122">_display-name_ for Sender field</span></span>  <br/> |<span data-ttu-id="b14f5-123">**PR_SENT_REPRESENTING_NAME**([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b14f5-123">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span></span>  <br/> |
| <span data-ttu-id="b14f5-124">_電子メール アドレス_</span><span class="sxs-lookup"><span data-stu-id="b14f5-124">_email-address_</span></span> <br/> |<span data-ttu-id="b14f5-125">**PR_EMAIL_ADDRESS**([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b14f5-125">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="b14f5-126">暗黙に、常に"SMTP"</span><span class="sxs-lookup"><span data-stu-id="b14f5-126">implicit, always "SMTP"</span></span>  <br/> |<span data-ttu-id="b14f5-127">**PR_ADDRTYPE**([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b14f5-127">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>  <br/> |
   
<span data-ttu-id="b14f5-128">受信メールのアドレスの表示名がない場合は、全体の電子メール アドレスを代わりに使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b14f5-128">If there is no display name for an address on inbound mail, the entire email address should be used instead.</span></span> <span data-ttu-id="b14f5-129">アドレス タイプは SMTP では常にします。</span><span class="sxs-lookup"><span data-stu-id="b14f5-129">The address type is always SMTP.</span></span>
  
<span data-ttu-id="b14f5-130">受信者のプロパティは、MAPI メッセージの受信者テーブルから取得されます。センダーのプロパティは、メッセージ自体から取得されます。</span><span class="sxs-lookup"><span data-stu-id="b14f5-130">Recipient properties are taken from the MAPI message's recipient table; sender properties are taken from the message itself.</span></span>
  

