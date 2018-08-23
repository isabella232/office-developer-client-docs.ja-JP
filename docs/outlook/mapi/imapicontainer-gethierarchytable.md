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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b30c6e9840ed5dddfd2d3a5f149a3f0f6e8da605
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800474"
---
# <a name="imapicontainergethierarchytable"></a><span data-ttu-id="53f4f-103">IMAPIContainer::GetHierarchyTable</span><span class="sxs-lookup"><span data-stu-id="53f4f-103">IMAPIContainer::GetHierarchyTable</span></span>

  
  
<span data-ttu-id="53f4f-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="53f4f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="53f4f-105">コンテナーの階層構造のテーブルへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="53f4f-105">Returns a pointer to the container's hierarchy table.</span></span>
  
```cpp
HRESULT GetHierarchyTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="53f4f-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="53f4f-106">Parameters</span></span>

 <span data-ttu-id="53f4f-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="53f4f-107">_ulFlags_</span></span>
  
> <span data-ttu-id="53f4f-108">[in]テーブルの情報を返す方法を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="53f4f-108">[in] A bitmask of flags that controls how information is returned in the table.</span></span> <span data-ttu-id="53f4f-109">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="53f4f-109">The following flags can be set:</span></span>
    
<span data-ttu-id="53f4f-110">CONVENIENT_DEPTH</span><span class="sxs-lookup"><span data-stu-id="53f4f-110">CONVENIENT_DEPTH</span></span> 
  
> <span data-ttu-id="53f4f-111">コンテナーが複数のレベルから階層テーブルに格納します。</span><span class="sxs-lookup"><span data-stu-id="53f4f-111">Fills the hierarchy table with containers from multiple levels.</span></span> <span data-ttu-id="53f4f-112">CONVENIENT_DEPTH が設定されていない場合、階層テーブルには、コンテナーの直下の子のコンテナーだけが含まれています。</span><span class="sxs-lookup"><span data-stu-id="53f4f-112">If CONVENIENT_DEPTH is not set, the hierarchy table contains only the container's immediate child containers.</span></span>
    
<span data-ttu-id="53f4f-113">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="53f4f-113">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="53f4f-114">**GetHierarchyTable**が正常に完了可能性があります前にテーブルが使用可能な呼び出し元にします。</span><span class="sxs-lookup"><span data-stu-id="53f4f-114">**GetHierarchyTable** can return successfully, possibly before the table is made available to the caller.</span></span> <span data-ttu-id="53f4f-115">テーブルが使用できない場合は、テーブルのそれ以降の呼び出しを行うとエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="53f4f-115">If the table is not available, making a subsequent table call can raise an error.</span></span> 
    
<span data-ttu-id="53f4f-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="53f4f-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="53f4f-117">Unicode 形式で文字列データを含む列が返されるように要求します。</span><span class="sxs-lookup"><span data-stu-id="53f4f-117">Requests that the columns that contain string data be returned in Unicode format.</span></span> <span data-ttu-id="53f4f-118">MAPI_UNICODE フラグが設定されていない場合、文字列が ANSI 形式で返されます。</span><span class="sxs-lookup"><span data-stu-id="53f4f-118">If the MAPI_UNICODE flag is not set, the strings should be returned in ANSI format.</span></span> 
    
<span data-ttu-id="53f4f-119">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="53f4f-119">SHOW_SOFT_DELETES</span></span>
  
> <span data-ttu-id="53f4f-120">ソフトとしてマークされているアイテムの削除を示しています-は削除済みアイテムの保存に時間の段階です。</span><span class="sxs-lookup"><span data-stu-id="53f4f-120">Shows items that are currently marked as soft deleted—that is, they are in the deleted item retention time phase.</span></span>
    
 <span data-ttu-id="53f4f-121">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="53f4f-121">_lppTable_</span></span>
  
> <span data-ttu-id="53f4f-122">[out]階層テーブルへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="53f4f-122">[out] A pointer to a pointer to the hierarchy table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="53f4f-123">�߂�l</span><span class="sxs-lookup"><span data-stu-id="53f4f-123">Return value</span></span>

<span data-ttu-id="53f4f-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="53f4f-124">S_OK</span></span> 
  
> <span data-ttu-id="53f4f-125">階層テーブルが正常に取得しました。</span><span class="sxs-lookup"><span data-stu-id="53f4f-125">The hierarchy table was successfully retrieved.</span></span>
    
<span data-ttu-id="53f4f-126">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="53f4f-126">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="53f4f-127">か、MAPI_UNICODE フラグが設定された実装は Unicode をサポートしていないまたは MAPI_UNICODE が設定されていませんでしたし、実装は、Unicode だけをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="53f4f-127">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="53f4f-128">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="53f4f-128">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="53f4f-129">コンテナーは、子コンテナーがないと、階層テーブルを提供することはできません。</span><span class="sxs-lookup"><span data-stu-id="53f4f-129">The container has no child containers and cannot provide a hierarchy table.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="53f4f-130">注釈</span><span class="sxs-lookup"><span data-stu-id="53f4f-130">Remarks</span></span>

<span data-ttu-id="53f4f-131">**IMAPIContainer::GetHierarchyTable**メソッドは、コンテナーの階層テーブルにポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="53f4f-131">The **IMAPIContainer::GetHierarchyTable** method returns a pointer to the hierarchy table of a container.</span></span> <span data-ttu-id="53f4f-132">階層テーブルは、コンテナー内の子コンテナーに関する要約情報を保持します。</span><span class="sxs-lookup"><span data-stu-id="53f4f-132">A hierarchy table holds summary information about the child containers in the container.</span></span> <span data-ttu-id="53f4f-133">フォルダーの階層テーブルには、サブフォルダーの情報を保持します。アドレス帳階層テーブルは、アドレス帳コンテナーや配布リストに子に関する情報を保持します。</span><span class="sxs-lookup"><span data-stu-id="53f4f-133">Folder hierarchy tables hold information about subfolders; address book hierarchy tables hold information about child address book containers and distribution lists.</span></span> 
  
<span data-ttu-id="53f4f-134">いくつかのコンテナーに子コンテナーがないことができます。</span><span class="sxs-lookup"><span data-stu-id="53f4f-134">It is possible for some containers to have no child containers.</span></span> <span data-ttu-id="53f4f-135">これらのコンテナーでは、 **GetHierarchyTable**の実装から MAPI_E_NO_SUPPORT を返します。</span><span class="sxs-lookup"><span data-stu-id="53f4f-135">These containers return MAPI_E_NO_SUPPORT from their implementations of **GetHierarchyTable**.</span></span>
  
<span data-ttu-id="53f4f-136">CONVENIENT_DEPTH フラグを設定すると、階層テーブル内の各行にはにより、その列としても**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) のプロパティが含まれます。</span><span class="sxs-lookup"><span data-stu-id="53f4f-136">When the CONVENIENT_DEPTH flag is set, each row in the hierarchy table also includes the **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) property as a column.</span></span> <span data-ttu-id="53f4f-137">**PR_DEPTH**は、テーブルを実装するコンテナーを基準にして、各コンテナーのレベルを示します。</span><span class="sxs-lookup"><span data-stu-id="53f4f-137">**PR_DEPTH** indicates the level of each container relative to the container that implements the table.</span></span> <span data-ttu-id="53f4f-138">深さが 1 というように実装するコンテナーの直下の子コンテナーは、0、0 の深さのコンテナー内の子コンテナーの深さがあります。</span><span class="sxs-lookup"><span data-stu-id="53f4f-138">The implementing container's immediate child containers are at depth zero, child containers in the zero depth containers are at depth one, and so on.</span></span> <span data-ttu-id="53f4f-139">レベルの階層を深めるよう、 **PR_DEPTH**の値は順番に増加します。</span><span class="sxs-lookup"><span data-stu-id="53f4f-139">The values of **PR_DEPTH** increase sequentially as the hierarchy of levels deepens.</span></span> 
  
<span data-ttu-id="53f4f-140">階層テーブル内の必須および省略可能な列の一覧については、[階層テーブル](hierarchy-tables.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="53f4f-140">For a complete list of required and optional columns in hierarchy tables, see [Hierarchy Tables](hierarchy-tables.md).</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="53f4f-141">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="53f4f-141">Notes to implementers</span></span>

<span data-ttu-id="53f4f-142">コンテナーの階層テーブルをサポートする場合も、次の行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="53f4f-142">If you support a hierarchy table for your container, you must also do the following:</span></span>
  
- <span data-ttu-id="53f4f-143">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) のプロパティを開くには、コンテナーの[IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出しをサポートしてください。</span><span class="sxs-lookup"><span data-stu-id="53f4f-143">Support a call to the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="53f4f-144">コンテナーの[IMAPIProp::GetPropList](imapiprop-getproplist.md)または[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドの呼び出しから**PR_CONTAINER_HIERARCHY**を返します。</span><span class="sxs-lookup"><span data-stu-id="53f4f-144">Return **PR_CONTAINER_HIERARCHY** from a call to the container's [IMAPIProp::GetPropList](imapiprop-getproplist.md) or [IMAPIProp::GetProps](imapiprop-getprops.md) methods.</span></span> 
    
## <a name="notes-to-callers"></a><span data-ttu-id="53f4f-145">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="53f4f-145">Notes to callers</span></span>

<span data-ttu-id="53f4f-146">文字列とバイナリの内容のテーブルの列を切り捨てることができます。</span><span class="sxs-lookup"><span data-stu-id="53f4f-146">String and binary contents table columns can be truncated.</span></span> <span data-ttu-id="53f4f-147">通常、プロバイダーは、255 文字を返します。</span><span class="sxs-lookup"><span data-stu-id="53f4f-147">Typically, providers return 255 characters.</span></span> <span data-ttu-id="53f4f-148">テーブルには、切り捨てられた列が含まれて かどうか、あらかじめ知ることはできません、ため、列の長さが 255 であるか、510 バイトである場合、列が切り捨てられることを想定しています。</span><span class="sxs-lookup"><span data-stu-id="53f4f-148">Because you cannot know beforehand whether a table includes truncated columns, assume that a column is truncated if the length of the column is either 255 or 510 bytes.</span></span> <span data-ttu-id="53f4f-149">常にから取得できます、切り捨てられた列の最大の価値に応じて、直接オブジェクトを開くには、そのエントリの識別子を使用して、 [IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを呼び出すことによって。</span><span class="sxs-lookup"><span data-stu-id="53f4f-149">You can always retrieve the full value of a truncated column, if necessary, directly from the object by using its entry identifier to open it and then calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
  
<span data-ttu-id="53f4f-150">プロバイダーの実装の制限や並べ替え操作によっては、全体の文字列とその文字列の切り捨てられたバージョンを適用できます。</span><span class="sxs-lookup"><span data-stu-id="53f4f-150">Depending on the provider's implementation, restrictions and sorting operations can apply to the whole string or to the truncated version of that string.</span></span> <span data-ttu-id="53f4f-151">さらに、ストア プロバイダーは、階層テーブルの[SSortOrderSet](ssortorderset.md)が指定されている並べ替え順序のセットを優先するとは限りません。</span><span class="sxs-lookup"><span data-stu-id="53f4f-151">Moreover, store providers are not guaranteed to honor the sort order set [SSortOrderSet](ssortorderset.md) specified for hierarchy tables.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="53f4f-152">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="53f4f-152">MFCMAPI reference</span></span>

<span data-ttu-id="53f4f-153">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="53f4f-153">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="53f4f-154">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="53f4f-154">**File**</span></span>|<span data-ttu-id="53f4f-155">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="53f4f-155">**Function**</span></span>|<span data-ttu-id="53f4f-156">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="53f4f-156">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="53f4f-157">HierarchyTableTreeCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="53f4f-157">HierarchyTableTreeCtrl.cpp</span></span>  <br/> |<span data-ttu-id="53f4f-158">CHierarchyTableTreeCtrl::GetHierarchyTable</span><span class="sxs-lookup"><span data-stu-id="53f4f-158">CHierarchyTableTreeCtrl::GetHierarchyTable</span></span>  <br/> |<span data-ttu-id="53f4f-159">CHierarchyTableTreeCtrl クラスでは、 **GetHierarchyTable**を使用して、ツリー ビュー コントロールに表示する階層テーブルを取得します。</span><span class="sxs-lookup"><span data-stu-id="53f4f-159">The CHierarchyTableTreeCtrl class uses **GetHierarchyTable** to obtain hierarchy tables to display in a tree view control.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="53f4f-160">関連項目</span><span class="sxs-lookup"><span data-stu-id="53f4f-160">See also</span></span>



[<span data-ttu-id="53f4f-161">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="53f4f-161">IMAPIProp::GetPropList</span></span>](imapiprop-getproplist.md)
  
[<span data-ttu-id="53f4f-162">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="53f4f-162">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="53f4f-163">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="53f4f-163">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="53f4f-164">PidTagContainerHierarchy 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="53f4f-164">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="53f4f-165">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="53f4f-165">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


<span data-ttu-id="53f4f-166">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="53f4f-166">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

