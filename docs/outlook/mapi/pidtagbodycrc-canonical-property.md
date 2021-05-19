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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 416486c3b06c485a1fa6525b54c37a6e0d23f56c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415181"
---
# <a name="pidtagbodycrc-canonical-property"></a><span data-ttu-id="c889d-103">PidTagBodyCrc 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c889d-103">PidTagBodyCrc Canonical Property</span></span>

  
  
<span data-ttu-id="c889d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c889d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c889d-105">メッセージ テキストの循環冗長チェック (CRC) 値を含む。</span><span class="sxs-lookup"><span data-stu-id="c889d-105">Contains a cyclic redundancy check (CRC) value on the message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c889d-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="c889d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c889d-107">PR_BODY_CRC</span><span class="sxs-lookup"><span data-stu-id="c889d-107">PR_BODY_CRC</span></span>  <br/> |
|<span data-ttu-id="c889d-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="c889d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c889d-109">0x0E1C</span><span class="sxs-lookup"><span data-stu-id="c889d-109">0x0E1C</span></span>  <br/> |
|<span data-ttu-id="c889d-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="c889d-110">Data type:</span></span>  <br/> |<span data-ttu-id="c889d-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c889d-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c889d-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="c889d-112">Area:</span></span>  <br/> |<span data-ttu-id="c889d-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="c889d-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c889d-114">注釈</span><span class="sxs-lookup"><span data-stu-id="c889d-114">Remarks</span></span>

<span data-ttu-id="c889d-115">メッセージ ストアでは、値を生成する任意の CRC アルゴリズムPT_LONGできます。</span><span class="sxs-lookup"><span data-stu-id="c889d-115">The message store can use any CRC algorithm that generates a PT_LONG value.</span></span> <span data-ttu-id="c889d-116">PR_BODY ([PidTagBody](pidtagbody-canonical-property.md)) プロパティが初めて設定され、その後変更されるたびに、**この** プロパティを [IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドの一部として計算する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c889d-116">It must compute this property as part of the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method when the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property has been set for the first time and whenever it has been subsequently modified.</span></span>
  
<span data-ttu-id="c889d-117">クライアント アプリケーションは **、PR_BODY_CRC** プロパティまたはバリアントに含まれるメッセージ テキスト文字列を比較 **PR_BODY使用します** 。</span><span class="sxs-lookup"><span data-stu-id="c889d-117">A client application uses **PR_BODY_CRC** to aid in comparing message text strings contained in **PR_BODY** properties or their variants.</span></span> <span data-ttu-id="c889d-118">このプロパティを使用すると、クライアントはメッセージ テキストが変更された時点を迅速かつ簡単に検出できます。</span><span class="sxs-lookup"><span data-stu-id="c889d-118">Using this property, the client can quickly and easily detect when the message text has changed.</span></span> <span data-ttu-id="c889d-119">メッセージ ストアから PR_BODY_CRC を取得しPR_BODYバージョンと比較する代わりに、パフォーマンスの大幅な向上を実現できます。</span><span class="sxs-lookup"><span data-stu-id="c889d-119">It can realize significant performance gains by using **PR_BODY_CRC** instead of obtaining **PR_BODY** from the message store and comparing it with a local version.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c889d-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="c889d-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="c889d-121">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="c889d-121">Header files</span></span>

<span data-ttu-id="c889d-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c889d-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="c889d-123">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="c889d-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="c889d-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c889d-124">Mapitags.h</span></span>
  
> <span data-ttu-id="c889d-125">関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="c889d-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c889d-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="c889d-126">See also</span></span>



[<span data-ttu-id="c889d-127">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="c889d-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c889d-128">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c889d-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c889d-129">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="c889d-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c889d-130">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="c889d-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

