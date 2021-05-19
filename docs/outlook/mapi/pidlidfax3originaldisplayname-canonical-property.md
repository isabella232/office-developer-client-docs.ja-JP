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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 72cb81a487c80244dbf3920bf3aa044290fff2db
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357597"
---
# <a name="pidlidfax3originaldisplayname-canonical-property"></a><span data-ttu-id="1d643-103">PidLidFax3OriginalDisplayName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1d643-103">PidLidFax3OriginalDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="1d643-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1d643-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1d643-105">連絡先の他の FAX アドレスの元の表示名を指定します。</span><span class="sxs-lookup"><span data-stu-id="1d643-105">Specifies the original display name of the contact's other fax address.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1d643-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="1d643-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1d643-107">dispidFax3OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="1d643-107">dispidFax3OriginalDisplayName</span></span>  <br/> |
|<span data-ttu-id="1d643-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="1d643-108">Property set:</span></span>  <br/> |<span data-ttu-id="1d643-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="1d643-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="1d643-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="1d643-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="1d643-111">0x000080D4</span><span class="sxs-lookup"><span data-stu-id="1d643-111">0x000080D4</span></span>  <br/> |
|<span data-ttu-id="1d643-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="1d643-112">Data type:</span></span>  <br/> |<span data-ttu-id="1d643-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1d643-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="1d643-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="1d643-114">Area:</span></span>  <br/> |<span data-ttu-id="1d643-115">Contact</span><span class="sxs-lookup"><span data-stu-id="1d643-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1d643-116">注釈</span><span class="sxs-lookup"><span data-stu-id="1d643-116">Remarks</span></span>

<span data-ttu-id="1d643-117">このプロパティが存在する場合は、プロパティ ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) プロパティと同 **PR_NORMALIZED_SUBJECT** に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1d643-117">This property, if present, must be set to the same value as the **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1d643-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="1d643-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1d643-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="1d643-119">Protocol specifications</span></span>

<span data-ttu-id="1d643-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1d643-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1d643-121">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="1d643-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1d643-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1d643-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1d643-123">連絡先と個人用配布リストで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="1d643-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1d643-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="1d643-124">Header files</span></span>

<span data-ttu-id="1d643-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1d643-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="1d643-126">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="1d643-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1d643-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="1d643-127">See also</span></span>



[<span data-ttu-id="1d643-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="1d643-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1d643-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1d643-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1d643-130">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="1d643-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1d643-131">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="1d643-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

