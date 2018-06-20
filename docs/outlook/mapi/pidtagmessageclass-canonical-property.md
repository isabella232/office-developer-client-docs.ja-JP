---
title: PidTagMessageClass の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: d4e478b053bc1aa81643a60899480ac2ad9d4265
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802966"
---
# <a name="pidtagmessageclass-canonical-property"></a><span data-ttu-id="0d67e-103">PidTagMessageClass の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="0d67e-103">PidTagMessageClass Canonical Property</span></span>

  
  
<span data-ttu-id="0d67e-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0d67e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0d67e-105">IPM などのメッセージの送信者が定義されているクラスを識別する文字列が含まれています。注意してください。</span><span class="sxs-lookup"><span data-stu-id="0d67e-105">Contains a text string that identifies the sender-defined message class, such as IPM.Note.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0d67e-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="0d67e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0d67e-107">PR_MESSAGE_CLASS、PR_MESSAGE_CLASS_A、PR_MESSAGE_CLASS_W</span><span class="sxs-lookup"><span data-stu-id="0d67e-107">PR_MESSAGE_CLASS, PR_MESSAGE_CLASS_A, PR_MESSAGE_CLASS_W</span></span>  <br/> |
|<span data-ttu-id="0d67e-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="0d67e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0d67e-109">0x001A</span><span class="sxs-lookup"><span data-stu-id="0d67e-109">0x001A</span></span>  <br/> |
|<span data-ttu-id="0d67e-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="0d67e-110">Data type:</span></span>  <br/> |<span data-ttu-id="0d67e-111">PT_UNICODE、PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="0d67e-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="0d67e-112">領域:</span><span class="sxs-lookup"><span data-stu-id="0d67e-112">Area:</span></span>  <br/> |<span data-ttu-id="0d67e-113">Common</span><span class="sxs-lookup"><span data-stu-id="0d67e-113">Common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0d67e-114">備考</span><span class="sxs-lookup"><span data-stu-id="0d67e-114">Remarks</span></span>

<span data-ttu-id="0d67e-115">メッセージ クラスは、メッセージの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="0d67e-115">The message class specifies the type of the message.</span></span> <span data-ttu-id="0d67e-116">一連のメッセージは、情報メッセージの種類を表す、定義されているプロパティとメッセージを処理する方法を決定します。</span><span class="sxs-lookup"><span data-stu-id="0d67e-116">It determines the set of properties defined for the message, the kind of information the message conveys, and how to handle the message.</span></span> 
  
<span data-ttu-id="0d67e-117">これらのプロパティには、期間を含む連結された文字列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="0d67e-117">These properties contain strings concatenated with periods.</span></span> <span data-ttu-id="0d67e-118">各文字列は、サブクラス化のレベルを表します。</span><span class="sxs-lookup"><span data-stu-id="0d67e-118">Each string represents a level of subclassing.</span></span> <span data-ttu-id="0d67e-119">たとえば、IPM.メモは、IPM のサブクラスと IPM のスーパークラスです。Note.Private。</span><span class="sxs-lookup"><span data-stu-id="0d67e-119">For example, IPM.Note is a subclass of IPM and a superclass of IPM.Note.Private.</span></span> 
  
<span data-ttu-id="0d67e-120">これらのプロパティは、32 127 からの ASCII 文字で構成されている必要があり、ピリオド (ASCII 46) で終了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0d67e-120">These properties must consist of the ASCII characters 32 through 127 and must not end with a period (ASCII 46).</span></span> <span data-ttu-id="0d67e-121">並べ替えおよび比較操作を大文字の文字列として扱う必要があります。</span><span class="sxs-lookup"><span data-stu-id="0d67e-121">Sort and compare operations must treat it as a case-insensitive string.</span></span> <span data-ttu-id="0d67e-122">許容される最大長は 255 文字が、MAPI の修飾子を追加する場所を確保するためにお勧めの 128 文字で元の長さを保持すること。</span><span class="sxs-lookup"><span data-stu-id="0d67e-122">The maximum possible length is 255 characters, but in order to allow MAPI room to append qualifiers it is recommended that the original length be kept under 128 characters.</span></span> 
  
<span data-ttu-id="0d67e-123">すべてのメッセージは、これらのプロパティを再度入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0d67e-123">Every message is required to furnish these properties.</span></span> <span data-ttu-id="0d67e-124">通常、新しいメッセージを作成するクライアント アプリケーション設定[IMAPIFolder::CreateMessage](imapifolder-createmessage.md)が正常に戻るとすぐにされます。</span><span class="sxs-lookup"><span data-stu-id="0d67e-124">Normally, the client application creating a new message sets it as soon as [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) returns successfully.</span></span> <span data-ttu-id="0d67e-125">クライアントは、 [IMAPIProp::SaveChanges](imapiprop-savechanges.md)を呼び出すときに、プロパティが設定されていない場合、メッセージ ・ ストアする必要があります設定は、IPM。</span><span class="sxs-lookup"><span data-stu-id="0d67e-125">But if the property has not been set when the client calls [IMAPIProp::SaveChanges](imapiprop-savechanges.md), the message store should set it to IPM.</span></span> 
  
<span data-ttu-id="0d67e-126">MAPI によって定義された値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="0d67e-126">The values defined by MAPI are:</span></span> 
  
```cpp
IPM.Note for a standard interpersonal message 
REPORT.<subject message class>.DR for a delivery report 
REPORT.<subject message class>.NDR for a nondelivery report 
REPORT.<subject message class>.IPNRN for a read report 
REPORT.<subject message class>.IPNNRN for a nonread report 
 
```

<span data-ttu-id="0d67e-127">IPM と IPC を想定スーパークラスのみ、およびメッセージの少なくとも 1 つのサブクラス修飾子を保存または送信する前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0d67e-127">IPM and IPC are intended to be superclasses only, and a message should have at least one subclass qualifier appended before being stored or submitted.</span></span> <span data-ttu-id="0d67e-128">メッセージ クラスの使用方法の詳細については、[メッセージ クラス](mapi-message-classes.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0d67e-128">For more information on message class usage, see [Message Classes](mapi-message-classes.md).</span></span> <span data-ttu-id="0d67e-129">メッセージ クラスの必須およびオプションのプロパティのリストは、[メッセージのプロパティについて](message-properties-overview.md)のサブトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="0d67e-129">For lists of required and optional properties for message classes, see the subtopics of [About Message Properties](message-properties-overview.md).</span></span>
  
<span data-ttu-id="0d67e-130">カスタム メッセージ クラスは、メッセージ クラスだけで使用するための予約済み範囲のプロパティを定義できます。</span><span class="sxs-lookup"><span data-stu-id="0d67e-130">A custom message class can define properties in a reserved range for use with that message class only.</span></span> <span data-ttu-id="0d67e-131">詳細については、[プロパティ識別子の詳細](mapi-property-identifier-overview.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0d67e-131">For more information, see [About Property Identifiers](mapi-property-identifier-overview.md).</span></span> 
  
<span data-ttu-id="0d67e-132">フォルダー、受信メッセージを受信するメッセージ クラスのコントロールが格納されます。</span><span class="sxs-lookup"><span data-stu-id="0d67e-132">Message classes control which receive folder an incoming message is stored in.</span></span> <span data-ttu-id="0d67e-133">詳細については、 [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md)メソッドを参照してください。</span><span class="sxs-lookup"><span data-stu-id="0d67e-133">For more information, see the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) method.</span></span> 
  
<span data-ttu-id="0d67e-134">フォームおよびフォームのサーバーとメッセージ クラスの使用方法の詳細については、[メッセージ クラスを選択する](choosing-a-message-class.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0d67e-134">For more information on using message classes with forms and form servers, see [Choosing a Message Class](choosing-a-message-class.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="0d67e-135">関連リソース</span><span class="sxs-lookup"><span data-stu-id="0d67e-135">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0d67e-136">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="0d67e-136">Protocol specifications</span></span>

<span data-ttu-id="0d67e-137">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0d67e-137">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0d67e-138">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="0d67e-138">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0d67e-139">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0d67e-139">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0d67e-140">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="0d67e-140">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="0d67e-141">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0d67e-141">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0d67e-142">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="0d67e-142">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="0d67e-143">[[MS OXOUM]](http://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0d67e-143">[[MS-OXOUM]](http://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0d67e-144">プロパティとは、ボイス メールと fax メッセージを表示するための許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="0d67e-144">Specifies the properties and operations that are permissible for representing voice mail and fax messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0d67e-145">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="0d67e-145">Header files</span></span>

<span data-ttu-id="0d67e-146">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0d67e-146">Mapidefs.h</span></span>
  
> <span data-ttu-id="0d67e-147">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="0d67e-147">Provides data type definitions.</span></span>
    
<span data-ttu-id="0d67e-148">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0d67e-148">Mapitags.h</span></span>
  
> <span data-ttu-id="0d67e-149">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="0d67e-149">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0d67e-150">関連項目</span><span class="sxs-lookup"><span data-stu-id="0d67e-150">See also</span></span>



[<span data-ttu-id="0d67e-151">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="0d67e-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0d67e-152">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="0d67e-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0d67e-153">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="0d67e-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0d67e-154">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="0d67e-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

