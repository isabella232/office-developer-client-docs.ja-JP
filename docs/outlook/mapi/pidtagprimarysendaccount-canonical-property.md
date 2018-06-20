---
title: PidTagPrimarySendAccount の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagPrimarySendAccount
api_type:
- COM
ms.assetid: 2f268b3b-2e4c-4aea-8879-bdd0ac1df35c
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 222ca10e58b50fa06876718658d1a6f3843da2f2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803181"
---
# <a name="pidtagprimarysendaccount-canonical-property"></a><span data-ttu-id="9a91f-103">PidTagPrimarySendAccount の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="9a91f-103">PidTagPrimarySendAccount Canonical Property</span></span>

  
  
<span data-ttu-id="9a91f-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9a91f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9a91f-105">メッセージを送信するために使用される最初のサーバーの名前を示す文字列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9a91f-105">Contains a string that names the first server that is used to send the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9a91f-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="9a91f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9a91f-107">PR_PRIMARY_SEND_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="9a91f-107">PR_PRIMARY_SEND_ACCOUNT</span></span>  <br/> |
|<span data-ttu-id="9a91f-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="9a91f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9a91f-109">0x0E28</span><span class="sxs-lookup"><span data-stu-id="9a91f-109">0x0E28</span></span>  <br/> |
|<span data-ttu-id="9a91f-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="9a91f-110">Data type:</span></span>  <br/> |<span data-ttu-id="9a91f-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9a91f-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="9a91f-112">領域:</span><span class="sxs-lookup"><span data-stu-id="9a91f-112">Area:</span></span>  <br/> |<span data-ttu-id="9a91f-113">Account</span><span class="sxs-lookup"><span data-stu-id="9a91f-113">Account</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9a91f-114">備考</span><span class="sxs-lookup"><span data-stu-id="9a91f-114">Remarks</span></span>

<span data-ttu-id="9a91f-115">メールを送信するクライアントを使用する必要があります最初のサーバーを指定します。</span><span class="sxs-lookup"><span data-stu-id="9a91f-115">Specifies the first server that a client should use to send the mail.</span></span> <span data-ttu-id="9a91f-116">これらのプロパティの形式は、実装に依存します。</span><span class="sxs-lookup"><span data-stu-id="9a91f-116">The format of these properties is implementation dependent.</span></span> <span data-ttu-id="9a91f-117">これらのプロパティを通じて、メールを送信するサーバーを決定するのには、クライアントで使用できますが、オプションと値は、サーバーに意味を持ちません。</span><span class="sxs-lookup"><span data-stu-id="9a91f-117">These properties can be used by the client to determine which server to direct the mail through, but is optional and the value has no meaning to the server.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9a91f-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="9a91f-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9a91f-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="9a91f-119">Protocol specifications</span></span>

<span data-ttu-id="9a91f-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9a91f-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9a91f-121">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="9a91f-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9a91f-122">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9a91f-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9a91f-123">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="9a91f-123">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9a91f-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="9a91f-124">Header files</span></span>

<span data-ttu-id="9a91f-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9a91f-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="9a91f-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="9a91f-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="9a91f-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9a91f-127">Mapitags.h</span></span>
  
> <span data-ttu-id="9a91f-128">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9a91f-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9a91f-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="9a91f-129">See also</span></span>



[<span data-ttu-id="9a91f-130">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="9a91f-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9a91f-131">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="9a91f-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9a91f-132">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="9a91f-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9a91f-133">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="9a91f-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

