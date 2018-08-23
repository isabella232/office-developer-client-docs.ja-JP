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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 4ca565f97851a2efe2f3279f062f6ea89a4c6326
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579964"
---
# <a name="imapicontainergetsearchcriteria"></a><span data-ttu-id="5ffe1-103">IMAPIContainer::GetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="5ffe1-103">IMAPIContainer::GetSearchCriteria</span></span>

  
  
<span data-ttu-id="5ffe1-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5ffe1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5ffe1-105">コンテナーの検索条件を取得します。</span><span class="sxs-lookup"><span data-stu-id="5ffe1-105">Obtains the search criteria for the container.</span></span>
  
```cpp
HRESULT GetSearchCriteria(
  ULONG ulFlags,
  LPSRestriction FAR * lppRestriction,
  LPENTRYLIST FAR * lppContainerList,
  ULONG FAR * lpulSearchState
);
```

## <a name="parameters"></a><span data-ttu-id="5ffe1-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="5ffe1-106">Parameters</span></span>

 <span data-ttu-id="5ffe1-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5ffe1-107">_ulFlags_</span></span>
  
> <span data-ttu-id="5ffe1-108">[in]渡された文字列の種類を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="5ffe1-108">[in] A bitmask of flags that controls the type of the passed-in strings.</span></span> <span data-ttu-id="5ffe1-109">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="5ffe1-109">The following flag can be set:</span></span>
    
<span data-ttu-id="5ffe1-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5ffe1-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="5ffe1-111">渡された文字列は、Unicode 形式では。</span><span class="sxs-lookup"><span data-stu-id="5ffe1-111">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="5ffe1-112">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。</span><span class="sxs-lookup"><span data-stu-id="5ffe1-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="5ffe1-113">_lppRestriction_</span><span class="sxs-lookup"><span data-stu-id="5ffe1-113">_lppRestriction_</span></span>
  
> <span data-ttu-id="5ffe1-114">[out]検索条件を定義する[SRestriction](srestriction.md)構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="5ffe1-114">[out] A pointer to a pointer to an [SRestriction](srestriction.md) structure that defines the search criteria.</span></span> <span data-ttu-id="5ffe1-115">クライアント アプリケーションは、 _lppRestriction_パラメーターに NULL を渡す、 **GetSearchCriteria**は**SRestriction**構造体を返しません。</span><span class="sxs-lookup"><span data-stu-id="5ffe1-115">If a client application passes NULL in the  _lppRestriction_ parameter, **GetSearchCriteria** does not return an **SRestriction** structure.</span></span> 
    
 <span data-ttu-id="5ffe1-116">_lppContainerList_</span><span class="sxs-lookup"><span data-stu-id="5ffe1-116">_lppContainerList_</span></span>
  
> <span data-ttu-id="5ffe1-117">[out]検索に含まれるコンテナーを表すエントリの識別子の配列へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="5ffe1-117">[out] A pointer to a pointer to an array of entry identifiers that represent containers to be included in the search.</span></span> <span data-ttu-id="5ffe1-118">クライアントは、 _lppContainerList_パラメーターに NULL を渡す、 **GetSearchCriteria**はエントリの識別子の配列を返しません。</span><span class="sxs-lookup"><span data-stu-id="5ffe1-118">If a client passes NULL in the  _lppContainerList_ parameter, **GetSearchCriteria** does not return an array of entry identifiers.</span></span> 
    
 <span data-ttu-id="5ffe1-119">_lpulSearchState_</span><span class="sxs-lookup"><span data-stu-id="5ffe1-119">_lpulSearchState_</span></span>
  
> <span data-ttu-id="5ffe1-120">[out]検索の現在の状態を示すために使用されるフラグのビットマスクへのポインター。</span><span class="sxs-lookup"><span data-stu-id="5ffe1-120">[out] A pointer to a bitmask of flags used to indicate the current state of the search.</span></span> <span data-ttu-id="5ffe1-121">場合は、クライアントでは、 _lpulSearchState_パラメーターに NULL を渡す、 **GetSearchCriteria**フラグを返しますありません。</span><span class="sxs-lookup"><span data-stu-id="5ffe1-121">If a client passes NULL in the  _lpulSearchState_ parameter, **GetSearchCriteria** returns no flags.</span></span> <span data-ttu-id="5ffe1-122">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="5ffe1-122">The following flags can be set:</span></span> 
    
<span data-ttu-id="5ffe1-123">SEARCH_FOREGROUND</span><span class="sxs-lookup"><span data-stu-id="5ffe1-123">SEARCH_FOREGROUND</span></span> 
  
> <span data-ttu-id="5ffe1-124">検索は、他の検索基準とした優先度の高いで実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5ffe1-124">The search should run at high priority relative to other searches.</span></span> <span data-ttu-id="5ffe1-125">このフラグが設定されていない場合は、他の検索基準にして通常の優先順位で検索が実行されます。</span><span class="sxs-lookup"><span data-stu-id="5ffe1-125">If this flag is not set, the search runs at normal priority relative to other searches.</span></span>
    
<span data-ttu-id="5ffe1-126">SEARCH_REBUILD</span><span class="sxs-lookup"><span data-stu-id="5ffe1-126">SEARCH_REBUILD</span></span> 
  
> <span data-ttu-id="5ffe1-127">検索では、CPU を消費するのモードでの操作は、条件に一致するメッセージを検索しようとしています。</span><span class="sxs-lookup"><span data-stu-id="5ffe1-127">The search is in the CPU-intensive mode of its operation, trying to locate messages that match the criteria.</span></span> <span data-ttu-id="5ffe1-128">このフラグが設定されていない場合、CPU を消費するで検索の操作は上です。</span><span class="sxs-lookup"><span data-stu-id="5ffe1-128">If this flag is not set, the CPU-intensive part of the search's operation is over.</span></span> <span data-ttu-id="5ffe1-129">このフラグは、意味、検索がアクティブな場合にのみ (つまり、SEARCH_RUNNING フラグが設定されます) 場合。</span><span class="sxs-lookup"><span data-stu-id="5ffe1-129">This flag has meaning only if the search is active (that is, if the SEARCH_RUNNING flag is set).</span></span>
    
<span data-ttu-id="5ffe1-130">SEARCH_RECURSIVE</span><span class="sxs-lookup"><span data-stu-id="5ffe1-130">SEARCH_RECURSIVE</span></span> 
  
> <span data-ttu-id="5ffe1-131">検索は、指定されたコンテナーとそのすべての子コンテナーのエントリに一致する予定です。</span><span class="sxs-lookup"><span data-stu-id="5ffe1-131">The search is looking in specified containers and all their child containers for matching entries.</span></span> <span data-ttu-id="5ffe1-132">このフラグが設定されていない場合、 [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md)メソッドの最後の呼び出しで明示的に含まれているコンテナーだけを検索対象がします。</span><span class="sxs-lookup"><span data-stu-id="5ffe1-132">If this flag is not set, only the containers explicitly included in the last call to the [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method are being searched.</span></span> 
    
<span data-ttu-id="5ffe1-133">SEARCH_RUNNING</span><span class="sxs-lookup"><span data-stu-id="5ffe1-133">SEARCH_RUNNING</span></span> 
  
> <span data-ttu-id="5ffe1-134">検索はアクティブで、メッセージ ・ ストア内の変更を反映または、アドレス帳コンテナーの内容のテーブルが更新されています。</span><span class="sxs-lookup"><span data-stu-id="5ffe1-134">The search is active and the container's contents table is being updated to reflect changes in the message store or address book.</span></span> <span data-ttu-id="5ffe1-135">このフラグが設定されていない場合、検索はアクティブではなく、内容のテーブルでは、静的です。</span><span class="sxs-lookup"><span data-stu-id="5ffe1-135">If this flag is not set, the search is inactive and the contents table is static.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5ffe1-136">�߂�l</span><span class="sxs-lookup"><span data-stu-id="5ffe1-136">Return value</span></span>

<span data-ttu-id="5ffe1-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="5ffe1-137">S_OK</span></span> 
  
> <span data-ttu-id="5ffe1-138">検索条件が正常に取得しました。</span><span class="sxs-lookup"><span data-stu-id="5ffe1-138">The search criteria was successfully obtained.</span></span>
    
<span data-ttu-id="5ffe1-139">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="5ffe1-139">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="5ffe1-140">か、MAPI_UNICODE フラグが設定された実装は Unicode をサポートしていないまたは MAPI_UNICODE が設定されていませんでしたし、実装は、Unicode だけをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="5ffe1-140">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="5ffe1-141">MAPI_E_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="5ffe1-141">MAPI_E_NOT_INITIALIZED</span></span> 
  
> <span data-ttu-id="5ffe1-142">コンテナーには、検索条件は確立されたことはありません。</span><span class="sxs-lookup"><span data-stu-id="5ffe1-142">Search criteria were never established for the container.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5ffe1-143">注釈</span><span class="sxs-lookup"><span data-stu-id="5ffe1-143">Remarks</span></span>

<span data-ttu-id="5ffe1-144">**IMAPIContainer::GetSearchCriteria**メソッドは、通常の検索結果フォルダーの検索をサポートするコンテナーの検索条件を取得します。</span><span class="sxs-lookup"><span data-stu-id="5ffe1-144">The **IMAPIContainer::GetSearchCriteria** method obtains the search criteria for a container that supports searches, typically a search-results folder.</span></span> <span data-ttu-id="5ffe1-145">検索条件を作成するには、コンテナーの**IMAPIContainer::SetSearchCriteria**メソッドを呼び出すとします。</span><span class="sxs-lookup"><span data-stu-id="5ffe1-145">You create search criteria by calling a container's **IMAPIContainer::SetSearchCriteria** method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="5ffe1-146">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="5ffe1-146">Notes to implementers</span></span>

<span data-ttu-id="5ffe1-147">アドレス帳コンテナーは、 **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) のプロパティに関連付けられている高度な検索機能を提供する場合にのみ、 **GetSearchCriteria**をサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5ffe1-147">Address book containers may need to support **GetSearchCriteria** only if they provide the advanced search capabilities associated with the **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) property.</span></span> <span data-ttu-id="5ffe1-148">アドレス帳コンテナーの高度な検索機能を実装する方法の詳細については、[高度な検索を実装する](implementing-advanced-searching.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5ffe1-148">For more information about how to implement the advanced search feature for address book containers, see [Implementing Advanced Searching](implementing-advanced-searching.md).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="5ffe1-149">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="5ffe1-149">Notes to callers</span></span>

<span data-ttu-id="5ffe1-150">完了したら、 _lppRestriction_および_lppContainerList_パラメーターが指すデータ構造体を持つ、 [MAPIFreeBuffer](mapifreebuffer.md) 1 回の各構造体を解放するを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="5ffe1-150">When you are finished with the data structures pointed to by the  _lppRestriction_ and  _lppContainerList_ parameters, call [MAPIFreeBuffer](mapifreebuffer.md) once for each structure to be released.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="5ffe1-151">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="5ffe1-151">MFCMAPI reference</span></span>

<span data-ttu-id="5ffe1-152">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="5ffe1-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="5ffe1-153">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="5ffe1-153">**File**</span></span>|<span data-ttu-id="5ffe1-154">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="5ffe1-154">**Function**</span></span>|<span data-ttu-id="5ffe1-155">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="5ffe1-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5ffe1-156">HierarchyTableDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="5ffe1-156">HierarchyTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="5ffe1-157">CHierarchyTableDlg::OnEditSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="5ffe1-157">CHierarchyTableDlg::OnEditSearchCriteria</span></span>  <br/> |<span data-ttu-id="5ffe1-158">MFCMAPI では、 **IMAPIContainer::GetSearchCriteria**メソッドを使用して表示するためのフォルダーから検索条件を取得します。</span><span class="sxs-lookup"><span data-stu-id="5ffe1-158">MFCMAPI uses the **IMAPIContainer::GetSearchCriteria** method to obtain search criteria from a folder to display.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5ffe1-159">関連項目</span><span class="sxs-lookup"><span data-stu-id="5ffe1-159">See also</span></span>



[<span data-ttu-id="5ffe1-160">IMAPIContainer::SetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="5ffe1-160">IMAPIContainer::SetSearchCriteria</span></span>](imapicontainer-setsearchcriteria.md)
  
[<span data-ttu-id="5ffe1-161">IMAPIFolder::CreateFolder</span><span class="sxs-lookup"><span data-stu-id="5ffe1-161">IMAPIFolder::CreateFolder</span></span>](imapifolder-createfolder.md)
  
[<span data-ttu-id="5ffe1-162">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="5ffe1-162">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="5ffe1-163">PidTagSearch 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5ffe1-163">PidTagSearch Canonical Property</span></span>](pidtagsearch-canonical-property.md)
  
[<span data-ttu-id="5ffe1-164">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="5ffe1-164">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


<span data-ttu-id="5ffe1-165">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="5ffe1-165">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

