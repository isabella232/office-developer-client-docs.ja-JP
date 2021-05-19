---
title: IMAPIContainerGetHierarchyTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer.GetHierarchyTable
api_type:
- COM
ms.assetid: d0c54092-86a3-47e0-8133-72e119e74b65
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: efc7f7a2fa703004afe361d766e0209ba40ffe46
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426199"
---
# <a name="imapicontainergethierarchytable"></a><span data-ttu-id="d2d88-103">IMAPIContainer::GetHierarchyTable</span><span class="sxs-lookup"><span data-stu-id="d2d88-103">IMAPIContainer::GetHierarchyTable</span></span>

  
  
<span data-ttu-id="d2d88-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d2d88-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d2d88-105">コンテナーの階層テーブルへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="d2d88-105">Returns a pointer to the container's hierarchy table.</span></span>
  
```cpp
HRESULT GetHierarchyTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="d2d88-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d2d88-106">Parameters</span></span>

 <span data-ttu-id="d2d88-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d2d88-107">_ulFlags_</span></span>
  
> <span data-ttu-id="d2d88-108">[in]テーブルで情報を返す方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="d2d88-108">[in] A bitmask of flags that controls how information is returned in the table.</span></span> <span data-ttu-id="d2d88-109">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="d2d88-109">The following flags can be set:</span></span>
    
<span data-ttu-id="d2d88-110">CONVENIENT_DEPTH</span><span class="sxs-lookup"><span data-stu-id="d2d88-110">CONVENIENT_DEPTH</span></span> 
  
> <span data-ttu-id="d2d88-111">階層テーブルに複数のレベルのコンテナーを入力します。</span><span class="sxs-lookup"><span data-stu-id="d2d88-111">Fills the hierarchy table with containers from multiple levels.</span></span> <span data-ttu-id="d2d88-112">このCONVENIENT_DEPTH設定されていない場合、階層テーブルにはコンテナーの直接の子コンテナーだけが含まれます。</span><span class="sxs-lookup"><span data-stu-id="d2d88-112">If CONVENIENT_DEPTH is not set, the hierarchy table contains only the container's immediate child containers.</span></span>
    
<span data-ttu-id="d2d88-113">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="d2d88-113">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="d2d88-114">**GetHierarchyTable は** 、呼び出し元がテーブルを使用できる前に、正常に返すことができます。</span><span class="sxs-lookup"><span data-stu-id="d2d88-114">**GetHierarchyTable** can return successfully, possibly before the table is made available to the caller.</span></span> <span data-ttu-id="d2d88-115">テーブルが使用できない場合は、後続のテーブル呼び出しでエラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="d2d88-115">If the table is not available, making a subsequent table call can raise an error.</span></span> 
    
<span data-ttu-id="d2d88-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d2d88-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="d2d88-117">文字列データを含む列を Unicode 形式で返す要求。</span><span class="sxs-lookup"><span data-stu-id="d2d88-117">Requests that the columns that contain string data be returned in Unicode format.</span></span> <span data-ttu-id="d2d88-118">このフラグMAPI_UNICODE設定しない場合は、文字列を ANSI 形式で返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="d2d88-118">If the MAPI_UNICODE flag is not set, the strings should be returned in ANSI format.</span></span> 
    
<span data-ttu-id="d2d88-119">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="d2d88-119">SHOW_SOFT_DELETES</span></span>
  
> <span data-ttu-id="d2d88-120">現在、削除済みアイテムとしてマークされているアイテム、つまり削除済みアイテムの保持時間フェーズにあるアイテムを表示します。</span><span class="sxs-lookup"><span data-stu-id="d2d88-120">Shows items that are currently marked as soft deleted—that is, they are in the deleted item retention time phase.</span></span>
    
 <span data-ttu-id="d2d88-121">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="d2d88-121">_lppTable_</span></span>
  
> <span data-ttu-id="d2d88-122">[out]階層テーブルへのポインターを指すポインター。</span><span class="sxs-lookup"><span data-stu-id="d2d88-122">[out] A pointer to a pointer to the hierarchy table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d2d88-123">戻り値</span><span class="sxs-lookup"><span data-stu-id="d2d88-123">Return value</span></span>

<span data-ttu-id="d2d88-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="d2d88-124">S_OK</span></span> 
  
> <span data-ttu-id="d2d88-125">階層テーブルが正常に取得されました。</span><span class="sxs-lookup"><span data-stu-id="d2d88-125">The hierarchy table was successfully retrieved.</span></span>
    
<span data-ttu-id="d2d88-126">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="d2d88-126">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="d2d88-127">このフラグMAPI_UNICODE設定され、実装が Unicode をサポートしていないか、または設定されていないMAPI_UNICODE実装が Unicode のみをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="d2d88-127">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="d2d88-128">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="d2d88-128">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="d2d88-129">コンテナーには子コンテナーが含まれていますが、階層テーブルを指定することはできません。</span><span class="sxs-lookup"><span data-stu-id="d2d88-129">The container has no child containers and cannot provide a hierarchy table.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d2d88-130">注釈</span><span class="sxs-lookup"><span data-stu-id="d2d88-130">Remarks</span></span>

<span data-ttu-id="d2d88-131">**IMAPIContainer::GetHierarchyTable** メソッドは、コンテナーの階層テーブルへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="d2d88-131">The **IMAPIContainer::GetHierarchyTable** method returns a pointer to the hierarchy table of a container.</span></span> <span data-ttu-id="d2d88-132">階層テーブルには、コンテナー内の子コンテナーに関する概要情報が格納されます。</span><span class="sxs-lookup"><span data-stu-id="d2d88-132">A hierarchy table holds summary information about the child containers in the container.</span></span> <span data-ttu-id="d2d88-133">フォルダー階層テーブルには、サブフォルダーに関する情報が格納されます。アドレス帳階層テーブルには、子アドレス帳コンテナーと配布リストに関する情報が格納されます。</span><span class="sxs-lookup"><span data-stu-id="d2d88-133">Folder hierarchy tables hold information about subfolders; address book hierarchy tables hold information about child address book containers and distribution lists.</span></span> 
  
<span data-ttu-id="d2d88-134">一部のコンテナーに子コンテナーがない場合があります。</span><span class="sxs-lookup"><span data-stu-id="d2d88-134">It is possible for some containers to have no child containers.</span></span> <span data-ttu-id="d2d88-135">これらのコンテナーは **、getHierarchyTable** MAPI_E_NO_SUPPORT実装からデータを返します。</span><span class="sxs-lookup"><span data-stu-id="d2d88-135">These containers return MAPI_E_NO_SUPPORT from their implementations of **GetHierarchyTable**.</span></span>
  
<span data-ttu-id="d2d88-136">このフラグCONVENIENT_DEPTH設定すると、階層テーブルの各行には、PR_DEPTH **(** [PidTagDepth](pidtagdepth-canonical-property.md)) プロパティも列として含まれます。</span><span class="sxs-lookup"><span data-stu-id="d2d88-136">When the CONVENIENT_DEPTH flag is set, each row in the hierarchy table also includes the **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) property as a column.</span></span> <span data-ttu-id="d2d88-137">**PR_DEPTH** は、テーブルを実装するコンテナーに対する各コンテナーのレベルを示します。</span><span class="sxs-lookup"><span data-stu-id="d2d88-137">**PR_DEPTH** indicates the level of each container relative to the container that implements the table.</span></span> <span data-ttu-id="d2d88-138">実装するコンテナーの直接の子コンテナーは深度 0、深度 0 のコンテナーの子コンテナーは深度 1 などです。</span><span class="sxs-lookup"><span data-stu-id="d2d88-138">The implementing container's immediate child containers are at depth zero, child containers in the zero depth containers are at depth one, and so on.</span></span> <span data-ttu-id="d2d88-139">レベルの階層 **が深PR_DEPTH、** 値は順次増加します。</span><span class="sxs-lookup"><span data-stu-id="d2d88-139">The values of **PR_DEPTH** increase sequentially as the hierarchy of levels deepens.</span></span> 
  
<span data-ttu-id="d2d88-140">階層テーブルの必須列とオプション列の完全な一覧については、「階層テーブル」 [を参照してください](hierarchy-tables.md)。</span><span class="sxs-lookup"><span data-stu-id="d2d88-140">For a complete list of required and optional columns in hierarchy tables, see [Hierarchy Tables](hierarchy-tables.md).</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="d2d88-141">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="d2d88-141">Notes to implementers</span></span>

<span data-ttu-id="d2d88-142">コンテナーの階層テーブルをサポートする場合は、次の操作も行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="d2d88-142">If you support a hierarchy table for your container, you must also do the following:</span></span>
  
- <span data-ttu-id="d2d88-143">コンテナーの [IMAPIProp::OpenProperty](imapiprop-openproperty.md) メソッドの呼び出しをサポートして **、PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) プロパティを開きます。</span><span class="sxs-lookup"><span data-stu-id="d2d88-143">Support a call to the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="d2d88-144">コンテナー **PR_CONTAINER_HIERARCHY** [IMAPIProp::GetPropList](imapiprop-getproplist.md) または [IMAPIProp::GetProps](imapiprop-getprops.md) メソッドへの呼び出しから返します。</span><span class="sxs-lookup"><span data-stu-id="d2d88-144">Return **PR_CONTAINER_HIERARCHY** from a call to the container's [IMAPIProp::GetPropList](imapiprop-getproplist.md) or [IMAPIProp::GetProps](imapiprop-getprops.md) methods.</span></span> 
    
## <a name="notes-to-callers"></a><span data-ttu-id="d2d88-145">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="d2d88-145">Notes to callers</span></span>

<span data-ttu-id="d2d88-146">文字列およびバイナリコンテンツテーブルの列は切り捨て可能です。</span><span class="sxs-lookup"><span data-stu-id="d2d88-146">String and binary contents table columns can be truncated.</span></span> <span data-ttu-id="d2d88-147">通常、プロバイダーは 255 文字を返します。</span><span class="sxs-lookup"><span data-stu-id="d2d88-147">Typically, providers return 255 characters.</span></span> <span data-ttu-id="d2d88-148">テーブルに切り捨てられた列が含まれるかどうかは事前に分からないので、列の長さが 255 バイトまたは 510 バイトの場合は、列が切り捨てられると仮定します。</span><span class="sxs-lookup"><span data-stu-id="d2d88-148">Because you cannot know beforehand whether a table includes truncated columns, assume that a column is truncated if the length of the column is either 255 or 510 bytes.</span></span> <span data-ttu-id="d2d88-149">必要に応じて、切り捨てられた列の完全な値をオブジェクトから直接取得するには、そのエントリ識別子を使用して開き [、IMAPIProp::GetProps](imapiprop-getprops.md) メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d2d88-149">You can always retrieve the full value of a truncated column, if necessary, directly from the object by using its entry identifier to open it and then calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
  
<span data-ttu-id="d2d88-150">プロバイダーの実装に応じて、制限と並べ替え操作は、文字列全体またはその文字列の切り捨てられたバージョンに適用できます。</span><span class="sxs-lookup"><span data-stu-id="d2d88-150">Depending on the provider's implementation, restrictions and sorting operations can apply to the whole string or to the truncated version of that string.</span></span> <span data-ttu-id="d2d88-151">さらに、ストア プロバイダーは、階層テーブルに指定された並べ替え順序セット [SSortOrderSet を](ssortorderset.md) 受け入れ保証されません。</span><span class="sxs-lookup"><span data-stu-id="d2d88-151">Moreover, store providers are not guaranteed to honor the sort order set [SSortOrderSet](ssortorderset.md) specified for hierarchy tables.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="d2d88-152">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="d2d88-152">MFCMAPI reference</span></span>

<span data-ttu-id="d2d88-153">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d2d88-153">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d2d88-154">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="d2d88-154">**File**</span></span>|<span data-ttu-id="d2d88-155">**関数**</span><span class="sxs-lookup"><span data-stu-id="d2d88-155">**Function**</span></span>|<span data-ttu-id="d2d88-156">**コメント**</span><span class="sxs-lookup"><span data-stu-id="d2d88-156">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d2d88-157">HierarchyTableTreeCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="d2d88-157">HierarchyTableTreeCtrl.cpp</span></span>  <br/> |<span data-ttu-id="d2d88-158">CHierarchyTableTreeCtrl::GetHierarchyTable</span><span class="sxs-lookup"><span data-stu-id="d2d88-158">CHierarchyTableTreeCtrl::GetHierarchyTable</span></span>  <br/> |<span data-ttu-id="d2d88-159">CHierarchyTableTreeCtrl クラスは **GetHierarchyTable** を使用して、ツリー ビュー コントロールに表示する階層テーブルを取得します。</span><span class="sxs-lookup"><span data-stu-id="d2d88-159">The CHierarchyTableTreeCtrl class uses **GetHierarchyTable** to obtain hierarchy tables to display in a tree view control.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d2d88-160">関連項目</span><span class="sxs-lookup"><span data-stu-id="d2d88-160">See also</span></span>



[<span data-ttu-id="d2d88-161">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="d2d88-161">IMAPIProp::GetPropList</span></span>](imapiprop-getproplist.md)
  
[<span data-ttu-id="d2d88-162">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="d2d88-162">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="d2d88-163">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d2d88-163">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="d2d88-164">PidTagContainerHierarchy 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d2d88-164">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="d2d88-165">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="d2d88-165">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


<span data-ttu-id="d2d88-166">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="d2d88-166">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

