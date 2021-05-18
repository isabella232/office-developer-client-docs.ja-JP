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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ebd64392d24cd170a7babf77865aa00c7be24802
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315457"
---
# <a name="pidlidinternetaccountstamp-canonical-property"></a><span data-ttu-id="707b5-103">PidLidInternetAccountStamp 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="707b5-103">PidLidInternetAccountStamp Canonical Property</span></span>

  
  
<span data-ttu-id="707b5-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="707b5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="707b5-105">電子メール メッセージが送信される電子メール アカウント ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="707b5-105">Specifies the email account ID through which the email message is sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="707b5-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="707b5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="707b5-107">dispidInetAcctStamp</span><span class="sxs-lookup"><span data-stu-id="707b5-107">dispidInetAcctStamp</span></span>  <br/> |
|<span data-ttu-id="707b5-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="707b5-108">Property set:</span></span>  <br/> |<span data-ttu-id="707b5-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="707b5-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="707b5-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="707b5-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="707b5-111">0x00008581</span><span class="sxs-lookup"><span data-stu-id="707b5-111">0x00008581</span></span>  <br/> |
|<span data-ttu-id="707b5-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="707b5-112">Data type:</span></span>  <br/> |<span data-ttu-id="707b5-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="707b5-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="707b5-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="707b5-114">Area:</span></span>  <br/> |<span data-ttu-id="707b5-115">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="707b5-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="707b5-116">注釈</span><span class="sxs-lookup"><span data-stu-id="707b5-116">Remarks</span></span>

<span data-ttu-id="707b5-117">この文字列の形式は実装に依存します。</span><span class="sxs-lookup"><span data-stu-id="707b5-117">The format of this string is implementation dependent.</span></span> <span data-ttu-id="707b5-118">このプロパティは、クライアントがメールを送信するサーバーを決定するために使用できますが、オプションであり、値はサーバーに対して意味を持つ必要はありません。</span><span class="sxs-lookup"><span data-stu-id="707b5-118">This property can be used by the client to determine which server to direct the mail to, but is optional and the value has no meaning to the server.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="707b5-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="707b5-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="707b5-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="707b5-120">Protocol specifications</span></span>

<span data-ttu-id="707b5-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="707b5-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="707b5-122">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="707b5-122">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="707b5-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="707b5-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="707b5-124">電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="707b5-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="707b5-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="707b5-125">Header files</span></span>

<span data-ttu-id="707b5-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="707b5-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="707b5-127">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="707b5-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="707b5-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="707b5-128">See also</span></span>



[<span data-ttu-id="707b5-129">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="707b5-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="707b5-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="707b5-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="707b5-131">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="707b5-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="707b5-132">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="707b5-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

