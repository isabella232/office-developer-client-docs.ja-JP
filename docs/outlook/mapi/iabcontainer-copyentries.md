---
title: IABContainerCopyEntries
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABContainer.CopyEntries
api_type:
- COM
ms.assetid: 4e775228-5ceb-4002-9b68-999fb5889b86
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 36e0db77097178d2db7a11b1339d19ebb8c91f2c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565327"
---
# <a name="iabcontainercopyentries"></a><span data-ttu-id="c4a3c-103">IABContainer::CopyEntries</span><span class="sxs-lookup"><span data-stu-id="c4a3c-103">IABContainer::CopyEntries</span></span>

  
  
<span data-ttu-id="c4a3c-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c4a3c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c4a3c-105">1 つまたは複数のエントリ、メッセージを通常のユーザーまたは配布リストにコピーします。</span><span class="sxs-lookup"><span data-stu-id="c4a3c-105">Copies one or more entries, typically messaging users or distribution lists.</span></span>
  
```cpp
HRESULT CopyEntries(
  LPENTRYLIST lpEntries,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="c4a3c-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c4a3c-106">Parameters</span></span>

 <span data-ttu-id="c4a3c-107">_lpEntries_</span><span class="sxs-lookup"><span data-stu-id="c4a3c-107">_lpEntries_</span></span>
  
> <span data-ttu-id="c4a3c-108">[in]コピーするエントリのエントリ id が含まれている[ENTRYLIST](entrylist.md)構造体の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="c4a3c-108">[in] A pointer to an array of [ENTRYLIST](entrylist.md) structures that contains the entry identifiers of the entries to copy.</span></span> 
    
 <span data-ttu-id="c4a3c-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="c4a3c-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="c4a3c-110">[in]すべてのダイアログ ボックスの親ウィンドウまたはこのメソッドを表示するウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="c4a3c-110">[in] The handle to the parent window of any dialog boxes or windows that this method displays.</span></span> <span data-ttu-id="c4a3c-111">_UlFlags_パラメーターに AB_NO_DIALOG フラグが設定されている場合、 _ulUIParam_パラメーターは 0 にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c4a3c-111">The  _ulUIParam_ parameter must be zero if the AB_NO_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="c4a3c-112">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="c4a3c-112">_lpProgress_</span></span>
  
> <span data-ttu-id="c4a3c-113">[in]進行状況インジケーターの場合、または NULL を表示する進行中のオブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="c4a3c-113">[in] A pointer to a progress object that displays a progress indicator, or NULL.</span></span> <span data-ttu-id="c4a3c-114">_LpProgress_が NULL の場合は、 [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md)メソッドを介して、MAPI によって提供される進行中のオブジェクトを使用して進行状況のインジケーターを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c4a3c-114">If  _lpProgress_ is NULL, a progress indicator should be displayed by using the progress object supplied by MAPI through the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method.</span></span> <span data-ttu-id="c4a3c-115">_UlFlags_に AB_NO_DIALOG フラグが設定されている場合、 _lpProgress_パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="c4a3c-115">The  _lpProgress_ parameter is ignored if the AB_NO_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="c4a3c-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c4a3c-116">_ulFlags_</span></span>
  
> <span data-ttu-id="c4a3c-117">[in]コピー操作の実行方法を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="c4a3c-117">[in] A bitmask of flags that controls how the copy operation is performed.</span></span> <span data-ttu-id="c4a3c-118">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="c4a3c-118">The following flags can be set:</span></span>
    
<span data-ttu-id="c4a3c-119">AB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="c4a3c-119">AB_NO_DIALOG</span></span> 
  
> <span data-ttu-id="c4a3c-120">進行状況インジケーターの表示を抑制します。</span><span class="sxs-lookup"><span data-stu-id="c4a3c-120">Suppresses display of a progress indicator.</span></span> <span data-ttu-id="c4a3c-121">このフラグが設定されていない場合は、進行状況のインジケーターが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c4a3c-121">If this flag is not set, a progress indicator is displayed.</span></span>
    
<span data-ttu-id="c4a3c-122">CREATE_CHECK_DUP_LOOSE</span><span class="sxs-lookup"><span data-stu-id="c4a3c-122">CREATE_CHECK_DUP_LOOSE</span></span> 
  
> <span data-ttu-id="c4a3c-123">緩やかなレベルの重複するエントリのチェックを実行することを示します。</span><span class="sxs-lookup"><span data-stu-id="c4a3c-123">Indicates that a loose level of duplicate entry checking should be performed.</span></span> <span data-ttu-id="c4a3c-124">緩やかな重複するエントリのチェックの実装は、特定のプロバイダーです。</span><span class="sxs-lookup"><span data-stu-id="c4a3c-124">The implementation of loose duplicate entry checking is provider specific.</span></span> <span data-ttu-id="c4a3c-125">などのプロバイダーは、同じ 2 つのエントリの表示名と緩やかな一致を定義できます。</span><span class="sxs-lookup"><span data-stu-id="c4a3c-125">For example, a provider can define a loose match as any two entries that have the same display name.</span></span>
    
<span data-ttu-id="c4a3c-126">CREATE_CHECK_DUP_STRICT</span><span class="sxs-lookup"><span data-stu-id="c4a3c-126">CREATE_CHECK_DUP_STRICT</span></span> 
  
> <span data-ttu-id="c4a3c-127">厳密なレベルの重複するエントリのチェックを実行することを示します。</span><span class="sxs-lookup"><span data-stu-id="c4a3c-127">Indicates that a strict level of duplicate entry checking should be performed.</span></span> <span data-ttu-id="c4a3c-128">厳密な重複するエントリのチェックの実装は、特定のプロバイダーです。</span><span class="sxs-lookup"><span data-stu-id="c4a3c-128">The implementation of strict duplicate entry checking is provider specific.</span></span> <span data-ttu-id="c4a3c-129">などのプロバイダーは、両方同じ 2 つのエントリの名前とメッセージのアドレスを表示すると、厳密な一致を定義できます。</span><span class="sxs-lookup"><span data-stu-id="c4a3c-129">For example, a provider can define a strict match as any two entries that have both the same display name and messaging address.</span></span>
    
<span data-ttu-id="c4a3c-130">CREATE_REPLACE</span><span class="sxs-lookup"><span data-stu-id="c4a3c-130">CREATE_REPLACE</span></span> 
  
> <span data-ttu-id="c4a3c-131">2 つ重複していることが判明した場合に新しいエントリが既存のものを置換する必要があることを示します。</span><span class="sxs-lookup"><span data-stu-id="c4a3c-131">Indicates that a new entry should replace an existing one if it is determined that the two are duplicates.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c4a3c-132">�߂�l</span><span class="sxs-lookup"><span data-stu-id="c4a3c-132">Return value</span></span>

<span data-ttu-id="c4a3c-133">S_OK</span><span class="sxs-lookup"><span data-stu-id="c4a3c-133">S_OK</span></span> 
  
> <span data-ttu-id="c4a3c-134">コピー操作が成功しました。</span><span class="sxs-lookup"><span data-stu-id="c4a3c-134">The copy operation succeeded.</span></span>
    
<span data-ttu-id="c4a3c-135">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="c4a3c-135">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="c4a3c-136">コピー操作は完了しましたが、1 つまたは複数のエントリをコピーできませんでした。</span><span class="sxs-lookup"><span data-stu-id="c4a3c-136">The copy operation succeeded overall, but one or more of the entries could not be copied.</span></span> <span data-ttu-id="c4a3c-137">この値が返されると、呼び出しを成功として処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c4a3c-137">When this value is returned, the call should be handled as successful.</span></span> <span data-ttu-id="c4a3c-138">この値をテストするには、 **HR_FAILED**マクロを使用します。</span><span class="sxs-lookup"><span data-stu-id="c4a3c-138">To test for this value, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="c4a3c-139">詳細については、[エラーを処理するためのマクロの使用](using-macros-for-error-handling.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c4a3c-139">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c4a3c-140">注釈</span><span class="sxs-lookup"><span data-stu-id="c4a3c-140">Remarks</span></span>

<span data-ttu-id="c4a3c-141">**IABContainer::CopyEntries**メソッドは、同じコンテナーまたは別のコンテナーからエントリをコピーします。</span><span class="sxs-lookup"><span data-stu-id="c4a3c-141">The **IABContainer::CopyEntries** method copies entries from the same container or a different container.</span></span> <span data-ttu-id="c4a3c-142">**CopyEntries**への呼び出しは、コピーするには、各エントリの次の呼び出しと同等の機能です。</span><span class="sxs-lookup"><span data-stu-id="c4a3c-142">A call to **CopyEntries** is functionally equivalent to making the following calls for each entry to be copied:</span></span> 
  
1. <span data-ttu-id="c4a3c-143">新しいエントリを作成する[IABContainer::CreateEntry](iabcontainer-createentry.md)メソッドです。</span><span class="sxs-lookup"><span data-stu-id="c4a3c-143">The [IABContainer::CreateEntry](iabcontainer-createentry.md) method to create the new entry.</span></span> 
    
2. <span data-ttu-id="c4a3c-144">コピーするエントリからプロパティを読み取る[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドです。</span><span class="sxs-lookup"><span data-stu-id="c4a3c-144">The [IMAPIProp::GetProps](imapiprop-getprops.md) method to read properties from the entry to be copied.</span></span> 
    
3. <span data-ttu-id="c4a3c-145">新しいエントリのプロパティを記述する[IMAPIProp::SetProps](imapiprop-setprops.md)メソッドです。</span><span class="sxs-lookup"><span data-stu-id="c4a3c-145">The [IMAPIProp::SetProps](imapiprop-setprops.md) method to write properties to the new entry.</span></span> 
    
4. <span data-ttu-id="c4a3c-146">[IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドを新しいエントリの保存を実行します。</span><span class="sxs-lookup"><span data-stu-id="c4a3c-146">The new entry's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to perform a save.</span></span> 
    
5. <span data-ttu-id="c4a3c-147">コンテナーの参照を解放するのには、新しいエントリの[リ ス](http://msdn.microsoft.com/en-us/library/ms682317%28VS.85%29.aspx)のメソッドです。</span><span class="sxs-lookup"><span data-stu-id="c4a3c-147">The new entry's [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28VS.85%29.aspx) method to release the container's reference.</span></span> 
    
## <a name="notes-to-implementers"></a><span data-ttu-id="c4a3c-148">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="c4a3c-148">Notes to implementers</span></span>

<span data-ttu-id="c4a3c-149">**IABContainer::CopyEntries**メソッドをサポートするすべてのコンテナーは、変更可能である必要があります。</span><span class="sxs-lookup"><span data-stu-id="c4a3c-149">All containers that support the **IABContainer::CopyEntries** method must be modifiable.</span></span> <span data-ttu-id="c4a3c-150">変更可能であることを示すには、その**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) プロパティで、コンテナーの AB_MODIFIABLE フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="c4a3c-150">Set your container's AB_MODIFIABLE flag in its **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) property to indicate that it is modifiable.</span></span> 
  
<span data-ttu-id="c4a3c-151">すべてのフラグの操作をサポートする必要があります。ただし、解釈し、これらのフラグの使用は、特定の実装-は、実装のコンテキストでは、CREATE_CHECK_DUP_LOOSE と CREATE_CHECK_DUP_STRICT のフラグの意味は何を意味を判断できます。</span><span class="sxs-lookup"><span data-stu-id="c4a3c-151">You must support all of the flags; however, the interpretation and use of these flags is implementation specific—that is, you can determine what the semantics of the CREATE_CHECK_DUP_LOOSE and CREATE_CHECK_DUP_STRICT flags mean in the context of your implementation.</span></span> <span data-ttu-id="c4a3c-152">できないかのエントリは、重複しているかどうかを決定できません、コピーするエントリを常に許可します。</span><span class="sxs-lookup"><span data-stu-id="c4a3c-152">If you cannot or do not determine whether an entry is a duplicate, always allow the entry to be copied.</span></span> 
  
<span data-ttu-id="c4a3c-153">CREATE_REPLACE フラグが設定されている場合は、常に CREATE_CHECK_DUP_LOOSE または CREATE_CHECK_DUP_STRICT を設定するかどうかと、エントリは、重複しているかどうかに関係なくエントリをコピーします。</span><span class="sxs-lookup"><span data-stu-id="c4a3c-153">If the CREATE_REPLACE flag is set, always copy the entry regardless of whether CREATE_CHECK_DUP_LOOSE or CREATE_CHECK_DUP_STRICT is set and whether the entry is a duplicate.</span></span> 
  
<span data-ttu-id="c4a3c-154">CREATE_REPLACE が設定されていない場合は、CREATE_CHECK_DUP_STRICT の設定は、重複データをチェックします。</span><span class="sxs-lookup"><span data-stu-id="c4a3c-154">If CREATE_REPLACE is not set and CREATE_CHECK_DUP_STRICT is set, check for duplicates.</span></span> <span data-ttu-id="c4a3c-155">重複エントリが確認された場合は、エントリをコピーできません。</span><span class="sxs-lookup"><span data-stu-id="c4a3c-155">If an entry is determined to be a duplicate, do not copy the entry.</span></span> 
  
<span data-ttu-id="c4a3c-156">CREATE_REPLACE; をサポートする必要はありません。CREATE_REPLACE をサポートしていないことは、無視しても安全とコピーが常に実行を意味します。</span><span class="sxs-lookup"><span data-stu-id="c4a3c-156">You do not need to support CREATE_REPLACE; not supporting CREATE_REPLACE means that you can safely ignore it and always perform a copy.</span></span> 
  
<span data-ttu-id="c4a3c-157">重複していないエントリをコピーできない場合にのみ、MAPI_W_PARTIAL_COMPLETION の警告を返します。</span><span class="sxs-lookup"><span data-stu-id="c4a3c-157">Return the warning MAPI_W_PARTIAL_COMPLETION only if a nonduplicate entry cannot be copied.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="c4a3c-158">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="c4a3c-158">Notes to callers</span></span>

<span data-ttu-id="c4a3c-159">プロバイダーに重複するエントリのチェックを実行するためにコンテナーをどのようにするかを示すために、CREATE_CHECK_DUP_LOOSE と CREATE_CHECK_DUP_STRICT フラグを使用します。</span><span class="sxs-lookup"><span data-stu-id="c4a3c-159">Use the CREATE_CHECK_DUP_LOOSE and CREATE_CHECK_DUP_STRICT flags to indicate to the provider how you want the container to perform duplicate-entry checking.</span></span> <span data-ttu-id="c4a3c-160">重複しているかどうかに関係なく追加のエントリがある場合は、いずれかまたは設定しませんこれらのフラグのいずれかの CREATE_REPLACE フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="c4a3c-160">If you need to have an entry added regardless of whether it is a duplicate, either do not set either of these flags or set the CREATE_REPLACE flag.</span></span> <span data-ttu-id="c4a3c-161">CREATE_REPLACE は、エントリが重複の場合を限定しないことを示します常にそれをする元のエントリを置き換えます。</span><span class="sxs-lookup"><span data-stu-id="c4a3c-161">CREATE_REPLACE indicates that you do not care if an entry is a duplicate; you always want it to replace the original entry.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c4a3c-162">関連項目</span><span class="sxs-lookup"><span data-stu-id="c4a3c-162">See also</span></span>



[<span data-ttu-id="c4a3c-163">ENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="c4a3c-163">ENTRYLIST</span></span>](entrylist.md)
  
[<span data-ttu-id="c4a3c-164">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="c4a3c-164">IABContainer::CreateEntry</span></span>](iabcontainer-createentry.md)
  
[<span data-ttu-id="c4a3c-165">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c4a3c-165">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)
  
[<span data-ttu-id="c4a3c-166">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="c4a3c-166">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="c4a3c-167">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="c4a3c-167">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)

