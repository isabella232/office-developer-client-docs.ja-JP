---
title: PidTagOriginalMessageClass 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalMessageClass
api_type:
- COM
ms.assetid: 49deb153-03c6-4be2-a3a5-53cca01accba
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 677ba61e3d812909ac4f28f3542f6a79f971ed06
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342624"
---
# <a name="pidtagoriginalmessageclass-canonical-property"></a><span data-ttu-id="78e9c-103">PidTagOriginalMessageClass 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="78e9c-103">PidTagOriginalMessageClass Canonical Property</span></span>

  
  
<span data-ttu-id="78e9c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="78e9c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="78e9c-105">レポートで使用する元のメッセージのクラスが含まれています。</span><span class="sxs-lookup"><span data-stu-id="78e9c-105">Contains the class of the original message for use in a report.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="78e9c-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="78e9c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="78e9c-107">PR_ORIG_MESSAGE_CLASS、PR_ORIG_MESSAGE_CLASS_A、PR_ORIG_MESSAGE_CLASS_W</span><span class="sxs-lookup"><span data-stu-id="78e9c-107">PR_ORIG_MESSAGE_CLASS, PR_ORIG_MESSAGE_CLASS_A, PR_ORIG_MESSAGE_CLASS_W</span></span>  <br/> |
|<span data-ttu-id="78e9c-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="78e9c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="78e9c-109">0x004b</span><span class="sxs-lookup"><span data-stu-id="78e9c-109">0x004B</span></span>  <br/> |
|<span data-ttu-id="78e9c-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="78e9c-110">Data type:</span></span>  <br/> |<span data-ttu-id="78e9c-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="78e9c-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="78e9c-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="78e9c-112">Area:</span></span>  <br/> |<span data-ttu-id="78e9c-113">セキュリティで保護されたメッセージングのプロパティ</span><span class="sxs-lookup"><span data-stu-id="78e9c-113">Secure Messaging Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="78e9c-114">解説</span><span class="sxs-lookup"><span data-stu-id="78e9c-114">Remarks</span></span>

<span data-ttu-id="78e9c-115">これらのプロパティには、レポートが生成されるメッセージの**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) プロパティのコピーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="78e9c-115">These properties contain a copy of the **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property of the message for which the report is being generated.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="78e9c-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="78e9c-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="78e9c-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="78e9c-117">Protocol specifications</span></span>

<span data-ttu-id="78e9c-118">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="78e9c-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="78e9c-119">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="78e9c-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="78e9c-120">[[OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="78e9c-120">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="78e9c-121">メッセージと添付ファイルオブジェクトをエンコードし、効率的なストリーム表現にデコードします。</span><span class="sxs-lookup"><span data-stu-id="78e9c-121">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="78e9c-122">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="78e9c-122">Header files</span></span>

<span data-ttu-id="78e9c-123">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="78e9c-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="78e9c-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="78e9c-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="78e9c-125">Mapitags</span><span class="sxs-lookup"><span data-stu-id="78e9c-125">Mapitags.h</span></span>
  
> <span data-ttu-id="78e9c-126">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="78e9c-126">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="78e9c-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="78e9c-127">See also</span></span>



[<span data-ttu-id="78e9c-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="78e9c-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="78e9c-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="78e9c-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="78e9c-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="78e9c-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="78e9c-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="78e9c-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

