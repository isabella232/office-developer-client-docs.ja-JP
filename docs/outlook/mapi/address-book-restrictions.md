---
title: アドレス帳の制限
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6ace8c03-45a7-484b-8c12-516ac0e40dc2
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 7419c174c1f68653794c2dbd836577e8dd3e596e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432801"
---
# <a name="address-book-restrictions"></a><span data-ttu-id="1a75d-103">アドレス帳の制限</span><span class="sxs-lookup"><span data-stu-id="1a75d-103">Address Book Restrictions</span></span>

  
  
<span data-ttu-id="1a75d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1a75d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1a75d-105">アドレス帳プロバイダーは、コンテナーのコンテンツテーブルに対して3種類の制限をサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="1a75d-105">Address book providers are required to support three types of restrictions on the contents tables of their containers:</span></span>
  
- <span data-ttu-id="1a75d-106">あいまいな名前のプロパティの制限</span><span class="sxs-lookup"><span data-stu-id="1a75d-106">Ambiguous name property restrictions</span></span>
    
- <span data-ttu-id="1a75d-107">インスタンスのキープロパティの制限</span><span class="sxs-lookup"><span data-stu-id="1a75d-107">Instance key property restrictions</span></span>
    
- <span data-ttu-id="1a75d-108">プレフィックス付きの表示名コンテンツの制限</span><span class="sxs-lookup"><span data-stu-id="1a75d-108">Prefixed display name content restrictions</span></span>
    
<span data-ttu-id="1a75d-109">あいまいな名前の制限は、 **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) プロパティを使用してアドレス帳コンテナー内のエントリで受信者名を一致させるプロパティの制限です。</span><span class="sxs-lookup"><span data-stu-id="1a75d-109">Ambiguous name restrictions are property restrictions using the **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) property to match recipient names with entries in address book containers.</span></span> <span data-ttu-id="1a75d-110">**PR_ANR**プロパティの制限は、"最適な推測" の種類の検索として、アドレス帳プロバイダーが自分のコンテナーに最適な対応するプロパティを選択できるようにするものです。</span><span class="sxs-lookup"><span data-stu-id="1a75d-110">The **PR_ANR** property restriction is a "best guess" type of search whereby address book providers can choose the matching property that works best for their container.</span></span> <span data-ttu-id="1a75d-111">たとえば、1つのアドレス帳プロバイダーは、受信者名を各コンテナーエントリの**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) プロパティと一致させることによって**PR_ANR**制限を実装し、別のプロバイダーが PR_DISPLAY を使用する場合があります。 **_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1a75d-111">For example, one address book provider might implement the **PR_ANR** restriction by matching recipient names against the **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) property of each container entry whereas another provider might use **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span></span>
  
<span data-ttu-id="1a75d-112">MAPI では、 **PR_ANR**制限の実装によって、十分なパフォーマンスとユーザーの満足度のバランスを取ることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="1a75d-112">MAPI recommends that implementations of the **PR_ANR** restriction strike a balance between adequate performance and user satisfaction.</span></span> <span data-ttu-id="1a75d-113">アドレス帳プロバイダーが、一致する件数が少なすぎる、または見つからないような制限を実装すると、ユーザーの満足度が低下する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="1a75d-113">User satisfaction can be compromised when an address book provider implements the restriction in such a way that too few or too many matches are found.</span></span> <span data-ttu-id="1a75d-114">アドレス帳プロバイダーの中には、識別可能な名前の制限に一致していても、ダイアログボックスには設定できない、識別可能な名前として知られているものをサポートしているものがあります。</span><span class="sxs-lookup"><span data-stu-id="1a75d-114">Some address book providers support what is known as a distinguished, or common, name that is not displayable in a dialog box but can match an ambiguous name restriction.</span></span> 
  
<span data-ttu-id="1a75d-115">一般的な実装では、受信者の表示名を単語で解析して、すべての単語を含むエントリに一致させることができます。</span><span class="sxs-lookup"><span data-stu-id="1a75d-115">A typical implementation might be to parse the recipient's display name into words, matching any entry that contains all of the words.</span></span> <span data-ttu-id="1a75d-116">nonconsecutive の単語が一致しているかどうか、単語の位置に対する感度などの詳細に注意してください。区切り文字の選択はさまざまです。</span><span class="sxs-lookup"><span data-stu-id="1a75d-116">Attention to details such as sensitivity to word position, whether nonconsecutive words are matched, and the choice of separator characters can vary.</span></span> <span data-ttu-id="1a75d-117">たとえば、解決される名前が "Bill L" の場合、一般的な**PR_ANR**制限は、次のエントリを一致として選択します。</span><span class="sxs-lookup"><span data-stu-id="1a75d-117">For example, if the name to be resolved is "Bill L," a typical **PR_ANR** restriction would select the following entries as matching:</span></span> 
  
- <span data-ttu-id="1a75d-118">Billy Larson</span><span class="sxs-lookup"><span data-stu-id="1a75d-118">Billy Larson</span></span>
    
- <span data-ttu-id="1a75d-119">Bill Lee</span><span class="sxs-lookup"><span data-stu-id="1a75d-119">Bill Lee</span></span>
    
- <span data-ttu-id="1a75d-120">Bill logan。</span><span class="sxs-lookup"><span data-stu-id="1a75d-120">Bill Logan Jr.</span></span> 
    
- <span data-ttu-id="1a75d-121">Sam Bill Lee</span><span class="sxs-lookup"><span data-stu-id="1a75d-121">Sam Bill Lee</span></span>
    
<span data-ttu-id="1a75d-122">インスタンスキー制限または**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) プロパティの制限は、MAPI テーブルを表示するためにクライアントアプリケーションで使用されるリストボックスの実装で使用されます。</span><span class="sxs-lookup"><span data-stu-id="1a75d-122">Instance key restrictions, or **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property restrictions, are used in the implementation of list boxes that are used in client applications for viewing MAPI tables.</span></span> <span data-ttu-id="1a75d-123">リストボックスの実装によっては、複数の選択を行ったり、上下にスクロールしたり、選択した最初の項目に戻ることができます。</span><span class="sxs-lookup"><span data-stu-id="1a75d-123">Some list box implementations allow users to make multiple selections, scroll up or down, and return to the first item selected.</span></span> <span data-ttu-id="1a75d-124">この動作を実装するために、クライアントは[IMAPITable:: FindRow](imapitable-findrow.md)を呼び出し、 **PR_INSTANCE_KEY**プロパティのプロパティ制限をメソッドに渡します。</span><span class="sxs-lookup"><span data-stu-id="1a75d-124">To implement this behavior, clients call [IMAPITable::FindRow](imapitable-findrow.md), passing a property restriction on the **PR_INSTANCE_KEY** property to the method.</span></span> <span data-ttu-id="1a75d-125">この制限をサポートするには、アドレス帳プロバイダーが必要です。</span><span class="sxs-lookup"><span data-stu-id="1a75d-125">Address book providers are required to support this restriction.</span></span> 
  
<span data-ttu-id="1a75d-126">表の表示に使用されるリストボックスのもう1つの機能は、一連の先頭文字に基づいてカーソルを配置する機能です。</span><span class="sxs-lookup"><span data-stu-id="1a75d-126">Another feature of list boxes used for table viewing is the ability to position the cursor based on a set of prefix characters.</span></span> <span data-ttu-id="1a75d-127">ユーザーがプレフィックス文字の入力を開始すると、クライアントは、次の文字で始まる最初の項目にカーソルを移動します。</span><span class="sxs-lookup"><span data-stu-id="1a75d-127">As the user starts typing prefix characters, the client moves the cursor to the first item that begins with these characters.</span></span> <span data-ttu-id="1a75d-128">クライアントは、 **PR_DISPLAY_NAME**プロパティと FL_PREFIX あいまいレベルに基づくコンテンツ制限を使用してこの機能を実装します。</span><span class="sxs-lookup"><span data-stu-id="1a75d-128">Clients implement this feature with a content restriction based on the **PR_DISPLAY_NAME** property and the FL_PREFIX fuzzy level.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1a75d-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="1a75d-129">See also</span></span>



[<span data-ttu-id="1a75d-130">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="1a75d-130">MAPI Tables</span></span>](mapi-tables.md)

