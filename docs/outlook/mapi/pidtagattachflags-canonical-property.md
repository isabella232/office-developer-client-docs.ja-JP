---
title: PidTagAttachFlags の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: b934f9694061e17118be35e3fabeeff3bbc61a37
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802467"
---
# <a name="pidtagattachflags-canonical-property"></a><span data-ttu-id="aefda-103">PidTagAttachFlags の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="aefda-103">PidTagAttachFlags Canonical Property</span></span>

  
  
<span data-ttu-id="aefda-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="aefda-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="aefda-105">添付ファイルのフラグのビットマスクを格納します。</span><span class="sxs-lookup"><span data-stu-id="aefda-105">Contains a bitmask of flags for an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="aefda-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="aefda-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="aefda-107">PR_ATTACH_FLAGS</span><span class="sxs-lookup"><span data-stu-id="aefda-107">PR_ATTACH_FLAGS</span></span>  <br/> |
|<span data-ttu-id="aefda-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="aefda-108">Identifier:</span></span>  <br/> |<span data-ttu-id="aefda-109">0x3714</span><span class="sxs-lookup"><span data-stu-id="aefda-109">0x3714</span></span>  <br/> |
|<span data-ttu-id="aefda-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="aefda-110">Data type:</span></span>  <br/> |<span data-ttu-id="aefda-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="aefda-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="aefda-112">領域:</span><span class="sxs-lookup"><span data-stu-id="aefda-112">Area:</span></span>  <br/> |<span data-ttu-id="aefda-113">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="aefda-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aefda-114">備考</span><span class="sxs-lookup"><span data-stu-id="aefda-114">Remarks</span></span>

<span data-ttu-id="aefda-115">このプロパティが使用される MHTML をサポートするためです。</span><span class="sxs-lookup"><span data-stu-id="aefda-115">This property is used for MHTML support.</span></span> 
  
<span data-ttu-id="aefda-116">**PR_ATTACH_FLAGS**ビットマスクについては、次のフラグの 1 つ以上を設定できます。</span><span class="sxs-lookup"><span data-stu-id="aefda-116">One or more of the following flags can be set for the **PR_ATTACH_FLAGS** bitmask:</span></span> 
  
<span data-ttu-id="aefda-117">ATT_INVISIBLE_IN_HTML</span><span class="sxs-lookup"><span data-stu-id="aefda-117">ATT_INVISIBLE_IN_HTML</span></span> 
  
> <span data-ttu-id="aefda-118">この添付ファイルが HTML のレンダリング アプリケーションで使用可能ではありませんし、多目的インターネット メール拡張機能 (MIME) の処理で無視するかを示します。</span><span class="sxs-lookup"><span data-stu-id="aefda-118">Indicates that this attachment is not available to HTML rendering applications and should be ignored in Multipurpose Internet Mail Extensions (MIME) processing.</span></span> 
    
<span data-ttu-id="aefda-119">ATT_INVISIBLE_IN_RTF</span><span class="sxs-lookup"><span data-stu-id="aefda-119">ATT_INVISIBLE_IN_RTF</span></span> 
  
> <span data-ttu-id="aefda-120">この添付ファイルをリッチ テキスト形式 (RTF) でのレンダリング アプリケーションで使用可能ではありませんし、MAPI によって無視されることを示します。</span><span class="sxs-lookup"><span data-stu-id="aefda-120">Indicates that this attachment is not available to applications rendering in Rich Text Format (RTF) and should be ignored by MAPI.</span></span>
    
<span data-ttu-id="aefda-121">**PR_ATTACH_FLAGS**プロパティが 0 の場合または省略すると、添付ファイルでは、すべてのアプリケーションによって処理されます。</span><span class="sxs-lookup"><span data-stu-id="aefda-121">If the **PR_ATTACH_FLAGS** property is zero or absent, the attachment is to be processed by all applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="aefda-122">関連リソース</span><span class="sxs-lookup"><span data-stu-id="aefda-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="aefda-123">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="aefda-123">Protocol specifications</span></span>

<span data-ttu-id="aefda-124">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aefda-124">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="aefda-125">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="aefda-125">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="aefda-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="aefda-126">Header files</span></span>

<span data-ttu-id="aefda-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="aefda-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="aefda-128">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="aefda-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="aefda-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="aefda-129">Mapitags.h</span></span>
  
> <span data-ttu-id="aefda-130">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="aefda-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="aefda-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="aefda-131">See also</span></span>



[<span data-ttu-id="aefda-132">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="aefda-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="aefda-133">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="aefda-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="aefda-134">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="aefda-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="aefda-135">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="aefda-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

