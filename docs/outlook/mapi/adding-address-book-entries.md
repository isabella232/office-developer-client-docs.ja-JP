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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421341"
---
# <a name="adding-address-book-entries"></a><span data-ttu-id="4ed70-103">アドレス帳エントリの追加</span><span class="sxs-lookup"><span data-stu-id="4ed70-103">Adding Address Book Entries</span></span>

  
  
<span data-ttu-id="4ed70-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4ed70-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4ed70-105">メッセージング ユーザーまたは配布リストをコンテナーに追加するには、クライアントが [IAddrBook::NewEntry](iaddrbook-newentry.md)を呼び出すか、プロバイダーが _lpEIDContainer_ パラメーターのターゲット コンテナーのエントリ識別子を使用して [IMAPISupport::NewEntry](imapisupport-newentry.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="4ed70-105">To add a messaging user or distribution list to a container, a client calls [IAddrBook::NewEntry](iaddrbook-newentry.md) or a provider calls [IMAPISupport::NewEntry](imapisupport-newentry.md) with the entry identifier of the target container in the  _lpEIDContainer_ parameter.</span></span> <span data-ttu-id="4ed70-106">MAPI は、コンテナーの [IABContainer::CreateEntry](iabcontainer-createentry.md) メソッドを呼び出して、1 回きりテーブルから 1 回のテンプレートを使用してエントリを作成します。</span><span class="sxs-lookup"><span data-stu-id="4ed70-106">MAPI in turn calls the container's [IABContainer::CreateEntry](iabcontainer-createentry.md) method to create the entry using a one-off template from a one-off table.</span></span> <span data-ttu-id="4ed70-107">1 回限定のテンプレートを使用すると、クライアントは特定の種類の新しい受信者を作成できます。</span><span class="sxs-lookup"><span data-stu-id="4ed70-107">A one-off template allows the client to create a new recipient of a particular type.</span></span> <span data-ttu-id="4ed70-108">ほとんどのフィールドは編集可能です。</span><span class="sxs-lookup"><span data-stu-id="4ed70-108">Most of the fields are editable.</span></span> <span data-ttu-id="4ed70-109">_lpEntryID_ パラメーターが示すテンプレートは、プロバイダーが提供するテンプレートか、プロバイダーが外部テンプレートをサポートしている場合は、外部プロバイダーのテンプレートである可能性があります。</span><span class="sxs-lookup"><span data-stu-id="4ed70-109">The template pointed to by the  _lpEntryID_ parameter might be one that your provider supplies or it might be a template from a foreign provider, if your provider supports foreign templates.</span></span> <span data-ttu-id="4ed70-110">外部テンプレートから受信者を作成できるプロバイダーの **CreateEntry** の実装は、できないプロバイダーの実装よりも常に複雑です。</span><span class="sxs-lookup"><span data-stu-id="4ed70-110">Implementations of **CreateEntry** for providers that can create recipients from a foreign template are always more complex than implementations for providers that cannot.</span></span> 
  
 <span data-ttu-id="4ed70-111">**IABContainer を実装するには::CreateEntry**</span><span class="sxs-lookup"><span data-stu-id="4ed70-111">**To implement IABContainer::CreateEntry**</span></span>
  
1. <span data-ttu-id="4ed70-112">lpEntryID パラメーターで指定されたエントリ識別子  _の種類を決定_ します。</span><span class="sxs-lookup"><span data-stu-id="4ed70-112">Determine the type of entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
2. <span data-ttu-id="4ed70-113">エントリ識別子が、プロバイダーが所有するメッセージング ユーザー、配布リスト、またはアドレス帳コンテナーのテンプレートを表す場合:</span><span class="sxs-lookup"><span data-stu-id="4ed70-113">If the entry identifier represents a template for a messaging user, distribution list, or address book container owned by your provider:</span></span>
    
1. <span data-ttu-id="4ed70-114">適切なオブジェクトを作成して初期化します。</span><span class="sxs-lookup"><span data-stu-id="4ed70-114">Create and initialize the appropriate object.</span></span> <span data-ttu-id="4ed70-115">プロバイダーは、必要に応じていくつかの初期プロパティを設定できます。</span><span class="sxs-lookup"><span data-stu-id="4ed70-115">Your provider can set some initial properties if desired.</span></span> <span data-ttu-id="4ed70-116">これらのプロパティは、作成する受信者の種類によって異なります。</span><span class="sxs-lookup"><span data-stu-id="4ed70-116">These properties depend on the type of recipient being created.</span></span> 
    
2. <span data-ttu-id="4ed70-117">_lppMAPIPropEntry_ パラメーターの内容でオブジェクトの実装へのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="4ed70-117">Return a pointer to the object's implementation in the contents of the  _lppMAPIPropEntry_ parameter.</span></span> 
    
3. <span data-ttu-id="4ed70-118">エントリ識別子が外部プロバイダーのテンプレートを表す場合:</span><span class="sxs-lookup"><span data-stu-id="4ed70-118">If the entry identifier represents a template for a foreign provider:</span></span>
    
1. <span data-ttu-id="4ed70-119">[IMAPISupport::OpenEntry を呼び出して](imapisupport-openentry.md)、外部オブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="4ed70-119">Call [IMAPISupport::OpenEntry](imapisupport-openentry.md) to open the foreign object.</span></span> 
    
2. <span data-ttu-id="4ed70-120">オブジェクトの [IMAPIProp::GetProps](imapiprop-getprops.md) メソッドを呼び出し、プロパティ タグ配列に NULL を渡してプロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="4ed70-120">Call the object's [IMAPIProp::GetProps](imapiprop-getprops.md) method, passing NULL for the property tag array, to retrieve its properties.</span></span> 
    
3. <span data-ttu-id="4ed70-121">**GetProps** から返されるプロパティ値配列を編集するには、新しいオブジェクトに適用されないすべてのプロパティのプロパティ タグを PR_NULL に変更し、転送する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4ed70-121">Edit the property value array returned from **GetProps** by changing the property tag to PR_NULL for all properties that will not apply to the new object and should not be transferred.</span></span> 
    
4. <span data-ttu-id="4ed70-122">新しいオブジェクトのエントリ識別子を作成します。</span><span class="sxs-lookup"><span data-stu-id="4ed70-122">Create an entry identifier for the new object.</span></span> 
    
5. <span data-ttu-id="4ed70-123">メッセージング ユーザーまたは配布リストのいずれかの適切な種類の新しいオブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="4ed70-123">Create a new object of the appropriate type, either messaging user or distribution list.</span></span>
    
6. <span data-ttu-id="4ed70-124">既定のプロパティを設定して、新しいオブジェクトを初期化します。</span><span class="sxs-lookup"><span data-stu-id="4ed70-124">Initialize the new object by setting default properties.</span></span>
    
7. <span data-ttu-id="4ed70-125">外部オブジェクトがプロパティ ([PidTagTemplateid](pidtagtemplateid-canonical-property.md) **)** プロパティPR_TEMPLATEIDサポートするかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="4ed70-125">Check whether or not the foreign object supports the **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property.</span></span> 
    
8. <span data-ttu-id="4ed70-126">外部オブジェクトが **PR_TEMPLATEID** をサポートしている場合は [、IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) を呼び出して、外部プロバイダーからプロパティ オブジェクト インターフェイスを取得し  _、lppMAPIPropEntry_ パラメーターの内容を外部プロパティ オブジェクトの実装に設定します。</span><span class="sxs-lookup"><span data-stu-id="4ed70-126">If the foreign object supports **PR_TEMPLATEID**, call [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) to retrieve a property object interface from the foreign provider and set the contents of the  _lppMAPIPropEntry_ parameter to the foreign property object implementation.</span></span> 
    
9. <span data-ttu-id="4ed70-127">外部オブジェクトが **PR_TEMPLATEIDをサポート** していない場合は  _、lppMAPIPropEntry_ パラメーターの内容を、プロバイダーの新しいオブジェクトの実装に設定します。</span><span class="sxs-lookup"><span data-stu-id="4ed70-127">If the foreign object does not support **PR_TEMPLATEID**, set the contents of the  _lppMAPIPropEntry_ parameter to your provider's implementation of the new object.</span></span> 
    
10. <span data-ttu-id="4ed70-128">_lppMAPIPropEntry_ パラメーターが指すオブジェクトの [IMAPIProp::SetProps](imapiprop-setprops.md)メソッドを呼び出して、外部オブジェクトから適切なプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="4ed70-128">Call the [IMAPIProp::SetProps](imapiprop-setprops.md) method of the object pointed to by the  _lppMAPIPropEntry_ parameter to set the appropriate properties from the foreign object.</span></span> 
    

