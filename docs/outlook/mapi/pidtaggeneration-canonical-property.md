---
title: PidTagGeneration の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagGeneration
api_type:
- HeaderDef
ms.assetid: 81c2e479-84a1-42ba-a9ce-25e3fc8d80cb
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 4f13aa14569daeb60271ea6d8645af6f6fe3bcd8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802795"
---
# <a name="pidtaggeneration-canonical-property"></a><span data-ttu-id="1281a-103">PidTagGeneration の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="1281a-103">PidTagGeneration Canonical Property</span></span>

  
  
<span data-ttu-id="1281a-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1281a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1281a-105">受信者の完全な名前を次世代の省略形が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1281a-105">Contains a generational abbreviation that follows the full name of the recipient.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1281a-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="1281a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1281a-107">PR_GENERATION、PR_GENERATION_A、PR_GENERATION_W</span><span class="sxs-lookup"><span data-stu-id="1281a-107">PR_GENERATION, PR_GENERATION_A, PR_GENERATION_W</span></span>  <br/> |
|<span data-ttu-id="1281a-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="1281a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1281a-109">0x3A05</span><span class="sxs-lookup"><span data-stu-id="1281a-109">0x3A05</span></span>  <br/> |
|<span data-ttu-id="1281a-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="1281a-110">Data type:</span></span>  <br/> |<span data-ttu-id="1281a-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1281a-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="1281a-112">領域:</span><span class="sxs-lookup"><span data-stu-id="1281a-112">Area:</span></span>  <br/> |<span data-ttu-id="1281a-113">MAPI メール ユーザー</span><span class="sxs-lookup"><span data-stu-id="1281a-113">MAPI mail user</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1281a-114">備考</span><span class="sxs-lookup"><span data-stu-id="1281a-114">Remarks</span></span>

<span data-ttu-id="1281a-115">これらのプロパティでは、識別を提供し、受信者に関する情報にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="1281a-115">These properties provide identification and access information about a recipient.</span></span> <span data-ttu-id="1281a-116">受信者とその構造によって定義されます。</span><span class="sxs-lookup"><span data-stu-id="1281a-116">They are defined by the recipient and their organization.</span></span> 
  
<span data-ttu-id="1281a-117">共通の値は、ジュニア、シニア、および III。</span><span class="sxs-lookup"><span data-stu-id="1281a-117">Common values include Jr., Sr., and III.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1281a-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="1281a-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1281a-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="1281a-119">Protocol specifications</span></span>

<span data-ttu-id="1281a-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1281a-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1281a-121">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="1281a-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1281a-122">[[MS OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1281a-122">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1281a-123">プロパティは、連絡先、個人用配布リストの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="1281a-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="1281a-124">[[MS OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1281a-124">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1281a-125">プロパティとユーザー、連絡先、グループ、およびリソースのリストの操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="1281a-125">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1281a-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="1281a-126">Header files</span></span>

<span data-ttu-id="1281a-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1281a-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="1281a-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="1281a-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="1281a-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1281a-129">Mapitags.h</span></span>
  
> <span data-ttu-id="1281a-130">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1281a-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1281a-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="1281a-131">See also</span></span>



[<span data-ttu-id="1281a-132">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="1281a-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1281a-133">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="1281a-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1281a-134">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="1281a-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1281a-135">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="1281a-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

