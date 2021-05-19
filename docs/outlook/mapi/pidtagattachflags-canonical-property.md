---
title: PidTagAttachFlags 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachFlags
api_type:
- HeaderDef
ms.assetid: 47e01131-f399-43cb-9815-aba69638c3fb
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: efccd75cce04e4e392a7fbd9feecc7c8b49ab57e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339334"
---
# <a name="pidtagattachflags-canonical-property"></a><span data-ttu-id="15739-103">PidTagAttachFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="15739-103">PidTagAttachFlags Canonical Property</span></span>

  
  
<span data-ttu-id="15739-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="15739-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="15739-105">添付ファイルのフラグのビットマスクが含まれる。</span><span class="sxs-lookup"><span data-stu-id="15739-105">Contains a bitmask of flags for an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="15739-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="15739-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="15739-107">PR_ATTACH_FLAGS</span><span class="sxs-lookup"><span data-stu-id="15739-107">PR_ATTACH_FLAGS</span></span>  <br/> |
|<span data-ttu-id="15739-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="15739-108">Identifier:</span></span>  <br/> |<span data-ttu-id="15739-109">0x3714</span><span class="sxs-lookup"><span data-stu-id="15739-109">0x3714</span></span>  <br/> |
|<span data-ttu-id="15739-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="15739-110">Data type:</span></span>  <br/> |<span data-ttu-id="15739-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="15739-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="15739-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="15739-112">Area:</span></span>  <br/> |<span data-ttu-id="15739-113">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="15739-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="15739-114">注釈</span><span class="sxs-lookup"><span data-stu-id="15739-114">Remarks</span></span>

<span data-ttu-id="15739-115">このプロパティは、MHTML のサポートに使用されます。</span><span class="sxs-lookup"><span data-stu-id="15739-115">This property is used for MHTML support.</span></span> 
  
<span data-ttu-id="15739-116">次のフラグの 1 つ以上を、ビットマスクに **PR_ATTACH_FLAGS** できます。</span><span class="sxs-lookup"><span data-stu-id="15739-116">One or more of the following flags can be set for the **PR_ATTACH_FLAGS** bitmask:</span></span> 
  
<span data-ttu-id="15739-117">ATT_INVISIBLE_IN_HTML</span><span class="sxs-lookup"><span data-stu-id="15739-117">ATT_INVISIBLE_IN_HTML</span></span> 
  
> <span data-ttu-id="15739-118">この添付ファイルは HTML レンダリング アプリケーションでは使用できないので、多目的インターネット メール拡張機能 (MIME) 処理では無視する必要があります。</span><span class="sxs-lookup"><span data-stu-id="15739-118">Indicates that this attachment is not available to HTML rendering applications and should be ignored in Multipurpose Internet Mail Extensions (MIME) processing.</span></span> 
    
<span data-ttu-id="15739-119">ATT_INVISIBLE_IN_RTF</span><span class="sxs-lookup"><span data-stu-id="15739-119">ATT_INVISIBLE_IN_RTF</span></span> 
  
> <span data-ttu-id="15739-120">リッチ テキスト形式 (RTF) でレンダリングするアプリケーションではこの添付ファイルを使用できないので、MAPI では無視する必要があります。</span><span class="sxs-lookup"><span data-stu-id="15739-120">Indicates that this attachment is not available to applications rendering in Rich Text Format (RTF) and should be ignored by MAPI.</span></span>
    
<span data-ttu-id="15739-121">PR_ATTACH_FLAGS **プロパティが** 0 または不在の場合、添付ファイルは、すべてのアプリケーションによって処理されます。</span><span class="sxs-lookup"><span data-stu-id="15739-121">If the **PR_ATTACH_FLAGS** property is zero or absent, the attachment is to be processed by all applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="15739-122">関連リソース</span><span class="sxs-lookup"><span data-stu-id="15739-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="15739-123">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="15739-123">Protocol specifications</span></span>

<span data-ttu-id="15739-124">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="15739-124">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="15739-125">メッセージ オブジェクトと添付ファイル オブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="15739-125">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="15739-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="15739-126">Header files</span></span>

<span data-ttu-id="15739-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="15739-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="15739-128">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="15739-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="15739-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="15739-129">Mapitags.h</span></span>
  
> <span data-ttu-id="15739-130">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="15739-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="15739-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="15739-131">See also</span></span>



[<span data-ttu-id="15739-132">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="15739-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="15739-133">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="15739-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="15739-134">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="15739-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="15739-135">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="15739-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

