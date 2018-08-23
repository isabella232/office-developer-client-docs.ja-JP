---
title: PidTagAttachDataObject 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachDataObject
api_type:
- HeaderDef
ms.assetid: b76312c6-7682-4ded-be25-55e21b0b091b
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d2926b09dd3dfd89ab771206e0c8848415238eba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585480"
---
# <a name="pidtagattachdataobject-canonical-property"></a><span data-ttu-id="eeca8-103">PidTagAttachDataObject 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="eeca8-103">PidTagAttachDataObject Canonical Property</span></span>

  
  
<span data-ttu-id="eeca8-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eeca8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eeca8-105">通常、オブジェクトのリンクと埋め込み (OLE) **IStorage**インターフェイスを使用してアクセスの添付ファイル オブジェクトが含まれています。</span><span class="sxs-lookup"><span data-stu-id="eeca8-105">Contains an attachment object typically accessed through the Object Linking and Embedding (OLE) **IStorage** interface.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="eeca8-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="eeca8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="eeca8-107">PR_ATTACH_DATA_OBJ</span><span class="sxs-lookup"><span data-stu-id="eeca8-107">PR_ATTACH_DATA_OBJ</span></span>  <br/> |
|<span data-ttu-id="eeca8-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="eeca8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="eeca8-109">0x3701</span><span class="sxs-lookup"><span data-stu-id="eeca8-109">0x3701</span></span>  <br/> |
|<span data-ttu-id="eeca8-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="eeca8-110">Data type:</span></span>  <br/> |<span data-ttu-id="eeca8-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="eeca8-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="eeca8-112">領域:</span><span class="sxs-lookup"><span data-stu-id="eeca8-112">Area:</span></span>  <br/> |<span data-ttu-id="eeca8-113">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="eeca8-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="eeca8-114">注釈</span><span class="sxs-lookup"><span data-stu-id="eeca8-114">Remarks</span></span>

<span data-ttu-id="eeca8-115">**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) プロパティの値が**ATTACH_EMBEDDED_MSG**または**ATTACH_OLE**である場合、このプロパティは、添付ファイルを保持します。</span><span class="sxs-lookup"><span data-stu-id="eeca8-115">This property holds the attachment when the value of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) property is **ATTACH_EMBEDDED_MSG** or **ATTACH_OLE**.</span></span> <span data-ttu-id="eeca8-116">**PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) からは、OLE のエンコードの種類を決定できます。</span><span class="sxs-lookup"><span data-stu-id="eeca8-116">The OLE encoding type can be determined from **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)).</span></span> 
  
<span data-ttu-id="eeca8-117">**ATTACH_EMBEDDED_MSG**の値に関連付けられている添付ファイルの高速アクセスの[IMessage:IMAPIProp](imessageimapiprop.md)インターフェイスを使用できます。</span><span class="sxs-lookup"><span data-stu-id="eeca8-117">For an attachment associated with the **ATTACH_EMBEDDED_MSG** value, the [IMessage:IMAPIProp](imessageimapiprop.md) interface can be used for faster access.</span></span> 
  
<span data-ttu-id="eeca8-118">埋め込み動的 OLE オブジェクトは、 **PR_ATTACH_DATA_OBJ**プロパティには、独自のレンダリング情報が含まれています、 **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) のプロパティが存在しないか、または空にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="eeca8-118">For an embedded dynamic OLE object, the **PR_ATTACH_DATA_OBJ** property contains its own rendering information, and the **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) property should be either nonexistent or empty.</span></span> 
  
<span data-ttu-id="eeca8-119">ファイルに添付ファイル、OLE ドキュメントのメッセージ ストア プロバイダーが**PR_ATTACH_DATA_OBJ**で、 [IMAPIProp::OpenProperty](imapiprop-openproperty.md)の呼び出しに応答する必要があり、 **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)の呼び出しに応答可能性があります (オプション)).</span><span class="sxs-lookup"><span data-stu-id="eeca8-119">For an OLE document file attachment, the message store provider must respond to an [IMAPIProp::OpenProperty](imapiprop-openproperty.md) call on **PR_ATTACH_DATA_OBJ** and may optionally respond to a call on **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)).</span></span> <span data-ttu-id="eeca8-120">**PR_ATTACH_DATA_BIN**と**PR_ATTACH_DATA_OBJ**のプロパティは、同じプロパティの識別子を共有し、したがって、同じプロパティの 2 つのレンディションは、します。</span><span class="sxs-lookup"><span data-stu-id="eeca8-120">The **PR_ATTACH_DATA_BIN** and **PR_ATTACH_DATA_OBJ** properties share the same property identifier and thus are two renditions of the same property.</span></span> 
  
<span data-ttu-id="eeca8-121">ストレージ オブジェクトでは、OLE 2.0 のドキュメント形式、複合ファイルなど一部のサービス プロバイダーを許可しないメンバーを追加して、パフォーマンスを最適化するように設計された**IStream**のサブクラスである MAPI **IStreamDocfile**インターフェイスを使用して開くことができません。</span><span class="sxs-lookup"><span data-stu-id="eeca8-121">For a storage object, such as a compound file in OLE 2.0 docfile format, some service providers allow it to be opened with the MAPI **IStreamDocfile** interface, a subclass of **IStream** with no additional members, designed to optimize performance.</span></span> <span data-ttu-id="eeca8-122">潜在的な保存は、 **IStreamDocfile**から**PR_ATTACH_DATA_OBJ**を開こうとして正当性を確保します。</span><span class="sxs-lookup"><span data-stu-id="eeca8-122">The potential saving is enough to justify attempting to open **PR_ATTACH_DATA_OBJ** through **IStreamDocfile**.</span></span> <span data-ttu-id="eeca8-123">**MAPI_E_INTERFACE_NOT_SUPPORTED**が返された場合、クライアントが**IStream**に**PR_ATTACH_DATA_BIN**を開くことができますし。</span><span class="sxs-lookup"><span data-stu-id="eeca8-123">If **MAPI_E_INTERFACE_NOT_SUPPORTED** is returned, the client can then open **PR_ATTACH_DATA_BIN** with **IStream**.</span></span> 
  
<span data-ttu-id="eeca8-124">クライアント アプリケーションまたはサービス プロバイダーは、 **PR_ATTACH_METHOD**の**PR_ATTACH_DATA_OBJ**を使用して、添付ファイルのサブオブジェクトを開くことができません、 **PR_ATTACH_DATA_BIN**を使用してください。</span><span class="sxs-lookup"><span data-stu-id="eeca8-124">If the client application or service provider cannot open an attachment subobject by using **PR_ATTACH_DATA_OBJ** with the help of **PR_ATTACH_METHOD**, it should use **PR_ATTACH_DATA_BIN**.</span></span> 
  
<span data-ttu-id="eeca8-125">OLE インターフェイスとフォーマットの詳細については、 [OLE アプリケーションとデータの転送](http://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="eeca8-125">For more information on OLE interfaces and formats, see [OLE and Data Transfer](http://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="eeca8-126">関連リソース</span><span class="sxs-lookup"><span data-stu-id="eeca8-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="eeca8-127">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="eeca8-127">Protocol specifications</span></span>

<span data-ttu-id="eeca8-128">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="eeca8-128">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="eeca8-129">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="eeca8-129">Handles message and attachment objects.</span></span>
    
## <a name="header-files"></a><span data-ttu-id="eeca8-130">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="eeca8-130">Header Files</span></span>

<span data-ttu-id="eeca8-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="eeca8-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="eeca8-132">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="eeca8-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="eeca8-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="eeca8-133">Mapitags.h</span></span>
  
> <span data-ttu-id="eeca8-134">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="eeca8-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="eeca8-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="eeca8-135">See also</span></span>



[<span data-ttu-id="eeca8-136">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="eeca8-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="eeca8-137">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="eeca8-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="eeca8-138">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="eeca8-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="eeca8-139">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="eeca8-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

