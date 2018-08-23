---
title: PidTagSendInternetEncoding 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSendInternetEncoding
api_type:
- COM
ms.assetid: ae408b4f-dee3-484b-a19c-f472cfa95996
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 33b9931a269eb4b5ee0429287d60fa1962b0e4f2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584234"
---
# <a name="pidtagsendinternetencoding-canonical-property"></a><span data-ttu-id="74388-103">PidTagSendInternetEncoding 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="74388-103">PidTagSendInternetEncoding Canonical Property</span></span>

  
  
<span data-ttu-id="74388-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="74388-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="74388-105">環境設定のエンコーディングのビットマスクを格納します。</span><span class="sxs-lookup"><span data-stu-id="74388-105">Contains a bitmask of encoding preferences.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="74388-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="74388-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="74388-107">PR_SEND_INTERNET_ENCODING</span><span class="sxs-lookup"><span data-stu-id="74388-107">PR_SEND_INTERNET_ENCODING</span></span>  <br/> |
|<span data-ttu-id="74388-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="74388-108">Identifier:</span></span>  <br/> |<span data-ttu-id="74388-109">0x3A71</span><span class="sxs-lookup"><span data-stu-id="74388-109">0x3A71</span></span>  <br/> |
|<span data-ttu-id="74388-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="74388-110">Data type:</span></span>  <br/> |<span data-ttu-id="74388-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="74388-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="74388-112">領域:</span><span class="sxs-lookup"><span data-stu-id="74388-112">Area:</span></span>  <br/> |<span data-ttu-id="74388-113">Address</span><span class="sxs-lookup"><span data-stu-id="74388-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="74388-114">注釈</span><span class="sxs-lookup"><span data-stu-id="74388-114">Remarks</span></span>

<span data-ttu-id="74388-115">使用するエンコード オプションを指定するには、このプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="74388-115">Set this property to indicate the encoding options used.</span></span> 
  
<span data-ttu-id="74388-116">このプロパティには、次のフラグが含まれています。</span><span class="sxs-lookup"><span data-stu-id="74388-116">This property contains the following flags:</span></span>
  
<span data-ttu-id="74388-117">BODY_ENCODING_HTML</span><span class="sxs-lookup"><span data-stu-id="74388-117">BODY_ENCODING_HTML</span></span> 
  
> <span data-ttu-id="74388-118">Html 形式でメッセージのテキストをエンコードします。</span><span class="sxs-lookup"><span data-stu-id="74388-118">Encode the message text in HTML.</span></span> <span data-ttu-id="74388-119">ENCODING_MIME フラグが設定されていない場合、このフラグは無視されます。</span><span class="sxs-lookup"><span data-stu-id="74388-119">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="74388-120">BODY_ENCODING_TEXT_AND_HTML</span><span class="sxs-lookup"><span data-stu-id="74388-120">BODY_ENCODING_TEXT_AND_HTML</span></span> 
  
> <span data-ttu-id="74388-121">多目的インターネット メール拡張 (MIME) の複数の代替手段として、テキストと HTML を使用してメッセージのテキストをエンコードします。</span><span class="sxs-lookup"><span data-stu-id="74388-121">Encode the message text using text and HTML as Multipurpose Internet Mail Extensions (MIME) multipart alternatives.</span></span> <span data-ttu-id="74388-122">ENCODING_MIME フラグが設定されていない場合、このフラグは無視されます。</span><span class="sxs-lookup"><span data-stu-id="74388-122">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="74388-123">ENCODING_MIME</span><span class="sxs-lookup"><span data-stu-id="74388-123">ENCODING_MIME</span></span> 
  
> <span data-ttu-id="74388-124">MIME を使用してメッセージをエンコードします。</span><span class="sxs-lookup"><span data-stu-id="74388-124">Encode the message using MIME.</span></span> <span data-ttu-id="74388-125">このフラグが設定されていない場合、MAPI は、テキスト形式でメッセージのテキストと、UUENCODE の添付ファイルをエンコードします。</span><span class="sxs-lookup"><span data-stu-id="74388-125">If this flag is not set, MAPI encodes the message text in plain text and the attachments in UUENCODE.</span></span> 
    
<span data-ttu-id="74388-126">ENCODING_PREFERENCE</span><span class="sxs-lookup"><span data-stu-id="74388-126">ENCODING_PREFERENCE</span></span> 
  
> <span data-ttu-id="74388-127">このビットマスクで他のフラグを使用して、エンコーディングを判断します。</span><span class="sxs-lookup"><span data-stu-id="74388-127">Use the other flags in this bitmask to determine the encoding.</span></span> <span data-ttu-id="74388-128">このフラグが設定されていない場合は、MAPI はエンコードを決定するメッセージング システムに残ります。</span><span class="sxs-lookup"><span data-stu-id="74388-128">If this flag is not set, MAPI leaves it to the messaging system to make encoding decisions.</span></span> 
    
<span data-ttu-id="74388-129">MAC_ATTACH_ENCODING_APPLEDOUBLE</span><span class="sxs-lookup"><span data-stu-id="74388-129">MAC_ATTACH_ENCODING_APPLEDOUBLE</span></span> 
  
> <span data-ttu-id="74388-130">Apple の二重モードで、Macintosh の添付ファイルをエンコードします。</span><span class="sxs-lookup"><span data-stu-id="74388-130">Encode Macintosh attachments in Apple double mode.</span></span> <span data-ttu-id="74388-131">ENCODING_MIME フラグが設定されていない場合、このフラグは無視されます。</span><span class="sxs-lookup"><span data-stu-id="74388-131">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="74388-132">MAC_ATTACH_ENCODING_APPLESINGLE</span><span class="sxs-lookup"><span data-stu-id="74388-132">MAC_ATTACH_ENCODING_APPLESINGLE</span></span> 
  
> <span data-ttu-id="74388-133">Apple の 1 つのモードで、Macintosh の添付ファイルをエンコードします。</span><span class="sxs-lookup"><span data-stu-id="74388-133">Encode Macintosh attachments in Apple single mode.</span></span> <span data-ttu-id="74388-134">ENCODING_MIME フラグが設定されていない場合、このフラグは無視されます。</span><span class="sxs-lookup"><span data-stu-id="74388-134">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="74388-135">MAC_ATTACH_ENCODING_UUENCODE</span><span class="sxs-lookup"><span data-stu-id="74388-135">MAC_ATTACH_ENCODING_UUENCODE</span></span> 
  
> <span data-ttu-id="74388-136">Macintosh 添付ファイルを UUENCODE でエンコードします。</span><span class="sxs-lookup"><span data-stu-id="74388-136">Encode Macintosh attachments in UUENCODE.</span></span> <span data-ttu-id="74388-137">ENCODING_MIME フラグが設定されている場合は、このフラグは無視され、BinHex エンコーディングが代わりに使用します。</span><span class="sxs-lookup"><span data-stu-id="74388-137">If the ENCODING_MIME flag is set, this flag is ignored and BinHex encoding is used instead.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="74388-138">関連リソース</span><span class="sxs-lookup"><span data-stu-id="74388-138">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="74388-139">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="74388-139">Protocol specifications</span></span>

<span data-ttu-id="74388-140">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="74388-140">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="74388-141">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="74388-141">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="74388-142">[[MS OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="74388-142">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="74388-143">プロパティとユーザー、連絡先、グループ、およびリソースのリストの操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="74388-143">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="74388-144">[[MS OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="74388-144">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="74388-145">メッセージ オブジェクト インターネット標準の電子メールの表記規則からに変換します。</span><span class="sxs-lookup"><span data-stu-id="74388-145">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="74388-146">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="74388-146">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="74388-147">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="74388-147">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="74388-148">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="74388-148">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="74388-149">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="74388-149">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="74388-150">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="74388-150">Header files</span></span>

<span data-ttu-id="74388-151">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="74388-151">Mapidefs.h</span></span>
  
> <span data-ttu-id="74388-152">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="74388-152">Provides data type definitions.</span></span>
    
<span data-ttu-id="74388-153">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="74388-153">Mapitags.h</span></span>
  
> <span data-ttu-id="74388-154">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="74388-154">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="74388-155">関連項目</span><span class="sxs-lookup"><span data-stu-id="74388-155">See also</span></span>



[<span data-ttu-id="74388-156">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="74388-156">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="74388-157">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="74388-157">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="74388-158">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="74388-158">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="74388-159">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="74388-159">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

