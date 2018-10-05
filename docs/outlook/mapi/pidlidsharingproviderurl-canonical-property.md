---
title: PidLidSharingProviderUrl 標準プロパティ
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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 82ef37e6c41c88cdd58cb05c97ff2e4e41537a64
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388372"
---
# <a name="pidlidsharingproviderurl-canonical-property"></a><span data-ttu-id="36739-103">PidLidSharingProviderUrl 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="36739-103">PidLidSharingProviderUrl Canonical Property</span></span>

  
  
<span data-ttu-id="36739-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="36739-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="36739-105">共有プロバイダーに関連する、 **dispidSharingProviderGuid** ([PidLidSharingProviderGuid](pidlidsharingproviderguid-canonical-property.md)) のプロパティで指定された URL を指定します。</span><span class="sxs-lookup"><span data-stu-id="36739-105">Specifies the URL that is related to the sharing provider and identified by the **dispidSharingProviderGuid** ([PidLidSharingProviderGuid](pidlidsharingproviderguid-canonical-property.md)) property.</span></span> <span data-ttu-id="36739-106">これは、共有メッセージのプロパティです。</span><span class="sxs-lookup"><span data-stu-id="36739-106">This is a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="36739-107">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="36739-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="36739-108">dispidSharingProviderUrl</span><span class="sxs-lookup"><span data-stu-id="36739-108">dispidSharingProviderUrl</span></span>  <br/> |
|<span data-ttu-id="36739-109">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="36739-109">Property set:</span></span>  <br/> |<span data-ttu-id="36739-110">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="36739-110">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="36739-111">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="36739-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="36739-112">0x00008A03</span><span class="sxs-lookup"><span data-stu-id="36739-112">0x00008A03</span></span>  <br/> |
|<span data-ttu-id="36739-113">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="36739-113">Data type:</span></span>  <br/> |<span data-ttu-id="36739-114">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="36739-114">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="36739-115">エリア:</span><span class="sxs-lookup"><span data-stu-id="36739-115">Area:</span></span>  <br/> |<span data-ttu-id="36739-116">共有</span><span class="sxs-lookup"><span data-stu-id="36739-116">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="36739-117">備考</span><span class="sxs-lookup"><span data-stu-id="36739-117">Remarks</span></span>

<span data-ttu-id="36739-118">このプロパティは、共有プロバイダーに関する詳細情報を提供するために使用が一般的にですが、無視する必要があります。</span><span class="sxs-lookup"><span data-stu-id="36739-118">This property is generally used to provide more information about the sharing provider, but should be ignored.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="36739-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="36739-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="36739-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="36739-120">Protocol specifications</span></span>

<span data-ttu-id="36739-121">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="36739-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="36739-122">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="36739-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="36739-123">[[MS OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="36739-123">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="36739-124">クライアント間でのメールボックスのフォルダーを共有します。</span><span class="sxs-lookup"><span data-stu-id="36739-124">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="36739-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="36739-125">Header files</span></span>

<span data-ttu-id="36739-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="36739-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="36739-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="36739-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="36739-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="36739-128">See also</span></span>



[<span data-ttu-id="36739-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="36739-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="36739-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="36739-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="36739-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="36739-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="36739-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="36739-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

