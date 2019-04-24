---
title: PidLidSharingRemoteType 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingRemoteType
api_type:
- COM
ms.assetid: e9bc7c7c-86df-45d8-922b-76e3b076144a
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3297ca951097c9f3601086809c6e294854c88656
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331212"
---
# <a name="pidlidsharingremotetype-canonical-property"></a><span data-ttu-id="a5879-103">PidLidSharingRemoteType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a5879-103">PidLidSharingRemoteType Canonical Property</span></span>

  
  
<span data-ttu-id="a5879-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a5879-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a5879-105">リモート共有フォルダーの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="a5879-105">Specifies the type of the remote shared folder.</span></span> <span data-ttu-id="a5879-106">これは、共有メッセージのプロパティです。</span><span class="sxs-lookup"><span data-stu-id="a5879-106">This is a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a5879-107">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="a5879-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="a5879-108">dispidsharingremotetype</span><span class="sxs-lookup"><span data-stu-id="a5879-108">dispidSharingRemoteType</span></span>  <br/> |
|<span data-ttu-id="a5879-109">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="a5879-109">Property set:</span></span>  <br/> |<span data-ttu-id="a5879-110">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="a5879-110">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="a5879-111">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="a5879-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="a5879-112">0x00008a1d</span><span class="sxs-lookup"><span data-stu-id="a5879-112">0x00008A1D</span></span>  <br/> |
|<span data-ttu-id="a5879-113">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="a5879-113">Data type:</span></span>  <br/> |<span data-ttu-id="a5879-114">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a5879-114">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="a5879-115">エリア:</span><span class="sxs-lookup"><span data-stu-id="a5879-115">Area:</span></span>  <br/> |<span data-ttu-id="a5879-116">共有</span><span class="sxs-lookup"><span data-stu-id="a5879-116">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a5879-117">解説</span><span class="sxs-lookup"><span data-stu-id="a5879-117">Remarks</span></span>

<span data-ttu-id="a5879-118">このプロパティは、 **dispidsharinglocaltype** ([PidLidSharingLocalType](pidlidsharinglocaltype-canonical-property.md)) プロパティと同じ値に設定する必要があります。無視する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a5879-118">This property must be set to the same value as the **dispidSharingLocalType** ([PidLidSharingLocalType](pidlidsharinglocaltype-canonical-property.md)) property and should be ignored.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a5879-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="a5879-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a5879-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="a5879-120">Protocol specifications</span></span>

<span data-ttu-id="a5879-121">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a5879-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a5879-122">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="a5879-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a5879-123">[[OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a5879-123">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a5879-124">クライアント間でメールボックスフォルダーを共有します。</span><span class="sxs-lookup"><span data-stu-id="a5879-124">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a5879-125">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="a5879-125">Header files</span></span>

<span data-ttu-id="a5879-126">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a5879-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="a5879-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="a5879-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a5879-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="a5879-128">See also</span></span>



[<span data-ttu-id="a5879-129">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="a5879-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a5879-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a5879-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a5879-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="a5879-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a5879-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="a5879-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

