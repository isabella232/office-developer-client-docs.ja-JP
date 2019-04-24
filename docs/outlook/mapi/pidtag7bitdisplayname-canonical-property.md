---
title: PidTag7BitDisplayName 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTag7BitDisplayName
api_type:
- HeaderDef
ms.assetid: 803d7c4e-ed80-4d5b-988f-27068a8ccd63
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e5177d47749c2f60a883bd12fbba27045114c601
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315814"
---
# <a name="pidtag7bitdisplayname-canonical-property"></a><span data-ttu-id="f2c5b-103">PidTag7BitDisplayName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f2c5b-103">PidTag7BitDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="f2c5b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f2c5b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f2c5b-105">メッセージングユーザー名の7ビットの ASCII 表記を含みます。</span><span class="sxs-lookup"><span data-stu-id="f2c5b-105">Contains a 7-bit ASCII representation of a messaging user's name.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f2c5b-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="f2c5b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f2c5b-107">PR_7BIT_DISPLAY_NAME、PR_7BIT_DISPLAY_NAME_A、PR_7BIT_DISPLAY_NAME_W</span><span class="sxs-lookup"><span data-stu-id="f2c5b-107">PR_7BIT_DISPLAY_NAME, PR_7BIT_DISPLAY_NAME_A, PR_7BIT_DISPLAY_NAME_W</span></span>  <br/> |
|<span data-ttu-id="f2c5b-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="f2c5b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f2c5b-109">0x39ff</span><span class="sxs-lookup"><span data-stu-id="f2c5b-109">0x39FF</span></span>  <br/> |
|<span data-ttu-id="f2c5b-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="f2c5b-110">Data type:</span></span>  <br/> |<span data-ttu-id="f2c5b-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f2c5b-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="f2c5b-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="f2c5b-112">Area:</span></span>  <br/> |<span data-ttu-id="f2c5b-113">アドレス帳</span><span class="sxs-lookup"><span data-stu-id="f2c5b-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f2c5b-114">解説</span><span class="sxs-lookup"><span data-stu-id="f2c5b-114">Remarks</span></span>

<span data-ttu-id="f2c5b-115">これらのプロパティは、 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティを7ビット文字セットにマッピングします。</span><span class="sxs-lookup"><span data-stu-id="f2c5b-115">These properties map the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property into a 7-bit character set.</span></span> <span data-ttu-id="f2c5b-116">インターネットや特定の x-blade リンクなど、一部のメッセージングシステムは、128文字の7ビット ASCII コードセットに制限されています。</span><span class="sxs-lookup"><span data-stu-id="f2c5b-116">Some messaging systems, such as Internet and certain X.400 links, are limited to the 128-character 7-bit ASCII code set.</span></span> <span data-ttu-id="f2c5b-117">このようなメッセージングシステムへのゲートウェイは、 [IAddrBook::P reparerecips](iaddrbook-preparerecips.md)メソッドを直接呼び出してこのプロパティを取得することによって、パフォーマンスを向上させることができます。これにより、コード変換のためのその他の処理を回避できます。</span><span class="sxs-lookup"><span data-stu-id="f2c5b-117">Gateways to such messaging systems can improve their performance by calling the [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) method directly to retrieve the this property, thereby avoiding extra processing for code conversion.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f2c5b-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="f2c5b-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f2c5b-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="f2c5b-119">Protocol specifications</span></span>

<span data-ttu-id="f2c5b-120">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f2c5b-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f2c5b-121">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="f2c5b-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f2c5b-122">[[OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f2c5b-122">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f2c5b-123">ユーザー、連絡先、グループ、およびリソースのリストに対するプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="f2c5b-123">Specifies the properties and operations on lists of users, contacts, groups and resources.</span></span>
    
<span data-ttu-id="f2c5b-124">[[MS-CHAP]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f2c5b-124">[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f2c5b-125">クライアントの NSPI サーバーとの通信を処理します。</span><span class="sxs-lookup"><span data-stu-id="f2c5b-125">Handles a client's communications with an NSPI server.</span></span>
    
<span data-ttu-id="f2c5b-126">[[OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f2c5b-126">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f2c5b-127">クライアントとサーバーの間でデータを転送するために使用される順序とデータフローを処理します。</span><span class="sxs-lookup"><span data-stu-id="f2c5b-127">Handles the order and data flow that is used to transfers data between client and server.</span></span>
    
<span data-ttu-id="f2c5b-128">[[OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f2c5b-128">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f2c5b-129">メッセージと添付ファイルオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="f2c5b-129">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="f2c5b-130">[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f2c5b-130">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f2c5b-131">電子メールメッセージに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="f2c5b-131">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f2c5b-132">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="f2c5b-132">Header files</span></span>

<span data-ttu-id="f2c5b-133">Mapitags</span><span class="sxs-lookup"><span data-stu-id="f2c5b-133">Mapitags.h</span></span>
  
> <span data-ttu-id="f2c5b-134">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="f2c5b-134">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="f2c5b-135">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f2c5b-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="f2c5b-136">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="f2c5b-136">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f2c5b-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="f2c5b-137">See also</span></span>



[<span data-ttu-id="f2c5b-138">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="f2c5b-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f2c5b-139">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f2c5b-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f2c5b-140">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="f2c5b-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f2c5b-141">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="f2c5b-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

