---
title: PidLidFax2OriginalEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFax2OriginalEntryId
api_type:
- COM
ms.assetid: da80d72f-9389-463f-8665-f26bb30c0ed2
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f6b8a00070cba755eb043e90586528674e461514
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592613"
---
# <a name="pidlidfax2originalentryid-canonical-property"></a><span data-ttu-id="980dd-103">PidLidFax2OriginalEntryId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="980dd-103">PidLidFax2OriginalEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="980dd-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="980dd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="980dd-105">連絡先の自宅の fax アドレスの元のエントリ Id を指定します。</span><span class="sxs-lookup"><span data-stu-id="980dd-105">Specifies the original EntryID of the contact's home fax address.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="980dd-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="980dd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="980dd-107">dispidFax2OriginalEntryID</span><span class="sxs-lookup"><span data-stu-id="980dd-107">dispidFax2OriginalEntryID</span></span>  <br/> |
|<span data-ttu-id="980dd-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="980dd-108">Property set:</span></span>  <br/> |<span data-ttu-id="980dd-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="980dd-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="980dd-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="980dd-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="980dd-111">0x000080C5</span><span class="sxs-lookup"><span data-stu-id="980dd-111">0x000080C5</span></span>  <br/> |
|<span data-ttu-id="980dd-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="980dd-112">Data type:</span></span>  <br/> |<span data-ttu-id="980dd-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="980dd-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="980dd-114">領域:</span><span class="sxs-lookup"><span data-stu-id="980dd-114">Area:</span></span>  <br/> |<span data-ttu-id="980dd-115">Contact</span><span class="sxs-lookup"><span data-stu-id="980dd-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="980dd-116">注釈</span><span class="sxs-lookup"><span data-stu-id="980dd-116">Remarks</span></span>

<span data-ttu-id="980dd-117">このプロパティは、存在する場合がこの fax アドレスに対応する 1 回限りのエントリ Id を指定しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="980dd-117">This property, if present, must specify the one-off EntryId that corresponds to this fax address.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="980dd-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="980dd-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="980dd-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="980dd-119">Protocol specifications</span></span>

<span data-ttu-id="980dd-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="980dd-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="980dd-121">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="980dd-121">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="980dd-122">[[MS OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="980dd-122">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="980dd-123">プロパティは、連絡先、個人用配布リストの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="980dd-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="980dd-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="980dd-124">Header files</span></span>

<span data-ttu-id="980dd-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="980dd-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="980dd-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="980dd-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="980dd-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="980dd-127">See also</span></span>



[<span data-ttu-id="980dd-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="980dd-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="980dd-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="980dd-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="980dd-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="980dd-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="980dd-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="980dd-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

