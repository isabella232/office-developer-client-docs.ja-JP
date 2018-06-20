---
title: PidTagAttachSize の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachSize
api_type:
- HeaderDef
ms.assetid: 768b3215-dd9f-4aa0-b52c-178ca81a7b07
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 2d6b585c00ffb3d9dd5fb0864d98b0a221c7d8c2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802499"
---
# <a name="pidtagattachsize-canonical-property"></a><span data-ttu-id="65414-103">PidTagAttachSize の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="65414-103">PidTagAttachSize Canonical Property</span></span>

  
  
<span data-ttu-id="65414-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="65414-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="65414-105">添付ファイルのすべてのプロパティのサイズの合計 (バイト単位) にはが含まれています。</span><span class="sxs-lookup"><span data-stu-id="65414-105">Contains the sum, in bytes, of the sizes of all properties on an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="65414-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="65414-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="65414-107">PR_ATTACH_SIZE</span><span class="sxs-lookup"><span data-stu-id="65414-107">PR_ATTACH_SIZE</span></span>  <br/> |
|<span data-ttu-id="65414-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="65414-108">Identifier:</span></span>  <br/> |<span data-ttu-id="65414-109">0x0e20 が使えるはず</span><span class="sxs-lookup"><span data-stu-id="65414-109">0x0E20</span></span>  <br/> |
|<span data-ttu-id="65414-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="65414-110">Data type:</span></span>  <br/> |<span data-ttu-id="65414-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="65414-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="65414-112">領域:</span><span class="sxs-lookup"><span data-stu-id="65414-112">Area:</span></span>  <br/> |<span data-ttu-id="65414-113">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="65414-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="65414-114">備考</span><span class="sxs-lookup"><span data-stu-id="65414-114">Remarks</span></span>

<span data-ttu-id="65414-115">サブオブジェクトの添付ファイルが、 **PR_ATTACH_SIZE**プロパティを公開することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="65414-115">It is recommended that attachment subobjects expose the **PR_ATTACH_SIZE** property.</span></span> <span data-ttu-id="65414-116">**PR_ATTACH_SIZE**に含まれている合計には、 **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) または**PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) のプロパティのサイズが含まれています。</span><span class="sxs-lookup"><span data-stu-id="65414-116">The sum contained in **PR_ATTACH_SIZE** includes the size of the **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) or **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property.</span></span> <span data-ttu-id="65414-117">したがって、 **PR_ATTACH_SIZE**は、通常、単独での添付ファイルの内容より大きくです。</span><span class="sxs-lookup"><span data-stu-id="65414-117">Accordingly, **PR_ATTACH_SIZE** is usually larger than the contents of the attachment alone.</span></span> 
  
<span data-ttu-id="65414-118">モデム経由でリモートの転送を実行する前に添付ファイルのおおよそのサイズを確認し、添付ファイルをディスクに保存するときに進行状況インジケーターを表示するのには、このプロパティを使用できます。</span><span class="sxs-lookup"><span data-stu-id="65414-118">This property can be used to check the approximate size of the attachment before performing a remote transfer by modem and to display progress indicators when saving the attachment to disk.</span></span> <span data-ttu-id="65414-119">添付された OLE オブジェクトで特に便利です。</span><span class="sxs-lookup"><span data-stu-id="65414-119">It is particularly useful with attached OLE objects.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="65414-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="65414-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="65414-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="65414-121">Protocol specifications</span></span>

<span data-ttu-id="65414-122">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="65414-122">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="65414-123">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="65414-123">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="65414-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="65414-124">Header files</span></span>

<span data-ttu-id="65414-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="65414-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="65414-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="65414-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="65414-127">mapitags.h</span><span class="sxs-lookup"><span data-stu-id="65414-127">mapitags.h</span></span>
  
> <span data-ttu-id="65414-128">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="65414-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="65414-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="65414-129">See also</span></span>



[<span data-ttu-id="65414-130">PidTagMessageSize の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="65414-130">PidTagMessageSize Canonical Property</span></span>](pidtagmessagesize-canonical-property.md)


[<span data-ttu-id="65414-131">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="65414-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="65414-132">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="65414-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="65414-133">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="65414-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="65414-134">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="65414-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

