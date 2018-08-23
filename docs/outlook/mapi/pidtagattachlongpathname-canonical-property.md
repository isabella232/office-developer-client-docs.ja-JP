---
title: PidTagAttachLongPathname 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachLongPathname
api_type:
- HeaderDef
ms.assetid: 3262cf95-48b5-4764-a96e-d752ce35b2dc
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c0a3a96c3d8835550c4b0fda233183214cb4a786
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587426"
---
# <a name="pidtagattachlongpathname-canonical-property"></a><span data-ttu-id="5c6c9-103">PidTagAttachLongPathname 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5c6c9-103">PidTagAttachLongPathname Canonical Property</span></span>

  
  
<span data-ttu-id="5c6c9-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5c6c9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5c6c9-105">添付ファイルの長さの完全修飾パスとファイル名が含まれています。</span><span class="sxs-lookup"><span data-stu-id="5c6c9-105">Contains an attachment's fully-qualified long path and filename.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5c6c9-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="5c6c9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5c6c9-107">PR_ATTACH_LONG_PATHNAME、PR_ATTACH_LONG_PATHNAME_A、PR_ATTACH_LONG_PATHNAME_W</span><span class="sxs-lookup"><span data-stu-id="5c6c9-107">PR_ATTACH_LONG_PATHNAME, PR_ATTACH_LONG_PATHNAME_A, PR_ATTACH_LONG_PATHNAME_W</span></span>  <br/> |
|<span data-ttu-id="5c6c9-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="5c6c9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5c6c9-109">0x370D</span><span class="sxs-lookup"><span data-stu-id="5c6c9-109">0x370D</span></span>  <br/> |
|<span data-ttu-id="5c6c9-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="5c6c9-110">Data type:</span></span>  <br/> |<span data-ttu-id="5c6c9-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5c6c9-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="5c6c9-112">領域:</span><span class="sxs-lookup"><span data-stu-id="5c6c9-112">Area:</span></span>  <br/> |<span data-ttu-id="5c6c9-113">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="5c6c9-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5c6c9-114">注釈</span><span class="sxs-lookup"><span data-stu-id="5c6c9-114">Remarks</span></span>

<span data-ttu-id="5c6c9-115">これらのプロパティは、参照、添付ファイルを指定する**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) プロパティの値のいずれかを使用する場合に適用します**ATTACH_BY_REFERENCE**、 **ATTACH_BY_REF_RESOLVE**、または**ATTACH_BY。_REF_ONLY**。</span><span class="sxs-lookup"><span data-stu-id="5c6c9-115">These properties are applicable when you use any of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) property's values that indicate attachment by reference: **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**, or **ATTACH_BY_REF_ONLY**.</span></span> <span data-ttu-id="5c6c9-116">長いファイル名をサポートするプラットフォームは、 **PR_ATTACH_LONG_PATHNAME**または関連付けられているプロパティと**PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) プロパティの両方を送信すると、 **PR_ATTACH_LONG_PATHNAME をチェックする必要があります。 を設定する必要があります。** を受信する場合はプロパティを最初に関連付けられているか。</span><span class="sxs-lookup"><span data-stu-id="5c6c9-116">Platforms that support long filenames should set both **PR_ATTACH_LONG_PATHNAME** or associated properties and **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) properties when sending, and should check **PR_ATTACH_LONG_PATHNAME** or associated properties first when receiving.</span></span> 
  
<span data-ttu-id="5c6c9-117">クライアント アプリケーションは、長いパスが推奨されると、メッセージを受信するホスト ・ マシンには、長いファイル名がサポートしている場合に使用するファイル名にこれらのプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5c6c9-117">The client application should set these properties to a suggested long path and filename to be used if the host machine receiving a message supports long filenames.</span></span> <span data-ttu-id="5c6c9-118">これらのプロパティを設定するには、添付ファイルのデータがメッセージに含まれていないが、共通のファイル ・ サーバで使用可能なことを示します。</span><span class="sxs-lookup"><span data-stu-id="5c6c9-118">Setting these properties indicates that the attachment data is not included with the message but is available on a common file server.</span></span> 
  
<span data-ttu-id="5c6c9-119">ディレクトリとファイル名が**PR_ATTACH_PATHNAME**によって提供されるとは異なりこれらのディレクトリとファイル名は、8 文字のディレクトリまたはファイル名と拡張子 3 文字に制限付きではありません。</span><span class="sxs-lookup"><span data-stu-id="5c6c9-119">Unlike the directories and filenames provided by **PR_ATTACH_PATHNAME**, these directories and filenames are not restricted to an eight-character directory or filename plus three-character extension.</span></span> <span data-ttu-id="5c6c9-120">代わりに、各ディレクトリまたはファイル名、最大 256 文字、名前、拡張子、および区切り記号のピリオドを含みます。</span><span class="sxs-lookup"><span data-stu-id="5c6c9-120">Instead, each directory or filename can be up to 256 characters long, including the name, extension, and separator period.</span></span> <span data-ttu-id="5c6c9-121">ただし、全体的なパスは、256 文字に制限されています。</span><span class="sxs-lookup"><span data-stu-id="5c6c9-121">However, the overall path is limited to 256 characters.</span></span> 
  
<span data-ttu-id="5c6c9-122">クライアントは、ファイルが共有され、ファイルがローカルの絶対パスを使用する必要がある場合に、ほとんどの場合、汎用名前付け規則 (UNC) を使用します。</span><span class="sxs-lookup"><span data-stu-id="5c6c9-122">Clients should use a universal naming convention (UNC) in most cases when the file is shared, and should use an absolute path when the file is local.</span></span>
  
<span data-ttu-id="5c6c9-123">MAPI はパスとファイル名に ANSI 文字セットです。</span><span class="sxs-lookup"><span data-stu-id="5c6c9-123">MAPI works only with paths and filenames in the ANSI character set.</span></span> <span data-ttu-id="5c6c9-124">OEM 文字セット内のパスとファイル名を使用するクライアント アプリケーションする必要があります ANSI に変換する、MAPI を呼び出す前にします。</span><span class="sxs-lookup"><span data-stu-id="5c6c9-124">Client applications that use paths and filenames in an OEM character set must convert them to ANSI before calling MAPI.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="5c6c9-125">関連リソース</span><span class="sxs-lookup"><span data-stu-id="5c6c9-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5c6c9-126">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="5c6c9-126">Protocol specifications</span></span>

<span data-ttu-id="5c6c9-127">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5c6c9-127">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5c6c9-128">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="5c6c9-128">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="5c6c9-129">[[MS OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5c6c9-129">[[MS-OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5c6c9-130">権限管理でエンコードされたメッセージのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="5c6c9-130">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5c6c9-131">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="5c6c9-131">Header files</span></span>

<span data-ttu-id="5c6c9-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5c6c9-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="5c6c9-133">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="5c6c9-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="5c6c9-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5c6c9-134">Mapitags.h</span></span>
  
> <span data-ttu-id="5c6c9-135">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="5c6c9-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5c6c9-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="5c6c9-136">See also</span></span>



[<span data-ttu-id="5c6c9-137">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="5c6c9-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5c6c9-138">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="5c6c9-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5c6c9-139">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="5c6c9-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5c6c9-140">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="5c6c9-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

