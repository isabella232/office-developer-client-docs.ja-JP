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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: efccd75cce04e4e392a7fbd9feecc7c8b49ab57e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339334"
---
# <a name="pidtagattachflags-canonical-property"></a><span data-ttu-id="2b84a-103">PidTagAttachFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2b84a-103">PidTagAttachFlags Canonical Property</span></span>

  
  
<span data-ttu-id="2b84a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2b84a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2b84a-105">添付ファイルのフラグのビットマスクを含みます。</span><span class="sxs-lookup"><span data-stu-id="2b84a-105">Contains a bitmask of flags for an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2b84a-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="2b84a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2b84a-107">PR_ATTACH_FLAGS</span><span class="sxs-lookup"><span data-stu-id="2b84a-107">PR_ATTACH_FLAGS</span></span>  <br/> |
|<span data-ttu-id="2b84a-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="2b84a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2b84a-109">0x3714</span><span class="sxs-lookup"><span data-stu-id="2b84a-109">0x3714</span></span>  <br/> |
|<span data-ttu-id="2b84a-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="2b84a-110">Data type:</span></span>  <br/> |<span data-ttu-id="2b84a-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="2b84a-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="2b84a-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="2b84a-112">Area:</span></span>  <br/> |<span data-ttu-id="2b84a-113">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="2b84a-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2b84a-114">解説</span><span class="sxs-lookup"><span data-stu-id="2b84a-114">Remarks</span></span>

<span data-ttu-id="2b84a-115">このプロパティは、MHTML サポートに使用されます。</span><span class="sxs-lookup"><span data-stu-id="2b84a-115">This property is used for MHTML support.</span></span> 
  
<span data-ttu-id="2b84a-116">**PR_ATTACH_FLAGS**ビットマスクには、次の1つ以上のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="2b84a-116">One or more of the following flags can be set for the **PR_ATTACH_FLAGS** bitmask:</span></span> 
  
<span data-ttu-id="2b84a-117">ATT_INVISIBLE_IN_HTML</span><span class="sxs-lookup"><span data-stu-id="2b84a-117">ATT_INVISIBLE_IN_HTML</span></span> 
  
> <span data-ttu-id="2b84a-118">この添付ファイルは、HTML レンダリングアプリケーションでは使用できず、多目的インターネットメール Extensions (MIME) 処理で無視する必要があることを示します。</span><span class="sxs-lookup"><span data-stu-id="2b84a-118">Indicates that this attachment is not available to HTML rendering applications and should be ignored in Multipurpose Internet Mail Extensions (MIME) processing.</span></span> 
    
<span data-ttu-id="2b84a-119">ATT_INVISIBLE_IN_RTF</span><span class="sxs-lookup"><span data-stu-id="2b84a-119">ATT_INVISIBLE_IN_RTF</span></span> 
  
> <span data-ttu-id="2b84a-120">この添付ファイルは、リッチテキスト形式 (RTF) のアプリケーションでは使用できず、MAPI で無視する必要があることを示します。</span><span class="sxs-lookup"><span data-stu-id="2b84a-120">Indicates that this attachment is not available to applications rendering in Rich Text Format (RTF) and should be ignored by MAPI.</span></span>
    
<span data-ttu-id="2b84a-121">**PR_ATTACH_FLAGS**プロパティが0に設定されているか、存在しない場合、添付ファイルはすべてのアプリケーションによって処理されます。</span><span class="sxs-lookup"><span data-stu-id="2b84a-121">If the **PR_ATTACH_FLAGS** property is zero or absent, the attachment is to be processed by all applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="2b84a-122">関連リソース</span><span class="sxs-lookup"><span data-stu-id="2b84a-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2b84a-123">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="2b84a-123">Protocol specifications</span></span>

<span data-ttu-id="2b84a-124">[[OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2b84a-124">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2b84a-125">メッセージと添付ファイルオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="2b84a-125">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2b84a-126">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="2b84a-126">Header files</span></span>

<span data-ttu-id="2b84a-127">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2b84a-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="2b84a-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="2b84a-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="2b84a-129">Mapitags</span><span class="sxs-lookup"><span data-stu-id="2b84a-129">Mapitags.h</span></span>
  
> <span data-ttu-id="2b84a-130">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="2b84a-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2b84a-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="2b84a-131">See also</span></span>



[<span data-ttu-id="2b84a-132">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="2b84a-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2b84a-133">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2b84a-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2b84a-134">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="2b84a-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2b84a-135">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="2b84a-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

