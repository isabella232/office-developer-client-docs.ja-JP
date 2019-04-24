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
ms.openlocfilehash: e157fa640026d13362084b30ad73cdb66a0b35b5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342673"
---
# <a name="pidtagsendinternetencoding-canonical-property"></a><span data-ttu-id="e5cd7-103">PidTagSendInternetEncoding 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e5cd7-103">PidTagSendInternetEncoding Canonical Property</span></span>

  
  
<span data-ttu-id="e5cd7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e5cd7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e5cd7-105">エンコード設定のビットマスクを含みます。</span><span class="sxs-lookup"><span data-stu-id="e5cd7-105">Contains a bitmask of encoding preferences.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e5cd7-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="e5cd7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e5cd7-107">PR_SEND_INTERNET_ENCODING</span><span class="sxs-lookup"><span data-stu-id="e5cd7-107">PR_SEND_INTERNET_ENCODING</span></span>  <br/> |
|<span data-ttu-id="e5cd7-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="e5cd7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e5cd7-109">0x3a71</span><span class="sxs-lookup"><span data-stu-id="e5cd7-109">0x3A71</span></span>  <br/> |
|<span data-ttu-id="e5cd7-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="e5cd7-110">Data type:</span></span>  <br/> |<span data-ttu-id="e5cd7-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e5cd7-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="e5cd7-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="e5cd7-112">Area:</span></span>  <br/> |<span data-ttu-id="e5cd7-113">Address</span><span class="sxs-lookup"><span data-stu-id="e5cd7-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e5cd7-114">解説</span><span class="sxs-lookup"><span data-stu-id="e5cd7-114">Remarks</span></span>

<span data-ttu-id="e5cd7-115">このプロパティを設定して、使用するエンコードオプションを指定します。</span><span class="sxs-lookup"><span data-stu-id="e5cd7-115">Set this property to indicate the encoding options used.</span></span> 
  
<span data-ttu-id="e5cd7-116">このプロパティには、次のフラグが含まれています。</span><span class="sxs-lookup"><span data-stu-id="e5cd7-116">This property contains the following flags:</span></span>
  
<span data-ttu-id="e5cd7-117">BODY_ENCODING_HTML</span><span class="sxs-lookup"><span data-stu-id="e5cd7-117">BODY_ENCODING_HTML</span></span> 
  
> <span data-ttu-id="e5cd7-118">メッセージテキストを HTML 形式でエンコードします。</span><span class="sxs-lookup"><span data-stu-id="e5cd7-118">Encode the message text in HTML.</span></span> <span data-ttu-id="e5cd7-119">ENCODING_MIME フラグが設定されていない場合、このフラグは無視されます。</span><span class="sxs-lookup"><span data-stu-id="e5cd7-119">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="e5cd7-120">BODY_ENCODING_TEXT_AND_HTML</span><span class="sxs-lookup"><span data-stu-id="e5cd7-120">BODY_ENCODING_TEXT_AND_HTML</span></span> 
  
> <span data-ttu-id="e5cd7-121">テキストと HTML を使用して、メッセージテキストをエンコードするマルチパーパスインターネットメール拡張機能 (MIME) マルチパートの代替手段として使用します。</span><span class="sxs-lookup"><span data-stu-id="e5cd7-121">Encode the message text using text and HTML as Multipurpose Internet Mail Extensions (MIME) multipart alternatives.</span></span> <span data-ttu-id="e5cd7-122">ENCODING_MIME フラグが設定されていない場合、このフラグは無視されます。</span><span class="sxs-lookup"><span data-stu-id="e5cd7-122">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="e5cd7-123">ENCODING_MIME</span><span class="sxs-lookup"><span data-stu-id="e5cd7-123">ENCODING_MIME</span></span> 
  
> <span data-ttu-id="e5cd7-124">MIME を使用してメッセージをエンコードします。</span><span class="sxs-lookup"><span data-stu-id="e5cd7-124">Encode the message using MIME.</span></span> <span data-ttu-id="e5cd7-125">このフラグが設定されていない場合、MAPI はテキスト形式のメッセージテキストと UUENCODE の添付ファイルをエンコードします。</span><span class="sxs-lookup"><span data-stu-id="e5cd7-125">If this flag is not set, MAPI encodes the message text in plain text and the attachments in UUENCODE.</span></span> 
    
<span data-ttu-id="e5cd7-126">ENCODING_PREFERENCE</span><span class="sxs-lookup"><span data-stu-id="e5cd7-126">ENCODING_PREFERENCE</span></span> 
  
> <span data-ttu-id="e5cd7-127">このビットマスクの他のフラグを使用して、エンコーディングを決定します。</span><span class="sxs-lookup"><span data-stu-id="e5cd7-127">Use the other flags in this bitmask to determine the encoding.</span></span> <span data-ttu-id="e5cd7-128">このフラグが設定されていない場合、MAPI はメッセージングシステムにメッセージを発信して、エンコード決定を行います。</span><span class="sxs-lookup"><span data-stu-id="e5cd7-128">If this flag is not set, MAPI leaves it to the messaging system to make encoding decisions.</span></span> 
    
<span data-ttu-id="e5cd7-129">MAC_ATTACH_ENCODING_APPLEDOUBLE</span><span class="sxs-lookup"><span data-stu-id="e5cd7-129">MAC_ATTACH_ENCODING_APPLEDOUBLE</span></span> 
  
> <span data-ttu-id="e5cd7-130">Macintosh の添付ファイルを Apple のダブルモードでエンコードします。</span><span class="sxs-lookup"><span data-stu-id="e5cd7-130">Encode Macintosh attachments in Apple double mode.</span></span> <span data-ttu-id="e5cd7-131">ENCODING_MIME フラグが設定されていない場合、このフラグは無視されます。</span><span class="sxs-lookup"><span data-stu-id="e5cd7-131">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="e5cd7-132">MAC_ATTACH_ENCODING_APPLESINGLE</span><span class="sxs-lookup"><span data-stu-id="e5cd7-132">MAC_ATTACH_ENCODING_APPLESINGLE</span></span> 
  
> <span data-ttu-id="e5cd7-133">Macintosh の添付ファイルを Apple のシングルモードでエンコードします。</span><span class="sxs-lookup"><span data-stu-id="e5cd7-133">Encode Macintosh attachments in Apple single mode.</span></span> <span data-ttu-id="e5cd7-134">ENCODING_MIME フラグが設定されていない場合、このフラグは無視されます。</span><span class="sxs-lookup"><span data-stu-id="e5cd7-134">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="e5cd7-135">MAC_ATTACH_ENCODING_UUENCODE</span><span class="sxs-lookup"><span data-stu-id="e5cd7-135">MAC_ATTACH_ENCODING_UUENCODE</span></span> 
  
> <span data-ttu-id="e5cd7-136">UUENCODE で Macintosh の添付ファイルをエンコードします。</span><span class="sxs-lookup"><span data-stu-id="e5cd7-136">Encode Macintosh attachments in UUENCODE.</span></span> <span data-ttu-id="e5cd7-137">ENCODING_MIME フラグが設定されている場合、このフラグは無視され、代わりに BinHex エンコードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="e5cd7-137">If the ENCODING_MIME flag is set, this flag is ignored and BinHex encoding is used instead.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="e5cd7-138">関連リソース</span><span class="sxs-lookup"><span data-stu-id="e5cd7-138">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e5cd7-139">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="e5cd7-139">Protocol specifications</span></span>

<span data-ttu-id="e5cd7-140">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e5cd7-140">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e5cd7-141">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="e5cd7-141">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e5cd7-142">[[OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e5cd7-142">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e5cd7-143">ユーザー、連絡先、グループ、およびリソースのリストのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="e5cd7-143">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="e5cd7-144">[[OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e5cd7-144">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e5cd7-145">インターネット標準の電子メールの規則からメッセージオブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="e5cd7-145">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="e5cd7-146">[[OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e5cd7-146">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e5cd7-147">メッセージと添付ファイルオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="e5cd7-147">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="e5cd7-148">[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e5cd7-148">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e5cd7-149">電子メールメッセージオブジェクトに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="e5cd7-149">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e5cd7-150">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="e5cd7-150">Header files</span></span>

<span data-ttu-id="e5cd7-151">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e5cd7-151">Mapidefs.h</span></span>
  
> <span data-ttu-id="e5cd7-152">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="e5cd7-152">Provides data type definitions.</span></span>
    
<span data-ttu-id="e5cd7-153">Mapitags</span><span class="sxs-lookup"><span data-stu-id="e5cd7-153">Mapitags.h</span></span>
  
> <span data-ttu-id="e5cd7-154">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="e5cd7-154">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e5cd7-155">関連項目</span><span class="sxs-lookup"><span data-stu-id="e5cd7-155">See also</span></span>



[<span data-ttu-id="e5cd7-156">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="e5cd7-156">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e5cd7-157">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e5cd7-157">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e5cd7-158">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e5cd7-158">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e5cd7-159">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="e5cd7-159">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

