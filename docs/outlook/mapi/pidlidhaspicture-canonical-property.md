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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3aef2fc1038751c9ad6fb97cf347c2dcab114fda
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357751"
---
# <a name="pidlidhaspicture-canonical-property"></a><span data-ttu-id="bcaaa-103">PidLidHasPicture 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="bcaaa-103">PidLidHasPicture Canonical Property</span></span>

  
  
<span data-ttu-id="bcaaa-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bcaaa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bcaaa-105">連絡先に写真添付ファイルが存在するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="bcaaa-105">Specifies whether a photo attachment exists for a contact.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bcaaa-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="bcaaa-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bcaaa-107">dispidHasPicture</span><span class="sxs-lookup"><span data-stu-id="bcaaa-107">dispidHasPicture</span></span>  <br/> |
|<span data-ttu-id="bcaaa-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="bcaaa-108">Property set:</span></span>  <br/> |<span data-ttu-id="bcaaa-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="bcaaa-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="bcaaa-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="bcaaa-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="bcaaa-111">0x00008015</span><span class="sxs-lookup"><span data-stu-id="bcaaa-111">0x00008015</span></span>  <br/> |
|<span data-ttu-id="bcaaa-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="bcaaa-112">Data type:</span></span>  <br/> |<span data-ttu-id="bcaaa-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="bcaaa-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="bcaaa-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="bcaaa-114">Area:</span></span>  <br/> |<span data-ttu-id="bcaaa-115">Contact</span><span class="sxs-lookup"><span data-stu-id="bcaaa-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bcaaa-116">注釈</span><span class="sxs-lookup"><span data-stu-id="bcaaa-116">Remarks</span></span>

<span data-ttu-id="bcaaa-117">このプロパティが存在し、TRUE に設定されている場合、連絡先の添付ファイル テーブルには **、PR_ATTACHMENT_CONTACTPHOTO** ([PidTagAttachmentContactPhoto](pidtagattachmentcontactphoto-canonical-property.md)) プロパティが TRUE に設定された添付ファイルが含まれる。</span><span class="sxs-lookup"><span data-stu-id="bcaaa-117">If this property exists and is set to TRUE, the contact's attachment table contains an attachment with the **PR_ATTACHMENT_CONTACTPHOTO** ([PidTagAttachmentContactPhoto](pidtagattachmentcontactphoto-canonical-property.md)) property set to TRUE.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bcaaa-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="bcaaa-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bcaaa-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="bcaaa-119">Protocol specifications</span></span>

<span data-ttu-id="bcaaa-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bcaaa-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bcaaa-121">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="bcaaa-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bcaaa-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bcaaa-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bcaaa-123">連絡先と個人用配布リストで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="bcaaa-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bcaaa-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="bcaaa-124">Header files</span></span>

<span data-ttu-id="bcaaa-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bcaaa-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="bcaaa-126">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="bcaaa-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bcaaa-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="bcaaa-127">See also</span></span>



[<span data-ttu-id="bcaaa-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="bcaaa-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bcaaa-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="bcaaa-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bcaaa-130">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="bcaaa-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bcaaa-131">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="bcaaa-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

