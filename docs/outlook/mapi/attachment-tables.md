---
title: 添付ファイル テーブル
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 92a07f7b-d34c-4085-ab11-eadcd918fa1b
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 2fd79cfe18e7d39f26563c87b8fb15553bf32ddf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799701"
---
# <a name="attachment-tables"></a><span data-ttu-id="78183-103">添付ファイル テーブル</span><span class="sxs-lookup"><span data-stu-id="78183-103">Attachment tables</span></span>

<span data-ttu-id="78183-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="78183-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="78183-105">添付ファイル テーブルには、すべての送信されたメッセージや、メッセージは、コンポジションに関連付けられている添付ファイルのオブジェクトに関する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="78183-105">An attachment table contains information about all of the attachment objects that are associated with a submitted message or a message under composition.</span></span> 
  
<span data-ttu-id="78183-106">テーブルには、メッセージの[IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドを呼び出すことによって保存されている添付ファイルだけが含まれます。</span><span class="sxs-lookup"><span data-stu-id="78183-106">Only attachments that have been saved through a call to the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method are included in the table.</span></span> <span data-ttu-id="78183-107">添付ファイル テーブルはメッセージ ストア プロバイダーによって実装され、クライアント アプリケーションおよびトランスポート プロバイダーによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="78183-107">Attachment tables are implemented by message store providers and used by client applications and transport providers.</span></span> 
  
<span data-ttu-id="78183-108">次のいずれかを呼び出すことによって、添付ファイル テーブルにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="78183-108">An attachment table can be accessed by calling either of the following:</span></span>
  
- [<span data-ttu-id="78183-109">IMessage::GetAttachmentTable</span><span class="sxs-lookup"><span data-stu-id="78183-109">IMessage::GetAttachmentTable</span></span>](imessage-getattachmenttable.md)
    
- <span data-ttu-id="78183-110">[IMAPIProp::OpenProperty](imapiprop-openproperty.md)、 **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) のプロパティを要求します。</span><span class="sxs-lookup"><span data-stu-id="78183-110">[IMAPIProp::OpenProperty](imapiprop-openproperty.md), requesting the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="78183-111">添付ファイル テーブルでは、動的です。</span><span class="sxs-lookup"><span data-stu-id="78183-111">Attachment tables are dynamic.</span></span>
  
<span data-ttu-id="78183-112">メッセージ ストア プロバイダーは、その添付ファイル テーブルの並べ替えをサポートする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="78183-112">Message store providers are not required to support sorting on their attachment tables.</span></span> <span data-ttu-id="78183-113">描画位置の順序でテーブルを表示する必要があります並べ替えがサポートされていない場合、 **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) のプロパティです。</span><span class="sxs-lookup"><span data-stu-id="78183-113">If sorting is not supported, the table must be presented in order by rendering position — the **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="78183-114">メッセージ ストア プロバイダーも、添付ファイル テーブルの制限をサポートするために必要ありません。</span><span class="sxs-lookup"><span data-stu-id="78183-114">Message store providers are also not required to support restrictions on their attachment tables.</span></span> <span data-ttu-id="78183-115">制限をサポートしていないプロバイダーでは、 [IMAPITable::Restrict](imapitable-restrict.md)と[IMAPITable::FindRow](imapitable-findrow.md)の実装から MAPI_E_NO_SUPPORT を返します。</span><span class="sxs-lookup"><span data-stu-id="78183-115">Providers that do not support restrictions return MAPI_E_NO_SUPPORT from their implementations of [IMAPITable::Restrict](imapitable-restrict.md) and [IMAPITable::FindRow](imapitable-findrow.md).</span></span>
  
<span data-ttu-id="78183-116">添付ファイル テーブル小さいこともあります。必要な列のセットでは、のみ 4 つの列があります。</span><span class="sxs-lookup"><span data-stu-id="78183-116">Attachment tables can be small; there are only four columns in the required column set:</span></span>
  
- <span data-ttu-id="78183-117">**PR_ATTACH_NUM**([PidTagAttachNumber](pidtagattachnumber-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="78183-117">**PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md))</span></span> 
    
- <span data-ttu-id="78183-118">**PR_INSTANCE_KEY**([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="78183-118">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span> 
    
- <span data-ttu-id="78183-119">**PR_RECORD_KEY**([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="78183-119">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span> 
    
- <span data-ttu-id="78183-120">**PR_RENDERING_POSITION**</span><span class="sxs-lookup"><span data-stu-id="78183-120">**PR_RENDERING_POSITION**</span></span>
    
 <span data-ttu-id="78183-121">**PR_ATTACH_NUM**は nontransmittable であるため、メッセージ内の添付ファイルを一意に識別する値を含んでいます。</span><span class="sxs-lookup"><span data-stu-id="78183-121">**PR_ATTACH_NUM** is nontransmittable and contains a value for uniquely identifying an attachment within a message.</span></span> <span data-ttu-id="78183-122">このプロパティは、テーブルの行に、インデックスとしてよく使用されます。</span><span class="sxs-lookup"><span data-stu-id="78183-122">This property is often used as an index into the rows of the table.</span></span> <span data-ttu-id="78183-123">**PR_ATTACH_NUM**には、短い寿命です。添付ファイルを含むメッセージを開いている間のみ有効です。</span><span class="sxs-lookup"><span data-stu-id="78183-123">**PR_ATTACH_NUM** has a short lifespan; it is only valid while the message containing the attachment is open.</span></span> <span data-ttu-id="78183-124">添付ファイル テーブルが開いている限り一定に保つには、その値が保証されます。</span><span class="sxs-lookup"><span data-stu-id="78183-124">Its value is guaranteed to remain constant as long as the attachment table is open.</span></span> 
  
 <span data-ttu-id="78183-125">ほぼすべてのテーブルでは、 **PR_INSTANCE_KEY**が必要です。</span><span class="sxs-lookup"><span data-stu-id="78183-125">**PR_INSTANCE_KEY** is required in nearly every table.</span></span> <span data-ttu-id="78183-126">特定の行を一意に識別に使用されます。</span><span class="sxs-lookup"><span data-stu-id="78183-126">It is used to uniquely identify a particular row.</span></span> 
  
 <span data-ttu-id="78183-127">**PR_RECORD_KEY**は、比較のためのオブジェクトを一意に識別する通常使用されます。</span><span class="sxs-lookup"><span data-stu-id="78183-127">**PR_RECORD_KEY** is commonly used to uniquely identify an object for comparison purposes.</span></span> <span data-ttu-id="78183-128">**PR_RECORD_KEY**は**PR_ATTACH_NUM**とは異なり、長期的なエントリ id と同じスコープを持つメッセージが閉じられ、再オープン後も使用可能で有効なを維持します。</span><span class="sxs-lookup"><span data-stu-id="78183-128">Unlike **PR_ATTACH_NUM**, **PR_RECORD_KEY** has the same scope as a long-term entry identifier; it remains available and valid even after the message is closed and reopened.</span></span> <span data-ttu-id="78183-129">MAPI でのレコードのキーの使用に関する詳細については、 [MAPI の記録と検索キー](mapi-record-and-search-keys.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="78183-129">For more information about the use of record keys in MAPI, see [MAPI Record and Search Keys](mapi-record-and-search-keys.md).</span></span>
  
 <span data-ttu-id="78183-130">**PR_RENDERING_POSITION**では、リッチ テキスト メッセージに添付ファイルを表示する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="78183-130">**PR_RENDERING_POSITION** indicates how an attachment should be displayed in a rich text message.</span></span> <span data-ttu-id="78183-131">または-1 (0 xffffffff)、メッセージ内で添付ファイルを表示されないことを示す 0 が相殺される ([PidTagBody](pidtagbody-canonical-property.md)) である**PR_BODY**プロパティに格納されているメッセージの内容の最初の文字で、文字単位のオフセットを設定することができます。すべてのテキストです。</span><span class="sxs-lookup"><span data-stu-id="78183-131">It can be set to an offset in characters, with the first character of the message content as stored in the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property being offset 0, or to -1 (0xFFFFFFFF), indicating that the attachment should not be rendered within the message text at all.</span></span> <span data-ttu-id="78183-132">**PR_RENDERING_POSITION**を設定しないとは、また、オプションです。</span><span class="sxs-lookup"><span data-stu-id="78183-132">Not setting **PR_RENDERING_POSITION** is also an option.</span></span> 
  
<span data-ttu-id="78183-133">描画位置を指定して、添付ファイル テーブルが並べ替えられて、メッセージ ストア プロバイダーは符号付きの値 (PT_LONG) として扱います。</span><span class="sxs-lookup"><span data-stu-id="78183-133">When an attachment table is sorted by rendering position, the message store provider treats it as a signed value (PT_LONG).</span></span> <span data-ttu-id="78183-134">したがって、-1 のレンダリング位置を持つ添付ファイルは、有効なオフセットを反映するためのレンダリング位置を持つ添付ファイルの前に並べ替えられます。</span><span class="sxs-lookup"><span data-stu-id="78183-134">Therefore, attachments with rendering positions of -1 are sorted before attachments with rendering positions that reflect valid offsets.</span></span> 
  
<span data-ttu-id="78183-135">テキスト形式のメッセージの添付ファイルのレンダリングの詳細については、[テキスト形式の添付ファイルのレンダリング](rendering-an-attachment-in-plain-text.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="78183-135">For more information about rendering an attachment in a plain text message, see [Rendering an Attachment in Plain Text](rendering-an-attachment-in-plain-text.md).</span></span> 
  
<span data-ttu-id="78183-136">添付ファイルをリッチ テキスト形式 (RTF) などの書式設定されたテキストのレンダリング方法の詳細については、 [rtf 形式のテキストの添付ファイルのレンダリング](rendering-an-attachment-in-rtf-text.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="78183-136">For information about rendering an attachment in formatted text such as Rich Text Format (RTF), see [Rendering an Attachment in RTF Text](rendering-an-attachment-in-rtf-text.md).</span></span>
  
<span data-ttu-id="78183-137">メッセージ ストア プロバイダーよくは、添付ファイル テーブルでは簡単に計算または取得するためのプロパティは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="78183-137">Some of the properties message store providers commonly include in an attachment table because they are easy to compute or retrieve are:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="78183-138">**PR_ATTACH_ENCODING**([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="78183-138">**PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="78183-139">**PR_ATTACH_EXTENSION**([PidTagAttachExtension](pidtagattachextension-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="78183-139">**PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="78183-140">**PR_ATTACH_FILENAME**([PidTagAttachFilename](pidtagattachfilename-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="78183-140">**PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="78183-141">**PR_ATTACH_LONG_FILENAME**([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="78183-141">**PR_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="78183-142">**PR_ATTACH_PATHNAME**([PidTagAttachPathname](pidtagattachpathname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="78183-142">**PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="78183-143">**PR_ATTACH_LONG_PATHNAME**([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="78183-143">**PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="78183-144">**PR_ATTACH_METHOD**([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="78183-144">**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="78183-145">**PR_ATTACH_TAG**([PidTagAttachTag](pidtagattachtag-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="78183-145">**PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="78183-146">**PR_CREATION_TIME**([PidTagCreationTime](pidtagcreationtime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="78183-146">**PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="78183-147">**PR_ATTACH_TRANSPORT_NAME**([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="78183-147">**PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="78183-148">**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="78183-148">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="78183-149">**PR_LAST_MODIFICATION_TIME**([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="78183-149">**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="78183-150">関連項目</span><span class="sxs-lookup"><span data-stu-id="78183-150">See also</span></span>

- [<span data-ttu-id="78183-151">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="78183-151">MAPI Tables</span></span>](mapi-tables.md)

