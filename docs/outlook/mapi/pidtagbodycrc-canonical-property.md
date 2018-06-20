---
title: PidTagBodyCrc の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 66a150cf3f83465840aa0e79a9ef921b1534f814
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802529"
---
# <a name="pidtagbodycrc-canonical-property"></a><span data-ttu-id="43291-103">PidTagBodyCrc の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="43291-103">PidTagBodyCrc Canonical Property</span></span>

  
  
<span data-ttu-id="43291-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="43291-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="43291-105">メッセージ テキストの巡回冗長検査 (CRC) の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="43291-105">Contains a cyclic redundancy check (CRC) value on the message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="43291-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="43291-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="43291-107">PR_BODY_CRC</span><span class="sxs-lookup"><span data-stu-id="43291-107">PR_BODY_CRC</span></span>  <br/> |
|<span data-ttu-id="43291-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="43291-108">Identifier:</span></span>  <br/> |<span data-ttu-id="43291-109">0x0E1C</span><span class="sxs-lookup"><span data-stu-id="43291-109">0x0E1C</span></span>  <br/> |
|<span data-ttu-id="43291-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="43291-110">Data type:</span></span>  <br/> |<span data-ttu-id="43291-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="43291-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="43291-112">領域:</span><span class="sxs-lookup"><span data-stu-id="43291-112">Area:</span></span>  <br/> |<span data-ttu-id="43291-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="43291-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="43291-114">備考</span><span class="sxs-lookup"><span data-stu-id="43291-114">Remarks</span></span>

<span data-ttu-id="43291-115">メッセージ ・ ストアには、PT_LONG の値を生成する任意の CRC アルゴリズムを使用できます。</span><span class="sxs-lookup"><span data-stu-id="43291-115">The message store can use any CRC algorithm that generates a PT_LONG value.</span></span> <span data-ttu-id="43291-116">[IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドの一部としてこのプロパティを計算すると、最初に、後で変更されるたびに ([PidTagBody](pidtagbody-canonical-property.md)) である**PR_BODY**プロパティが設定されていること必要があります。</span><span class="sxs-lookup"><span data-stu-id="43291-116">It must compute this property as part of the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method when the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property has been set for the first time and whenever it has been subsequently modified.</span></span>
  
<span data-ttu-id="43291-117">**PR_BODY**プロパティまたはその変種に含まれるメッセージのテキスト文字列を比較するを支援するクライアント アプリケーションが**PR_BODY_CRC**を使用します。</span><span class="sxs-lookup"><span data-stu-id="43291-117">A client application uses **PR_BODY_CRC** to aid in comparing message text strings contained in **PR_BODY** properties or their variants.</span></span> <span data-ttu-id="43291-118">このプロパティを使用するクライアント迅速かつ容易に検出できるメッセージのテキストが変更されたとき。</span><span class="sxs-lookup"><span data-stu-id="43291-118">Using this property, the client can quickly and easily detect when the message text has changed.</span></span> <span data-ttu-id="43291-119">**PR_BODY_CRC**を使用して**PR_BODY**をメッセージ ・ ストアから取得し、ローカル バージョンと比較することではなく、その大幅なパフォーマンス向上を実感できます。</span><span class="sxs-lookup"><span data-stu-id="43291-119">It can realize significant performance gains by using **PR_BODY_CRC** instead of obtaining **PR_BODY** from the message store and comparing it with a local version.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="43291-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="43291-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="43291-121">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="43291-121">Header files</span></span>

<span data-ttu-id="43291-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="43291-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="43291-123">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="43291-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="43291-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="43291-124">Mapitags.h</span></span>
  
> <span data-ttu-id="43291-125">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="43291-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="43291-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="43291-126">See also</span></span>



[<span data-ttu-id="43291-127">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="43291-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="43291-128">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="43291-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="43291-129">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="43291-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="43291-130">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="43291-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

