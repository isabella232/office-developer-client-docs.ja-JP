---
title: PidLidSharingCapabilities の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 73f39c0b97ebcd5c84bb908b62f758eaacd4eabf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802150"
---
# <a name="pidlidsharingcapabilities-canonical-property"></a><span data-ttu-id="7e505-103">PidLidSharingCapabilities の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="7e505-103">PidLidSharingCapabilities Canonical Property</span></span>

  
  
<span data-ttu-id="7e505-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7e505-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7e505-105">共有メッセージのプロパティとして指定します。</span><span class="sxs-lookup"><span data-stu-id="7e505-105">Designates as a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7e505-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="7e505-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7e505-107">dispidSharingCaps</span><span class="sxs-lookup"><span data-stu-id="7e505-107">dispidSharingCaps</span></span>  <br/> |
|<span data-ttu-id="7e505-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="7e505-108">Property set:</span></span>  <br/> |<span data-ttu-id="7e505-109">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="7e505-109">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="7e505-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="7e505-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="7e505-111">0x00008A17</span><span class="sxs-lookup"><span data-stu-id="7e505-111">0x00008A17</span></span>  <br/> |
|<span data-ttu-id="7e505-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="7e505-112">Data type:</span></span>  <br/> |<span data-ttu-id="7e505-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="7e505-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="7e505-114">領域:</span><span class="sxs-lookup"><span data-stu-id="7e505-114">Area:</span></span>  <br/> |<span data-ttu-id="7e505-115">共有</span><span class="sxs-lookup"><span data-stu-id="7e505-115">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7e505-116">備考</span><span class="sxs-lookup"><span data-stu-id="7e505-116">Remarks</span></span>

<span data-ttu-id="7e505-117">このプロパティは、次の値のいずれかに設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7e505-117">This property must be set to one of the following values:</span></span>
  
|<span data-ttu-id="7e505-118">**値**</span><span class="sxs-lookup"><span data-stu-id="7e505-118">**Value**</span></span>|<span data-ttu-id="7e505-119">**シナリオ**</span><span class="sxs-lookup"><span data-stu-id="7e505-119">**Scenario**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7e505-120">0x00040290</span><span class="sxs-lookup"><span data-stu-id="7e505-120">0x00040290</span></span>  <br/> |<span data-ttu-id="7e505-121">このメッセージの共有オブジェクトは、特別なフォルダーに関連します。</span><span class="sxs-lookup"><span data-stu-id="7e505-121">This Sharing Message object relates to a special folder.</span></span>  <br/> |
|<span data-ttu-id="7e505-122">0x000402B0</span><span class="sxs-lookup"><span data-stu-id="7e505-122">0x000402B0</span></span>  <br/> |<span data-ttu-id="7e505-123">このメッセージの共有オブジェクトは、特別なフォルダーには関係ないです。</span><span class="sxs-lookup"><span data-stu-id="7e505-123">This Sharing Message object does not relate to a special folder.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="7e505-124">関連リソース</span><span class="sxs-lookup"><span data-stu-id="7e505-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7e505-125">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="7e505-125">Protocol specifications</span></span>

<span data-ttu-id="7e505-126">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7e505-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7e505-127">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="7e505-127">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7e505-128">[[MS OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7e505-128">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7e505-129">クライアント間でのメールボックスのフォルダーを共有します。</span><span class="sxs-lookup"><span data-stu-id="7e505-129">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7e505-130">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="7e505-130">Header files</span></span>

<span data-ttu-id="7e505-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7e505-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="7e505-132">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="7e505-132">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7e505-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="7e505-133">See also</span></span>



[<span data-ttu-id="7e505-134">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="7e505-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7e505-135">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="7e505-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7e505-136">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="7e505-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7e505-137">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="7e505-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

