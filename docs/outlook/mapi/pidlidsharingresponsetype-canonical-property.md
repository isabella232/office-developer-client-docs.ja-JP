---
title: PidLidSharingResponseType の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: a645ee26b56355c6594f5667585becbcff2e3eec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802180"
---
# <a name="pidlidsharingresponsetype-canonical-property"></a><span data-ttu-id="63b45-103">PidLidSharingResponseType の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="63b45-103">PidLidSharingResponseType Canonical Property</span></span>

  
  
<span data-ttu-id="63b45-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="63b45-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="63b45-105">共有要求の受信者が返信している応答の種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="63b45-105">Specifies the type of response with which the recipient of the sharing request responded.</span></span> <span data-ttu-id="63b45-106">これは、共有メッセージのプロパティです。</span><span class="sxs-lookup"><span data-stu-id="63b45-106">This is a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="63b45-107">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="63b45-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="63b45-108">dispidSharingResponseType</span><span class="sxs-lookup"><span data-stu-id="63b45-108">dispidSharingResponseType</span></span>  <br/> |
|<span data-ttu-id="63b45-109">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="63b45-109">Property set:</span></span>  <br/> |<span data-ttu-id="63b45-110">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="63b45-110">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="63b45-111">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="63b45-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="63b45-112">0x00008A27</span><span class="sxs-lookup"><span data-stu-id="63b45-112">0x00008A27</span></span>  <br/> |
|<span data-ttu-id="63b45-113">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="63b45-113">Data type:</span></span>  <br/> |<span data-ttu-id="63b45-114">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="63b45-114">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="63b45-115">領域:</span><span class="sxs-lookup"><span data-stu-id="63b45-115">Area:</span></span>  <br/> |<span data-ttu-id="63b45-116">共有</span><span class="sxs-lookup"><span data-stu-id="63b45-116">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="63b45-117">備考</span><span class="sxs-lookup"><span data-stu-id="63b45-117">Remarks</span></span>

<span data-ttu-id="63b45-118">このプロパティの値を次の値のいずれかに設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="63b45-118">The value of this property must be set to one of the following values:</span></span>
  
|<span data-ttu-id="63b45-119">**値**</span><span class="sxs-lookup"><span data-stu-id="63b45-119">**Value**</span></span>|<span data-ttu-id="63b45-120">**説明**</span><span class="sxs-lookup"><span data-stu-id="63b45-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="63b45-121">0x00000000</span><span class="sxs-lookup"><span data-stu-id="63b45-121">0x00000000</span></span>  <br/> |<span data-ttu-id="63b45-122">応答がありません。</span><span class="sxs-lookup"><span data-stu-id="63b45-122">No response</span></span>  <br/> |
|<span data-ttu-id="63b45-123">0x00000001</span><span class="sxs-lookup"><span data-stu-id="63b45-123">0x00000001</span></span>  <br/> |<span data-ttu-id="63b45-124">了承済み</span><span class="sxs-lookup"><span data-stu-id="63b45-124">Accepted</span></span>  <br/> |
|<span data-ttu-id="63b45-125">0x00000002</span><span class="sxs-lookup"><span data-stu-id="63b45-125">0x00000002</span></span>  <br/> |<span data-ttu-id="63b45-126">拒否</span><span class="sxs-lookup"><span data-stu-id="63b45-126">Denied</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="63b45-127">関連リソース</span><span class="sxs-lookup"><span data-stu-id="63b45-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="63b45-128">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="63b45-128">Protocol specifications</span></span>

<span data-ttu-id="63b45-129">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="63b45-129">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="63b45-130">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="63b45-130">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="63b45-131">[[MS OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="63b45-131">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="63b45-132">クライアント間でのメールボックスのフォルダーを共有します。</span><span class="sxs-lookup"><span data-stu-id="63b45-132">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="63b45-133">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="63b45-133">Header files</span></span>

<span data-ttu-id="63b45-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="63b45-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="63b45-135">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="63b45-135">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="63b45-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="63b45-136">See also</span></span>



[<span data-ttu-id="63b45-137">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="63b45-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="63b45-138">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="63b45-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="63b45-139">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="63b45-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="63b45-140">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="63b45-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

