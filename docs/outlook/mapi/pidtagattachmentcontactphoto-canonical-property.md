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
ms.openlocfilehash: 5d61289349306b763d13a9a2111c2cd02ff3937e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345767"
---
# <a name="pidtagattachmentcontactphoto-canonical-property"></a><span data-ttu-id="3c0d7-103">PidTagAttachmentContactPhoto 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="3c0d7-103">PidTagAttachmentContactPhoto Canonical Property</span></span>

  
  
<span data-ttu-id="3c0d7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3c0d7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3c0d7-105">連絡先の写真の添付ファイルが存在することを示します。</span><span class="sxs-lookup"><span data-stu-id="3c0d7-105">Indicates the existence of a photo attachment for a contact.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3c0d7-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="3c0d7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3c0d7-107">PR_ATTACHMENT_CONTACTPHOTO</span><span class="sxs-lookup"><span data-stu-id="3c0d7-107">PR_ATTACHMENT_CONTACTPHOTO</span></span>  <br/> |
|<span data-ttu-id="3c0d7-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="3c0d7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3c0d7-109">~</span><span class="sxs-lookup"><span data-stu-id="3c0d7-109">0x7FFF</span></span>  <br/> |
|<span data-ttu-id="3c0d7-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="3c0d7-110">Data type:</span></span>  <br/> |<span data-ttu-id="3c0d7-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="3c0d7-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="3c0d7-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="3c0d7-112">Area:</span></span>  <br/> |<span data-ttu-id="3c0d7-113">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="3c0d7-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3c0d7-114">解説</span><span class="sxs-lookup"><span data-stu-id="3c0d7-114">Remarks</span></span>

<span data-ttu-id="3c0d7-115">このプロパティの値は TRUE に設定する必要があり、指定された連絡先オブジェクトには添付ファイルが1つだけである必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c0d7-115">This property's value must be set to TRUE, and there should only be one attachment on a given Contact object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3c0d7-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="3c0d7-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3c0d7-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="3c0d7-117">Protocol specifications</span></span>

<span data-ttu-id="3c0d7-118">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3c0d7-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3c0d7-119">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="3c0d7-119">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3c0d7-120">[[OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3c0d7-120">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3c0d7-121">連絡先および個人用配布リストに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="3c0d7-121">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3c0d7-122">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="3c0d7-122">Header files</span></span>

<span data-ttu-id="3c0d7-123">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3c0d7-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="3c0d7-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="3c0d7-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="3c0d7-125">Mapitags</span><span class="sxs-lookup"><span data-stu-id="3c0d7-125">Mapitags.h</span></span>
  
> <span data-ttu-id="3c0d7-126">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="3c0d7-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3c0d7-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="3c0d7-127">See also</span></span>



[<span data-ttu-id="3c0d7-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="3c0d7-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3c0d7-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="3c0d7-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3c0d7-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="3c0d7-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3c0d7-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="3c0d7-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

