---
title: PidTagRtfSyncBodyCrc 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfSyncBodyCrc
api_type:
- COM
ms.assetid: 95db4837-400f-476f-b313-60e8baa1c6d1
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 85ac61d968243283e5ad9283730941adcd87cd5e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357870"
---
# <a name="pidtagrtfsyncbodycrc-canonical-property"></a><span data-ttu-id="7509c-103">PidTagRtfSyncBodyCrc 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="7509c-103">PidTagRtfSyncBodyCrc Canonical Property</span></span>

  
  
<span data-ttu-id="7509c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7509c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7509c-105">メッセージテキストに対して計算された巡回冗長検査 (CRC) を含みます。</span><span class="sxs-lookup"><span data-stu-id="7509c-105">Contains the cyclical redundancy check (CRC) computed for the message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7509c-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="7509c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7509c-107">PR_RTF_SYNC_BODY_CRC</span><span class="sxs-lookup"><span data-stu-id="7509c-107">PR_RTF_SYNC_BODY_CRC</span></span>  <br/> |
|<span data-ttu-id="7509c-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="7509c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7509c-109">0x1006</span><span class="sxs-lookup"><span data-stu-id="7509c-109">0x1006</span></span>  <br/> |
|<span data-ttu-id="7509c-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="7509c-110">Data type:</span></span>  <br/> |<span data-ttu-id="7509c-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="7509c-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="7509c-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="7509c-112">Area:</span></span>  <br/> |<span data-ttu-id="7509c-113">MAPI メッセージ</span><span class="sxs-lookup"><span data-stu-id="7509c-113">MAPI message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7509c-114">解説</span><span class="sxs-lookup"><span data-stu-id="7509c-114">Remarks</span></span>

<span data-ttu-id="7509c-115">[rtfsync](rtfsync.md)関数は、メッセージに対して有意と見なされる文字のみを使用して CRC を計算します。</span><span class="sxs-lookup"><span data-stu-id="7509c-115">The [RTFSync](rtfsync.md) function computes the CRC by using only the characters that it considers to be significant to the message.</span></span> <span data-ttu-id="7509c-116">たとえば、一部の空白文字とその他の無視できる文字は、CRC で省略されています。</span><span class="sxs-lookup"><span data-stu-id="7509c-116">For example, some white space and other ignorable characters are omitted from the CRC.</span></span> 
  
<span data-ttu-id="7509c-117">このプロパティは、リッチテキスト形式 (RTF) の補助プロパティです。</span><span class="sxs-lookup"><span data-stu-id="7509c-117">This property is a Rich Text Format (RTF) auxiliary property.</span></span> <span data-ttu-id="7509c-118">これらのプロパティは、 **rtfsync**関数で使用され、クライアントアプリケーションによって直接使用されることを意図したものではありません。</span><span class="sxs-lookup"><span data-stu-id="7509c-118">These properties are used by the **RTFSync** function and are not intended to be used directly by client applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="7509c-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="7509c-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7509c-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="7509c-120">Protocol specifications</span></span>

<span data-ttu-id="7509c-121">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7509c-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7509c-122">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="7509c-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7509c-123">[[OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7509c-123">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7509c-124">メッセージと添付ファイルオブジェクトをエンコードし、効率的なストリーム表現にデコードします。</span><span class="sxs-lookup"><span data-stu-id="7509c-124">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7509c-125">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="7509c-125">Header files</span></span>

<span data-ttu-id="7509c-126">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7509c-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="7509c-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="7509c-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="7509c-128">Mapitags</span><span class="sxs-lookup"><span data-stu-id="7509c-128">Mapitags.h</span></span>
  
> <span data-ttu-id="7509c-129">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7509c-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7509c-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="7509c-130">See also</span></span>



[<span data-ttu-id="7509c-131">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="7509c-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7509c-132">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="7509c-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7509c-133">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="7509c-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7509c-134">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="7509c-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

