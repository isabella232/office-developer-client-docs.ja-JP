---
title: アドレス帳プロバイダーのオプション機能
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f1558259-7f0b-4731-80d2-88e51e203df0
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 9f5d8f0cd1b21f58e4e5c7d7ccd6cb19f3626c38
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414572"
---
# <a name="optional-features-for-address-book-providers"></a><span data-ttu-id="38e0f-103">アドレス帳プロバイダーのオプション機能</span><span class="sxs-lookup"><span data-stu-id="38e0f-103">Optional Features for Address Book Providers</span></span>

  
  
<span data-ttu-id="38e0f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="38e0f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="38e0f-105">アドレス帳プロバイダーには、多くのオプション機能があります。</span><span class="sxs-lookup"><span data-stu-id="38e0f-105">There are many optional features for address book providers.</span></span> <span data-ttu-id="38e0f-106">より一般的に実装される機能のいくつかは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="38e0f-106">Some of the more commonly implemented features include:</span></span>
  
- <span data-ttu-id="38e0f-107">あるコンテナーからのエントリを別のプロバイダーのコンテナーに追加できるようにして、外部プロバイダーとして機能します。</span><span class="sxs-lookup"><span data-stu-id="38e0f-107">Acting as a foreign provider by allowing entries from one of your containers to be added to another provider's container.</span></span>
    
- <span data-ttu-id="38e0f-108">別のプロバイダーのエントリをコンテナーの 1 つに追加して、ホスト プロバイダーとして機能します。</span><span class="sxs-lookup"><span data-stu-id="38e0f-108">Acting as a host provider by adding entries from another provider to one of your containers.</span></span>
    
- <span data-ttu-id="38e0f-109">高度な検索。</span><span class="sxs-lookup"><span data-stu-id="38e0f-109">Advanced searching.</span></span>
    
- <span data-ttu-id="38e0f-110">コンテンツ テーブルをスクロールするプレフィックス。</span><span class="sxs-lookup"><span data-stu-id="38e0f-110">Prefix scrolling through contents tables.</span></span>
    
- <span data-ttu-id="38e0f-111">配布リストのサポート。</span><span class="sxs-lookup"><span data-stu-id="38e0f-111">Support for distribution lists.</span></span>
    
- <span data-ttu-id="38e0f-112">イベント通知のサポート。</span><span class="sxs-lookup"><span data-stu-id="38e0f-112">Support for event notification.</span></span>
    
<span data-ttu-id="38e0f-113">次の表では、これらのオプション機能とそれらを実装する方法について簡単に説明します。</span><span class="sxs-lookup"><span data-stu-id="38e0f-113">The following table briefly describes these optional features and how you implement them:</span></span>
  
|<span data-ttu-id="38e0f-114">**機能**</span><span class="sxs-lookup"><span data-stu-id="38e0f-114">**Feature**</span></span>|<span data-ttu-id="38e0f-115">**実装方法**</span><span class="sxs-lookup"><span data-stu-id="38e0f-115">**How to implement**</span></span>|
|:-----|:-----|
|<span data-ttu-id="38e0f-116">メッセージ受信者リストのエントリを作成するためのテンプレートを指定する</span><span class="sxs-lookup"><span data-stu-id="38e0f-116">Supply templates for creating entries for message recipient lists</span></span>  <br/> |<span data-ttu-id="38e0f-117">[IABLogon::GetOneOffTable メソッドを実装](iablogon-getoneofftable.md)します。</span><span class="sxs-lookup"><span data-stu-id="38e0f-117">Implement the [IABLogon::GetOneOffTable](iablogon-getoneofftable.md) method.</span></span> <span data-ttu-id="38e0f-118">詳細については [、「One-Off Tables」](one-off-tables.md) および [「Implementing One-Off参照してください](implementing-one-off-tables.md)。</span><span class="sxs-lookup"><span data-stu-id="38e0f-118">For more information, see [One-Off Tables](one-off-tables.md) and [Implementing One-Off Tables](implementing-one-off-tables.md).</span></span>  <br/> |
|<span data-ttu-id="38e0f-119">受信者を名前付きユニットにグループ化する</span><span class="sxs-lookup"><span data-stu-id="38e0f-119">Group recipients into a named unit</span></span>  <br/> |<span data-ttu-id="38e0f-120">[IDistList : IMAPIContainer インターフェイスを実装して、配布リストのプロパティをサポート](idistlistimapicontainer.md)します。</span><span class="sxs-lookup"><span data-stu-id="38e0f-120">Support the properties of distribution lists by implementing the [IDistList : IMAPIContainer](idistlistimapicontainer.md) interface.</span></span>  <br/> |
|<span data-ttu-id="38e0f-121">別のプロバイダーのコンテナーにエントリを追加できるようにして、外部アドレス帳プロバイダーとして機能する</span><span class="sxs-lookup"><span data-stu-id="38e0f-121">Act as a foreign address book provider by allowing entries to be added to a container in another provider</span></span>  <br/> | <span data-ttu-id="38e0f-122">次の方法で、ホスト プロバイダーのデータへのバインド コードをサポートします。</span><span class="sxs-lookup"><span data-stu-id="38e0f-122">Support binding code to data in the host provider by:</span></span>  <br/>  <span data-ttu-id="38e0f-123">メッセージング ユーザー **PR_TEMPLATEID** 配布リストの [プロパティ (PidTagTemplateid)](pidtagtemplateid-canonical-property.md)プロパティをサポートします。</span><span class="sxs-lookup"><span data-stu-id="38e0f-123">Supporting the **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property on messaging users and distribution lists.</span></span> <span data-ttu-id="38e0f-124">詳細については、「アドレス帳 [識別子」を参照してください](address-book-identifiers.md)。</span><span class="sxs-lookup"><span data-stu-id="38e0f-124">For more information, see [Address Book Identifiers](address-book-identifiers.md).</span></span>  <br/>  <span data-ttu-id="38e0f-125">[IABLogon::OpenTemplateID メソッドを実装](iablogon-opentemplateid.md)します。</span><span class="sxs-lookup"><span data-stu-id="38e0f-125">Implementing the [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) method.</span></span> <span data-ttu-id="38e0f-126">詳細については、「外部アドレス [帳プロバイダーとして機能する」を参照してください](acting-as-a-foreign-address-book-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="38e0f-126">For more information, see [Acting as a Foreign Address Book Provider](acting-as-a-foreign-address-book-provider.md).</span></span>  <br/> |
|<span data-ttu-id="38e0f-127">別のプロバイダーからのエントリを挿入してホスト アドレス帳プロバイダーとして機能する</span><span class="sxs-lookup"><span data-stu-id="38e0f-127">Acting as a host address book provider by inserting entries from another provider</span></span>  <br/> |<span data-ttu-id="38e0f-128">[IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md)メソッドを呼び出して、外部プロバイダーからのコードへのデータのバインドをサポートします。</span><span class="sxs-lookup"><span data-stu-id="38e0f-128">Support binding data to code from a foreign provider by calling the [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) method.</span></span> <span data-ttu-id="38e0f-129">詳細については、「ホスト アドレス [帳プロバイダーとして機能する」を参照してください](acting-as-a-host-address-book-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="38e0f-129">For more information, see [Acting as a Host Address Book Provider](acting-as-a-host-address-book-provider.md).</span></span>  <br/> |
|<span data-ttu-id="38e0f-130">プレフィックスのスクロール</span><span class="sxs-lookup"><span data-stu-id="38e0f-130">Prefix scrolling</span></span>  <br/> |<span data-ttu-id="38e0f-131">コンテナー コンテンツ テーブルの制限をサポートします。</span><span class="sxs-lookup"><span data-stu-id="38e0f-131">Support restrictions on container contents tables.</span></span> <span data-ttu-id="38e0f-132">詳細については、「制限について [」を参照してください](about-restrictions.md)。</span><span class="sxs-lookup"><span data-stu-id="38e0f-132">For more information, see [About Restrictions](about-restrictions.md).</span></span>  <br/> |
|<span data-ttu-id="38e0f-133">コンテナー内の高度な検索</span><span class="sxs-lookup"><span data-stu-id="38e0f-133">Advanced searching in a container</span></span>  <br/> |<span data-ttu-id="38e0f-134">コンテナーの **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) プロパティをサポートします。</span><span class="sxs-lookup"><span data-stu-id="38e0f-134">Support the **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) property on containers.</span></span> <span data-ttu-id="38e0f-135">詳細については、「高度な [検索の実装」を参照してください](implementing-advanced-searching.md)。</span><span class="sxs-lookup"><span data-stu-id="38e0f-135">For more information, see [Implementing Advanced Searching](implementing-advanced-searching.md).</span></span>  <br/> |
|<span data-ttu-id="38e0f-136">イベント通知</span><span class="sxs-lookup"><span data-stu-id="38e0f-136">Event notification</span></span>  <br/> |<span data-ttu-id="38e0f-137">[IABLogon::Advise メソッドと](iablogon-advise.md) [IABLogon::Unadvise メソッドを](iablogon-unadvise.md)実装します。</span><span class="sxs-lookup"><span data-stu-id="38e0f-137">Implement the [IABLogon::Advise](iablogon-advise.md) and [IABLogon::Unadvise](iablogon-unadvise.md) methods.</span></span> <span data-ttu-id="38e0f-138">詳細については [、「MAPI でのイベント通知」および「サポート](event-notification-in-mapi.md) イベント通知 [」を参照してください](supporting-event-notification.md)。</span><span class="sxs-lookup"><span data-stu-id="38e0f-138">For more information, see [Event Notification in MAPI](event-notification-in-mapi.md) and [Supporting Event Notification](supporting-event-notification.md).</span></span>  <br/> |
   
<span data-ttu-id="38e0f-139">イベント通知の場合 **、IABLogon::Advise** メソッドは、クライアントが **IAddrBook::Advise** を呼び出して、コンテナー、メッセージング ユーザー、または配布リストのいずれかの通知に登録するときに MAPI によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="38e0f-139">For event notification, your **IABLogon::Advise** method will be called by MAPI when a client calls **IAddrBook::Advise** to register for notifications on any one of your containers, messaging users, or distribution lists.</span></span> <span data-ttu-id="38e0f-140">ただし、サポート イベント通知はオプションなので、これらのメソッドからMAPI_E_NO_SUPPORT返します。</span><span class="sxs-lookup"><span data-stu-id="38e0f-140">However, because supporting event notification is optional, you can return MAPI_E_NO_SUPPORT from these methods.</span></span> <span data-ttu-id="38e0f-141">ただし、MAPI では、少なくともコンテンツ テーブルの通知をサポートすることをお勧めします。  _また、fnevSearchComplete_ および  _fnevCriticalError_ イベントを除くすべての種類のオブジェクト通知をサポートして値を追加することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="38e0f-141">However, MAPI does recommend that you at least support notifications on your contents tables and encourages you to support all types of object notification except for  _fnevSearchComplete_ and the  _fnevCriticalError_ event to add value.</span></span> 
  

