---
title: PidTagAttachRendering 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachRendering
api_type:
- HeaderDef
ms.assetid: 1f31f7f4-fbda-4337-95e5-5474dd1bf84a
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 45d4b0bfe7f902ee2cfe1d735c990d80f8fbb60d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588945"
---
# <a name="pidtagattachrendering-canonical-property"></a><span data-ttu-id="1ea91-103">PidTagAttachRendering 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1ea91-103">PidTagAttachRendering Canonical Property</span></span>

  
  
<span data-ttu-id="1ea91-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1ea91-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1ea91-105">添付ファイルの表示情報を使用して Microsoft Windows メタファイルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="1ea91-105">Contains a Microsoft Windows metafile with rendering information for an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1ea91-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="1ea91-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1ea91-107">PR_ATTACH_RENDERING</span><span class="sxs-lookup"><span data-stu-id="1ea91-107">PR_ATTACH_RENDERING</span></span>  <br/> |
|<span data-ttu-id="1ea91-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="1ea91-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1ea91-109">0x3709</span><span class="sxs-lookup"><span data-stu-id="1ea91-109">0x3709</span></span>  <br/> |
|<span data-ttu-id="1ea91-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="1ea91-110">Data type:</span></span>  <br/> |<span data-ttu-id="1ea91-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="1ea91-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="1ea91-112">領域:</span><span class="sxs-lookup"><span data-stu-id="1ea91-112">Area:</span></span>  <br/> |<span data-ttu-id="1ea91-113">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="1ea91-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1ea91-114">注釈</span><span class="sxs-lookup"><span data-stu-id="1ea91-114">Remarks</span></span>

<span data-ttu-id="1ea91-115">このプロパティの目的は、アイコン、またはその他の添付ファイルの時点で親のメッセージ内で表示可能な図で表現を提供することにします。</span><span class="sxs-lookup"><span data-stu-id="1ea91-115">The purpose of this property is to provide an icon or other pictorial representation that can be displayed within the parent message at the point of attachment.</span></span> <span data-ttu-id="1ea91-116">通常、このような表現には、存在する場合、添付ファイルの名前や、Microsoft Office Word 文書の添付ファイルの内容が含まれます。</span><span class="sxs-lookup"><span data-stu-id="1ea91-116">Such representation typically includes the name of the attachment, if any, and the nature of the attachment, such as a Microsoft Office Word document.</span></span> <span data-ttu-id="1ea91-117">クライアント アプリケーションは、メッセージの表示で、この表現を使用できます。</span><span class="sxs-lookup"><span data-stu-id="1ea91-117">A client application can use this representation in the display of the message.</span></span> 
  
<span data-ttu-id="1ea91-118">添付ファイルの場合、このプロパティは通常、ファイルのアイコンを示します。</span><span class="sxs-lookup"><span data-stu-id="1ea91-118">For an attached file, this property usually portrays an icon for the file.</span></span> 
  
<span data-ttu-id="1ea91-119">添付されているメッセージでは、このプロパティは、通常設定されません。</span><span class="sxs-lookup"><span data-stu-id="1ea91-119">For an attached message, this property is typically not set.</span></span> <span data-ttu-id="1ea91-120">添付メッセージをレンダリングする必要があるクライアント アプリケーションは、 **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) のプロパティを取得する必要があります、 [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md)を対応するフォームについては、オブジェクトへのポインターの呼び出し、そのオブジェクトの[IMAPIFormInfo](imapiforminfoimapiprop.md)インターフェイスを開き、 **GetProps**を使用して、 **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) または**PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) のプロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="1ea91-120">A client application needing to render an attached message should obtain its **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property, call [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) for a pointer to the corresponding form information object, open the [IMAPIFormInfo](imapiforminfoimapiprop.md) interface on that object, and use **GetProps** to retrieve the **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) or **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="1ea91-121">埋め込み静的 OLE オブジェクトは、このプロパティには、ウィンドウで、添付ファイルの形式を描画に使用できる Microsoft Windows メタファイルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="1ea91-121">For an embedded static OLE object, this property contains a Microsoft Windows metafile that can be used to draw the attachment representation in a window.</span></span> 
  
<span data-ttu-id="1ea91-122">動的埋め込み OLE オブジェクトをクライアントは、レンダリング情報を生成するのに OLE データを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1ea91-122">For an embedded dynamic OLE object, the client should use the OLE data to generate the rendering information.</span></span> 
  
<span data-ttu-id="1ea91-123">すべての場合、クライアント アプリケーションはこのプロパティがいくつかの数百バイトのサイズは、通常、添付ファイル テーブルの切り捨ての対象となることに注意することはあります。</span><span class="sxs-lookup"><span data-stu-id="1ea91-123">In all cases, the client application should be aware that this property is usually several hundred bytes in size and is subject to truncation in the attachment table.</span></span> <span data-ttu-id="1ea91-124">クライアント自体の添付ファイルを開かずにこのプロパティから添付ファイルをレンダリングする場合は、テーブルの切り捨てルール内で作業する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1ea91-124">If a client wishes to render the attachment from this property without opening the attachment itself, it must work within the table truncation rule.</span></span> <span data-ttu-id="1ea91-125">詳細については、[大規模な列の使用](working-with-large-columns.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1ea91-125">For more information, see [Working with Large Columns](working-with-large-columns.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1ea91-126">関連リソース</span><span class="sxs-lookup"><span data-stu-id="1ea91-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1ea91-127">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="1ea91-127">Protocol specifications</span></span>

<span data-ttu-id="1ea91-128">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1ea91-128">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1ea91-129">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="1ea91-129">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1ea91-130">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="1ea91-130">Header files</span></span>

<span data-ttu-id="1ea91-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1ea91-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="1ea91-132">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="1ea91-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="1ea91-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1ea91-133">Mapitags.h</span></span>
  
> <span data-ttu-id="1ea91-134">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1ea91-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1ea91-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="1ea91-135">See also</span></span>



[<span data-ttu-id="1ea91-136">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="1ea91-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1ea91-137">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="1ea91-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1ea91-138">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1ea91-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1ea91-139">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1ea91-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

