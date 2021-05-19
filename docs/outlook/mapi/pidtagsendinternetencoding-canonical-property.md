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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e157fa640026d13362084b30ad73cdb66a0b35b5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342673"
---
# <a name="pidtagsendinternetencoding-canonical-property"></a><span data-ttu-id="da5b7-103">PidTagSendInternetEncoding 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="da5b7-103">PidTagSendInternetEncoding Canonical Property</span></span>

  
  
<span data-ttu-id="da5b7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="da5b7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="da5b7-105">エンコードの基本設定のビットマスクが含まれる。</span><span class="sxs-lookup"><span data-stu-id="da5b7-105">Contains a bitmask of encoding preferences.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="da5b7-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="da5b7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="da5b7-107">PR_SEND_INTERNET_ENCODING</span><span class="sxs-lookup"><span data-stu-id="da5b7-107">PR_SEND_INTERNET_ENCODING</span></span>  <br/> |
|<span data-ttu-id="da5b7-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="da5b7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="da5b7-109">0x3A71</span><span class="sxs-lookup"><span data-stu-id="da5b7-109">0x3A71</span></span>  <br/> |
|<span data-ttu-id="da5b7-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="da5b7-110">Data type:</span></span>  <br/> |<span data-ttu-id="da5b7-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="da5b7-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="da5b7-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="da5b7-112">Area:</span></span>  <br/> |<span data-ttu-id="da5b7-113">Address</span><span class="sxs-lookup"><span data-stu-id="da5b7-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="da5b7-114">注釈</span><span class="sxs-lookup"><span data-stu-id="da5b7-114">Remarks</span></span>

<span data-ttu-id="da5b7-115">使用するエンコード オプションを示すために、このプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="da5b7-115">Set this property to indicate the encoding options used.</span></span> 
  
<span data-ttu-id="da5b7-116">このプロパティには、次のフラグが含まれます。</span><span class="sxs-lookup"><span data-stu-id="da5b7-116">This property contains the following flags:</span></span>
  
<span data-ttu-id="da5b7-117">BODY_ENCODING_HTML</span><span class="sxs-lookup"><span data-stu-id="da5b7-117">BODY_ENCODING_HTML</span></span> 
  
> <span data-ttu-id="da5b7-118">HTML でメッセージ テキストをエンコードします。</span><span class="sxs-lookup"><span data-stu-id="da5b7-118">Encode the message text in HTML.</span></span> <span data-ttu-id="da5b7-119">このフラグは、フラグが設定されていないENCODING_MIME無視されます。</span><span class="sxs-lookup"><span data-stu-id="da5b7-119">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="da5b7-120">BODY_ENCODING_TEXT_AND_HTML</span><span class="sxs-lookup"><span data-stu-id="da5b7-120">BODY_ENCODING_TEXT_AND_HTML</span></span> 
  
> <span data-ttu-id="da5b7-121">テキストと HTML を使用してメッセージ テキストを多目的インターネット メール拡張機能 (MIME) マルチパート代替としてエンコードします。</span><span class="sxs-lookup"><span data-stu-id="da5b7-121">Encode the message text using text and HTML as Multipurpose Internet Mail Extensions (MIME) multipart alternatives.</span></span> <span data-ttu-id="da5b7-122">このフラグは、フラグが設定されていないENCODING_MIME無視されます。</span><span class="sxs-lookup"><span data-stu-id="da5b7-122">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="da5b7-123">ENCODING_MIME</span><span class="sxs-lookup"><span data-stu-id="da5b7-123">ENCODING_MIME</span></span> 
  
> <span data-ttu-id="da5b7-124">MIME を使用してメッセージをエンコードします。</span><span class="sxs-lookup"><span data-stu-id="da5b7-124">Encode the message using MIME.</span></span> <span data-ttu-id="da5b7-125">このフラグを設定しない場合、MAPI はメッセージ テキストをプレーン テキストでエンコードし、添付ファイルは UUENCODE でエンコードします。</span><span class="sxs-lookup"><span data-stu-id="da5b7-125">If this flag is not set, MAPI encodes the message text in plain text and the attachments in UUENCODE.</span></span> 
    
<span data-ttu-id="da5b7-126">ENCODING_PREFERENCE</span><span class="sxs-lookup"><span data-stu-id="da5b7-126">ENCODING_PREFERENCE</span></span> 
  
> <span data-ttu-id="da5b7-127">エンコードを決定するには、このビットマスクの他のフラグを使用します。</span><span class="sxs-lookup"><span data-stu-id="da5b7-127">Use the other flags in this bitmask to determine the encoding.</span></span> <span data-ttu-id="da5b7-128">このフラグが設定されていない場合、MAPI はメッセージング システムに送信してエンコードの決定を行います。</span><span class="sxs-lookup"><span data-stu-id="da5b7-128">If this flag is not set, MAPI leaves it to the messaging system to make encoding decisions.</span></span> 
    
<span data-ttu-id="da5b7-129">MAC_ATTACH_ENCODING_APPLEDOUBLE</span><span class="sxs-lookup"><span data-stu-id="da5b7-129">MAC_ATTACH_ENCODING_APPLEDOUBLE</span></span> 
  
> <span data-ttu-id="da5b7-130">Apple ダブル モードで Macintosh 添付ファイルをエンコードします。</span><span class="sxs-lookup"><span data-stu-id="da5b7-130">Encode Macintosh attachments in Apple double mode.</span></span> <span data-ttu-id="da5b7-131">このフラグは、フラグが設定されていないENCODING_MIME無視されます。</span><span class="sxs-lookup"><span data-stu-id="da5b7-131">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="da5b7-132">MAC_ATTACH_ENCODING_APPLESINGLE</span><span class="sxs-lookup"><span data-stu-id="da5b7-132">MAC_ATTACH_ENCODING_APPLESINGLE</span></span> 
  
> <span data-ttu-id="da5b7-133">Apple シングル モードで Macintosh 添付ファイルをエンコードします。</span><span class="sxs-lookup"><span data-stu-id="da5b7-133">Encode Macintosh attachments in Apple single mode.</span></span> <span data-ttu-id="da5b7-134">このフラグは、フラグが設定されていないENCODING_MIME無視されます。</span><span class="sxs-lookup"><span data-stu-id="da5b7-134">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="da5b7-135">MAC_ATTACH_ENCODING_UUENCODE</span><span class="sxs-lookup"><span data-stu-id="da5b7-135">MAC_ATTACH_ENCODING_UUENCODE</span></span> 
  
> <span data-ttu-id="da5b7-136">UUENCODE で Macintosh 添付ファイルをエンコードします。</span><span class="sxs-lookup"><span data-stu-id="da5b7-136">Encode Macintosh attachments in UUENCODE.</span></span> <span data-ttu-id="da5b7-137">このフラグENCODING_MIME設定すると、このフラグは無視され、代わりに BinHex エンコードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="da5b7-137">If the ENCODING_MIME flag is set, this flag is ignored and BinHex encoding is used instead.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="da5b7-138">関連リソース</span><span class="sxs-lookup"><span data-stu-id="da5b7-138">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="da5b7-139">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="da5b7-139">Protocol specifications</span></span>

<span data-ttu-id="da5b7-140">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="da5b7-140">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="da5b7-141">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="da5b7-141">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="da5b7-142">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="da5b7-142">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="da5b7-143">ユーザー、連絡先、グループ、およびリソースの一覧のプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="da5b7-143">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="da5b7-144">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="da5b7-144">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="da5b7-145">インターネット標準の電子メール規則からメッセージ オブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="da5b7-145">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="da5b7-146">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="da5b7-146">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="da5b7-147">メッセージ オブジェクトと添付ファイル オブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="da5b7-147">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="da5b7-148">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="da5b7-148">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="da5b7-149">電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="da5b7-149">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="da5b7-150">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="da5b7-150">Header files</span></span>

<span data-ttu-id="da5b7-151">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="da5b7-151">Mapidefs.h</span></span>
  
> <span data-ttu-id="da5b7-152">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="da5b7-152">Provides data type definitions.</span></span>
    
<span data-ttu-id="da5b7-153">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="da5b7-153">Mapitags.h</span></span>
  
> <span data-ttu-id="da5b7-154">関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="da5b7-154">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="da5b7-155">関連項目</span><span class="sxs-lookup"><span data-stu-id="da5b7-155">See also</span></span>



[<span data-ttu-id="da5b7-156">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="da5b7-156">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="da5b7-157">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="da5b7-157">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="da5b7-158">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="da5b7-158">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="da5b7-159">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="da5b7-159">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

