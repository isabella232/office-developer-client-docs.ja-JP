---
title: PidLidFax2OriginalEntryId の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: d8a7082f76af761cd04a9c190324b7e6cf6e54fb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801939"
---
# <a name="pidlidfax2originalentryid-canonical-property"></a><span data-ttu-id="c2d11-103">PidLidFax2OriginalEntryId の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="c2d11-103">PidLidFax2OriginalEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="c2d11-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c2d11-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c2d11-105">連絡先の自宅の fax アドレスの元のエントリ Id を指定します。</span><span class="sxs-lookup"><span data-stu-id="c2d11-105">Specifies the original EntryID of the contact's home fax address.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c2d11-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="c2d11-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c2d11-107">dispidFax2OriginalEntryID</span><span class="sxs-lookup"><span data-stu-id="c2d11-107">dispidFax2OriginalEntryID</span></span>  <br/> |
|<span data-ttu-id="c2d11-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="c2d11-108">Property set:</span></span>  <br/> |<span data-ttu-id="c2d11-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="c2d11-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="c2d11-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="c2d11-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="c2d11-111">0x000080C5</span><span class="sxs-lookup"><span data-stu-id="c2d11-111">0x000080C5</span></span>  <br/> |
|<span data-ttu-id="c2d11-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="c2d11-112">Data type:</span></span>  <br/> |<span data-ttu-id="c2d11-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="c2d11-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="c2d11-114">領域:</span><span class="sxs-lookup"><span data-stu-id="c2d11-114">Area:</span></span>  <br/> |<span data-ttu-id="c2d11-115">連絡先</span><span class="sxs-lookup"><span data-stu-id="c2d11-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c2d11-116">備考</span><span class="sxs-lookup"><span data-stu-id="c2d11-116">Remarks</span></span>

<span data-ttu-id="c2d11-117">このプロパティは、存在する場合がこの fax アドレスに対応する 1 回限りのエントリ Id を指定しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="c2d11-117">This property, if present, must specify the one-off EntryId that corresponds to this fax address.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c2d11-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="c2d11-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c2d11-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="c2d11-119">Protocol specifications</span></span>

<span data-ttu-id="c2d11-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c2d11-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c2d11-121">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="c2d11-121">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c2d11-122">[[MS OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c2d11-122">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c2d11-123">プロパティは、連絡先、個人用配布リストの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="c2d11-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c2d11-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="c2d11-124">Header files</span></span>

<span data-ttu-id="c2d11-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c2d11-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="c2d11-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="c2d11-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c2d11-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="c2d11-127">See also</span></span>



[<span data-ttu-id="c2d11-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="c2d11-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c2d11-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="c2d11-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c2d11-130">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="c2d11-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c2d11-131">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="c2d11-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

