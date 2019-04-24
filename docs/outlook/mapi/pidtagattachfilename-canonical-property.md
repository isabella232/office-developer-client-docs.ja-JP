---
title: PidTagAttachFilename 標準プロパティ
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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f5dcf90e8224f1bf2e96042a7344109293cc2c3f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319223"
---
# <a name="pidtagattachfilename-canonical-property"></a><span data-ttu-id="a746c-103">PidTagAttachFilename 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a746c-103">PidTagAttachFilename Canonical Property</span></span>

  
  
<span data-ttu-id="a746c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a746c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a746c-105">添付ファイルの基本ファイル名と拡張子を含みます (パスを除く)。</span><span class="sxs-lookup"><span data-stu-id="a746c-105">Contains an attachment's base file name and extension, excluding path.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a746c-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="a746c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a746c-107">PR_ATTACH_FILENAME、PR_ATTACH_FILENAME_A、PR_ATTACH_FILENAME_W</span><span class="sxs-lookup"><span data-stu-id="a746c-107">PR_ATTACH_FILENAME, PR_ATTACH_FILENAME_A, PR_ATTACH_FILENAME_W</span></span>  <br/> |
|<span data-ttu-id="a746c-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="a746c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a746c-109">0x3704</span><span class="sxs-lookup"><span data-stu-id="a746c-109">0x3704</span></span>  <br/> |
|<span data-ttu-id="a746c-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="a746c-110">Data type:</span></span>  <br/> |<span data-ttu-id="a746c-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a746c-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="a746c-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="a746c-112">Area:</span></span>  <br/> |<span data-ttu-id="a746c-113">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="a746c-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a746c-114">解説</span><span class="sxs-lookup"><span data-stu-id="a746c-114">Remarks</span></span>

<span data-ttu-id="a746c-115">attachment オブジェクトは、これらのプロパティを公開することをお勧めします。これらのプロパティは、 **PR_ATTACH_METHOD**の**ATTACH_BY_VALUE**、 **ATTACH_BY_REFERENCE**、 **ATTACH_BY_REF_RESOLVE**、および**ATTACH_BY_REF_ONLY**の値に関連しています。([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) プロパティ。</span><span class="sxs-lookup"><span data-stu-id="a746c-115">It is recommended that attachment objects expose these properties which pertain to the **ATTACH_BY_VALUE**, **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**, and **ATTACH_BY_REF_ONLY** values of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) property.</span></span> <span data-ttu-id="a746c-116">これらの値のいずれかを使用する場合は、 **PR_ATTACH_FILENAME**および関連するプロパティが必要です。</span><span class="sxs-lookup"><span data-stu-id="a746c-116">**PR_ATTACH_FILENAME** and associated properties are required when any of these values is used.</span></span> 
  
<span data-ttu-id="a746c-117">これらのプロパティは、添付ファイルを保存するための推奨されるファイル名として使用でき、 **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) プロパティが指定されていない場合はファイル名拡張子を指定します。</span><span class="sxs-lookup"><span data-stu-id="a746c-117">These properties can be used as a suggested file name for saving the attachment and to supply the file name extension if the **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) property is not provided.</span></span> 
  
<span data-ttu-id="a746c-118">ファイル名が8文字に制限され、3文字の拡張子になります。</span><span class="sxs-lookup"><span data-stu-id="a746c-118">The file name is restricted to eight characters plus a three-character extension.</span></span> <span data-ttu-id="a746c-119">長いファイル名をサポートするプラットフォームでは、このプロパティと**PR_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) プロパティの両方を設定します。</span><span class="sxs-lookup"><span data-stu-id="a746c-119">For a platform that supports long file names, set both this property and the **PR_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="a746c-120">MAPI は、米国規格協会 (ANSI) 文字セットで、ファイル名とそれに渡されるその他の文字列に対してのみ機能します。</span><span class="sxs-lookup"><span data-stu-id="a746c-120">MAPI works only with file names, and other strings passed to it, in the American National Standards Institute (ANSI) character set.</span></span> <span data-ttu-id="a746c-121">OEM (相手先ブランド供給) 文字セットでファイル名を使用するクライアントアプリケーションは、MAPI を呼び出す前に、それらを ANSI に変換する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a746c-121">Client applications that use file names in an original equipment manufacturer (OEM) character set must convert them to ANSI before calling MAPI.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="a746c-122">関連リソース</span><span class="sxs-lookup"><span data-stu-id="a746c-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a746c-123">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="a746c-123">Protocol specifications</span></span>

<span data-ttu-id="a746c-124">[[OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a746c-124">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a746c-125">メッセージと添付ファイルオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="a746c-125">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="a746c-126">[[OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a746c-126">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a746c-127">インターネット標準の電子メールの規則からメッセージオブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="a746c-127">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="a746c-128">[[OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a746c-128">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a746c-129">権限が管理されたエンコード済みメッセージのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="a746c-129">Specifies the properties of rights-managed encoded messages.</span></span>
    
<span data-ttu-id="a746c-130">[[OXOSMIME]](https://msdn.microsoft.com/library/bb17d126-d211-462c-8cd3-454ed33c8746%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a746c-130">[[MS-OXOSMIME]](https://msdn.microsoft.com/library/bb17d126-d211-462c-8cd3-454ed33c8746%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a746c-131">S/MIME で署名および暗号化されたメッセージのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="a746c-131">Specifies S/MIME signed and encrypted message properties.</span></span>
    
<span data-ttu-id="a746c-132">[[OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a746c-132">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a746c-133">メッセージと添付ファイルオブジェクトをエンコードし、効率的なストリーム表現にデコードします。</span><span class="sxs-lookup"><span data-stu-id="a746c-133">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a746c-134">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="a746c-134">Header files</span></span>

<span data-ttu-id="a746c-135">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a746c-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="a746c-136">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="a746c-136">Provides data type definitions.</span></span>
    
<span data-ttu-id="a746c-137">Mapitags</span><span class="sxs-lookup"><span data-stu-id="a746c-137">Mapitags.h</span></span>
  
> <span data-ttu-id="a746c-138">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="a746c-138">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a746c-139">関連項目</span><span class="sxs-lookup"><span data-stu-id="a746c-139">See also</span></span>



[<span data-ttu-id="a746c-140">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="a746c-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a746c-141">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a746c-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a746c-142">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="a746c-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a746c-143">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="a746c-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

