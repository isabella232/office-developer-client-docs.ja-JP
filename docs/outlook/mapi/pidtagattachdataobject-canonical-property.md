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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3961330476cad8947f94152e49c90adb1e8f8b21
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339285"
---
# <a name="pidtagattachdataobject-canonical-property"></a><span data-ttu-id="57860-103">PidTagAttachDataObject 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="57860-103">PidTagAttachDataObject Canonical Property</span></span>

  
  
<span data-ttu-id="57860-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="57860-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="57860-105">通常、オブジェクト リンクおよび埋め込み (OLE) **IStorage** インターフェイスを介してアクセスされる添付ファイル オブジェクトが含まれる。</span><span class="sxs-lookup"><span data-stu-id="57860-105">Contains an attachment object typically accessed through the Object Linking and Embedding (OLE) **IStorage** interface.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="57860-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="57860-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="57860-107">PR_ATTACH_DATA_OBJ</span><span class="sxs-lookup"><span data-stu-id="57860-107">PR_ATTACH_DATA_OBJ</span></span>  <br/> |
|<span data-ttu-id="57860-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="57860-108">Identifier:</span></span>  <br/> |<span data-ttu-id="57860-109">0x3701</span><span class="sxs-lookup"><span data-stu-id="57860-109">0x3701</span></span>  <br/> |
|<span data-ttu-id="57860-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="57860-110">Data type:</span></span>  <br/> |<span data-ttu-id="57860-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="57860-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="57860-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="57860-112">Area:</span></span>  <br/> |<span data-ttu-id="57860-113">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="57860-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="57860-114">注釈</span><span class="sxs-lookup"><span data-stu-id="57860-114">Remarks</span></span>

<span data-ttu-id="57860-115">このプロパティは、PR_ATTACH_METHOD **(** [PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) プロパティの値が **ATTACH_EMBEDDED_MSGまたは** ATTACH_OLE。 </span><span class="sxs-lookup"><span data-stu-id="57860-115">This property holds the attachment when the value of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) property is **ATTACH_EMBEDDED_MSG** or **ATTACH_OLE**.</span></span> <span data-ttu-id="57860-116">OLE エンコードの種類は[、(PidTagAttachTag)](pidtagattachtag-canonical-property.md)PR_ATTACH_TAGから決定できます。 </span><span class="sxs-lookup"><span data-stu-id="57860-116">The OLE encoding type can be determined from **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)).</span></span> 
  
<span data-ttu-id="57860-117">ATTACH_EMBEDDED_MSG値に関連 **付けられた** 添付ファイルの場合 [、IMessage:IMAPIProp](imessageimapiprop.md) インターフェイスを使用して、アクセスを高速化できます。</span><span class="sxs-lookup"><span data-stu-id="57860-117">For an attachment associated with the **ATTACH_EMBEDDED_MSG** value, the [IMessage:IMAPIProp](imessageimapiprop.md) interface can be used for faster access.</span></span> 
  
<span data-ttu-id="57860-118">埋め込み動的 OLE オブジェクトの **場合、PR_ATTACH_DATA_OBJ** プロパティには独自のレンダリング情報が含まれているので **、PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) プロパティは存在しないか空にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="57860-118">For an embedded dynamic OLE object, the **PR_ATTACH_DATA_OBJ** property contains its own rendering information, and the **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) property should be either nonexistent or empty.</span></span> 
  
<span data-ttu-id="57860-119">OLE ドキュメント ファイル添付ファイルの場合、メッセージ ストア プロバイダーは PR_ATTACH_DATA_OBJ の [IMAPIProp::OpenProperty](imapiprop-openproperty.md)呼び出しに応答する必要があります。オプションで **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary)](pidtagattachdatabinary-canonical-property.md)の呼び出しに応答できます。 </span><span class="sxs-lookup"><span data-stu-id="57860-119">For an OLE document file attachment, the message store provider must respond to an [IMAPIProp::OpenProperty](imapiprop-openproperty.md) call on **PR_ATTACH_DATA_OBJ** and may optionally respond to a call on **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)).</span></span> <span data-ttu-id="57860-120">プロパティ **PR_ATTACH_DATA_BIN** プロパティ **PR_ATTACH_DATA_OBJ** 同じプロパティ識別子を共有するため、同じプロパティの 2 つの表示です。</span><span class="sxs-lookup"><span data-stu-id="57860-120">The **PR_ATTACH_DATA_BIN** and **PR_ATTACH_DATA_OBJ** properties share the same property identifier and thus are two renditions of the same property.</span></span> 
  
<span data-ttu-id="57860-121">OLE 2.0 docfile 形式の複合ファイルなどのストレージ オブジェクトの場合、一部のサービス プロバイダーでは、パフォーマンスを最適化するように設計された、追加のメンバーを持つ **IStream** のサブクラスである MAPI **IStreamDocfile** インターフェイスで開くこともできます。</span><span class="sxs-lookup"><span data-stu-id="57860-121">For a storage object, such as a compound file in OLE 2.0 docfile format, some service providers allow it to be opened with the MAPI **IStreamDocfile** interface, a subclass of **IStream** with no additional members, designed to optimize performance.</span></span> <span data-ttu-id="57860-122">潜在的な保存は、IStreamDocfile を介してファイルを開PR_ATTACH_DATA_OBJ **正当化するのに十分です**。</span><span class="sxs-lookup"><span data-stu-id="57860-122">The potential saving is enough to justify attempting to open **PR_ATTACH_DATA_OBJ** through **IStreamDocfile**.</span></span> <span data-ttu-id="57860-123">この **MAPI_E_INTERFACE_NOT_SUPPORTED** 返された場合、クライアントは IStream **を使用** してPR_ATTACH_DATA_BIN **を開きます**。</span><span class="sxs-lookup"><span data-stu-id="57860-123">If **MAPI_E_INTERFACE_NOT_SUPPORTED** is returned, the client can then open **PR_ATTACH_DATA_BIN** with **IStream**.</span></span> 
  
<span data-ttu-id="57860-124">クライアント アプリケーションまたはサービス プロバイダーが、PR_ATTACH_DATA_OBJ のヘルプを使用して添付ファイル サブオブジェクトを開 **PR_ATTACH_METHOD場合は**、PR_ATTACH_DATA_BIN を **使用する必要があります**。</span><span class="sxs-lookup"><span data-stu-id="57860-124">If the client application or service provider cannot open an attachment subobject by using **PR_ATTACH_DATA_OBJ** with the help of **PR_ATTACH_METHOD**, it should use **PR_ATTACH_DATA_BIN**.</span></span> 
  
<span data-ttu-id="57860-125">OLE インターフェイスと形式の詳細については、「OLE と [データ転送」を参照してください](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx)。</span><span class="sxs-lookup"><span data-stu-id="57860-125">For more information on OLE interfaces and formats, see [OLE and Data Transfer](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="57860-126">関連リソース</span><span class="sxs-lookup"><span data-stu-id="57860-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="57860-127">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="57860-127">Protocol specifications</span></span>

<span data-ttu-id="57860-128">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="57860-128">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="57860-129">メッセージ オブジェクトと添付ファイル オブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="57860-129">Handles message and attachment objects.</span></span>
    
## <a name="header-files"></a><span data-ttu-id="57860-130">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="57860-130">Header Files</span></span>

<span data-ttu-id="57860-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="57860-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="57860-132">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="57860-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="57860-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="57860-133">Mapitags.h</span></span>
  
> <span data-ttu-id="57860-134">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="57860-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="57860-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="57860-135">See also</span></span>



[<span data-ttu-id="57860-136">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="57860-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="57860-137">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="57860-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="57860-138">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="57860-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="57860-139">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="57860-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

