---
title: Long-Termエントリ識別子
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a514275e-40c2-48db-8072-1dfc392a7ac6
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: b65656992681618aa8a1c53217bdd7101bc2502b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409224"
---
# <a name="long-term-entry-identifiers"></a><span data-ttu-id="20b87-103">Long-Termエントリ識別子</span><span class="sxs-lookup"><span data-stu-id="20b87-103">Long-Term Entry Identifiers</span></span>

  
  
<span data-ttu-id="20b87-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="20b87-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="20b87-105">長期エントリ識別子は、オブジェクトが長期間の寿命を持つ識別子を必要とする場合に、サービス プロバイダーによってオブジェクトに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="20b87-105">A long-term entry identifier is assigned by a service provider to an object when an object requires an identifier with a prolonged lifespan.</span></span> <span data-ttu-id="20b87-106">長期エントリ識別子は、常に数週間または数か月有効であり、プロバイダーに応じて他のワークステーションで有効な場合があります。</span><span class="sxs-lookup"><span data-stu-id="20b87-106">Long-term entry identifiers are always valid for weeks or months and can be valid on other workstations, depending on the provider.</span></span> <span data-ttu-id="20b87-107">カスタム受信者のアドレス帳プロバイダーによって作成された長期的な識別子は、汎用的に有効です。</span><span class="sxs-lookup"><span data-stu-id="20b87-107">The long-term identifiers created by address book providers for custom recipients are universally valid.</span></span> 
  
<span data-ttu-id="20b87-108">長期エントリ識別子は、メッセージ ストア、フォルダー、メッセージ、アドレス帳コンテナー、メッセージング ユーザー、配布リストに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="20b87-108">Long-term entry identifiers are assigned to message stores, folders, messages, address book containers, messaging users, and distribution lists.</span></span> <span data-ttu-id="20b87-109">クライアント アプリケーションがこれらのオブジェクト [の IMAPIProp::GetProps](imapiprop-getprops.md) メソッドを呼び出す場合、常に返される長期エントリ識別子です。</span><span class="sxs-lookup"><span data-stu-id="20b87-109">When client applications call the [IMAPIProp::GetProps](imapiprop-getprops.md) method of these objects, it is always a long-term entry identifier that is returned.</span></span> 
  
<span data-ttu-id="20b87-110">長期エントリ識別子は、アクティブ なプロファイル内のすべてのメッセージ ストアで一意である必要があります。したがって、あるメッセージ ストアから別のメッセージ ストアにメッセージまたはフォルダーをコピーする場合は、新しいエントリ識別子を割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="20b87-110">Long-term entry identifiers must be unique across all message stores in the active profile; therefore, when a message or folder is copied from one message store to another, it must be assigned a new entry identifier.</span></span> <span data-ttu-id="20b87-111">メッセージ ストア オブジェクトを移動すると、移動を実装するメッセージ ストア プロバイダーによって、元のエントリ識別子が有効なままであるかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="20b87-111">When a message store object is moved, the message store provider that implements the move determines whether the original entry identifier will remain valid.</span></span> <span data-ttu-id="20b87-112">一部のサービス プロバイダーは、移動したオブジェクトに新しいエントリ識別子を割り当てる。他のユーザーはそうではありません。</span><span class="sxs-lookup"><span data-stu-id="20b87-112">Some service providers assign new entry identifiers to moved objects; others do not.</span></span> <span data-ttu-id="20b87-113">変更がある場合は、移動の通知を受け取ったクライアントに渡される情報に新しいエントリ識別子が含まれます。</span><span class="sxs-lookup"><span data-stu-id="20b87-113">If there is a change, the new entry identifier will be included in the information passed to clients when they are notified of the move.</span></span> 
  
<span data-ttu-id="20b87-114">通常、メッセージ ストア プロバイダーはフォルダーを移動するときに次の動作を実装します。</span><span class="sxs-lookup"><span data-stu-id="20b87-114">Typically, message store providers implement the following behavior when they move folders:</span></span>
  
- <span data-ttu-id="20b87-115">あるメッセージ ストアから別の種類の別のストアにフォルダーを移動すると、エントリ識別子が変更される保証があります。</span><span class="sxs-lookup"><span data-stu-id="20b87-115">When a folder is moved from one message store to another store of a different type, the entry identifier is guaranteed to change.</span></span>
    
- <span data-ttu-id="20b87-116">フォルダーを 1 つのメッセージ ストアから同じ種類の別のストアに移動すると、エントリ識別子はほとんど常に変更されます。</span><span class="sxs-lookup"><span data-stu-id="20b87-116">When a folder is moved from one message store to another store of the same type, the entry identifier almost always changes.</span></span>
    
- <span data-ttu-id="20b87-117">フォルダーを同じメッセージ ストア内の別の場所に移動すると、メッセージ ストア プロバイダーによっては、エントリ識別子が変更される場合と変更されない場合があります。</span><span class="sxs-lookup"><span data-stu-id="20b87-117">When a folder is moved to another location within the same message store, the entry identifier might or might not change, depending on the message store provider.</span></span>
    
<span data-ttu-id="20b87-118">通常、親フォルダーを変更せずにフォルダーの名前を変更しても、エントリ識別子は変更されません。</span><span class="sxs-lookup"><span data-stu-id="20b87-118">Renaming a folder without changing its parent folder usually does not cause the entry identifier to change.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="20b87-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="20b87-119">See also</span></span>



[<span data-ttu-id="20b87-120">MAPI エントリ識別子</span><span class="sxs-lookup"><span data-stu-id="20b87-120">MAPI Entry Identifiers</span></span>](mapi-entry-identifiers.md)

