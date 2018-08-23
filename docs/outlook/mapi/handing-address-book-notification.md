---
title: アドレス帳の通知の処理
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0dc4bb48-c8a1-447f-9e38-1c234a358fca
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: b5428ccde0e16bd32408b2ea908f5c5522992fc9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582918"
---
# <a name="handing-address-book-notification"></a><span data-ttu-id="93c88-103">アドレス帳の通知の処理</span><span class="sxs-lookup"><span data-stu-id="93c88-103">Handing address book notification</span></span>
  
<span data-ttu-id="93c88-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="93c88-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="93c88-105">アドレス帳の通知は、任意のアドレス帳のエントリに、または特定のエントリに、発生するイベントを取得するためのクライアントを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93c88-105">Address book notifications allow a client to learn of events that occur to any address book entry or to a particular entry.</span></span> <span data-ttu-id="93c88-106">[IAddrBook::Advise](iaddrbook-advise.md)を呼び出すことによって、MAPI アドレス帳またはアドレス帳コンテナーの階層構造または内容のテーブルを介して、これらの通知を登録するには、 [IMAPITable::Advise](imapitable-advise.md)を呼び出すことです。</span><span class="sxs-lookup"><span data-stu-id="93c88-106">You can register for these notifications either through the MAPI address book by calling [IAddrBook::Advise](iaddrbook-advise.md) or through an address book container's hierarchy or contents table by calling [IMAPITable::Advise](imapitable-advise.md).</span></span> 
  
<span data-ttu-id="93c88-107">全体のアドレス帳についての通知を登録する場合、特定のエントリでの通知を登録する場合は、アドレス帳コンテナー、配布リスト、またはメッセージングのユーザーのエントリの識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="93c88-107">Specify the entry identifier of an address book container, distribution list, or messaging user if you are registering for notifications on a particular entry and NULL if registering for notifications on the entire address book.</span></span> <span data-ttu-id="93c88-108">エントリの識別子には、メッセージングのユーザーや、アドレス帳コンテナー内の配布リストを表す必要があります。</span><span class="sxs-lookup"><span data-stu-id="93c88-108">The entry identifier must represent a messaging user or distribution list in an address book container.</span></span> <span data-ttu-id="93c88-109">**IAddrBook::Advise**は、どのアドレス帳プロバイダーは、対応するオブジェクトを決定するには、このエントリ id を検証し、適切なアドレス帳プロバイダーの[IABLogon::Advise](iablogon-advise.md)メソッドの呼び出しを転送します。</span><span class="sxs-lookup"><span data-stu-id="93c88-109">**IAddrBook::Advise** examines this entry identifier to determine which address book provider is responsible for the corresponding object and forwards the call to the appropriate address book provider's [IABLogon::Advise](iablogon-advise.md) method.</span></span> 
  
<span data-ttu-id="93c88-110">クライアントは、次の種類のアドレス帳のエントリのイベントを登録できます。</span><span class="sxs-lookup"><span data-stu-id="93c88-110">Clients can register for the following types of events on address book entries:</span></span>
  
- <span data-ttu-id="93c88-111">重大なエラー</span><span class="sxs-lookup"><span data-stu-id="93c88-111">Critical error</span></span>
    
- <span data-ttu-id="93c88-112">(作成、変更、削除、移動、またはコピー) のオブジェクトのイベントのいずれか</span><span class="sxs-lookup"><span data-stu-id="93c88-112">Any of the object events (created, modified, deleted, moved, or copied)</span></span>
    
- <span data-ttu-id="93c88-113">変更テーブル</span><span class="sxs-lookup"><span data-stu-id="93c88-113">Table modified</span></span>
    
<span data-ttu-id="93c88-114">通常、登録は、アドレス帳コンテナーのコンテンツおよび階層テーブルでのみ発生します。</span><span class="sxs-lookup"><span data-stu-id="93c88-114">Typically, registration occurs only on address book container contents and hierarchy tables.</span></span> <span data-ttu-id="93c88-115">クライアントがメッセージングのユーザーと配布リスト内のオブジェクトの下位レベルで登録することはまれです。</span><span class="sxs-lookup"><span data-stu-id="93c88-115">It is rare that clients register with the lower level messaging user and distribution list objects.</span></span> <span data-ttu-id="93c88-116">です。</span><span class="sxs-lookup"><span data-stu-id="93c88-116">This is because:</span></span>
  
- <span data-ttu-id="93c88-117">アドレス帳プロバイダーの多くは、メッセージングのユーザーと配布リストの通知をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="93c88-117">Many address book providers do not support notifications on their messaging users and distribution lists.</span></span>
    
- <span data-ttu-id="93c88-118">テーブルの通知は、変更を追跡し、ユーザーに報告のための十分です。</span><span class="sxs-lookup"><span data-stu-id="93c88-118">Table notifications are sufficient for tracking changes and reporting them to users.</span></span>
    

