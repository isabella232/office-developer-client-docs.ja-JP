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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388323"
---
# <a name="pidlidsharingcapabilities-canonical-property"></a><span data-ttu-id="665d9-103">PidLidSharingCapabilities 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="665d9-103">PidLidSharingCapabilities Canonical Property</span></span>

  
  
<span data-ttu-id="665d9-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="665d9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="665d9-105">共有メッセージのプロパティとして指定します。</span><span class="sxs-lookup"><span data-stu-id="665d9-105">Designates as a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="665d9-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="665d9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="665d9-107">dispidSharingCaps</span><span class="sxs-lookup"><span data-stu-id="665d9-107">dispidSharingCaps</span></span>  <br/> |
|<span data-ttu-id="665d9-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="665d9-108">Property set:</span></span>  <br/> |<span data-ttu-id="665d9-109">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="665d9-109">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="665d9-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="665d9-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="665d9-111">0x00008A17</span><span class="sxs-lookup"><span data-stu-id="665d9-111">0x00008A17</span></span>  <br/> |
|<span data-ttu-id="665d9-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="665d9-112">Data type:</span></span>  <br/> |<span data-ttu-id="665d9-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="665d9-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="665d9-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="665d9-114">Area:</span></span>  <br/> |<span data-ttu-id="665d9-115">共有</span><span class="sxs-lookup"><span data-stu-id="665d9-115">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="665d9-116">備考</span><span class="sxs-lookup"><span data-stu-id="665d9-116">Remarks</span></span>

<span data-ttu-id="665d9-117">このプロパティは、次の値のいずれかに設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="665d9-117">This property must be set to one of the following values:</span></span>
  
|<span data-ttu-id="665d9-118">**値**</span><span class="sxs-lookup"><span data-stu-id="665d9-118">**Value**</span></span>|<span data-ttu-id="665d9-119">**シナリオ**</span><span class="sxs-lookup"><span data-stu-id="665d9-119">**Scenario**</span></span>|
|:-----|:-----|
|<span data-ttu-id="665d9-120">0x00040290</span><span class="sxs-lookup"><span data-stu-id="665d9-120">0x00040290</span></span>  <br/> |<span data-ttu-id="665d9-121">このメッセージの共有オブジェクトは、特別なフォルダーに関連します。</span><span class="sxs-lookup"><span data-stu-id="665d9-121">This Sharing Message object relates to a special folder.</span></span>  <br/> |
|<span data-ttu-id="665d9-122">0x000402B0</span><span class="sxs-lookup"><span data-stu-id="665d9-122">0x000402B0</span></span>  <br/> |<span data-ttu-id="665d9-123">このメッセージの共有オブジェクトは、特別なフォルダーには関係ないです。</span><span class="sxs-lookup"><span data-stu-id="665d9-123">This Sharing Message object does not relate to a special folder.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="665d9-124">関連リソース</span><span class="sxs-lookup"><span data-stu-id="665d9-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="665d9-125">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="665d9-125">Protocol specifications</span></span>

<span data-ttu-id="665d9-126">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="665d9-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="665d9-127">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="665d9-127">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="665d9-128">[[MS OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="665d9-128">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="665d9-129">クライアント間でのメールボックスのフォルダーを共有します。</span><span class="sxs-lookup"><span data-stu-id="665d9-129">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="665d9-130">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="665d9-130">Header files</span></span>

<span data-ttu-id="665d9-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="665d9-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="665d9-132">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="665d9-132">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="665d9-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="665d9-133">See also</span></span>



[<span data-ttu-id="665d9-134">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="665d9-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="665d9-135">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="665d9-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="665d9-136">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="665d9-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="665d9-137">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="665d9-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

