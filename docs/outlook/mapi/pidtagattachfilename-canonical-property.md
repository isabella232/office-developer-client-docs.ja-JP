---
title: PidTagAttachFilename の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachFilename
api_type:
- HeaderDef
ms.assetid: cbf34dd6-7733-47f6-9c41-9d82656ca9dc
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 4468ecd5946c95fab62d0885d9c0b3343a1508dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802477"
---
# <a name="pidtagattachfilename-canonical-property"></a><span data-ttu-id="a6005-103">PidTagAttachFilename の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="a6005-103">PidTagAttachFilename Canonical Property</span></span>

  
  
<span data-ttu-id="a6005-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a6005-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a6005-105">添付ファイルのベース ファイル名とパスを除外する拡張子が含まれています。</span><span class="sxs-lookup"><span data-stu-id="a6005-105">Contains an attachment's base file name and extension, excluding path.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a6005-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="a6005-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a6005-107">PR_ATTACH_FILENAME、PR_ATTACH_FILENAME_A、PR_ATTACH_FILENAME_W</span><span class="sxs-lookup"><span data-stu-id="a6005-107">PR_ATTACH_FILENAME, PR_ATTACH_FILENAME_A, PR_ATTACH_FILENAME_W</span></span>  <br/> |
|<span data-ttu-id="a6005-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="a6005-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a6005-109">0x3704</span><span class="sxs-lookup"><span data-stu-id="a6005-109">0x3704</span></span>  <br/> |
|<span data-ttu-id="a6005-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="a6005-110">Data type:</span></span>  <br/> |<span data-ttu-id="a6005-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a6005-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="a6005-112">領域:</span><span class="sxs-lookup"><span data-stu-id="a6005-112">Area:</span></span>  <br/> |<span data-ttu-id="a6005-113">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="a6005-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a6005-114">備考</span><span class="sxs-lookup"><span data-stu-id="a6005-114">Remarks</span></span>

<span data-ttu-id="a6005-115">オブジェクトの添付ファイルが**PR_ATTACH_METHOD**の**ATTACH_BY_VALUE**、 **ATTACH_BY_REFERENCE**、 **ATTACH_BY_REF_RESOLVE**、および**ATTACH_BY_REF_ONLY**の値に関係するこれらのプロパティを公開することをお勧めします。([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) のプロパティです。</span><span class="sxs-lookup"><span data-stu-id="a6005-115">It is recommended that attachment objects expose these properties which pertain to the **ATTACH_BY_VALUE**, **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**, and **ATTACH_BY_REF_ONLY** values of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) property.</span></span> <span data-ttu-id="a6005-116">**PR_ATTACH_FILENAME**と関連付けられているプロパティは、必要な場合これらの値のいずれかを使用します。</span><span class="sxs-lookup"><span data-stu-id="a6005-116">**PR_ATTACH_FILENAME** and associated properties are required when any of these values is used.</span></span> 
  
<span data-ttu-id="a6005-117">**PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) のプロパティが指定されていない場合は、ファイル名の拡張子を指定して、添付ファイルを保存するため、これらのプロパティを既定のファイル名として使用できます。</span><span class="sxs-lookup"><span data-stu-id="a6005-117">These properties can be used as a suggested file name for saving the attachment and to supply the file name extension if the **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) property is not provided.</span></span> 
  
<span data-ttu-id="a6005-118">ファイル名は、8 文字および 3 文字の拡張子に制限されます。</span><span class="sxs-lookup"><span data-stu-id="a6005-118">The file name is restricted to eight characters plus a three-character extension.</span></span> <span data-ttu-id="a6005-119">長いファイル名をサポートしているプラットフォームでは、このプロパティと**PR_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) のプロパティの両方を設定します。</span><span class="sxs-lookup"><span data-stu-id="a6005-119">For a platform that supports long file names, set both this property and the **PR_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="a6005-120">MAPI の機能をファイル名に、および米国規格協会 (ANSI) 文字セットで、その他の文字列が渡されます。</span><span class="sxs-lookup"><span data-stu-id="a6005-120">MAPI works only with file names, and other strings passed to it, in the American National Standards Institute (ANSI) character set.</span></span> <span data-ttu-id="a6005-121">正規機器製造元 (OEM) 文字セットでファイル名を使用するクライアント アプリケーションする必要があります ANSI に変換する、MAPI を呼び出す前にします。</span><span class="sxs-lookup"><span data-stu-id="a6005-121">Client applications that use file names in an original equipment manufacturer (OEM) character set must convert them to ANSI before calling MAPI.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="a6005-122">関連リソース</span><span class="sxs-lookup"><span data-stu-id="a6005-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a6005-123">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="a6005-123">Protocol specifications</span></span>

<span data-ttu-id="a6005-124">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a6005-124">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a6005-125">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="a6005-125">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="a6005-126">[[MS OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a6005-126">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a6005-127">メッセージ オブジェクト インターネット標準の電子メールの表記規則からに変換します。</span><span class="sxs-lookup"><span data-stu-id="a6005-127">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="a6005-128">[[MS OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a6005-128">[[MS-OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a6005-129">権限管理でエンコードされたメッセージのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="a6005-129">Specifies the properties of rights-managed encoded messages.</span></span>
    
<span data-ttu-id="a6005-130">[[MS OXOSMIME]](http://msdn.microsoft.com/library/bb17d126-d211-462c-8cd3-454ed33c8746%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a6005-130">[[MS-OXOSMIME]](http://msdn.microsoft.com/library/bb17d126-d211-462c-8cd3-454ed33c8746%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a6005-131">S/MIME 署名され、暗号化メッセージのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="a6005-131">Specifies S/MIME signed and encrypted message properties.</span></span>
    
<span data-ttu-id="a6005-132">[[MS OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a6005-132">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a6005-133">エンコードし、メッセージと添付ファイルのオブジェクトを効率的なストリーム形式をデコードします。</span><span class="sxs-lookup"><span data-stu-id="a6005-133">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a6005-134">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="a6005-134">Header files</span></span>

<span data-ttu-id="a6005-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a6005-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="a6005-136">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="a6005-136">Provides data type definitions.</span></span>
    
<span data-ttu-id="a6005-137">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a6005-137">Mapitags.h</span></span>
  
> <span data-ttu-id="a6005-138">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="a6005-138">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a6005-139">関連項目</span><span class="sxs-lookup"><span data-stu-id="a6005-139">See also</span></span>



[<span data-ttu-id="a6005-140">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="a6005-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a6005-141">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="a6005-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a6005-142">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="a6005-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a6005-143">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="a6005-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

