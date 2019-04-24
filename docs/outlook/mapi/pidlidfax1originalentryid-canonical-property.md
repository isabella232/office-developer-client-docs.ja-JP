---
title: PidLidFax1OriginalEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFax1OriginalEntryId
api_type:
- COM
ms.assetid: 0e02dfcd-918e-4d0c-b701-505dee1b32d4
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 096d1c785c220b7507e2a178e654b6d54ffea7da
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328750"
---
# <a name="pidlidfax1originalentryid-canonical-property"></a><span data-ttu-id="8cc68-103">PidLidFax1OriginalEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="8cc68-103">PidLidFax1OriginalEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="8cc68-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8cc68-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8cc68-105">連絡先の勤務先の fax アドレスの元の EntryID を指定します。</span><span class="sxs-lookup"><span data-stu-id="8cc68-105">Specifies the original EntryID of the contact's business fax address.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8cc68-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="8cc68-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8cc68-107">dispidFax1OriginalEntryID</span><span class="sxs-lookup"><span data-stu-id="8cc68-107">dispidFax1OriginalEntryID</span></span>  <br/> |
|<span data-ttu-id="8cc68-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="8cc68-108">Property set:</span></span>  <br/> |<span data-ttu-id="8cc68-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="8cc68-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="8cc68-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="8cc68-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="8cc68-111">0x000080b5</span><span class="sxs-lookup"><span data-stu-id="8cc68-111">0x000080B5</span></span>  <br/> |
|<span data-ttu-id="8cc68-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="8cc68-112">Data type:</span></span>  <br/> |<span data-ttu-id="8cc68-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="8cc68-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="8cc68-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="8cc68-114">Area:</span></span>  <br/> |<span data-ttu-id="8cc68-115">連絡先</span><span class="sxs-lookup"><span data-stu-id="8cc68-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8cc68-116">解説</span><span class="sxs-lookup"><span data-stu-id="8cc68-116">Remarks</span></span>

<span data-ttu-id="8cc68-117">このプロパティが存在する場合、この fax アドレスに対応する1回限りの EntryId を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8cc68-117">This property, if present, must specify the one-off EntryId that corresponds to this fax address.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8cc68-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="8cc68-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8cc68-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="8cc68-119">Protocol specifications</span></span>

<span data-ttu-id="8cc68-120">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8cc68-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8cc68-121">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="8cc68-121">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8cc68-122">[[OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8cc68-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8cc68-123">連絡先および個人用配布リストに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="8cc68-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8cc68-124">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="8cc68-124">Header files</span></span>

<span data-ttu-id="8cc68-125">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8cc68-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="8cc68-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="8cc68-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8cc68-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="8cc68-127">See also</span></span>



[<span data-ttu-id="8cc68-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="8cc68-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8cc68-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="8cc68-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8cc68-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="8cc68-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8cc68-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="8cc68-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

