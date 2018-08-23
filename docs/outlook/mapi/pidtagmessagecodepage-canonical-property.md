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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3a343ba1a8ef5a10f23a17b5ac62fd8def5fa7f6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802968"
---
# <a name="pidtagmessagecodepage-canonical-property"></a><span data-ttu-id="c93c0-103">PidTagMessageCodepage 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c93c0-103">PidTagMessageCodepage Canonical Property</span></span>

  
  
<span data-ttu-id="c93c0-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c93c0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c93c0-105">メッセージに使用されるコード ページが含まれています。</span><span class="sxs-lookup"><span data-stu-id="c93c0-105">Contains the code page that is used for the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c93c0-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="c93c0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c93c0-107">PR_MESSAGE_CODEPAGE</span><span class="sxs-lookup"><span data-stu-id="c93c0-107">PR_MESSAGE_CODEPAGE</span></span>  <br/> |
|<span data-ttu-id="c93c0-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="c93c0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c93c0-109">0x3FFD</span><span class="sxs-lookup"><span data-stu-id="c93c0-109">0x3FFD</span></span>  <br/> |
|<span data-ttu-id="c93c0-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="c93c0-110">Data type:</span></span>  <br/> |<span data-ttu-id="c93c0-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c93c0-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c93c0-112">領域:</span><span class="sxs-lookup"><span data-stu-id="c93c0-112">Area:</span></span>  <br/> |<span data-ttu-id="c93c0-113">Common</span><span class="sxs-lookup"><span data-stu-id="c93c0-113">Common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c93c0-114">注釈</span><span class="sxs-lookup"><span data-stu-id="c93c0-114">Remarks</span></span>

<span data-ttu-id="c93c0-115">このプロパティをゼロ (0) に設定されている場合、フォルダーのオブジェクトのコード ページが使用されます。</span><span class="sxs-lookup"><span data-stu-id="c93c0-115">The folder object code page is used if this property is set to zero (0).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c93c0-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="c93c0-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c93c0-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="c93c0-117">Protocol specifications</span></span>

<span data-ttu-id="c93c0-118">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c93c0-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c93c0-119">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="c93c0-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c93c0-120">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c93c0-120">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c93c0-121">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="c93c0-121">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="c93c0-122">[[MS OXPFOAB]](http://msdn.microsoft.com/library/258a07a7-34a7-4373-87c1-cddf51447d00%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c93c0-122">[[MS-OXPFOAB]](http://msdn.microsoft.com/library/258a07a7-34a7-4373-87c1-cddf51447d00%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c93c0-123">オフライン アドレス帳 (OAB) のデータをサーバーからクライアントに配信する方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="c93c0-123">Specifies the method of delivering offline address book (OAB) data from server to client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c93c0-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="c93c0-124">Header files</span></span>

<span data-ttu-id="c93c0-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c93c0-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="c93c0-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="c93c0-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="c93c0-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c93c0-127">Mapitags.h</span></span>
  
> <span data-ttu-id="c93c0-128">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="c93c0-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c93c0-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="c93c0-129">See also</span></span>



[<span data-ttu-id="c93c0-130">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="c93c0-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c93c0-131">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="c93c0-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c93c0-132">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="c93c0-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c93c0-133">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="c93c0-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

