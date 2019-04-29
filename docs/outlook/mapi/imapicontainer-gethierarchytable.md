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
# <a name="imapicontainergethierarchytable"></a><span data-ttu-id="7c748-103">IMAPIContainer::GetHierarchyTable</span><span class="sxs-lookup"><span data-stu-id="7c748-103">IMAPIContainer::GetHierarchyTable</span></span>

  
  
<span data-ttu-id="7c748-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7c748-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7c748-105">コンテナーの階層テーブルへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="7c748-105">Returns a pointer to the container's hierarchy table.</span></span>
  
```cpp
HRESULT GetHierarchyTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="7c748-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7c748-106">Parameters</span></span>

 <span data-ttu-id="7c748-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7c748-107">_ulFlags_</span></span>
  
> <span data-ttu-id="7c748-108">順番テーブルでの情報の返さ方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="7c748-108">[in] A bitmask of flags that controls how information is returned in the table.</span></span> <span data-ttu-id="7c748-109">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="7c748-109">The following flags can be set:</span></span>
    
<span data-ttu-id="7c748-110">CONVENIENT_DEPTH</span><span class="sxs-lookup"><span data-stu-id="7c748-110">CONVENIENT_DEPTH</span></span> 
  
> <span data-ttu-id="7c748-111">階層テーブルに複数のレベルのコンテナーを格納します。</span><span class="sxs-lookup"><span data-stu-id="7c748-111">Fills the hierarchy table with containers from multiple levels.</span></span> <span data-ttu-id="7c748-112">CONVENIENT_DEPTH が設定されていない場合、階層テーブルにはコンテナーの直下の子コンテナーのみが含まれます。</span><span class="sxs-lookup"><span data-stu-id="7c748-112">If CONVENIENT_DEPTH is not set, the hierarchy table contains only the container's immediate child containers.</span></span>
    
<span data-ttu-id="7c748-113">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="7c748-113">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="7c748-114">**GetHierarchyTable**は、呼び出し元がテーブルを使用できるようになる前に、正常に返すことができます。</span><span class="sxs-lookup"><span data-stu-id="7c748-114">**GetHierarchyTable** can return successfully, possibly before the table is made available to the caller.</span></span> <span data-ttu-id="7c748-115">テーブルが使用できない場合は、次のテーブル呼び出しを行うとエラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="7c748-115">If the table is not available, making a subsequent table call can raise an error.</span></span> 
    
<span data-ttu-id="7c748-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7c748-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="7c748-117">文字列データを含む列を Unicode 形式で返すように要求します。</span><span class="sxs-lookup"><span data-stu-id="7c748-117">Requests that the columns that contain string data be returned in Unicode format.</span></span> <span data-ttu-id="7c748-118">MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式で返されます。</span><span class="sxs-lookup"><span data-stu-id="7c748-118">If the MAPI_UNICODE flag is not set, the strings should be returned in ANSI format.</span></span> 
    
<span data-ttu-id="7c748-119">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="7c748-119">SHOW_SOFT_DELETES</span></span>
  
> <span data-ttu-id="7c748-120">現在、削除済みアイテムの保存期間の段階にあるとマークされているアイテムを表示します。</span><span class="sxs-lookup"><span data-stu-id="7c748-120">Shows items that are currently marked as soft deleted—that is, they are in the deleted item retention time phase.</span></span>
    
 <span data-ttu-id="7c748-121">_lpptable_</span><span class="sxs-lookup"><span data-stu-id="7c748-121">_lppTable_</span></span>
  
> <span data-ttu-id="7c748-122">読み上げ階層テーブルへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="7c748-122">[out] A pointer to a pointer to the hierarchy table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7c748-123">戻り値</span><span class="sxs-lookup"><span data-stu-id="7c748-123">Return value</span></span>

<span data-ttu-id="7c748-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="7c748-124">S_OK</span></span> 
  
> <span data-ttu-id="7c748-125">階層テーブルが正常に取得されました。</span><span class="sxs-lookup"><span data-stu-id="7c748-125">The hierarchy table was successfully retrieved.</span></span>
    
<span data-ttu-id="7c748-126">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="7c748-126">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="7c748-127">MAPI_UNICODE フラグが設定されていて、実装が unicode をサポートしていないか、または MAPI_UNICODE が設定されておらず、実装で unicode のみがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="7c748-127">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="7c748-128">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="7c748-128">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="7c748-129">コンテナーは子コンテナーを持たず、階層テーブルを提供できません。</span><span class="sxs-lookup"><span data-stu-id="7c748-129">The container has no child containers and cannot provide a hierarchy table.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7c748-130">注釈</span><span class="sxs-lookup"><span data-stu-id="7c748-130">Remarks</span></span>

<span data-ttu-id="7c748-131">**IMAPIContainer:: GetHierarchyTable**メソッドは、コンテナーの階層テーブルへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="7c748-131">The **IMAPIContainer::GetHierarchyTable** method returns a pointer to the hierarchy table of a container.</span></span> <span data-ttu-id="7c748-132">階層テーブルは、コンテナー内の子コンテナーに関する概要情報を保持します。</span><span class="sxs-lookup"><span data-stu-id="7c748-132">A hierarchy table holds summary information about the child containers in the container.</span></span> <span data-ttu-id="7c748-133">フォルダー階層テーブルは、サブフォルダーに関する情報を保持します。アドレス帳階層テーブルは、子アドレス帳コンテナーおよび配布リストに関する情報を保持します。</span><span class="sxs-lookup"><span data-stu-id="7c748-133">Folder hierarchy tables hold information about subfolders; address book hierarchy tables hold information about child address book containers and distribution lists.</span></span> 
  
<span data-ttu-id="7c748-134">一部のコンテナーに子コンテナーを持たせることはできません。</span><span class="sxs-lookup"><span data-stu-id="7c748-134">It is possible for some containers to have no child containers.</span></span> <span data-ttu-id="7c748-135">これらのコンテナーは、 **GetHierarchyTable**の実装から MAPI_E_NO_SUPPORT を返します。</span><span class="sxs-lookup"><span data-stu-id="7c748-135">These containers return MAPI_E_NO_SUPPORT from their implementations of **GetHierarchyTable**.</span></span>
  
<span data-ttu-id="7c748-136">CONVENIENT_DEPTH フラグが設定されている場合、階層テーブル内の各行には、 **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) プロパティも列として含まれます。</span><span class="sxs-lookup"><span data-stu-id="7c748-136">When the CONVENIENT_DEPTH flag is set, each row in the hierarchy table also includes the **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) property as a column.</span></span> <span data-ttu-id="7c748-137">**PR_DEPTH**は、テーブルを実装するコンテナーを基準とした、各コンテナーのレベルを示します。</span><span class="sxs-lookup"><span data-stu-id="7c748-137">**PR_DEPTH** indicates the level of each container relative to the container that implements the table.</span></span> <span data-ttu-id="7c748-138">実装するコンテナーの直下の子コンテナーは、深さ0、深さが0のコンテナー内の子コンテナーは深さ1というようになります。</span><span class="sxs-lookup"><span data-stu-id="7c748-138">The implementing container's immediate child containers are at depth zero, child containers in the zero depth containers are at depth one, and so on.</span></span> <span data-ttu-id="7c748-139">**PR_DEPTH**の値は、deepens レベルの階層として順番に増加します。</span><span class="sxs-lookup"><span data-stu-id="7c748-139">The values of **PR_DEPTH** increase sequentially as the hierarchy of levels deepens.</span></span> 
  
<span data-ttu-id="7c748-140">階層テーブルで必須および省略可能な列の完全な一覧については、「 [hierarchy tables](hierarchy-tables.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7c748-140">For a complete list of required and optional columns in hierarchy tables, see [Hierarchy Tables](hierarchy-tables.md).</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="7c748-141">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="7c748-141">Notes to implementers</span></span>

<span data-ttu-id="7c748-142">コンテナーの階層テーブルをサポートしている場合は、次の操作も実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7c748-142">If you support a hierarchy table for your container, you must also do the following:</span></span>
  
- <span data-ttu-id="7c748-143">コンテナーの[imapiprop:: openproperty](imapiprop-openproperty.md)メソッドの呼び出しをサポートして、 **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) プロパティを開きます。</span><span class="sxs-lookup"><span data-stu-id="7c748-143">Support a call to the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="7c748-144">コンテナーの[imapiprop:: getproplist](imapiprop-getproplist.md)または[imapiprop:: GetProps](imapiprop-getprops.md)メソッドへの呼び出しから**PR_CONTAINER_HIERARCHY**を返します。</span><span class="sxs-lookup"><span data-stu-id="7c748-144">Return **PR_CONTAINER_HIERARCHY** from a call to the container's [IMAPIProp::GetPropList](imapiprop-getproplist.md) or [IMAPIProp::GetProps](imapiprop-getprops.md) methods.</span></span> 
    
## <a name="notes-to-callers"></a><span data-ttu-id="7c748-145">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="7c748-145">Notes to callers</span></span>

<span data-ttu-id="7c748-146">文字列およびバイナリコンテンツの表の列を切り捨てられます。</span><span class="sxs-lookup"><span data-stu-id="7c748-146">String and binary contents table columns can be truncated.</span></span> <span data-ttu-id="7c748-147">通常、プロバイダーは255文字を返します。</span><span class="sxs-lookup"><span data-stu-id="7c748-147">Typically, providers return 255 characters.</span></span> <span data-ttu-id="7c748-148">テーブルに切り捨てられた列が含まれているかどうかを事前に知ることはできないため、列の長さが255または510バイトの場合は、列が切り捨てられていると仮定します。</span><span class="sxs-lookup"><span data-stu-id="7c748-148">Because you cannot know beforehand whether a table includes truncated columns, assume that a column is truncated if the length of the column is either 255 or 510 bytes.</span></span> <span data-ttu-id="7c748-149">必要に応じて、エントリ id を使用して、切り捨てられた列の完全な値をオブジェクトから直接取得して、 [imapiprop:: GetProps](imapiprop-getprops.md)メソッドを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="7c748-149">You can always retrieve the full value of a truncated column, if necessary, directly from the object by using its entry identifier to open it and then calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
  
<span data-ttu-id="7c748-150">プロバイダーの実装に応じて、制限および並べ替え操作は、文字列全体またはその文字列の切り捨てられたバージョンに適用できます。</span><span class="sxs-lookup"><span data-stu-id="7c748-150">Depending on the provider's implementation, restrictions and sorting operations can apply to the whole string or to the truncated version of that string.</span></span> <span data-ttu-id="7c748-151">さらに、ストアプロバイダーは、階層テーブルに指定されたソート順序セット[ssortorderset](ssortorderset.md)を優先することは保証されません。</span><span class="sxs-lookup"><span data-stu-id="7c748-151">Moreover, store providers are not guaranteed to honor the sort order set [SSortOrderSet](ssortorderset.md) specified for hierarchy tables.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="7c748-152">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="7c748-152">MFCMAPI reference</span></span>

<span data-ttu-id="7c748-153">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7c748-153">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="7c748-154">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="7c748-154">**File**</span></span>|<span data-ttu-id="7c748-155">**関数**</span><span class="sxs-lookup"><span data-stu-id="7c748-155">**Function**</span></span>|<span data-ttu-id="7c748-156">**コメント**</span><span class="sxs-lookup"><span data-stu-id="7c748-156">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7c748-157">HierarchyTableTreeCtrl</span><span class="sxs-lookup"><span data-stu-id="7c748-157">HierarchyTableTreeCtrl.cpp</span></span>  <br/> |<span data-ttu-id="7c748-158">CHierarchyTableTreeCtrl:: GetHierarchyTable</span><span class="sxs-lookup"><span data-stu-id="7c748-158">CHierarchyTableTreeCtrl::GetHierarchyTable</span></span>  <br/> |<span data-ttu-id="7c748-159">CHierarchyTableTreeCtrl クラスは、 **GetHierarchyTable**を使用して、ツリービューコントロールに表示する階層テーブルを取得します。</span><span class="sxs-lookup"><span data-stu-id="7c748-159">The CHierarchyTableTreeCtrl class uses **GetHierarchyTable** to obtain hierarchy tables to display in a tree view control.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7c748-160">関連項目</span><span class="sxs-lookup"><span data-stu-id="7c748-160">See also</span></span>



[<span data-ttu-id="7c748-161">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="7c748-161">IMAPIProp::GetPropList</span></span>](imapiprop-getproplist.md)
  
[<span data-ttu-id="7c748-162">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="7c748-162">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="7c748-163">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7c748-163">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="7c748-164">PidTagContainerHierarchy 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="7c748-164">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="7c748-165">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="7c748-165">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


<span data-ttu-id="7c748-166">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="7c748-166">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

