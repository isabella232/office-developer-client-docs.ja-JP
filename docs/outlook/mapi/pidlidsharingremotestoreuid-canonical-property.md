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
ms.openlocfilehash: bf1376e1efe23aa59aa9a70c1f0accdeac92d250
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331305"
---
# <a name="pidlidsharingremotestoreuid-canonical-property"></a><span data-ttu-id="7c199-103">PidLidSharingRemoteStoreUid 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="7c199-103">PidLidSharingRemoteStoreUid Canonical Property</span></span>

  
  
<span data-ttu-id="7c199-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7c199-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7c199-105">共有フォルダーの**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) プロパティの値の16進文字列表現を指定します。</span><span class="sxs-lookup"><span data-stu-id="7c199-105">Specifies the hexadecimal string representation of the value of the **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) property on the shared folder.</span></span> <span data-ttu-id="7c199-106">これは、共有メッセージのプロパティです。</span><span class="sxs-lookup"><span data-stu-id="7c199-106">This is a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7c199-107">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="7c199-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="7c199-108">dispidSharingRemoteStoreUid</span><span class="sxs-lookup"><span data-stu-id="7c199-108">dispidSharingRemoteStoreUid</span></span>  <br/> |
|<span data-ttu-id="7c199-109">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="7c199-109">Property set:</span></span>  <br/> |<span data-ttu-id="7c199-110">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="7c199-110">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="7c199-111">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="7c199-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="7c199-112">0x00008a48</span><span class="sxs-lookup"><span data-stu-id="7c199-112">0x00008A48</span></span>  <br/> |
|<span data-ttu-id="7c199-113">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="7c199-113">Data type:</span></span>  <br/> |<span data-ttu-id="7c199-114">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7c199-114">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="7c199-115">エリア:</span><span class="sxs-lookup"><span data-stu-id="7c199-115">Area:</span></span>  <br/> |<span data-ttu-id="7c199-116">共有</span><span class="sxs-lookup"><span data-stu-id="7c199-116">Sharing</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="7c199-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="7c199-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7c199-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="7c199-118">Protocol specifications</span></span>

<span data-ttu-id="7c199-119">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7c199-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7c199-120">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="7c199-120">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7c199-121">[[OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7c199-121">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7c199-122">クライアント間でメールボックスフォルダーを共有します。</span><span class="sxs-lookup"><span data-stu-id="7c199-122">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7c199-123">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="7c199-123">Header files</span></span>

<span data-ttu-id="7c199-124">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7c199-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="7c199-125">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="7c199-125">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7c199-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="7c199-126">See also</span></span>



[<span data-ttu-id="7c199-127">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="7c199-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7c199-128">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="7c199-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7c199-129">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="7c199-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7c199-130">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="7c199-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

