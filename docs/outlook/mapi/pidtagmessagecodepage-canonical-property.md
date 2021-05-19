---
title: PidTagMessageCodepage 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageCodepage
api_type:
- HeaderDef
ms.assetid: eef73e34-470c-4c37-94ce-ea95fe83bc10
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 49f2c1c0b8af21f837582698763c17b9c41e1923
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358465"
---
# <a name="pidtagmessagecodepage-canonical-property"></a><span data-ttu-id="10f53-103">PidTagMessageCodepage 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="10f53-103">PidTagMessageCodepage Canonical Property</span></span>

  
  
<span data-ttu-id="10f53-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="10f53-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="10f53-105">メッセージに使用されるコード ページが含まれる。</span><span class="sxs-lookup"><span data-stu-id="10f53-105">Contains the code page that is used for the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="10f53-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="10f53-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="10f53-107">PR_MESSAGE_CODEPAGE</span><span class="sxs-lookup"><span data-stu-id="10f53-107">PR_MESSAGE_CODEPAGE</span></span>  <br/> |
|<span data-ttu-id="10f53-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="10f53-108">Identifier:</span></span>  <br/> |<span data-ttu-id="10f53-109">0x3FFD</span><span class="sxs-lookup"><span data-stu-id="10f53-109">0x3FFD</span></span>  <br/> |
|<span data-ttu-id="10f53-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="10f53-110">Data type:</span></span>  <br/> |<span data-ttu-id="10f53-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="10f53-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="10f53-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="10f53-112">Area:</span></span>  <br/> |<span data-ttu-id="10f53-113">共通</span><span class="sxs-lookup"><span data-stu-id="10f53-113">Common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="10f53-114">注釈</span><span class="sxs-lookup"><span data-stu-id="10f53-114">Remarks</span></span>

<span data-ttu-id="10f53-115">このプロパティがゼロ (0) に設定されている場合は、フォルダー オブジェクト コード ページが使用されます。</span><span class="sxs-lookup"><span data-stu-id="10f53-115">The folder object code page is used if this property is set to zero (0).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="10f53-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="10f53-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="10f53-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="10f53-117">Protocol specifications</span></span>

<span data-ttu-id="10f53-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="10f53-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="10f53-119">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="10f53-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="10f53-120">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="10f53-120">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="10f53-121">メッセージ オブジェクトと添付ファイル オブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="10f53-121">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="10f53-122">[[MS-OXPFOAB]](https://msdn.microsoft.com/library/258a07a7-34a7-4373-87c1-cddf51447d00%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="10f53-122">[[MS-OXPFOAB]](https://msdn.microsoft.com/library/258a07a7-34a7-4373-87c1-cddf51447d00%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="10f53-123">サーバーからクライアントにオフライン アドレス帳 (OAB) データを配信する方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="10f53-123">Specifies the method of delivering offline address book (OAB) data from server to client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="10f53-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="10f53-124">Header files</span></span>

<span data-ttu-id="10f53-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="10f53-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="10f53-126">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="10f53-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="10f53-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="10f53-127">Mapitags.h</span></span>
  
> <span data-ttu-id="10f53-128">関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="10f53-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="10f53-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="10f53-129">See also</span></span>



[<span data-ttu-id="10f53-130">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="10f53-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="10f53-131">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="10f53-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="10f53-132">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="10f53-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="10f53-133">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="10f53-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

