---
title: PidLidFax3OriginalEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFax3OriginalEntryId
api_type:
- COM
ms.assetid: afccacf1-0b8b-410c-b701-bf1bd8dcca99
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 2a77ab1fcebd729f6463a3480f1b217cd6e6041c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355875"
---
# <a name="pidlidfax3originalentryid-canonical-property"></a><span data-ttu-id="eaa39-103">PidLidFax3OriginalEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="eaa39-103">PidLidFax3OriginalEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="eaa39-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eaa39-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eaa39-105">連絡先の他の fax アドレスの元の EntryID を指定します。</span><span class="sxs-lookup"><span data-stu-id="eaa39-105">Specifies the original EntryID of the contact's other fax address.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="eaa39-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="eaa39-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="eaa39-107">dispidFax3OriginalEntryID</span><span class="sxs-lookup"><span data-stu-id="eaa39-107">dispidFax3OriginalEntryID</span></span>  <br/> |
|<span data-ttu-id="eaa39-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="eaa39-108">Property set:</span></span>  <br/> |<span data-ttu-id="eaa39-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="eaa39-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="eaa39-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="eaa39-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="eaa39-111">0x000080d5</span><span class="sxs-lookup"><span data-stu-id="eaa39-111">0x000080D5</span></span>  <br/> |
|<span data-ttu-id="eaa39-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="eaa39-112">Data type:</span></span>  <br/> |<span data-ttu-id="eaa39-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="eaa39-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="eaa39-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="eaa39-114">Area:</span></span>  <br/> |<span data-ttu-id="eaa39-115">連絡先</span><span class="sxs-lookup"><span data-stu-id="eaa39-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="eaa39-116">解説</span><span class="sxs-lookup"><span data-stu-id="eaa39-116">Remarks</span></span>

<span data-ttu-id="eaa39-117">このプロパティが存在する場合、この fax アドレスに対応する1回限りの EntryId を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="eaa39-117">This property, if present, must specify the one-off EntryId that corresponds to this fax address.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="eaa39-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="eaa39-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="eaa39-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="eaa39-119">Protocol specifications</span></span>

<span data-ttu-id="eaa39-120">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="eaa39-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="eaa39-121">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="eaa39-121">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="eaa39-122">[[OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="eaa39-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="eaa39-123">連絡先および個人用配布リストに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="eaa39-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="eaa39-124">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="eaa39-124">Header files</span></span>

<span data-ttu-id="eaa39-125">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="eaa39-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="eaa39-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="eaa39-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="eaa39-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="eaa39-127">See also</span></span>



[<span data-ttu-id="eaa39-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="eaa39-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="eaa39-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="eaa39-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="eaa39-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="eaa39-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="eaa39-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="eaa39-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

