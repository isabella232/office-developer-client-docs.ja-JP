---
title: PidTagBodyCrc 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagBodyCrc
api_type:
- HeaderDef
ms.assetid: 6efe9dc3-e988-4042-ab02-2863b5e0f294
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 66a150cf3f83465840aa0e79a9ef921b1534f814
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802529"
---
# <a name="pidtagbodycrc-canonical-property"></a><span data-ttu-id="2e64f-103">PidTagBodyCrc 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2e64f-103">PidTagBodyCrc Canonical Property</span></span>

  
  
<span data-ttu-id="2e64f-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2e64f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2e64f-105">メッセージ テキストの巡回冗長検査 (CRC) の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="2e64f-105">Contains a cyclic redundancy check (CRC) value on the message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2e64f-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="2e64f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2e64f-107">PR_BODY_CRC</span><span class="sxs-lookup"><span data-stu-id="2e64f-107">PR_BODY_CRC</span></span>  <br/> |
|<span data-ttu-id="2e64f-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="2e64f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2e64f-109">0x0E1C</span><span class="sxs-lookup"><span data-stu-id="2e64f-109">0x0E1C</span></span>  <br/> |
|<span data-ttu-id="2e64f-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="2e64f-110">Data type:</span></span>  <br/> |<span data-ttu-id="2e64f-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="2e64f-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="2e64f-112">領域:</span><span class="sxs-lookup"><span data-stu-id="2e64f-112">Area:</span></span>  <br/> |<span data-ttu-id="2e64f-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="2e64f-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2e64f-114">注釈</span><span class="sxs-lookup"><span data-stu-id="2e64f-114">Remarks</span></span>

<span data-ttu-id="2e64f-115">メッセージ ・ ストアには、PT_LONG の値を生成する任意の CRC アルゴリズムを使用できます。</span><span class="sxs-lookup"><span data-stu-id="2e64f-115">The message store can use any CRC algorithm that generates a PT_LONG value.</span></span> <span data-ttu-id="2e64f-116">[IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドの一部としてこのプロパティを計算すると、最初に、後で変更されるたびに ([PidTagBody](pidtagbody-canonical-property.md)) である**PR_BODY**プロパティが設定されていること必要があります。</span><span class="sxs-lookup"><span data-stu-id="2e64f-116">It must compute this property as part of the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method when the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property has been set for the first time and whenever it has been subsequently modified.</span></span>
  
<span data-ttu-id="2e64f-117">**PR_BODY**プロパティまたはその変種に含まれるメッセージのテキスト文字列を比較するを支援するクライアント アプリケーションが**PR_BODY_CRC**を使用します。</span><span class="sxs-lookup"><span data-stu-id="2e64f-117">A client application uses **PR_BODY_CRC** to aid in comparing message text strings contained in **PR_BODY** properties or their variants.</span></span> <span data-ttu-id="2e64f-118">このプロパティを使用するクライアント迅速かつ容易に検出できるメッセージのテキストが変更されたとき。</span><span class="sxs-lookup"><span data-stu-id="2e64f-118">Using this property, the client can quickly and easily detect when the message text has changed.</span></span> <span data-ttu-id="2e64f-119">**PR_BODY_CRC**を使用して**PR_BODY**をメッセージ ・ ストアから取得し、ローカル バージョンと比較することではなく、その大幅なパフォーマンス向上を実感できます。</span><span class="sxs-lookup"><span data-stu-id="2e64f-119">It can realize significant performance gains by using **PR_BODY_CRC** instead of obtaining **PR_BODY** from the message store and comparing it with a local version.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="2e64f-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="2e64f-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="2e64f-121">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="2e64f-121">Header files</span></span>

<span data-ttu-id="2e64f-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2e64f-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="2e64f-123">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="2e64f-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="2e64f-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2e64f-124">Mapitags.h</span></span>
  
> <span data-ttu-id="2e64f-125">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="2e64f-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2e64f-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="2e64f-126">See also</span></span>



[<span data-ttu-id="2e64f-127">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="2e64f-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2e64f-128">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="2e64f-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2e64f-129">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="2e64f-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2e64f-130">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="2e64f-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

