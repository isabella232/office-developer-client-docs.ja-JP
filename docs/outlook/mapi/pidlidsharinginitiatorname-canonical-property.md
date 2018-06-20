---
title: PidLidSharingInitiatorName の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 1b20c2171f77451d9b7e85573260acff3243238f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802160"
---
# <a name="pidlidsharinginitiatorname-canonical-property"></a><span data-ttu-id="28828-103">PidLidSharingInitiatorName の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="28828-103">PidLidSharingInitiatorName Canonical Property</span></span>

  
  
<span data-ttu-id="28828-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="28828-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="28828-105">共有メッセージのプロパティとして指定します。</span><span class="sxs-lookup"><span data-stu-id="28828-105">Designates as a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="28828-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="28828-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="28828-107">dispidSharingInitiatorName</span><span class="sxs-lookup"><span data-stu-id="28828-107">dispidSharingInitiatorName</span></span>  <br/> |
|<span data-ttu-id="28828-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="28828-108">Property set:</span></span>  <br/> |<span data-ttu-id="28828-109">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="28828-109">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="28828-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="28828-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="28828-111">0x00008A07</span><span class="sxs-lookup"><span data-stu-id="28828-111">0x00008A07</span></span>  <br/> |
|<span data-ttu-id="28828-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="28828-112">Data type:</span></span>  <br/> |<span data-ttu-id="28828-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="28828-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="28828-114">領域:</span><span class="sxs-lookup"><span data-stu-id="28828-114">Area:</span></span>  <br/> |<span data-ttu-id="28828-115">共有</span><span class="sxs-lookup"><span data-stu-id="28828-115">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="28828-116">備考</span><span class="sxs-lookup"><span data-stu-id="28828-116">Remarks</span></span>

<span data-ttu-id="28828-117">このプロパティは、 **dispidSharingInitiatorEid** ([PidLidSharingInitiatorEntryId](pidlidsharinginitiatorentryid-canonical-property.md)) で識別されるアドレス帳からの**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) の値を設定する必要があります、無視してください。</span><span class="sxs-lookup"><span data-stu-id="28828-117">This property must be set to the value of **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) from the Address Book identified by **dispidSharingInitiatorEid** ([PidLidSharingInitiatorEntryId](pidlidsharinginitiatorentryid-canonical-property.md)) and should be ignored.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="28828-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="28828-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="28828-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="28828-119">Protocol specifications</span></span>

<span data-ttu-id="28828-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="28828-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="28828-121">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="28828-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="28828-122">[[MS OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="28828-122">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="28828-123">クライアント間でのメールボックスのフォルダーを共有します。</span><span class="sxs-lookup"><span data-stu-id="28828-123">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="28828-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="28828-124">Header files</span></span>

<span data-ttu-id="28828-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="28828-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="28828-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="28828-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="28828-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="28828-127">See also</span></span>



[<span data-ttu-id="28828-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="28828-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="28828-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="28828-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="28828-130">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="28828-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="28828-131">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="28828-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

