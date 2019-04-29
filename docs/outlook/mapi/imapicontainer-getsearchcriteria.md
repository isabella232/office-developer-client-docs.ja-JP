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
# <a name="imapicontainergetsearchcriteria"></a><span data-ttu-id="79660-103">IMAPIContainer::GetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="79660-103">IMAPIContainer::GetSearchCriteria</span></span>

  
  
<span data-ttu-id="79660-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="79660-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="79660-105">コンテナーの検索条件を取得します。</span><span class="sxs-lookup"><span data-stu-id="79660-105">Obtains the search criteria for the container.</span></span>
  
```cpp
HRESULT GetSearchCriteria(
  ULONG ulFlags,
  LPSRestriction FAR * lppRestriction,
  LPENTRYLIST FAR * lppContainerList,
  ULONG FAR * lpulSearchState
);
```

## <a name="parameters"></a><span data-ttu-id="79660-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="79660-106">Parameters</span></span>

 <span data-ttu-id="79660-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="79660-107">_ulFlags_</span></span>
  
> <span data-ttu-id="79660-108">順番渡された文字列の種類を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="79660-108">[in] A bitmask of flags that controls the type of the passed-in strings.</span></span> <span data-ttu-id="79660-109">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="79660-109">The following flag can be set:</span></span>
    
<span data-ttu-id="79660-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="79660-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="79660-111">渡された文字列は Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="79660-111">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="79660-112">MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="79660-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="79660-113">_lppRestriction_</span><span class="sxs-lookup"><span data-stu-id="79660-113">_lppRestriction_</span></span>
  
> <span data-ttu-id="79660-114">読み上げ検索条件を定義する[srestriction](srestriction.md)構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="79660-114">[out] A pointer to a pointer to an [SRestriction](srestriction.md) structure that defines the search criteria.</span></span> <span data-ttu-id="79660-115">クライアントアプリケーションが_lppRestriction_パラメーターで NULL を渡した場合、 **getsearchcriteria**は**srestriction**構造を返しません。</span><span class="sxs-lookup"><span data-stu-id="79660-115">If a client application passes NULL in the  _lppRestriction_ parameter, **GetSearchCriteria** does not return an **SRestriction** structure.</span></span> 
    
 <span data-ttu-id="79660-116">_lppContainerList_</span><span class="sxs-lookup"><span data-stu-id="79660-116">_lppContainerList_</span></span>
  
> <span data-ttu-id="79660-117">読み上げ検索に含めるコンテナーを表すエントリ識別子の配列へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="79660-117">[out] A pointer to a pointer to an array of entry identifiers that represent containers to be included in the search.</span></span> <span data-ttu-id="79660-118">クライアントが_lppContainerList_パラメーターで NULL を渡した場合、 **getsearchcriteria**はエントリ識別子の配列を返しません。</span><span class="sxs-lookup"><span data-stu-id="79660-118">If a client passes NULL in the  _lppContainerList_ parameter, **GetSearchCriteria** does not return an array of entry identifiers.</span></span> 
    
 <span data-ttu-id="79660-119">_lpulsearchstate_</span><span class="sxs-lookup"><span data-stu-id="79660-119">_lpulSearchState_</span></span>
  
> <span data-ttu-id="79660-120">読み上げ検索の現在の状態を示すために使用されるフラグのビットマスクへのポインター。</span><span class="sxs-lookup"><span data-stu-id="79660-120">[out] A pointer to a bitmask of flags used to indicate the current state of the search.</span></span> <span data-ttu-id="79660-121">クライアントが_lpulsearchstate_パラメーターで NULL を渡すと、 **getsearchcriteria**はフラグを返しません。</span><span class="sxs-lookup"><span data-stu-id="79660-121">If a client passes NULL in the  _lpulSearchState_ parameter, **GetSearchCriteria** returns no flags.</span></span> <span data-ttu-id="79660-122">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="79660-122">The following flags can be set:</span></span> 
    
<span data-ttu-id="79660-123">SEARCH_FOREGROUND</span><span class="sxs-lookup"><span data-stu-id="79660-123">SEARCH_FOREGROUND</span></span> 
  
> <span data-ttu-id="79660-124">検索は、他の検索と比較して高い優先度で実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="79660-124">The search should run at high priority relative to other searches.</span></span> <span data-ttu-id="79660-125">このフラグが設定されていない場合、検索は他の検索と比較して標準の優先度で実行されます。</span><span class="sxs-lookup"><span data-stu-id="79660-125">If this flag is not set, the search runs at normal priority relative to other searches.</span></span>
    
<span data-ttu-id="79660-126">SEARCH_REBUILD</span><span class="sxs-lookup"><span data-stu-id="79660-126">SEARCH_REBUILD</span></span> 
  
> <span data-ttu-id="79660-127">検索は、CPU を集中的に消費する操作で、条件に一致するメッセージを見つけようとしています。</span><span class="sxs-lookup"><span data-stu-id="79660-127">The search is in the CPU-intensive mode of its operation, trying to locate messages that match the criteria.</span></span> <span data-ttu-id="79660-128">このフラグが設定されていない場合は、検索の処理の CPU に負荷のかかる部分があります。</span><span class="sxs-lookup"><span data-stu-id="79660-128">If this flag is not set, the CPU-intensive part of the search's operation is over.</span></span> <span data-ttu-id="79660-129">このフラグは、検索がアクティブである場合 (つまり、SEARCH_RUNNING フラグが設定されている場合) にのみ意味を持ちます。</span><span class="sxs-lookup"><span data-stu-id="79660-129">This flag has meaning only if the search is active (that is, if the SEARCH_RUNNING flag is set).</span></span>
    
<span data-ttu-id="79660-130">SEARCH_RECURSIVE</span><span class="sxs-lookup"><span data-stu-id="79660-130">SEARCH_RECURSIVE</span></span> 
  
> <span data-ttu-id="79660-131">指定されたコンテナーと、そのすべての子コンテナーを検索して、一致するエントリを探します。</span><span class="sxs-lookup"><span data-stu-id="79660-131">The search is looking in specified containers and all their child containers for matching entries.</span></span> <span data-ttu-id="79660-132">このフラグが設定されていない場合、 [IMAPIContainer:: setsearchcriteria](imapicontainer-setsearchcriteria.md)メソッドへの最後の呼び出しに明示的に含まれているコンテナーのみが検索されます。</span><span class="sxs-lookup"><span data-stu-id="79660-132">If this flag is not set, only the containers explicitly included in the last call to the [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method are being searched.</span></span> 
    
<span data-ttu-id="79660-133">SEARCH_RUNNING</span><span class="sxs-lookup"><span data-stu-id="79660-133">SEARCH_RUNNING</span></span> 
  
> <span data-ttu-id="79660-134">検索がアクティブで、メッセージストアまたはアドレス帳の変更を反映するためにコンテナーの contents テーブルが更新されています。</span><span class="sxs-lookup"><span data-stu-id="79660-134">The search is active and the container's contents table is being updated to reflect changes in the message store or address book.</span></span> <span data-ttu-id="79660-135">このフラグが設定されていない場合、検索は非アクティブで、contents テーブルは静的です。</span><span class="sxs-lookup"><span data-stu-id="79660-135">If this flag is not set, the search is inactive and the contents table is static.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="79660-136">戻り値</span><span class="sxs-lookup"><span data-stu-id="79660-136">Return value</span></span>

<span data-ttu-id="79660-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="79660-137">S_OK</span></span> 
  
> <span data-ttu-id="79660-138">検索条件が正常に取得されました。</span><span class="sxs-lookup"><span data-stu-id="79660-138">The search criteria was successfully obtained.</span></span>
    
<span data-ttu-id="79660-139">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="79660-139">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="79660-140">MAPI_UNICODE フラグが設定されていて、実装が unicode をサポートしていないか、または MAPI_UNICODE が設定されておらず、実装で unicode のみがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="79660-140">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="79660-141">MAPI_E_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="79660-141">MAPI_E_NOT_INITIALIZED</span></span> 
  
> <span data-ttu-id="79660-142">コンテナーに対して検索条件が設定されていません。</span><span class="sxs-lookup"><span data-stu-id="79660-142">Search criteria were never established for the container.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="79660-143">注釈</span><span class="sxs-lookup"><span data-stu-id="79660-143">Remarks</span></span>

<span data-ttu-id="79660-144">**IMAPIContainer:: getsearchcriteria**メソッドは、通常、検索結果フォルダーである検索をサポートするコンテナーの検索条件を取得します。</span><span class="sxs-lookup"><span data-stu-id="79660-144">The **IMAPIContainer::GetSearchCriteria** method obtains the search criteria for a container that supports searches, typically a search-results folder.</span></span> <span data-ttu-id="79660-145">検索条件を作成するには、コンテナーの**IMAPIContainer:: setsearchcriteria**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="79660-145">You create search criteria by calling a container's **IMAPIContainer::SetSearchCriteria** method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="79660-146">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="79660-146">Notes to implementers</span></span>

<span data-ttu-id="79660-147">**PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) プロパティに関連付けられている高度な検索機能を提供する場合にのみ、アドレス帳コンテナーで**getsearchcriteria**をサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="79660-147">Address book containers may need to support **GetSearchCriteria** only if they provide the advanced search capabilities associated with the **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) property.</span></span> <span data-ttu-id="79660-148">アドレス帳コンテナーの高度な検索機能を実装する方法の詳細については、「[高度な](implementing-advanced-searching.md)検索の実装」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="79660-148">For more information about how to implement the advanced search feature for address book containers, see [Implementing Advanced Searching](implementing-advanced-searching.md).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="79660-149">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="79660-149">Notes to callers</span></span>

<span data-ttu-id="79660-150">_lppRestriction_パラメーターと_lppContainerList_パラメーターで示されるデータ構造が完成したら、各構造体を解放するために、 [MAPIFreeBuffer](mapifreebuffer.md)を1回呼び出します。</span><span class="sxs-lookup"><span data-stu-id="79660-150">When you are finished with the data structures pointed to by the  _lppRestriction_ and  _lppContainerList_ parameters, call [MAPIFreeBuffer](mapifreebuffer.md) once for each structure to be released.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="79660-151">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="79660-151">MFCMAPI reference</span></span>

<span data-ttu-id="79660-152">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="79660-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="79660-153">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="79660-153">**File**</span></span>|<span data-ttu-id="79660-154">**関数**</span><span class="sxs-lookup"><span data-stu-id="79660-154">**Function**</span></span>|<span data-ttu-id="79660-155">**コメント**</span><span class="sxs-lookup"><span data-stu-id="79660-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="79660-156">HierarchyTableDlg</span><span class="sxs-lookup"><span data-stu-id="79660-156">HierarchyTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="79660-157">CHierarchyTableDlg:: oneditsearchcriteria</span><span class="sxs-lookup"><span data-stu-id="79660-157">CHierarchyTableDlg::OnEditSearchCriteria</span></span>  <br/> |<span data-ttu-id="79660-158">mfcmapi は、 **IMAPIContainer:: getsearchcriteria**メソッドを使用して、フォルダーから表示する検索条件を取得します。</span><span class="sxs-lookup"><span data-stu-id="79660-158">MFCMAPI uses the **IMAPIContainer::GetSearchCriteria** method to obtain search criteria from a folder to display.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="79660-159">関連項目</span><span class="sxs-lookup"><span data-stu-id="79660-159">See also</span></span>



[<span data-ttu-id="79660-160">IMAPIContainer::SetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="79660-160">IMAPIContainer::SetSearchCriteria</span></span>](imapicontainer-setsearchcriteria.md)
  
[<span data-ttu-id="79660-161">IMAPIFolder::CreateFolder</span><span class="sxs-lookup"><span data-stu-id="79660-161">IMAPIFolder::CreateFolder</span></span>](imapifolder-createfolder.md)
  
[<span data-ttu-id="79660-162">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="79660-162">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="79660-163">PidTagSearch 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="79660-163">PidTagSearch Canonical Property</span></span>](pidtagsearch-canonical-property.md)
  
[<span data-ttu-id="79660-164">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="79660-164">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


<span data-ttu-id="79660-165">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="79660-165">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

