---
title: PidLidHasPicture の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 74a54db3ebb55c178fd5f8b7317bb27c83a47311
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802004"
---
# <a name="pidlidhaspicture-canonical-property"></a><span data-ttu-id="cf091-103">PidLidHasPicture の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="cf091-103">PidLidHasPicture Canonical Property</span></span>

  
  
<span data-ttu-id="cf091-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cf091-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cf091-105">連絡先の写真の添付ファイルが存在するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="cf091-105">Specifies whether a photo attachment exists for a contact.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cf091-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="cf091-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cf091-107">dispidHasPicture</span><span class="sxs-lookup"><span data-stu-id="cf091-107">dispidHasPicture</span></span>  <br/> |
|<span data-ttu-id="cf091-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="cf091-108">Property set:</span></span>  <br/> |<span data-ttu-id="cf091-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="cf091-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="cf091-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="cf091-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="cf091-111">0x00008015</span><span class="sxs-lookup"><span data-stu-id="cf091-111">0x00008015</span></span>  <br/> |
|<span data-ttu-id="cf091-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="cf091-112">Data type:</span></span>  <br/> |<span data-ttu-id="cf091-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="cf091-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="cf091-114">領域:</span><span class="sxs-lookup"><span data-stu-id="cf091-114">Area:</span></span>  <br/> |<span data-ttu-id="cf091-115">連絡先</span><span class="sxs-lookup"><span data-stu-id="cf091-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cf091-116">備考</span><span class="sxs-lookup"><span data-stu-id="cf091-116">Remarks</span></span>

<span data-ttu-id="cf091-117">このプロパティが存在し、TRUE に設定されて場合、連絡先の添付ファイル テーブルには、 **PR_ATTACHMENT_CONTACTPHOTO** ([PidTagAttachmentContactPhoto](pidtagattachmentcontactphoto-canonical-property.md)) プロパティが TRUE に設定の添付ファイルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="cf091-117">If this property exists and is set to TRUE, the contact's attachment table contains an attachment with the **PR_ATTACHMENT_CONTACTPHOTO** ([PidTagAttachmentContactPhoto](pidtagattachmentcontactphoto-canonical-property.md)) property set to TRUE.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="cf091-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="cf091-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cf091-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="cf091-119">Protocol specifications</span></span>

<span data-ttu-id="cf091-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cf091-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cf091-121">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="cf091-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cf091-122">[[MS OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cf091-122">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cf091-123">プロパティは、連絡先、個人用配布リストの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="cf091-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cf091-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="cf091-124">Header files</span></span>

<span data-ttu-id="cf091-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cf091-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="cf091-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="cf091-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cf091-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="cf091-127">See also</span></span>



[<span data-ttu-id="cf091-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="cf091-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cf091-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="cf091-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cf091-130">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="cf091-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cf091-131">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="cf091-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

