---
title: PidTagParentEntryId の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagParentEntryId
api_type:
- COM
ms.assetid: 55e08ace-493c-4246-8ebf-c304f4abc56a
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: ba30514df028805135e9e31e7214ca336b1b3f85
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803164"
---
# <a name="pidtagparententryid-canonical-property"></a><span data-ttu-id="141e2-103">PidTagParentEntryId の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="141e2-103">PidTagParentEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="141e2-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="141e2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="141e2-105">フォルダーまたはメッセージを含むフォルダーのエントリ id が含まれています。</span><span class="sxs-lookup"><span data-stu-id="141e2-105">Contains the entry identifier of the folder that contains a folder or message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="141e2-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="141e2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="141e2-107">PR_PARENT_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="141e2-107">PR_PARENT_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="141e2-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="141e2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="141e2-109">0x0E09</span><span class="sxs-lookup"><span data-stu-id="141e2-109">0x0E09</span></span>  <br/> |
|<span data-ttu-id="141e2-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="141e2-110">Data type:</span></span>  <br/> |<span data-ttu-id="141e2-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="141e2-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="141e2-112">領域:</span><span class="sxs-lookup"><span data-stu-id="141e2-112">Area:</span></span>  <br/> |<span data-ttu-id="141e2-113">ID プロパティ</span><span class="sxs-lookup"><span data-stu-id="141e2-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="141e2-114">備考</span><span class="sxs-lookup"><span data-stu-id="141e2-114">Remarks</span></span>

<span data-ttu-id="141e2-115">このプロパティは、すべてのフォルダーとメッセージのメッセージ ・ ストアによって計算されます。</span><span class="sxs-lookup"><span data-stu-id="141e2-115">This property is computed by message stores for all folders and messages.</span></span>
  
<span data-ttu-id="141e2-116">メッセージ ストアのルート フォルダーには、このプロパティには、フォルダーのエントリ id が含まれています。</span><span class="sxs-lookup"><span data-stu-id="141e2-116">For a message store root folder, this property contains the folder's own entry identifier.</span></span>
  
 <span data-ttu-id="141e2-117">**PR_PARENT_DISPLAY**([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) と、このプロパティは互いに関連付けられていません。</span><span class="sxs-lookup"><span data-stu-id="141e2-117">**PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) and this property are not related to each other.</span></span> <span data-ttu-id="141e2-118">まったく異なるコンテキストに属しているとします。</span><span class="sxs-lookup"><span data-stu-id="141e2-118">They belong to entirely different contexts.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="141e2-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="141e2-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="141e2-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="141e2-120">Protocol specifications</span></span>

<span data-ttu-id="141e2-121">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="141e2-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="141e2-122">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="141e2-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="141e2-123">[[MS OXCDATA]](http://msdn.microsoft.com/library/ 1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="141e2-123">[[MS-OXCDATA]](http://msdn.microsoft.com/library/ 1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="141e2-124">リモート操作で使用される基本的なデータ構造を定義します。</span><span class="sxs-lookup"><span data-stu-id="141e2-124">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="141e2-125">[[MS OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="141e2-125">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="141e2-126">フォルダーの操作を処理します。</span><span class="sxs-lookup"><span data-stu-id="141e2-126">Handles folder operations.</span></span>
    
<span data-ttu-id="141e2-127">[[MS OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="141e2-127">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="141e2-128">IETF RFC2445、RFC2446、RFC2447、および予定と会議のオブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="141e2-128">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="141e2-129">[[MS OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="141e2-129">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="141e2-130">許可/禁止リストの処理、迷惑メール メッセージの決定を可能にします。</span><span class="sxs-lookup"><span data-stu-id="141e2-130">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
<span data-ttu-id="141e2-131">[[MS OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="141e2-131">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="141e2-132">プロパティを作成すると、メールボックス内の特別なフォルダーを検索する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="141e2-132">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="141e2-133">[[MS OXPFOAB]](http://msdn.microsoft.com/library/258a07a7-34a7-4373-87c1-cddf51447d00%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="141e2-133">[[MS-OXPFOAB]](http://msdn.microsoft.com/library/258a07a7-34a7-4373-87c1-cddf51447d00%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="141e2-134">オフライン アドレス帳 (OAB) のデータをサーバーからクライアントに配信する方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="141e2-134">Specifies the method of delivering offline address book (OAB) data from server to client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="141e2-135">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="141e2-135">Header files</span></span>

<span data-ttu-id="141e2-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="141e2-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="141e2-137">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="141e2-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="141e2-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="141e2-138">Mapitags.h</span></span>
  
> <span data-ttu-id="141e2-139">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="141e2-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="141e2-140">関連項目</span><span class="sxs-lookup"><span data-stu-id="141e2-140">See also</span></span>



[<span data-ttu-id="141e2-141">PidTagFolderType の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="141e2-141">PidTagFolderType Canonical Property</span></span>](pidtagfoldertype-canonical-property.md)


[<span data-ttu-id="141e2-142">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="141e2-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="141e2-143">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="141e2-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="141e2-144">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="141e2-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="141e2-145">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="141e2-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

