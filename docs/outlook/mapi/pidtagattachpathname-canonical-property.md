---
title: PidTagAttachPathname の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachPathname
api_type:
- HeaderDef
ms.assetid: e19c7cd1-7c56-4f63-8736-d6971c7c5f4d
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: b7e0c174f0b31522cffbb4761ab64a50267874be
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802490"
---
# <a name="pidtagattachpathname-canonical-property"></a><span data-ttu-id="b42b8-103">PidTagAttachPathname の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="b42b8-103">PidTagAttachPathname Canonical Property</span></span>

  
  
<span data-ttu-id="b42b8-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b42b8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b42b8-105">添付ファイルの完全修飾パスとファイル名が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b42b8-105">Contains an attachment's fully-qualified path and filename.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b42b8-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="b42b8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b42b8-107">PR_ATTACH_PATHNAME、PR_ATTACH_PATHNAME_A、PR_ATTACH_PATHNAME_W</span><span class="sxs-lookup"><span data-stu-id="b42b8-107">PR_ATTACH_PATHNAME, PR_ATTACH_PATHNAME_A, PR_ATTACH_PATHNAME_W</span></span>  <br/> |
|<span data-ttu-id="b42b8-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="b42b8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b42b8-109">0x3708</span><span class="sxs-lookup"><span data-stu-id="b42b8-109">0x3708</span></span>  <br/> |
|<span data-ttu-id="b42b8-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="b42b8-110">Data type:</span></span>  <br/> |<span data-ttu-id="b42b8-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b42b8-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="b42b8-112">領域:</span><span class="sxs-lookup"><span data-stu-id="b42b8-112">Area:</span></span>  <br/> |<span data-ttu-id="b42b8-113">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="b42b8-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b42b8-114">備考</span><span class="sxs-lookup"><span data-stu-id="b42b8-114">Remarks</span></span>

<span data-ttu-id="b42b8-115">添付ファイルの下位オブジェクトがこれらのプロパティを公開することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="b42b8-115">It is recommended that attachment subobjects expose these properties.</span></span> <span data-ttu-id="b42b8-116">それらの設定は、添付ファイルのデータがメッセージに含まれていないが、共通のファイル ・ サーバで使用可能なことを示します。</span><span class="sxs-lookup"><span data-stu-id="b42b8-116">Setting them indicates that the attachment data is not included with the message but is available on a common file server.</span></span> <span data-ttu-id="b42b8-117">これらのプロパティが参照渡しで添付ファイルを示す**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) のフラグのいずれかと共に必要な: **ATTACH_BY_REFERENCE**、 **ATTACH_BY_REF_RESOLVE**、または**ATTACH_BY_REF_だけ**。</span><span class="sxs-lookup"><span data-stu-id="b42b8-117">These properties are required in conjunction with any of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) flags that indicate attachment by reference: **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**, or **ATTACH_BY_REF_ONLY**.</span></span> 
  
<span data-ttu-id="b42b8-118">各ディレクトリまたはファイル名は、8 文字の名前と拡張子が 3 文字に制限されています。</span><span class="sxs-lookup"><span data-stu-id="b42b8-118">Each directory or filename is restricted to an eight-character name plus a three-character extension.</span></span> <span data-ttu-id="b42b8-119">全体的なパスでは、256 文字に制限されます。</span><span class="sxs-lookup"><span data-stu-id="b42b8-119">The overall path is restricted to 256 characters.</span></span> <span data-ttu-id="b42b8-120">長いファイル名をサポートしているプラットフォームでは、これらのプロパティと**PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)) の両方を設定します。</span><span class="sxs-lookup"><span data-stu-id="b42b8-120">For a platform that supports long filenames, set both these properties and **PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)).</span></span> 
  
<span data-ttu-id="b42b8-121">クライアント アプリケーションは、ファイルが共有され、ファイルがローカルの絶対パスを使用する必要があるときに、ほとんどの場合、汎用名前付け規則 (UNC) を使用します。</span><span class="sxs-lookup"><span data-stu-id="b42b8-121">Client applications should use a universal naming convention (UNC) in most cases when the file is shared, and should use an absolute path when the file is local.</span></span>
  
<span data-ttu-id="b42b8-122">MAPI はパスとファイル名に ANSI 文字セットです。</span><span class="sxs-lookup"><span data-stu-id="b42b8-122">MAPI works only with paths and filenames in the ANSI character set.</span></span> <span data-ttu-id="b42b8-123">OEM 文字セット内のパスとファイル名を使用するクライアントする必要があります ANSI に変換する、MAPI を呼び出す前にします。</span><span class="sxs-lookup"><span data-stu-id="b42b8-123">Clients that use paths and filenames in an OEM character set must convert them to ANSI before calling MAPI.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="b42b8-124">関連リソース</span><span class="sxs-lookup"><span data-stu-id="b42b8-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b42b8-125">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="b42b8-125">Protocol specifications</span></span>

<span data-ttu-id="b42b8-126">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b42b8-126">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b42b8-127">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="b42b8-127">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="b42b8-128">[[MS OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b42b8-128">[[MS-OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b42b8-129">権限管理でエンコードされたメッセージのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="b42b8-129">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b42b8-130">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="b42b8-130">Header files</span></span>

<span data-ttu-id="b42b8-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b42b8-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="b42b8-132">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="b42b8-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="b42b8-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b42b8-133">Mapitags.h</span></span>
  
> <span data-ttu-id="b42b8-134">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b42b8-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b42b8-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="b42b8-135">See also</span></span>



[<span data-ttu-id="b42b8-136">ScLocalPathFromUNC</span><span class="sxs-lookup"><span data-stu-id="b42b8-136">ScLocalPathFromUNC</span></span>](sclocalpathfromunc.md)
  
[<span data-ttu-id="b42b8-137">ScUNCFromLocalPath</span><span class="sxs-lookup"><span data-stu-id="b42b8-137">ScUNCFromLocalPath</span></span>](scuncfromlocalpath.md)


[<span data-ttu-id="b42b8-138">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="b42b8-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b42b8-139">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="b42b8-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b42b8-140">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="b42b8-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b42b8-141">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="b42b8-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

