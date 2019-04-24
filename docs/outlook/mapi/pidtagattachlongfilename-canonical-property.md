---
title: PidTagAttachLongFilename 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachLongFilename
api_type:
- HeaderDef
ms.assetid: 83b69e8f-0b5a-4992-b5b8-160d3bdfa22a
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 45b6b3fb0c67d854fddf3773c06cef7b36f54992
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339327"
---
# <a name="pidtagattachlongfilename-canonical-property"></a><span data-ttu-id="d5d4d-103">PidTagAttachLongFilename 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d5d4d-103">PidTagAttachLongFilename Canonical Property</span></span>

  
  
<span data-ttu-id="d5d4d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d5d4d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d5d4d-105">添付ファイルの長いファイル名と拡張子を含みます (パスを除く)。</span><span class="sxs-lookup"><span data-stu-id="d5d4d-105">Contains an attachment's long filename and extension, excluding path.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d5d4d-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="d5d4d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d5d4d-107">PR_ATTACH_LONG_FILENAME、PR_ATTACH_LONG_FILENAME_A、PR_ATTACH_LONG_FILENAME_W</span><span class="sxs-lookup"><span data-stu-id="d5d4d-107">PR_ATTACH_LONG_FILENAME, PR_ATTACH_LONG_FILENAME_A, PR_ATTACH_LONG_FILENAME_W</span></span>  <br/> |
|<span data-ttu-id="d5d4d-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="d5d4d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d5d4d-109">0x3707</span><span class="sxs-lookup"><span data-stu-id="d5d4d-109">0x3707</span></span>  <br/> |
|<span data-ttu-id="d5d4d-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="d5d4d-110">Data type:</span></span>  <br/> |<span data-ttu-id="d5d4d-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d5d4d-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="d5d4d-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="d5d4d-112">Area:</span></span>  <br/> |<span data-ttu-id="d5d4d-113">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="d5d4d-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d5d4d-114">解説</span><span class="sxs-lookup"><span data-stu-id="d5d4d-114">Remarks</span></span>

<span data-ttu-id="d5d4d-115">これらのプロパティは、 **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) プロパティの ATTACH_BY_VALUE、ATTACH_BY_REFERENCE、ATTACH_BY_REF_RESOLVE、および ATTACH_BY_REF_ONLY の各値に関連しています。</span><span class="sxs-lookup"><span data-stu-id="d5d4d-115">These properties pertain to the ATTACH_BY_VALUE, ATTACH_BY_REFERENCE, ATTACH_BY_REF_RESOLVE, and ATTACH_BY_REF_ONLY values of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) property.</span></span> <span data-ttu-id="d5d4d-116">長いファイル名をサポートするプラットフォームは、送信時に**PR_ATTACH_LONG_FILENAME**プロパティと**PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) プロパティの両方を設定する必要があります。また、 **PR_ATTACH_LONG_FILENAME** first when をチェックする必要があります。いう.</span><span class="sxs-lookup"><span data-stu-id="d5d4d-116">Platforms that support long filenames should set both the **PR_ATTACH_LONG_FILENAME** and **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) properties when sending, and should check **PR_ATTACH_LONG_FILENAME** first when receiving.</span></span> 
  
<span data-ttu-id="d5d4d-117">クライアントアプリケーションは、メッセージを受信するホストコンピューターが長いファイル名をサポートしている場合に、このプロパティに推奨される長いファイル名を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d5d4d-117">The client application should set this property to a suggested long filename to be used if the host computer receiving a message supports long filenames.</span></span> <span data-ttu-id="d5d4d-118">**PR_ATTACH_LONG_FILENAME**は、添付ファイルを保存するためのファイル名として使用でき、 **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) プロパティが指定されていない場合は、ファイル拡張子を指定します。</span><span class="sxs-lookup"><span data-stu-id="d5d4d-118">**PR_ATTACH_LONG_FILENAME** can be used as a filename for saving the attachment, and to supply the filename extension if the **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) property is not provided.</span></span> 
  
<span data-ttu-id="d5d4d-119">**PR_ATTACH_FILENAME**によって提供されるファイル名とは異なり、この名前は8文字のファイル名に加えて、3文字の拡張子に制限されません。</span><span class="sxs-lookup"><span data-stu-id="d5d4d-119">Unlike the filename provided by **PR_ATTACH_FILENAME**, this name is not restricted to an eight-character filename plus a three-character extension.</span></span> <span data-ttu-id="d5d4d-120">その代わりに、ファイル名、内線番号、区切り期間など、最大256文字の長さを指定できます。</span><span class="sxs-lookup"><span data-stu-id="d5d4d-120">Instead, it can be up to 256 characters long, including the filename, extension, and separator period.</span></span> 
  
<span data-ttu-id="d5d4d-121">MAPI は、ANSI 文字セットのファイル名に対してのみ機能します。</span><span class="sxs-lookup"><span data-stu-id="d5d4d-121">MAPI works only with filenames in the ANSI character set.</span></span> <span data-ttu-id="d5d4d-122">OEM 文字セットでファイル名を使用するクライアントアプリケーションは、MAPI を呼び出す前に、それらを ANSI に変換する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d5d4d-122">Client applications that use filenames in an OEM character set must convert them to ANSI before calling MAPI.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d5d4d-123">関連リソース</span><span class="sxs-lookup"><span data-stu-id="d5d4d-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d5d4d-124">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="d5d4d-124">Protocol specifications</span></span>

<span data-ttu-id="d5d4d-125">[[OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d5d4d-125">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d5d4d-126">メッセージと添付ファイルオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="d5d4d-126">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="d5d4d-127">[[OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d5d4d-127">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d5d4d-128">インターネット標準の電子メールの規則からメッセージオブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="d5d4d-128">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="d5d4d-129">[[OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d5d4d-129">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d5d4d-130">権限が管理されたエンコード済みメッセージのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="d5d4d-130">Specifies the properties of rights-managed encoded messages.</span></span>
    
<span data-ttu-id="d5d4d-131">[[OXOUM]](https://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d5d4d-131">[[MS-OXOUM]](https://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d5d4d-132">ボイスメールおよび fax メッセージを表すために許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="d5d4d-132">Specifies the properties and operations that are permissible for representing voice mail and fax messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d5d4d-133">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="d5d4d-133">Header files</span></span>

<span data-ttu-id="d5d4d-134">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d5d4d-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="d5d4d-135">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="d5d4d-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="d5d4d-136">Mmapitags</span><span class="sxs-lookup"><span data-stu-id="d5d4d-136">Mmapitags.h</span></span>
  
> <span data-ttu-id="d5d4d-137">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d5d4d-137">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d5d4d-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="d5d4d-138">See also</span></span>



[<span data-ttu-id="d5d4d-139">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="d5d4d-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d5d4d-140">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d5d4d-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d5d4d-141">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="d5d4d-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d5d4d-142">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="d5d4d-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

