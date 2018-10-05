---
title: PidLidSharingInitiatorName 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingInitiatorName
api_type:
- COM
ms.assetid: f2b126fc-41fa-4dc4-9f13-07bc4f621d0b
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b9e3236affa9612356e68044d2943ea7b9276384
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394383"
---
# <a name="pidlidsharinginitiatorname-canonical-property"></a><span data-ttu-id="05576-103">PidLidSharingInitiatorName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="05576-103">PidLidSharingInitiatorName Canonical Property</span></span>

  
  
<span data-ttu-id="05576-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="05576-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="05576-105">共有メッセージのプロパティとして指定します。</span><span class="sxs-lookup"><span data-stu-id="05576-105">Designates as a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="05576-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="05576-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="05576-107">dispidSharingInitiatorName</span><span class="sxs-lookup"><span data-stu-id="05576-107">dispidSharingInitiatorName</span></span>  <br/> |
|<span data-ttu-id="05576-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="05576-108">Property set:</span></span>  <br/> |<span data-ttu-id="05576-109">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="05576-109">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="05576-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="05576-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="05576-111">0x00008A07</span><span class="sxs-lookup"><span data-stu-id="05576-111">0x00008A07</span></span>  <br/> |
|<span data-ttu-id="05576-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="05576-112">Data type:</span></span>  <br/> |<span data-ttu-id="05576-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="05576-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="05576-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="05576-114">Area:</span></span>  <br/> |<span data-ttu-id="05576-115">共有</span><span class="sxs-lookup"><span data-stu-id="05576-115">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="05576-116">備考</span><span class="sxs-lookup"><span data-stu-id="05576-116">Remarks</span></span>

<span data-ttu-id="05576-117">このプロパティは、 **dispidSharingInitiatorEid** ([PidLidSharingInitiatorEntryId](pidlidsharinginitiatorentryid-canonical-property.md)) で識別されるアドレス帳からの**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) の値を設定する必要があります、無視してください。</span><span class="sxs-lookup"><span data-stu-id="05576-117">This property must be set to the value of **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) from the Address Book identified by **dispidSharingInitiatorEid** ([PidLidSharingInitiatorEntryId](pidlidsharinginitiatorentryid-canonical-property.md)) and should be ignored.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="05576-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="05576-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="05576-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="05576-119">Protocol specifications</span></span>

<span data-ttu-id="05576-120">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="05576-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="05576-121">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="05576-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="05576-122">[[MS OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="05576-122">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="05576-123">クライアント間でのメールボックスのフォルダーを共有します。</span><span class="sxs-lookup"><span data-stu-id="05576-123">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="05576-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="05576-124">Header files</span></span>

<span data-ttu-id="05576-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="05576-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="05576-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="05576-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="05576-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="05576-127">See also</span></span>



[<span data-ttu-id="05576-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="05576-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="05576-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="05576-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="05576-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="05576-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="05576-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="05576-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

