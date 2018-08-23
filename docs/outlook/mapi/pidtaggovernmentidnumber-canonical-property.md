---
title: PidTagGovernmentIdNumber 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagGovernmentIdNumber
api_type:
- HeaderDef
ms.assetid: fa265d37-a1ea-4812-8fe9-21dac374cd7c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ab2c4caf74da8bce143e6b1f4fa6fd2946e37de3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593208"
---
# <a name="pidtaggovernmentidnumber-canonical-property"></a><span data-ttu-id="c4079-103">PidTagGovernmentIdNumber 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c4079-103">PidTagGovernmentIdNumber Canonical Property</span></span>

  
  
<span data-ttu-id="c4079-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c4079-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c4079-105">受信者の自治体 id が含まれています。</span><span class="sxs-lookup"><span data-stu-id="c4079-105">Contains a government identifier for the recipient.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c4079-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="c4079-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c4079-107">PR_GOVERNMENT_ID_NUMBER、PR_GOVERNMENT_ID_NUMBER_A、PR_GOVERNMENT_ID_NUMBER_W</span><span class="sxs-lookup"><span data-stu-id="c4079-107">PR_GOVERNMENT_ID_NUMBER, PR_GOVERNMENT_ID_NUMBER_A, PR_GOVERNMENT_ID_NUMBER_W</span></span>  <br/> |
|<span data-ttu-id="c4079-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="c4079-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c4079-109">0x3A07</span><span class="sxs-lookup"><span data-stu-id="c4079-109">0x3A07</span></span>  <br/> |
|<span data-ttu-id="c4079-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="c4079-110">Data type:</span></span>  <br/> |<span data-ttu-id="c4079-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c4079-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="c4079-112">領域:</span><span class="sxs-lookup"><span data-stu-id="c4079-112">Area:</span></span>  <br/> |<span data-ttu-id="c4079-113">MAPI メール ユーザー</span><span class="sxs-lookup"><span data-stu-id="c4079-113">MAPI mail user</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c4079-114">注釈</span><span class="sxs-lookup"><span data-stu-id="c4079-114">Remarks</span></span>

<span data-ttu-id="c4079-115">これらのプロパティでは、識別を提供し、受信者に関する情報にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="c4079-115">These properties provide identification and access information about a recipient.</span></span> <span data-ttu-id="c4079-116">受信者と受信者の組織によって定義されます。</span><span class="sxs-lookup"><span data-stu-id="c4079-116">They are defined by the recipient and the recipient's organization.</span></span> 
  
<span data-ttu-id="c4079-117">これらのプロパティは通常、パスポート番号、市民の数、または社会保障番号などの納税者番号に設定されます。</span><span class="sxs-lookup"><span data-stu-id="c4079-117">These properties are commonly set to a passport number, citizen number, or taxpayer number such as a Social Security number.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c4079-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="c4079-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c4079-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="c4079-119">Protocol specifications</span></span>

<span data-ttu-id="c4079-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c4079-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c4079-121">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="c4079-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c4079-122">[[MS OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c4079-122">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c4079-123">プロパティは、連絡先、個人用配布リストの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="c4079-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="c4079-124">[[MS OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c4079-124">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c4079-125">プロパティとユーザー、連絡先、グループ、およびリソースのリストの操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="c4079-125">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c4079-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="c4079-126">Header files</span></span>

<span data-ttu-id="c4079-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c4079-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="c4079-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="c4079-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="c4079-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c4079-129">Mapitags.h</span></span>
  
> <span data-ttu-id="c4079-130">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="c4079-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c4079-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="c4079-131">See also</span></span>



[<span data-ttu-id="c4079-132">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="c4079-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c4079-133">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="c4079-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c4079-134">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="c4079-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c4079-135">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="c4079-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

