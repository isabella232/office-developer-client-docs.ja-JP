---
title: アドレス帳の制限
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6ace8c03-45a7-484b-8c12-516ac0e40dc2
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: b8ad765a2bbd3aafd87a7eff79993978816729b2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799648"
---
# <a name="address-book-restrictions"></a><span data-ttu-id="50a33-103">アドレス帳の制限</span><span class="sxs-lookup"><span data-stu-id="50a33-103">Address Book Restrictions</span></span>

  
  
<span data-ttu-id="50a33-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="50a33-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="50a33-105">アドレス帳プロバイダーがそのコンテナーのコンテンツ テーブルに 3 種類の制限をサポートするために必要です。</span><span class="sxs-lookup"><span data-stu-id="50a33-105">Address book providers are required to support three types of restrictions on the contents tables of their containers:</span></span>
  
- <span data-ttu-id="50a33-106">あいまいな名前のプロパティの制限</span><span class="sxs-lookup"><span data-stu-id="50a33-106">Ambiguous name property restrictions</span></span>
    
- <span data-ttu-id="50a33-107">インスタンスのキー プロパティの制限</span><span class="sxs-lookup"><span data-stu-id="50a33-107">Instance key property restrictions</span></span>
    
- <span data-ttu-id="50a33-108">プレフィックスが付けられた表示名のコンテンツの制限</span><span class="sxs-lookup"><span data-stu-id="50a33-108">Prefixed display name content restrictions</span></span>
    
<span data-ttu-id="50a33-109">あいまいな名前の制限とは、アドレス帳コンテナー内のエントリに受信者の名前を一致するように**PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) プロパティを使用してプロパティの制限事項です。</span><span class="sxs-lookup"><span data-stu-id="50a33-109">Ambiguous name restrictions are property restrictions using the **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) property to match recipient names with entries in address book containers.</span></span> <span data-ttu-id="50a33-110">**PR_ANR**プロパティの制限は、「最適な推測」アドレス帳プロバイダーがそのコンテナーに最も適した一致するプロパティを選択する、検索の型です。</span><span class="sxs-lookup"><span data-stu-id="50a33-110">The **PR_ANR** property restriction is a "best guess" type of search whereby address book providers can choose the matching property that works best for their container.</span></span> <span data-ttu-id="50a33-111">たとえば、1 つのアドレス帳プロバイダーを実装**PR_ANR**制限各コンテナーのエントリの**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) プロパティと一致する受信者の名前で別のプロバイダーは、 **PR_DISPLAY を使用して可能性がありますが、名**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))。</span><span class="sxs-lookup"><span data-stu-id="50a33-111">For example, one address book provider might implement the **PR_ANR** restriction by matching recipient names against the **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) property of each container entry whereas another provider might use **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span></span>
  
<span data-ttu-id="50a33-112">MAPI では、 **PR_ANR**の制限の実装が十分なパフォーマンスとユーザーの満足度の間でバランスを取ることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="50a33-112">MAPI recommends that implementations of the **PR_ANR** restriction strike a balance between adequate performance and user satisfaction.</span></span> <span data-ttu-id="50a33-113">アドレス帳プロバイダーなどの制限を実装する場合、ユーザーの満足度が侵害される可能性が少なすぎるか多すぎるの一致が見つかったことです。</span><span class="sxs-lookup"><span data-stu-id="50a33-113">User satisfaction can be compromised when an address book provider implements the restriction in such a way that too few or too many matches are found.</span></span> <span data-ttu-id="50a33-114">いくつかのアドレス帳プロバイダー] ダイアログ ボックスで表示可能な項目はありませんが、あいまいな名前の制限に一致することができます識別、または共通名と呼ばれるものをサポートします。</span><span class="sxs-lookup"><span data-stu-id="50a33-114">Some address book providers support what is known as a distinguished, or common, name that is not displayable in a dialog box but can match an ambiguous name restriction.</span></span> 
  
<span data-ttu-id="50a33-115">単語、単語のすべてを含む任意のエントリに一致する受信者の表示名を解析する一般的な実装があります。</span><span class="sxs-lookup"><span data-stu-id="50a33-115">A typical implementation might be to parse the recipient's display name into words, matching any entry that contains all of the words.</span></span> <span data-ttu-id="50a33-116">位置の単語を小文字の区別などの詳細に注意、隣接していない複数の単語が一致するかどうか、および区切り文字の選択を変更できます。</span><span class="sxs-lookup"><span data-stu-id="50a33-116">Attention to details such as sensitivity to word position, whether nonconsecutive words are matched, and the choice of separator characters can vary.</span></span> <span data-ttu-id="50a33-117">などを解決するのには名前が「部品 L」の場合は、一般的な**PR_ANR**制限は次のエントリと一致する選択します。</span><span class="sxs-lookup"><span data-stu-id="50a33-117">For example, if the name to be resolved is "Bill L," a typical **PR_ANR** restriction would select the following entries as matching:</span></span> 
  
- <span data-ttu-id="50a33-118">Billy Larson</span><span class="sxs-lookup"><span data-stu-id="50a33-118">Billy Larson</span></span>
    
- <span data-ttu-id="50a33-119">Bill Lee</span><span class="sxs-lookup"><span data-stu-id="50a33-119">Bill Lee</span></span>
    
- <span data-ttu-id="50a33-120">手形ローガン Jr。</span><span class="sxs-lookup"><span data-stu-id="50a33-120">Bill Logan Jr.</span></span> 
    
- <span data-ttu-id="50a33-121">Sam Bill Lee</span><span class="sxs-lookup"><span data-stu-id="50a33-121">Sam Bill Lee</span></span>
    
<span data-ttu-id="50a33-122">インスタンス キーの制限、または、[プロパティ制限の**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) は、MAPI テーブルを表示するためにクライアント アプリケーションで使用されているリスト ボックスの実装で使用されます。</span><span class="sxs-lookup"><span data-stu-id="50a33-122">Instance key restrictions, or **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property restrictions, are used in the implementation of list boxes that are used in client applications for viewing MAPI tables.</span></span> <span data-ttu-id="50a33-123">いくつかのリスト ボックスの実装には、ユーザーが複数選択するには、上にスクロールができるようにまたは、最初の項目に戻り値を選択します。</span><span class="sxs-lookup"><span data-stu-id="50a33-123">Some list box implementations allow users to make multiple selections, scroll up or down, and return to the first item selected.</span></span> <span data-ttu-id="50a33-124">この動作を実装するには、クライアントは、 [IMAPITable::FindRow](imapitable-findrow.md)、 **PR_INSTANCE_KEY**プロパティにプロパティ制約をメソッドに渡すを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="50a33-124">To implement this behavior, clients call [IMAPITable::FindRow](imapitable-findrow.md), passing a property restriction on the **PR_INSTANCE_KEY** property to the method.</span></span> <span data-ttu-id="50a33-125">アドレス帳プロバイダーがこの制限をサポートするために必要です。</span><span class="sxs-lookup"><span data-stu-id="50a33-125">Address book providers are required to support this restriction.</span></span> 
  
<span data-ttu-id="50a33-126">テーブルの表示のためのリスト ボックスのほかの機能は、先頭の文字のセットに基づいたカーソルを配置することです。</span><span class="sxs-lookup"><span data-stu-id="50a33-126">Another feature of list boxes used for table viewing is the ability to position the cursor based on a set of prefix characters.</span></span> <span data-ttu-id="50a33-127">ユーザーは、先頭の文字の入力を開始するとクライアントはこれらの文字で始まる最初の項目にカーソルを移動します。</span><span class="sxs-lookup"><span data-stu-id="50a33-127">As the user starts typing prefix characters, the client moves the cursor to the first item that begins with these characters.</span></span> <span data-ttu-id="50a33-128">クライアントは、 **PR_DISPLAY_NAME**プロパティと FL_PREFIX あいまいレベルに基づいて、コンテンツの制限でこの機能を実装します。</span><span class="sxs-lookup"><span data-stu-id="50a33-128">Clients implement this feature with a content restriction based on the **PR_DISPLAY_NAME** property and the FL_PREFIX fuzzy level.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="50a33-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="50a33-129">See also</span></span>



[<span data-ttu-id="50a33-130">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="50a33-130">MAPI Tables</span></span>](mapi-tables.md)

