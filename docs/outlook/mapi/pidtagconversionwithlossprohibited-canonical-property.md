---
title: PidTagConversionWithLossProhibited 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagConversionWithLossProhibited
api_type:
- HeaderDef
ms.assetid: a18b560a-e054-45b3-946d-6504465db5b7
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e5d9261a9f33d77d52cfd6e448e69a2c1e8df415
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585235"
---
# <a name="pidtagconversionwithlossprohibited-canonical-property"></a><span data-ttu-id="1f26d-103">PidTagConversionWithLossProhibited 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1f26d-103">PidTagConversionWithLossProhibited Canonical Property</span></span>

  
  
<span data-ttu-id="1f26d-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1f26d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1f26d-105">メッセージ転送エージェント (MTA) がメッセージの情報が失われるテキストの変換をすることから禁止されている場合 TRUE が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1f26d-105">Contains TRUE if a message transfer agent (MTA) is prohibited from making message text conversions that lose information.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1f26d-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="1f26d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1f26d-107">PR_CONVERSION_WITH_LOSS_PROHIBITED</span><span class="sxs-lookup"><span data-stu-id="1f26d-107">PR_CONVERSION_WITH_LOSS_PROHIBITED</span></span>  <br/> |
|<span data-ttu-id="1f26d-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="1f26d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1f26d-109">0x000D</span><span class="sxs-lookup"><span data-stu-id="1f26d-109">0x000D</span></span>  <br/> |
|<span data-ttu-id="1f26d-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="1f26d-110">Data type:</span></span>  <br/> |<span data-ttu-id="1f26d-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="1f26d-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="1f26d-112">領域:</span><span class="sxs-lookup"><span data-stu-id="1f26d-112">Area:</span></span>  <br/> |<span data-ttu-id="1f26d-113">一般的な構成</span><span class="sxs-lookup"><span data-stu-id="1f26d-113">General configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1f26d-114">注釈</span><span class="sxs-lookup"><span data-stu-id="1f26d-114">Remarks</span></span>

<span data-ttu-id="1f26d-115">禁止されている変換の種類の例が、「損失」のマッピング Unicode (1 文字あたり 2 バイト) からシングル バイト文字セットです。</span><span class="sxs-lookup"><span data-stu-id="1f26d-115">An example of the type of conversion being prohibited is the "lossy" mapping from Unicode (two bytes per character) to a single-byte character set.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1f26d-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="1f26d-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="1f26d-117">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="1f26d-117">Header files</span></span>

<span data-ttu-id="1f26d-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1f26d-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="1f26d-119">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="1f26d-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="1f26d-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1f26d-120">Mapitags.h</span></span>
  
> <span data-ttu-id="1f26d-121">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1f26d-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1f26d-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="1f26d-122">See also</span></span>



[<span data-ttu-id="1f26d-123">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="1f26d-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1f26d-124">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="1f26d-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1f26d-125">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1f26d-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1f26d-126">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1f26d-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

