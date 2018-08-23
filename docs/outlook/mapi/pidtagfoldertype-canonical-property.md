---
title: PidTagFolderType 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFolderType
api_type:
- HeaderDef
ms.assetid: 2ab4681e-0013-4ba0-ba26-50517bbf3f5b
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 8d6167a7a3c983171f2ff9cb2a54c879a14dca0e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591416"
---
# <a name="pidtagfoldertype-canonical-property"></a><span data-ttu-id="4cef8-103">PidTagFolderType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="4cef8-103">PidTagFolderType Canonical Property</span></span>

  
  
<span data-ttu-id="4cef8-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4cef8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4cef8-105">フォルダーの種類を示す定数が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4cef8-105">Contains a constant that indicates the folder type.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4cef8-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="4cef8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4cef8-107">PR_FOLDER_TYPE</span><span class="sxs-lookup"><span data-stu-id="4cef8-107">PR_FOLDER_TYPE</span></span>  <br/> |
|<span data-ttu-id="4cef8-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="4cef8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4cef8-109">0x3601</span><span class="sxs-lookup"><span data-stu-id="4cef8-109">0x3601</span></span>  <br/> |
|<span data-ttu-id="4cef8-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="4cef8-110">Data type:</span></span>  <br/> |<span data-ttu-id="4cef8-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="4cef8-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="4cef8-112">領域:</span><span class="sxs-lookup"><span data-stu-id="4cef8-112">Area:</span></span>  <br/> |<span data-ttu-id="4cef8-113">MAPI のコンテナー</span><span class="sxs-lookup"><span data-stu-id="4cef8-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4cef8-114">注釈</span><span class="sxs-lookup"><span data-stu-id="4cef8-114">Remarks</span></span>

<span data-ttu-id="4cef8-115">このプロパティは、次の値の 1 つだけ持つことができます。</span><span class="sxs-lookup"><span data-stu-id="4cef8-115">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="4cef8-116">FOLDER_GENERIC</span><span class="sxs-lookup"><span data-stu-id="4cef8-116">FOLDER_GENERIC</span></span> 
  
> <span data-ttu-id="4cef8-117">メッセージおよびその他のフォルダーに含まれている一般的なフォルダーです。</span><span class="sxs-lookup"><span data-stu-id="4cef8-117">A generic folder that contains messages and other folders.</span></span>
    
<span data-ttu-id="4cef8-118">FOLDER_ROOT</span><span class="sxs-lookup"><span data-stu-id="4cef8-118">FOLDER_ROOT</span></span> 
  
> <span data-ttu-id="4cef8-119">フォルダーの階層テーブル、つまり、親フォルダーがないフォルダーのルート フォルダーです。</span><span class="sxs-lookup"><span data-stu-id="4cef8-119">The root folder of the folder hierarchy table, that is, a folder that has no parent folder.</span></span>
    
<span data-ttu-id="4cef8-120">FOLDER_SEARCH</span><span class="sxs-lookup"><span data-stu-id="4cef8-120">FOLDER_SEARCH</span></span> 
  
> <span data-ttu-id="4cef8-121">検索条件を満たすメッセージへのリンクの形式で、検索の結果を格納するフォルダーです。</span><span class="sxs-lookup"><span data-stu-id="4cef8-121">A folder that contains the results of a search, in the form of links to messages that meet search criteria.</span></span>
    
<span data-ttu-id="4cef8-122">メッセージ ストアのルートは、そのストア内の個人間メッセージ (IPM) サブツリーのルートと混同しないでください。</span><span class="sxs-lookup"><span data-stu-id="4cef8-122">The root of a message store should not be confused with the root of the interpersonal message (IPM) subtree in that store.</span></span> <span data-ttu-id="4cef8-123">ストアのルート フォルダーは、親を持たないが null のエントリの識別子を使用して[IMsgStore::OpenEntry](imsgstore-openentry.md)メソッドを呼び出すことによって取得されます。</span><span class="sxs-lookup"><span data-stu-id="4cef8-123">The store's root folder, which has no parent, is obtained by calling the [IMsgStore::OpenEntry](imsgstore-openentry.md) method with a null entry identifier.</span></span> <span data-ttu-id="4cef8-124">**OpenEntry**呼び出しの**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) プロパティの値を使用して、IPM サブツリーのルート フォルダーは、親を持っているが、取得します。</span><span class="sxs-lookup"><span data-stu-id="4cef8-124">The IPM subtree's root folder, which does have a parent, is obtained by using the value of the **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) property for the **OpenEntry** call.</span></span> 
  
<span data-ttu-id="4cef8-125">MAPI は、メッセージ ・ ストアごとに 1 つだけのルート フォルダーを使用できます。</span><span class="sxs-lookup"><span data-stu-id="4cef8-125">MAPI allows only one root folder per message store.</span></span> <span data-ttu-id="4cef8-126">このフォルダーには、メッセージ、およびその他のフォルダーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="4cef8-126">This folder contains messages and other folders.</span></span> <span data-ttu-id="4cef8-127">ルート フォルダーの**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) のプロパティには、フォルダーのエントリ id が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4cef8-127">The root folder's **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) property contains the folder's own entry identifier.</span></span>
  
<span data-ttu-id="4cef8-128">検索結果フォルダー内の情報がそのコンテンツ ・ テーブルの一般的な内容のテーブルと同じ列と一致する各メッセージが含まれているフォルダーを識別する 2 つの余分な列が含まれている主に格納されている: **PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) (表示名が必要です)、このプロパティ (エントリの識別子、省略可能)。</span><span class="sxs-lookup"><span data-stu-id="4cef8-128">The information in a search-results folder is mainly stored in its contents table, which contains the same columns as a typical contents table, as well as two extra columns identifying the folder in which each message was found: **PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) (display name, required) and this property (entry identifier, optional).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4cef8-129">関連リソース</span><span class="sxs-lookup"><span data-stu-id="4cef8-129">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4cef8-130">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="4cef8-130">Protocol specifications</span></span>

<span data-ttu-id="4cef8-131">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4cef8-131">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4cef8-132">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="4cef8-132">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4cef8-133">[[MS OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4cef8-133">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4cef8-134">フォルダーの操作を処理します。</span><span class="sxs-lookup"><span data-stu-id="4cef8-134">Handles folder operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4cef8-135">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="4cef8-135">Header files</span></span>

<span data-ttu-id="4cef8-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4cef8-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="4cef8-137">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="4cef8-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="4cef8-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4cef8-138">Mapitags.h</span></span>
  
> <span data-ttu-id="4cef8-139">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4cef8-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4cef8-140">関連項目</span><span class="sxs-lookup"><span data-stu-id="4cef8-140">See also</span></span>



[<span data-ttu-id="4cef8-141">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="4cef8-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4cef8-142">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="4cef8-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4cef8-143">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="4cef8-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4cef8-144">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="4cef8-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

