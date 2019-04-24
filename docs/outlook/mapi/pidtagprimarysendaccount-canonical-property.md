---
title: PidTagPrimarySendAccount 標準プロパティ
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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 2c32cc61fea63cd38215c30e04e8a467d4901cc9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339376"
---
# <a name="pidtagprimarysendaccount-canonical-property"></a><span data-ttu-id="2c620-103">PidTagPrimarySendAccount 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2c620-103">PidTagPrimarySendAccount Canonical Property</span></span>

  
  
<span data-ttu-id="2c620-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2c620-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2c620-105">メッセージの送信に使用される最初のサーバーの名前を示す文字列を格納します。</span><span class="sxs-lookup"><span data-stu-id="2c620-105">Contains a string that names the first server that is used to send the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2c620-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="2c620-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2c620-107">PR_PRIMARY_SEND_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="2c620-107">PR_PRIMARY_SEND_ACCOUNT</span></span>  <br/> |
|<span data-ttu-id="2c620-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="2c620-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2c620-109">0x0e28</span><span class="sxs-lookup"><span data-stu-id="2c620-109">0x0E28</span></span>  <br/> |
|<span data-ttu-id="2c620-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="2c620-110">Data type:</span></span>  <br/> |<span data-ttu-id="2c620-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2c620-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="2c620-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="2c620-112">Area:</span></span>  <br/> |<span data-ttu-id="2c620-113">アカウント</span><span class="sxs-lookup"><span data-stu-id="2c620-113">Account</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2c620-114">解説</span><span class="sxs-lookup"><span data-stu-id="2c620-114">Remarks</span></span>

<span data-ttu-id="2c620-115">クライアントがメールを送信するために使用する最初のサーバーを指定します。</span><span class="sxs-lookup"><span data-stu-id="2c620-115">Specifies the first server that a client should use to send the mail.</span></span> <span data-ttu-id="2c620-116">これらのプロパティの形式は、実装によって異なります。</span><span class="sxs-lookup"><span data-stu-id="2c620-116">The format of these properties is implementation dependent.</span></span> <span data-ttu-id="2c620-117">これらのプロパティは、クライアントがメールを送信するサーバーを決定するために使用できますが、オプションであり、値はサーバーには意味がありません。</span><span class="sxs-lookup"><span data-stu-id="2c620-117">These properties can be used by the client to determine which server to direct the mail through, but is optional and the value has no meaning to the server.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2c620-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="2c620-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2c620-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="2c620-119">Protocol specifications</span></span>

<span data-ttu-id="2c620-120">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2c620-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2c620-121">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="2c620-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2c620-122">[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2c620-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2c620-123">電子メールメッセージオブジェクトに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="2c620-123">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2c620-124">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="2c620-124">Header files</span></span>

<span data-ttu-id="2c620-125">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2c620-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="2c620-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="2c620-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="2c620-127">Mapitags</span><span class="sxs-lookup"><span data-stu-id="2c620-127">Mapitags.h</span></span>
  
> <span data-ttu-id="2c620-128">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="2c620-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2c620-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="2c620-129">See also</span></span>



[<span data-ttu-id="2c620-130">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="2c620-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2c620-131">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2c620-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2c620-132">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="2c620-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2c620-133">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="2c620-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

