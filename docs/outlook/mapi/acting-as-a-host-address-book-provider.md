---
title: ホスト アドレス帳プロバイダーとして機能
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f06a1034-ee49-4a09-831e-9752713228a8
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: cf52062eacbd13b45087df9d8558bffd43ccd744
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799634"
---
# <a name="acting-as-a-host-address-book-provider"></a><span data-ttu-id="eb1ea-103">ホスト アドレス帳プロバイダーとして機能</span><span class="sxs-lookup"><span data-stu-id="eb1ea-103">Acting as a Host Address Book Provider</span></span>

  
  
<span data-ttu-id="eb1ea-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="eb1ea-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="eb1ea-105">ホスト プロバイダーとは、そのコンテナー内の他のプロバイダーからの受信者が含まれていて、受信者のメンテナンスを部分的に制御するその他のプロバイダーの実装に依存しているアドレス帳プロバイダーです。</span><span class="sxs-lookup"><span data-stu-id="eb1ea-105">A host provider is an address book provider that includes recipients from other providers in its containers and relies on the implementation of the recipients by the other providers to partially control their maintenance.</span></span> <span data-ttu-id="eb1ea-106">ホスト プロバイダーでは、これらの受信者が外部のテンプレート識別子を使用して、外部プロバイダーのコードにこれらの受信者に対してデータをバインドします。</span><span class="sxs-lookup"><span data-stu-id="eb1ea-106">A host provider uses the template identifiers of these foreign recipients to bind the data for these recipients to code in the foreign provider.</span></span> <span data-ttu-id="eb1ea-107">プロバイダーは、 **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) のプロパティ、受信者を取得し、 [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md)への呼び出しに渡されます場合は、バインディング プロセスが開始されます。</span><span class="sxs-lookup"><span data-stu-id="eb1ea-107">This binding process is initiated when your provider retrieves the **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property of a recipient and passes it in a call to [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md).</span></span> 
  
<span data-ttu-id="eb1ea-108">**IMAPISupport::OpenTemplateID**、MAPI プロバイダー呼び出し内の**MAPIUID**に一致して、 **MAPIUID**を持つテンプレート id プロバイダーが登録されているプロバイダーの[IABLogon::OpenTemplateID](iablogon-opentemplateid.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="eb1ea-108">When your provider calls **IMAPISupport::OpenTemplateID**, MAPI matches the **MAPIUID** within the template identifier with a **MAPIUID** registered by a provider and calls the provider's [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) method.</span></span> <span data-ttu-id="eb1ea-109">外部のプロバイダーは、プロバイダーのプロパティ オブジェクト、プロパティ オブジェクトの実装を独自にポインターを返すことがありますか、プロバイダーのオブジェクトをラップする、実装します。</span><span class="sxs-lookup"><span data-stu-id="eb1ea-109">The foreign provider might return a pointer to your provider's property object, to its own property object implementation, or to an implementation that wraps your provider's object.</span></span> <span data-ttu-id="eb1ea-110">返されるポインターは、 _lppMAPIPropNew_パラメーターの内容に配置されます。</span><span class="sxs-lookup"><span data-stu-id="eb1ea-110">The returned pointer is placed in the contents of the  _lppMAPIPropNew_ parameter.</span></span> 
  
<span data-ttu-id="eb1ea-111">プロバイダーは、FILL_ENTRY フラグを設定して**IMAPISupport::OpenTemplateID**をコールするかどうかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="eb1ea-111">Your provider can choose whether or not to call **IMAPISupport::OpenTemplateID** with the FILL_ENTRY flag set.</span></span> <span data-ttu-id="eb1ea-112">受信者を作成するとき、または長い時間が経過、プロバイダーが、受信者のプロパティを更新するときは、このフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="eb1ea-112">Set this flag when the recipient is being created or when a long time has passed since your provider has refreshed the recipient's properties.</span></span> <span data-ttu-id="eb1ea-113">FILL_ENTRY フラグの一般的な用途では、同期元プロバイダーで、受信者を保持します。</span><span class="sxs-lookup"><span data-stu-id="eb1ea-113">A common use of the FILL_ENTRY flag is to keep a recipient in your provider synchronized with the original.</span></span> <span data-ttu-id="eb1ea-114">同期スケジュールのこの型を実装すると、パフォーマンスが向上します。</span><span class="sxs-lookup"><span data-stu-id="eb1ea-114">Implementing this type of synchronization schedule enhances performance.</span></span> 
  
 <span data-ttu-id="eb1ea-115">**外部の受信者を保持するのには次のように同期します。**</span><span class="sxs-lookup"><span data-stu-id="eb1ea-115">**To keep a foreign recipient synchronized**</span></span>
  
1. <span data-ttu-id="eb1ea-116">定期的な更新プログラムの適切な間隔を決定します。</span><span class="sxs-lookup"><span data-stu-id="eb1ea-116">Determine an appropriate interval for periodic updates.</span></span> 
    
2. <span data-ttu-id="eb1ea-117">各タイムスタンプは、 [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="eb1ea-117">Timestamp each call to [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md).</span></span> 
    
3. <span data-ttu-id="eb1ea-118">前回の呼び出し後に期限が切れている時間の量に基づくフル更新を実行する必要があるかどうかを評価します。</span><span class="sxs-lookup"><span data-stu-id="eb1ea-118">Evaluate whether or not it is necessary to perform a full update based on the amount of time that has expired since the last call.</span></span> <span data-ttu-id="eb1ea-119">フル更新が必要な場合は、FILL_ENTRY フラグを使用して**IMAPISupport::OpenTemplateID**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="eb1ea-119">If a full update is necessary, call **IMAPISupport::OpenTemplateID** with the FILL_ENTRY flag.</span></span> <span data-ttu-id="eb1ea-120">そうでないために必要な場合、呼び出しのフラグは設定しません。</span><span class="sxs-lookup"><span data-stu-id="eb1ea-120">If it is not necessary, do not set the flag on the call.</span></span> 
    
<span data-ttu-id="eb1ea-121">クライアント コピーの受信者のプロパティのいずれかを要求すると、プロバイダーはその要求を処理または外部のプロバイダーから提供されたコードを使用するかどうかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="eb1ea-121">When a client makes a request for one of the copied recipient's properties, your provider can choose whether to handle the request itself or use the code supplied by the foreign provider.</span></span> <span data-ttu-id="eb1ea-122">[IMAPIProp::OpenProperty](imapiprop-openproperty.md)以外の**IMAPIProp**を呼び出し、されていない場合、プロバイダーは、ほとんどをインターセプトするための外部プロバイダーを期待できます。</span><span class="sxs-lookup"><span data-stu-id="eb1ea-122">Your provider can expect the foreign provider to intercept most, if not all, calls to **IMAPIProp** except for [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span> <span data-ttu-id="eb1ea-123">**PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) のプロパティを要求する**OpenProperty**への呼び出しは常に、プロバイダーに転送されます。</span><span class="sxs-lookup"><span data-stu-id="eb1ea-123">A call to **OpenProperty** requesting the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property is always forwarded to your provider.</span></span>
  
 <span data-ttu-id="eb1ea-124">**テンプレート識別子のコードへのアクセス**</span><span class="sxs-lookup"><span data-stu-id="eb1ea-124">**To access template identifier code**</span></span>
  
1. <span data-ttu-id="eb1ea-125">受信者を開き、メソッドを呼び出して、 [IMAPIProp::GetProps](imapiprop-getprops.md) **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) のプロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="eb1ea-125">Open the recipient and call its [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property.</span></span> <span data-ttu-id="eb1ea-126">**GetProps**には、 **PR_TEMPLATEID**が使用できないため失敗した場合、外部のプロバイダー サポートしていません、テンプレート識別子と関連するコードをこの受信者の。</span><span class="sxs-lookup"><span data-stu-id="eb1ea-126">If **GetProps** fails because **PR_TEMPLATEID** is unavailable, the foreign provider does not support a template identifier and related code for this recipient.</span></span> <span data-ttu-id="eb1ea-127">プロバイダーは、すべてのメンテナンスのため、受信者の実装を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="eb1ea-127">Your provider will need to use its implementation of the recipient for all maintenance.</span></span> 
    
2. <span data-ttu-id="eb1ea-128">**GetProps**からテンプレートの識別子が返された場合、受信者の**IMAPIProp**の実装では、 **IMAPISupport::OpenTemplateID**メソッドの呼び出しにし、ポインターを渡します。</span><span class="sxs-lookup"><span data-stu-id="eb1ea-128">If the template identifier is returned from **GetProps**, pass it and a pointer to the recipient's **IMAPIProp** implementation in a call to the **IMAPISupport::OpenTemplateID** method.</span></span> <span data-ttu-id="eb1ea-129">受信者のプロパティのほとんどまたはすべてをする必要がある場合、FILL_ENTRY フラグを設定の作成時またはかどうかは、更新されていない間に、ように更新します。</span><span class="sxs-lookup"><span data-stu-id="eb1ea-129">Set the FILL_ENTRY flag if most or all of the recipient's properties need to be updated, such as at creation time or if they have not been updated for a while.</span></span> 
    
3. <span data-ttu-id="eb1ea-130">**OpenTemplateID**では、外部プロバイダーの**IMAPIProp**の実装が返された場合は、[クライアントにこの実装へのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="eb1ea-130">If **OpenTemplateID** returns the foreign provider's **IMAPIProp** implementation, return to the client a pointer to this implementation.</span></span> 
    
4. <span data-ttu-id="eb1ea-131">**OpenTemplateID**が返されない場合、実装、通常プロファイルでは、外部のプロバイダーがないためクライアントに返す**IMAPIProp**プロバイダーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="eb1ea-131">If **OpenTemplateID** does not return an implementation, typically because the foreign provider is not in the profile, return to the client a pointer to your provider's **IMAPIProp** implementation.</span></span> <span data-ttu-id="eb1ea-132">クライアントがいずれかのインターフェイスを使用してオブジェクトのプロパティを操作することがあります。</span><span class="sxs-lookup"><span data-stu-id="eb1ea-132">The client should be able to work with the object's properties using either interface.</span></span> 
    

