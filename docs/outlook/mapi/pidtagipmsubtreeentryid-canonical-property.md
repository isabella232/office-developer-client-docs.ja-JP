---
title: PidTagIpmSubtreeEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmSubtreeEntryId
api_type:
- HeaderDef
ms.assetid: 5763fc78-5192-4162-be27-4aadc7ed65bc
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ade74b13811445c39c73f778b6de49b67b59093b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587559"
---
# <a name="pidtagipmsubtreeentryid-canonical-property"></a><span data-ttu-id="21041-103">PidTagIpmSubtreeEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="21041-103">PidTagIpmSubtreeEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="21041-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="21041-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="21041-105">メッセージ ストアのフォルダー ツリーで、個人間メッセージ (IPM) フォルダーのサブツリーのルートのエントリ id が含まれています。</span><span class="sxs-lookup"><span data-stu-id="21041-105">Contains the entry identifier of the root of the interpersonal message (IPM) folder subtree in the message store's folder tree.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="21041-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="21041-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="21041-107">PR_IPM_SUBTREE_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="21041-107">PR_IPM_SUBTREE_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="21041-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="21041-108">Identifier:</span></span>  <br/> |<span data-ttu-id="21041-109">0x35E0</span><span class="sxs-lookup"><span data-stu-id="21041-109">0x35E0</span></span>  <br/> |
|<span data-ttu-id="21041-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="21041-110">Data type:</span></span>  <br/> |<span data-ttu-id="21041-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="21041-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="21041-112">領域:</span><span class="sxs-lookup"><span data-stu-id="21041-112">Area:</span></span>  <br/> |<span data-ttu-id="21041-113">Folder</span><span class="sxs-lookup"><span data-stu-id="21041-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="21041-114">注釈</span><span class="sxs-lookup"><span data-stu-id="21041-114">Remarks</span></span>

<span data-ttu-id="21041-115">このプロパティでは、IPM の階層のルートを表します。</span><span class="sxs-lookup"><span data-stu-id="21041-115">This property represents the root of the IPM hierarchy.</span></span> <span data-ttu-id="21041-116">IPM のクライアントでは、このプロパティによって表されるフォルダーのサブフォルダーではないすべてのフォルダーが表示されない必要があります。</span><span class="sxs-lookup"><span data-stu-id="21041-116">IPM clients should not display any folders that are not subfolders of the folder represented by this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="21041-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="21041-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="21041-118">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="21041-118">Header files</span></span>

<span data-ttu-id="21041-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="21041-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="21041-120">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="21041-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="21041-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="21041-121">Mapitags.h</span></span>
  
> <span data-ttu-id="21041-122">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="21041-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="21041-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="21041-123">See also</span></span>



[<span data-ttu-id="21041-124">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="21041-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="21041-125">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="21041-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="21041-126">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="21041-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="21041-127">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="21041-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

