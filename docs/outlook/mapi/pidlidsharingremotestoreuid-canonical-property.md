---
title: PidLidSharingRemoteStoreUid 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingRemoteStoreUid
api_type:
- COM
ms.assetid: f6773bba-45ef-4aef-90da-acad8ff64615
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b907b3385a89e0746740a4363bead41cd8fed8fd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802188"
---
# <a name="pidlidsharingremotestoreuid-canonical-property"></a><span data-ttu-id="4a138-103">PidLidSharingRemoteStoreUid 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="4a138-103">PidLidSharingRemoteStoreUid Canonical Property</span></span>

  
  
<span data-ttu-id="4a138-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4a138-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4a138-105">共有フォルダーに、 **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) プロパティの値の 16 進数の文字列形式を指定します。</span><span class="sxs-lookup"><span data-stu-id="4a138-105">Specifies the hexadecimal string representation of the value of the **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) property on the shared folder.</span></span> <span data-ttu-id="4a138-106">これは、共有メッセージのプロパティです。</span><span class="sxs-lookup"><span data-stu-id="4a138-106">This is a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4a138-107">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="4a138-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="4a138-108">dispidSharingRemoteStoreUid</span><span class="sxs-lookup"><span data-stu-id="4a138-108">dispidSharingRemoteStoreUid</span></span>  <br/> |
|<span data-ttu-id="4a138-109">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="4a138-109">Property set:</span></span>  <br/> |<span data-ttu-id="4a138-110">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="4a138-110">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="4a138-111">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="4a138-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="4a138-112">0x00008A48</span><span class="sxs-lookup"><span data-stu-id="4a138-112">0x00008A48</span></span>  <br/> |
|<span data-ttu-id="4a138-113">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="4a138-113">Data type:</span></span>  <br/> |<span data-ttu-id="4a138-114">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4a138-114">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="4a138-115">領域:</span><span class="sxs-lookup"><span data-stu-id="4a138-115">Area:</span></span>  <br/> |<span data-ttu-id="4a138-116">共有</span><span class="sxs-lookup"><span data-stu-id="4a138-116">Sharing</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="4a138-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="4a138-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4a138-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="4a138-118">Protocol specifications</span></span>

<span data-ttu-id="4a138-119">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4a138-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4a138-120">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="4a138-120">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4a138-121">[[MS OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4a138-121">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4a138-122">クライアント間でのメールボックスのフォルダーを共有します。</span><span class="sxs-lookup"><span data-stu-id="4a138-122">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4a138-123">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="4a138-123">Header files</span></span>

<span data-ttu-id="4a138-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4a138-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="4a138-125">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="4a138-125">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4a138-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="4a138-126">See also</span></span>



[<span data-ttu-id="4a138-127">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="4a138-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4a138-128">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="4a138-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4a138-129">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="4a138-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4a138-130">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="4a138-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

