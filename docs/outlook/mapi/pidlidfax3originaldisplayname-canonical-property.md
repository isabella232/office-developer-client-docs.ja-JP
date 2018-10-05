---
title: PidLidFax3OriginalDisplayName 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFax3OriginalDisplayName
api_type:
- COM
ms.assetid: 13d0c431-7e46-4971-9b62-62e680a4cae9
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 72cb81a487c80244dbf3920bf3aa044290fff2db
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396352"
---
# <a name="pidlidfax3originaldisplayname-canonical-property"></a><span data-ttu-id="13647-103">PidLidFax3OriginalDisplayName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="13647-103">PidLidFax3OriginalDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="13647-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="13647-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="13647-105">連絡先の元の表示名はの他の fax アドレスを指定します。</span><span class="sxs-lookup"><span data-stu-id="13647-105">Specifies the original display name of the contact's other fax address.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="13647-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="13647-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="13647-107">dispidFax3OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="13647-107">dispidFax3OriginalDisplayName</span></span>  <br/> |
|<span data-ttu-id="13647-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="13647-108">Property set:</span></span>  <br/> |<span data-ttu-id="13647-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="13647-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="13647-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="13647-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="13647-111">0x000080D4</span><span class="sxs-lookup"><span data-stu-id="13647-111">0x000080D4</span></span>  <br/> |
|<span data-ttu-id="13647-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="13647-112">Data type:</span></span>  <br/> |<span data-ttu-id="13647-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="13647-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="13647-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="13647-114">Area:</span></span>  <br/> |<span data-ttu-id="13647-115">Contact</span><span class="sxs-lookup"><span data-stu-id="13647-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="13647-116">備考</span><span class="sxs-lookup"><span data-stu-id="13647-116">Remarks</span></span>

<span data-ttu-id="13647-117">このプロパティは、存在する場合、必要があります設定する**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) のプロパティと同じ値にします。</span><span class="sxs-lookup"><span data-stu-id="13647-117">This property, if present, must be set to the same value as the **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="13647-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="13647-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="13647-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="13647-119">Protocol specifications</span></span>

<span data-ttu-id="13647-120">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="13647-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="13647-121">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="13647-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="13647-122">[[MS OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="13647-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="13647-123">プロパティは、連絡先、個人用配布リストの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="13647-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="13647-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="13647-124">Header files</span></span>

<span data-ttu-id="13647-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="13647-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="13647-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="13647-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="13647-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="13647-127">See also</span></span>



[<span data-ttu-id="13647-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="13647-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="13647-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="13647-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="13647-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="13647-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="13647-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="13647-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

