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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 6051d3403cede21fa4aebdb6ca561dd3efb46771
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360087"
---
# <a name="pidtagaddresstype-canonical-property"></a><span data-ttu-id="6888f-103">PidTagAddressType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="6888f-103">PidTagAddressType Canonical Property</span></span>

<span data-ttu-id="6888f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6888f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6888f-105">SMTP などのメッセージング ユーザーの電子メール アドレスの種類が含まれる。</span><span class="sxs-lookup"><span data-stu-id="6888f-105">Contains the messaging user's email address type, such as SMTP.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6888f-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="6888f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6888f-107">PR_ADDRTYPE、PR_ADDRTYPE_A、PR_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="6888f-107">PR_ADDRTYPE, PR_ADDRTYPE_A, PR_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="6888f-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="6888f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6888f-109">0x3002</span><span class="sxs-lookup"><span data-stu-id="6888f-109">0x3002</span></span>  <br/> |
|<span data-ttu-id="6888f-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="6888f-110">Data type:</span></span>  <br/> |<span data-ttu-id="6888f-111">PT_UNICODE、PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="6888f-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="6888f-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="6888f-112">Area:</span></span>  <br/> |<span data-ttu-id="6888f-113">Address</span><span class="sxs-lookup"><span data-stu-id="6888f-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6888f-114">注釈</span><span class="sxs-lookup"><span data-stu-id="6888f-114">Remarks</span></span>

<span data-ttu-id="6888f-115">これらのプロパティは、すべてのメッセージング ユーザーに共通の基本アドレス プロパティの例です。</span><span class="sxs-lookup"><span data-stu-id="6888f-115">These properties are examples of the base address properties common to all messaging users.</span></span> <span data-ttu-id="6888f-116">MAPI が特定のメッセージを処理するために使用するメッセージング システムを指定します。</span><span class="sxs-lookup"><span data-stu-id="6888f-116">It specifies which messaging system MAPI uses to handle a given message.</span></span>
  
<span data-ttu-id="6888f-117">また、このプロパティは、[(PidTagEmailAddress)](pidtagemailaddress-canonical-property.md)のアドレス **文字列** のPR_EMAIL_ADRESSを決定します。</span><span class="sxs-lookup"><span data-stu-id="6888f-117">This property also determines the format of the address string in the **PR_EMAIL_ADRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)).</span></span> <span data-ttu-id="6888f-118">指定する文字列には、A ~ Z の大文字と 0 ~ 9 の数字のみを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="6888f-118">The string it provides can contain only the uppercase alphabetic characters from A through Z and the numbers from 0 through 9.</span></span>
  
<span data-ttu-id="6888f-119">文字列の有効な例は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="6888f-119">Valid examples for the string include:</span></span> 
  
```cpp
FAX
MHS
PROFS
SMTP
X400

```

## <a name="related-resources"></a><span data-ttu-id="6888f-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="6888f-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6888f-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="6888f-121">Protocol specifications</span></span>

<span data-ttu-id="6888f-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6888f-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6888f-123">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="6888f-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6888f-124">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6888f-124">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6888f-125">ユーザー、連絡先、グループ、およびリソースの一覧のプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="6888f-125">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="6888f-126">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6888f-126">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6888f-127">インターネット標準の電子メール規則からメッセージ オブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="6888f-127">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="6888f-128">[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6888f-128">[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6888f-129">ネーム サービス プロバイダー インターフェイス (NSPI) サーバーとのクライアントの通信を処理します。</span><span class="sxs-lookup"><span data-stu-id="6888f-129">Handles a client's communications with a Name Service Provider Interface (NSPI) server.</span></span>
    
<span data-ttu-id="6888f-130">[[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6888f-130">[[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6888f-131">リモート操作で使用される基本的なデータ構造を定義します。</span><span class="sxs-lookup"><span data-stu-id="6888f-131">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="6888f-132">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6888f-132">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6888f-133">クライアントとサーバー間のデータ転送の順序とフローを処理します。</span><span class="sxs-lookup"><span data-stu-id="6888f-133">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="6888f-134">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6888f-134">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6888f-135">IETF RFC2445、RFC2446、RFC2447、および予定オブジェクトと会議オブジェクトの間で変換します。</span><span class="sxs-lookup"><span data-stu-id="6888f-135">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="6888f-136">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6888f-136">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6888f-137">メッセージ オブジェクトと添付ファイル オブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="6888f-137">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="6888f-138">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6888f-138">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6888f-139">コア メッセージ ストア オブジェクトに対して許容される操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="6888f-139">Specifies permissible operations for the core message store objects.</span></span>
    
<span data-ttu-id="6888f-140">[[MS-OXOABKT]](https://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6888f-140">[[MS-OXOABKT]](https://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6888f-141">アドレス帳テンプレートで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="6888f-141">Specifies the properties and operations that are permissible for address book templates.</span></span>
    
<span data-ttu-id="6888f-142">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6888f-142">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6888f-143">電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="6888f-143">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="6888f-144">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6888f-144">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6888f-145">サーバー上の受信メール メッセージを操作します。</span><span class="sxs-lookup"><span data-stu-id="6888f-145">Manipulates incoming email messages on a server.</span></span>
    
<span data-ttu-id="6888f-146">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6888f-146">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6888f-147">検索フォルダー 一覧の構成を操作するためのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="6888f-147">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6888f-148">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="6888f-148">Header files</span></span>

<span data-ttu-id="6888f-149">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6888f-149">Mapidefs.h</span></span>
  
> <span data-ttu-id="6888f-150">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="6888f-150">Provides data type definitions.</span></span>
    
<span data-ttu-id="6888f-151">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6888f-151">Mapitags.h</span></span>
  
> <span data-ttu-id="6888f-152">関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="6888f-152">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6888f-153">関連項目</span><span class="sxs-lookup"><span data-stu-id="6888f-153">See also</span></span>



[<span data-ttu-id="6888f-154">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="6888f-154">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6888f-155">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="6888f-155">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6888f-156">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="6888f-156">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6888f-157">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="6888f-157">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
  
[<span data-ttu-id="6888f-158">MAPI アドレスの種類</span><span class="sxs-lookup"><span data-stu-id="6888f-158">MAPI Address Types</span></span>](mapi-address-types.md)

