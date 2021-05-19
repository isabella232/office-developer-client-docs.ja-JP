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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: ddb730ed92db4c8d281e7c8d5d9b18bc44505598
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346397"
---
# <a name="iabcontainercopyentries"></a><span data-ttu-id="a10b7-103">IABContainer::CopyEntries</span><span class="sxs-lookup"><span data-stu-id="a10b7-103">IABContainer::CopyEntries</span></span>

  
  
<span data-ttu-id="a10b7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a10b7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a10b7-105">1 つ以上のエントリ (通常はメッセージング ユーザーまたは配布リスト) をコピーします。</span><span class="sxs-lookup"><span data-stu-id="a10b7-105">Copies one or more entries, typically messaging users or distribution lists.</span></span>
  
```cpp
HRESULT CopyEntries(
  LPENTRYLIST lpEntries,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="a10b7-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a10b7-106">Parameters</span></span>

 <span data-ttu-id="a10b7-107">_lpEntries_</span><span class="sxs-lookup"><span data-stu-id="a10b7-107">_lpEntries_</span></span>
  
> <span data-ttu-id="a10b7-108">[in]コピーするエントリのエントリ識別子を含む [ENTRYLIST](entrylist.md) 構造体の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a10b7-108">[in] A pointer to an array of [ENTRYLIST](entrylist.md) structures that contains the entry identifiers of the entries to copy.</span></span> 
    
 <span data-ttu-id="a10b7-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="a10b7-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="a10b7-110">[in]このメソッドが表示するダイアログ ボックスまたはウィンドウの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="a10b7-110">[in] The handle to the parent window of any dialog boxes or windows that this method displays.</span></span> <span data-ttu-id="a10b7-111">_ulUIParam_ パラメーターは、ulFlags パラメーターで AB_NO_DIALOGフラグが設定されている場合は _0 である必要_ があります。</span><span class="sxs-lookup"><span data-stu-id="a10b7-111">The  _ulUIParam_ parameter must be zero if the AB_NO_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="a10b7-112">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="a10b7-112">_lpProgress_</span></span>
  
> <span data-ttu-id="a10b7-113">[in]進行状況インジケーター (NULL) を表示する進行状況オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="a10b7-113">[in] A pointer to a progress object that displays a progress indicator, or NULL.</span></span> <span data-ttu-id="a10b7-114">_lpProgress が_ NULL の場合は [、IMAPISupport::D oProgressDialog](imapisupport-doprogressdialog.md)メソッドを介して MAPI によって提供される進行状況オブジェクトを使用して進行状況インジケーターを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a10b7-114">If  _lpProgress_ is NULL, a progress indicator should be displayed by using the progress object supplied by MAPI through the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method.</span></span> <span data-ttu-id="a10b7-115">_lpProgress パラメーター_ は _、ulFlags_ で AB_NO_DIALOGフラグが設定されている場合は無視されます。</span><span class="sxs-lookup"><span data-stu-id="a10b7-115">The  _lpProgress_ parameter is ignored if the AB_NO_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="a10b7-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a10b7-116">_ulFlags_</span></span>
  
> <span data-ttu-id="a10b7-117">[in]コピー操作の実行方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="a10b7-117">[in] A bitmask of flags that controls how the copy operation is performed.</span></span> <span data-ttu-id="a10b7-118">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="a10b7-118">The following flags can be set:</span></span>
    
<span data-ttu-id="a10b7-119">AB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="a10b7-119">AB_NO_DIALOG</span></span> 
  
> <span data-ttu-id="a10b7-120">進行状況インジケーターの表示を抑制します。</span><span class="sxs-lookup"><span data-stu-id="a10b7-120">Suppresses display of a progress indicator.</span></span> <span data-ttu-id="a10b7-121">このフラグが設定されていない場合は、進行状況インジケーターが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a10b7-121">If this flag is not set, a progress indicator is displayed.</span></span>
    
<span data-ttu-id="a10b7-122">CREATE_CHECK_DUP_LOOSE</span><span class="sxs-lookup"><span data-stu-id="a10b7-122">CREATE_CHECK_DUP_LOOSE</span></span> 
  
> <span data-ttu-id="a10b7-123">重複するエントリチェックの緩いレベルを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a10b7-123">Indicates that a loose level of duplicate entry checking should be performed.</span></span> <span data-ttu-id="a10b7-124">緩やかな重複エントリチェックの実装は、プロバイダー固有です。</span><span class="sxs-lookup"><span data-stu-id="a10b7-124">The implementation of loose duplicate entry checking is provider specific.</span></span> <span data-ttu-id="a10b7-125">たとえば、プロバイダーは、同じ表示名を持つ任意の 2 つのエントリとして緩やかな一致を定義できます。</span><span class="sxs-lookup"><span data-stu-id="a10b7-125">For example, a provider can define a loose match as any two entries that have the same display name.</span></span>
    
<span data-ttu-id="a10b7-126">CREATE_CHECK_DUP_STRICT</span><span class="sxs-lookup"><span data-stu-id="a10b7-126">CREATE_CHECK_DUP_STRICT</span></span> 
  
> <span data-ttu-id="a10b7-127">厳密なレベルの重複エントリチェックを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a10b7-127">Indicates that a strict level of duplicate entry checking should be performed.</span></span> <span data-ttu-id="a10b7-128">厳密な重複エントリチェックの実装は、プロバイダー固有です。</span><span class="sxs-lookup"><span data-stu-id="a10b7-128">The implementation of strict duplicate entry checking is provider specific.</span></span> <span data-ttu-id="a10b7-129">たとえば、プロバイダーは、同じ表示名とメッセージング アドレスの両方を持つ任意の 2 つのエントリとして厳密な一致を定義できます。</span><span class="sxs-lookup"><span data-stu-id="a10b7-129">For example, a provider can define a strict match as any two entries that have both the same display name and messaging address.</span></span>
    
<span data-ttu-id="a10b7-130">CREATE_REPLACE</span><span class="sxs-lookup"><span data-stu-id="a10b7-130">CREATE_REPLACE</span></span> 
  
> <span data-ttu-id="a10b7-131">2 つのエントリが重複すると判断された場合は、新しいエントリで既存のエントリを置き換える必要があります。</span><span class="sxs-lookup"><span data-stu-id="a10b7-131">Indicates that a new entry should replace an existing one if it is determined that the two are duplicates.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a10b7-132">戻り値</span><span class="sxs-lookup"><span data-stu-id="a10b7-132">Return value</span></span>

<span data-ttu-id="a10b7-133">S_OK</span><span class="sxs-lookup"><span data-stu-id="a10b7-133">S_OK</span></span> 
  
> <span data-ttu-id="a10b7-134">コピー操作が成功しました。</span><span class="sxs-lookup"><span data-stu-id="a10b7-134">The copy operation succeeded.</span></span>
    
<span data-ttu-id="a10b7-135">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="a10b7-135">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="a10b7-136">コピー操作は全体的に成功しましたが、1 つ以上のエントリをコピーする必要がありました。</span><span class="sxs-lookup"><span data-stu-id="a10b7-136">The copy operation succeeded overall, but one or more of the entries could not be copied.</span></span> <span data-ttu-id="a10b7-137">この値が返されると、呼び出しは正常に処理されます。</span><span class="sxs-lookup"><span data-stu-id="a10b7-137">When this value is returned, the call should be handled as successful.</span></span> <span data-ttu-id="a10b7-138">この値をテストするには、次のマクロ **HR_FAILED** します。</span><span class="sxs-lookup"><span data-stu-id="a10b7-138">To test for this value, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="a10b7-139">詳細については、「Using [Macros for Error Handling 」を参照してください](using-macros-for-error-handling.md)。</span><span class="sxs-lookup"><span data-stu-id="a10b7-139">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a10b7-140">注釈</span><span class="sxs-lookup"><span data-stu-id="a10b7-140">Remarks</span></span>

<span data-ttu-id="a10b7-141">**IABContainer::CopyEntries メソッドは**、同じコンテナーまたは別のコンテナーからエントリをコピーします。</span><span class="sxs-lookup"><span data-stu-id="a10b7-141">The **IABContainer::CopyEntries** method copies entries from the same container or a different container.</span></span> <span data-ttu-id="a10b7-142">**CopyEntries の呼び出し** は、コピーするエントリごとに次の呼び出しを行うのと機能的に同等です。</span><span class="sxs-lookup"><span data-stu-id="a10b7-142">A call to **CopyEntries** is functionally equivalent to making the following calls for each entry to be copied:</span></span> 
  
1. <span data-ttu-id="a10b7-143">[新しいエントリを作成する IABContainer::CreateEntry](iabcontainer-createentry.md)メソッド。</span><span class="sxs-lookup"><span data-stu-id="a10b7-143">The [IABContainer::CreateEntry](iabcontainer-createentry.md) method to create the new entry.</span></span> 
    
2. <span data-ttu-id="a10b7-144">コピーするエントリからプロパティを読み取る [IMAPIProp::GetProps](imapiprop-getprops.md) メソッド。</span><span class="sxs-lookup"><span data-stu-id="a10b7-144">The [IMAPIProp::GetProps](imapiprop-getprops.md) method to read properties from the entry to be copied.</span></span> 
    
3. <span data-ttu-id="a10b7-145">新 [しいエントリにプロパティを書き込む IMAPIProp::SetProps](imapiprop-setprops.md) メソッド。</span><span class="sxs-lookup"><span data-stu-id="a10b7-145">The [IMAPIProp::SetProps](imapiprop-setprops.md) method to write properties to the new entry.</span></span> 
    
4. <span data-ttu-id="a10b7-146">保存を実行する新 [しいエントリの IMAPIProp::SaveChanges](imapiprop-savechanges.md) メソッド。</span><span class="sxs-lookup"><span data-stu-id="a10b7-146">The new entry's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to perform a save.</span></span> 
    
5. <span data-ttu-id="a10b7-147">コンテナーの参照を解放する新しいエントリの [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) メソッド。</span><span class="sxs-lookup"><span data-stu-id="a10b7-147">The new entry's [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) method to release the container's reference.</span></span> 
    
## <a name="notes-to-implementers"></a><span data-ttu-id="a10b7-148">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="a10b7-148">Notes to implementers</span></span>

<span data-ttu-id="a10b7-149">**IABContainer::CopyEntries** メソッドをサポートするコンテナーはすべて、変更可能である必要があります。</span><span class="sxs-lookup"><span data-stu-id="a10b7-149">All containers that support the **IABContainer::CopyEntries** method must be modifiable.</span></span> <span data-ttu-id="a10b7-150">コンテナーの AB_MODIFIABLE **フラグを** PR_CONTAINER_FLAGS ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) プロパティに設定して、変更可能であることを示します。</span><span class="sxs-lookup"><span data-stu-id="a10b7-150">Set your container's AB_MODIFIABLE flag in its **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) property to indicate that it is modifiable.</span></span> 
  
<span data-ttu-id="a10b7-151">すべてのフラグをサポートする必要があります。ただし、これらのフラグの解釈と使用は実装固有です。つまり、CREATE_CHECK_DUP_LOOSE フラグと CREATE_CHECK_DUP_STRICT フラグのセマンティクスが実装のコンテキストで何を意味するのかを判断できます。</span><span class="sxs-lookup"><span data-stu-id="a10b7-151">You must support all of the flags; however, the interpretation and use of these flags is implementation specific—that is, you can determine what the semantics of the CREATE_CHECK_DUP_LOOSE and CREATE_CHECK_DUP_STRICT flags mean in the context of your implementation.</span></span> <span data-ttu-id="a10b7-152">エントリが重複するかどうかを判断できない場合、または判断できない場合は、常にエントリのコピーを許可します。</span><span class="sxs-lookup"><span data-stu-id="a10b7-152">If you cannot or do not determine whether an entry is a duplicate, always allow the entry to be copied.</span></span> 
  
<span data-ttu-id="a10b7-153">CREATE_REPLACE フラグが設定されている場合は、CREATE_CHECK_DUP_LOOSE または CREATE_CHECK_DUP_STRICT が設定されているかどうか、およびエントリが重複するかどうかに関係なく、常にエントリをコピーします。</span><span class="sxs-lookup"><span data-stu-id="a10b7-153">If the CREATE_REPLACE flag is set, always copy the entry regardless of whether CREATE_CHECK_DUP_LOOSE or CREATE_CHECK_DUP_STRICT is set and whether the entry is a duplicate.</span></span> 
  
<span data-ttu-id="a10b7-154">設定CREATE_REPLACE設定されていない場合は、CREATE_CHECK_DUP_STRICT重複を確認します。</span><span class="sxs-lookup"><span data-stu-id="a10b7-154">If CREATE_REPLACE is not set and CREATE_CHECK_DUP_STRICT is set, check for duplicates.</span></span> <span data-ttu-id="a10b7-155">エントリが重複と判断された場合は、そのエントリをコピーしない。</span><span class="sxs-lookup"><span data-stu-id="a10b7-155">If an entry is determined to be a duplicate, do not copy the entry.</span></span> 
  
<span data-ttu-id="a10b7-156">サポートする必要CREATE_REPLACE。サポートされていないCREATE_REPLACE、安全に無視して、常にコピーを実行できます。</span><span class="sxs-lookup"><span data-stu-id="a10b7-156">You do not need to support CREATE_REPLACE; not supporting CREATE_REPLACE means that you can safely ignore it and always perform a copy.</span></span> 
  
<span data-ttu-id="a10b7-157">重複しないエントリMAPI_W_PARTIAL_COMPLETIONコピーできない場合にのみ、警告メッセージを返します。</span><span class="sxs-lookup"><span data-stu-id="a10b7-157">Return the warning MAPI_W_PARTIAL_COMPLETION only if a nonduplicate entry cannot be copied.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a10b7-158">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="a10b7-158">Notes to callers</span></span>

<span data-ttu-id="a10b7-159">コンテナーで重複CREATE_CHECK_DUP_LOOSEチェックCREATE_CHECK_DUP_STRICTする方法をプロバイダーに示すフラグを使用します。</span><span class="sxs-lookup"><span data-stu-id="a10b7-159">Use the CREATE_CHECK_DUP_LOOSE and CREATE_CHECK_DUP_STRICT flags to indicate to the provider how you want the container to perform duplicate-entry checking.</span></span> <span data-ttu-id="a10b7-160">重複するかどうかに関係なく、エントリを追加する必要がある場合は、これらのフラグを設定したり、CREATE_REPLACE フラグを設定したりしません。</span><span class="sxs-lookup"><span data-stu-id="a10b7-160">If you need to have an entry added regardless of whether it is a duplicate, either do not set either of these flags or set the CREATE_REPLACE flag.</span></span> <span data-ttu-id="a10b7-161">CREATE_REPLACEは、エントリが重複している場合は気にしないかどうかを示します。常に元のエントリを置き換える必要があります。</span><span class="sxs-lookup"><span data-stu-id="a10b7-161">CREATE_REPLACE indicates that you do not care if an entry is a duplicate; you always want it to replace the original entry.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a10b7-162">関連項目</span><span class="sxs-lookup"><span data-stu-id="a10b7-162">See also</span></span>



[<span data-ttu-id="a10b7-163">ENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="a10b7-163">ENTRYLIST</span></span>](entrylist.md)
  
[<span data-ttu-id="a10b7-164">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="a10b7-164">IABContainer::CreateEntry</span></span>](iabcontainer-createentry.md)
  
[<span data-ttu-id="a10b7-165">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a10b7-165">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)
  
[<span data-ttu-id="a10b7-166">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="a10b7-166">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="a10b7-167">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="a10b7-167">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)

