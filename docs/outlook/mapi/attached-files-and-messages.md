---
title: 添付ファイルとメッセージ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b2f2fb72-23ae-4e0b-a8a1-3b78a1862acb
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: c4dbe1a761a753bef77168aec8d2674a1b2b100e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436840"
---
# <a name="attached-files-and-messages"></a><span data-ttu-id="1a57f-103">添付ファイルとメッセージ</span><span class="sxs-lookup"><span data-stu-id="1a57f-103">Attached Files and Messages</span></span>

  
  
<span data-ttu-id="1a57f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1a57f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1a57f-105">メッセージ コンテンツのエンコード中に TNEF を含む MIME を使用すると、すべての添付ファイルプロパティとコンテンツが TNEF ストリームに含まれます。</span><span class="sxs-lookup"><span data-stu-id="1a57f-105">If MIME with TNEF is used while encoding message content,all attachment properties and content are in the TNEF stream.</span></span> <span data-ttu-id="1a57f-106">TNEF 自体は Winmail.dat という名前の単一のバイナリ添付ファイルで、TNEF のない MIME でエンコードされています。</span><span class="sxs-lookup"><span data-stu-id="1a57f-106">The TNEF itself is a single, binary attached file named Winmail.dat, encoded as described for MIME without TNEF.</span></span> 
  
<span data-ttu-id="1a57f-107">TNEF なしで MIME を使用する場合、添付ファイルは MIME メッセージ コンテンツ パーツとして送信されます。</span><span class="sxs-lookup"><span data-stu-id="1a57f-107">If MIME is used without TNEF, attached files are sent as MIME message content parts.</span></span> <span data-ttu-id="1a57f-108">ファイル名は、添付ファイル  *の*  *Content-type*  ヘッダーの name パラメーターに配置されます。</span><span class="sxs-lookup"><span data-stu-id="1a57f-108">The filename is placed in the  *name*  parameter to the  *Content-type*  header for the attachment.</span></span> <span data-ttu-id="1a57f-109">添付ファイルの文字セットは  *、charset*  パラメーターに  *Content-type に配置されます*  。コンテンツ転送エンコードは、添付ファイルのコンテンツ全体をスキャンすることで決まります。</span><span class="sxs-lookup"><span data-stu-id="1a57f-109">The character set for the attachment is placed in the  *charset*  parameter to the  *Content-type*  ; it and the content-transfer-encoding are determined by scanning the entire attachment content.</span></span> <span data-ttu-id="1a57f-110">URL 添付ファイルは特別に扱います。</span><span class="sxs-lookup"><span data-stu-id="1a57f-110">URL attachments are treated specially:</span></span> 
  
- <span data-ttu-id="1a57f-111">添付ファイルが URL (拡張子が付いている添付ファイル) の場合。URL)、およびその中で定義されているアクセス モードは匿名 FTP であり、外部メッセージとしてエンコードされ、ファイルのコンテンツ (URL) は外部メッセージのヘッダーにコピーされます。</span><span class="sxs-lookup"><span data-stu-id="1a57f-111">If the attachment is a URL (an attached file with extension .URL), and the access mode defined in it is anonymous FTP, it is encoded as an external message, and the content of the file (the URL) is copied into the header of the external message.</span></span> <span data-ttu-id="1a57f-112">*コンテンツ タイプ: メッセージ/外部本文、access-type=anon-ftp (Content-Transfer-Encoding:*  7bit が想定されます)。</span><span class="sxs-lookup"><span data-stu-id="1a57f-112">*Content-type: message/external-body; access-type=anon-ftp*  (Content-Transfer-Encoding: 7bit is assumed.)</span></span> 
    
- <span data-ttu-id="1a57f-113">7 ビット文字だけが見つかり、行の長さが 140 文字を超えない場合、添付ファイルは ASCII テキストです。</span><span class="sxs-lookup"><span data-stu-id="1a57f-113">If only 7-bit characters are found and no line exceeds 140 characters in length, the attachment is ASCII text.</span></span> <span data-ttu-id="1a57f-114">*コンテンツ タイプ: テキスト/プレーン。charset=us-ascii Content-Transfer-Encoding: 7bit*</span><span class="sxs-lookup"><span data-stu-id="1a57f-114">*Content-type: text/plain; charset=us-ascii Content-Transfer-Encoding: 7bit*</span></span> 
    
- <span data-ttu-id="1a57f-115">長い行または最大 25% の 8 ビット文字が見つかった場合、添付ファイルのコンテンツはテキストであり、文字セットはロケールによって決まります。</span><span class="sxs-lookup"><span data-stu-id="1a57f-115">If long lines or up to 25% 8-bit characters are found, the attachment content is text and the character set is determined by the locale.</span></span> <span data-ttu-id="1a57f-116">ISO 標準 8859 で定義されている文字セットから選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1a57f-116">It should be chosen from the character sets defined by ISO standard 8859.</span></span> <span data-ttu-id="1a57f-117">*コンテンツ タイプ: テキスト/プレーン、charset=ISO-8859-1*  (たとえば)</span><span class="sxs-lookup"><span data-stu-id="1a57f-117">*Content-type: text/plain; charset=ISO-8859-1*  (for example)</span></span> 
    
     <span data-ttu-id="1a57f-118">*Content-Transfer-Encoding: quoted-printable*</span><span class="sxs-lookup"><span data-stu-id="1a57f-118">*Content-Transfer-Encoding: quoted-printable*</span></span> 
    
- <span data-ttu-id="1a57f-119">25% 以上の文字にハイ ビットが設定されている場合、添付ファイルはバイナリになります。</span><span class="sxs-lookup"><span data-stu-id="1a57f-119">If 25% or more of the characters have the high bit set, the attachment is binary.</span></span> <span data-ttu-id="1a57f-120">Base64 アルゴリズムを使用してエンコードされます。</span><span class="sxs-lookup"><span data-stu-id="1a57f-120">It is encoded using the Base64 algorithm.</span></span> <span data-ttu-id="1a57f-121">*コンテンツタイプ: application/octet-stream*  (既定では、ファイル拡張子に基づく)</span><span class="sxs-lookup"><span data-stu-id="1a57f-121">*Content-type: application/octet-stream*  (by default; based on file extension)</span></span> 
    
     * <span data-ttu-id="1a57f-122">Content-Transfer-Encoding: base64 \*</span><span class="sxs-lookup"><span data-stu-id="1a57f-122">Content-Transfer-Encoding: base64 \*</span></span> 
    
<span data-ttu-id="1a57f-123">送信メッセージでは、コンテンツ タイプはファイル名の 3 文字の拡張子から派生する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1a57f-123">On outbound messages, the content-type should be derived from the filename's three-letter extension.</span></span> <span data-ttu-id="1a57f-124">このマッピングは、システム レジストリに存在します。の下には、MIME コンテンツ タイプが定義されている場合に MIME コンテンツ タイプを与える "Content Type" という名前の文字列値があります。</span><span class="sxs-lookup"><span data-stu-id="1a57f-124">This mapping exists in the system registry; under there is a string value named "Content Type" that gives the MIME content type if one is defined.</span></span> <span data-ttu-id="1a57f-125">次の例は、TIFF イメージ ファイル用です。</span><span class="sxs-lookup"><span data-stu-id="1a57f-125">This example is for a TIFF image file:</span></span>
  
<span data-ttu-id="1a57f-126">HKEY_LOCAL_MACHINE</span><span class="sxs-lookup"><span data-stu-id="1a57f-126">HKEY_LOCAL_MACHINE</span></span>\
  
<span data-ttu-id="1a57f-127">Software</span><span class="sxs-lookup"><span data-stu-id="1a57f-127">Software</span></span>\
  
<span data-ttu-id="1a57f-128">Microsoft</span><span class="sxs-lookup"><span data-stu-id="1a57f-128">Microsoft</span></span>\
  
<span data-ttu-id="1a57f-129">クラス</span><span class="sxs-lookup"><span data-stu-id="1a57f-129">Classes</span></span>\
  
<span data-ttu-id="1a57f-130">.tif</span><span class="sxs-lookup"><span data-stu-id="1a57f-130">.tif</span></span>
  
<span data-ttu-id="1a57f-131">コンテンツ タイプ = "image/tiff"</span><span class="sxs-lookup"><span data-stu-id="1a57f-131">Content Type = "image/tiff"</span></span>
  
<span data-ttu-id="1a57f-132">ファイル拡張子のマッピングがない場合は、既定の  *アプリケーション/オクテット ストリームを*  使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1a57f-132">If there is no mapping for the file extension, the default  *application/octet*  stream should be used.</span></span> 
  
<span data-ttu-id="1a57f-133">受信メッセージでは、添付ファイルのコンテンツ タイプは常に MAPI プロパティ [(PidTagAttachMimeTag)](pidtagattachmimetag-canonical-property.md)にコピー **PR_ATTACH_MIME_TAGする** 必要があります。</span><span class="sxs-lookup"><span data-stu-id="1a57f-133">On inbound messages, the content-type for an attachment should always be copied to the MAPI property **PR_ATTACH_MIME_TAG** ([PidTagAttachMimeTag](pidtagattachmimetag-canonical-property.md)).</span></span> <span data-ttu-id="1a57f-134">添付ファイルに対してファイル名が定義されている場合でも、PR_ATTACH_FILENAME ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) プロパティおよび **PR_ATTACH_EXTENSION** **(** [PidTagAttachExtension](pidtagattachextension-canonical-property.md)) プロパティで、コンテンツ タイプによってマップされた拡張子を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1a57f-134">Even if a filename is defined for an attached file, the extension mapped by the content-type should be used in the **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) and **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) properties.</span></span>
  
<span data-ttu-id="1a57f-135">name  *パラメーター*  は、RFC 821 によって正式に非推奨です。</span><span class="sxs-lookup"><span data-stu-id="1a57f-135">The  *name*  parameter is officially deprecated by RFC 821.</span></span> <span data-ttu-id="1a57f-136">標準が進化するにつれて、添付ファイル名の代替マッピングの指定を検討します。</span><span class="sxs-lookup"><span data-stu-id="1a57f-136">As standards evolve, Microsoft will consider specifying an alternate mapping for attached filenames.</span></span> 
  
<span data-ttu-id="1a57f-137">送信添付メッセージは \* Content-type: message/rfc822 \* 添付メッセージ内のメッセージは、適切な場所で再帰的にエンコードされます。</span><span class="sxs-lookup"><span data-stu-id="1a57f-137">Outbound attached messages are sent as \* Content-type: message/rfc822 \*  Messages within attached messages are encoded recursively, in their proper place.</span></span> <span data-ttu-id="1a57f-138">*Content-Type: マルチパート/* ダイジェストを持つ受信メッセージ コンテンツ パーツも、埋め込みメッセージにマップされます。</span><span class="sxs-lookup"><span data-stu-id="1a57f-138">Inbound message content parts with  *Content-Type: multipart/digest*  are also mapped to embedded messages.</span></span> 
  
<span data-ttu-id="1a57f-139">メッセージ コンテンツのエンコード中に TNEF を含む uuencode を使用すると、すべての添付ファイルのプロパティとコンテンツが TNEF ストリームに含まれます。</span><span class="sxs-lookup"><span data-stu-id="1a57f-139">If uuencode with TNEF is used while encoding message content, all attachment properties and content are in the TNEF stream.</span></span> <span data-ttu-id="1a57f-140">TNEF 自体は Winmail.dat という名前の単一のバイナリ添付ファイルで、TNEF のない Uuencode で記述されています。</span><span class="sxs-lookup"><span data-stu-id="1a57f-140">The TNEF itself is a single, binary attached file named Winmail.dat, encoded as described for Uuencode without TNEF.</span></span>
  
<span data-ttu-id="1a57f-141">TNEF を使用せずに uuencode を使用すると、添付ファイルはすべてバイナリと uuencoded として処理され、メッセージ テキストに続いて処理されます。</span><span class="sxs-lookup"><span data-stu-id="1a57f-141">If uuencode is used without TNEF, all attached files are treated as binary and uuencoded, following the message text.</span></span> <span data-ttu-id="1a57f-142">ファイル名は uuencode ヘッダーに存在します。</span><span class="sxs-lookup"><span data-stu-id="1a57f-142">The file name is present in the uuencode header:</span></span>
  
 <span data-ttu-id="1a57f-143">begin 0755 Winmail.dat</span><span class="sxs-lookup"><span data-stu-id="1a57f-143">begin 0755 Winmail.dat</span></span> 
  
 <span data-ttu-id="1a57f-144">...data ...</span><span class="sxs-lookup"><span data-stu-id="1a57f-144">... data ...</span></span> 
  
 <span data-ttu-id="1a57f-145">end</span><span class="sxs-lookup"><span data-stu-id="1a57f-145">end</span></span> 
  
<span data-ttu-id="1a57f-146">添付されたメッセージは、メッセージ テキストにテキスト化されます。</span><span class="sxs-lookup"><span data-stu-id="1a57f-146">Attached messages are textized into the message text.</span></span> <span data-ttu-id="1a57f-147">添付メッセージの階層は常にフラット化されます。つまり、添付メッセージ内のメッセージはトップ レベルにプルアウトされます。</span><span class="sxs-lookup"><span data-stu-id="1a57f-147">The hierarchy of attached messages is always flattened; that is, messages within attached messages are pulled out to the top level.</span></span>
  
<span data-ttu-id="1a57f-148">埋め込み OLE オブジェクトは破棄されます。</span><span class="sxs-lookup"><span data-stu-id="1a57f-148">Embedded OLE objects are discarded.</span></span>
  
<span data-ttu-id="1a57f-149">添付ファイルのレンダリング位置は、TNEF のプロパティ PR_ATTACH_RENDERING **(** [PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) を使用して、文字通り送信されます。</span><span class="sxs-lookup"><span data-stu-id="1a57f-149">Attachment rendering positions are transmitted literally, using the property **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) in the TNEF.</span></span> <span data-ttu-id="1a57f-150">TNEF を使用しない場合、それらは失われます。</span><span class="sxs-lookup"><span data-stu-id="1a57f-150">If TNEF is not used, they are lost.</span></span> <span data-ttu-id="1a57f-151">レンダリング位置がない受信添付ファイル (TNEF がない場合を含む) は、レンダリング位置を 0xFFFFFFFF に設定します。つまり、メッセージ テキスト内の位置はありません。</span><span class="sxs-lookup"><span data-stu-id="1a57f-151">Incoming attachments with no rendering position (including when there is no TNEF) have their rendering position set to 0xFFFFFFFF, that is, no position in the message text.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1a57f-152">関連項目</span><span class="sxs-lookup"><span data-stu-id="1a57f-152">See also</span></span>



[<span data-ttu-id="1a57f-153">インターネット メール属性の MAPI プロパティへのマッピング</span><span class="sxs-lookup"><span data-stu-id="1a57f-153">Mapping of Internet Mail Attributes to MAPI Properties</span></span>](mapping-of-internet-mail-attributes-to-mapi-properties.md)

