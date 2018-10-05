---
title: PidLidSharingResponseType 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingResponseType
api_type:
- COM
ms.assetid: c27b1239-3612-4bb3-9f22-4b89ee9900cd
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 34e8a3c73715a75b8007646e5ba3b0dc3e1ae919
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395533"
---
# <a name="pidlidsharingresponsetype-canonical-property"></a><span data-ttu-id="d5caf-103">PidLidSharingResponseType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d5caf-103">PidLidSharingResponseType Canonical Property</span></span>

  
  
<span data-ttu-id="d5caf-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d5caf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d5caf-105">共有要求の受信者が返信している応答の種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="d5caf-105">Specifies the type of response with which the recipient of the sharing request responded.</span></span> <span data-ttu-id="d5caf-106">これは、共有メッセージのプロパティです。</span><span class="sxs-lookup"><span data-stu-id="d5caf-106">This is a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d5caf-107">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="d5caf-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="d5caf-108">dispidSharingResponseType</span><span class="sxs-lookup"><span data-stu-id="d5caf-108">dispidSharingResponseType</span></span>  <br/> |
|<span data-ttu-id="d5caf-109">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="d5caf-109">Property set:</span></span>  <br/> |<span data-ttu-id="d5caf-110">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="d5caf-110">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="d5caf-111">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="d5caf-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="d5caf-112">0x00008A27</span><span class="sxs-lookup"><span data-stu-id="d5caf-112">0x00008A27</span></span>  <br/> |
|<span data-ttu-id="d5caf-113">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="d5caf-113">Data type:</span></span>  <br/> |<span data-ttu-id="d5caf-114">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d5caf-114">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d5caf-115">エリア:</span><span class="sxs-lookup"><span data-stu-id="d5caf-115">Area:</span></span>  <br/> |<span data-ttu-id="d5caf-116">共有</span><span class="sxs-lookup"><span data-stu-id="d5caf-116">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d5caf-117">備考</span><span class="sxs-lookup"><span data-stu-id="d5caf-117">Remarks</span></span>

<span data-ttu-id="d5caf-118">このプロパティの値を次の値のいずれかに設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d5caf-118">The value of this property must be set to one of the following values:</span></span>
  
|<span data-ttu-id="d5caf-119">**値**</span><span class="sxs-lookup"><span data-stu-id="d5caf-119">**Value**</span></span>|<span data-ttu-id="d5caf-120">**説明**</span><span class="sxs-lookup"><span data-stu-id="d5caf-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d5caf-121">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d5caf-121">0x00000000</span></span>  <br/> |<span data-ttu-id="d5caf-122">応答がありません。</span><span class="sxs-lookup"><span data-stu-id="d5caf-122">No response</span></span>  <br/> |
|<span data-ttu-id="d5caf-123">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d5caf-123">0x00000001</span></span>  <br/> |<span data-ttu-id="d5caf-124">了承済み</span><span class="sxs-lookup"><span data-stu-id="d5caf-124">Accepted</span></span>  <br/> |
|<span data-ttu-id="d5caf-125">0x00000002</span><span class="sxs-lookup"><span data-stu-id="d5caf-125">0x00000002</span></span>  <br/> |<span data-ttu-id="d5caf-126">拒否</span><span class="sxs-lookup"><span data-stu-id="d5caf-126">Denied</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="d5caf-127">関連リソース</span><span class="sxs-lookup"><span data-stu-id="d5caf-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d5caf-128">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="d5caf-128">Protocol specifications</span></span>

<span data-ttu-id="d5caf-129">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d5caf-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d5caf-130">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="d5caf-130">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d5caf-131">[[MS OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d5caf-131">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d5caf-132">クライアント間でのメールボックスのフォルダーを共有します。</span><span class="sxs-lookup"><span data-stu-id="d5caf-132">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d5caf-133">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="d5caf-133">Header files</span></span>

<span data-ttu-id="d5caf-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d5caf-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="d5caf-135">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="d5caf-135">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d5caf-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="d5caf-136">See also</span></span>



[<span data-ttu-id="d5caf-137">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="d5caf-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d5caf-138">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="d5caf-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d5caf-139">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="d5caf-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d5caf-140">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="d5caf-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

