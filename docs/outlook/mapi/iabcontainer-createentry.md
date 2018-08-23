---
title: IABContainerCreateEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABContainer.CreateEntry
api_type:
- COM
ms.assetid: ea1daf74-d9e3-4304-bf5d-889afeea6ae9
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: acf9cee9bf0713b909b0d82fc606b015ac28474e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800354"
---
# <a name="iabcontainercreateentry"></a><span data-ttu-id="6e6ea-103">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="6e6ea-103">IABContainer::CreateEntry</span></span>

  
  
<span data-ttu-id="6e6ea-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6e6ea-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6e6ea-105">メッセージングのユーザー、配布リスト、または別のコンテナーにすることができますが、新しいエントリを作成します。</span><span class="sxs-lookup"><span data-stu-id="6e6ea-105">Creates a new entry, which can be a messaging user, a distribution list, or another container.</span></span>
  
```cpp
HRESULT CreateEntry(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulCreateFlags,
  LPMAPIPROP FAR * lppMAPIPropEntry
);
```

## <a name="parameters"></a><span data-ttu-id="6e6ea-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6e6ea-106">Parameters</span></span>

 <span data-ttu-id="6e6ea-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="6e6ea-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="6e6ea-108">[in]_LpEntryID_パラメーターで指定されたエントリの識別子内のバイト数。</span><span class="sxs-lookup"><span data-stu-id="6e6ea-108">[in] The count of the bytes in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="6e6ea-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="6e6ea-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="6e6ea-110">[in]特定の種類の新しいエントリを作成するためのテンプレートのエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="6e6ea-110">[in] A pointer to the entry identifier of a template for creating new entries of a particular type.</span></span> 
    
 <span data-ttu-id="6e6ea-111">_ulCreateFlags_</span><span class="sxs-lookup"><span data-stu-id="6e6ea-111">_ulCreateFlags_</span></span>
  
> <span data-ttu-id="6e6ea-112">[in]エントリの作成を実行する方法を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="6e6ea-112">[in] A bitmask of flags that controls how entry creation is performed.</span></span> <span data-ttu-id="6e6ea-113">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="6e6ea-113">The following flags can be set:</span></span>
    
<span data-ttu-id="6e6ea-114">CREATE_CHECK_DUP_LOOSE</span><span class="sxs-lookup"><span data-stu-id="6e6ea-114">CREATE_CHECK_DUP_LOOSE</span></span> 
  
> <span data-ttu-id="6e6ea-115">緩やかなレベルの重複するエントリのチェックを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6e6ea-115">A loose level of duplicate entry checking should be performed.</span></span> <span data-ttu-id="6e6ea-116">緩やかな重複するエントリのチェックの実装は、特定のプロバイダーです。</span><span class="sxs-lookup"><span data-stu-id="6e6ea-116">The implementation of loose duplicate entry checking is provider specific.</span></span> <span data-ttu-id="6e6ea-117">などのプロバイダーは、同じ 2 つのエントリの表示名と緩やかな一致を定義できます。</span><span class="sxs-lookup"><span data-stu-id="6e6ea-117">For example, a provider can define a loose match as any two entries that have the same display name.</span></span>
    
<span data-ttu-id="6e6ea-118">CREATE_CHECK_DUP_STRICT</span><span class="sxs-lookup"><span data-stu-id="6e6ea-118">CREATE_CHECK_DUP_STRICT</span></span> 
  
> <span data-ttu-id="6e6ea-119">厳密なレベルの重複するエントリのチェックを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6e6ea-119">A strict level of duplicate entry checking should be performed.</span></span> <span data-ttu-id="6e6ea-120">厳密な重複するエントリのチェックの実装は、特定のプロバイダーです。</span><span class="sxs-lookup"><span data-stu-id="6e6ea-120">The implementation of strict duplicate entry checking is provider specific.</span></span> <span data-ttu-id="6e6ea-121">などのプロバイダーは、両方同じ 2 つのエントリの名前とメッセージのアドレスを表示すると、厳密な一致を定義できます。</span><span class="sxs-lookup"><span data-stu-id="6e6ea-121">For example, a provider can define a strict match as any two entries that have both the same display name and messaging address.</span></span>
    
<span data-ttu-id="6e6ea-122">CREATE_REPLACE</span><span class="sxs-lookup"><span data-stu-id="6e6ea-122">CREATE_REPLACE</span></span> 
  
> <span data-ttu-id="6e6ea-123">2 つ重複していることが判明した場合、新しいエントリは既存のものに置き換えてください。</span><span class="sxs-lookup"><span data-stu-id="6e6ea-123">A new entry should replace an existing one if it is determined that the two are duplicates.</span></span>
    
 <span data-ttu-id="6e6ea-124">_lppMAPIPropEntry_</span><span class="sxs-lookup"><span data-stu-id="6e6ea-124">_lppMAPIPropEntry_</span></span>
  
> <span data-ttu-id="6e6ea-125">[out]新しく作成されたエントリへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="6e6ea-125">[out] A pointer to a pointer to the newly created entry.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6e6ea-126">�߂�l</span><span class="sxs-lookup"><span data-stu-id="6e6ea-126">Return value</span></span>

<span data-ttu-id="6e6ea-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="6e6ea-127">S_OK</span></span> 
  
> <span data-ttu-id="6e6ea-128">新しいエントリが正しく作成されました。</span><span class="sxs-lookup"><span data-stu-id="6e6ea-128">The new entry was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6e6ea-129">注釈</span><span class="sxs-lookup"><span data-stu-id="6e6ea-129">Remarks</span></span>

<span data-ttu-id="6e6ea-130">**IABContainer::CreateEntry**メソッドは、インターフェイスの実装のエントリにさらにアクセスするためにポインターを返す、指定したコンテナーに特定の種類の新しいエントリを作成します。</span><span class="sxs-lookup"><span data-stu-id="6e6ea-130">The **IABContainer::CreateEntry** method creates a new entry of a particular type in the specified container, returning a pointer to an interface implementation for further access to the entry.</span></span> <span data-ttu-id="6e6ea-131">新しいエントリを作成するには、その一時テーブルで公開されている、利用可能なテンプレートのコンテナーの一覧から選択されているテンプレートを使用します。</span><span class="sxs-lookup"><span data-stu-id="6e6ea-131">The new entry is created by using a template that has been selected from the container's list of available templates published in its one-off table.</span></span> <span data-ttu-id="6e6ea-132">呼び出し元の[IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出すと、 **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) のプロパティを要求しているコンテナーの一時テーブルにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="6e6ea-132">Callers access a container's one-off table by calling its [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method and requesting the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="6e6ea-133">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="6e6ea-133">Notes to implementers</span></span>

<span data-ttu-id="6e6ea-134">**IABContainer::CreateEntry**メソッドをサポートするすべてのコンテナーは、変更可能である必要があります。</span><span class="sxs-lookup"><span data-stu-id="6e6ea-134">All containers that support the **IABContainer::CreateEntry** method must be modifiable.</span></span> <span data-ttu-id="6e6ea-135">変更可能であることを示すには、その**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) プロパティで、コンテナーの AB_MODIFIABLE フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="6e6ea-135">Set your container's AB_MODIFIABLE flag in its **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) property to indicate that it is modifiable.</span></span> 
  
<span data-ttu-id="6e6ea-136">_UlCreateFlags_フラグをすべてサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6e6ea-136">You should support all of the  _ulCreateFlags_ flags.</span></span> <span data-ttu-id="6e6ea-137">ただし、解釈し、これらのフラグの使用は、特定の実装-は、実装のコンテキストで意味する CREATE_CHECK_DUP_LOOSE と CREATE_CHECK_DUP_STRICT の意味を判断できます。</span><span class="sxs-lookup"><span data-stu-id="6e6ea-137">However, the interpretation and use of these flags is implementation specific—that is, you can determine what the semantics of CREATE_CHECK_DUP_LOOSE and CREATE_CHECK_DUP_STRICT mean in the context of your implementation.</span></span> <span data-ttu-id="6e6ea-138">できないかのエントリは、重複しているかどうかを判断できませんを作成するエントリを常に許可します。</span><span class="sxs-lookup"><span data-stu-id="6e6ea-138">If you cannot or do not determine whether an entry is a duplicate, always allow the entry to be created.</span></span> 
  
<span data-ttu-id="6e6ea-139">プロバイダーによって実装厳密なエントリの表示名を照合することによってチェックがメッセージング アドレス、および検索キーのエントリです。他のプロバイダーでは、名前とアドレスを表示するのには一致するものを制限します。</span><span class="sxs-lookup"><span data-stu-id="6e6ea-139">Some providers implement strict entry checking by matching the display name, messaging address, and search key in an entry; other providers limit the match to display name and address.</span></span> <span data-ttu-id="6e6ea-140">緩やかなエントリのチェックは、多くの場合のみの表示名を確認することによって実装されます。</span><span class="sxs-lookup"><span data-stu-id="6e6ea-140">Loose entry checking is often implemented by checking the display name only.</span></span> 
  
## <a name="notes-to-host-address-book-provider-implementers"></a><span data-ttu-id="6e6ea-141">アドレス帳プロバイダーの実装をホストするためのメモ</span><span class="sxs-lookup"><span data-stu-id="6e6ea-141">Notes to Host Address Book Provider Implementers</span></span>

<span data-ttu-id="6e6ea-142">コンテナーは、他のプロバイダーのテンプレートの中から、エントリを作成できます、 **CreateEntry**の実装は、作成されたエントリに関連付けられているプロパティの一部またはすべてのストレージを提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6e6ea-142">If your container can create entries from the templates of other providers, your implementation of **CreateEntry** should provide storage for some or all of the properties associated with the created entries.</span></span> <span data-ttu-id="6e6ea-143">などのエントリの**PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) のプロパティの記憶域を提供する場合は、外部プロバイダーに依存することがなくその [詳細] ダイアログ ボックスを生成できます。</span><span class="sxs-lookup"><span data-stu-id="6e6ea-143">For example, if you provide storage for an entry's **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property, you can generate its details dialog box without having to depend on the foreign provider.</span></span> 
  
<span data-ttu-id="6e6ea-144">コンテナーには、 **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) のプロパティをサポートするためのエントリを作成できます、 **CreateEntry**の実装が、次の操作にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6e6ea-144">If your container can create entries that support the **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property, your implementation of **CreateEntry** must do the following:</span></span> 
  
1. <span data-ttu-id="6e6ea-145">[IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="6e6ea-145">Call the [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) method.</span></span> <span data-ttu-id="6e6ea-146">**OpenTemplateID**は、外部プロバイダーのエントリが作成される新しいエントリにバインドするコードを有効にします。</span><span class="sxs-lookup"><span data-stu-id="6e6ea-146">**OpenTemplateID** enables the foreign provider's code for the entry to bind to the new entry being created.</span></span> <span data-ttu-id="6e6ea-147">外部プロバイダーでは、ホストのアドレス帳プロバイダーのコンテナー内にそのテンプレートから作成されたエントリの制御を維持するには、このバインド処理をサポートします。</span><span class="sxs-lookup"><span data-stu-id="6e6ea-147">Foreign providers support this binding process to maintain control over entries created from their templates into the containers of host address book providers.</span></span> 
    
2. <span data-ttu-id="6e6ea-148">、必要な初期化を実行し、新しいオブジェクトにすべての**OpenTemplateID**から、 _lppMAPIPropNew_パラメーターで返されるオブジェクトを外部のプロバイダーのエントリからプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="6e6ea-148">Perform any necessary initialization, and populate the new object with all of the properties from the entry in the foreign provider that the object returned in the  _lppMAPIPropNew_ parameter from **OpenTemplateID**.</span></span>
    
<span data-ttu-id="6e6ea-149">**OpenTemplateID**が成功した場合は、 _lpMAPIPropData_パラメーターで指定された実装に直接ではなく、 _lppMAPIPropNew_パラメーターで指定された実装にプロパティをコピーします。</span><span class="sxs-lookup"><span data-stu-id="6e6ea-149">If **OpenTemplateID** succeeds, copy the properties to the implementation pointed to by the  _lppMAPIPropNew_ parameter rather than directly to the implementation pointed to by the  _lpMAPIPropData_ parameter.</span></span> <span data-ttu-id="6e6ea-150">外部プロバイダーから他の任意のエントリを同じように、オフラインで使用する新しいエントリを初期化します。</span><span class="sxs-lookup"><span data-stu-id="6e6ea-150">Initialize the new entry for offline use as you would any other entry from a foreign provider.</span></span> 
  
<span data-ttu-id="6e6ea-151">**OpenTemplateID**には、エラーが返されます、 **CreateEntry**が失敗する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6e6ea-151">If **OpenTemplateID** returns an error, **CreateEntry** should fail.</span></span> <span data-ttu-id="6e6ea-152">作成するエントリを許可しません。</span><span class="sxs-lookup"><span data-stu-id="6e6ea-152">Do not allow the entry to be created.</span></span> <span data-ttu-id="6e6ea-153">外部のプロバイダーは、プロバイダーで、データに関する判断を行うことができます、ために、外部のプロバイダーに正常にバインドされていないいるテンプレート識別子を持つエントリは作成できません。</span><span class="sxs-lookup"><span data-stu-id="6e6ea-153">Because the foreign provider can make assumptions about the data in your provider, do not create an entry with a template identifier that has not been successfully bound to the foreign provider.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="6e6ea-154">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="6e6ea-154">Notes to callers</span></span>

<span data-ttu-id="6e6ea-155">**CreateEntry**が返されるときにする、新しいエントリのエントリ id をすぐにアクセスできない場合があります。</span><span class="sxs-lookup"><span data-stu-id="6e6ea-155">When **CreateEntry** returns, you may or may not be able to immediately access the entry identifier for the new entry.</span></span> <span data-ttu-id="6e6ea-156">アドレス帳のプロバイダーによって、それはないまで利用可能な新しいエントリの[IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドを呼び出した後。</span><span class="sxs-lookup"><span data-stu-id="6e6ea-156">Some address book providers do not make it available until after you have called the new entry's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
  
<span data-ttu-id="6e6ea-157">重複チェック フラグは、 **CreateEntry**にパラメーターとして渡されます、ただし、 **SaveChanges**が呼び出されるまで操作を確認した後、複製は発生しません。</span><span class="sxs-lookup"><span data-stu-id="6e6ea-157">Although duplicate checking flags are passed as parameters to **CreateEntry**, the duplicate checking operation does not occur until **SaveChanges** is called.</span></span> <span data-ttu-id="6e6ea-158">したがって、 **CreateEntry**ではなく、**たいていは SaveChanges**は、既に既存のエントリを作成しようとすることを示す、MAPI_E_COLLISION などの関連するエラーが返されます。</span><span class="sxs-lookup"><span data-stu-id="6e6ea-158">Therefore, related errors such as MAPI_E_COLLISION, which indicates that an attempt was made to create an already existing entry, are returned by **SaveChanges** rather than **CreateEntry**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6e6ea-159">関連項目</span><span class="sxs-lookup"><span data-stu-id="6e6ea-159">See also</span></span>



[<span data-ttu-id="6e6ea-160">IABContainer::CopyEntries</span><span class="sxs-lookup"><span data-stu-id="6e6ea-160">IABContainer::CopyEntries</span></span>](iabcontainer-copyentries.md)
  
[<span data-ttu-id="6e6ea-161">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="6e6ea-161">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="6e6ea-162">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="6e6ea-162">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="6e6ea-163">PidTagCreateTemplates 標準プロパティ Property</span><span class="sxs-lookup"><span data-stu-id="6e6ea-163">PidTagCreateTemplates Canonical Property</span></span>](pidtagcreatetemplates-canonical-property.md)
  
[<span data-ttu-id="6e6ea-164">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="6e6ea-164">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)

