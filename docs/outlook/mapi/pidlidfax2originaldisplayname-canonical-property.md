---
title: PidLidFax2OriginalDisplayName の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: d009118b8e4c11f70e9545302e2fd7ab9b43f00e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801931"
---
# <a name="pidlidfax2originaldisplayname-canonical-property"></a><span data-ttu-id="01867-103">PidLidFax2OriginalDisplayName の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="01867-103">PidLidFax2OriginalDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="01867-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="01867-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="01867-105">連絡先の自宅の fax アドレスの元の表示名を指定します。</span><span class="sxs-lookup"><span data-stu-id="01867-105">Specifies the original display name of the contact's home fax address.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="01867-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="01867-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="01867-107">dispidFax2OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="01867-107">dispidFax2OriginalDisplayName</span></span>  <br/> |
|<span data-ttu-id="01867-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="01867-108">Property set:</span></span>  <br/> |<span data-ttu-id="01867-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="01867-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="01867-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="01867-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="01867-111">0x000080C4</span><span class="sxs-lookup"><span data-stu-id="01867-111">0x000080C4</span></span>  <br/> |
|<span data-ttu-id="01867-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="01867-112">Data type:</span></span>  <br/> |<span data-ttu-id="01867-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="01867-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="01867-114">領域:</span><span class="sxs-lookup"><span data-stu-id="01867-114">Area:</span></span>  <br/> |<span data-ttu-id="01867-115">連絡先</span><span class="sxs-lookup"><span data-stu-id="01867-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="01867-116">備考</span><span class="sxs-lookup"><span data-stu-id="01867-116">Remarks</span></span>

<span data-ttu-id="01867-117">このプロパティは、存在する場合、必要があります設定する**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) のプロパティと同じ値にします。</span><span class="sxs-lookup"><span data-stu-id="01867-117">This property, if present, must be set to the same value as the **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="01867-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="01867-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="01867-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="01867-119">Protocol specifications</span></span>

<span data-ttu-id="01867-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="01867-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="01867-121">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="01867-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="01867-122">[[MS OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="01867-122">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="01867-123">プロパティは、連絡先、個人用配布リストの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="01867-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="01867-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="01867-124">Header files</span></span>

<span data-ttu-id="01867-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="01867-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="01867-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="01867-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="01867-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="01867-127">See also</span></span>



[<span data-ttu-id="01867-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="01867-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="01867-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="01867-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="01867-130">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="01867-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="01867-131">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="01867-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

