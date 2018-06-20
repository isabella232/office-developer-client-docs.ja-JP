---
title: PidLidSharingRemoteType の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 8a9975090a8b90946482fa77fd2dafdb503c1f68
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802172"
---
# <a name="pidlidsharingremotetype-canonical-property"></a><span data-ttu-id="461c7-103">PidLidSharingRemoteType の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="461c7-103">PidLidSharingRemoteType Canonical Property</span></span>

  
  
<span data-ttu-id="461c7-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="461c7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="461c7-105">リモート共有フォルダーの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="461c7-105">Specifies the type of the remote shared folder.</span></span> <span data-ttu-id="461c7-106">これは、共有メッセージのプロパティです。</span><span class="sxs-lookup"><span data-stu-id="461c7-106">This is a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="461c7-107">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="461c7-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="461c7-108">dispidSharingRemoteType</span><span class="sxs-lookup"><span data-stu-id="461c7-108">dispidSharingRemoteType</span></span>  <br/> |
|<span data-ttu-id="461c7-109">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="461c7-109">Property set:</span></span>  <br/> |<span data-ttu-id="461c7-110">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="461c7-110">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="461c7-111">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="461c7-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="461c7-112">0x00008A1D</span><span class="sxs-lookup"><span data-stu-id="461c7-112">0x00008A1D</span></span>  <br/> |
|<span data-ttu-id="461c7-113">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="461c7-113">Data type:</span></span>  <br/> |<span data-ttu-id="461c7-114">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="461c7-114">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="461c7-115">領域:</span><span class="sxs-lookup"><span data-stu-id="461c7-115">Area:</span></span>  <br/> |<span data-ttu-id="461c7-116">共有</span><span class="sxs-lookup"><span data-stu-id="461c7-116">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="461c7-117">備考</span><span class="sxs-lookup"><span data-stu-id="461c7-117">Remarks</span></span>

<span data-ttu-id="461c7-118">このプロパティは、 **dispidSharingLocalType** ([PidLidSharingLocalType](pidlidsharinglocaltype-canonical-property.md)) のプロパティと同じ値に設定する必要があります、無視してください。</span><span class="sxs-lookup"><span data-stu-id="461c7-118">This property must be set to the same value as the **dispidSharingLocalType** ([PidLidSharingLocalType](pidlidsharinglocaltype-canonical-property.md)) property and should be ignored.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="461c7-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="461c7-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="461c7-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="461c7-120">Protocol specifications</span></span>

<span data-ttu-id="461c7-121">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="461c7-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="461c7-122">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="461c7-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="461c7-123">[[MS OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="461c7-123">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="461c7-124">クライアント間でのメールボックスのフォルダーを共有します。</span><span class="sxs-lookup"><span data-stu-id="461c7-124">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="461c7-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="461c7-125">Header files</span></span>

<span data-ttu-id="461c7-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="461c7-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="461c7-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="461c7-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="461c7-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="461c7-128">See also</span></span>



[<span data-ttu-id="461c7-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="461c7-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="461c7-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="461c7-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="461c7-131">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="461c7-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="461c7-132">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="461c7-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

