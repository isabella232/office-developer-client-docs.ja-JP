---
title: PidLidSharingProviderUrl の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingProviderUrl
api_type:
- COM
ms.assetid: d217ab33-d697-4d27-a962-08d551d301f0
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: eab12ef45846a8f58eb3cf327fbb40777010be7f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802164"
---
# <a name="pidlidsharingproviderurl-canonical-property"></a><span data-ttu-id="8c854-103">PidLidSharingProviderUrl の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="8c854-103">PidLidSharingProviderUrl Canonical Property</span></span>

  
  
<span data-ttu-id="8c854-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8c854-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8c854-105">共有プロバイダーに関連する、 **dispidSharingProviderGuid** ([PidLidSharingProviderGuid](pidlidsharingproviderguid-canonical-property.md)) のプロパティで指定された URL を指定します。</span><span class="sxs-lookup"><span data-stu-id="8c854-105">Specifies the URL that is related to the sharing provider and identified by the **dispidSharingProviderGuid** ([PidLidSharingProviderGuid](pidlidsharingproviderguid-canonical-property.md)) property.</span></span> <span data-ttu-id="8c854-106">これは、共有メッセージのプロパティです。</span><span class="sxs-lookup"><span data-stu-id="8c854-106">This is a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8c854-107">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="8c854-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="8c854-108">dispidSharingProviderUrl</span><span class="sxs-lookup"><span data-stu-id="8c854-108">dispidSharingProviderUrl</span></span>  <br/> |
|<span data-ttu-id="8c854-109">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="8c854-109">Property set:</span></span>  <br/> |<span data-ttu-id="8c854-110">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="8c854-110">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="8c854-111">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="8c854-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="8c854-112">0x00008A03</span><span class="sxs-lookup"><span data-stu-id="8c854-112">0x00008A03</span></span>  <br/> |
|<span data-ttu-id="8c854-113">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="8c854-113">Data type:</span></span>  <br/> |<span data-ttu-id="8c854-114">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8c854-114">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="8c854-115">領域:</span><span class="sxs-lookup"><span data-stu-id="8c854-115">Area:</span></span>  <br/> |<span data-ttu-id="8c854-116">共有</span><span class="sxs-lookup"><span data-stu-id="8c854-116">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8c854-117">備考</span><span class="sxs-lookup"><span data-stu-id="8c854-117">Remarks</span></span>

<span data-ttu-id="8c854-118">このプロパティは、共有プロバイダーに関する詳細情報を提供するために使用が一般的にですが、無視する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8c854-118">This property is generally used to provide more information about the sharing provider, but should be ignored.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8c854-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="8c854-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8c854-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="8c854-120">Protocol specifications</span></span>

<span data-ttu-id="8c854-121">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8c854-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8c854-122">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="8c854-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8c854-123">[[MS OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8c854-123">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8c854-124">クライアント間でのメールボックスのフォルダーを共有します。</span><span class="sxs-lookup"><span data-stu-id="8c854-124">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8c854-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="8c854-125">Header files</span></span>

<span data-ttu-id="8c854-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8c854-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="8c854-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="8c854-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8c854-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="8c854-128">See also</span></span>



[<span data-ttu-id="8c854-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="8c854-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8c854-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="8c854-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8c854-131">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="8c854-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8c854-132">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="8c854-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

