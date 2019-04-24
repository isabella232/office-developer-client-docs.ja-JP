---
title: PidTagRtfSyncTrailingCount 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfSyncTrailingCount
api_type:
- COM
ms.assetid: 3f0e5b24-767e-46f5-bb3d-e9cb82cb935b
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 67093cf456db9df5f9e939bdda9d2e44f248dadc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331235"
---
# <a name="pidtagrtfsynctrailingcount-canonical-property"></a><span data-ttu-id="8dfc0-103">PidTagRtfSyncTrailingCount 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="8dfc0-103">PidTagRtfSyncTrailingCount Canonical Property</span></span>

  
  
<span data-ttu-id="8dfc0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8dfc0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8dfc0-105">メッセージの重要な文字の後に表示される無視できる文字の数を含みます。</span><span class="sxs-lookup"><span data-stu-id="8dfc0-105">Contains a count of the ignorable characters that appear after the significant characters of the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8dfc0-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="8dfc0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8dfc0-107">PR_RTF_SYNC_TRAILING_COUNT</span><span class="sxs-lookup"><span data-stu-id="8dfc0-107">PR_RTF_SYNC_TRAILING_COUNT</span></span>  <br/> |
|<span data-ttu-id="8dfc0-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="8dfc0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8dfc0-109">0x1011</span><span class="sxs-lookup"><span data-stu-id="8dfc0-109">0x1011</span></span>  <br/> |
|<span data-ttu-id="8dfc0-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="8dfc0-110">Data type:</span></span>  <br/> |<span data-ttu-id="8dfc0-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="8dfc0-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="8dfc0-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="8dfc0-112">Area:</span></span>  <br/> |<span data-ttu-id="8dfc0-113">MAPI メッセージ</span><span class="sxs-lookup"><span data-stu-id="8dfc0-113">MAPI message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8dfc0-114">解説</span><span class="sxs-lookup"><span data-stu-id="8dfc0-114">Remarks</span></span>

<span data-ttu-id="8dfc0-115">このプロパティは、リッチテキスト形式 (rft) の補助プロパティです。</span><span class="sxs-lookup"><span data-stu-id="8dfc0-115">This property is a Rich Text Format (RFT) auxiliary property.</span></span> <span data-ttu-id="8dfc0-116">これらのプロパティは、 [rtfsync](rtfsync.md)関数で使用され、クライアントアプリケーションによって直接使用されることを意図したものではありません。</span><span class="sxs-lookup"><span data-stu-id="8dfc0-116">These properties are used by the [RTFSync](rtfsync.md) function and are not intended to be used directly by client applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8dfc0-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="8dfc0-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8dfc0-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="8dfc0-118">Protocol specifications</span></span>

<span data-ttu-id="8dfc0-119">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8dfc0-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8dfc0-120">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="8dfc0-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8dfc0-121">[[OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8dfc0-121">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8dfc0-122">メッセージと添付ファイルオブジェクトをエンコードし、効率的なストリーム表現にデコードします。</span><span class="sxs-lookup"><span data-stu-id="8dfc0-122">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8dfc0-123">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="8dfc0-123">Header files</span></span>

<span data-ttu-id="8dfc0-124">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8dfc0-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="8dfc0-125">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="8dfc0-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="8dfc0-126">Mapitags</span><span class="sxs-lookup"><span data-stu-id="8dfc0-126">Mapitags.h</span></span>
  
> <span data-ttu-id="8dfc0-127">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8dfc0-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8dfc0-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="8dfc0-128">See also</span></span>



[<span data-ttu-id="8dfc0-129">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="8dfc0-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8dfc0-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="8dfc0-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8dfc0-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="8dfc0-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8dfc0-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="8dfc0-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

