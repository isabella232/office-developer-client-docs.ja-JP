---
title: PidTagConversionWithLossProhibited の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: eee70d97c35c7f115e424905b9e36f3dfa392c02
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802654"
---
# <a name="pidtagconversionwithlossprohibited-canonical-property"></a><span data-ttu-id="bb5b6-103">PidTagConversionWithLossProhibited の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="bb5b6-103">PidTagConversionWithLossProhibited Canonical Property</span></span>

  
  
<span data-ttu-id="bb5b6-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bb5b6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bb5b6-105">メッセージ転送エージェント (MTA) がメッセージの情報が失われるテキストの変換をすることから禁止されている場合 TRUE が含まれています。</span><span class="sxs-lookup"><span data-stu-id="bb5b6-105">Contains TRUE if a message transfer agent (MTA) is prohibited from making message text conversions that lose information.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bb5b6-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="bb5b6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bb5b6-107">PR_CONVERSION_WITH_LOSS_PROHIBITED</span><span class="sxs-lookup"><span data-stu-id="bb5b6-107">PR_CONVERSION_WITH_LOSS_PROHIBITED</span></span>  <br/> |
|<span data-ttu-id="bb5b6-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="bb5b6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bb5b6-109">0x000D</span><span class="sxs-lookup"><span data-stu-id="bb5b6-109">0x000D</span></span>  <br/> |
|<span data-ttu-id="bb5b6-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="bb5b6-110">Data type:</span></span>  <br/> |<span data-ttu-id="bb5b6-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="bb5b6-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="bb5b6-112">領域:</span><span class="sxs-lookup"><span data-stu-id="bb5b6-112">Area:</span></span>  <br/> |<span data-ttu-id="bb5b6-113">一般的な構成</span><span class="sxs-lookup"><span data-stu-id="bb5b6-113">General configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bb5b6-114">備考</span><span class="sxs-lookup"><span data-stu-id="bb5b6-114">Remarks</span></span>

<span data-ttu-id="bb5b6-115">禁止されている変換の種類の例が、「損失」のマッピング Unicode (1 文字あたり 2 バイト) からシングル バイト文字セットです。</span><span class="sxs-lookup"><span data-stu-id="bb5b6-115">An example of the type of conversion being prohibited is the "lossy" mapping from Unicode (two bytes per character) to a single-byte character set.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="bb5b6-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="bb5b6-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="bb5b6-117">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="bb5b6-117">Header files</span></span>

<span data-ttu-id="bb5b6-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bb5b6-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="bb5b6-119">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="bb5b6-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="bb5b6-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bb5b6-120">Mapitags.h</span></span>
  
> <span data-ttu-id="bb5b6-121">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="bb5b6-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bb5b6-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="bb5b6-122">See also</span></span>



[<span data-ttu-id="bb5b6-123">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="bb5b6-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bb5b6-124">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="bb5b6-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bb5b6-125">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="bb5b6-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bb5b6-126">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="bb5b6-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

