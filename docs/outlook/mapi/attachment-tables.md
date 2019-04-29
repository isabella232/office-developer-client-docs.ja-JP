---
title: 添付ファイル テーブル
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 92a07f7b-d34c-4085-ab11-eadcd918fa1b
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 4aa800b504e7ffb07d94ace6d8dc30c1463ed637
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427444"
---
# <a name="attachment-tables"></a><span data-ttu-id="80131-103">添付ファイル テーブル</span><span class="sxs-lookup"><span data-stu-id="80131-103">Attachment tables</span></span>

<span data-ttu-id="80131-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="80131-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="80131-105">添付ファイルテーブルには、送信されたメッセージまたは複合下のメッセージに関連付けられているすべての attachment オブジェクトに関する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="80131-105">An attachment table contains information about all of the attachment objects that are associated with a submitted message or a message under composition.</span></span> 
  
<span data-ttu-id="80131-106">表には、メッセージの[imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドへの呼び出しによって保存された添付ファイルのみが含まれています。</span><span class="sxs-lookup"><span data-stu-id="80131-106">Only attachments that have been saved through a call to the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method are included in the table.</span></span> <span data-ttu-id="80131-107">添付ファイルテーブルは、メッセージストアプロバイダーによって実装され、クライアントアプリケーションとトランスポートプロバイダーによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="80131-107">Attachment tables are implemented by message store providers and used by client applications and transport providers.</span></span> 
  
<span data-ttu-id="80131-108">添付ファイルテーブルには、次のどちらかを呼び出すことによってアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="80131-108">An attachment table can be accessed by calling either of the following:</span></span>
  
- [<span data-ttu-id="80131-109">IMessage::GetAttachmentTable</span><span class="sxs-lookup"><span data-stu-id="80131-109">IMessage::GetAttachmentTable</span></span>](imessage-getattachmenttable.md)
    
- <span data-ttu-id="80131-110">[imapiprop:: openproperty](imapiprop-openproperty.md)。 **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) プロパティを要求しています。</span><span class="sxs-lookup"><span data-stu-id="80131-110">[IMAPIProp::OpenProperty](imapiprop-openproperty.md), requesting the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="80131-111">添付ファイルテーブルは動的です。</span><span class="sxs-lookup"><span data-stu-id="80131-111">Attachment tables are dynamic.</span></span>
  
<span data-ttu-id="80131-112">メッセージストアプロバイダーは、添付ファイルテーブルでの並べ替えをサポートする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="80131-112">Message store providers are not required to support sorting on their attachment tables.</span></span> <span data-ttu-id="80131-113">並べ替えがサポートされていない場合は、 **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) プロパティを使用して、表を表示する順序を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="80131-113">If sorting is not supported, the table must be presented in order by rendering position — the **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="80131-114">メッセージストアプロバイダーは、添付ファイルテーブルの制限をサポートする必要もありません。</span><span class="sxs-lookup"><span data-stu-id="80131-114">Message store providers are also not required to support restrictions on their attachment tables.</span></span> <span data-ttu-id="80131-115">制限をサポートしないプロバイダーは、 [IMAPITable:: Restrict](imapitable-restrict.md)と[IMAPITable:: FindRow](imapitable-findrow.md)の実装から MAPI_E_NO_SUPPORT を返します。</span><span class="sxs-lookup"><span data-stu-id="80131-115">Providers that do not support restrictions return MAPI_E_NO_SUPPORT from their implementations of [IMAPITable::Restrict](imapitable-restrict.md) and [IMAPITable::FindRow](imapitable-findrow.md).</span></span>
  
<span data-ttu-id="80131-116">添付ファイルテーブルは小規模にすることができます。必要な列セットには、次の4つの列のみがあります。</span><span class="sxs-lookup"><span data-stu-id="80131-116">Attachment tables can be small; there are only four columns in the required column set:</span></span>
  
- <span data-ttu-id="80131-117">**PR_ATTACH_NUM**([PidTagAttachNumber](pidtagattachnumber-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="80131-117">**PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md))</span></span> 
    
- <span data-ttu-id="80131-118">**PR_INSTANCE_KEY**([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="80131-118">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span> 
    
- <span data-ttu-id="80131-119">**PR_RECORD_KEY**([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="80131-119">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span> 
    
- <span data-ttu-id="80131-120">**PR_RENDERING_POSITION**</span><span class="sxs-lookup"><span data-stu-id="80131-120">**PR_RENDERING_POSITION**</span></span>
    
 <span data-ttu-id="80131-121">**PR_ATTACH_NUM**はノン、メッセージ内の添付ファイルを一意に識別する値を格納します。</span><span class="sxs-lookup"><span data-stu-id="80131-121">**PR_ATTACH_NUM** is nontransmittable and contains a value for uniquely identifying an attachment within a message.</span></span> <span data-ttu-id="80131-122">このプロパティは、多くの場合、テーブルの行のインデックスとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="80131-122">This property is often used as an index into the rows of the table.</span></span> <span data-ttu-id="80131-123">**PR_ATTACH_NUM**の寿命は短くなります。添付ファイルを含むメッセージが開いている場合にのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="80131-123">**PR_ATTACH_NUM** has a short lifespan; it is only valid while the message containing the attachment is open.</span></span> <span data-ttu-id="80131-124">このプロパティの値は、添付ファイルテーブルが開いている間は常に一定であることが保証されます。</span><span class="sxs-lookup"><span data-stu-id="80131-124">Its value is guaranteed to remain constant as long as the attachment table is open.</span></span> 
  
 <span data-ttu-id="80131-125">**PR_INSTANCE_KEY**は、ほぼすべてのテーブルで必要です。</span><span class="sxs-lookup"><span data-stu-id="80131-125">**PR_INSTANCE_KEY** is required in nearly every table.</span></span> <span data-ttu-id="80131-126">このメソッドは、特定の行を一意に識別するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="80131-126">It is used to uniquely identify a particular row.</span></span> 
  
 <span data-ttu-id="80131-127">**PR_RECORD_KEY**は、通常、比較目的でオブジェクトを一意に識別するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="80131-127">**PR_RECORD_KEY** is commonly used to uniquely identify an object for comparison purposes.</span></span> <span data-ttu-id="80131-128">**PR_ATTACH_NUM**とは異なり、 **PR_RECORD_KEY**には長期間のエントリ id と同じスコープがあります。メッセージが閉じられてからもう一度開かれた後でも、利用可能な状態になります。</span><span class="sxs-lookup"><span data-stu-id="80131-128">Unlike **PR_ATTACH_NUM**, **PR_RECORD_KEY** has the same scope as a long-term entry identifier; it remains available and valid even after the message is closed and reopened.</span></span> <span data-ttu-id="80131-129">mapi でのレコードキーの使用の詳細については、「 [mapi レコードおよび検索キー](mapi-record-and-search-keys.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="80131-129">For more information about the use of record keys in MAPI, see [MAPI Record and Search Keys](mapi-record-and-search-keys.md).</span></span>
  
 <span data-ttu-id="80131-130">**PR_RENDERING_POSITION**は、添付ファイルがリッチテキストメッセージでどのように表示されるかを示します。</span><span class="sxs-lookup"><span data-stu-id="80131-130">**PR_RENDERING_POSITION** indicates how an attachment should be displayed in a rich text message.</span></span> <span data-ttu-id="80131-131">**PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) プロパティに格納されているメッセージの内容の最初の文字をオフセット0、または-1 (0xffffffff) に設定して、添付ファイルをメッセージ内にレンダリングしないことを示す、文字単位のオフセットに設定できます。文字列を入力します。</span><span class="sxs-lookup"><span data-stu-id="80131-131">It can be set to an offset in characters, with the first character of the message content as stored in the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property being offset 0, or to -1 (0xFFFFFFFF), indicating that the attachment should not be rendered within the message text at all.</span></span> <span data-ttu-id="80131-132">**PR_RENDERING_POSITION**を設定しないこともオプションです。</span><span class="sxs-lookup"><span data-stu-id="80131-132">Not setting **PR_RENDERING_POSITION** is also an option.</span></span> 
  
<span data-ttu-id="80131-133">添付ファイルテーブルがレンダリング位置で並べ替えられている場合、メッセージストアプロバイダーはそれを符号付きの値 (PT_LONG) として扱います。</span><span class="sxs-lookup"><span data-stu-id="80131-133">When an attachment table is sorted by rendering position, the message store provider treats it as a signed value (PT_LONG).</span></span> <span data-ttu-id="80131-134">そのため、-1 のレンダリング位置の添付ファイルは、有効なオフセットを反映するレンダリング位置に添付される前に並べ替えられます。</span><span class="sxs-lookup"><span data-stu-id="80131-134">Therefore, attachments with rendering positions of -1 are sorted before attachments with rendering positions that reflect valid offsets.</span></span> 
  
<span data-ttu-id="80131-135">テキスト形式の添付ファイルのレンダリングの詳細については、「[添付ファイルをテキスト形式でレンダリング](rendering-an-attachment-in-plain-text.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="80131-135">For more information about rendering an attachment in a plain text message, see [Rendering an Attachment in Plain Text](rendering-an-attachment-in-plain-text.md).</span></span> 
  
<span data-ttu-id="80131-136">リッチテキスト形式 (rtf) など、書式設定されたテキストで添付ファイルをレンダリングする方法については、「[添付ファイルを rtf テキスト形式でレンダリングする](rendering-an-attachment-in-rtf-text.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="80131-136">For information about rendering an attachment in formatted text such as Rich Text Format (RTF), see [Rendering an Attachment in RTF Text](rendering-an-attachment-in-rtf-text.md).</span></span>
  
<span data-ttu-id="80131-137">一部のプロパティメッセージストアプロバイダーは、次のように簡単に計算または取得できるため、添付ファイルテーブルに含まれています。</span><span class="sxs-lookup"><span data-stu-id="80131-137">Some of the properties message store providers commonly include in an attachment table because they are easy to compute or retrieve are:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="80131-138">**PR_ATTACH_ENCODING**([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="80131-138">**PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="80131-139">**PR_ATTACH_EXTENSION**([PidTagAttachExtension](pidtagattachextension-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="80131-139">**PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="80131-140">**PR_ATTACH_FILENAME**([PidTagAttachFilename](pidtagattachfilename-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="80131-140">**PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="80131-141">**PR_ATTACH_LONG_FILENAME**([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="80131-141">**PR_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="80131-142">**PR_ATTACH_PATHNAME**([PidTagAttachPathname](pidtagattachpathname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="80131-142">**PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="80131-143">**PR_ATTACH_LONG_PATHNAME**([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="80131-143">**PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="80131-144">**PR_ATTACH_METHOD**([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="80131-144">**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="80131-145">**PR_ATTACH_TAG**([PidTagAttachTag](pidtagattachtag-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="80131-145">**PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="80131-146">**PR_CREATION_TIME**([PidTagCreationTime](pidtagcreationtime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="80131-146">**PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="80131-147">**PR_ATTACH_TRANSPORT_NAME**([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="80131-147">**PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="80131-148">**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="80131-148">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="80131-149">**PR_LAST_MODIFICATION_TIME**([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="80131-149">**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="80131-150">関連項目</span><span class="sxs-lookup"><span data-stu-id="80131-150">See also</span></span>

- [<span data-ttu-id="80131-151">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="80131-151">MAPI Tables</span></span>](mapi-tables.md)

