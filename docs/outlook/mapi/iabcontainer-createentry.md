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
# <a name="iabcontainercreateentry"></a><span data-ttu-id="f26c3-103">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="f26c3-103">IABContainer::CreateEntry</span></span>

  
  
<span data-ttu-id="f26c3-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f26c3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f26c3-105">メッセージング ユーザー、配布リスト、または別のコンテナーを指定できる新しいエントリを作成します。</span><span class="sxs-lookup"><span data-stu-id="f26c3-105">Creates a new entry, which can be a messaging user, a distribution list, or another container.</span></span>
  
```cpp
HRESULT CreateEntry(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulCreateFlags,
  LPMAPIPROP FAR * lppMAPIPropEntry
);
```

## <a name="parameters"></a><span data-ttu-id="f26c3-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f26c3-106">Parameters</span></span>

 <span data-ttu-id="f26c3-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="f26c3-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="f26c3-108">[in]  _lpEntryID_ パラメーターが指すエントリ識別子内のバイト数。</span><span class="sxs-lookup"><span data-stu-id="f26c3-108">[in] The count of the bytes in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="f26c3-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="f26c3-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="f26c3-110">[in]特定の種類の新しいエントリを作成するためのテンプレートのエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="f26c3-110">[in] A pointer to the entry identifier of a template for creating new entries of a particular type.</span></span> 
    
 <span data-ttu-id="f26c3-111">_ulCreateFlags_</span><span class="sxs-lookup"><span data-stu-id="f26c3-111">_ulCreateFlags_</span></span>
  
> <span data-ttu-id="f26c3-112">[in]エントリの作成方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="f26c3-112">[in] A bitmask of flags that controls how entry creation is performed.</span></span> <span data-ttu-id="f26c3-113">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="f26c3-113">The following flags can be set:</span></span>
    
<span data-ttu-id="f26c3-114">CREATE_CHECK_DUP_LOOSE</span><span class="sxs-lookup"><span data-stu-id="f26c3-114">CREATE_CHECK_DUP_LOOSE</span></span> 
  
> <span data-ttu-id="f26c3-115">重複するエントリチェックの緩いレベルを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f26c3-115">A loose level of duplicate entry checking should be performed.</span></span> <span data-ttu-id="f26c3-116">緩やかな重複エントリチェックの実装は、プロバイダー固有です。</span><span class="sxs-lookup"><span data-stu-id="f26c3-116">The implementation of loose duplicate entry checking is provider specific.</span></span> <span data-ttu-id="f26c3-117">たとえば、プロバイダーは、同じ表示名を持つ任意の 2 つのエントリとして緩やかな一致を定義できます。</span><span class="sxs-lookup"><span data-stu-id="f26c3-117">For example, a provider can define a loose match as any two entries that have the same display name.</span></span>
    
<span data-ttu-id="f26c3-118">CREATE_CHECK_DUP_STRICT</span><span class="sxs-lookup"><span data-stu-id="f26c3-118">CREATE_CHECK_DUP_STRICT</span></span> 
  
> <span data-ttu-id="f26c3-119">厳密なレベルの重複エントリチェックを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f26c3-119">A strict level of duplicate entry checking should be performed.</span></span> <span data-ttu-id="f26c3-120">厳密な重複エントリチェックの実装は、プロバイダー固有です。</span><span class="sxs-lookup"><span data-stu-id="f26c3-120">The implementation of strict duplicate entry checking is provider specific.</span></span> <span data-ttu-id="f26c3-121">たとえば、プロバイダーは、同じ表示名とメッセージング アドレスの両方を持つ任意の 2 つのエントリとして厳密な一致を定義できます。</span><span class="sxs-lookup"><span data-stu-id="f26c3-121">For example, a provider can define a strict match as any two entries that have both the same display name and messaging address.</span></span>
    
<span data-ttu-id="f26c3-122">CREATE_REPLACE</span><span class="sxs-lookup"><span data-stu-id="f26c3-122">CREATE_REPLACE</span></span> 
  
> <span data-ttu-id="f26c3-123">2 つのエントリが重複すると判断された場合は、新しいエントリで既存のエントリが置き換わる必要があります。</span><span class="sxs-lookup"><span data-stu-id="f26c3-123">A new entry should replace an existing one if it is determined that the two are duplicates.</span></span>
    
 <span data-ttu-id="f26c3-124">_lppMAPIPropEntry_</span><span class="sxs-lookup"><span data-stu-id="f26c3-124">_lppMAPIPropEntry_</span></span>
  
> <span data-ttu-id="f26c3-125">[out]新しく作成されたエントリへのポインターを指すポインター。</span><span class="sxs-lookup"><span data-stu-id="f26c3-125">[out] A pointer to a pointer to the newly created entry.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f26c3-126">戻り値</span><span class="sxs-lookup"><span data-stu-id="f26c3-126">Return value</span></span>

<span data-ttu-id="f26c3-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="f26c3-127">S_OK</span></span> 
  
> <span data-ttu-id="f26c3-128">新しいエントリが正常に作成されました。</span><span class="sxs-lookup"><span data-stu-id="f26c3-128">The new entry was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f26c3-129">注釈</span><span class="sxs-lookup"><span data-stu-id="f26c3-129">Remarks</span></span>

<span data-ttu-id="f26c3-130">**IABContainer::CreateEntry** メソッドは、指定したコンテナー内の特定の型の新しいエントリを作成し、そのエントリにさらにアクセスするためにインターフェイス実装へのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="f26c3-130">The **IABContainer::CreateEntry** method creates a new entry of a particular type in the specified container, returning a pointer to an interface implementation for further access to the entry.</span></span> <span data-ttu-id="f26c3-131">新しいエントリは、コンテナーの一時テーブルに公開されている使用可能なテンプレートの一覧から選択されたテンプレートを使用して作成されます。</span><span class="sxs-lookup"><span data-stu-id="f26c3-131">The new entry is created by using a template that has been selected from the container's list of available templates published in its one-off table.</span></span> <span data-ttu-id="f26c3-132">呼び出し元は [、IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出し、PR_CREATE_TEMPLATES ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) プロパティを要求することで、コンテナーの **1** 回のテーブルにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="f26c3-132">Callers access a container's one-off table by calling its [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method and requesting the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="f26c3-133">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="f26c3-133">Notes to implementers</span></span>

<span data-ttu-id="f26c3-134">**IABContainer::CreateEntry** メソッドをサポートするコンテナーはすべて、変更可能である必要があります。</span><span class="sxs-lookup"><span data-stu-id="f26c3-134">All containers that support the **IABContainer::CreateEntry** method must be modifiable.</span></span> <span data-ttu-id="f26c3-135">コンテナーの AB_MODIFIABLE **フラグを** PR_CONTAINER_FLAGS ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) プロパティに設定して、変更可能であることを示します。</span><span class="sxs-lookup"><span data-stu-id="f26c3-135">Set your container's AB_MODIFIABLE flag in its **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) property to indicate that it is modifiable.</span></span> 
  
<span data-ttu-id="f26c3-136">すべての  _ulCreateFlags フラグをサポートする必要_ があります。</span><span class="sxs-lookup"><span data-stu-id="f26c3-136">You should support all of the  _ulCreateFlags_ flags.</span></span> <span data-ttu-id="f26c3-137">ただし、これらのフラグの解釈と使用は実装固有です。つまり、CREATE_CHECK_DUP_LOOSE と CREATE_CHECK_DUP_STRICT のセマンティクスが実装のコンテキストで何を意味するのかを判断できます。</span><span class="sxs-lookup"><span data-stu-id="f26c3-137">However, the interpretation and use of these flags is implementation specific—that is, you can determine what the semantics of CREATE_CHECK_DUP_LOOSE and CREATE_CHECK_DUP_STRICT mean in the context of your implementation.</span></span> <span data-ttu-id="f26c3-138">エントリが重複するかどうかを判断できない場合、または決定しない場合は、常にエントリの作成を許可します。</span><span class="sxs-lookup"><span data-stu-id="f26c3-138">If you cannot or do not determine whether an entry is a duplicate, always allow the entry to be created.</span></span> 
  
<span data-ttu-id="f26c3-139">一部のプロバイダーでは、エントリの表示名、メッセージング アドレス、および検索キーを照合して厳密なエントリ チェックを実装します。他のプロバイダーは、一致を表示名とアドレスに制限します。</span><span class="sxs-lookup"><span data-stu-id="f26c3-139">Some providers implement strict entry checking by matching the display name, messaging address, and search key in an entry; other providers limit the match to display name and address.</span></span> <span data-ttu-id="f26c3-140">ルーズ なエントリ チェックは、多くの場合、表示名のみをチェックすることで実装されます。</span><span class="sxs-lookup"><span data-stu-id="f26c3-140">Loose entry checking is often implemented by checking the display name only.</span></span> 
  
## <a name="notes-to-host-address-book-provider-implementers"></a><span data-ttu-id="f26c3-141">ホスト アドレス帳プロバイダーの実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="f26c3-141">Notes to Host Address Book Provider Implementers</span></span>

<span data-ttu-id="f26c3-142">コンテナーが他のプロバイダーのテンプレートからエントリを作成できる場合は **、CreateEntry** の実装によって、作成されたエントリに関連付けられたプロパティの一部またはすべてが格納されます。</span><span class="sxs-lookup"><span data-stu-id="f26c3-142">If your container can create entries from the templates of other providers, your implementation of **CreateEntry** should provide storage for some or all of the properties associated with the created entries.</span></span> <span data-ttu-id="f26c3-143">たとえば、エントリの **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) プロパティにストレージを提供する場合、外部プロバイダーに依存することなく詳細ダイアログ ボックスを生成できます。</span><span class="sxs-lookup"><span data-stu-id="f26c3-143">For example, if you provide storage for an entry's **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property, you can generate its details dialog box without having to depend on the foreign provider.</span></span> 
  
<span data-ttu-id="f26c3-144">コンテナーが PR_TEMPLATEID **(** [PidTagTemplateid](pidtagtemplateid-canonical-property.md)) プロパティをサポートするエントリを作成できる場合は **、CreateEntry** の実装で次の操作を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f26c3-144">If your container can create entries that support the **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property, your implementation of **CreateEntry** must do the following:</span></span> 
  
1. <span data-ttu-id="f26c3-145">[IMAPISupport::OpenTemplateID メソッドを呼び出](imapisupport-opentemplateid.md)します。</span><span class="sxs-lookup"><span data-stu-id="f26c3-145">Call the [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) method.</span></span> <span data-ttu-id="f26c3-146">**OpenTemplateID を使用** すると、エントリの外部プロバイダーのコードを作成する新しいエントリにバインドできます。</span><span class="sxs-lookup"><span data-stu-id="f26c3-146">**OpenTemplateID** enables the foreign provider's code for the entry to bind to the new entry being created.</span></span> <span data-ttu-id="f26c3-147">外部プロバイダーは、このバインド プロセスをサポートして、テンプレートからホスト アドレス帳プロバイダーのコンテナーに作成されたエントリを制御します。</span><span class="sxs-lookup"><span data-stu-id="f26c3-147">Foreign providers support this binding process to maintain control over entries created from their templates into the containers of host address book providers.</span></span> 
    
2. <span data-ttu-id="f26c3-148">必要な初期化を実行し **、OpenTemplateID** の _lppMAPIPropNew_ パラメーターでオブジェクトが返した外部プロバイダーのエントリのすべてのプロパティを新しいオブジェクトに設定します。</span><span class="sxs-lookup"><span data-stu-id="f26c3-148">Perform any necessary initialization, and populate the new object with all of the properties from the entry in the foreign provider that the object returned in the  _lppMAPIPropNew_ parameter from **OpenTemplateID**.</span></span>
    
<span data-ttu-id="f26c3-149">**OpenTemplateID** が成功した場合は _、lpMAPIPropData_ パラメーターが指す実装ではなく _、lppMAPIPropNew_ パラメーターが指す実装にプロパティをコピーします。</span><span class="sxs-lookup"><span data-stu-id="f26c3-149">If **OpenTemplateID** succeeds, copy the properties to the implementation pointed to by the  _lppMAPIPropNew_ parameter rather than directly to the implementation pointed to by the  _lpMAPIPropData_ parameter.</span></span> <span data-ttu-id="f26c3-150">外部プロバイダーの他のエントリと同様に、オフラインで使用する新しいエントリを初期化します。</span><span class="sxs-lookup"><span data-stu-id="f26c3-150">Initialize the new entry for offline use as you would any other entry from a foreign provider.</span></span> 
  
<span data-ttu-id="f26c3-151">**OpenTemplateID がエラー** を返す場合 **、CreateEntry は** 失敗します。</span><span class="sxs-lookup"><span data-stu-id="f26c3-151">If **OpenTemplateID** returns an error, **CreateEntry** should fail.</span></span> <span data-ttu-id="f26c3-152">エントリの作成を許可しない。</span><span class="sxs-lookup"><span data-stu-id="f26c3-152">Do not allow the entry to be created.</span></span> <span data-ttu-id="f26c3-153">外部プロバイダーは、プロバイダー内のデータを前提とすることができますので、外部プロバイダーに正常にバインドされていないテンプレート識別子を持つエントリを作成しない。</span><span class="sxs-lookup"><span data-stu-id="f26c3-153">Because the foreign provider can make assumptions about the data in your provider, do not create an entry with a template identifier that has not been successfully bound to the foreign provider.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f26c3-154">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="f26c3-154">Notes to callers</span></span>

<span data-ttu-id="f26c3-155">**CreateEntry が** 返された場合、新しいエントリのエントリ識別子にすぐにアクセスできる場合とアクセスできない場合があります。</span><span class="sxs-lookup"><span data-stu-id="f26c3-155">When **CreateEntry** returns, you may or may not be able to immediately access the entry identifier for the new entry.</span></span> <span data-ttu-id="f26c3-156">一部のアドレス帳プロバイダーでは、新しいエントリの [IMAPIProp::SaveChanges](imapiprop-savechanges.md) メソッドを呼び出すまで使用できません。</span><span class="sxs-lookup"><span data-stu-id="f26c3-156">Some address book providers do not make it available until after you have called the new entry's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
  
<span data-ttu-id="f26c3-157">重複チェック フラグはパラメーターとして **CreateEntry** に渡されますが **、SaveChanges** が呼び出されるまで、重複チェック操作は実行されません。</span><span class="sxs-lookup"><span data-stu-id="f26c3-157">Although duplicate checking flags are passed as parameters to **CreateEntry**, the duplicate checking operation does not occur until **SaveChanges** is called.</span></span> <span data-ttu-id="f26c3-158">したがって、MAPI_E_COLLISION などの関連するエラーは、既に既存のエントリを作成しようとした場合 **、CreateEntry** ではなく **SaveChanges** によって返されます。</span><span class="sxs-lookup"><span data-stu-id="f26c3-158">Therefore, related errors such as MAPI_E_COLLISION, which indicates that an attempt was made to create an already existing entry, are returned by **SaveChanges** rather than **CreateEntry**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f26c3-159">関連項目</span><span class="sxs-lookup"><span data-stu-id="f26c3-159">See also</span></span>



[<span data-ttu-id="f26c3-160">IABContainer::CopyEntries</span><span class="sxs-lookup"><span data-stu-id="f26c3-160">IABContainer::CopyEntries</span></span>](iabcontainer-copyentries.md)
  
[<span data-ttu-id="f26c3-161">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="f26c3-161">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="f26c3-162">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="f26c3-162">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="f26c3-163">PidTagCreateTemplates 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f26c3-163">PidTagCreateTemplates Canonical Property</span></span>](pidtagcreatetemplates-canonical-property.md)
  
[<span data-ttu-id="f26c3-164">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="f26c3-164">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)

