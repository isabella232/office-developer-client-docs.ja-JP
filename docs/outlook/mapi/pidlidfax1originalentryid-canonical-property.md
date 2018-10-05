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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394693"
---
# <a name="pidlidfax1originalentryid-canonical-property"></a><span data-ttu-id="369ff-103">PidLidFax1OriginalEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="369ff-103">PidLidFax1OriginalEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="369ff-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="369ff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="369ff-105">ビジネス、連絡先の fax アドレスの元のエントリ Id を指定します。</span><span class="sxs-lookup"><span data-stu-id="369ff-105">Specifies the original EntryID of the contact's business fax address.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="369ff-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="369ff-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="369ff-107">dispidFax1OriginalEntryID</span><span class="sxs-lookup"><span data-stu-id="369ff-107">dispidFax1OriginalEntryID</span></span>  <br/> |
|<span data-ttu-id="369ff-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="369ff-108">Property set:</span></span>  <br/> |<span data-ttu-id="369ff-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="369ff-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="369ff-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="369ff-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="369ff-111">0x000080B5</span><span class="sxs-lookup"><span data-stu-id="369ff-111">0x000080B5</span></span>  <br/> |
|<span data-ttu-id="369ff-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="369ff-112">Data type:</span></span>  <br/> |<span data-ttu-id="369ff-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="369ff-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="369ff-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="369ff-114">Area:</span></span>  <br/> |<span data-ttu-id="369ff-115">Contact</span><span class="sxs-lookup"><span data-stu-id="369ff-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="369ff-116">備考</span><span class="sxs-lookup"><span data-stu-id="369ff-116">Remarks</span></span>

<span data-ttu-id="369ff-117">このプロパティは、存在する場合がこの fax アドレスに対応する 1 回限りのエントリ Id を指定しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="369ff-117">This property, if present, must specify the one-off EntryId that corresponds to this fax address.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="369ff-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="369ff-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="369ff-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="369ff-119">Protocol specifications</span></span>

<span data-ttu-id="369ff-120">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="369ff-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="369ff-121">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="369ff-121">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="369ff-122">[[MS OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="369ff-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="369ff-123">プロパティは、連絡先、個人用配布リストの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="369ff-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="369ff-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="369ff-124">Header files</span></span>

<span data-ttu-id="369ff-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="369ff-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="369ff-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="369ff-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="369ff-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="369ff-127">See also</span></span>



[<span data-ttu-id="369ff-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="369ff-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="369ff-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="369ff-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="369ff-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="369ff-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="369ff-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="369ff-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

