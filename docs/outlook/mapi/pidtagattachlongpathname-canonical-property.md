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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d8fe8525cf4fc11ac17ed6d73fb5d97e4f2d003e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339369"
---
# <a name="pidtagattachlongpathname-canonical-property"></a><span data-ttu-id="ec324-103">PidTagAttachLongPathname 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ec324-103">PidTagAttachLongPathname Canonical Property</span></span>

  
  
<span data-ttu-id="ec324-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ec324-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ec324-105">添付ファイルの完全修飾長いパスとファイル名を含む。</span><span class="sxs-lookup"><span data-stu-id="ec324-105">Contains an attachment's fully-qualified long path and filename.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ec324-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="ec324-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ec324-107">PR_ATTACH_LONG_PATHNAME、PR_ATTACH_LONG_PATHNAME_A、PR_ATTACH_LONG_PATHNAME_W</span><span class="sxs-lookup"><span data-stu-id="ec324-107">PR_ATTACH_LONG_PATHNAME, PR_ATTACH_LONG_PATHNAME_A, PR_ATTACH_LONG_PATHNAME_W</span></span>  <br/> |
|<span data-ttu-id="ec324-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="ec324-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ec324-109">0x370D</span><span class="sxs-lookup"><span data-stu-id="ec324-109">0x370D</span></span>  <br/> |
|<span data-ttu-id="ec324-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="ec324-110">Data type:</span></span>  <br/> |<span data-ttu-id="ec324-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ec324-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="ec324-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="ec324-112">Area:</span></span>  <br/> |<span data-ttu-id="ec324-113">メッセージの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="ec324-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ec324-114">注釈</span><span class="sxs-lookup"><span data-stu-id="ec324-114">Remarks</span></span>

<span data-ttu-id="ec324-115">これらのプロパティは、参照によって添付ファイルを示す **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) プロパティの値を使用する場合に適用されます **。ATTACH_BY_REFERENCE、ATTACH_BY_REF_RESOLVE、** または **ATTACH_BY_REF_ONLY**。 </span><span class="sxs-lookup"><span data-stu-id="ec324-115">These properties are applicable when you use any of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) property's values that indicate attachment by reference: **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**, or **ATTACH_BY_REF_ONLY**.</span></span> <span data-ttu-id="ec324-116">長いファイル名をサポートするプラットフォームでは、送信時に **PR_ATTACH_LONG_PATHNAME** プロパティまたは関連プロパティと PR_ATTACH_PATHNAME ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) プロパティの両方を設定し、受信時に **PR_ATTACH_LONG_PATHNAME** または関連するプロパティを最初にチェックする必要があります。 </span><span class="sxs-lookup"><span data-stu-id="ec324-116">Platforms that support long filenames should set both **PR_ATTACH_LONG_PATHNAME** or associated properties and **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) properties when sending, and should check **PR_ATTACH_LONG_PATHNAME** or associated properties first when receiving.</span></span> 
  
<span data-ttu-id="ec324-117">クライアント アプリケーションは、メッセージを受信するホスト コンピューターが長いファイル名をサポートしている場合に使用する推奨される長いパスとファイル名にこれらのプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ec324-117">The client application should set these properties to a suggested long path and filename to be used if the host machine receiving a message supports long filenames.</span></span> <span data-ttu-id="ec324-118">これらのプロパティを設定すると、添付ファイル データはメッセージに含まれませんが、共通のファイル サーバーで使用できます。</span><span class="sxs-lookup"><span data-stu-id="ec324-118">Setting these properties indicates that the attachment data is not included with the message but is available on a common file server.</span></span> 
  
<span data-ttu-id="ec324-119">PR_ATTACH_PATHNAME によって提供されるディレクトリとファイル名とは異 **なり**、これらのディレクトリとファイル名は、8 文字のディレクトリまたはファイル名と 3 文字の拡張子に制限されません。</span><span class="sxs-lookup"><span data-stu-id="ec324-119">Unlike the directories and filenames provided by **PR_ATTACH_PATHNAME**, these directories and filenames are not restricted to an eight-character directory or filename plus three-character extension.</span></span> <span data-ttu-id="ec324-120">代わりに、各ディレクトリまたはファイル名は、名前、拡張子、区切り記号のピリオドを含めて、最大 256 文字の長くすることができます。</span><span class="sxs-lookup"><span data-stu-id="ec324-120">Instead, each directory or filename can be up to 256 characters long, including the name, extension, and separator period.</span></span> <span data-ttu-id="ec324-121">ただし、全体のパスは 256 文字に制限されます。</span><span class="sxs-lookup"><span data-stu-id="ec324-121">However, the overall path is limited to 256 characters.</span></span> 
  
<span data-ttu-id="ec324-122">クライアントは、ファイルが共有されているほとんどの場合、汎用名前付け規則 (UNC) を使用し、ファイルがローカルの場合は絶対パスを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ec324-122">Clients should use a universal naming convention (UNC) in most cases when the file is shared, and should use an absolute path when the file is local.</span></span>
  
<span data-ttu-id="ec324-123">MAPI は、ANSI 文字セット内のパスとファイル名でのみ動作します。</span><span class="sxs-lookup"><span data-stu-id="ec324-123">MAPI works only with paths and filenames in the ANSI character set.</span></span> <span data-ttu-id="ec324-124">OEM 文字セットでパスとファイル名を使用するクライアント アプリケーションは、MAPI を呼び出す前に、それらを ANSI に変換する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ec324-124">Client applications that use paths and filenames in an OEM character set must convert them to ANSI before calling MAPI.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ec324-125">関連リソース</span><span class="sxs-lookup"><span data-stu-id="ec324-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ec324-126">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="ec324-126">Protocol specifications</span></span>

<span data-ttu-id="ec324-127">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ec324-127">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ec324-128">メッセージ オブジェクトと添付ファイル オブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="ec324-128">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="ec324-129">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ec324-129">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ec324-130">権限で管理されたエンコードされたメッセージのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="ec324-130">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ec324-131">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="ec324-131">Header files</span></span>

<span data-ttu-id="ec324-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ec324-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="ec324-133">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="ec324-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="ec324-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ec324-134">Mapitags.h</span></span>
  
> <span data-ttu-id="ec324-135">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="ec324-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ec324-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="ec324-136">See also</span></span>



[<span data-ttu-id="ec324-137">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="ec324-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ec324-138">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="ec324-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ec324-139">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="ec324-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ec324-140">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="ec324-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

