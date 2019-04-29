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
# <a name="pidtagconversionwithlossprohibited-canonical-property"></a><span data-ttu-id="5539a-103">PidTagConversionWithLossProhibited 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5539a-103">PidTagConversionWithLossProhibited Canonical Property</span></span>

  
  
<span data-ttu-id="5539a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5539a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5539a-105">メッセージ転送エージェント (MTA) が、情報を失うメッセージテキスト変換を禁止する場合は、TRUE が含まれます。</span><span class="sxs-lookup"><span data-stu-id="5539a-105">Contains TRUE if a message transfer agent (MTA) is prohibited from making message text conversions that lose information.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5539a-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="5539a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5539a-107">PR_CONVERSION_WITH_LOSS_PROHIBITED</span><span class="sxs-lookup"><span data-stu-id="5539a-107">PR_CONVERSION_WITH_LOSS_PROHIBITED</span></span>  <br/> |
|<span data-ttu-id="5539a-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="5539a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5539a-109">0x000d</span><span class="sxs-lookup"><span data-stu-id="5539a-109">0x000D</span></span>  <br/> |
|<span data-ttu-id="5539a-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="5539a-110">Data type:</span></span>  <br/> |<span data-ttu-id="5539a-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="5539a-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="5539a-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="5539a-112">Area:</span></span>  <br/> |<span data-ttu-id="5539a-113">全般構成</span><span class="sxs-lookup"><span data-stu-id="5539a-113">General configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5539a-114">注釈</span><span class="sxs-lookup"><span data-stu-id="5539a-114">Remarks</span></span>

<span data-ttu-id="5539a-115">禁止されている変換の種類の例としては、Unicode (文字ごとに2バイト) から1バイト文字セットへの "可逆" マッピングがあります。</span><span class="sxs-lookup"><span data-stu-id="5539a-115">An example of the type of conversion being prohibited is the "lossy" mapping from Unicode (two bytes per character) to a single-byte character set.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="5539a-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="5539a-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="5539a-117">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="5539a-117">Header files</span></span>

<span data-ttu-id="5539a-118">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5539a-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="5539a-119">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="5539a-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="5539a-120">Mapitags</span><span class="sxs-lookup"><span data-stu-id="5539a-120">Mapitags.h</span></span>
  
> <span data-ttu-id="5539a-121">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="5539a-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5539a-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="5539a-122">See also</span></span>



[<span data-ttu-id="5539a-123">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="5539a-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5539a-124">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5539a-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5539a-125">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="5539a-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5539a-126">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="5539a-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

