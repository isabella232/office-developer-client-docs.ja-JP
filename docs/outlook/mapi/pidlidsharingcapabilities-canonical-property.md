---
title: PidLidSharingCapabilities 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingCapabilities
api_type:
- COM
ms.assetid: 86b3eab2-2594-4204-aedf-8ce2ee3b81ce
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d44851e1c863cb117eed3462eb98de87f8d1f0be
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358892"
---
# <a name="pidlidsharingcapabilities-canonical-property"></a><span data-ttu-id="932c4-103">PidLidSharingCapabilities 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="932c4-103">PidLidSharingCapabilities Canonical Property</span></span>

  
  
<span data-ttu-id="932c4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="932c4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="932c4-105">共有メッセージのプロパティとして指定します。</span><span class="sxs-lookup"><span data-stu-id="932c4-105">Designates as a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="932c4-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="932c4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="932c4-107">dispidsharingcaps</span><span class="sxs-lookup"><span data-stu-id="932c4-107">dispidSharingCaps</span></span>  <br/> |
|<span data-ttu-id="932c4-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="932c4-108">Property set:</span></span>  <br/> |<span data-ttu-id="932c4-109">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="932c4-109">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="932c4-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="932c4-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="932c4-111">0x00008a17</span><span class="sxs-lookup"><span data-stu-id="932c4-111">0x00008A17</span></span>  <br/> |
|<span data-ttu-id="932c4-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="932c4-112">Data type:</span></span>  <br/> |<span data-ttu-id="932c4-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="932c4-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="932c4-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="932c4-114">Area:</span></span>  <br/> |<span data-ttu-id="932c4-115">共有</span><span class="sxs-lookup"><span data-stu-id="932c4-115">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="932c4-116">解説</span><span class="sxs-lookup"><span data-stu-id="932c4-116">Remarks</span></span>

<span data-ttu-id="932c4-117">このプロパティは、次のいずれかの値に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="932c4-117">This property must be set to one of the following values:</span></span>
  
|<span data-ttu-id="932c4-118">**値**</span><span class="sxs-lookup"><span data-stu-id="932c4-118">**Value**</span></span>|<span data-ttu-id="932c4-119">**シナリオ**</span><span class="sxs-lookup"><span data-stu-id="932c4-119">**Scenario**</span></span>|
|:-----|:-----|
|<span data-ttu-id="932c4-120">0x00040290</span><span class="sxs-lookup"><span data-stu-id="932c4-120">0x00040290</span></span>  <br/> |<span data-ttu-id="932c4-121">この共有メッセージオブジェクトは、特別なフォルダーに関連しています。</span><span class="sxs-lookup"><span data-stu-id="932c4-121">This Sharing Message object relates to a special folder.</span></span>  <br/> |
|<span data-ttu-id="932c4-122">0x000402b0</span><span class="sxs-lookup"><span data-stu-id="932c4-122">0x000402B0</span></span>  <br/> |<span data-ttu-id="932c4-123">この共有メッセージオブジェクトは、特別なフォルダーに関連付けられていません。</span><span class="sxs-lookup"><span data-stu-id="932c4-123">This Sharing Message object does not relate to a special folder.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="932c4-124">関連リソース</span><span class="sxs-lookup"><span data-stu-id="932c4-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="932c4-125">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="932c4-125">Protocol specifications</span></span>

<span data-ttu-id="932c4-126">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="932c4-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="932c4-127">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="932c4-127">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="932c4-128">[[OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="932c4-128">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="932c4-129">クライアント間でメールボックスフォルダーを共有します。</span><span class="sxs-lookup"><span data-stu-id="932c4-129">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="932c4-130">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="932c4-130">Header files</span></span>

<span data-ttu-id="932c4-131">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="932c4-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="932c4-132">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="932c4-132">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="932c4-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="932c4-133">See also</span></span>



[<span data-ttu-id="932c4-134">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="932c4-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="932c4-135">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="932c4-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="932c4-136">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="932c4-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="932c4-137">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="932c4-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

