---
title: PidLidInternetAccountStamp 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidInternetAccountStamp
api_type:
- COM
ms.assetid: 819179fe-e58e-415c-abc7-1949036745ee
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ebd64392d24cd170a7babf77865aa00c7be24802
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396632"
---
# <a name="pidlidinternetaccountstamp-canonical-property"></a><span data-ttu-id="734d2-103">PidLidInternetAccountStamp 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="734d2-103">PidLidInternetAccountStamp Canonical Property</span></span>

  
  
<span data-ttu-id="734d2-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="734d2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="734d2-105">電子メール メッセージを送信する電子メール アカウントの ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="734d2-105">Specifies the email account ID through which the email message is sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="734d2-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="734d2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="734d2-107">dispidInetAcctStamp</span><span class="sxs-lookup"><span data-stu-id="734d2-107">dispidInetAcctStamp</span></span>  <br/> |
|<span data-ttu-id="734d2-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="734d2-108">Property set:</span></span>  <br/> |<span data-ttu-id="734d2-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="734d2-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="734d2-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="734d2-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="734d2-111">0x00008581</span><span class="sxs-lookup"><span data-stu-id="734d2-111">0x00008581</span></span>  <br/> |
|<span data-ttu-id="734d2-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="734d2-112">Data type:</span></span>  <br/> |<span data-ttu-id="734d2-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="734d2-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="734d2-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="734d2-114">Area:</span></span>  <br/> |<span data-ttu-id="734d2-115">メッセージ全般</span><span class="sxs-lookup"><span data-stu-id="734d2-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="734d2-116">備考</span><span class="sxs-lookup"><span data-stu-id="734d2-116">Remarks</span></span>

<span data-ttu-id="734d2-117">この文字列の形式は、実装に依存します。</span><span class="sxs-lookup"><span data-stu-id="734d2-117">The format of this string is implementation dependent.</span></span> <span data-ttu-id="734d2-118">このプロパティは、メールを送信するサーバーを決定するのには、クライアントで使用できますが、オプションし、値は、サーバーに意味を持ちません。</span><span class="sxs-lookup"><span data-stu-id="734d2-118">This property can be used by the client to determine which server to direct the mail to, but is optional and the value has no meaning to the server.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="734d2-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="734d2-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="734d2-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="734d2-120">Protocol specifications</span></span>

<span data-ttu-id="734d2-121">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="734d2-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="734d2-122">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="734d2-122">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="734d2-123">[[MS OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="734d2-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="734d2-124">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="734d2-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="734d2-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="734d2-125">Header files</span></span>

<span data-ttu-id="734d2-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="734d2-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="734d2-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="734d2-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="734d2-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="734d2-128">See also</span></span>



[<span data-ttu-id="734d2-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="734d2-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="734d2-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="734d2-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="734d2-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="734d2-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="734d2-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="734d2-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

