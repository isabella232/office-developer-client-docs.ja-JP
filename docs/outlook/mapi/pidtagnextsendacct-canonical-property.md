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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 76584e248f03deac62af94e4638fcead15594b3e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581133"
---
# <a name="pidtagnextsendacct-canonical-property"></a><span data-ttu-id="413b9-103">PidTagNextSendAcct 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="413b9-103">PidTagNextSendAcct Canonical Property</span></span>

  
  
<span data-ttu-id="413b9-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="413b9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="413b9-105">クライアントが電子メールの送信に使用する現在開こうとしているサーバーを指定します。</span><span class="sxs-lookup"><span data-stu-id="413b9-105">Specifies the server that a client is currently attempting to use to send email.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="413b9-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="413b9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="413b9-107">PR_NEXT_SEND_ACCT</span><span class="sxs-lookup"><span data-stu-id="413b9-107">PR_NEXT_SEND_ACCT</span></span>  <br/> |
|<span data-ttu-id="413b9-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="413b9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="413b9-109">0x0E29</span><span class="sxs-lookup"><span data-stu-id="413b9-109">0x0E29</span></span>  <br/> |
|<span data-ttu-id="413b9-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="413b9-110">Data type:</span></span>  <br/> |<span data-ttu-id="413b9-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="413b9-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="413b9-112">領域:</span><span class="sxs-lookup"><span data-stu-id="413b9-112">Area:</span></span>  <br/> |<span data-ttu-id="413b9-113">Outlook アプリケーション</span><span class="sxs-lookup"><span data-stu-id="413b9-113">Outlook application</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="413b9-114">注釈</span><span class="sxs-lookup"><span data-stu-id="413b9-114">Remarks</span></span>

<span data-ttu-id="413b9-115">このプロパティの形式は、実装に依存します。</span><span class="sxs-lookup"><span data-stu-id="413b9-115">The format of this property is implementation dependent.</span></span> <span data-ttu-id="413b9-116">このプロパティに電子メールを送信するサーバーを決定するのには、クライアントで使用できますが、オプションし、値は、サーバーに意味を持ちません。</span><span class="sxs-lookup"><span data-stu-id="413b9-116">This property can be used by the client to determine which server to direct the email to, but is optional and the value has no meaning to the server.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="413b9-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="413b9-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="413b9-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="413b9-118">Protocol specifications</span></span>

<span data-ttu-id="413b9-119">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="413b9-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="413b9-120">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="413b9-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="413b9-121">[[MS OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="413b9-121">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="413b9-122">IETF RFC2445、RFC2446、RFC2447、および予定と会議のオブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="413b9-122">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="413b9-123">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="413b9-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="413b9-124">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="413b9-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="413b9-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="413b9-125">Header files</span></span>

<span data-ttu-id="413b9-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="413b9-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="413b9-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="413b9-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="413b9-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="413b9-128">Mapitags.h</span></span>
  
> <span data-ttu-id="413b9-129">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="413b9-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="413b9-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="413b9-130">See also</span></span>



[<span data-ttu-id="413b9-131">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="413b9-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="413b9-132">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="413b9-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="413b9-133">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="413b9-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="413b9-134">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="413b9-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

