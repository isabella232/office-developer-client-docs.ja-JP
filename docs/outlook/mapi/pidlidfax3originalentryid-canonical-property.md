---
title: PidLidFax3OriginalEntryId の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 76b53e208f95aa2d87e3d47cfc5beb69075d376f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801966"
---
# <a name="pidlidfax3originalentryid-canonical-property"></a><span data-ttu-id="705d6-103">PidLidFax3OriginalEntryId の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="705d6-103">PidLidFax3OriginalEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="705d6-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="705d6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="705d6-105">連絡先の元のエントリ Id はの他の fax アドレスを指定します。</span><span class="sxs-lookup"><span data-stu-id="705d6-105">Specifies the original EntryID of the contact's other fax address.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="705d6-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="705d6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="705d6-107">dispidFax3OriginalEntryID</span><span class="sxs-lookup"><span data-stu-id="705d6-107">dispidFax3OriginalEntryID</span></span>  <br/> |
|<span data-ttu-id="705d6-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="705d6-108">Property set:</span></span>  <br/> |<span data-ttu-id="705d6-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="705d6-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="705d6-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="705d6-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="705d6-111">0x000080D5</span><span class="sxs-lookup"><span data-stu-id="705d6-111">0x000080D5</span></span>  <br/> |
|<span data-ttu-id="705d6-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="705d6-112">Data type:</span></span>  <br/> |<span data-ttu-id="705d6-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="705d6-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="705d6-114">領域:</span><span class="sxs-lookup"><span data-stu-id="705d6-114">Area:</span></span>  <br/> |<span data-ttu-id="705d6-115">連絡先</span><span class="sxs-lookup"><span data-stu-id="705d6-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="705d6-116">備考</span><span class="sxs-lookup"><span data-stu-id="705d6-116">Remarks</span></span>

<span data-ttu-id="705d6-117">このプロパティは、存在する場合がこの fax アドレスに対応する 1 回限りのエントリ Id を指定しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="705d6-117">This property, if present, must specify the one-off EntryId that corresponds to this fax address.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="705d6-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="705d6-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="705d6-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="705d6-119">Protocol specifications</span></span>

<span data-ttu-id="705d6-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="705d6-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="705d6-121">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="705d6-121">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="705d6-122">[[MS OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="705d6-122">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="705d6-123">プロパティは、連絡先、個人用配布リストの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="705d6-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="705d6-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="705d6-124">Header files</span></span>

<span data-ttu-id="705d6-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="705d6-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="705d6-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="705d6-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="705d6-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="705d6-127">See also</span></span>



[<span data-ttu-id="705d6-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="705d6-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="705d6-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="705d6-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="705d6-130">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="705d6-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="705d6-131">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="705d6-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

