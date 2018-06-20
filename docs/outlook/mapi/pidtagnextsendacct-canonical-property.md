---
title: PidTagNextSendAcct の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 517d0900e968ea55cedf6b17b31d97795fcf61c0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803015"
---
# <a name="pidtagnextsendacct-canonical-property"></a><span data-ttu-id="728e6-103">PidTagNextSendAcct の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="728e6-103">PidTagNextSendAcct Canonical Property</span></span>

  
  
<span data-ttu-id="728e6-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="728e6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="728e6-105">クライアントが電子メールの送信に使用する現在開こうとしているサーバーを指定します。</span><span class="sxs-lookup"><span data-stu-id="728e6-105">Specifies the server that a client is currently attempting to use to send email.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="728e6-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="728e6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="728e6-107">PR_NEXT_SEND_ACCT</span><span class="sxs-lookup"><span data-stu-id="728e6-107">PR_NEXT_SEND_ACCT</span></span>  <br/> |
|<span data-ttu-id="728e6-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="728e6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="728e6-109">0x0E29</span><span class="sxs-lookup"><span data-stu-id="728e6-109">0x0E29</span></span>  <br/> |
|<span data-ttu-id="728e6-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="728e6-110">Data type:</span></span>  <br/> |<span data-ttu-id="728e6-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="728e6-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="728e6-112">領域:</span><span class="sxs-lookup"><span data-stu-id="728e6-112">Area:</span></span>  <br/> |<span data-ttu-id="728e6-113">Outlook アプリケーション</span><span class="sxs-lookup"><span data-stu-id="728e6-113">Outlook application</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="728e6-114">備考</span><span class="sxs-lookup"><span data-stu-id="728e6-114">Remarks</span></span>

<span data-ttu-id="728e6-115">このプロパティの形式は、実装に依存します。</span><span class="sxs-lookup"><span data-stu-id="728e6-115">The format of this property is implementation dependent.</span></span> <span data-ttu-id="728e6-116">このプロパティに電子メールを送信するサーバーを決定するのには、クライアントで使用できますが、オプションし、値は、サーバーに意味を持ちません。</span><span class="sxs-lookup"><span data-stu-id="728e6-116">This property can be used by the client to determine which server to direct the email to, but is optional and the value has no meaning to the server.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="728e6-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="728e6-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="728e6-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="728e6-118">Protocol specifications</span></span>

<span data-ttu-id="728e6-119">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="728e6-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="728e6-120">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="728e6-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="728e6-121">[[MS OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="728e6-121">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="728e6-122">IETF RFC2445、RFC2446、RFC2447、および予定と会議のオブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="728e6-122">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="728e6-123">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="728e6-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="728e6-124">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="728e6-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="728e6-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="728e6-125">Header files</span></span>

<span data-ttu-id="728e6-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="728e6-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="728e6-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="728e6-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="728e6-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="728e6-128">Mapitags.h</span></span>
  
> <span data-ttu-id="728e6-129">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="728e6-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="728e6-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="728e6-130">See also</span></span>



[<span data-ttu-id="728e6-131">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="728e6-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="728e6-132">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="728e6-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="728e6-133">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="728e6-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="728e6-134">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="728e6-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

