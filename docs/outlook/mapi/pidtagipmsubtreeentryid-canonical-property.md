---
title: PidTagIpmSubtreeEntryId の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 9635c06ffa5638e370312e3b2b29e0c98161a766
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802897"
---
# <a name="pidtagipmsubtreeentryid-canonical-property"></a><span data-ttu-id="82e74-103">PidTagIpmSubtreeEntryId の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="82e74-103">PidTagIpmSubtreeEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="82e74-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="82e74-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="82e74-105">メッセージ ストアのフォルダー ツリーで、個人間メッセージ (IPM) フォルダーのサブツリーのルートのエントリ id が含まれています。</span><span class="sxs-lookup"><span data-stu-id="82e74-105">Contains the entry identifier of the root of the interpersonal message (IPM) folder subtree in the message store's folder tree.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="82e74-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="82e74-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="82e74-107">PR_IPM_SUBTREE_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="82e74-107">PR_IPM_SUBTREE_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="82e74-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="82e74-108">Identifier:</span></span>  <br/> |<span data-ttu-id="82e74-109">0x35E0</span><span class="sxs-lookup"><span data-stu-id="82e74-109">0x35E0</span></span>  <br/> |
|<span data-ttu-id="82e74-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="82e74-110">Data type:</span></span>  <br/> |<span data-ttu-id="82e74-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="82e74-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="82e74-112">領域:</span><span class="sxs-lookup"><span data-stu-id="82e74-112">Area:</span></span>  <br/> |<span data-ttu-id="82e74-113">Folder</span><span class="sxs-lookup"><span data-stu-id="82e74-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="82e74-114">備考</span><span class="sxs-lookup"><span data-stu-id="82e74-114">Remarks</span></span>

<span data-ttu-id="82e74-115">このプロパティでは、IPM の階層のルートを表します。</span><span class="sxs-lookup"><span data-stu-id="82e74-115">This property represents the root of the IPM hierarchy.</span></span> <span data-ttu-id="82e74-116">IPM のクライアントでは、このプロパティによって表されるフォルダーのサブフォルダーではないすべてのフォルダーが表示されない必要があります。</span><span class="sxs-lookup"><span data-stu-id="82e74-116">IPM clients should not display any folders that are not subfolders of the folder represented by this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="82e74-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="82e74-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="82e74-118">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="82e74-118">Header files</span></span>

<span data-ttu-id="82e74-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="82e74-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="82e74-120">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="82e74-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="82e74-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="82e74-121">Mapitags.h</span></span>
  
> <span data-ttu-id="82e74-122">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="82e74-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="82e74-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="82e74-123">See also</span></span>



[<span data-ttu-id="82e74-124">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="82e74-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="82e74-125">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="82e74-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="82e74-126">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="82e74-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="82e74-127">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="82e74-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

