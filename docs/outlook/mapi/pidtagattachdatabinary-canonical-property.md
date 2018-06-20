---
title: PidTagAttachDataBinary の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachDataBinary
api_type:
- HeaderDef
ms.assetid: 3b0a8b28-863e-4b96-a4c0-fdb8f40555b9
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 3646f3e3906e62fe148fe1c2b6ddca39013391e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802469"
---
# <a name="pidtagattachdatabinary-canonical-property"></a><span data-ttu-id="4740c-103">PidTagAttachDataBinary の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="4740c-103">PidTagAttachDataBinary Canonical Property</span></span>

  
  
<span data-ttu-id="4740c-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4740c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4740c-105">通常、オブジェクトのリンクと埋め込み (OLE) の**IStream**インターフェイスを使用してアクセス バイナリ添付ファイルのデータが含まれています。</span><span class="sxs-lookup"><span data-stu-id="4740c-105">Contains binary attachment data typically accessed through the Object Linking and Embedding (OLE) **IStream** interface.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4740c-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="4740c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4740c-107">PR_ATTACH_DATA_BIN</span><span class="sxs-lookup"><span data-stu-id="4740c-107">PR_ATTACH_DATA_BIN</span></span>  <br/> |
|<span data-ttu-id="4740c-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="4740c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4740c-109">0x3701</span><span class="sxs-lookup"><span data-stu-id="4740c-109">0x3701</span></span>  <br/> |
|<span data-ttu-id="4740c-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="4740c-110">Data type:</span></span>  <br/> |<span data-ttu-id="4740c-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="4740c-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="4740c-112">領域:</span><span class="sxs-lookup"><span data-stu-id="4740c-112">Area:</span></span>  <br/> |<span data-ttu-id="4740c-113">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="4740c-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4740c-114">備考</span><span class="sxs-lookup"><span data-stu-id="4740c-114">Remarks</span></span>

<span data-ttu-id="4740c-115">**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) プロパティの値では、ATTACH_BY_VALUE、通常の添付ファイルのメソッドと 1 つだけをサポートする必要がある場合、このプロパティは、添付ファイルを保持します。</span><span class="sxs-lookup"><span data-stu-id="4740c-115">This property holds the attachment when the value of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) property is ATTACH_BY_VALUE, which is the usual attachment method and the only one required to be supported.</span></span> <span data-ttu-id="4740c-116">**PR_ATTACH_DATA_BIN**は、 **PR_ATTACH_METHOD**の値が ATTACH_OLE である場合にも OLE 1.0 **OLESTREAM**の添付ファイルを保持します。</span><span class="sxs-lookup"><span data-stu-id="4740c-116">**PR_ATTACH_DATA_BIN** also holds an OLE 1.0 **OLESTREAM** attachment when the value of **PR_ATTACH_METHOD** is ATTACH_OLE.</span></span> 
  
 <span data-ttu-id="4740c-117">**OLESTREAM**の添付ファイルは、OLE **IStream::CopyTo**メソッドを呼び出すことによって、ファイルにコピーすることができます。</span><span class="sxs-lookup"><span data-stu-id="4740c-117">**OLESTREAM** attachments can be copied into a file by calling the OLE **IStream::CopyTo** method.</span></span> <span data-ttu-id="4740c-118">エンコードの種類の OLE は、 **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) のプロパティから確認できます。</span><span class="sxs-lookup"><span data-stu-id="4740c-118">The OLE encoding type can be determined from the **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="4740c-119">ファイルに添付ファイル、OLE ドキュメントのメッセージ ストア プロバイダーは**PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) で、 [IMAPIProp::OpenProperty](imapiprop-openproperty.md)の呼び出しに応答する必要があり、PR_ATTACH_DATA_BIN を**の呼び出しに応答可能性があります (オプション)**.</span><span class="sxs-lookup"><span data-stu-id="4740c-119">For an OLE document file attachment, the message store provider must respond to an [IMAPIProp::OpenProperty](imapiprop-openproperty.md) call on **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) and may optionally respond to a call on **PR_ATTACH_DATA_BIN**.</span></span> <span data-ttu-id="4740c-120">**PR_ATTACH_DATA_BIN**と**PR_ATTACH_DATA_OBJ**同じプロパティの識別子を共有し、したがって、同じプロパティの 2 つのレンディションは、注意してください。</span><span class="sxs-lookup"><span data-stu-id="4740c-120">Note that **PR_ATTACH_DATA_BIN** and **PR_ATTACH_DATA_OBJ** share the same property identifier and thus are two renditions of the same property.</span></span> 
  
<span data-ttu-id="4740c-121">ストレージ ・ オブジェクト、OLE 2.0 のドキュメント形式、複合ファイルなど一部のサービス プロバイダーを許可パフォーマンス向上のため**IStreamDocfile**の MAPI インターフェイスを使用して開くことができません。</span><span class="sxs-lookup"><span data-stu-id="4740c-121">For a storage object, such as a compound file in OLE 2.0 docfile format, some service providers allow it to be opened with the MAPI **IStreamDocfile** interface for improved performance.</span></span> <span data-ttu-id="4740c-122">**IStreamDocfile**をサポートするプロバイダーは、 **PR_ATTACH_DATA_OBJ**上に公開する必要があり、 **PR_ATTACH_DATA_BIN**を失う必要に応じて可能性があります。</span><span class="sxs-lookup"><span data-stu-id="4740c-122">A provider that supports **IStreamDocfile** must expose it on **PR_ATTACH_DATA_OBJ** and may optionally expose it on **PR_ATTACH_DATA_BIN**.</span></span> 
  
<span data-ttu-id="4740c-123">OLE インターフェイスとフォーマットの詳細については、 [OLE アプリケーションとデータの転送](http://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4740c-123">For more information on OLE interfaces and formats, see [OLE and Data Transfer](http://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="4740c-124">関連リソース</span><span class="sxs-lookup"><span data-stu-id="4740c-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4740c-125">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="4740c-125">Protocol specifications</span></span>

<span data-ttu-id="4740c-126">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4740c-126">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4740c-127">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="4740c-127">Handles message and attachment objects.</span></span>
    
## <a name="header-files"></a><span data-ttu-id="4740c-128">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="4740c-128">Header Files</span></span>

<span data-ttu-id="4740c-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4740c-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="4740c-130">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="4740c-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="4740c-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4740c-131">Mapitags.h</span></span>
  
> <span data-ttu-id="4740c-132">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4740c-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4740c-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="4740c-133">See also</span></span>



[<span data-ttu-id="4740c-134">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="4740c-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4740c-135">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="4740c-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4740c-136">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="4740c-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4740c-137">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="4740c-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

