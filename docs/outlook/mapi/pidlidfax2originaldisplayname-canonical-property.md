---
title: PidLidFax2OriginalDisplayName 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFax2OriginalDisplayName
api_type:
- COM
ms.assetid: 7f521e27-834c-4fb5-9782-2c5d1380690f
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b0ff001dd02b577fd6c08f3f857c4194d3afc1b5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384417"
---
# <a name="pidlidfax2originaldisplayname-canonical-property"></a><span data-ttu-id="50bff-103">PidLidFax2OriginalDisplayName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="50bff-103">PidLidFax2OriginalDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="50bff-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="50bff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="50bff-105">連絡先の自宅の fax アドレスの元の表示名を指定します。</span><span class="sxs-lookup"><span data-stu-id="50bff-105">Specifies the original display name of the contact's home fax address.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="50bff-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="50bff-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="50bff-107">dispidFax2OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="50bff-107">dispidFax2OriginalDisplayName</span></span>  <br/> |
|<span data-ttu-id="50bff-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="50bff-108">Property set:</span></span>  <br/> |<span data-ttu-id="50bff-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="50bff-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="50bff-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="50bff-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="50bff-111">0x000080C4</span><span class="sxs-lookup"><span data-stu-id="50bff-111">0x000080C4</span></span>  <br/> |
|<span data-ttu-id="50bff-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="50bff-112">Data type:</span></span>  <br/> |<span data-ttu-id="50bff-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="50bff-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="50bff-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="50bff-114">Area:</span></span>  <br/> |<span data-ttu-id="50bff-115">Contact</span><span class="sxs-lookup"><span data-stu-id="50bff-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="50bff-116">備考</span><span class="sxs-lookup"><span data-stu-id="50bff-116">Remarks</span></span>

<span data-ttu-id="50bff-117">このプロパティは、存在する場合、必要があります設定する**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) のプロパティと同じ値にします。</span><span class="sxs-lookup"><span data-stu-id="50bff-117">This property, if present, must be set to the same value as the **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="50bff-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="50bff-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="50bff-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="50bff-119">Protocol specifications</span></span>

<span data-ttu-id="50bff-120">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="50bff-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="50bff-121">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="50bff-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="50bff-122">[[MS OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="50bff-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="50bff-123">プロパティは、連絡先、個人用配布リストの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="50bff-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="50bff-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="50bff-124">Header files</span></span>

<span data-ttu-id="50bff-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="50bff-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="50bff-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="50bff-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="50bff-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="50bff-127">See also</span></span>



[<span data-ttu-id="50bff-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="50bff-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="50bff-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="50bff-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="50bff-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="50bff-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="50bff-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="50bff-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

