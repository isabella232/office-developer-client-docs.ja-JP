---
title: PidTagAttachPathname 標準プロパティ
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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 05df7fe04f511de9310edc7a8ef09130e6354ad2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327231"
---
# <a name="pidtagattachpathname-canonical-property"></a><span data-ttu-id="ee080-103">PidTagAttachPathname 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ee080-103">PidTagAttachPathname Canonical Property</span></span>

  
  
<span data-ttu-id="ee080-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ee080-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ee080-105">添付ファイルの完全修飾パスとファイル名が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ee080-105">Contains an attachment's fully-qualified path and filename.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ee080-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="ee080-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ee080-107">PR_ATTACH_PATHNAME、PR_ATTACH_PATHNAME_A、PR_ATTACH_PATHNAME_W</span><span class="sxs-lookup"><span data-stu-id="ee080-107">PR_ATTACH_PATHNAME, PR_ATTACH_PATHNAME_A, PR_ATTACH_PATHNAME_W</span></span>  <br/> |
|<span data-ttu-id="ee080-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="ee080-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ee080-109">0x3708</span><span class="sxs-lookup"><span data-stu-id="ee080-109">0x3708</span></span>  <br/> |
|<span data-ttu-id="ee080-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="ee080-110">Data type:</span></span>  <br/> |<span data-ttu-id="ee080-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ee080-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="ee080-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="ee080-112">Area:</span></span>  <br/> |<span data-ttu-id="ee080-113">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="ee080-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ee080-114">解説</span><span class="sxs-lookup"><span data-stu-id="ee080-114">Remarks</span></span>

<span data-ttu-id="ee080-115">attachment サブオブジェクトは、これらのプロパティを公開することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="ee080-115">It is recommended that attachment subobjects expose these properties.</span></span> <span data-ttu-id="ee080-116">この設定は、添付ファイルデータがメッセージに含まれていないが、共通のファイルサーバーで使用できることを示します。</span><span class="sxs-lookup"><span data-stu-id="ee080-116">Setting them indicates that the attachment data is not included with the message but is available on a common file server.</span></span> <span data-ttu-id="ee080-117">これらのプロパティは、参照によって添付ファイルを示す**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) フラグのいずれか ( **ATTACH_BY_REFERENCE**、 **ATTACH_BY_REF_RESOLVE**、または ATTACH_BY_REF_) と組み合わせて使用する必要があります。 **のみ**です。</span><span class="sxs-lookup"><span data-stu-id="ee080-117">These properties are required in conjunction with any of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) flags that indicate attachment by reference: **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**, or **ATTACH_BY_REF_ONLY**.</span></span> 
  
<span data-ttu-id="ee080-118">各ディレクトリまたはファイル名は、8文字の名前と3文字の拡張子に制限されています。</span><span class="sxs-lookup"><span data-stu-id="ee080-118">Each directory or filename is restricted to an eight-character name plus a three-character extension.</span></span> <span data-ttu-id="ee080-119">全体のパスは、256文字に制限されています。</span><span class="sxs-lookup"><span data-stu-id="ee080-119">The overall path is restricted to 256 characters.</span></span> <span data-ttu-id="ee080-120">長いファイル名をサポートするプラットフォームでは、これらのプロパティと**PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)) の両方を設定します。</span><span class="sxs-lookup"><span data-stu-id="ee080-120">For a platform that supports long filenames, set both these properties and **PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)).</span></span> 
  
<span data-ttu-id="ee080-121">ほとんどの場合、クライアントアプリケーションは、ファイルが共有されている場合は汎用名前付け規則 (UNC) を使用し、ファイルがローカルの場合は絶対パスを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ee080-121">Client applications should use a universal naming convention (UNC) in most cases when the file is shared, and should use an absolute path when the file is local.</span></span>
  
<span data-ttu-id="ee080-122">MAPI は、ANSI 文字セットのパスとファイル名に対してのみ機能します。</span><span class="sxs-lookup"><span data-stu-id="ee080-122">MAPI works only with paths and filenames in the ANSI character set.</span></span> <span data-ttu-id="ee080-123">OEM 文字セットでパスとファイル名を使用するクライアントは、MAPI を呼び出す前に、それらを ANSI に変換する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ee080-123">Clients that use paths and filenames in an OEM character set must convert them to ANSI before calling MAPI.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ee080-124">関連リソース</span><span class="sxs-lookup"><span data-stu-id="ee080-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ee080-125">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="ee080-125">Protocol specifications</span></span>

<span data-ttu-id="ee080-126">[[OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ee080-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ee080-127">メッセージと添付ファイルオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="ee080-127">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="ee080-128">[[OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ee080-128">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ee080-129">権限が管理されたエンコード済みメッセージのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="ee080-129">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ee080-130">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="ee080-130">Header files</span></span>

<span data-ttu-id="ee080-131">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ee080-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="ee080-132">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="ee080-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="ee080-133">Mapitags</span><span class="sxs-lookup"><span data-stu-id="ee080-133">Mapitags.h</span></span>
  
> <span data-ttu-id="ee080-134">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ee080-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ee080-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="ee080-135">See also</span></span>



[<span data-ttu-id="ee080-136">ScLocalPathFromUNC</span><span class="sxs-lookup"><span data-stu-id="ee080-136">ScLocalPathFromUNC</span></span>](sclocalpathfromunc.md)
  
[<span data-ttu-id="ee080-137">ScUNCFromLocalPath</span><span class="sxs-lookup"><span data-stu-id="ee080-137">ScUNCFromLocalPath</span></span>](scuncfromlocalpath.md)


[<span data-ttu-id="ee080-138">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="ee080-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ee080-139">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ee080-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ee080-140">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="ee080-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ee080-141">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="ee080-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

