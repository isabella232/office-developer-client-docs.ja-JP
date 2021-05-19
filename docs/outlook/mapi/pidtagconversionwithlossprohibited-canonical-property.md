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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 972df747e0ee459996b9b4da5732be1490fbd08a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417127"
---
# <a name="pidtagconversionwithlossprohibited-canonical-property"></a><span data-ttu-id="06402-103">PidTagConversionWithLossProhibited 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="06402-103">PidTagConversionWithLossProhibited Canonical Property</span></span>

  
  
<span data-ttu-id="06402-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="06402-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="06402-105">メッセージ転送エージェント (MTA) が情報を失うメッセージ テキスト変換を禁止されている場合は TRUE を含む。</span><span class="sxs-lookup"><span data-stu-id="06402-105">Contains TRUE if a message transfer agent (MTA) is prohibited from making message text conversions that lose information.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="06402-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="06402-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="06402-107">PR_CONVERSION_WITH_LOSS_PROHIBITED</span><span class="sxs-lookup"><span data-stu-id="06402-107">PR_CONVERSION_WITH_LOSS_PROHIBITED</span></span>  <br/> |
|<span data-ttu-id="06402-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="06402-108">Identifier:</span></span>  <br/> |<span data-ttu-id="06402-109">0x000D</span><span class="sxs-lookup"><span data-stu-id="06402-109">0x000D</span></span>  <br/> |
|<span data-ttu-id="06402-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="06402-110">Data type:</span></span>  <br/> |<span data-ttu-id="06402-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="06402-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="06402-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="06402-112">Area:</span></span>  <br/> |<span data-ttu-id="06402-113">一般的な構成</span><span class="sxs-lookup"><span data-stu-id="06402-113">General configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="06402-114">注釈</span><span class="sxs-lookup"><span data-stu-id="06402-114">Remarks</span></span>

<span data-ttu-id="06402-115">禁止されている変換の種類の例は、Unicode (1 文字あたり 2 バイト) から 1 バイト文字セットへの "損失" マッピングです。</span><span class="sxs-lookup"><span data-stu-id="06402-115">An example of the type of conversion being prohibited is the "lossy" mapping from Unicode (two bytes per character) to a single-byte character set.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="06402-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="06402-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="06402-117">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="06402-117">Header files</span></span>

<span data-ttu-id="06402-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="06402-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="06402-119">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="06402-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="06402-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="06402-120">Mapitags.h</span></span>
  
> <span data-ttu-id="06402-121">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="06402-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="06402-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="06402-122">See also</span></span>



[<span data-ttu-id="06402-123">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="06402-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="06402-124">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="06402-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="06402-125">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="06402-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="06402-126">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="06402-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

