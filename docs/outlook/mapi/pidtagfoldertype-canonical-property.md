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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7cca884eae2111a94d87cc24a6d30542148ab845
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316318"
---
# <a name="pidtagfoldertype-canonical-property"></a><span data-ttu-id="c4032-103">PidTagFolderType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c4032-103">PidTagFolderType Canonical Property</span></span>

  
  
<span data-ttu-id="c4032-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c4032-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c4032-105">フォルダーの種類を示す定数を含む。</span><span class="sxs-lookup"><span data-stu-id="c4032-105">Contains a constant that indicates the folder type.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c4032-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="c4032-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c4032-107">PR_FOLDER_TYPE</span><span class="sxs-lookup"><span data-stu-id="c4032-107">PR_FOLDER_TYPE</span></span>  <br/> |
|<span data-ttu-id="c4032-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="c4032-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c4032-109">0x3601</span><span class="sxs-lookup"><span data-stu-id="c4032-109">0x3601</span></span>  <br/> |
|<span data-ttu-id="c4032-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="c4032-110">Data type:</span></span>  <br/> |<span data-ttu-id="c4032-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c4032-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c4032-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="c4032-112">Area:</span></span>  <br/> |<span data-ttu-id="c4032-113">MAPI コンテナー</span><span class="sxs-lookup"><span data-stu-id="c4032-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c4032-114">注釈</span><span class="sxs-lookup"><span data-stu-id="c4032-114">Remarks</span></span>

<span data-ttu-id="c4032-115">このプロパティには、次のいずれかの値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="c4032-115">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="c4032-116">FOLDER_GENERIC</span><span class="sxs-lookup"><span data-stu-id="c4032-116">FOLDER_GENERIC</span></span> 
  
> <span data-ttu-id="c4032-117">メッセージおよび他のフォルダーを含む汎用フォルダー。</span><span class="sxs-lookup"><span data-stu-id="c4032-117">A generic folder that contains messages and other folders.</span></span>
    
<span data-ttu-id="c4032-118">FOLDER_ROOT</span><span class="sxs-lookup"><span data-stu-id="c4032-118">FOLDER_ROOT</span></span> 
  
> <span data-ttu-id="c4032-119">フォルダー階層テーブルのルート フォルダー、つまり親フォルダーがないフォルダー。</span><span class="sxs-lookup"><span data-stu-id="c4032-119">The root folder of the folder hierarchy table, that is, a folder that has no parent folder.</span></span>
    
<span data-ttu-id="c4032-120">FOLDER_SEARCH</span><span class="sxs-lookup"><span data-stu-id="c4032-120">FOLDER_SEARCH</span></span> 
  
> <span data-ttu-id="c4032-121">検索条件を満たすメッセージへのリンクの形式で、検索の結果を含むフォルダー。</span><span class="sxs-lookup"><span data-stu-id="c4032-121">A folder that contains the results of a search, in the form of links to messages that meet search criteria.</span></span>
    
<span data-ttu-id="c4032-122">メッセージ ストアのルートは、そのストア内の対人間メッセージ (IPM) サブツリーのルートと混同しないでください。</span><span class="sxs-lookup"><span data-stu-id="c4032-122">The root of a message store should not be confused with the root of the interpersonal message (IPM) subtree in that store.</span></span> <span data-ttu-id="c4032-123">親がないストアのルート フォルダーは、NULL エントリ識別子を使用して [IMsgStore::OpenEntry](imsgstore-openentry.md) メソッドを呼び出すことによって取得されます。</span><span class="sxs-lookup"><span data-stu-id="c4032-123">The store's root folder, which has no parent, is obtained by calling the [IMsgStore::OpenEntry](imsgstore-openentry.md) method with a null entry identifier.</span></span> <span data-ttu-id="c4032-124">親を持つ IPM サブツリーのルート フォルダーは **、OpenEntry** 呼び出しに **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId)](pidtagipmsubtreeentryid-canonical-property.md)プロパティの値を使用して取得されます。</span><span class="sxs-lookup"><span data-stu-id="c4032-124">The IPM subtree's root folder, which does have a parent, is obtained by using the value of the **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) property for the **OpenEntry** call.</span></span> 
  
<span data-ttu-id="c4032-125">MAPI では、メッセージ ストアごとに 1 つのルート フォルダーのみを許可します。</span><span class="sxs-lookup"><span data-stu-id="c4032-125">MAPI allows only one root folder per message store.</span></span> <span data-ttu-id="c4032-126">このフォルダーには、メッセージと他のフォルダーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="c4032-126">This folder contains messages and other folders.</span></span> <span data-ttu-id="c4032-127">ルート フォルダー **PR_PARENT_ENTRYID** のプロパティ [(PidTagParentEntryId) プロパティ ( PidTagParentEntryId](pidtagparententryid-canonical-property.md)) には、フォルダーの独自のエントリ識別子が含まれる。</span><span class="sxs-lookup"><span data-stu-id="c4032-127">The root folder's **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) property contains the folder's own entry identifier.</span></span>
  
<span data-ttu-id="c4032-128">検索結果フォルダー内の情報は、主にコンテンツ テーブルに格納され、一般的なコンテンツ テーブルと同じ列と、各メッセージが見つかったフォルダーを識別する 2 つの追加列 **(PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) (表示名、必須) とこのプロパティ (エントリ識別子、省略可能) が格納されます。</span><span class="sxs-lookup"><span data-stu-id="c4032-128">The information in a search-results folder is mainly stored in its contents table, which contains the same columns as a typical contents table, as well as two extra columns identifying the folder in which each message was found: **PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) (display name, required) and this property (entry identifier, optional).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c4032-129">関連リソース</span><span class="sxs-lookup"><span data-stu-id="c4032-129">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c4032-130">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="c4032-130">Protocol specifications</span></span>

<span data-ttu-id="c4032-131">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c4032-131">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c4032-132">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="c4032-132">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c4032-133">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c4032-133">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c4032-134">フォルダー操作を処理します。</span><span class="sxs-lookup"><span data-stu-id="c4032-134">Handles folder operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c4032-135">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="c4032-135">Header files</span></span>

<span data-ttu-id="c4032-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c4032-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="c4032-137">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="c4032-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="c4032-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c4032-138">Mapitags.h</span></span>
  
> <span data-ttu-id="c4032-139">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="c4032-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c4032-140">関連項目</span><span class="sxs-lookup"><span data-stu-id="c4032-140">See also</span></span>



[<span data-ttu-id="c4032-141">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="c4032-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c4032-142">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c4032-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c4032-143">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="c4032-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c4032-144">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="c4032-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

