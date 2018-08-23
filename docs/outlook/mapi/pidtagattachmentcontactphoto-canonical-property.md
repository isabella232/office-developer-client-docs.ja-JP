---
title: PidTagAttachmentContactPhoto 標準プロパティ
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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 332b6b857921c8f72837dc115805084efd8c5a19
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574749"
---
# <a name="pidtagattachmentcontactphoto-canonical-property"></a><span data-ttu-id="5f378-103">PidTagAttachmentContactPhoto 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5f378-103">PidTagAttachmentContactPhoto Canonical Property</span></span>

  
  
<span data-ttu-id="5f378-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5f378-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5f378-105">連絡先の写真の添付ファイルの存在を示しています。</span><span class="sxs-lookup"><span data-stu-id="5f378-105">Indicates the existence of a photo attachment for a contact.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5f378-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="5f378-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5f378-107">PR_ATTACHMENT_CONTACTPHOTO</span><span class="sxs-lookup"><span data-stu-id="5f378-107">PR_ATTACHMENT_CONTACTPHOTO</span></span>  <br/> |
|<span data-ttu-id="5f378-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="5f378-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5f378-109">0x7FFF</span><span class="sxs-lookup"><span data-stu-id="5f378-109">0x7FFF</span></span>  <br/> |
|<span data-ttu-id="5f378-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="5f378-110">Data type:</span></span>  <br/> |<span data-ttu-id="5f378-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="5f378-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="5f378-112">領域:</span><span class="sxs-lookup"><span data-stu-id="5f378-112">Area:</span></span>  <br/> |<span data-ttu-id="5f378-113">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="5f378-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5f378-114">注釈</span><span class="sxs-lookup"><span data-stu-id="5f378-114">Remarks</span></span>

<span data-ttu-id="5f378-115">このプロパティの値を true に設定する必要があり、のみが表示されます、特定の連絡先オブジェクトの 1 つの添付ファイルです。</span><span class="sxs-lookup"><span data-stu-id="5f378-115">This property's value must be set to TRUE, and there should only be one attachment on a given Contact object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5f378-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="5f378-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5f378-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="5f378-117">Protocol specifications</span></span>

<span data-ttu-id="5f378-118">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5f378-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5f378-119">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="5f378-119">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5f378-120">[[MS OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5f378-120">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5f378-121">プロパティは、連絡先、個人用配布リストの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="5f378-121">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5f378-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="5f378-122">Header files</span></span>

<span data-ttu-id="5f378-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5f378-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="5f378-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="5f378-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="5f378-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5f378-125">Mapitags.h</span></span>
  
> <span data-ttu-id="5f378-126">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="5f378-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5f378-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="5f378-127">See also</span></span>



[<span data-ttu-id="5f378-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="5f378-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5f378-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="5f378-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5f378-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="5f378-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5f378-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="5f378-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

