---
title: PidTagNextSendAcct 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagNextSendAcct
api_type:
- HeaderDef
ms.assetid: b7429c2e-0d9d-4921-9f56-9ecad817f8cb
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: eff053fda58266afd5500e322559059f051d5ac3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329394"
---
# <a name="pidtagnextsendacct-canonical-property"></a><span data-ttu-id="6be56-103">PidTagNextSendAcct 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="6be56-103">PidTagNextSendAcct Canonical Property</span></span>

  
  
<span data-ttu-id="6be56-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6be56-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6be56-105">クライアントが現在電子メールの送信に使用するサーバーを指定します。</span><span class="sxs-lookup"><span data-stu-id="6be56-105">Specifies the server that a client is currently attempting to use to send email.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6be56-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="6be56-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6be56-107">PR_NEXT_SEND_ACCT</span><span class="sxs-lookup"><span data-stu-id="6be56-107">PR_NEXT_SEND_ACCT</span></span>  <br/> |
|<span data-ttu-id="6be56-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="6be56-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6be56-109">0x0E29</span><span class="sxs-lookup"><span data-stu-id="6be56-109">0x0E29</span></span>  <br/> |
|<span data-ttu-id="6be56-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="6be56-110">Data type:</span></span>  <br/> |<span data-ttu-id="6be56-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6be56-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="6be56-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="6be56-112">Area:</span></span>  <br/> |<span data-ttu-id="6be56-113">Outlookアプリケーション</span><span class="sxs-lookup"><span data-stu-id="6be56-113">Outlook application</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6be56-114">注釈</span><span class="sxs-lookup"><span data-stu-id="6be56-114">Remarks</span></span>

<span data-ttu-id="6be56-115">このプロパティの形式は実装に依存します。</span><span class="sxs-lookup"><span data-stu-id="6be56-115">The format of this property is implementation dependent.</span></span> <span data-ttu-id="6be56-116">このプロパティは、クライアントが電子メールを送信するサーバーを決定するために使用できますが、オプションであり、値はサーバーに対して意味を持つ必要はありません。</span><span class="sxs-lookup"><span data-stu-id="6be56-116">This property can be used by the client to determine which server to direct the email to, but is optional and the value has no meaning to the server.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6be56-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="6be56-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6be56-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="6be56-118">Protocol specifications</span></span>

<span data-ttu-id="6be56-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6be56-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6be56-120">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="6be56-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6be56-121">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6be56-121">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6be56-122">IETF RFC2445、RFC2446、RFC2447、および予定オブジェクトと会議オブジェクトの間で変換します。</span><span class="sxs-lookup"><span data-stu-id="6be56-122">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="6be56-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6be56-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6be56-124">電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="6be56-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6be56-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="6be56-125">Header files</span></span>

<span data-ttu-id="6be56-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6be56-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="6be56-127">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="6be56-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="6be56-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6be56-128">Mapitags.h</span></span>
  
> <span data-ttu-id="6be56-129">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="6be56-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6be56-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="6be56-130">See also</span></span>



[<span data-ttu-id="6be56-131">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="6be56-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6be56-132">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="6be56-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6be56-133">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="6be56-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6be56-134">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="6be56-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

