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
# <a name="address-book-restrictions"></a><span data-ttu-id="e41af-103">アドレス帳の制限</span><span class="sxs-lookup"><span data-stu-id="e41af-103">Address Book Restrictions</span></span>

  
  
<span data-ttu-id="e41af-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e41af-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e41af-105">アドレス帳プロバイダーは、コンテナーのコンテンツ テーブルに対する 3 種類の制限をサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e41af-105">Address book providers are required to support three types of restrictions on the contents tables of their containers:</span></span>
  
- <span data-ttu-id="e41af-106">あいまいな名前プロパティの制限</span><span class="sxs-lookup"><span data-stu-id="e41af-106">Ambiguous name property restrictions</span></span>
    
- <span data-ttu-id="e41af-107">インスタンス キープロパティの制限</span><span class="sxs-lookup"><span data-stu-id="e41af-107">Instance key property restrictions</span></span>
    
- <span data-ttu-id="e41af-108">プレフィックス付き表示名のコンテンツ制限</span><span class="sxs-lookup"><span data-stu-id="e41af-108">Prefixed display name content restrictions</span></span>
    
<span data-ttu-id="e41af-109">あいまいな名前の制限は **、PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) プロパティを使用して、受信者名とアドレス帳コンテナー内のエントリを一致するプロパティの制限です。</span><span class="sxs-lookup"><span data-stu-id="e41af-109">Ambiguous name restrictions are property restrictions using the **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) property to match recipient names with entries in address book containers.</span></span> <span data-ttu-id="e41af-110">この **PR_ANR** プロパティの制限は、アドレス帳プロバイダーがコンテナーに最適な一致するプロパティを選択できる、"最適な推測" 型の検索です。</span><span class="sxs-lookup"><span data-stu-id="e41af-110">The **PR_ANR** property restriction is a "best guess" type of search whereby address book providers can choose the matching property that works best for their container.</span></span> <span data-ttu-id="e41af-111">たとえば、あるアドレス帳プロバイダーは、受信者名を各コンテナー エントリの **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) プロパティと照合して PR_ANR 制限を実装します。一方、別のプロバイダーは **PR_DISPLAY_NAME** ([PidTagDisplayName)](pidtagdisplayname-canonical-property.md)を使用する場合があります。</span><span class="sxs-lookup"><span data-stu-id="e41af-111">For example, one address book provider might implement the **PR_ANR** restriction by matching recipient names against the **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) property of each container entry whereas another provider might use **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span></span>
  
<span data-ttu-id="e41af-112">MAPI では、適切なパフォーマンスとユーザー **PR_ANRの** バランスを取る制限の実装をお勧めします。</span><span class="sxs-lookup"><span data-stu-id="e41af-112">MAPI recommends that implementations of the **PR_ANR** restriction strike a balance between adequate performance and user satisfaction.</span></span> <span data-ttu-id="e41af-113">アドレス帳プロバイダーが制限を実装して、一致する数が少なすぎたり、多すぎたりする場合、ユーザーの満足度が損なわれる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="e41af-113">User satisfaction can be compromised when an address book provider implements the restriction in such a way that too few or too many matches are found.</span></span> <span data-ttu-id="e41af-114">一部のアドレス帳プロバイダーは、ダイアログ ボックスでは表示できないが、あいまいな名前の制限に一致する識別名または一般的な名前と呼ばれる名前をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="e41af-114">Some address book providers support what is known as a distinguished, or common, name that is not displayable in a dialog box but can match an ambiguous name restriction.</span></span> 
  
<span data-ttu-id="e41af-115">一般的な実装は、受信者の表示名を単語に解析し、すべての単語を含むエントリと一致する場合があります。</span><span class="sxs-lookup"><span data-stu-id="e41af-115">A typical implementation might be to parse the recipient's display name into words, matching any entry that contains all of the words.</span></span> <span data-ttu-id="e41af-116">単語の位置に対する感度、不起訴語が一致するかどうか、区切り文字の選択など、詳細に注意してください。</span><span class="sxs-lookup"><span data-stu-id="e41af-116">Attention to details such as sensitivity to word position, whether nonconsecutive words are matched, and the choice of separator characters can vary.</span></span> <span data-ttu-id="e41af-117">たとえば、解決する名前が "Bill L" の場合、一般的な制限PR_ANR一致として次のエントリが選択されます。</span><span class="sxs-lookup"><span data-stu-id="e41af-117">For example, if the name to be resolved is "Bill L," a typical **PR_ANR** restriction would select the following entries as matching:</span></span> 
  
- <span data-ttu-id="e41af-118">ビリー・ラーソン</span><span class="sxs-lookup"><span data-stu-id="e41af-118">Billy Larson</span></span>
    
- <span data-ttu-id="e41af-119">Bill Lee</span><span class="sxs-lookup"><span data-stu-id="e41af-119">Bill Lee</span></span>
    
- <span data-ttu-id="e41af-120">Bill Logan Jr.</span><span class="sxs-lookup"><span data-stu-id="e41af-120">Bill Logan Jr.</span></span> 
    
- <span data-ttu-id="e41af-121">Sam Bill Lee</span><span class="sxs-lookup"><span data-stu-id="e41af-121">Sam Bill Lee</span></span>
    
<span data-ttu-id="e41af-122">MAPI テーブルを表示するためにクライアント アプリケーションで使用されるリスト ボックスの実装では、インスタンス キーの制限 **(PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) プロパティの制限が使用されます。</span><span class="sxs-lookup"><span data-stu-id="e41af-122">Instance key restrictions, or **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property restrictions, are used in the implementation of list boxes that are used in client applications for viewing MAPI tables.</span></span> <span data-ttu-id="e41af-123">一部のリスト ボックスの実装では、ユーザーは複数の選択を行い、上下にスクロールして、選択した最初の項目に戻る場合があります。</span><span class="sxs-lookup"><span data-stu-id="e41af-123">Some list box implementations allow users to make multiple selections, scroll up or down, and return to the first item selected.</span></span> <span data-ttu-id="e41af-124">この動作を実装するために、クライアントは [IMAPITable::FindRow](imapitable-findrow.md)を呼び出し、PR_INSTANCE_KEY **プロパティの** プロパティ制限をメソッドに渡します。</span><span class="sxs-lookup"><span data-stu-id="e41af-124">To implement this behavior, clients call [IMAPITable::FindRow](imapitable-findrow.md), passing a property restriction on the **PR_INSTANCE_KEY** property to the method.</span></span> <span data-ttu-id="e41af-125">この制限をサポートするには、アドレス帳プロバイダーが必要です。</span><span class="sxs-lookup"><span data-stu-id="e41af-125">Address book providers are required to support this restriction.</span></span> 
  
<span data-ttu-id="e41af-126">テーブル表示に使用されるリスト ボックスのもう 1 つの機能は、プレフィックス文字のセットに基づいてカーソルを配置する機能です。</span><span class="sxs-lookup"><span data-stu-id="e41af-126">Another feature of list boxes used for table viewing is the ability to position the cursor based on a set of prefix characters.</span></span> <span data-ttu-id="e41af-127">ユーザーがプレフィックス文字の入力を開始すると、クライアントはカーソルをこれらの文字で始まる最初の項目に移動します。</span><span class="sxs-lookup"><span data-stu-id="e41af-127">As the user starts typing prefix characters, the client moves the cursor to the first item that begins with these characters.</span></span> <span data-ttu-id="e41af-128">クライアントは、PR_DISPLAY_NAME プロパティとファジー レベルに基 **FL_PREFIX** この機能を実装します。</span><span class="sxs-lookup"><span data-stu-id="e41af-128">Clients implement this feature with a content restriction based on the **PR_DISPLAY_NAME** property and the FL_PREFIX fuzzy level.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e41af-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="e41af-129">See also</span></span>



[<span data-ttu-id="e41af-130">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="e41af-130">MAPI Tables</span></span>](mapi-tables.md)

