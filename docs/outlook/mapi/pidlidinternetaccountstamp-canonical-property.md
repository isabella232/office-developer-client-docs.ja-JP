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
ms.openlocfilehash: 6edbf4e9c1300a7e2e67b1f4226c8e2d05e453c8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585221"
---
# <a name="pidlidinternetaccountstamp-canonical-property"></a><span data-ttu-id="5c125-103">PidLidInternetAccountStamp 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5c125-103">PidLidInternetAccountStamp Canonical Property</span></span>

  
  
<span data-ttu-id="5c125-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5c125-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5c125-105">電子メール メッセージを送信する電子メール アカウントの ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="5c125-105">Specifies the email account ID through which the email message is sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5c125-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="5c125-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5c125-107">dispidInetAcctStamp</span><span class="sxs-lookup"><span data-stu-id="5c125-107">dispidInetAcctStamp</span></span>  <br/> |
|<span data-ttu-id="5c125-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="5c125-108">Property set:</span></span>  <br/> |<span data-ttu-id="5c125-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="5c125-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="5c125-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="5c125-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="5c125-111">0x00008581</span><span class="sxs-lookup"><span data-stu-id="5c125-111">0x00008581</span></span>  <br/> |
|<span data-ttu-id="5c125-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="5c125-112">Data type:</span></span>  <br/> |<span data-ttu-id="5c125-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5c125-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="5c125-114">領域:</span><span class="sxs-lookup"><span data-stu-id="5c125-114">Area:</span></span>  <br/> |<span data-ttu-id="5c125-115">メッセージ全般</span><span class="sxs-lookup"><span data-stu-id="5c125-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5c125-116">注釈</span><span class="sxs-lookup"><span data-stu-id="5c125-116">Remarks</span></span>

<span data-ttu-id="5c125-117">この文字列の形式は、実装に依存します。</span><span class="sxs-lookup"><span data-stu-id="5c125-117">The format of this string is implementation dependent.</span></span> <span data-ttu-id="5c125-118">このプロパティは、メールを送信するサーバーを決定するのには、クライアントで使用できますが、オプションし、値は、サーバーに意味を持ちません。</span><span class="sxs-lookup"><span data-stu-id="5c125-118">This property can be used by the client to determine which server to direct the mail to, but is optional and the value has no meaning to the server.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5c125-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="5c125-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5c125-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="5c125-120">Protocol specifications</span></span>

<span data-ttu-id="5c125-121">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5c125-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5c125-122">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="5c125-122">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5c125-123">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5c125-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5c125-124">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="5c125-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5c125-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="5c125-125">Header files</span></span>

<span data-ttu-id="5c125-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5c125-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="5c125-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="5c125-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5c125-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="5c125-128">See also</span></span>



[<span data-ttu-id="5c125-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="5c125-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5c125-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="5c125-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5c125-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="5c125-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5c125-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="5c125-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

