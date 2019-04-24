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
# <a name="iabcontainercopyentries"></a><span data-ttu-id="20230-103">IABContainer::CopyEntries</span><span class="sxs-lookup"><span data-stu-id="20230-103">IABContainer::CopyEntries</span></span>

  
  
<span data-ttu-id="20230-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="20230-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="20230-105">1つまたは複数のエントリ (通常はメッセージングユーザーまたは配布リスト) をコピーします。</span><span class="sxs-lookup"><span data-stu-id="20230-105">Copies one or more entries, typically messaging users or distribution lists.</span></span>
  
```cpp
HRESULT CopyEntries(
  LPENTRYLIST lpEntries,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="20230-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20230-106">Parameters</span></span>

 <span data-ttu-id="20230-107">_lpentries_</span><span class="sxs-lookup"><span data-stu-id="20230-107">_lpEntries_</span></span>
  
> <span data-ttu-id="20230-108">順番コピーするエントリのエントリ識別子を含む[entrylist](entrylist.md)構造体の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="20230-108">[in] A pointer to an array of [ENTRYLIST](entrylist.md) structures that contains the entry identifiers of the entries to copy.</span></span> 
    
 <span data-ttu-id="20230-109">_uluiparam_</span><span class="sxs-lookup"><span data-stu-id="20230-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="20230-110">順番このメソッドが表示するダイアログボックスまたはウィンドウの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="20230-110">[in] The handle to the parent window of any dialog boxes or windows that this method displays.</span></span> <span data-ttu-id="20230-111">_ulflags_パラメーターに AB_NO_DIALOG フラグが設定されている場合、 _uluiparam_パラメーターは0である必要があります。</span><span class="sxs-lookup"><span data-stu-id="20230-111">The  _ulUIParam_ parameter must be zero if the AB_NO_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="20230-112">_lpprogress_</span><span class="sxs-lookup"><span data-stu-id="20230-112">_lpProgress_</span></span>
  
> <span data-ttu-id="20230-113">順番進行状況インジケーターを表示する progress オブジェクトへのポインター、または NULL。</span><span class="sxs-lookup"><span data-stu-id="20230-113">[in] A pointer to a progress object that displays a progress indicator, or NULL.</span></span> <span data-ttu-id="20230-114">_lpprogress_が NULL の場合、 [imapisupport::D oprogress dialog](imapisupport-doprogressdialog.md)メソッドによって、MAPI によって提供される progress オブジェクトを使用して進行状況インジケーターを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="20230-114">If  _lpProgress_ is NULL, a progress indicator should be displayed by using the progress object supplied by MAPI through the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method.</span></span> <span data-ttu-id="20230-115">AB_NO_DIALOG フラグが_ulflags_で設定されている場合、 _lpprogress_パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="20230-115">The  _lpProgress_ parameter is ignored if the AB_NO_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="20230-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="20230-116">_ulFlags_</span></span>
  
> <span data-ttu-id="20230-117">順番コピー操作の実行方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="20230-117">[in] A bitmask of flags that controls how the copy operation is performed.</span></span> <span data-ttu-id="20230-118">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="20230-118">The following flags can be set:</span></span>
    
<span data-ttu-id="20230-119">AB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="20230-119">AB_NO_DIALOG</span></span> 
  
> <span data-ttu-id="20230-120">進行状況インジケーターの表示を抑制します。</span><span class="sxs-lookup"><span data-stu-id="20230-120">Suppresses display of a progress indicator.</span></span> <span data-ttu-id="20230-121">このフラグが設定されていない場合は、進行状況のインジケーターが表示されます。</span><span class="sxs-lookup"><span data-stu-id="20230-121">If this flag is not set, a progress indicator is displayed.</span></span>
    
<span data-ttu-id="20230-122">CREATE_CHECK_DUP_LOOSE</span><span class="sxs-lookup"><span data-stu-id="20230-122">CREATE_CHECK_DUP_LOOSE</span></span> 
  
> <span data-ttu-id="20230-123">重複したエントリのチェックを緩やかに実行する必要があることを示します。</span><span class="sxs-lookup"><span data-stu-id="20230-123">Indicates that a loose level of duplicate entry checking should be performed.</span></span> <span data-ttu-id="20230-124">重複していない重複するエントリのチェックは、プロバイダーに固有のものです。</span><span class="sxs-lookup"><span data-stu-id="20230-124">The implementation of loose duplicate entry checking is provider specific.</span></span> <span data-ttu-id="20230-125">たとえば、プロバイダーは、同じ表示名を持つ2つのエントリとして緩やかな一致を定義できます。</span><span class="sxs-lookup"><span data-stu-id="20230-125">For example, a provider can define a loose match as any two entries that have the same display name.</span></span>
    
<span data-ttu-id="20230-126">CREATE_CHECK_DUP_STRICT</span><span class="sxs-lookup"><span data-stu-id="20230-126">CREATE_CHECK_DUP_STRICT</span></span> 
  
> <span data-ttu-id="20230-127">重複するエントリの厳密なチェックを実行する必要があることを示します。</span><span class="sxs-lookup"><span data-stu-id="20230-127">Indicates that a strict level of duplicate entry checking should be performed.</span></span> <span data-ttu-id="20230-128">厳密に重複したエントリチェックの実装は、プロバイダーに固有のものです。</span><span class="sxs-lookup"><span data-stu-id="20230-128">The implementation of strict duplicate entry checking is provider specific.</span></span> <span data-ttu-id="20230-129">たとえば、プロバイダーは、同じ表示名とメッセージアドレスの両方を持つ2つのエントリとして厳密な一致を定義できます。</span><span class="sxs-lookup"><span data-stu-id="20230-129">For example, a provider can define a strict match as any two entries that have both the same display name and messaging address.</span></span>
    
<span data-ttu-id="20230-130">CREATE_REPLACE</span><span class="sxs-lookup"><span data-stu-id="20230-130">CREATE_REPLACE</span></span> 
  
> <span data-ttu-id="20230-131">2つのレコードが重複していると判断された場合は、新しいエントリで既存のエントリを置き換える必要があることを示します。</span><span class="sxs-lookup"><span data-stu-id="20230-131">Indicates that a new entry should replace an existing one if it is determined that the two are duplicates.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="20230-132">戻り値</span><span class="sxs-lookup"><span data-stu-id="20230-132">Return value</span></span>

<span data-ttu-id="20230-133">S_OK</span><span class="sxs-lookup"><span data-stu-id="20230-133">S_OK</span></span> 
  
> <span data-ttu-id="20230-134">コピー操作が正常に完了しました。</span><span class="sxs-lookup"><span data-stu-id="20230-134">The copy operation succeeded.</span></span>
    
<span data-ttu-id="20230-135">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="20230-135">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="20230-136">全体のコピー操作に成功しましたが、1つ以上のエントリをコピーできませんでした。</span><span class="sxs-lookup"><span data-stu-id="20230-136">The copy operation succeeded overall, but one or more of the entries could not be copied.</span></span> <span data-ttu-id="20230-137">この値が返されると、呼び出しが成功したとして処理されます。</span><span class="sxs-lookup"><span data-stu-id="20230-137">When this value is returned, the call should be handled as successful.</span></span> <span data-ttu-id="20230-138">この値をテストするには、 **HR_FAILED**マクロを使用します。</span><span class="sxs-lookup"><span data-stu-id="20230-138">To test for this value, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="20230-139">詳細については、「[エラー処理にマクロを使用する](using-macros-for-error-handling.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20230-139">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="20230-140">解説</span><span class="sxs-lookup"><span data-stu-id="20230-140">Remarks</span></span>

<span data-ttu-id="20230-141">**IABContainer:: copyentries**メソッドは、同じコンテナーまたは別のコンテナーからエントリをコピーします。</span><span class="sxs-lookup"><span data-stu-id="20230-141">The **IABContainer::CopyEntries** method copies entries from the same container or a different container.</span></span> <span data-ttu-id="20230-142">**copyentries**の呼び出しは、各エントリのコピーに対して次の呼び出しを行うことと機能的には同じです。</span><span class="sxs-lookup"><span data-stu-id="20230-142">A call to **CopyEntries** is functionally equivalent to making the following calls for each entry to be copied:</span></span> 
  
1. <span data-ttu-id="20230-143">[IABContainer:: createentry](iabcontainer-createentry.md)メソッドを実行して、新しいエントリを作成します。</span><span class="sxs-lookup"><span data-stu-id="20230-143">The [IABContainer::CreateEntry](iabcontainer-createentry.md) method to create the new entry.</span></span> 
    
2. <span data-ttu-id="20230-144">コピーするエントリからプロパティを読み取るための[imapiprop:: GetProps](imapiprop-getprops.md)メソッド。</span><span class="sxs-lookup"><span data-stu-id="20230-144">The [IMAPIProp::GetProps](imapiprop-getprops.md) method to read properties from the entry to be copied.</span></span> 
    
3. <span data-ttu-id="20230-145">[imapiprop:: setprops](imapiprop-setprops.md)メソッドを実行して、新しいエントリにプロパティを書き込みます。</span><span class="sxs-lookup"><span data-stu-id="20230-145">The [IMAPIProp::SetProps](imapiprop-setprops.md) method to write properties to the new entry.</span></span> 
    
4. <span data-ttu-id="20230-146">保存を実行するための、新しいエントリの[imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッド。</span><span class="sxs-lookup"><span data-stu-id="20230-146">The new entry's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to perform a save.</span></span> 
    
5. <span data-ttu-id="20230-147">コンテナーの参照を解放するための、新しいエントリの[IUnknown:: release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx)メソッド。</span><span class="sxs-lookup"><span data-stu-id="20230-147">The new entry's [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) method to release the container's reference.</span></span> 
    
## <a name="notes-to-implementers"></a><span data-ttu-id="20230-148">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="20230-148">Notes to implementers</span></span>

<span data-ttu-id="20230-149">**IABContainer:: copyentries**メソッドをサポートするすべてのコンテナーを変更可能にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="20230-149">All containers that support the **IABContainer::CopyEntries** method must be modifiable.</span></span> <span data-ttu-id="20230-150">コンテナーの AB_MODIFIABLE フラグを**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) プロパティに設定して、それが変更可能であることを示します。</span><span class="sxs-lookup"><span data-stu-id="20230-150">Set your container's AB_MODIFIABLE flag in its **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) property to indicate that it is modifiable.</span></span> 
  
<span data-ttu-id="20230-151">すべてのフラグをサポートする必要があります。ただし、これらのフラグの解釈と使用は実装に固有です。つまり、実装のコンテキストで CREATE_CHECK_DUP_LOOSE と CREATE_CHECK_DUP_STRICT のフラグの意味を判断できます。</span><span class="sxs-lookup"><span data-stu-id="20230-151">You must support all of the flags; however, the interpretation and use of these flags is implementation specific—that is, you can determine what the semantics of the CREATE_CHECK_DUP_LOOSE and CREATE_CHECK_DUP_STRICT flags mean in the context of your implementation.</span></span> <span data-ttu-id="20230-152">エントリが重複しているかどうかを判断できない場合、または指定しない場合は、常にエントリのコピーが許可されます。</span><span class="sxs-lookup"><span data-stu-id="20230-152">If you cannot or do not determine whether an entry is a duplicate, always allow the entry to be copied.</span></span> 
  
<span data-ttu-id="20230-153">CREATE_REPLACE フラグが設定されている場合は、CREATE_CHECK_DUP_LOOSE または CREATE_CHECK_DUP_STRICT が設定されているかどうかと、エントリが重複しているかどうかに関係なく、常にエントリをコピーします。</span><span class="sxs-lookup"><span data-stu-id="20230-153">If the CREATE_REPLACE flag is set, always copy the entry regardless of whether CREATE_CHECK_DUP_LOOSE or CREATE_CHECK_DUP_STRICT is set and whether the entry is a duplicate.</span></span> 
  
<span data-ttu-id="20230-154">CREATE_REPLACE が設定されておらず、CREATE_CHECK_DUP_STRICT が設定されている場合は、重複をチェックします。</span><span class="sxs-lookup"><span data-stu-id="20230-154">If CREATE_REPLACE is not set and CREATE_CHECK_DUP_STRICT is set, check for duplicates.</span></span> <span data-ttu-id="20230-155">エントリが重複していると判断された場合は、エントリをコピーしないでください。</span><span class="sxs-lookup"><span data-stu-id="20230-155">If an entry is determined to be a duplicate, do not copy the entry.</span></span> 
  
<span data-ttu-id="20230-156">CREATE_REPLACE をサポートする必要はありません。CREATE_REPLACE をサポートしていない場合は、無視して安全にコピーを実行できることを意味します。</span><span class="sxs-lookup"><span data-stu-id="20230-156">You do not need to support CREATE_REPLACE; not supporting CREATE_REPLACE means that you can safely ignore it and always perform a copy.</span></span> 
  
<span data-ttu-id="20230-157">重複していないエントリをコピーできない場合にのみ、警告 MAPI_W_PARTIAL_COMPLETION を返します。</span><span class="sxs-lookup"><span data-stu-id="20230-157">Return the warning MAPI_W_PARTIAL_COMPLETION only if a nonduplicate entry cannot be copied.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="20230-158">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="20230-158">Notes to callers</span></span>

<span data-ttu-id="20230-159">CREATE_CHECK_DUP_LOOSE および CREATE_CHECK_DUP_STRICT フラグを使用して、コンテナーが複製入力チェックを実行する方法をプロバイダーに示します。</span><span class="sxs-lookup"><span data-stu-id="20230-159">Use the CREATE_CHECK_DUP_LOOSE and CREATE_CHECK_DUP_STRICT flags to indicate to the provider how you want the container to perform duplicate-entry checking.</span></span> <span data-ttu-id="20230-160">重複しているかどうかにかかわらずエントリを追加する必要がある場合は、これらのフラグのどちらも設定しないか、CREATE_REPLACE フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="20230-160">If you need to have an entry added regardless of whether it is a duplicate, either do not set either of these flags or set the CREATE_REPLACE flag.</span></span> <span data-ttu-id="20230-161">CREATE_REPLACE は、エントリが重複していてもかまわないことを示します。常に、元のエントリを置換することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="20230-161">CREATE_REPLACE indicates that you do not care if an entry is a duplicate; you always want it to replace the original entry.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="20230-162">関連項目</span><span class="sxs-lookup"><span data-stu-id="20230-162">See also</span></span>



[<span data-ttu-id="20230-163">ENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="20230-163">ENTRYLIST</span></span>](entrylist.md)
  
[<span data-ttu-id="20230-164">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="20230-164">IABContainer::CreateEntry</span></span>](iabcontainer-createentry.md)
  
[<span data-ttu-id="20230-165">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="20230-165">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)
  
[<span data-ttu-id="20230-166">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="20230-166">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="20230-167">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="20230-167">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)

