---
title: ホストアドレス帳プロバイダーとして機能
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f06a1034-ee49-4a09-831e-9752713228a8
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 202d4b4391de7553e39e50dc527df5502ebcefb3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331270"
---
# <a name="acting-as-a-host-address-book-provider"></a><span data-ttu-id="02ed6-103">ホストアドレス帳プロバイダーとして機能</span><span class="sxs-lookup"><span data-stu-id="02ed6-103">Acting as a Host Address Book Provider</span></span>

  
  
<span data-ttu-id="02ed6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="02ed6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="02ed6-105">ホストプロバイダーは、コンテナー内の他のプロバイダーからの受信者を含むアドレス帳プロバイダーで、その他のプロバイダーによって受信者の実装を部分的に管理することに依存します。</span><span class="sxs-lookup"><span data-stu-id="02ed6-105">A host provider is an address book provider that includes recipients from other providers in its containers and relies on the implementation of the recipients by the other providers to partially control their maintenance.</span></span> <span data-ttu-id="02ed6-106">ホストプロバイダーは、これらの外部受信者のテンプレート識別子を使用して、これらの受信者のデータを外部プロバイダーのコードにバインドします。</span><span class="sxs-lookup"><span data-stu-id="02ed6-106">A host provider uses the template identifiers of these foreign recipients to bind the data for these recipients to code in the foreign provider.</span></span> <span data-ttu-id="02ed6-107">このバインドプロセスは、プロバイダーが受信者の**PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) プロパティを取得し、 [imapisupport:: OpenTemplateID](imapisupport-opentemplateid.md)の呼び出しに渡すと開始されます。</span><span class="sxs-lookup"><span data-stu-id="02ed6-107">This binding process is initiated when your provider retrieves the **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property of a recipient and passes it in a call to [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md).</span></span> 
  
<span data-ttu-id="02ed6-108">プロバイダーが**imapisupport:: OpenTemplateID**を呼び出すと、MAPI はテンプレート識別子内の**MAPIUID**とプロバイダーによって登録された**MAPIUID**を照合し、プロバイダーの[IABLogon:: OpenTemplateID](iablogon-opentemplateid.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="02ed6-108">When your provider calls **IMAPISupport::OpenTemplateID**, MAPI matches the **MAPIUID** within the template identifier with a **MAPIUID** registered by a provider and calls the provider's [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) method.</span></span> <span data-ttu-id="02ed6-109">外部プロバイダーは、プロバイダーの property オブジェクトへのポインター、独自の property オブジェクトの実装、またはプロバイダーのオブジェクトをラップする実装に返すことができます。</span><span class="sxs-lookup"><span data-stu-id="02ed6-109">The foreign provider might return a pointer to your provider's property object, to its own property object implementation, or to an implementation that wraps your provider's object.</span></span> <span data-ttu-id="02ed6-110">返されるポインターは、 _lppMAPIPropNew_パラメーターの内容に配置されます。</span><span class="sxs-lookup"><span data-stu-id="02ed6-110">The returned pointer is placed in the contents of the  _lppMAPIPropNew_ parameter.</span></span> 
  
<span data-ttu-id="02ed6-111">プロバイダーは、FILL_ENTRY フラグセットを使用して**imapisupport:: OpenTemplateID**を呼び出すかどうかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="02ed6-111">Your provider can choose whether or not to call **IMAPISupport::OpenTemplateID** with the FILL_ENTRY flag set.</span></span> <span data-ttu-id="02ed6-112">受信者が作成されているとき、またはプロバイダーが受信者のプロパティを更新してから長い時間が経過したときに、このフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="02ed6-112">Set this flag when the recipient is being created or when a long time has passed since your provider has refreshed the recipient's properties.</span></span> <span data-ttu-id="02ed6-113">FILL_ENTRY フラグの一般的な使用方法は、プロバイダー内の受信者を元のと同期された状態に保つことです。</span><span class="sxs-lookup"><span data-stu-id="02ed6-113">A common use of the FILL_ENTRY flag is to keep a recipient in your provider synchronized with the original.</span></span> <span data-ttu-id="02ed6-114">この種類の同期スケジュールを実装すると、パフォーマンスが向上します。</span><span class="sxs-lookup"><span data-stu-id="02ed6-114">Implementing this type of synchronization schedule enhances performance.</span></span> 
  
 <span data-ttu-id="02ed6-115">**外部の受信者の同期を維持するには**</span><span class="sxs-lookup"><span data-stu-id="02ed6-115">**To keep a foreign recipient synchronized**</span></span>
  
1. <span data-ttu-id="02ed6-116">定期的に更新するための適切な間隔を決定します。</span><span class="sxs-lookup"><span data-stu-id="02ed6-116">Determine an appropriate interval for periodic updates.</span></span> 
    
2. <span data-ttu-id="02ed6-117">タイムスタンプ imapisupport への各呼び出し[:: OpenTemplateID](imapisupport-opentemplateid.md)。</span><span class="sxs-lookup"><span data-stu-id="02ed6-117">Timestamp each call to [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md).</span></span> 
    
3. <span data-ttu-id="02ed6-118">前回の呼び出しからの経過時間に基づいて、完全な更新を実行する必要があるかどうかを評価します。</span><span class="sxs-lookup"><span data-stu-id="02ed6-118">Evaluate whether or not it is necessary to perform a full update based on the amount of time that has expired since the last call.</span></span> <span data-ttu-id="02ed6-119">完全な更新が必要な場合は、FILL_ENTRY フラグを使用して**imapisupport:: OpenTemplateID**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="02ed6-119">If a full update is necessary, call **IMAPISupport::OpenTemplateID** with the FILL_ENTRY flag.</span></span> <span data-ttu-id="02ed6-120">必要でない場合は、呼び出しにフラグを設定しないようにします。</span><span class="sxs-lookup"><span data-stu-id="02ed6-120">If it is not necessary, do not set the flag on the call.</span></span> 
    
<span data-ttu-id="02ed6-121">クライアントがコピーされた受信者のプロパティの1つに対して要求を行うと、プロバイダーは要求を処理するか、または外部プロバイダーから提供されたコードを使用するかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="02ed6-121">When a client makes a request for one of the copied recipient's properties, your provider can choose whether to handle the request itself or use the code supplied by the foreign provider.</span></span> <span data-ttu-id="02ed6-122">プロバイダーは、外部プロバイダーが、imapiprop [:: openproperty](imapiprop-openproperty.md)を除く**imapiprop**を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="02ed6-122">Your provider can expect the foreign provider to intercept most, if not all, calls to **IMAPIProp** except for [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span> <span data-ttu-id="02ed6-123">**PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) プロパティを要求する**openproperty**への呼び出しは、常にプロバイダーに転送されます。</span><span class="sxs-lookup"><span data-stu-id="02ed6-123">A call to **OpenProperty** requesting the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property is always forwarded to your provider.</span></span>
  
 <span data-ttu-id="02ed6-124">**テンプレート識別子コードにアクセスするには**</span><span class="sxs-lookup"><span data-stu-id="02ed6-124">**To access template identifier code**</span></span>
  
1. <span data-ttu-id="02ed6-125">受信者を開き、 [imapiprop:: GetProps](imapiprop-getprops.md)メソッドを呼び出して、 **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) プロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="02ed6-125">Open the recipient and call its [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property.</span></span> <span data-ttu-id="02ed6-126">**PR_TEMPLATEID**を使用できないために**GetProps**が失敗した場合、外部プロバイダーは、この受信者のテンプレート識別子と関連コードをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="02ed6-126">If **GetProps** fails because **PR_TEMPLATEID** is unavailable, the foreign provider does not support a template identifier and related code for this recipient.</span></span> <span data-ttu-id="02ed6-127">プロバイダーは、すべてのメンテナンスで受信者の実装を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="02ed6-127">Your provider will need to use its implementation of the recipient for all maintenance.</span></span> 
    
2. <span data-ttu-id="02ed6-128">テンプレート識別子が**GetProps**から返された場合は、 **imapiprop:: OpenTemplateID**メソッドの呼び出しで、受信者の**imapiprop**実装へのポインターを渡します。</span><span class="sxs-lookup"><span data-stu-id="02ed6-128">If the template identifier is returned from **GetProps**, pass it and a pointer to the recipient's **IMAPIProp** implementation in a call to the **IMAPISupport::OpenTemplateID** method.</span></span> <span data-ttu-id="02ed6-129">受信者のプロパティのほとんどまたはすべてを更新する必要がある場合、または更新されていない場合には、FILL_ENTRY フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="02ed6-129">Set the FILL_ENTRY flag if most or all of the recipient's properties need to be updated, such as at creation time or if they have not been updated for a while.</span></span> 
    
3. <span data-ttu-id="02ed6-130">**OpenTemplateID**が外部プロバイダーの**imapiprop**実装を返す場合は、この実装へのポインターをクライアントに返します。</span><span class="sxs-lookup"><span data-stu-id="02ed6-130">If **OpenTemplateID** returns the foreign provider's **IMAPIProp** implementation, return to the client a pointer to this implementation.</span></span> 
    
4. <span data-ttu-id="02ed6-131">**OpenTemplateID**が実装を返さない場合は、通常、外部プロバイダーがプロファイルに含まれていないため、プロバイダーの**imapiprop**実装へのポインターをクライアントに返します。</span><span class="sxs-lookup"><span data-stu-id="02ed6-131">If **OpenTemplateID** does not return an implementation, typically because the foreign provider is not in the profile, return to the client a pointer to your provider's **IMAPIProp** implementation.</span></span> <span data-ttu-id="02ed6-132">クライアントは、いずれかのインターフェイスを使用して、オブジェクトのプロパティを操作できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="02ed6-132">The client should be able to work with the object's properties using either interface.</span></span> 
    

