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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 45b6b3fb0c67d854fddf3773c06cef7b36f54992
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339327"
---
# <a name="pidtagattachlongfilename-canonical-property"></a><span data-ttu-id="385a0-103">PidTagAttachLongFilename 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="385a0-103">PidTagAttachLongFilename Canonical Property</span></span>

  
  
<span data-ttu-id="385a0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="385a0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="385a0-105">パスを除く添付ファイルの長いファイル名と拡張子を含む。</span><span class="sxs-lookup"><span data-stu-id="385a0-105">Contains an attachment's long filename and extension, excluding path.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="385a0-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="385a0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="385a0-107">PR_ATTACH_LONG_FILENAME、PR_ATTACH_LONG_FILENAME_A、PR_ATTACH_LONG_FILENAME_W</span><span class="sxs-lookup"><span data-stu-id="385a0-107">PR_ATTACH_LONG_FILENAME, PR_ATTACH_LONG_FILENAME_A, PR_ATTACH_LONG_FILENAME_W</span></span>  <br/> |
|<span data-ttu-id="385a0-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="385a0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="385a0-109">0x3707</span><span class="sxs-lookup"><span data-stu-id="385a0-109">0x3707</span></span>  <br/> |
|<span data-ttu-id="385a0-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="385a0-110">Data type:</span></span>  <br/> |<span data-ttu-id="385a0-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="385a0-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="385a0-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="385a0-112">Area:</span></span>  <br/> |<span data-ttu-id="385a0-113">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="385a0-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="385a0-114">注釈</span><span class="sxs-lookup"><span data-stu-id="385a0-114">Remarks</span></span>

<span data-ttu-id="385a0-115">これらのプロパティは、ATTACH_BY_VALUE(PidTagAttachMethod) プロパティの ATTACH_BY_VALUE、ATTACH_BY_REFERENCE、ATTACH_BY_REF_RESOLVE、ATTACH_BY_REF_ONLY **PR_ATTACH_METHOD** の値に関連 [](pidtagattachmethod-canonical-property.md)します。</span><span class="sxs-lookup"><span data-stu-id="385a0-115">These properties pertain to the ATTACH_BY_VALUE, ATTACH_BY_REFERENCE, ATTACH_BY_REF_RESOLVE, and ATTACH_BY_REF_ONLY values of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) property.</span></span> <span data-ttu-id="385a0-116">長いファイル **名** をサポートするプラットフォームでは、送信時に **PR_ATTACH_LONG_FILENAME** プロパティと **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) プロパティの両方を設定し、受信時に最初に PR_ATTACH_LONG_FILENAME を確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="385a0-116">Platforms that support long filenames should set both the **PR_ATTACH_LONG_FILENAME** and **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) properties when sending, and should check **PR_ATTACH_LONG_FILENAME** first when receiving.</span></span> 
  
<span data-ttu-id="385a0-117">クライアント アプリケーションは、メッセージを受信するホスト コンピューターが長いファイル名をサポートしている場合に使用する推奨される長いファイル名にこのプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="385a0-117">The client application should set this property to a suggested long filename to be used if the host computer receiving a message supports long filenames.</span></span> <span data-ttu-id="385a0-118">**PR_ATTACH_LONG_FILENAME** を保存するファイル名として使用し **、PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) プロパティが指定されていない場合は、ファイル名の拡張子を指定できます。</span><span class="sxs-lookup"><span data-stu-id="385a0-118">**PR_ATTACH_LONG_FILENAME** can be used as a filename for saving the attachment, and to supply the filename extension if the **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) property is not provided.</span></span> 
  
<span data-ttu-id="385a0-119">PR_ATTACH_FILENAME によって提供 **されるファイル名** とは異なり、この名前は 8 文字のファイル名と 3 文字の拡張子に制限されません。</span><span class="sxs-lookup"><span data-stu-id="385a0-119">Unlike the filename provided by **PR_ATTACH_FILENAME**, this name is not restricted to an eight-character filename plus a three-character extension.</span></span> <span data-ttu-id="385a0-120">その代わりに、ファイル名、拡張子、区切り記号のピリオドを含む最大 256 文字の長い文字を指定できます。</span><span class="sxs-lookup"><span data-stu-id="385a0-120">Instead, it can be up to 256 characters long, including the filename, extension, and separator period.</span></span> 
  
<span data-ttu-id="385a0-121">MAPI は、ANSI 文字セット内のファイル名でのみ動作します。</span><span class="sxs-lookup"><span data-stu-id="385a0-121">MAPI works only with filenames in the ANSI character set.</span></span> <span data-ttu-id="385a0-122">OEM 文字セットでファイル名を使用するクライアント アプリケーションは、MAPI を呼び出す前に ANSI に変換する必要があります。</span><span class="sxs-lookup"><span data-stu-id="385a0-122">Client applications that use filenames in an OEM character set must convert them to ANSI before calling MAPI.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="385a0-123">関連リソース</span><span class="sxs-lookup"><span data-stu-id="385a0-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="385a0-124">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="385a0-124">Protocol specifications</span></span>

<span data-ttu-id="385a0-125">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="385a0-125">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="385a0-126">メッセージ オブジェクトと添付ファイル オブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="385a0-126">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="385a0-127">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="385a0-127">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="385a0-128">インターネット標準の電子メール規則からメッセージ オブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="385a0-128">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="385a0-129">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="385a0-129">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="385a0-130">権限で管理されたエンコードされたメッセージのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="385a0-130">Specifies the properties of rights-managed encoded messages.</span></span>
    
<span data-ttu-id="385a0-131">[[MS-OXOUM]](https://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="385a0-131">[[MS-OXOUM]](https://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="385a0-132">ボイス メールおよび FAX メッセージを表す場合に許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="385a0-132">Specifies the properties and operations that are permissible for representing voice mail and fax messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="385a0-133">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="385a0-133">Header files</span></span>

<span data-ttu-id="385a0-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="385a0-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="385a0-135">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="385a0-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="385a0-136">Mmapitags.h</span><span class="sxs-lookup"><span data-stu-id="385a0-136">Mmapitags.h</span></span>
  
> <span data-ttu-id="385a0-137">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="385a0-137">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="385a0-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="385a0-138">See also</span></span>



[<span data-ttu-id="385a0-139">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="385a0-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="385a0-140">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="385a0-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="385a0-141">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="385a0-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="385a0-142">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="385a0-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

