---
title: PidTagAttachmentContactPhoto の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachmentContactPhoto
api_type:
- HeaderDef
ms.assetid: ea5b77b7-8440-4e54-abd2-c475138c8f63
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: ae25bd32819de06e91ccb20ada7c7a14b723cd65
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802473"
---
# <a name="pidtagattachmentcontactphoto-canonical-property"></a><span data-ttu-id="400d6-103">PidTagAttachmentContactPhoto の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="400d6-103">PidTagAttachmentContactPhoto Canonical Property</span></span>

  
  
<span data-ttu-id="400d6-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="400d6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="400d6-105">連絡先の写真の添付ファイルの存在を示しています。</span><span class="sxs-lookup"><span data-stu-id="400d6-105">Indicates the existence of a photo attachment for a contact.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="400d6-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="400d6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="400d6-107">PR_ATTACHMENT_CONTACTPHOTO</span><span class="sxs-lookup"><span data-stu-id="400d6-107">PR_ATTACHMENT_CONTACTPHOTO</span></span>  <br/> |
|<span data-ttu-id="400d6-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="400d6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="400d6-109">0x7FFF</span><span class="sxs-lookup"><span data-stu-id="400d6-109">0x7FFF</span></span>  <br/> |
|<span data-ttu-id="400d6-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="400d6-110">Data type:</span></span>  <br/> |<span data-ttu-id="400d6-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="400d6-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="400d6-112">領域:</span><span class="sxs-lookup"><span data-stu-id="400d6-112">Area:</span></span>  <br/> |<span data-ttu-id="400d6-113">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="400d6-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="400d6-114">備考</span><span class="sxs-lookup"><span data-stu-id="400d6-114">Remarks</span></span>

<span data-ttu-id="400d6-115">このプロパティの値を true に設定する必要があり、のみが表示されます、特定の連絡先オブジェクトの 1 つの添付ファイルです。</span><span class="sxs-lookup"><span data-stu-id="400d6-115">This property's value must be set to TRUE, and there should only be one attachment on a given Contact object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="400d6-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="400d6-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="400d6-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="400d6-117">Protocol specifications</span></span>

<span data-ttu-id="400d6-118">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="400d6-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="400d6-119">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="400d6-119">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="400d6-120">[[MS OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="400d6-120">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="400d6-121">プロパティは、連絡先、個人用配布リストの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="400d6-121">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="400d6-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="400d6-122">Header files</span></span>

<span data-ttu-id="400d6-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="400d6-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="400d6-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="400d6-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="400d6-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="400d6-125">Mapitags.h</span></span>
  
> <span data-ttu-id="400d6-126">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="400d6-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="400d6-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="400d6-127">See also</span></span>



[<span data-ttu-id="400d6-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="400d6-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="400d6-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="400d6-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="400d6-130">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="400d6-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="400d6-131">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="400d6-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

