---
title: PidTagAddressType 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAddressType
api_type:
- HeaderDef
ms.assetid: 986719d2-8837-46b4-8d04-c24508f5e19a
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 464121a969beea06294049985052eb150651765f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580090"
---
# <a name="pidtagaddresstype-canonical-property"></a><span data-ttu-id="3fca1-103">PidTagAddressType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="3fca1-103">PidTagAddressType Canonical Property</span></span>

<span data-ttu-id="3fca1-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3fca1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3fca1-105">SMTP など、メッセージング ユーザーの電子メール アドレスの種類が含まれています。</span><span class="sxs-lookup"><span data-stu-id="3fca1-105">Contains the messaging user's email address type, such as SMTP.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3fca1-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="3fca1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3fca1-107">PR_ADDRTYPE、PR_ADDRTYPE_A、PR_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="3fca1-107">PR_ADDRTYPE, PR_ADDRTYPE_A, PR_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="3fca1-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="3fca1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3fca1-109">0x3002</span><span class="sxs-lookup"><span data-stu-id="3fca1-109">0x3002</span></span>  <br/> |
|<span data-ttu-id="3fca1-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="3fca1-110">Data type:</span></span>  <br/> |<span data-ttu-id="3fca1-111">PT_UNICODE、PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="3fca1-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="3fca1-112">領域:</span><span class="sxs-lookup"><span data-stu-id="3fca1-112">Area:</span></span>  <br/> |<span data-ttu-id="3fca1-113">Address</span><span class="sxs-lookup"><span data-stu-id="3fca1-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3fca1-114">注釈</span><span class="sxs-lookup"><span data-stu-id="3fca1-114">Remarks</span></span>

<span data-ttu-id="3fca1-115">これらのプロパティでは、すべてのメッセージング ユーザーに共通の基本のアドレスのプロパティの例を示します。</span><span class="sxs-lookup"><span data-stu-id="3fca1-115">These properties are examples of the base address properties common to all messaging users.</span></span> <span data-ttu-id="3fca1-116">どのメッセージング システムの特定のメッセージを処理するために MAPI を使用して指定します。</span><span class="sxs-lookup"><span data-stu-id="3fca1-116">It specifies which messaging system MAPI uses to handle a given message.</span></span>
  
<span data-ttu-id="3fca1-117">このプロパティは、 **PR_EMAIL_ADRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) のアドレスの文字列の形式も決まります。</span><span class="sxs-lookup"><span data-stu-id="3fca1-117">This property also determines the format of the address string in the **PR_EMAIL_ADRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)).</span></span> <span data-ttu-id="3fca1-118">提供する文字列には、A Z からの大文字のアルファベット文字のみ、0 から 9 までの番号を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="3fca1-118">The string it provides can contain only the uppercase alphabetic characters from A through Z and the numbers from 0 through 9.</span></span>
  
<span data-ttu-id="3fca1-119">文字列の有効な例は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="3fca1-119">Valid examples for the string include:</span></span> 
  
```cpp
FAX
MHS
PROFS
SMTP
X400

```

## <a name="related-resources"></a><span data-ttu-id="3fca1-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="3fca1-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3fca1-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="3fca1-121">Protocol specifications</span></span>

<span data-ttu-id="3fca1-122">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3fca1-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3fca1-123">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="3fca1-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3fca1-124">[[MS OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3fca1-124">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3fca1-125">プロパティとユーザー、連絡先、グループ、およびリソースのリストの操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="3fca1-125">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="3fca1-126">[[MS OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3fca1-126">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3fca1-127">メッセージ オブジェクト インターネット標準の電子メールの表記規則からに変換します。</span><span class="sxs-lookup"><span data-stu-id="3fca1-127">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="3fca1-128">[[MS NSPI]](http://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3fca1-128">[[MS-NSPI]](http://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3fca1-129">ネーム サービス プロバイダー インターフェイス (NSPI) サーバーとクライアントの通信を処理します。</span><span class="sxs-lookup"><span data-stu-id="3fca1-129">Handles a client's communications with a Name Service Provider Interface (NSPI) server.</span></span>
    
<span data-ttu-id="3fca1-130">[[MS OXCDATA]](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3fca1-130">[[MS-OXCDATA]](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3fca1-131">リモート操作で使用される基本的なデータ構造を定義します。</span><span class="sxs-lookup"><span data-stu-id="3fca1-131">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="3fca1-132">[[MS OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3fca1-132">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3fca1-133">順序と、クライアントとサーバー間のデータ転送のフローを処理します。</span><span class="sxs-lookup"><span data-stu-id="3fca1-133">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="3fca1-134">[[MS OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3fca1-134">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3fca1-135">IETF RFC2445、RFC2446、RFC2447、および予定と会議のオブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="3fca1-135">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="3fca1-136">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3fca1-136">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3fca1-137">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="3fca1-137">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="3fca1-138">[[MS OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3fca1-138">[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3fca1-139">コア メッセージのストア オブジェクトの許可された操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="3fca1-139">Specifies permissible operations for the core message store objects.</span></span>
    
<span data-ttu-id="3fca1-140">[[MS OXOABKT]](http://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3fca1-140">[[MS-OXOABKT]](http://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3fca1-141">プロパティは、アドレス帳のテンプレートの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="3fca1-141">Specifies the properties and operations that are permissible for address book templates.</span></span>
    
<span data-ttu-id="3fca1-142">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3fca1-142">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3fca1-143">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="3fca1-143">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="3fca1-144">[[MS OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3fca1-144">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3fca1-145">サーバー上の受信電子メール メッセージを操作します。</span><span class="sxs-lookup"><span data-stu-id="3fca1-145">Manipulates incoming email messages on a server.</span></span>
    
<span data-ttu-id="3fca1-146">[[MS OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3fca1-146">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3fca1-147">プロパティや検索フォルダーの一覧の構成を操作するための動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="3fca1-147">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3fca1-148">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="3fca1-148">Header files</span></span>

<span data-ttu-id="3fca1-149">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3fca1-149">Mapidefs.h</span></span>
  
> <span data-ttu-id="3fca1-150">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="3fca1-150">Provides data type definitions.</span></span>
    
<span data-ttu-id="3fca1-151">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3fca1-151">Mapitags.h</span></span>
  
> <span data-ttu-id="3fca1-152">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="3fca1-152">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3fca1-153">関連項目</span><span class="sxs-lookup"><span data-stu-id="3fca1-153">See also</span></span>



[<span data-ttu-id="3fca1-154">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="3fca1-154">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3fca1-155">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="3fca1-155">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3fca1-156">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="3fca1-156">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3fca1-157">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="3fca1-157">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
  
[<span data-ttu-id="3fca1-158">MAPI アドレスの種類</span><span class="sxs-lookup"><span data-stu-id="3fca1-158">MAPI Address Types</span></span>](mapi-address-types.md)

