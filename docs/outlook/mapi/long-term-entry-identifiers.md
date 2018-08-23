---
title: 長期エントリ ID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a514275e-40c2-48db-8072-1dfc392a7ac6
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: e624ab4f39ef5a5385119779b0780ee7173a3ee7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586922"
---
# <a name="long-term-entry-identifiers"></a><span data-ttu-id="2f70d-103">長期エントリ ID</span><span class="sxs-lookup"><span data-stu-id="2f70d-103">Long-Term Entry Identifiers</span></span>

  
  
<span data-ttu-id="2f70d-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2f70d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2f70d-105">長期のエントリ id は、オブジェクトには、長寿命を持つ識別子が必要な場合、オブジェクトへのサービス プロバイダーによって割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="2f70d-105">A long-term entry identifier is assigned by a service provider to an object when an object requires an identifier with a prolonged lifespan.</span></span> <span data-ttu-id="2f70d-106">長期のエントリ id は、常に有効期間は数週間または数か月と、プロバイダーによって、他のワークステーションで有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="2f70d-106">Long-term entry identifiers are always valid for weeks or months and can be valid on other workstations, depending on the provider.</span></span> <span data-ttu-id="2f70d-107">カスタム受信者のアドレス帳のプロバイダーによって作成された長期的な識別子は、汎用的に有効です。</span><span class="sxs-lookup"><span data-stu-id="2f70d-107">The long-term identifiers created by address book providers for custom recipients are universally valid.</span></span> 
  
<span data-ttu-id="2f70d-108">長期のエントリ id に割り当てられているメールの保存場所、フォルダー、メッセージ、アドレス帳コンテナー、メッセージング ユーザー、および配布リストです。</span><span class="sxs-lookup"><span data-stu-id="2f70d-108">Long-term entry identifiers are assigned to message stores, folders, messages, address book containers, messaging users, and distribution lists.</span></span> <span data-ttu-id="2f70d-109">クライアント アプリケーションは、これらのオブジェクトの[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを呼び出すときは、常に長期のエントリ id が返されるです。</span><span class="sxs-lookup"><span data-stu-id="2f70d-109">When client applications call the [IMAPIProp::GetProps](imapiprop-getprops.md) method of these objects, it is always a long-term entry identifier that is returned.</span></span> 
  
<span data-ttu-id="2f70d-110">長期のエントリ id は、現在のプロファイル内のすべてのメッセージ ストア間で一意でなければなりませんしたがって、メッセージまたはフォルダーをコピー 1 つのメッセージ ・ ストアから別に割り当てる必要があります新しいエントリの識別子です。</span><span class="sxs-lookup"><span data-stu-id="2f70d-110">Long-term entry identifiers must be unique across all message stores in the active profile; therefore, when a message or folder is copied from one message store to another, it must be assigned a new entry identifier.</span></span> <span data-ttu-id="2f70d-111">メッセージ ストアのオブジェクトを移動すると、移動を実装しているメッセージ ストア プロバイダーは、元のエントリ id が有効なままかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="2f70d-111">When a message store object is moved, the message store provider that implements the move determines whether the original entry identifier will remain valid.</span></span> <span data-ttu-id="2f70d-112">サービス プロバイダーによっては、移動されたオブジェクトに新しいエントリの識別子を割り当てるそうでないです。</span><span class="sxs-lookup"><span data-stu-id="2f70d-112">Some service providers assign new entry identifiers to moved objects; others do not.</span></span> <span data-ttu-id="2f70d-113">変更がある場合は、新しいエントリの識別子は、移動が通知されるときに、クライアントに渡される情報に含まれます。</span><span class="sxs-lookup"><span data-stu-id="2f70d-113">If there is a change, the new entry identifier will be included in the information passed to clients when they are notified of the move.</span></span> 
  
<span data-ttu-id="2f70d-114">通常、メッセージ ストア プロバイダーは、フォルダーを移動する際、次の動作を実装します。</span><span class="sxs-lookup"><span data-stu-id="2f70d-114">Typically, message store providers implement the following behavior when they move folders:</span></span>
  
- <span data-ttu-id="2f70d-115">フォルダー移動すると、1 つのメッセージ ・ ストアから別の種類の別のストアに変更するのには、エントリ id が保証されます。</span><span class="sxs-lookup"><span data-stu-id="2f70d-115">When a folder is moved from one message store to another store of a different type, the entry identifier is guaranteed to change.</span></span>
    
- <span data-ttu-id="2f70d-116">フォルダー移動すると、1 つのメッセージ ・ ストアから同じ種類の別のストアにほとんどのエントリ id を変更します。</span><span class="sxs-lookup"><span data-stu-id="2f70d-116">When a folder is moved from one message store to another store of the same type, the entry identifier almost always changes.</span></span>
    
- <span data-ttu-id="2f70d-117">同じメッセージ ・ ストア内の別の場所にフォルダーを移動すると、エントリ id は可能性がありますか、変わらないことがあります、メッセージ ストア プロバイダーによって。</span><span class="sxs-lookup"><span data-stu-id="2f70d-117">When a folder is moved to another location within the same message store, the entry identifier might or might not change, depending on the message store provider.</span></span>
    
<span data-ttu-id="2f70d-118">通常、親フォルダーを変更することがなく、フォルダーの名前を変更しても、エントリ id を変更するのには発生しません。</span><span class="sxs-lookup"><span data-stu-id="2f70d-118">Renaming a folder without changing its parent folder usually does not cause the entry identifier to change.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2f70d-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="2f70d-119">See also</span></span>



[<span data-ttu-id="2f70d-120">MAPI エントリの識別子</span><span class="sxs-lookup"><span data-stu-id="2f70d-120">MAPI Entry Identifiers</span></span>](mapi-entry-identifiers.md)

