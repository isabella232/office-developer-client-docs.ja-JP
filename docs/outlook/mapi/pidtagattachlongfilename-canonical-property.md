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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394462"
---
# <a name="pidtagattachlongfilename-canonical-property"></a><span data-ttu-id="d984e-103">PidTagAttachLongFilename 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d984e-103">PidTagAttachLongFilename Canonical Property</span></span>

  
  
<span data-ttu-id="d984e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d984e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d984e-105">添付ファイルの長いファイル名とパスを除外する拡張子が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d984e-105">Contains an attachment's long filename and extension, excluding path.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d984e-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="d984e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d984e-107">PR_ATTACH_LONG_FILENAME、PR_ATTACH_LONG_FILENAME_A、PR_ATTACH_LONG_FILENAME_W</span><span class="sxs-lookup"><span data-stu-id="d984e-107">PR_ATTACH_LONG_FILENAME, PR_ATTACH_LONG_FILENAME_A, PR_ATTACH_LONG_FILENAME_W</span></span>  <br/> |
|<span data-ttu-id="d984e-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="d984e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d984e-109">0x3707</span><span class="sxs-lookup"><span data-stu-id="d984e-109">0x3707</span></span>  <br/> |
|<span data-ttu-id="d984e-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="d984e-110">Data type:</span></span>  <br/> |<span data-ttu-id="d984e-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d984e-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="d984e-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="d984e-112">Area:</span></span>  <br/> |<span data-ttu-id="d984e-113">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="d984e-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d984e-114">備考</span><span class="sxs-lookup"><span data-stu-id="d984e-114">Remarks</span></span>

<span data-ttu-id="d984e-115">これらのプロパティは、ATTACH_BY_VALUE、ATTACH_BY_REFERENCE、ATTACH_BY_REF_RESOLVE、および ATTACH_BY_REF_ONLY **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) プロパティの値に適用されます。</span><span class="sxs-lookup"><span data-stu-id="d984e-115">These properties pertain to the ATTACH_BY_VALUE, ATTACH_BY_REFERENCE, ATTACH_BY_REF_RESOLVE, and ATTACH_BY_REF_ONLY values of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) property.</span></span> <span data-ttu-id="d984e-116">長いファイル名をサポートしているプラットフォームは、 **PR_ATTACH_LONG_FILENAME**と**PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) のプロパティの両方を送信するとき、設定する必要があり、確認してください**PR_ATTACH_LONG_FILENAME**最初に受信しています。</span><span class="sxs-lookup"><span data-stu-id="d984e-116">Platforms that support long filenames should set both the **PR_ATTACH_LONG_FILENAME** and **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) properties when sending, and should check **PR_ATTACH_LONG_FILENAME** first when receiving.</span></span> 
  
<span data-ttu-id="d984e-117">クライアント アプリケーションは、メッセージを受信するホスト コンピューターは、長いファイル名をサポートしている場合に使用する推奨の長いファイル名にこのプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d984e-117">The client application should set this property to a suggested long filename to be used if the host computer receiving a message supports long filenames.</span></span> <span data-ttu-id="d984e-118">**PR_ATTACH_LONG_FILENAME**は、 **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) のプロパティが指定されていない場合は、ファイル名の拡張子を指定して、添付ファイルを保存するため、ファイル名として使用できます。</span><span class="sxs-lookup"><span data-stu-id="d984e-118">**PR_ATTACH_LONG_FILENAME** can be used as a filename for saving the attachment, and to supply the filename extension if the **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) property is not provided.</span></span> 
  
<span data-ttu-id="d984e-119">**PR_ATTACH_FILENAME**によって提供されるファイル名とは異なりこの名前は 8 文字のファイル名と拡張子が 3 文字に制限はありません。</span><span class="sxs-lookup"><span data-stu-id="d984e-119">Unlike the filename provided by **PR_ATTACH_FILENAME**, this name is not restricted to an eight-character filename plus a three-character extension.</span></span> <span data-ttu-id="d984e-120">代わりに、ことができます最大 256 文字、ファイル名、拡張子、および区切り記号のピリオドを含みます。</span><span class="sxs-lookup"><span data-stu-id="d984e-120">Instead, it can be up to 256 characters long, including the filename, extension, and separator period.</span></span> 
  
<span data-ttu-id="d984e-121">MAPI は、ファイル名に ANSI 文字セットでのみ動作します。</span><span class="sxs-lookup"><span data-stu-id="d984e-121">MAPI works only with filenames in the ANSI character set.</span></span> <span data-ttu-id="d984e-122">OEM 文字セットでファイル名を使用するクライアント アプリケーションする必要があります ANSI に変換する、MAPI を呼び出す前にします。</span><span class="sxs-lookup"><span data-stu-id="d984e-122">Client applications that use filenames in an OEM character set must convert them to ANSI before calling MAPI.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d984e-123">関連リソース</span><span class="sxs-lookup"><span data-stu-id="d984e-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d984e-124">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="d984e-124">Protocol specifications</span></span>

<span data-ttu-id="d984e-125">[[MS OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d984e-125">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d984e-126">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="d984e-126">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="d984e-127">[[MS OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d984e-127">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d984e-128">メッセージ オブジェクト インターネット標準の電子メールの表記規則からに変換します。</span><span class="sxs-lookup"><span data-stu-id="d984e-128">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="d984e-129">[[MS OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d984e-129">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d984e-130">権限管理でエンコードされたメッセージのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="d984e-130">Specifies the properties of rights-managed encoded messages.</span></span>
    
<span data-ttu-id="d984e-131">[[MS OXOUM]](https://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d984e-131">[[MS-OXOUM]](https://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d984e-132">プロパティとは、ボイス メールと fax メッセージを表示するための許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="d984e-132">Specifies the properties and operations that are permissible for representing voice mail and fax messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d984e-133">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="d984e-133">Header files</span></span>

<span data-ttu-id="d984e-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d984e-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="d984e-135">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="d984e-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="d984e-136">Mmapitags.h</span><span class="sxs-lookup"><span data-stu-id="d984e-136">Mmapitags.h</span></span>
  
> <span data-ttu-id="d984e-137">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d984e-137">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d984e-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="d984e-138">See also</span></span>



[<span data-ttu-id="d984e-139">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="d984e-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d984e-140">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="d984e-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d984e-141">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="d984e-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d984e-142">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="d984e-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

