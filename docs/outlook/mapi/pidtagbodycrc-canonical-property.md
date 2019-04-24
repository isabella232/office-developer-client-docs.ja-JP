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
ms.openlocfilehash: 416486c3b06c485a1fa6525b54c37a6e0d23f56c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350926"
---
# <a name="pidtagbodycrc-canonical-property"></a><span data-ttu-id="08245-103">PidTagBodyCrc 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="08245-103">PidTagBodyCrc Canonical Property</span></span>

  
  
<span data-ttu-id="08245-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="08245-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="08245-105">メッセージテキストの巡回冗長検査 (CRC) 値を含みます。</span><span class="sxs-lookup"><span data-stu-id="08245-105">Contains a cyclic redundancy check (CRC) value on the message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="08245-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="08245-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="08245-107">PR_BODY_CRC</span><span class="sxs-lookup"><span data-stu-id="08245-107">PR_BODY_CRC</span></span>  <br/> |
|<span data-ttu-id="08245-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="08245-108">Identifier:</span></span>  <br/> |<span data-ttu-id="08245-109">0x0e1c</span><span class="sxs-lookup"><span data-stu-id="08245-109">0x0E1C</span></span>  <br/> |
|<span data-ttu-id="08245-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="08245-110">Data type:</span></span>  <br/> |<span data-ttu-id="08245-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="08245-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="08245-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="08245-112">Area:</span></span>  <br/> |<span data-ttu-id="08245-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="08245-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="08245-114">解説</span><span class="sxs-lookup"><span data-stu-id="08245-114">Remarks</span></span>

<span data-ttu-id="08245-115">メッセージストアは、PT_LONG 値を生成する任意の CRC アルゴリズムを使用できます。</span><span class="sxs-lookup"><span data-stu-id="08245-115">The message store can use any CRC algorithm that generates a PT_LONG value.</span></span> <span data-ttu-id="08245-116">このプロパティは、 **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) プロパティが初めて設定されたときとその後に変更されたときの[imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドの一部として計算する必要があります。</span><span class="sxs-lookup"><span data-stu-id="08245-116">It must compute this property as part of the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method when the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property has been set for the first time and whenever it has been subsequently modified.</span></span>
  
<span data-ttu-id="08245-117">クライアントアプリケーションは**PR_BODY_CRC**を使用して、 **PR_BODY**のプロパティまたはそのバリエーションに含まれるメッセージテキスト文字列の比較を支援します。</span><span class="sxs-lookup"><span data-stu-id="08245-117">A client application uses **PR_BODY_CRC** to aid in comparing message text strings contained in **PR_BODY** properties or their variants.</span></span> <span data-ttu-id="08245-118">このプロパティを使用すると、クライアントは、メッセージテキストが変更されたときにすばやく簡単に検出できます。</span><span class="sxs-lookup"><span data-stu-id="08245-118">Using this property, the client can quickly and easily detect when the message text has changed.</span></span> <span data-ttu-id="08245-119">**PR_BODY_CRC**を使用して、メッセージストアから**PR_BODY**を取得し、ローカルバージョンと比較するのではなく、パフォーマンスを大幅に向上させることができます。</span><span class="sxs-lookup"><span data-stu-id="08245-119">It can realize significant performance gains by using **PR_BODY_CRC** instead of obtaining **PR_BODY** from the message store and comparing it with a local version.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="08245-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="08245-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="08245-121">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="08245-121">Header files</span></span>

<span data-ttu-id="08245-122">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="08245-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="08245-123">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="08245-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="08245-124">Mapitags</span><span class="sxs-lookup"><span data-stu-id="08245-124">Mapitags.h</span></span>
  
> <span data-ttu-id="08245-125">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="08245-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="08245-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="08245-126">See also</span></span>



[<span data-ttu-id="08245-127">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="08245-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="08245-128">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="08245-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="08245-129">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="08245-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="08245-130">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="08245-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

