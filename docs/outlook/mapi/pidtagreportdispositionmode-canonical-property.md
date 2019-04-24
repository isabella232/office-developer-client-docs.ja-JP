---
title: PidTagReportDispositionMode 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: 67b3c76a-f6f7-462b-955c-dc7b53e7e7eb
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3d598337a4a66b6345b2f7c827b62a2ccd8af366
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346362"
---
# <a name="pidtagreportdispositionmode-canonical-property"></a><span data-ttu-id="1b884-103">PidTagReportDispositionMode 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1b884-103">PidTagReportDispositionMode Canonical Property</span></span>

  
  
<span data-ttu-id="1b884-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1b884-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1b884-105">受信確認を要求するメッセージの受信のディスポジションを示します。</span><span class="sxs-lookup"><span data-stu-id="1b884-105">Indicates the disposition of the receipt for messages that request receipts.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1b884-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="1b884-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1b884-107">PR_REPORT_DISPOSITION_MODE、PR_REPORT_DISPOSITION_MODE_A、PR_REPORT_DISPOSITION_MODE_W</span><span class="sxs-lookup"><span data-stu-id="1b884-107">PR_REPORT_DISPOSITION_MODE, PR_REPORT_DISPOSITION_MODE_A, PR_REPORT_DISPOSITION_MODE_W</span></span>  <br/> |
|<span data-ttu-id="1b884-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="1b884-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1b884-109">0x0081</span><span class="sxs-lookup"><span data-stu-id="1b884-109">0x0081</span></span>  <br/> |
|<span data-ttu-id="1b884-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="1b884-110">Data type:</span></span>  <br/> |<span data-ttu-id="1b884-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1b884-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="1b884-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="1b884-112">Area:</span></span>  <br/> |<span data-ttu-id="1b884-113">MAPI エンベロープ</span><span class="sxs-lookup"><span data-stu-id="1b884-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1b884-114">解説</span><span class="sxs-lookup"><span data-stu-id="1b884-114">Remarks</span></span>

<span data-ttu-id="1b884-115">このプロパティに指定できる値は、"manual-action/mdn-送信-自動" および "manual-action/mdn-手動で送信する" です。</span><span class="sxs-lookup"><span data-stu-id="1b884-115">The possible values for this property are "manual-action/MDN-sent-automatically" and "manual-action/MDN-sent-manually".</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1b884-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="1b884-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1b884-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="1b884-117">Protocol specifications</span></span>

<span data-ttu-id="1b884-118">[[OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="1b884-118">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="1b884-119">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="1b884-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1b884-120">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="1b884-120">Header files</span></span>

<span data-ttu-id="1b884-121">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1b884-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="1b884-122">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="1b884-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="1b884-123">Mapitags</span><span class="sxs-lookup"><span data-stu-id="1b884-123">Mapitags.h</span></span>
  
> <span data-ttu-id="1b884-124">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="1b884-124">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1b884-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="1b884-125">See also</span></span>



[<span data-ttu-id="1b884-126">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="1b884-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1b884-127">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1b884-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1b884-128">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1b884-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1b884-129">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1b884-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

