---
title: 添付ファイルとメッセージ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b2f2fb72-23ae-4e0b-a8a1-3b78a1862acb
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: d5b37ea2e254e05ada3214309f58147e92f46393
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566832"
---
# <a name="attached-files-and-messages"></a><span data-ttu-id="a62b0-103">添付ファイルとメッセージ</span><span class="sxs-lookup"><span data-stu-id="a62b0-103">Attached Files and Messages</span></span>

  
  
<span data-ttu-id="a62b0-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a62b0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a62b0-105">メッセージの内容をエンコード中に TNEF で MIME を使用すると、すべての添付ファイルのプロパティとコンテンツが TNEF ストリームでは。</span><span class="sxs-lookup"><span data-stu-id="a62b0-105">If MIME with TNEF is used while encoding message content,all attachment properties and content are in the TNEF stream.</span></span> <span data-ttu-id="a62b0-106">自体 TNEF は、TNEF なしの MIME のエンコード、Winmail.dat という名前の 1 つ、バイナリ添付ファイルです。</span><span class="sxs-lookup"><span data-stu-id="a62b0-106">The TNEF itself is a single, binary attached file named Winmail.dat, encoded as described for MIME without TNEF.</span></span> 
  
<span data-ttu-id="a62b0-107">TNEF に MIME を使用する場合、添付ファイルは、MIME メッセージのコンテンツの一部として送信されます。</span><span class="sxs-lookup"><span data-stu-id="a62b0-107">If MIME is used without TNEF, attached files are sent as MIME message content parts.</span></span> <span data-ttu-id="a62b0-108">ファイル名は、添付ファイルの*コンテンツ タイプ*ヘッダーに*name*パラメーターに配置されます。</span><span class="sxs-lookup"><span data-stu-id="a62b0-108">The filename is placed in the  *name*  parameter to the  *Content-type*  header for the attachment.</span></span> <span data-ttu-id="a62b0-109">添付ファイルの文字セットは、*コンテンツ タイプ*に*文字セット*パラメーターに配置します。コンテンツ転送エンコードは、全体の添付ファイルのコンテンツをスキャンすることによって決定されます。</span><span class="sxs-lookup"><span data-stu-id="a62b0-109">The character set for the attachment is placed in the  *charset*  parameter to the  *Content-type*  ; it and the content-transfer-encoding are determined by scanning the entire attachment content.</span></span> <span data-ttu-id="a62b0-110">URL の添付ファイルは、特別に処理されます。</span><span class="sxs-lookup"><span data-stu-id="a62b0-110">URL attachments are treated specially:</span></span> 
  
- <span data-ttu-id="a62b0-111">場合は、添付ファイルは、URL (拡張子を持つ添付ファイルです。)、URL 内に定義されているアクセス ・ モードは、匿名 FTP と、外部メッセージとしてエンコードされ、ファイル (URL) の内容は、外部のメッセージのヘッダーにコピーされます。</span><span class="sxs-lookup"><span data-stu-id="a62b0-111">If the attachment is a URL (an attached file with extension .URL), and the access mode defined in it is anonymous FTP, it is encoded as an external message, and the content of the file (the URL) is copied into the header of the external message.</span></span> <span data-ttu-id="a62b0-112">*コンテンツの種類: メッセージ/外部ボディ; アクセスの種類 = つけ加え* (コンテンツ転送エンコード: 7 ビットであると見なされます)。</span><span class="sxs-lookup"><span data-stu-id="a62b0-112">*Content-type: message/external-body; access-type=anon-ftp*  (Content-Transfer-Encoding: 7bit is assumed.)</span></span> 
    
- <span data-ttu-id="a62b0-113">7 ビットの文字が見つかるし、行を超えると 140 文字の長さでない、だけの場合、添付ファイルは、ASCII テキストです。</span><span class="sxs-lookup"><span data-stu-id="a62b0-113">If only 7-bit characters are found and no line exceeds 140 characters in length, the attachment is ASCII text.</span></span> <span data-ttu-id="a62b0-114">*コンテンツの種類: テキスト/形式です。文字セット、us-ascii コンテンツ転送エンコードを =: 7 ビット*</span><span class="sxs-lookup"><span data-stu-id="a62b0-114">*Content-type: text/plain; charset=us-ascii Content-Transfer-Encoding: 7bit*</span></span> 
    
- <span data-ttu-id="a62b0-115">場合か、長い行を 25% に 8 ビットの文字が見つかると、添付ファイルのコンテンツがテキストで、文字セットは、ロケールによって決まります。</span><span class="sxs-lookup"><span data-stu-id="a62b0-115">If long lines or up to 25% 8-bit characters are found, the attachment content is text and the character set is determined by the locale.</span></span> <span data-ttu-id="a62b0-116">ISO 8859 の標準で定義されている文字セットから選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a62b0-116">It should be chosen from the character sets defined by ISO standard 8859.</span></span> <span data-ttu-id="a62b0-117">*コンテンツの種類: テキスト/形式; charset = ISO 8859-1* (例)</span><span class="sxs-lookup"><span data-stu-id="a62b0-117">*Content-type: text/plain; charset=ISO-8859-1*  (for example)</span></span> 
    
     <span data-ttu-id="a62b0-118">*Content-Transfer-Encoding: quoted-printable*</span><span class="sxs-lookup"><span data-stu-id="a62b0-118">*Content-Transfer-Encoding: quoted-printable*</span></span> 
    
- <span data-ttu-id="a62b0-119">25% 以上の文字には、上位ビットが設定がある場合、添付ファイルはバイナリです。</span><span class="sxs-lookup"><span data-stu-id="a62b0-119">If 25% or more of the characters have the high bit set, the attachment is binary.</span></span> <span data-ttu-id="a62b0-120">Base64 アルゴリズムを使用してエンコードされます。</span><span class="sxs-lookup"><span data-stu-id="a62b0-120">It is encoded using the Base64 algorithm.</span></span> <span data-ttu-id="a62b0-121">*コンテンツの種類: アプリケーションまたはオクテット ストリーム* (既定ではファイルの拡張子に基づいて)</span><span class="sxs-lookup"><span data-stu-id="a62b0-121">*Content-type: application/octet-stream*  (by default; based on file extension)</span></span> 
    
     * <span data-ttu-id="a62b0-122">Base64 のコンテンツ転送エンコード: \*</span><span class="sxs-lookup"><span data-stu-id="a62b0-122">Content-Transfer-Encoding: base64 \*</span></span> 
    
<span data-ttu-id="a62b0-123">送信メッセージは、コンテンツの種類必要がありますから派生するファイル名の 3 文字の拡張子。</span><span class="sxs-lookup"><span data-stu-id="a62b0-123">On outbound messages, the content-type should be derived from the filename's three-letter extension.</span></span> <span data-ttu-id="a62b0-124">システム レジストリにこのマッピングが存在します。下で文字列値の名前は「コンテンツの種類」が定義されている場合、MIME コンテンツの種類を示す。</span><span class="sxs-lookup"><span data-stu-id="a62b0-124">This mapping exists in the system registry; under there is a string value named "Content Type" that gives the MIME content type if one is defined.</span></span> <span data-ttu-id="a62b0-125">この例では、TIFF イメージ ファイルです。</span><span class="sxs-lookup"><span data-stu-id="a62b0-125">This example is for a TIFF image file:</span></span>
  
<span data-ttu-id="a62b0-126">HKEY_LOCAL_MACHINE\\</span><span class="sxs-lookup"><span data-stu-id="a62b0-126">HKEY_LOCAL_MACHINE\\</span></span>
  
<span data-ttu-id="a62b0-127">Software\\</span><span class="sxs-lookup"><span data-stu-id="a62b0-127">Software\\</span></span>
  
<span data-ttu-id="a62b0-128">Microsoft\\</span><span class="sxs-lookup"><span data-stu-id="a62b0-128">Microsoft\\</span></span>
  
<span data-ttu-id="a62b0-129">Classes\\</span><span class="sxs-lookup"><span data-stu-id="a62b0-129">Classes\\</span></span>
  
<span data-ttu-id="a62b0-130">.tif</span><span class="sxs-lookup"><span data-stu-id="a62b0-130">.tif</span></span>
  
<span data-ttu-id="a62b0-131">コンテンツ タイプ =「画像/tiff」</span><span class="sxs-lookup"><span data-stu-id="a62b0-131">Content Type = "image/tiff"</span></span>
  
<span data-ttu-id="a62b0-132">ファイル拡張子のマッピングがない場合、既定の*アプリケーションまたはオクテット*ストリームを使用してください。</span><span class="sxs-lookup"><span data-stu-id="a62b0-132">If there is no mapping for the file extension, the default  *application/octet*  stream should be used.</span></span> 
  
<span data-ttu-id="a62b0-133">受信したメッセージ、添付ファイルのコンテンツの種類が常に MAPI プロパティの**PR_ATTACH_MIME_TAG** ([PidTagAttachMimeTag](pidtagattachmimetag-canonical-property.md)) にコピーしてください。</span><span class="sxs-lookup"><span data-stu-id="a62b0-133">On inbound messages, the content-type for an attachment should always be copied to the MAPI property **PR_ATTACH_MIME_TAG** ([PidTagAttachMimeTag](pidtagattachmimetag-canonical-property.md)).</span></span> <span data-ttu-id="a62b0-134">**PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) と**PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) のプロパティ] でコンテンツ タイプにマップされている拡張機能を使用する必要がある場合でも、添付ファイルのファイル名が定義されると、.</span><span class="sxs-lookup"><span data-stu-id="a62b0-134">Even if a filename is defined for an attached file, the extension mapped by the content-type should be used in the **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) and **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) properties.</span></span>
  
<span data-ttu-id="a62b0-135">*Name*パラメーターは、RFC 821 で正式に廃止されます。</span><span class="sxs-lookup"><span data-stu-id="a62b0-135">The  *name*  parameter is officially deprecated by RFC 821.</span></span> <span data-ttu-id="a62b0-136">標準の出現に伴い、マイクロソフトは接続されているファイル名の代替マッピングを指定することを検討します。</span><span class="sxs-lookup"><span data-stu-id="a62b0-136">As standards evolve, Microsoft will consider specifying an alternate mapping for attached filenames.</span></span> 
  
<span data-ttu-id="a62b0-137">として添付されたメッセージの送信が送信されます * コンテンツの種類: メッセージと rfc822 * 添付されたメッセージ内のメッセージは、適切な場所で、エンコードを再帰的にします。</span><span class="sxs-lookup"><span data-stu-id="a62b0-137">Outbound attached messages are sent as * Content-type: message/rfc822 *  Messages within attached messages are encoded recursively, in their proper place.</span></span> <span data-ttu-id="a62b0-138">受信メッセージのコンテンツ部分を*コンテンツの種類: マルチパート/ダイジェスト*埋め込みメッセージにマッピングされます。</span><span class="sxs-lookup"><span data-stu-id="a62b0-138">Inbound message content parts with  *Content-Type: multipart/digest*  are also mapped to embedded messages.</span></span> 
  
<span data-ttu-id="a62b0-139">メッセージの内容をエンコード中に TNEF を uuencode を使用すると、すべての添付ファイルのプロパティとコンテンツが TNEF ストリームでは。</span><span class="sxs-lookup"><span data-stu-id="a62b0-139">If uuencode with TNEF is used while encoding message content, all attachment properties and content are in the TNEF stream.</span></span> <span data-ttu-id="a62b0-140">自体 TNEF は、TNEF なしでも、Uuencode のエンコード、Winmail.dat という名前の 1 つのバイナリ添付ファイルです。</span><span class="sxs-lookup"><span data-stu-id="a62b0-140">The TNEF itself is a single, binary attached file named Winmail.dat, encoded as described for Uuencode without TNEF.</span></span>
  
<span data-ttu-id="a62b0-141">TNEF なし uuencode を使用する場合は、すべての添付ファイルがバイナリ形式とエンコードされていない、次のメッセージのテキストとして扱われます。</span><span class="sxs-lookup"><span data-stu-id="a62b0-141">If uuencode is used without TNEF, all attached files are treated as binary and uuencoded, following the message text.</span></span> <span data-ttu-id="a62b0-142">ファイル名は、uuencode ヘッダー内に存在します。</span><span class="sxs-lookup"><span data-stu-id="a62b0-142">The file name is present in the uuencode header:</span></span>
  
 <span data-ttu-id="a62b0-143">0755 Winmail.dat を開始します。</span><span class="sxs-lookup"><span data-stu-id="a62b0-143">begin 0755 Winmail.dat</span></span> 
  
 <span data-ttu-id="a62b0-144">. データ.</span><span class="sxs-lookup"><span data-stu-id="a62b0-144">... data ...</span></span> 
  
 <span data-ttu-id="a62b0-145">end</span><span class="sxs-lookup"><span data-stu-id="a62b0-145">end</span></span> 
  
<span data-ttu-id="a62b0-146">添付されたメッセージは、メッセージ テキストに textized します。</span><span class="sxs-lookup"><span data-stu-id="a62b0-146">Attached messages are textized into the message text.</span></span> <span data-ttu-id="a62b0-147">添付されたメッセージの階層は常に平坦化します。添付されたメッセージ内のメッセージが引き出されている最上位レベルにします。</span><span class="sxs-lookup"><span data-stu-id="a62b0-147">The hierarchy of attached messages is always flattened; that is, messages within attached messages are pulled out to the top level.</span></span>
  
<span data-ttu-id="a62b0-148">埋め込み OLE オブジェクトは破棄されます。</span><span class="sxs-lookup"><span data-stu-id="a62b0-148">Embedded OLE objects are discarded.</span></span>
  
<span data-ttu-id="a62b0-149">添付ファイルのレンダリング位置は、 **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) のプロパティを使用して、TNEF でそのままで送信されます。</span><span class="sxs-lookup"><span data-stu-id="a62b0-149">Attachment rendering positions are transmitted literally, using the property **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) in the TNEF.</span></span> <span data-ttu-id="a62b0-150">TNEF を使用しない場合に失われます。</span><span class="sxs-lookup"><span data-stu-id="a62b0-150">If TNEF is not used, they are lost.</span></span> <span data-ttu-id="a62b0-151">(TNEF が存在しない場合を含む) のレンダリング位置で受信した添付ファイルには、その描画位置の設定は、0 xffffffff にないメッセージのテキスト内の位置があります。</span><span class="sxs-lookup"><span data-stu-id="a62b0-151">Incoming attachments with no rendering position (including when there is no TNEF) have their rendering position set to 0xFFFFFFFF, that is, no position in the message text.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a62b0-152">関連項目</span><span class="sxs-lookup"><span data-stu-id="a62b0-152">See also</span></span>



[<span data-ttu-id="a62b0-153">インターネット メールの属性から MAPI のプロパティへのマッピング</span><span class="sxs-lookup"><span data-stu-id="a62b0-153">Mapping of Internet Mail Attributes to MAPI Properties</span></span>](mapping-of-internet-mail-attributes-to-mapi-properties.md)

