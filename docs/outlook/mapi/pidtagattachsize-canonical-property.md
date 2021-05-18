---
title: PidTagAttachSize 標準プロパティ
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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f3e4f19ab43a3da7c4840d762d5131813c83d996
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361090"
---
# <a name="pidtagattachsize-canonical-property"></a><span data-ttu-id="c82b6-103">PidTagAttachSize 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c82b6-103">PidTagAttachSize Canonical Property</span></span>

  
  
<span data-ttu-id="c82b6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c82b6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c82b6-105">添付ファイルのすべてのプロパティのサイズの合計 (バイト単位) が含まれます。</span><span class="sxs-lookup"><span data-stu-id="c82b6-105">Contains the sum, in bytes, of the sizes of all properties on an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c82b6-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="c82b6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c82b6-107">PR_ATTACH_SIZE</span><span class="sxs-lookup"><span data-stu-id="c82b6-107">PR_ATTACH_SIZE</span></span>  <br/> |
|<span data-ttu-id="c82b6-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="c82b6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c82b6-109">0x0E20</span><span class="sxs-lookup"><span data-stu-id="c82b6-109">0x0E20</span></span>  <br/> |
|<span data-ttu-id="c82b6-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="c82b6-110">Data type:</span></span>  <br/> |<span data-ttu-id="c82b6-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c82b6-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c82b6-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="c82b6-112">Area:</span></span>  <br/> |<span data-ttu-id="c82b6-113">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="c82b6-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c82b6-114">注釈</span><span class="sxs-lookup"><span data-stu-id="c82b6-114">Remarks</span></span>

<span data-ttu-id="c82b6-115">添付ファイルのサブオブジェクトは、PR_ATTACH_SIZE **勧めします** 。</span><span class="sxs-lookup"><span data-stu-id="c82b6-115">It is recommended that attachment subobjects expose the **PR_ATTACH_SIZE** property.</span></span> <span data-ttu-id="c82b6-116">PR_ATTACH_SIZE に含まれる **合計には\*\*\*\*、PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) プロパティまたは PR_ATTACH_DATA_OBJ **(** [PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) プロパティのサイズが含まれます。</span><span class="sxs-lookup"><span data-stu-id="c82b6-116">The sum contained in **PR_ATTACH_SIZE** includes the size of the **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) or **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property.</span></span> <span data-ttu-id="c82b6-117">したがって **、通常PR_ATTACH_SIZE** は添付ファイルの内容よりも大きくなります。</span><span class="sxs-lookup"><span data-stu-id="c82b6-117">Accordingly, **PR_ATTACH_SIZE** is usually larger than the contents of the attachment alone.</span></span> 
  
<span data-ttu-id="c82b6-118">このプロパティを使用すると、モデムによるリモート転送を実行する前に添付ファイルのおおよそのサイズを確認し、添付ファイルをディスクに保存するときに進行状況インジケーターを表示できます。</span><span class="sxs-lookup"><span data-stu-id="c82b6-118">This property can be used to check the approximate size of the attachment before performing a remote transfer by modem and to display progress indicators when saving the attachment to disk.</span></span> <span data-ttu-id="c82b6-119">これは、添付された OLE オブジェクトで特に便利です。</span><span class="sxs-lookup"><span data-stu-id="c82b6-119">It is particularly useful with attached OLE objects.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c82b6-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="c82b6-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c82b6-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="c82b6-121">Protocol specifications</span></span>

<span data-ttu-id="c82b6-122">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c82b6-122">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c82b6-123">メッセージ オブジェクトと添付ファイル オブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="c82b6-123">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c82b6-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="c82b6-124">Header files</span></span>

<span data-ttu-id="c82b6-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c82b6-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="c82b6-126">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="c82b6-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="c82b6-127">mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c82b6-127">mapitags.h</span></span>
  
> <span data-ttu-id="c82b6-128">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="c82b6-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c82b6-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="c82b6-129">See also</span></span>



[<span data-ttu-id="c82b6-130">PidTagMessageSize 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c82b6-130">PidTagMessageSize Canonical Property</span></span>](pidtagmessagesize-canonical-property.md)


[<span data-ttu-id="c82b6-131">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="c82b6-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c82b6-132">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c82b6-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c82b6-133">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="c82b6-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c82b6-134">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="c82b6-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

