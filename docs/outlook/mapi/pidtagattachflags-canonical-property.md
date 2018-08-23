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
ms.openlocfilehash: bf92e62dc572a81b6e0aab4cb1b0fc8afe97800d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573097"
---
# <a name="pidtagattachflags-canonical-property"></a><span data-ttu-id="5009f-103">PidTagAttachFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5009f-103">PidTagAttachFlags Canonical Property</span></span>

  
  
<span data-ttu-id="5009f-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5009f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5009f-105">添付ファイルのフラグのビットマスクを格納します。</span><span class="sxs-lookup"><span data-stu-id="5009f-105">Contains a bitmask of flags for an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5009f-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="5009f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5009f-107">PR_ATTACH_FLAGS</span><span class="sxs-lookup"><span data-stu-id="5009f-107">PR_ATTACH_FLAGS</span></span>  <br/> |
|<span data-ttu-id="5009f-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="5009f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5009f-109">0x3714</span><span class="sxs-lookup"><span data-stu-id="5009f-109">0x3714</span></span>  <br/> |
|<span data-ttu-id="5009f-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="5009f-110">Data type:</span></span>  <br/> |<span data-ttu-id="5009f-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="5009f-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="5009f-112">領域:</span><span class="sxs-lookup"><span data-stu-id="5009f-112">Area:</span></span>  <br/> |<span data-ttu-id="5009f-113">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="5009f-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5009f-114">注釈</span><span class="sxs-lookup"><span data-stu-id="5009f-114">Remarks</span></span>

<span data-ttu-id="5009f-115">このプロパティが使用される MHTML をサポートするためです。</span><span class="sxs-lookup"><span data-stu-id="5009f-115">This property is used for MHTML support.</span></span> 
  
<span data-ttu-id="5009f-116">**PR_ATTACH_FLAGS**ビットマスクについては、次のフラグの 1 つ以上を設定できます。</span><span class="sxs-lookup"><span data-stu-id="5009f-116">One or more of the following flags can be set for the **PR_ATTACH_FLAGS** bitmask:</span></span> 
  
<span data-ttu-id="5009f-117">ATT_INVISIBLE_IN_HTML</span><span class="sxs-lookup"><span data-stu-id="5009f-117">ATT_INVISIBLE_IN_HTML</span></span> 
  
> <span data-ttu-id="5009f-118">この添付ファイルが HTML のレンダリング アプリケーションで使用可能ではありませんし、多目的インターネット メール拡張機能 (MIME) の処理で無視するかを示します。</span><span class="sxs-lookup"><span data-stu-id="5009f-118">Indicates that this attachment is not available to HTML rendering applications and should be ignored in Multipurpose Internet Mail Extensions (MIME) processing.</span></span> 
    
<span data-ttu-id="5009f-119">ATT_INVISIBLE_IN_RTF</span><span class="sxs-lookup"><span data-stu-id="5009f-119">ATT_INVISIBLE_IN_RTF</span></span> 
  
> <span data-ttu-id="5009f-120">この添付ファイルをリッチ テキスト形式 (RTF) でのレンダリング アプリケーションで使用可能ではありませんし、MAPI によって無視されることを示します。</span><span class="sxs-lookup"><span data-stu-id="5009f-120">Indicates that this attachment is not available to applications rendering in Rich Text Format (RTF) and should be ignored by MAPI.</span></span>
    
<span data-ttu-id="5009f-121">**PR_ATTACH_FLAGS**プロパティが 0 の場合または省略すると、添付ファイルでは、すべてのアプリケーションによって処理されます。</span><span class="sxs-lookup"><span data-stu-id="5009f-121">If the **PR_ATTACH_FLAGS** property is zero or absent, the attachment is to be processed by all applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="5009f-122">関連リソース</span><span class="sxs-lookup"><span data-stu-id="5009f-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5009f-123">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="5009f-123">Protocol specifications</span></span>

<span data-ttu-id="5009f-124">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5009f-124">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5009f-125">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="5009f-125">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5009f-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="5009f-126">Header files</span></span>

<span data-ttu-id="5009f-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5009f-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="5009f-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="5009f-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="5009f-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5009f-129">Mapitags.h</span></span>
  
> <span data-ttu-id="5009f-130">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="5009f-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5009f-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="5009f-131">See also</span></span>



[<span data-ttu-id="5009f-132">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="5009f-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5009f-133">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="5009f-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5009f-134">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="5009f-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5009f-135">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="5009f-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

