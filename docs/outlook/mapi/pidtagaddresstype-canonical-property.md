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
ms.openlocfilehash: 6051d3403cede21fa4aebdb6ca561dd3efb46771
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360087"
---
# <a name="pidtagaddresstype-canonical-property"></a><span data-ttu-id="d026e-103">PidTagAddressType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d026e-103">PidTagAddressType Canonical Property</span></span>

<span data-ttu-id="d026e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d026e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d026e-105">メッセージングユーザーの電子メールアドレスの種類 (SMTP など) を格納します。</span><span class="sxs-lookup"><span data-stu-id="d026e-105">Contains the messaging user's email address type, such as SMTP.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d026e-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="d026e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d026e-107">PR_ADDRTYPE、PR_ADDRTYPE_A、PR_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="d026e-107">PR_ADDRTYPE, PR_ADDRTYPE_A, PR_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="d026e-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="d026e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d026e-109">0x3002</span><span class="sxs-lookup"><span data-stu-id="d026e-109">0x3002</span></span>  <br/> |
|<span data-ttu-id="d026e-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="d026e-110">Data type:</span></span>  <br/> |<span data-ttu-id="d026e-111">PT_UNICODE、PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="d026e-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="d026e-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="d026e-112">Area:</span></span>  <br/> |<span data-ttu-id="d026e-113">Address</span><span class="sxs-lookup"><span data-stu-id="d026e-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d026e-114">解説</span><span class="sxs-lookup"><span data-stu-id="d026e-114">Remarks</span></span>

<span data-ttu-id="d026e-115">これらのプロパティは、すべてのメッセージングユーザーに共通のベースアドレスプロパティの例です。</span><span class="sxs-lookup"><span data-stu-id="d026e-115">These properties are examples of the base address properties common to all messaging users.</span></span> <span data-ttu-id="d026e-116">このメソッドは、MAPI が特定のメッセージを処理するために使用するメッセージングシステムを指定します。</span><span class="sxs-lookup"><span data-stu-id="d026e-116">It specifies which messaging system MAPI uses to handle a given message.</span></span>
  
<span data-ttu-id="d026e-117">このプロパティは、 **PR_EMAIL_ADRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) のアドレス文字列の書式も決定します。</span><span class="sxs-lookup"><span data-stu-id="d026e-117">This property also determines the format of the address string in the **PR_EMAIL_ADRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)).</span></span> <span data-ttu-id="d026e-118">この文字列には、a ~ Z の大文字と数字と 0 ~ 9 の数字のみを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="d026e-118">The string it provides can contain only the uppercase alphabetic characters from A through Z and the numbers from 0 through 9.</span></span>
  
<span data-ttu-id="d026e-119">文字列の有効な例は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="d026e-119">Valid examples for the string include:</span></span> 
  
```cpp
FAX
MHS
PROFS
SMTP
X400

```

## <a name="related-resources"></a><span data-ttu-id="d026e-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="d026e-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d026e-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="d026e-121">Protocol specifications</span></span>

<span data-ttu-id="d026e-122">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d026e-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d026e-123">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="d026e-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d026e-124">[[OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d026e-124">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d026e-125">ユーザー、連絡先、グループ、およびリソースのリストのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="d026e-125">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="d026e-126">[[OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d026e-126">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d026e-127">インターネット標準の電子メールの規則からメッセージオブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="d026e-127">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="d026e-128">[[MS-CHAP]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d026e-128">[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d026e-129">ネームサービスプロバイダインターフェイス (NSPI) サーバーとのクライアントの通信を処理します。</span><span class="sxs-lookup"><span data-stu-id="d026e-129">Handles a client's communications with a Name Service Provider Interface (NSPI) server.</span></span>
    
<span data-ttu-id="d026e-130">[[OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d026e-130">[[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d026e-131">リモート操作で使用される基本データ構造を定義します。</span><span class="sxs-lookup"><span data-stu-id="d026e-131">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="d026e-132">[[OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d026e-132">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d026e-133">クライアントとサーバー間のデータ転送の順序と流れを処理します。</span><span class="sxs-lookup"><span data-stu-id="d026e-133">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="d026e-134">[[OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d026e-134">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d026e-135">IETF RFC2445、RFC2446、RFC2447、予定および会議の各オブジェクトを変換します。</span><span class="sxs-lookup"><span data-stu-id="d026e-135">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="d026e-136">[[OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d026e-136">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d026e-137">メッセージと添付ファイルオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="d026e-137">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="d026e-138">[[OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d026e-138">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d026e-139">コアメッセージストアオブジェクトに対する許容される操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="d026e-139">Specifies permissible operations for the core message store objects.</span></span>
    
<span data-ttu-id="d026e-140">[[OXOABKT]](https://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d026e-140">[[MS-OXOABKT]](https://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d026e-141">アドレス帳テンプレートで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="d026e-141">Specifies the properties and operations that are permissible for address book templates.</span></span>
    
<span data-ttu-id="d026e-142">[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d026e-142">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d026e-143">電子メールメッセージオブジェクトに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="d026e-143">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="d026e-144">[[OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d026e-144">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d026e-145">サーバー上の受信電子メールメッセージを操作します。</span><span class="sxs-lookup"><span data-stu-id="d026e-145">Manipulates incoming email messages on a server.</span></span>
    
<span data-ttu-id="d026e-146">[[OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d026e-146">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d026e-147">検索フォルダーリストの構成を操作するためのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="d026e-147">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d026e-148">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="d026e-148">Header files</span></span>

<span data-ttu-id="d026e-149">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d026e-149">Mapidefs.h</span></span>
  
> <span data-ttu-id="d026e-150">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="d026e-150">Provides data type definitions.</span></span>
    
<span data-ttu-id="d026e-151">Mapitags</span><span class="sxs-lookup"><span data-stu-id="d026e-151">Mapitags.h</span></span>
  
> <span data-ttu-id="d026e-152">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="d026e-152">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d026e-153">関連項目</span><span class="sxs-lookup"><span data-stu-id="d026e-153">See also</span></span>



[<span data-ttu-id="d026e-154">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="d026e-154">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d026e-155">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d026e-155">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d026e-156">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="d026e-156">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d026e-157">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="d026e-157">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
  
[<span data-ttu-id="d026e-158">MAPI アドレスの種類</span><span class="sxs-lookup"><span data-stu-id="d026e-158">MAPI Address Types</span></span>](mapi-address-types.md)

