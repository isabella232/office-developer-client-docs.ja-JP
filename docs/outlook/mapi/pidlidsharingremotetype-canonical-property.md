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
ms.openlocfilehash: 87f3a1902c70cc9f875d472da406104ae1b45fda
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573944"
---
# <a name="pidlidsharingremotetype-canonical-property"></a><span data-ttu-id="1cf32-103">PidLidSharingRemoteType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1cf32-103">PidLidSharingRemoteType Canonical Property</span></span>

  
  
<span data-ttu-id="1cf32-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1cf32-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1cf32-105">リモート共有フォルダーの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="1cf32-105">Specifies the type of the remote shared folder.</span></span> <span data-ttu-id="1cf32-106">これは、共有メッセージのプロパティです。</span><span class="sxs-lookup"><span data-stu-id="1cf32-106">This is a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1cf32-107">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="1cf32-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="1cf32-108">dispidSharingRemoteType</span><span class="sxs-lookup"><span data-stu-id="1cf32-108">dispidSharingRemoteType</span></span>  <br/> |
|<span data-ttu-id="1cf32-109">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="1cf32-109">Property set:</span></span>  <br/> |<span data-ttu-id="1cf32-110">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="1cf32-110">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="1cf32-111">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="1cf32-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="1cf32-112">0x00008A1D</span><span class="sxs-lookup"><span data-stu-id="1cf32-112">0x00008A1D</span></span>  <br/> |
|<span data-ttu-id="1cf32-113">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="1cf32-113">Data type:</span></span>  <br/> |<span data-ttu-id="1cf32-114">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1cf32-114">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="1cf32-115">領域:</span><span class="sxs-lookup"><span data-stu-id="1cf32-115">Area:</span></span>  <br/> |<span data-ttu-id="1cf32-116">共有</span><span class="sxs-lookup"><span data-stu-id="1cf32-116">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1cf32-117">注釈</span><span class="sxs-lookup"><span data-stu-id="1cf32-117">Remarks</span></span>

<span data-ttu-id="1cf32-118">このプロパティは、 **dispidSharingLocalType** ([PidLidSharingLocalType](pidlidsharinglocaltype-canonical-property.md)) のプロパティと同じ値に設定する必要があります、無視してください。</span><span class="sxs-lookup"><span data-stu-id="1cf32-118">This property must be set to the same value as the **dispidSharingLocalType** ([PidLidSharingLocalType](pidlidsharinglocaltype-canonical-property.md)) property and should be ignored.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1cf32-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="1cf32-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1cf32-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="1cf32-120">Protocol specifications</span></span>

<span data-ttu-id="1cf32-121">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1cf32-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1cf32-122">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="1cf32-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1cf32-123">[[MS OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1cf32-123">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1cf32-124">クライアント間でのメールボックスのフォルダーを共有します。</span><span class="sxs-lookup"><span data-stu-id="1cf32-124">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1cf32-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="1cf32-125">Header files</span></span>

<span data-ttu-id="1cf32-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1cf32-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="1cf32-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="1cf32-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1cf32-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="1cf32-128">See also</span></span>



[<span data-ttu-id="1cf32-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="1cf32-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1cf32-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="1cf32-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1cf32-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1cf32-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1cf32-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1cf32-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

