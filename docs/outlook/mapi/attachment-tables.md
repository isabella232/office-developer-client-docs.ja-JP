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
# <a name="attachment-tables"></a><span data-ttu-id="f53c8-103">添付ファイル テーブル</span><span class="sxs-lookup"><span data-stu-id="f53c8-103">Attachment tables</span></span>

<span data-ttu-id="f53c8-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f53c8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f53c8-105">添付ファイル テーブルには、送信済みメッセージまたは構成下のメッセージに関連付けられているすべての添付ファイル オブジェクトに関する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f53c8-105">An attachment table contains information about all of the attachment objects that are associated with a submitted message or a message under composition.</span></span> 
  
<span data-ttu-id="f53c8-106">メッセージの [IMAPIProp::SaveChanges](imapiprop-savechanges.md) メソッドへの呼び出しによって保存された添付ファイルだけがテーブルに含まれます。</span><span class="sxs-lookup"><span data-stu-id="f53c8-106">Only attachments that have been saved through a call to the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method are included in the table.</span></span> <span data-ttu-id="f53c8-107">添付ファイル テーブルは、メッセージ ストア プロバイダーによって実装され、クライアント アプリケーションとトランスポート プロバイダーによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="f53c8-107">Attachment tables are implemented by message store providers and used by client applications and transport providers.</span></span> 
  
<span data-ttu-id="f53c8-108">添付ファイル テーブルにアクセスするには、次のいずれかを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f53c8-108">An attachment table can be accessed by calling either of the following:</span></span>
  
- [<span data-ttu-id="f53c8-109">IMessage::GetAttachmentTable</span><span class="sxs-lookup"><span data-stu-id="f53c8-109">IMessage::GetAttachmentTable</span></span>](imessage-getattachmenttable.md)
    
- <span data-ttu-id="f53c8-110">[IMAPIProp::OpenProperty](imapiprop-openproperty.md)、 プロパティ **(** [PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) PR_MESSAGE_ATTACHMENTSを要求します。</span><span class="sxs-lookup"><span data-stu-id="f53c8-110">[IMAPIProp::OpenProperty](imapiprop-openproperty.md), requesting the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="f53c8-111">添付ファイル テーブルは動的です。</span><span class="sxs-lookup"><span data-stu-id="f53c8-111">Attachment tables are dynamic.</span></span>
  
<span data-ttu-id="f53c8-112">メッセージ ストア プロバイダーは、添付ファイル テーブルでの並べ替えをサポートする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="f53c8-112">Message store providers are not required to support sorting on their attachment tables.</span></span> <span data-ttu-id="f53c8-113">並べ替えがサポートされていない場合は、テーブルをレンダリング位置 (PR_RENDERING_POSITION **(** [PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) プロパティで順番に表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f53c8-113">If sorting is not supported, the table must be presented in order by rendering position — the **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="f53c8-114">メッセージ ストア プロバイダーも、添付ファイル テーブルの制限をサポートする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="f53c8-114">Message store providers are also not required to support restrictions on their attachment tables.</span></span> <span data-ttu-id="f53c8-115">制限をサポートしていないプロバイダーは [、IMAPITable::Restrict](imapitable-restrict.md) MAPI_E_NO_SUPPORT [IMAPITable::FindRow](imapitable-findrow.md)の実装から、この値を返します。</span><span class="sxs-lookup"><span data-stu-id="f53c8-115">Providers that do not support restrictions return MAPI_E_NO_SUPPORT from their implementations of [IMAPITable::Restrict](imapitable-restrict.md) and [IMAPITable::FindRow](imapitable-findrow.md).</span></span>
  
<span data-ttu-id="f53c8-116">添付ファイル テーブルは小さい場合があります。必須の列セットには 4 つの列しか含めありません。</span><span class="sxs-lookup"><span data-stu-id="f53c8-116">Attachment tables can be small; there are only four columns in the required column set:</span></span>
  
- <span data-ttu-id="f53c8-117">**PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f53c8-117">**PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md))</span></span> 
    
- <span data-ttu-id="f53c8-118">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f53c8-118">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span> 
    
- <span data-ttu-id="f53c8-119">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f53c8-119">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span> 
    
- <span data-ttu-id="f53c8-120">**PR_RENDERING_POSITION**</span><span class="sxs-lookup"><span data-stu-id="f53c8-120">**PR_RENDERING_POSITION**</span></span>
    
 <span data-ttu-id="f53c8-121">**PR_ATTACH_NUM** は非送信可能で、メッセージ内の添付ファイルを一意に識別するための値を含む。</span><span class="sxs-lookup"><span data-stu-id="f53c8-121">**PR_ATTACH_NUM** is nontransmittable and contains a value for uniquely identifying an attachment within a message.</span></span> <span data-ttu-id="f53c8-122">このプロパティは、多くの場合、テーブルの行のインデックスとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="f53c8-122">This property is often used as an index into the rows of the table.</span></span> <span data-ttu-id="f53c8-123">**PR_ATTACH_NUM** の寿命が短い。添付ファイルを含むメッセージが開いている間のみ有効です。</span><span class="sxs-lookup"><span data-stu-id="f53c8-123">**PR_ATTACH_NUM** has a short lifespan; it is only valid while the message containing the attachment is open.</span></span> <span data-ttu-id="f53c8-124">添付ファイル テーブルが開いている限り、その値は一定に保たれ保証されます。</span><span class="sxs-lookup"><span data-stu-id="f53c8-124">Its value is guaranteed to remain constant as long as the attachment table is open.</span></span> 
  
 <span data-ttu-id="f53c8-125">**PR_INSTANCE_KEY、** ほぼすべてのテーブルで必要です。</span><span class="sxs-lookup"><span data-stu-id="f53c8-125">**PR_INSTANCE_KEY** is required in nearly every table.</span></span> <span data-ttu-id="f53c8-126">特定の行を一意に識別するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="f53c8-126">It is used to uniquely identify a particular row.</span></span> 
  
 <span data-ttu-id="f53c8-127">**PR_RECORD_KEY** は、比較のためにオブジェクトを一意に識別するために一般的に使用されます。</span><span class="sxs-lookup"><span data-stu-id="f53c8-127">**PR_RECORD_KEY** is commonly used to uniquely identify an object for comparison purposes.</span></span> <span data-ttu-id="f53c8-128">PR_ATTACH_NUM **とは** 異 **PR_RECORD_KEYは、** 長期エントリ識別子と同じスコープを持つ必要があります。メッセージを閉じて再度開いた後でも、使用可能で有効なままです。</span><span class="sxs-lookup"><span data-stu-id="f53c8-128">Unlike **PR_ATTACH_NUM**, **PR_RECORD_KEY** has the same scope as a long-term entry identifier; it remains available and valid even after the message is closed and reopened.</span></span> <span data-ttu-id="f53c8-129">MAPI でのレコード キーの使用の詳細については、「MAPI レコードと [検索キー」を参照してください](mapi-record-and-search-keys.md)。</span><span class="sxs-lookup"><span data-stu-id="f53c8-129">For more information about the use of record keys in MAPI, see [MAPI Record and Search Keys](mapi-record-and-search-keys.md).</span></span>
  
 <span data-ttu-id="f53c8-130">**PR_RENDERING_POSITION** リッチ テキスト メッセージに添付ファイルを表示する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="f53c8-130">**PR_RENDERING_POSITION** indicates how an attachment should be displayed in a rich text message.</span></span> <span data-ttu-id="f53c8-131">PR_BODY ([PidTagBody](pidtagbody-canonical-property.md)) プロパティに格納されているメッセージ コンテンツの最初の文字を **オフセット 0** または -1 (0xFFFFFFFF) に設定して、メッセージ テキスト内で添付ファイルを表示しなきことを示します。</span><span class="sxs-lookup"><span data-stu-id="f53c8-131">It can be set to an offset in characters, with the first character of the message content as stored in the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property being offset 0, or to -1 (0xFFFFFFFF), indicating that the attachment should not be rendered within the message text at all.</span></span> <span data-ttu-id="f53c8-132">また **、PR_RENDERING_POSITION** 設定しない場合もオプションです。</span><span class="sxs-lookup"><span data-stu-id="f53c8-132">Not setting **PR_RENDERING_POSITION** is also an option.</span></span> 
  
<span data-ttu-id="f53c8-133">添付ファイル テーブルをレンダリング位置で並べ替えた場合、メッセージ ストア プロバイダーは署名された値 (PT_LONG) として処理します。</span><span class="sxs-lookup"><span data-stu-id="f53c8-133">When an attachment table is sorted by rendering position, the message store provider treats it as a signed value (PT_LONG).</span></span> <span data-ttu-id="f53c8-134">したがって、レンダリング位置が -1 の添付ファイルは、有効なオフセットを反映するレンダリング位置を持つ添付ファイルの前に並べ替えされます。</span><span class="sxs-lookup"><span data-stu-id="f53c8-134">Therefore, attachments with rendering positions of -1 are sorted before attachments with rendering positions that reflect valid offsets.</span></span> 
  
<span data-ttu-id="f53c8-135">プレーン テキスト メッセージで添付ファイルをレンダリングする方法の詳細については、「プレーン テキストで [添付ファイルをレンダリングする」を参照してください](rendering-an-attachment-in-plain-text.md)。</span><span class="sxs-lookup"><span data-stu-id="f53c8-135">For more information about rendering an attachment in a plain text message, see [Rendering an Attachment in Plain Text](rendering-an-attachment-in-plain-text.md).</span></span> 
  
<span data-ttu-id="f53c8-136">リッチ テキスト形式 (RTF) などの書式設定されたテキストで添付ファイルをレンダリングする方法については、「RTF テキストで添付ファイルをレンダリングする」 [を参照してください](rendering-an-attachment-in-rtf-text.md)。</span><span class="sxs-lookup"><span data-stu-id="f53c8-136">For information about rendering an attachment in formatted text such as Rich Text Format (RTF), see [Rendering an Attachment in RTF Text](rendering-an-attachment-in-rtf-text.md).</span></span>
  
<span data-ttu-id="f53c8-137">メッセージ ストア プロバイダーの一般的なプロパティの中には、計算や取得が容易なので、添付ファイル テーブルに含まれるものがあります。</span><span class="sxs-lookup"><span data-stu-id="f53c8-137">Some of the properties message store providers commonly include in an attachment table because they are easy to compute or retrieve are:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f53c8-138">**PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f53c8-138">**PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f53c8-139">**PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f53c8-139">**PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="f53c8-140">**PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f53c8-140">**PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f53c8-141">**PR_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f53c8-141">**PR_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="f53c8-142">**PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f53c8-142">**PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f53c8-143">**PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f53c8-143">**PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="f53c8-144">**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f53c8-144">**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f53c8-145">**PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f53c8-145">**PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="f53c8-146">**PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f53c8-146">**PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f53c8-147">**PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f53c8-147">**PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="f53c8-148">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f53c8-148">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f53c8-149">**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f53c8-149">**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f53c8-150">関連項目</span><span class="sxs-lookup"><span data-stu-id="f53c8-150">See also</span></span>

- [<span data-ttu-id="f53c8-151">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="f53c8-151">MAPI Tables</span></span>](mapi-tables.md)

