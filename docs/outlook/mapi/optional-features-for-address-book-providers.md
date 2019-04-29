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
# <a name="optional-features-for-address-book-providers"></a><span data-ttu-id="d51bc-103">アドレス帳プロバイダーのオプション機能</span><span class="sxs-lookup"><span data-stu-id="d51bc-103">Optional Features for Address Book Providers</span></span>

  
  
<span data-ttu-id="d51bc-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d51bc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d51bc-105">アドレス帳プロバイダーには、多くのオプション機能があります。</span><span class="sxs-lookup"><span data-stu-id="d51bc-105">There are many optional features for address book providers.</span></span> <span data-ttu-id="d51bc-106">一般的に実装されている機能には、次のようなものがあります。</span><span class="sxs-lookup"><span data-stu-id="d51bc-106">Some of the more commonly implemented features include:</span></span>
  
- <span data-ttu-id="d51bc-107">コンテナーの1つのエントリを別のプロバイダーのコンテナーに追加できるようにすることで、外部プロバイダーとして機能します。</span><span class="sxs-lookup"><span data-stu-id="d51bc-107">Acting as a foreign provider by allowing entries from one of your containers to be added to another provider's container.</span></span>
    
- <span data-ttu-id="d51bc-108">別のプロバイダーからコンテナーの1つにエントリを追加することによって、ホストプロバイダーとして機能します。</span><span class="sxs-lookup"><span data-stu-id="d51bc-108">Acting as a host provider by adding entries from another provider to one of your containers.</span></span>
    
- <span data-ttu-id="d51bc-109">高度な検索。</span><span class="sxs-lookup"><span data-stu-id="d51bc-109">Advanced searching.</span></span>
    
- <span data-ttu-id="d51bc-110">目次テーブルをスクロールするプレフィックス。</span><span class="sxs-lookup"><span data-stu-id="d51bc-110">Prefix scrolling through contents tables.</span></span>
    
- <span data-ttu-id="d51bc-111">配布リストのサポート。</span><span class="sxs-lookup"><span data-stu-id="d51bc-111">Support for distribution lists.</span></span>
    
- <span data-ttu-id="d51bc-112">イベント通知のサポート。</span><span class="sxs-lookup"><span data-stu-id="d51bc-112">Support for event notification.</span></span>
    
<span data-ttu-id="d51bc-113">次の表に、これらのオプション機能とその実装方法を簡単に説明します。</span><span class="sxs-lookup"><span data-stu-id="d51bc-113">The following table briefly describes these optional features and how you implement them:</span></span>
  
|<span data-ttu-id="d51bc-114">**機能**</span><span class="sxs-lookup"><span data-stu-id="d51bc-114">**Feature**</span></span>|<span data-ttu-id="d51bc-115">**実装方法**</span><span class="sxs-lookup"><span data-stu-id="d51bc-115">**How to implement**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d51bc-116">メッセージ受信者リストのエントリを作成するためのテンプレートを提供する</span><span class="sxs-lookup"><span data-stu-id="d51bc-116">Supply templates for creating entries for message recipient lists</span></span>  <br/> |<span data-ttu-id="d51bc-117">[IABLogon:: getoneofftable](iablogon-getoneofftable.md)メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="d51bc-117">Implement the [IABLogon::GetOneOffTable](iablogon-getoneofftable.md) method.</span></span> <span data-ttu-id="d51bc-118">詳細については、「one-off[テーブル](one-off-tables.md)」と「 [1 回限りのテーブルの実装](implementing-one-off-tables.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d51bc-118">For more information, see [One-Off Tables](one-off-tables.md) and [Implementing One-Off Tables](implementing-one-off-tables.md).</span></span>  <br/> |
|<span data-ttu-id="d51bc-119">受信者を指定の単位にグループ化する</span><span class="sxs-lookup"><span data-stu-id="d51bc-119">Group recipients into a named unit</span></span>  <br/> |<span data-ttu-id="d51bc-120">[idistlist: IMAPIContainer](idistlistimapicontainer.md)インターフェイスを実装することによって、配布リストのプロパティをサポートします。</span><span class="sxs-lookup"><span data-stu-id="d51bc-120">Support the properties of distribution lists by implementing the [IDistList : IMAPIContainer](idistlistimapicontainer.md) interface.</span></span>  <br/> |
|<span data-ttu-id="d51bc-121">別のプロバイダーのコンテナーにエントリを追加できるようにすることにより、外部アドレス帳プロバイダーとして機能します。</span><span class="sxs-lookup"><span data-stu-id="d51bc-121">Act as a foreign address book provider by allowing entries to be added to a container in another provider</span></span>  <br/> | <span data-ttu-id="d51bc-122">次の方法でホストプロバイダーのデータへのバインドコードをサポートします。</span><span class="sxs-lookup"><span data-stu-id="d51bc-122">Support binding code to data in the host provider by:</span></span>  <br/>  <span data-ttu-id="d51bc-123">メッセージングユーザーおよび配布リストに対して**PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) プロパティをサポートします。</span><span class="sxs-lookup"><span data-stu-id="d51bc-123">Supporting the **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property on messaging users and distribution lists.</span></span> <span data-ttu-id="d51bc-124">詳細については、「[アドレス帳の識別子](address-book-identifiers.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d51bc-124">For more information, see [Address Book Identifiers](address-book-identifiers.md).</span></span>  <br/>  <span data-ttu-id="d51bc-125">[IABLogon:: OpenTemplateID](iablogon-opentemplateid.md)メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="d51bc-125">Implementing the [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) method.</span></span> <span data-ttu-id="d51bc-126">詳細については、「[外部アドレス帳プロバイダーとして機能する](acting-as-a-foreign-address-book-provider.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d51bc-126">For more information, see [Acting as a Foreign Address Book Provider](acting-as-a-foreign-address-book-provider.md).</span></span>  <br/> |
|<span data-ttu-id="d51bc-127">別のプロバイダーからエントリを挿入してホストアドレス帳プロバイダーとして機能する</span><span class="sxs-lookup"><span data-stu-id="d51bc-127">Acting as a host address book provider by inserting entries from another provider</span></span>  <br/> |<span data-ttu-id="d51bc-128">[imapisupport:: OpenTemplateID](imapisupport-opentemplateid.md)メソッドを呼び出して、外部プロバイダーからのコードへのデータのバインドをサポートします。</span><span class="sxs-lookup"><span data-stu-id="d51bc-128">Support binding data to code from a foreign provider by calling the [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) method.</span></span> <span data-ttu-id="d51bc-129">詳細については、「[ホストアドレス帳プロバイダーとして機能する](acting-as-a-host-address-book-provider.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d51bc-129">For more information, see [Acting as a Host Address Book Provider](acting-as-a-host-address-book-provider.md).</span></span>  <br/> |
|<span data-ttu-id="d51bc-130">プレフィックスのスクロール</span><span class="sxs-lookup"><span data-stu-id="d51bc-130">Prefix scrolling</span></span>  <br/> |<span data-ttu-id="d51bc-131">コンテナーコンテンツテーブルの制限をサポートします。</span><span class="sxs-lookup"><span data-stu-id="d51bc-131">Support restrictions on container contents tables.</span></span> <span data-ttu-id="d51bc-132">詳細については、「[制限につい](about-restrictions.md)て」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d51bc-132">For more information, see [About Restrictions](about-restrictions.md).</span></span>  <br/> |
|<span data-ttu-id="d51bc-133">コンテナー内での高度な検索</span><span class="sxs-lookup"><span data-stu-id="d51bc-133">Advanced searching in a container</span></span>  <br/> |<span data-ttu-id="d51bc-134">コンテナーの**PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) プロパティをサポートします。</span><span class="sxs-lookup"><span data-stu-id="d51bc-134">Support the **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) property on containers.</span></span> <span data-ttu-id="d51bc-135">詳細については、「[高度な検索の実装](implementing-advanced-searching.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d51bc-135">For more information, see [Implementing Advanced Searching](implementing-advanced-searching.md).</span></span>  <br/> |
|<span data-ttu-id="d51bc-136">イベント通知</span><span class="sxs-lookup"><span data-stu-id="d51bc-136">Event notification</span></span>  <br/> |<span data-ttu-id="d51bc-137">[IABLogon::](iablogon-advise.md)アドバイズおよび[IABLogon:: アドバイズ](iablogon-unadvise.md)中止メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="d51bc-137">Implement the [IABLogon::Advise](iablogon-advise.md) and [IABLogon::Unadvise](iablogon-unadvise.md) methods.</span></span> <span data-ttu-id="d51bc-138">詳細については、「 [MAPI でのイベント通知](event-notification-in-mapi.md)」および「[サポートイベントの通知](supporting-event-notification.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d51bc-138">For more information, see [Event Notification in MAPI](event-notification-in-mapi.md) and [Supporting Event Notification](supporting-event-notification.md).</span></span>  <br/> |
   
<span data-ttu-id="d51bc-139">イベント通知の場合、クライアントが**IAddrBook:: アドバイズ**を呼び出して、コンテナー、メッセージングユーザー、または配布リストのいずれかに通知を登録するときに、 **IABLogon:: アドバイズ**メソッドが MAPI によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d51bc-139">For event notification, your **IABLogon::Advise** method will be called by MAPI when a client calls **IAddrBook::Advise** to register for notifications on any one of your containers, messaging users, or distribution lists.</span></span> <span data-ttu-id="d51bc-140">ただし、イベント通知のサポートはオプションなので、これらのメソッドから MAPI_E_NO_SUPPORT を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="d51bc-140">However, because supporting event notification is optional, you can return MAPI_E_NO_SUPPORT from these methods.</span></span> <span data-ttu-id="d51bc-141">ただし、MAPI では、少なくともコンテンツテーブルに対する通知をサポートしており、 _fnevSearchComplete_以外のすべての種類のオブジェクト通知と、値を追加する_fnevCriticalError_イベントをサポートすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="d51bc-141">However, MAPI does recommend that you at least support notifications on your contents tables and encourages you to support all types of object notification except for  _fnevSearchComplete_ and the  _fnevCriticalError_ event to add value.</span></span> 
  

