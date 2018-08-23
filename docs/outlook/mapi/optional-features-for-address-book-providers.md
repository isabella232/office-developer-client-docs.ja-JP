---
title: アドレス帳プロバイダーのオプション機能
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f1558259-7f0b-4731-80d2-88e51e203df0
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 378dcc3e1506432de22731a27731c58067647952
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565894"
---
# <a name="optional-features-for-address-book-providers"></a><span data-ttu-id="fb2a0-103">アドレス帳プロバイダーのオプション機能</span><span class="sxs-lookup"><span data-stu-id="fb2a0-103">Optional Features for Address Book Providers</span></span>

  
  
<span data-ttu-id="fb2a0-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fb2a0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fb2a0-105">アドレス帳プロバイダーの多くのオプション機能があります。</span><span class="sxs-lookup"><span data-stu-id="fb2a0-105">There are many optional features for address book providers.</span></span> <span data-ttu-id="fb2a0-106">さらに一般的に実装された機能は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="fb2a0-106">Some of the more commonly implemented features include:</span></span>
  
- <span data-ttu-id="fb2a0-107">別のプロバイダーのコンテナーに追加するのには、コンテナーの 1 つのエントリを許可することでは、外部のプロバイダーとして動作しています。</span><span class="sxs-lookup"><span data-stu-id="fb2a0-107">Acting as a foreign provider by allowing entries from one of your containers to be added to another provider's container.</span></span>
    
- <span data-ttu-id="fb2a0-108">コンテナーのいずれかに別のプロバイダーからのエントリを追加するのには、ホスト プロバイダーとして動作しています。</span><span class="sxs-lookup"><span data-stu-id="fb2a0-108">Acting as a host provider by adding entries from another provider to one of your containers.</span></span>
    
- <span data-ttu-id="fb2a0-109">高度な検索します。</span><span class="sxs-lookup"><span data-stu-id="fb2a0-109">Advanced searching.</span></span>
    
- <span data-ttu-id="fb2a0-110">プレフィックスのテーブルの内容をスクロールします。</span><span class="sxs-lookup"><span data-stu-id="fb2a0-110">Prefix scrolling through contents tables.</span></span>
    
- <span data-ttu-id="fb2a0-111">配布リストをサポートします。</span><span class="sxs-lookup"><span data-stu-id="fb2a0-111">Support for distribution lists.</span></span>
    
- <span data-ttu-id="fb2a0-112">イベント通知をサポートします。</span><span class="sxs-lookup"><span data-stu-id="fb2a0-112">Support for event notification.</span></span>
    
<span data-ttu-id="fb2a0-113">次の表には、これらのオプションの機能とそれらを実装する方法について簡単にについて説明します。</span><span class="sxs-lookup"><span data-stu-id="fb2a0-113">The following table briefly describes these optional features and how you implement them:</span></span>
  
|<span data-ttu-id="fb2a0-114">**機能**</span><span class="sxs-lookup"><span data-stu-id="fb2a0-114">**Feature**</span></span>|<span data-ttu-id="fb2a0-115">**実装する方法**</span><span class="sxs-lookup"><span data-stu-id="fb2a0-115">**How to implement**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fb2a0-116">受信者の一覧メッセージのエントリを作成するためのテンプレートを指定します。</span><span class="sxs-lookup"><span data-stu-id="fb2a0-116">Supply templates for creating entries for message recipient lists</span></span>  <br/> |<span data-ttu-id="fb2a0-117">[IABLogon::GetOneOffTable](iablogon-getoneofftable.md)メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="fb2a0-117">Implement the [IABLogon::GetOneOffTable](iablogon-getoneofftable.md) method.</span></span> <span data-ttu-id="fb2a0-118">詳細については、[一時テーブル](one-off-tables.md)と[一時テーブルを実装する](implementing-one-off-tables.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fb2a0-118">For more information, see [One-Off Tables](one-off-tables.md) and [Implementing One-Off Tables](implementing-one-off-tables.md).</span></span>  <br/> |
|<span data-ttu-id="fb2a0-119">名前付きの単位にグループの受信者</span><span class="sxs-lookup"><span data-stu-id="fb2a0-119">Group recipients into a named unit</span></span>  <br/> |<span data-ttu-id="fb2a0-120">配布リストのプロパティをサポートして導入することにより、 [IDistList: IMAPIContainer](idistlistimapicontainer.md)インタ フェースです。</span><span class="sxs-lookup"><span data-stu-id="fb2a0-120">Support the properties of distribution lists by implementing the [IDistList : IMAPIContainer](idistlistimapicontainer.md) interface.</span></span>  <br/> |
|<span data-ttu-id="fb2a0-121">別のプロバイダーのコンテナーに追加するエントリを許可することで外部アドレス帳プロバイダーとして動作します。</span><span class="sxs-lookup"><span data-stu-id="fb2a0-121">Act as a foreign address book provider by allowing entries to be added to a container in another provider</span></span>  <br/> | <span data-ttu-id="fb2a0-122">ホスト プロバイダーにデータ バインディング コードをサポートしてください。</span><span class="sxs-lookup"><span data-stu-id="fb2a0-122">Support binding code to data in the host provider by:</span></span>  <br/>  <span data-ttu-id="fb2a0-123">ユーザーおよび配布リストをメッセージに**PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) のプロパティをサポートします。</span><span class="sxs-lookup"><span data-stu-id="fb2a0-123">Supporting the **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property on messaging users and distribution lists.</span></span> <span data-ttu-id="fb2a0-124">詳細については、[アドレス帳の識別子](address-book-identifiers.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fb2a0-124">For more information, see [Address Book Identifiers](address-book-identifiers.md).</span></span>  <br/>  <span data-ttu-id="fb2a0-125">[IABLogon::OpenTemplateID](iablogon-opentemplateid.md)メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="fb2a0-125">Implementing the [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) method.</span></span> <span data-ttu-id="fb2a0-126">詳細については、[外部のアドレス帳プロバイダーとしての機能](acting-as-a-foreign-address-book-provider.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fb2a0-126">For more information, see [Acting as a Foreign Address Book Provider](acting-as-a-foreign-address-book-provider.md).</span></span>  <br/> |
|<span data-ttu-id="fb2a0-127">別のプロバイダーからのエントリを挿入することによって、ホストのアドレス帳プロバイダーとして機能します。</span><span class="sxs-lookup"><span data-stu-id="fb2a0-127">Acting as a host address book provider by inserting entries from another provider</span></span>  <br/> |<span data-ttu-id="fb2a0-128">[IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md)メソッドを呼び出すことによってコードに外部プロバイダーからのデータ バインディングをサポートします。</span><span class="sxs-lookup"><span data-stu-id="fb2a0-128">Support binding data to code from a foreign provider by calling the [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) method.</span></span> <span data-ttu-id="fb2a0-129">詳細については、[ホストのアドレス帳プロバイダーとしての機能](acting-as-a-host-address-book-provider.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fb2a0-129">For more information, see [Acting as a Host Address Book Provider](acting-as-a-host-address-book-provider.md).</span></span>  <br/> |
|<span data-ttu-id="fb2a0-130">スクロールを付ける</span><span class="sxs-lookup"><span data-stu-id="fb2a0-130">Prefix scrolling</span></span>  <br/> |<span data-ttu-id="fb2a0-131">コンテナーの内容のテーブルの制約をサポートします。</span><span class="sxs-lookup"><span data-stu-id="fb2a0-131">Support restrictions on container contents tables.</span></span> <span data-ttu-id="fb2a0-132">詳細については、[制限の詳細](about-restrictions.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fb2a0-132">For more information, see [About Restrictions](about-restrictions.md).</span></span>  <br/> |
|<span data-ttu-id="fb2a0-133">高度なコンテナー内の検索</span><span class="sxs-lookup"><span data-stu-id="fb2a0-133">Advanced searching in a container</span></span>  <br/> |<span data-ttu-id="fb2a0-134">コンテナーの**PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) のプロパティをサポートします。</span><span class="sxs-lookup"><span data-stu-id="fb2a0-134">Support the **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) property on containers.</span></span> <span data-ttu-id="fb2a0-135">詳細については、[高度な検索を実装する](implementing-advanced-searching.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fb2a0-135">For more information, see [Implementing Advanced Searching](implementing-advanced-searching.md).</span></span>  <br/> |
|<span data-ttu-id="fb2a0-136">イベント通知</span><span class="sxs-lookup"><span data-stu-id="fb2a0-136">Event notification</span></span>  <br/> |<span data-ttu-id="fb2a0-137">[IABLogon::Advise](iablogon-advise.md)メソッドと[IABLogon::Unadvise](iablogon-unadvise.md)メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="fb2a0-137">Implement the [IABLogon::Advise](iablogon-advise.md) and [IABLogon::Unadvise](iablogon-unadvise.md) methods.</span></span> <span data-ttu-id="fb2a0-138">詳細については、 [MAPI でのイベント通知](event-notification-in-mapi.md)[イベント通知のサポート](supporting-event-notification.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fb2a0-138">For more information, see [Event Notification in MAPI](event-notification-in-mapi.md) and [Supporting Event Notification](supporting-event-notification.md).</span></span>  <br/> |
   
<span data-ttu-id="fb2a0-139">イベントの通知、 **IABLogon::Advise**メソッドが呼び出される MAPI によってクライアントは、ユーザーまたは配布リストをメッセージのコンテナーのいずれかの通知を登録する**IAddrBook::Advise**を呼び出すと。</span><span class="sxs-lookup"><span data-stu-id="fb2a0-139">For event notification, your **IABLogon::Advise** method will be called by MAPI when a client calls **IAddrBook::Advise** to register for notifications on any one of your containers, messaging users, or distribution lists.</span></span> <span data-ttu-id="fb2a0-140">ただし、イベント通知をサポートしているが省略可能であるために、これらのメソッドから MAPI_E_NO_SUPPORT を取得できます。</span><span class="sxs-lookup"><span data-stu-id="fb2a0-140">However, because supporting event notification is optional, you can return MAPI_E_NO_SUPPORT from these methods.</span></span> <span data-ttu-id="fb2a0-141">ただし、MAPI には少なくとも、内容のテーブルの通知をサポートしているすべての種類の値を追加するのには_fnevSearchComplete_と_fnevCriticalError_のイベントを除くオブジェクトの通知をサポートすることをお勧めはお勧めします。</span><span class="sxs-lookup"><span data-stu-id="fb2a0-141">However, MAPI does recommend that you at least support notifications on your contents tables and encourages you to support all types of object notification except for  _fnevSearchComplete_ and the  _fnevCriticalError_ event to add value.</span></span> 
  

