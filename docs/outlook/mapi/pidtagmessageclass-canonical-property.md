---
title: PidTagMessageClass 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageClass
api_type:
- HeaderDef
ms.assetid: 1e704023-1992-4b43-857e-0a7da7bc8e87
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7912a3831333ff8a464a12e567430eb5a3272172
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359265"
---
# <a name="pidtagmessageclass-canonical-property"></a><span data-ttu-id="4ec0d-103">PidTagMessageClass 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="4ec0d-103">PidTagMessageClass Canonical Property</span></span>

  
  
<span data-ttu-id="4ec0d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4ec0d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4ec0d-105">IPM.Note など、送信者が定義したメッセージ クラスを識別するテキスト文字列が含まれます。</span><span class="sxs-lookup"><span data-stu-id="4ec0d-105">Contains a text string that identifies the sender-defined message class, such as IPM.Note.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4ec0d-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="4ec0d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4ec0d-107">PR_MESSAGE_CLASS、PR_MESSAGE_CLASS_A、PR_MESSAGE_CLASS_W</span><span class="sxs-lookup"><span data-stu-id="4ec0d-107">PR_MESSAGE_CLASS, PR_MESSAGE_CLASS_A, PR_MESSAGE_CLASS_W</span></span>  <br/> |
|<span data-ttu-id="4ec0d-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="4ec0d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4ec0d-109">0x001A</span><span class="sxs-lookup"><span data-stu-id="4ec0d-109">0x001A</span></span>  <br/> |
|<span data-ttu-id="4ec0d-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="4ec0d-110">Data type:</span></span>  <br/> |<span data-ttu-id="4ec0d-111">PT_UNICODE、PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="4ec0d-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="4ec0d-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="4ec0d-112">Area:</span></span>  <br/> |<span data-ttu-id="4ec0d-113">共通</span><span class="sxs-lookup"><span data-stu-id="4ec0d-113">Common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4ec0d-114">注釈</span><span class="sxs-lookup"><span data-stu-id="4ec0d-114">Remarks</span></span>

<span data-ttu-id="4ec0d-115">メッセージ クラスは、メッセージの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="4ec0d-115">The message class specifies the type of the message.</span></span> <span data-ttu-id="4ec0d-116">メッセージに対して定義されたプロパティのセット、メッセージが伝える情報の種類、およびメッセージの処理方法を決定します。</span><span class="sxs-lookup"><span data-stu-id="4ec0d-116">It determines the set of properties defined for the message, the kind of information the message conveys, and how to handle the message.</span></span> 
  
<span data-ttu-id="4ec0d-117">これらのプロパティには、ピリオドと連結された文字列が含まれます。</span><span class="sxs-lookup"><span data-stu-id="4ec0d-117">These properties contain strings concatenated with periods.</span></span> <span data-ttu-id="4ec0d-118">各文字列は、サブクラス化のレベルを表します。</span><span class="sxs-lookup"><span data-stu-id="4ec0d-118">Each string represents a level of subclassing.</span></span> <span data-ttu-id="4ec0d-119">たとえば、IPM です。メモは IPM のサブクラスであり、IPM のスーパークラスです。Note.Private。</span><span class="sxs-lookup"><span data-stu-id="4ec0d-119">For example, IPM.Note is a subclass of IPM and a superclass of IPM.Note.Private.</span></span> 
  
<span data-ttu-id="4ec0d-120">これらのプロパティは、ASCII 文字 32 ~ 127 で構成する必要があります。ピリオド (ASCII 46) で終わることはできません。</span><span class="sxs-lookup"><span data-stu-id="4ec0d-120">These properties must consist of the ASCII characters 32 through 127 and must not end with a period (ASCII 46).</span></span> <span data-ttu-id="4ec0d-121">並べ替えと比較の操作では、大文字と小文字を区別しない文字列として扱う必要があります。</span><span class="sxs-lookup"><span data-stu-id="4ec0d-121">Sort and compare operations must treat it as a case-insensitive string.</span></span> <span data-ttu-id="4ec0d-122">指定できる最大長は 255 文字ですが、MAPI ルームで修飾子を追加するには、元の長さを 128 文字以内に保つ必要があります。</span><span class="sxs-lookup"><span data-stu-id="4ec0d-122">The maximum possible length is 255 characters, but in order to allow MAPI room to append qualifiers it is recommended that the original length be kept under 128 characters.</span></span> 
  
<span data-ttu-id="4ec0d-123">これらのプロパティを指定するには、すべてのメッセージが必要です。</span><span class="sxs-lookup"><span data-stu-id="4ec0d-123">Every message is required to furnish these properties.</span></span> <span data-ttu-id="4ec0d-124">通常、新しいメッセージを作成するクライアント アプリケーションは [、IMAPIFolder::CreateMessage](imapifolder-createmessage.md) が正常に返されるとすぐに設定します。</span><span class="sxs-lookup"><span data-stu-id="4ec0d-124">Normally, the client application creating a new message sets it as soon as [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) returns successfully.</span></span> <span data-ttu-id="4ec0d-125">ただし、クライアントが [IMAPIProp::SaveChanges](imapiprop-savechanges.md)を呼び出す際にプロパティが設定されていない場合は、メッセージ ストアで IPM に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4ec0d-125">But if the property has not been set when the client calls [IMAPIProp::SaveChanges](imapiprop-savechanges.md), the message store should set it to IPM.</span></span> 
  
<span data-ttu-id="4ec0d-126">MAPI によって定義される値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="4ec0d-126">The values defined by MAPI are:</span></span> 
  
```cpp
IPM.Note for a standard interpersonal message 
REPORT.<subject message class>.DR for a delivery report 
REPORT.<subject message class>.NDR for a nondelivery report 
REPORT.<subject message class>.IPNRN for a read report 
REPORT.<subject message class>.IPNNRN for a nonread report 
 
```

<span data-ttu-id="4ec0d-127">IPM と IPC はスーパークラスのみを対象とします。メッセージには、保存または送信の前に少なくとも 1 つのサブクラス修飾子が追加されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="4ec0d-127">IPM and IPC are intended to be superclasses only, and a message should have at least one subclass qualifier appended before being stored or submitted.</span></span> <span data-ttu-id="4ec0d-128">メッセージ クラスの使用方法の詳細については、「Message [Classes」を参照してください](mapi-message-classes.md)。</span><span class="sxs-lookup"><span data-stu-id="4ec0d-128">For more information on message class usage, see [Message Classes](mapi-message-classes.md).</span></span> <span data-ttu-id="4ec0d-129">メッセージ クラスの必須プロパティとオプション プロパティの一覧については、「メッセージプロパティについて」のサブ [トピックを参照してください](message-properties-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="4ec0d-129">For lists of required and optional properties for message classes, see the subtopics of [About Message Properties](message-properties-overview.md).</span></span>
  
<span data-ttu-id="4ec0d-130">カスタム メッセージ クラスは、そのメッセージ クラスでのみ使用するために予約範囲のプロパティを定義できます。</span><span class="sxs-lookup"><span data-stu-id="4ec0d-130">A custom message class can define properties in a reserved range for use with that message class only.</span></span> <span data-ttu-id="4ec0d-131">詳細については、「プロパティ識別子 [について」を参照してください](mapi-property-identifier-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="4ec0d-131">For more information, see [About Property Identifiers](mapi-property-identifier-overview.md).</span></span> 
  
<span data-ttu-id="4ec0d-132">メッセージ クラスは、受信メッセージが格納されている受信フォルダーを制御します。</span><span class="sxs-lookup"><span data-stu-id="4ec0d-132">Message classes control which receive folder an incoming message is stored in.</span></span> <span data-ttu-id="4ec0d-133">詳細については [、「IMsgStore::GetReceiveFolderTable メソッド」を参照](imsgstore-getreceivefoldertable.md) してください。</span><span class="sxs-lookup"><span data-stu-id="4ec0d-133">For more information, see the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) method.</span></span> 
  
<span data-ttu-id="4ec0d-134">フォームおよびフォーム サーバーでメッセージ クラスを使用する方法の詳細については、「メッセージ クラスの選択 [」を参照してください](choosing-a-message-class.md)。</span><span class="sxs-lookup"><span data-stu-id="4ec0d-134">For more information on using message classes with forms and form servers, see [Choosing a Message Class](choosing-a-message-class.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="4ec0d-135">関連リソース</span><span class="sxs-lookup"><span data-stu-id="4ec0d-135">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4ec0d-136">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="4ec0d-136">Protocol specifications</span></span>

<span data-ttu-id="4ec0d-137">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4ec0d-137">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4ec0d-138">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="4ec0d-138">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4ec0d-139">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4ec0d-139">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4ec0d-140">メッセージ オブジェクトと添付ファイル オブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="4ec0d-140">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="4ec0d-141">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4ec0d-141">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4ec0d-142">電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="4ec0d-142">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="4ec0d-143">[[MS-OXOUM]](https://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4ec0d-143">[[MS-OXOUM]](https://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4ec0d-144">ボイス メールおよび FAX メッセージを表す場合に許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="4ec0d-144">Specifies the properties and operations that are permissible for representing voice mail and fax messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4ec0d-145">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="4ec0d-145">Header files</span></span>

<span data-ttu-id="4ec0d-146">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4ec0d-146">Mapidefs.h</span></span>
  
> <span data-ttu-id="4ec0d-147">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="4ec0d-147">Provides data type definitions.</span></span>
    
<span data-ttu-id="4ec0d-148">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4ec0d-148">Mapitags.h</span></span>
  
> <span data-ttu-id="4ec0d-149">関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="4ec0d-149">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4ec0d-150">関連項目</span><span class="sxs-lookup"><span data-stu-id="4ec0d-150">See also</span></span>



[<span data-ttu-id="4ec0d-151">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="4ec0d-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4ec0d-152">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="4ec0d-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4ec0d-153">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="4ec0d-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4ec0d-154">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="4ec0d-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

