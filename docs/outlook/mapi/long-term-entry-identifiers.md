---
title: 長期入力識別子
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a514275e-40c2-48db-8072-1dfc392a7ac6
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: b65656992681618aa8a1c53217bdd7101bc2502b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307785"
---
# <a name="long-term-entry-identifiers"></a><span data-ttu-id="711db-103">長期入力識別子</span><span class="sxs-lookup"><span data-stu-id="711db-103">Long-Term Entry Identifiers</span></span>

  
  
<span data-ttu-id="711db-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="711db-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="711db-105">長期間の有効期限がある識別子をオブジェクトが必要とする場合は、サービスプロバイダーによって、長期間のエントリ識別子がオブジェクトに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="711db-105">A long-term entry identifier is assigned by a service provider to an object when an object requires an identifier with a prolonged lifespan.</span></span> <span data-ttu-id="711db-106">長期の入力識別子は、週または月に対して常に有効であり、プロバイダーによっては他のワークステーションでも有効です。</span><span class="sxs-lookup"><span data-stu-id="711db-106">Long-term entry identifiers are always valid for weeks or months and can be valid on other workstations, depending on the provider.</span></span> <span data-ttu-id="711db-107">カスタム受信者用のアドレス帳プロバイダーによって作成された長期識別子は、すべて有効です。</span><span class="sxs-lookup"><span data-stu-id="711db-107">The long-term identifiers created by address book providers for custom recipients are universally valid.</span></span> 
  
<span data-ttu-id="711db-108">長期入力識別子は、メッセージストア、フォルダー、メッセージ、アドレス帳コンテナー、メッセージングユーザー、および配布リストに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="711db-108">Long-term entry identifiers are assigned to message stores, folders, messages, address book containers, messaging users, and distribution lists.</span></span> <span data-ttu-id="711db-109">クライアントアプリケーションがこれらのオブジェクトの[imapiprop:: GetProps](imapiprop-getprops.md)メソッドを呼び出す場合は、常に、返される長期間のエントリ識別子になります。</span><span class="sxs-lookup"><span data-stu-id="711db-109">When client applications call the [IMAPIProp::GetProps](imapiprop-getprops.md) method of these objects, it is always a long-term entry identifier that is returned.</span></span> 
  
<span data-ttu-id="711db-110">長期のエントリ識別子は、アクティブなプロファイル内のすべてのメッセージストア間で一意である必要があります。そのため、メッセージまたはフォルダーを別のメッセージストアにコピーするときには、新しいエントリ識別子を割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="711db-110">Long-term entry identifiers must be unique across all message stores in the active profile; therefore, when a message or folder is copied from one message store to another, it must be assigned a new entry identifier.</span></span> <span data-ttu-id="711db-111">メッセージストアオブジェクトが移動されると、移動を実装するメッセージストアプロバイダーは、元のエントリ識別子が有効なままかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="711db-111">When a message store object is moved, the message store provider that implements the move determines whether the original entry identifier will remain valid.</span></span> <span data-ttu-id="711db-112">一部のサービスプロバイダーは、移動されたオブジェクトに新しいエントリ識別子を割り当てます。それ以外の場合は含まれません。</span><span class="sxs-lookup"><span data-stu-id="711db-112">Some service providers assign new entry identifiers to moved objects; others do not.</span></span> <span data-ttu-id="711db-113">変更がある場合は、移動の通知を受け取ったときにクライアントに渡される情報に新しいエントリ識別子が含まれます。</span><span class="sxs-lookup"><span data-stu-id="711db-113">If there is a change, the new entry identifier will be included in the information passed to clients when they are notified of the move.</span></span> 
  
<span data-ttu-id="711db-114">通常、メッセージストアプロバイダーは、フォルダーを移動すると、次の動作を実装します。</span><span class="sxs-lookup"><span data-stu-id="711db-114">Typically, message store providers implement the following behavior when they move folders:</span></span>
  
- <span data-ttu-id="711db-115">フォルダーがあるメッセージストアから別の種類の別のストアに移動されると、エントリ識別子の変更が保証されます。</span><span class="sxs-lookup"><span data-stu-id="711db-115">When a folder is moved from one message store to another store of a different type, the entry identifier is guaranteed to change.</span></span>
    
- <span data-ttu-id="711db-116">フォルダーがあるメッセージストアから同じ種類の別のストアに移動された場合、エントリ識別子はほぼ常に変更されます。</span><span class="sxs-lookup"><span data-stu-id="711db-116">When a folder is moved from one message store to another store of the same type, the entry identifier almost always changes.</span></span>
    
- <span data-ttu-id="711db-117">フォルダーを同じメッセージストア内の別の場所に移動すると、メッセージストアプロバイダーに応じて、エントリ識別子が変更される場合があります。</span><span class="sxs-lookup"><span data-stu-id="711db-117">When a folder is moved to another location within the same message store, the entry identifier might or might not change, depending on the message store provider.</span></span>
    
<span data-ttu-id="711db-118">通常、親フォルダーを変更せずにフォルダーの名前を変更しても、エントリ識別子が変更されることはありません。</span><span class="sxs-lookup"><span data-stu-id="711db-118">Renaming a folder without changing its parent folder usually does not cause the entry identifier to change.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="711db-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="711db-119">See also</span></span>



[<span data-ttu-id="711db-120">MAPI エントリ識別子</span><span class="sxs-lookup"><span data-stu-id="711db-120">MAPI Entry Identifiers</span></span>](mapi-entry-identifiers.md)

