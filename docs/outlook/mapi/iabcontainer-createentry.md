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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 9f80130279e3437dd9be947de97d3f0d4181165e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411275"
---
# <a name="iabcontainercreateentry"></a><span data-ttu-id="3e8f6-103">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="3e8f6-103">IABContainer::CreateEntry</span></span>

  
  
<span data-ttu-id="3e8f6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3e8f6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3e8f6-105">新しいエントリを作成します。これは、メッセージングユーザー、配布リスト、または別のコンテナーにすることができます。</span><span class="sxs-lookup"><span data-stu-id="3e8f6-105">Creates a new entry, which can be a messaging user, a distribution list, or another container.</span></span>
  
```cpp
HRESULT CreateEntry(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulCreateFlags,
  LPMAPIPROP FAR * lppMAPIPropEntry
);
```

## <a name="parameters"></a><span data-ttu-id="3e8f6-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="3e8f6-106">Parameters</span></span>

 <span data-ttu-id="3e8f6-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="3e8f6-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="3e8f6-108">順番_lな tryid_パラメーターで指定されたエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="3e8f6-108">[in] The count of the bytes in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="3e8f6-109">_lて tryid_</span><span class="sxs-lookup"><span data-stu-id="3e8f6-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="3e8f6-110">順番特定の種類の新しいエントリを作成するためのテンプレートのエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="3e8f6-110">[in] A pointer to the entry identifier of a template for creating new entries of a particular type.</span></span> 
    
 <span data-ttu-id="3e8f6-111">_ulcreateflags_</span><span class="sxs-lookup"><span data-stu-id="3e8f6-111">_ulCreateFlags_</span></span>
  
> <span data-ttu-id="3e8f6-112">順番エントリの作成を実行する方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="3e8f6-112">[in] A bitmask of flags that controls how entry creation is performed.</span></span> <span data-ttu-id="3e8f6-113">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="3e8f6-113">The following flags can be set:</span></span>
    
<span data-ttu-id="3e8f6-114">CREATE_CHECK_DUP_LOOSE</span><span class="sxs-lookup"><span data-stu-id="3e8f6-114">CREATE_CHECK_DUP_LOOSE</span></span> 
  
> <span data-ttu-id="3e8f6-115">重複したエントリのチェックは、緩やかなレベルで実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3e8f6-115">A loose level of duplicate entry checking should be performed.</span></span> <span data-ttu-id="3e8f6-116">重複していない重複するエントリのチェックは、プロバイダーに固有のものです。</span><span class="sxs-lookup"><span data-stu-id="3e8f6-116">The implementation of loose duplicate entry checking is provider specific.</span></span> <span data-ttu-id="3e8f6-117">たとえば、プロバイダーは、同じ表示名を持つ2つのエントリとして緩やかな一致を定義できます。</span><span class="sxs-lookup"><span data-stu-id="3e8f6-117">For example, a provider can define a loose match as any two entries that have the same display name.</span></span>
    
<span data-ttu-id="3e8f6-118">CREATE_CHECK_DUP_STRICT</span><span class="sxs-lookup"><span data-stu-id="3e8f6-118">CREATE_CHECK_DUP_STRICT</span></span> 
  
> <span data-ttu-id="3e8f6-119">重複するエントリの厳密なレベルのチェックを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3e8f6-119">A strict level of duplicate entry checking should be performed.</span></span> <span data-ttu-id="3e8f6-120">厳密に重複したエントリチェックの実装は、プロバイダーに固有のものです。</span><span class="sxs-lookup"><span data-stu-id="3e8f6-120">The implementation of strict duplicate entry checking is provider specific.</span></span> <span data-ttu-id="3e8f6-121">たとえば、プロバイダーは、同じ表示名とメッセージアドレスの両方を持つ2つのエントリとして厳密な一致を定義できます。</span><span class="sxs-lookup"><span data-stu-id="3e8f6-121">For example, a provider can define a strict match as any two entries that have both the same display name and messaging address.</span></span>
    
<span data-ttu-id="3e8f6-122">CREATE_REPLACE</span><span class="sxs-lookup"><span data-stu-id="3e8f6-122">CREATE_REPLACE</span></span> 
  
> <span data-ttu-id="3e8f6-123">2つが重複していると判断された場合は、新しいエントリで既存のエントリを置き換える必要があります。</span><span class="sxs-lookup"><span data-stu-id="3e8f6-123">A new entry should replace an existing one if it is determined that the two are duplicates.</span></span>
    
 <span data-ttu-id="3e8f6-124">_lppMAPIPropEntry_</span><span class="sxs-lookup"><span data-stu-id="3e8f6-124">_lppMAPIPropEntry_</span></span>
  
> <span data-ttu-id="3e8f6-125">読み上げ新しく作成されたエントリへのポインターへのポインターを示します。</span><span class="sxs-lookup"><span data-stu-id="3e8f6-125">[out] A pointer to a pointer to the newly created entry.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3e8f6-126">戻り値</span><span class="sxs-lookup"><span data-stu-id="3e8f6-126">Return value</span></span>

<span data-ttu-id="3e8f6-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="3e8f6-127">S_OK</span></span> 
  
> <span data-ttu-id="3e8f6-128">新しいエントリが正常に作成されました。</span><span class="sxs-lookup"><span data-stu-id="3e8f6-128">The new entry was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3e8f6-129">注釈</span><span class="sxs-lookup"><span data-stu-id="3e8f6-129">Remarks</span></span>

<span data-ttu-id="3e8f6-130">**IABContainer:: createentry**メソッドは、指定されたコンテナーに特定の型の新しいエントリを作成し、そのエントリにさらにアクセスするためのインターフェイス実装へのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="3e8f6-130">The **IABContainer::CreateEntry** method creates a new entry of a particular type in the specified container, returning a pointer to an interface implementation for further access to the entry.</span></span> <span data-ttu-id="3e8f6-131">新しいエントリは、1回限りのテーブルで公開されている使用可能なテンプレートの一覧から選択されたテンプレートを使用して作成されます。</span><span class="sxs-lookup"><span data-stu-id="3e8f6-131">The new entry is created by using a template that has been selected from the container's list of available templates published in its one-off table.</span></span> <span data-ttu-id="3e8f6-132">発信者は、 [imapiprop:: openproperty](imapiprop-openproperty.md)メソッドを呼び出して、 **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) プロパティを要求することによって、コンテナーの1回限りのテーブルにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="3e8f6-132">Callers access a container's one-off table by calling its [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method and requesting the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="3e8f6-133">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="3e8f6-133">Notes to implementers</span></span>

<span data-ttu-id="3e8f6-134">**IABContainer:: createentry**メソッドをサポートするすべてのコンテナーを変更可能にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="3e8f6-134">All containers that support the **IABContainer::CreateEntry** method must be modifiable.</span></span> <span data-ttu-id="3e8f6-135">コンテナーの AB_MODIFIABLE フラグを**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) プロパティに設定して、それが変更可能であることを示します。</span><span class="sxs-lookup"><span data-stu-id="3e8f6-135">Set your container's AB_MODIFIABLE flag in its **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) property to indicate that it is modifiable.</span></span> 
  
<span data-ttu-id="3e8f6-136">_ulcreateflags_フラグはすべてサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="3e8f6-136">You should support all of the  _ulCreateFlags_ flags.</span></span> <span data-ttu-id="3e8f6-137">ただし、これらのフラグの解釈と使用は実装に固有です。つまり、実装のコンテキストにおける CREATE_CHECK_DUP_LOOSE と CREATE_CHECK_DUP_STRICT の意味を判断できます。</span><span class="sxs-lookup"><span data-stu-id="3e8f6-137">However, the interpretation and use of these flags is implementation specific—that is, you can determine what the semantics of CREATE_CHECK_DUP_LOOSE and CREATE_CHECK_DUP_STRICT mean in the context of your implementation.</span></span> <span data-ttu-id="3e8f6-138">エントリが重複しているかどうかを判断できない場合、または指定しない場合は、常にエントリの作成を許可します。</span><span class="sxs-lookup"><span data-stu-id="3e8f6-138">If you cannot or do not determine whether an entry is a duplicate, always allow the entry to be created.</span></span> 
  
<span data-ttu-id="3e8f6-139">プロバイダーによっては、エントリの表示名、メッセージアドレス、および検索キーを一致させることによって、厳密なエントリチェックを実装しています。その他のプロバイダーは、表示名とアドレスに一致するものを制限します。</span><span class="sxs-lookup"><span data-stu-id="3e8f6-139">Some providers implement strict entry checking by matching the display name, messaging address, and search key in an entry; other providers limit the match to display name and address.</span></span> <span data-ttu-id="3e8f6-140">厳密なエントリチェックは、表示名のみをチェックすることによって実装されることがよくあります。</span><span class="sxs-lookup"><span data-stu-id="3e8f6-140">Loose entry checking is often implemented by checking the display name only.</span></span> 
  
## <a name="notes-to-host-address-book-provider-implementers"></a><span data-ttu-id="3e8f6-141">アドレス帳プロバイダー実装者をホストするためのメモ</span><span class="sxs-lookup"><span data-stu-id="3e8f6-141">Notes to Host Address Book Provider Implementers</span></span>

<span data-ttu-id="3e8f6-142">コンテナーが他のプロバイダーのテンプレートからエントリを作成できる場合は、 **createentry**の実装によって、作成されたエントリに関連付けられているプロパティの一部またはすべてに対してストレージを提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3e8f6-142">If your container can create entries from the templates of other providers, your implementation of **CreateEntry** should provide storage for some or all of the properties associated with the created entries.</span></span> <span data-ttu-id="3e8f6-143">たとえば、エントリの**PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) プロパティのストレージを提供している場合は、外部プロバイダーに依存せずに [詳細] ダイアログボックスを生成することができます。</span><span class="sxs-lookup"><span data-stu-id="3e8f6-143">For example, if you provide storage for an entry's **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property, you can generate its details dialog box without having to depend on the foreign provider.</span></span> 
  
<span data-ttu-id="3e8f6-144">コンテナーが**PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) プロパティをサポートするエントリを作成できる場合、 **createentry**の実装は次のことを行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="3e8f6-144">If your container can create entries that support the **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property, your implementation of **CreateEntry** must do the following:</span></span> 
  
1. <span data-ttu-id="3e8f6-145">[imapisupport:: OpenTemplateID](imapisupport-opentemplateid.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="3e8f6-145">Call the [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) method.</span></span> <span data-ttu-id="3e8f6-146">**OpenTemplateID**では、エントリの外部プロバイダーのコードを使用して、作成される新しいエントリにバインドできます。</span><span class="sxs-lookup"><span data-stu-id="3e8f6-146">**OpenTemplateID** enables the foreign provider's code for the entry to bind to the new entry being created.</span></span> <span data-ttu-id="3e8f6-147">外部プロバイダーは、このバインドプロセスをサポートして、テンプレートから作成されたエントリに対する制御をホストアドレス帳プロバイダーのコンテナーに保持します。</span><span class="sxs-lookup"><span data-stu-id="3e8f6-147">Foreign providers support this binding process to maintain control over entries created from their templates into the containers of host address book providers.</span></span> 
    
2. <span data-ttu-id="3e8f6-148">必要な初期化を実行し、外部プロバイダーのエントリから、 **OpenTemplateID**から_lppMAPIPropNew_パラメーターで返されるオブジェクトが返されるすべてのプロパティを新しいオブジェクトに設定します。</span><span class="sxs-lookup"><span data-stu-id="3e8f6-148">Perform any necessary initialization, and populate the new object with all of the properties from the entry in the foreign provider that the object returned in the  _lppMAPIPropNew_ parameter from **OpenTemplateID**.</span></span>
    
<span data-ttu-id="3e8f6-149">**OpenTemplateID**が正常に終了した場合は、 _lpMAPIPropData_パラメーターで示される実装に直接ではなく、 _lppMAPIPropNew_パラメーターによって示される実装にプロパティをコピーします。</span><span class="sxs-lookup"><span data-stu-id="3e8f6-149">If **OpenTemplateID** succeeds, copy the properties to the implementation pointed to by the  _lppMAPIPropNew_ parameter rather than directly to the implementation pointed to by the  _lpMAPIPropData_ parameter.</span></span> <span data-ttu-id="3e8f6-150">外部プロバイダーからの他のエントリと同様に、オフラインで使用するために新しいエントリを初期化します。</span><span class="sxs-lookup"><span data-stu-id="3e8f6-150">Initialize the new entry for offline use as you would any other entry from a foreign provider.</span></span> 
  
<span data-ttu-id="3e8f6-151">**OpenTemplateID**がエラーを返す場合、 **createentry**は失敗します。</span><span class="sxs-lookup"><span data-stu-id="3e8f6-151">If **OpenTemplateID** returns an error, **CreateEntry** should fail.</span></span> <span data-ttu-id="3e8f6-152">エントリの作成を許可しません。</span><span class="sxs-lookup"><span data-stu-id="3e8f6-152">Do not allow the entry to be created.</span></span> <span data-ttu-id="3e8f6-153">外部プロバイダーはプロバイダーのデータについて想定することができるので、外部プロバイダーに正常にバインドされていないテンプレート識別子を使用してエントリを作成しないでください。</span><span class="sxs-lookup"><span data-stu-id="3e8f6-153">Because the foreign provider can make assumptions about the data in your provider, do not create an entry with a template identifier that has not been successfully bound to the foreign provider.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="3e8f6-154">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="3e8f6-154">Notes to callers</span></span>

<span data-ttu-id="3e8f6-155">**createentry**から戻ると、新しいエントリのエントリ識別子にすぐにアクセスすることができます。</span><span class="sxs-lookup"><span data-stu-id="3e8f6-155">When **CreateEntry** returns, you may or may not be able to immediately access the entry identifier for the new entry.</span></span> <span data-ttu-id="3e8f6-156">アドレス帳プロバイダーによっては、新しいエントリの[imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドを呼び出した後に使用できなくなります。</span><span class="sxs-lookup"><span data-stu-id="3e8f6-156">Some address book providers do not make it available until after you have called the new entry's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
  
<span data-ttu-id="3e8f6-157">重複チェックフラグはパラメーターとして**createentry**に渡されますが、 **SaveChanges**が呼び出されるまで重複したチェック操作は発生しません。</span><span class="sxs-lookup"><span data-stu-id="3e8f6-157">Although duplicate checking flags are passed as parameters to **CreateEntry**, the duplicate checking operation does not occur until **SaveChanges** is called.</span></span> <span data-ttu-id="3e8f6-158">そのため、MAPI_E_COLLISION などの関連エラーは、既に存在するエントリを作成しようとしたことを示しています。これは、 **createentry**ではなく**SaveChanges**によって返されます。</span><span class="sxs-lookup"><span data-stu-id="3e8f6-158">Therefore, related errors such as MAPI_E_COLLISION, which indicates that an attempt was made to create an already existing entry, are returned by **SaveChanges** rather than **CreateEntry**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3e8f6-159">関連項目</span><span class="sxs-lookup"><span data-stu-id="3e8f6-159">See also</span></span>



[<span data-ttu-id="3e8f6-160">IABContainer::CopyEntries</span><span class="sxs-lookup"><span data-stu-id="3e8f6-160">IABContainer::CopyEntries</span></span>](iabcontainer-copyentries.md)
  
[<span data-ttu-id="3e8f6-161">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="3e8f6-161">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="3e8f6-162">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="3e8f6-162">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="3e8f6-163">PidTagCreateTemplates 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="3e8f6-163">PidTagCreateTemplates Canonical Property</span></span>](pidtagcreatetemplates-canonical-property.md)
  
[<span data-ttu-id="3e8f6-164">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="3e8f6-164">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)

