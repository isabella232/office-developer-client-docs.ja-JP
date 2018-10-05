---
title: PidLidHasPicture 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidHasPicture
api_type:
- COM
ms.assetid: c3bea11c-3197-4060-8672-f1b4bf352112
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3aef2fc1038751c9ad6fb97cf347c2dcab114fda
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399173"
---
# <a name="pidlidhaspicture-canonical-property"></a><span data-ttu-id="5a37a-103">PidLidHasPicture 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5a37a-103">PidLidHasPicture Canonical Property</span></span>

  
  
<span data-ttu-id="5a37a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5a37a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5a37a-105">連絡先の写真の添付ファイルが存在するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="5a37a-105">Specifies whether a photo attachment exists for a contact.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5a37a-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="5a37a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5a37a-107">dispidHasPicture</span><span class="sxs-lookup"><span data-stu-id="5a37a-107">dispidHasPicture</span></span>  <br/> |
|<span data-ttu-id="5a37a-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="5a37a-108">Property set:</span></span>  <br/> |<span data-ttu-id="5a37a-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="5a37a-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="5a37a-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="5a37a-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="5a37a-111">0x00008015</span><span class="sxs-lookup"><span data-stu-id="5a37a-111">0x00008015</span></span>  <br/> |
|<span data-ttu-id="5a37a-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="5a37a-112">Data type:</span></span>  <br/> |<span data-ttu-id="5a37a-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="5a37a-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="5a37a-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="5a37a-114">Area:</span></span>  <br/> |<span data-ttu-id="5a37a-115">Contact</span><span class="sxs-lookup"><span data-stu-id="5a37a-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5a37a-116">備考</span><span class="sxs-lookup"><span data-stu-id="5a37a-116">Remarks</span></span>

<span data-ttu-id="5a37a-117">このプロパティが存在し、TRUE に設定されて場合、連絡先の添付ファイル テーブルには、 **PR_ATTACHMENT_CONTACTPHOTO** ([PidTagAttachmentContactPhoto](pidtagattachmentcontactphoto-canonical-property.md)) プロパティが TRUE に設定の添付ファイルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="5a37a-117">If this property exists and is set to TRUE, the contact's attachment table contains an attachment with the **PR_ATTACHMENT_CONTACTPHOTO** ([PidTagAttachmentContactPhoto](pidtagattachmentcontactphoto-canonical-property.md)) property set to TRUE.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5a37a-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="5a37a-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5a37a-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="5a37a-119">Protocol specifications</span></span>

<span data-ttu-id="5a37a-120">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5a37a-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5a37a-121">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="5a37a-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5a37a-122">[[MS OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5a37a-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5a37a-123">プロパティは、連絡先、個人用配布リストの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="5a37a-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5a37a-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="5a37a-124">Header files</span></span>

<span data-ttu-id="5a37a-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5a37a-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="5a37a-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="5a37a-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5a37a-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="5a37a-127">See also</span></span>



[<span data-ttu-id="5a37a-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="5a37a-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5a37a-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="5a37a-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5a37a-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="5a37a-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5a37a-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="5a37a-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

