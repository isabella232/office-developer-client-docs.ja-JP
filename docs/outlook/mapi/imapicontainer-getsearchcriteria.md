---
title: IMAPIContainerGetSearchCriteria
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer.GetSearchCriteria
api_type:
- COM
ms.assetid: 41b6c162-9984-43a3-b38e-44f0afae67de
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7845238722ce81b84210b6f4fc33f9df0abacc07
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412024"
---
# <a name="imapicontainergetsearchcriteria"></a><span data-ttu-id="c8656-103">IMAPIContainer::GetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="c8656-103">IMAPIContainer::GetSearchCriteria</span></span>

  
  
<span data-ttu-id="c8656-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c8656-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c8656-105">コンテナーの検索条件を取得します。</span><span class="sxs-lookup"><span data-stu-id="c8656-105">Obtains the search criteria for the container.</span></span>
  
```cpp
HRESULT GetSearchCriteria(
  ULONG ulFlags,
  LPSRestriction FAR * lppRestriction,
  LPENTRYLIST FAR * lppContainerList,
  ULONG FAR * lpulSearchState
);
```

## <a name="parameters"></a><span data-ttu-id="c8656-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c8656-106">Parameters</span></span>

 <span data-ttu-id="c8656-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c8656-107">_ulFlags_</span></span>
  
> <span data-ttu-id="c8656-108">[in]渡された文字列の種類を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="c8656-108">[in] A bitmask of flags that controls the type of the passed-in strings.</span></span> <span data-ttu-id="c8656-109">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="c8656-109">The following flag can be set:</span></span>
    
<span data-ttu-id="c8656-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c8656-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="c8656-111">渡された文字列は Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="c8656-111">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="c8656-112">このフラグMAPI_UNICODE設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="c8656-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="c8656-113">_lppRestriction_</span><span class="sxs-lookup"><span data-stu-id="c8656-113">_lppRestriction_</span></span>
  
> <span data-ttu-id="c8656-114">[out]検索条件を定義する [SRestriction](srestriction.md) 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="c8656-114">[out] A pointer to a pointer to an [SRestriction](srestriction.md) structure that defines the search criteria.</span></span> <span data-ttu-id="c8656-115">クライアント アプリケーションが  _lppRestriction_ パラメーターで NULL を渡した場合 **、GetSearchCriteria** は **SRestriction 構造を返す必要** があります。</span><span class="sxs-lookup"><span data-stu-id="c8656-115">If a client application passes NULL in the  _lppRestriction_ parameter, **GetSearchCriteria** does not return an **SRestriction** structure.</span></span> 
    
 <span data-ttu-id="c8656-116">_lppContainerList_</span><span class="sxs-lookup"><span data-stu-id="c8656-116">_lppContainerList_</span></span>
  
> <span data-ttu-id="c8656-117">[out]検索に含めるコンテナーを表すエントリ識別子の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="c8656-117">[out] A pointer to a pointer to an array of entry identifiers that represent containers to be included in the search.</span></span> <span data-ttu-id="c8656-118">クライアントが  _lppContainerList_ パラメーターで NULL を渡した場合 **、GetSearchCriteria** はエントリ識別子の配列を返します。</span><span class="sxs-lookup"><span data-stu-id="c8656-118">If a client passes NULL in the  _lppContainerList_ parameter, **GetSearchCriteria** does not return an array of entry identifiers.</span></span> 
    
 <span data-ttu-id="c8656-119">_lpulSearchState_</span><span class="sxs-lookup"><span data-stu-id="c8656-119">_lpulSearchState_</span></span>
  
> <span data-ttu-id="c8656-120">[out]検索の現在の状態を示すために使用されるフラグのビットマスクへのポインター。</span><span class="sxs-lookup"><span data-stu-id="c8656-120">[out] A pointer to a bitmask of flags used to indicate the current state of the search.</span></span> <span data-ttu-id="c8656-121">クライアントが  _lpulSearchState_ パラメーターで NULL を渡した場合 **、GetSearchCriteria は** フラグを返します。</span><span class="sxs-lookup"><span data-stu-id="c8656-121">If a client passes NULL in the  _lpulSearchState_ parameter, **GetSearchCriteria** returns no flags.</span></span> <span data-ttu-id="c8656-122">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="c8656-122">The following flags can be set:</span></span> 
    
<span data-ttu-id="c8656-123">SEARCH_FOREGROUND</span><span class="sxs-lookup"><span data-stu-id="c8656-123">SEARCH_FOREGROUND</span></span> 
  
> <span data-ttu-id="c8656-124">検索は、他の検索と相対的に高い優先度で実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c8656-124">The search should run at high priority relative to other searches.</span></span> <span data-ttu-id="c8656-125">このフラグが設定されていない場合、検索は他の検索に対して通常の優先度で実行されます。</span><span class="sxs-lookup"><span data-stu-id="c8656-125">If this flag is not set, the search runs at normal priority relative to other searches.</span></span>
    
<span data-ttu-id="c8656-126">SEARCH_REBUILD</span><span class="sxs-lookup"><span data-stu-id="c8656-126">SEARCH_REBUILD</span></span> 
  
> <span data-ttu-id="c8656-127">検索は CPU 負荷の高い操作モードで、条件に一致するメッセージを検索します。</span><span class="sxs-lookup"><span data-stu-id="c8656-127">The search is in the CPU-intensive mode of its operation, trying to locate messages that match the criteria.</span></span> <span data-ttu-id="c8656-128">このフラグが設定されていない場合、検索の操作の CPU 負荷の高い部分は終了します。</span><span class="sxs-lookup"><span data-stu-id="c8656-128">If this flag is not set, the CPU-intensive part of the search's operation is over.</span></span> <span data-ttu-id="c8656-129">このフラグは、検索がアクティブである場合にのみ意味を持ちます (つまり、SEARCH_RUNNINGフラグが設定されている場合)。</span><span class="sxs-lookup"><span data-stu-id="c8656-129">This flag has meaning only if the search is active (that is, if the SEARCH_RUNNING flag is set).</span></span>
    
<span data-ttu-id="c8656-130">SEARCH_RECURSIVE</span><span class="sxs-lookup"><span data-stu-id="c8656-130">SEARCH_RECURSIVE</span></span> 
  
> <span data-ttu-id="c8656-131">検索では、指定したコンテナーとそのすべての子コンテナーで、一致するエントリが検索されます。</span><span class="sxs-lookup"><span data-stu-id="c8656-131">The search is looking in specified containers and all their child containers for matching entries.</span></span> <span data-ttu-id="c8656-132">このフラグが設定されていない場合 [、IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) メソッドの最後の呼び出しに明示的に含まれるコンテナーだけが検索されます。</span><span class="sxs-lookup"><span data-stu-id="c8656-132">If this flag is not set, only the containers explicitly included in the last call to the [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method are being searched.</span></span> 
    
<span data-ttu-id="c8656-133">SEARCH_RUNNING</span><span class="sxs-lookup"><span data-stu-id="c8656-133">SEARCH_RUNNING</span></span> 
  
> <span data-ttu-id="c8656-134">検索がアクティブで、コンテナーのコンテンツ テーブルが更新され、メッセージ ストアまたはアドレス帳の変更が反映されます。</span><span class="sxs-lookup"><span data-stu-id="c8656-134">The search is active and the container's contents table is being updated to reflect changes in the message store or address book.</span></span> <span data-ttu-id="c8656-135">このフラグが設定されていない場合、検索は非アクティブであり、コンテンツ テーブルは静的です。</span><span class="sxs-lookup"><span data-stu-id="c8656-135">If this flag is not set, the search is inactive and the contents table is static.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c8656-136">戻り値</span><span class="sxs-lookup"><span data-stu-id="c8656-136">Return value</span></span>

<span data-ttu-id="c8656-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="c8656-137">S_OK</span></span> 
  
> <span data-ttu-id="c8656-138">検索条件が正常に取得されました。</span><span class="sxs-lookup"><span data-stu-id="c8656-138">The search criteria was successfully obtained.</span></span>
    
<span data-ttu-id="c8656-139">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="c8656-139">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="c8656-140">このフラグMAPI_UNICODE設定され、実装が Unicode をサポートしていないか、または設定されていないMAPI_UNICODE実装が Unicode のみをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="c8656-140">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="c8656-141">MAPI_E_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="c8656-141">MAPI_E_NOT_INITIALIZED</span></span> 
  
> <span data-ttu-id="c8656-142">コンテナーに対して検索条件が確立されていませんでした。</span><span class="sxs-lookup"><span data-stu-id="c8656-142">Search criteria were never established for the container.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c8656-143">注釈</span><span class="sxs-lookup"><span data-stu-id="c8656-143">Remarks</span></span>

<span data-ttu-id="c8656-144">**IMAPIContainer::GetSearchCriteria** メソッドは、検索をサポートするコンテナー (通常は検索結果フォルダー) の検索条件を取得します。</span><span class="sxs-lookup"><span data-stu-id="c8656-144">The **IMAPIContainer::GetSearchCriteria** method obtains the search criteria for a container that supports searches, typically a search-results folder.</span></span> <span data-ttu-id="c8656-145">検索条件を作成するには、コンテナーの **IMAPIContainer::SetSearchCriteria メソッドを呼び出** します。</span><span class="sxs-lookup"><span data-stu-id="c8656-145">You create search criteria by calling a container's **IMAPIContainer::SetSearchCriteria** method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="c8656-146">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="c8656-146">Notes to implementers</span></span>

<span data-ttu-id="c8656-147">アドレス帳コンテナーは **、GetSearchCriteria** プロパティ [(PidTagSearch)](pidtagsearch-canonical-property.md)プロパティに関連付けられている高度な検索機能を提供する場合にのみ **、PR_SEARCH** GetSearchCriteria をサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c8656-147">Address book containers may need to support **GetSearchCriteria** only if they provide the advanced search capabilities associated with the **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) property.</span></span> <span data-ttu-id="c8656-148">アドレス帳コンテナーの高度な検索機能を実装する方法の詳細については [、「Implementing Advanced Searching」を参照してください](implementing-advanced-searching.md)。</span><span class="sxs-lookup"><span data-stu-id="c8656-148">For more information about how to implement the advanced search feature for address book containers, see [Implementing Advanced Searching](implementing-advanced-searching.md).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="c8656-149">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="c8656-149">Notes to callers</span></span>

<span data-ttu-id="c8656-150">_lppRestriction_ パラメーターと _lppContainerList_ パラメーターが示すデータ構造が終了したら、リリースする構造体ごとに [MAPIFreeBuffer](mapifreebuffer.md)を 1 回呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c8656-150">When you are finished with the data structures pointed to by the  _lppRestriction_ and  _lppContainerList_ parameters, call [MAPIFreeBuffer](mapifreebuffer.md) once for each structure to be released.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c8656-151">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="c8656-151">MFCMAPI reference</span></span>

<span data-ttu-id="c8656-152">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c8656-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c8656-153">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="c8656-153">**File**</span></span>|<span data-ttu-id="c8656-154">**関数**</span><span class="sxs-lookup"><span data-stu-id="c8656-154">**Function**</span></span>|<span data-ttu-id="c8656-155">**コメント**</span><span class="sxs-lookup"><span data-stu-id="c8656-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c8656-156">HierarchyTableDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="c8656-156">HierarchyTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="c8656-157">CHierarchyTableDlg::OnEditSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="c8656-157">CHierarchyTableDlg::OnEditSearchCriteria</span></span>  <br/> |<span data-ttu-id="c8656-158">MFCMAPI は **IMAPIContainer::GetSearchCriteria** メソッドを使用して、表示するフォルダーから検索条件を取得します。</span><span class="sxs-lookup"><span data-stu-id="c8656-158">MFCMAPI uses the **IMAPIContainer::GetSearchCriteria** method to obtain search criteria from a folder to display.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c8656-159">関連項目</span><span class="sxs-lookup"><span data-stu-id="c8656-159">See also</span></span>



[<span data-ttu-id="c8656-160">IMAPIContainer::SetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="c8656-160">IMAPIContainer::SetSearchCriteria</span></span>](imapicontainer-setsearchcriteria.md)
  
[<span data-ttu-id="c8656-161">IMAPIFolder::CreateFolder</span><span class="sxs-lookup"><span data-stu-id="c8656-161">IMAPIFolder::CreateFolder</span></span>](imapifolder-createfolder.md)
  
[<span data-ttu-id="c8656-162">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="c8656-162">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="c8656-163">PidTagSearch 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c8656-163">PidTagSearch Canonical Property</span></span>](pidtagsearch-canonical-property.md)
  
[<span data-ttu-id="c8656-164">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="c8656-164">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


<span data-ttu-id="c8656-165">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="c8656-165">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

