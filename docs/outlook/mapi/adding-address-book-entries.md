---
title: アドレス帳エントリの追加
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 63444a65-d56a-4dbd-9aa6-e60f18ba8104
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 8dc82a99ee088d42c076ca9a3a75eac6553f7d35
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331879"
---
# <a name="adding-address-book-entries"></a><span data-ttu-id="f7c25-103">アドレス帳エントリの追加</span><span class="sxs-lookup"><span data-stu-id="f7c25-103">Adding Address Book Entries</span></span>

  
  
<span data-ttu-id="f7c25-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f7c25-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f7c25-105">メッセージングユーザーまたは配布リストをコンテナーに追加するために、クライアントは[IAddrBook:: newentry](iaddrbook-newentry.md)またはプロバイダーから[imapisupport:: newentry](imapisupport-newentry.md)を呼び出します。 _lpeidcontainer_パラメーターには、ターゲットコンテナーのエントリ id を指定します。</span><span class="sxs-lookup"><span data-stu-id="f7c25-105">To add a messaging user or distribution list to a container, a client calls [IAddrBook::NewEntry](iaddrbook-newentry.md) or a provider calls [IMAPISupport::NewEntry](imapisupport-newentry.md) with the entry identifier of the target container in the  _lpEIDContainer_ parameter.</span></span> <span data-ttu-id="f7c25-106">次に、MAPI は、1回限りのテーブルから1回限りのテンプレートを使用してエントリを作成するために、コンテナーの[IABContainer:: createentry](iabcontainer-createentry.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f7c25-106">MAPI in turn calls the container's [IABContainer::CreateEntry](iabcontainer-createentry.md) method to create the entry using a one-off template from a one-off table.</span></span> <span data-ttu-id="f7c25-107">1回限りのテンプレートでは、クライアントは特定の種類の新しい受信者を作成できます。</span><span class="sxs-lookup"><span data-stu-id="f7c25-107">A one-off template allows the client to create a new recipient of a particular type.</span></span> <span data-ttu-id="f7c25-108">ほとんどのフィールドは編集できます。</span><span class="sxs-lookup"><span data-stu-id="f7c25-108">Most of the fields are editable.</span></span> <span data-ttu-id="f7c25-109">_lな tryid_パラメーターで指定されているテンプレートは、プロバイダーが外部テンプレートをサポートしている場合に、プロバイダーが提供するか、外部プロバイダーからのテンプレートである可能性があります。</span><span class="sxs-lookup"><span data-stu-id="f7c25-109">The template pointed to by the  _lpEntryID_ parameter might be one that your provider supplies or it might be a template from a foreign provider, if your provider supports foreign templates.</span></span> <span data-ttu-id="f7c25-110">外部テンプレートから受信者を作成できるプロバイダーの**createentry**の実装は、常に、できないプロバイダーの実装よりも複雑です。</span><span class="sxs-lookup"><span data-stu-id="f7c25-110">Implementations of **CreateEntry** for providers that can create recipients from a foreign template are always more complex than implementations for providers that cannot.</span></span> 
  
 <span data-ttu-id="f7c25-111">**IABContainer:: createentry を実装するには**</span><span class="sxs-lookup"><span data-stu-id="f7c25-111">**To implement IABContainer::CreateEntry**</span></span>
  
1. <span data-ttu-id="f7c25-112">_lpentryid_パラメーターで指定されたエントリ id の種類を決定します。</span><span class="sxs-lookup"><span data-stu-id="f7c25-112">Determine the type of entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
2. <span data-ttu-id="f7c25-113">入力識別子が、プロバイダーが所有するメッセージングユーザー、配布リスト、またはアドレス帳コンテナーのテンプレートを表している場合:</span><span class="sxs-lookup"><span data-stu-id="f7c25-113">If the entry identifier represents a template for a messaging user, distribution list, or address book container owned by your provider:</span></span>
    
1. <span data-ttu-id="f7c25-114">適切なオブジェクトを作成し、初期化します。</span><span class="sxs-lookup"><span data-stu-id="f7c25-114">Create and initialize the appropriate object.</span></span> <span data-ttu-id="f7c25-115">プロバイダーは、必要に応じて、いくつかの初期プロパティを設定できます。</span><span class="sxs-lookup"><span data-stu-id="f7c25-115">Your provider can set some initial properties if desired.</span></span> <span data-ttu-id="f7c25-116">これらのプロパティは、作成される受信者の種類によって異なります。</span><span class="sxs-lookup"><span data-stu-id="f7c25-116">These properties depend on the type of recipient being created.</span></span> 
    
2. <span data-ttu-id="f7c25-117">_lppMAPIPropEntry_パラメーターの内容で、オブジェクトの実装へのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="f7c25-117">Return a pointer to the object's implementation in the contents of the  _lppMAPIPropEntry_ parameter.</span></span> 
    
3. <span data-ttu-id="f7c25-118">エントリ識別子が外部プロバイダーのテンプレートを表す場合:</span><span class="sxs-lookup"><span data-stu-id="f7c25-118">If the entry identifier represents a template for a foreign provider:</span></span>
    
1. <span data-ttu-id="f7c25-119">open [imapisupport:: openentry](imapisupport-openentry.md)を呼び出して、外部オブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="f7c25-119">Call [IMAPISupport::OpenEntry](imapisupport-openentry.md) to open the foreign object.</span></span> 
    
2. <span data-ttu-id="f7c25-120">プロパティタグ配列に NULL を渡すオブジェクトの[imapiprop:: GetProps](imapiprop-getprops.md)メソッドを呼び出して、プロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="f7c25-120">Call the object's [IMAPIProp::GetProps](imapiprop-getprops.md) method, passing NULL for the property tag array, to retrieve its properties.</span></span> 
    
3. <span data-ttu-id="f7c25-121">新しいオブジェクトに適用されず、転送されないすべてのプロパティのプロパティタグを PR_NULL に変更することによって、 **GetProps**から返されたプロパティ値の配列を編集します。</span><span class="sxs-lookup"><span data-stu-id="f7c25-121">Edit the property value array returned from **GetProps** by changing the property tag to PR_NULL for all properties that will not apply to the new object and should not be transferred.</span></span> 
    
4. <span data-ttu-id="f7c25-122">新しいオブジェクトのエントリ識別子を作成します。</span><span class="sxs-lookup"><span data-stu-id="f7c25-122">Create an entry identifier for the new object.</span></span> 
    
5. <span data-ttu-id="f7c25-123">メッセージユーザーまたは配布リストのいずれかで、適切な種類の新しいオブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="f7c25-123">Create a new object of the appropriate type, either messaging user or distribution list.</span></span>
    
6. <span data-ttu-id="f7c25-124">既定のプロパティを設定して、新しいオブジェクトを初期化します。</span><span class="sxs-lookup"><span data-stu-id="f7c25-124">Initialize the new object by setting default properties.</span></span>
    
7. <span data-ttu-id="f7c25-125">外部オブジェクトが**PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) プロパティをサポートしているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="f7c25-125">Check whether or not the foreign object supports the **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property.</span></span> 
    
8. <span data-ttu-id="f7c25-126">外部オブジェクトが**PR_TEMPLATEID**をサポートしている場合は、 [imapisupport:: OpenTemplateID](imapisupport-opentemplateid.md)を呼び出して、外部プロバイダーから property オブジェクトインターフェイスを取得し、 _lppMAPIPropEntry_パラメーターの内容を foreign プロパティに設定します。オブジェクトの実装。</span><span class="sxs-lookup"><span data-stu-id="f7c25-126">If the foreign object supports **PR_TEMPLATEID**, call [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) to retrieve a property object interface from the foreign provider and set the contents of the  _lppMAPIPropEntry_ parameter to the foreign property object implementation.</span></span> 
    
9. <span data-ttu-id="f7c25-127">外部オブジェクトが**PR_TEMPLATEID**をサポートしていない場合は、 _lppMAPIPropEntry_パラメーターの内容をプロバイダーの新しいオブジェクトの実装に設定します。</span><span class="sxs-lookup"><span data-stu-id="f7c25-127">If the foreign object does not support **PR_TEMPLATEID**, set the contents of the  _lppMAPIPropEntry_ parameter to your provider's implementation of the new object.</span></span> 
    
10. <span data-ttu-id="f7c25-128">_lppMAPIPropEntry_パラメーターによって指定されるオブジェクトの[imapiprop:: setprops](imapiprop-setprops.md)メソッドを呼び出して、外部オブジェクトから適切なプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="f7c25-128">Call the [IMAPIProp::SetProps](imapiprop-setprops.md) method of the object pointed to by the  _lppMAPIPropEntry_ parameter to set the appropriate properties from the foreign object.</span></span> 
    

