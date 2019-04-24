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
ms.openlocfilehash: eff053fda58266afd5500e322559059f051d5ac3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329394"
---
# <a name="pidtagnextsendacct-canonical-property"></a><span data-ttu-id="7611a-103">PidTagNextSendAcct 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="7611a-103">PidTagNextSendAcct Canonical Property</span></span>

  
  
<span data-ttu-id="7611a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7611a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7611a-105">クライアントが電子メールの送信に現在使用しているサーバーを指定します。</span><span class="sxs-lookup"><span data-stu-id="7611a-105">Specifies the server that a client is currently attempting to use to send email.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7611a-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="7611a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7611a-107">PR_NEXT_SEND_ACCT</span><span class="sxs-lookup"><span data-stu-id="7611a-107">PR_NEXT_SEND_ACCT</span></span>  <br/> |
|<span data-ttu-id="7611a-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="7611a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7611a-109">0x0e29</span><span class="sxs-lookup"><span data-stu-id="7611a-109">0x0E29</span></span>  <br/> |
|<span data-ttu-id="7611a-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="7611a-110">Data type:</span></span>  <br/> |<span data-ttu-id="7611a-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7611a-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="7611a-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="7611a-112">Area:</span></span>  <br/> |<span data-ttu-id="7611a-113">Outlook アプリケーション</span><span class="sxs-lookup"><span data-stu-id="7611a-113">Outlook application</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7611a-114">解説</span><span class="sxs-lookup"><span data-stu-id="7611a-114">Remarks</span></span>

<span data-ttu-id="7611a-115">このプロパティの形式は、実装によって異なります。</span><span class="sxs-lookup"><span data-stu-id="7611a-115">The format of this property is implementation dependent.</span></span> <span data-ttu-id="7611a-116">このプロパティは、クライアントが電子メールの送信先となるサーバーを決定するために使用できますが、その値はサーバーには意味がありません。</span><span class="sxs-lookup"><span data-stu-id="7611a-116">This property can be used by the client to determine which server to direct the email to, but is optional and the value has no meaning to the server.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7611a-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="7611a-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7611a-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="7611a-118">Protocol specifications</span></span>

<span data-ttu-id="7611a-119">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7611a-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7611a-120">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="7611a-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7611a-121">[[OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7611a-121">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7611a-122">IETF RFC2445、RFC2446、RFC2447、予定および会議の各オブジェクトを変換します。</span><span class="sxs-lookup"><span data-stu-id="7611a-122">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="7611a-123">[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7611a-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7611a-124">電子メールメッセージオブジェクトに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="7611a-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7611a-125">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="7611a-125">Header files</span></span>

<span data-ttu-id="7611a-126">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7611a-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="7611a-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="7611a-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="7611a-128">Mapitags</span><span class="sxs-lookup"><span data-stu-id="7611a-128">Mapitags.h</span></span>
  
> <span data-ttu-id="7611a-129">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7611a-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7611a-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="7611a-130">See also</span></span>



[<span data-ttu-id="7611a-131">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="7611a-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7611a-132">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="7611a-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7611a-133">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="7611a-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7611a-134">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="7611a-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

