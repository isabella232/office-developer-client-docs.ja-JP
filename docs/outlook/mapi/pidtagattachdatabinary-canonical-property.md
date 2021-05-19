---
title: PidTagAttachDataBinary 標準プロパティ
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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 1a5f8688b8ea747590cf2a2d6d5efb271aa488f8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356547"
---
# <a name="pidtagattachdatabinary-canonical-property"></a><span data-ttu-id="38e4d-103">PidTagAttachDataBinary 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="38e4d-103">PidTagAttachDataBinary Canonical Property</span></span>

  
  
<span data-ttu-id="38e4d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="38e4d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="38e4d-105">通常、オブジェクト リンクおよび埋め込み (OLE) IStream インターフェイスを介してアクセスされるバイナリ添付ファイル データ **が格納** されます。</span><span class="sxs-lookup"><span data-stu-id="38e4d-105">Contains binary attachment data typically accessed through the Object Linking and Embedding (OLE) **IStream** interface.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="38e4d-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="38e4d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="38e4d-107">PR_ATTACH_DATA_BIN</span><span class="sxs-lookup"><span data-stu-id="38e4d-107">PR_ATTACH_DATA_BIN</span></span>  <br/> |
|<span data-ttu-id="38e4d-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="38e4d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="38e4d-109">0x3701</span><span class="sxs-lookup"><span data-stu-id="38e4d-109">0x3701</span></span>  <br/> |
|<span data-ttu-id="38e4d-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="38e4d-110">Data type:</span></span>  <br/> |<span data-ttu-id="38e4d-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="38e4d-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="38e4d-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="38e4d-112">Area:</span></span>  <br/> |<span data-ttu-id="38e4d-113">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="38e4d-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="38e4d-114">注釈</span><span class="sxs-lookup"><span data-stu-id="38e4d-114">Remarks</span></span>

<span data-ttu-id="38e4d-115">このプロパティは **、PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) プロパティの値が ATTACH_BY_VALUE の場合に添付ファイルを保持します。これは通常の添付メソッドであり、サポートするために必要な唯一のメソッドです。</span><span class="sxs-lookup"><span data-stu-id="38e4d-115">This property holds the attachment when the value of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) property is ATTACH_BY_VALUE, which is the usual attachment method and the only one required to be supported.</span></span> <span data-ttu-id="38e4d-116">**PR_ATTACH_DATA_BIN** の値が指定されている場合、OLE 1.0 **OLESTREAM** 添付 **ファイル** PR_ATTACH_METHOD保持ATTACH_OLE。</span><span class="sxs-lookup"><span data-stu-id="38e4d-116">**PR_ATTACH_DATA_BIN** also holds an OLE 1.0 **OLESTREAM** attachment when the value of **PR_ATTACH_METHOD** is ATTACH_OLE.</span></span> 
  
 <span data-ttu-id="38e4d-117">**OLESTREAM 添付** ファイルは、OLE **IStream::CopyTo** メソッドを呼び出すことによってファイルにコピーできます。</span><span class="sxs-lookup"><span data-stu-id="38e4d-117">**OLESTREAM** attachments can be copied into a file by calling the OLE **IStream::CopyTo** method.</span></span> <span data-ttu-id="38e4d-118">OLE エンコードの種類は、プロパティ ([PidTagAttachTag](pidtagattachtag-canonical-property.md) **)** PR_ATTACH_TAGプロパティから決定できます。</span><span class="sxs-lookup"><span data-stu-id="38e4d-118">The OLE encoding type can be determined from the **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="38e4d-119">OLE ドキュメント ファイルの添付ファイルの場合、メッセージ ストア プロバイダーは PR_ATTACH_DATA_OBJ ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) の [IMAPIProp::OpenProperty](imapiprop-openproperty.md)呼び出しに応答する必要があります。必要に応じて **PR_ATTACH_DATA_BIN** の呼び出し **に応答できます**。</span><span class="sxs-lookup"><span data-stu-id="38e4d-119">For an OLE document file attachment, the message store provider must respond to an [IMAPIProp::OpenProperty](imapiprop-openproperty.md) call on **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) and may optionally respond to a call on **PR_ATTACH_DATA_BIN**.</span></span> <span data-ttu-id="38e4d-120">同じ **PR_ATTACH_DATA_BIN\*\*\*\*プロパティPR_ATTACH_DATA_OBJ** 共有するため、同じプロパティの 2 つの表示に注意してください。</span><span class="sxs-lookup"><span data-stu-id="38e4d-120">Note that **PR_ATTACH_DATA_BIN** and **PR_ATTACH_DATA_OBJ** share the same property identifier and thus are two renditions of the same property.</span></span> 
  
<span data-ttu-id="38e4d-121">OLE 2.0 docfile 形式の複合ファイルなどの記憶域オブジェクトの場合、一部のサービス プロバイダーでは、パフォーマンスを向上するために MAPI **IStreamDocfile** インターフェイスで開くこともできます。</span><span class="sxs-lookup"><span data-stu-id="38e4d-121">For a storage object, such as a compound file in OLE 2.0 docfile format, some service providers allow it to be opened with the MAPI **IStreamDocfile** interface for improved performance.</span></span> <span data-ttu-id="38e4d-122">**IStreamDocfile** をサポートするプロバイダーは、このファイルを PR_ATTACH_DATA_OBJで公開する必要があります。必要に応じて、このファイルを **PR_ATTACH_DATA_BIN。**</span><span class="sxs-lookup"><span data-stu-id="38e4d-122">A provider that supports **IStreamDocfile** must expose it on **PR_ATTACH_DATA_OBJ** and may optionally expose it on **PR_ATTACH_DATA_BIN**.</span></span> 
  
<span data-ttu-id="38e4d-123">OLE インターフェイスと形式の詳細については、「OLE と [データ転送」を参照してください](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx)。</span><span class="sxs-lookup"><span data-stu-id="38e4d-123">For more information on OLE interfaces and formats, see [OLE and Data Transfer](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="38e4d-124">関連リソース</span><span class="sxs-lookup"><span data-stu-id="38e4d-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="38e4d-125">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="38e4d-125">Protocol specifications</span></span>

<span data-ttu-id="38e4d-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="38e4d-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="38e4d-127">メッセージ オブジェクトと添付ファイル オブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="38e4d-127">Handles message and attachment objects.</span></span>
    
## <a name="header-files"></a><span data-ttu-id="38e4d-128">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="38e4d-128">Header Files</span></span>

<span data-ttu-id="38e4d-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="38e4d-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="38e4d-130">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="38e4d-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="38e4d-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="38e4d-131">Mapitags.h</span></span>
  
> <span data-ttu-id="38e4d-132">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="38e4d-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="38e4d-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="38e4d-133">See also</span></span>



[<span data-ttu-id="38e4d-134">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="38e4d-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="38e4d-135">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="38e4d-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="38e4d-136">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="38e4d-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="38e4d-137">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="38e4d-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

