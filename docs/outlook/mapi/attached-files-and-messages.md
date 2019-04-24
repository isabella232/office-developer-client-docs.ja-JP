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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318131"
---
# <a name="attached-files-and-messages"></a><span data-ttu-id="06f0a-103">添付ファイルとメッセージ</span><span class="sxs-lookup"><span data-stu-id="06f0a-103">Attached Files and Messages</span></span>

  
  
<span data-ttu-id="06f0a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="06f0a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="06f0a-105">メッセージの内容をエンコードする際に、tnef の MIME を使用する場合は、すべての添付ファイルのプロパティとコンテンツが tnef ストリームに含まれています。</span><span class="sxs-lookup"><span data-stu-id="06f0a-105">If MIME with TNEF is used while encoding message content,all attachment properties and content are in the TNEF stream.</span></span> <span data-ttu-id="06f0a-106">tnef 自体は、tnef なしで記述された、winmail.dat という名前の単一のバイナリ添付ファイルです。</span><span class="sxs-lookup"><span data-stu-id="06f0a-106">The TNEF itself is a single, binary attached file named Winmail.dat, encoded as described for MIME without TNEF.</span></span> 
  
<span data-ttu-id="06f0a-107">mime が TNEF なしで使用される場合、添付ファイルは mime メッセージコンテンツのパーツとして送信されます。</span><span class="sxs-lookup"><span data-stu-id="06f0a-107">If MIME is used without TNEF, attached files are sent as MIME message content parts.</span></span> <span data-ttu-id="06f0a-108">filename は、添付ファイルの*content-type*ヘッダーの*name*パラメーターに配置されます。</span><span class="sxs-lookup"><span data-stu-id="06f0a-108">The filename is placed in the  *name*  parameter to the  *Content-type*  header for the attachment.</span></span> <span data-ttu-id="06f0a-109">添付ファイルの文字セットは、*コンテンツタイプ*の*charset*パラメーターに配置されます。また、コンテンツ転送エンコードは、添付ファイルコンテンツ全体をスキャンすることによって決定されます。</span><span class="sxs-lookup"><span data-stu-id="06f0a-109">The character set for the attachment is placed in the  *charset*  parameter to the  *Content-type*  ; it and the content-transfer-encoding are determined by scanning the entire attachment content.</span></span> <span data-ttu-id="06f0a-110">URL の添付ファイルは、特別に扱われます。</span><span class="sxs-lookup"><span data-stu-id="06f0a-110">URL attachments are treated specially:</span></span> 
  
- <span data-ttu-id="06f0a-111">添付ファイルが URL (拡張子が付いた添付ファイル) の場合。url) を指定し、それに定義されているアクセスモードが匿名 FTP である場合は、外部メッセージとしてエンコードされ、ファイル (URL) の内容が外部メッセージのヘッダーにコピーされます。</span><span class="sxs-lookup"><span data-stu-id="06f0a-111">If the attachment is a URL (an attached file with extension .URL), and the access mode defined in it is anonymous FTP, it is encoded as an external message, and the content of the file (the URL) is copied into the header of the external message.</span></span> <span data-ttu-id="06f0a-112">*コンテンツタイプ: メッセージ/外部-本文、アクセスタイプ = 無効化-ftp* (コンテンツ転送エンコード: 7bit が想定されています。)</span><span class="sxs-lookup"><span data-stu-id="06f0a-112">*Content-type: message/external-body; access-type=anon-ftp*  (Content-Transfer-Encoding: 7bit is assumed.)</span></span> 
    
- <span data-ttu-id="06f0a-113">7ビット文字のみが検索され、長さが140文字を超える行がない場合、添付ファイルは ASCII テキストになります。</span><span class="sxs-lookup"><span data-stu-id="06f0a-113">If only 7-bit characters are found and no line exceeds 140 characters in length, the attachment is ASCII text.</span></span> <span data-ttu-id="06f0a-114">*コンテンツタイプ: text/plain。charset = us-ascii コンテンツ転送エンコード: 7bit*</span><span class="sxs-lookup"><span data-stu-id="06f0a-114">*Content-type: text/plain; charset=us-ascii Content-Transfer-Encoding: 7bit*</span></span> 
    
- <span data-ttu-id="06f0a-115">long 行または最大 25% の8ビット文字が検出された場合、添付ファイルのコンテンツはテキストであり、文字セットはロケールによって決定されます。</span><span class="sxs-lookup"><span data-stu-id="06f0a-115">If long lines or up to 25% 8-bit characters are found, the attachment content is text and the character set is determined by the locale.</span></span> <span data-ttu-id="06f0a-116">ISO 規格8859で定義されている文字セットから選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="06f0a-116">It should be chosen from the character sets defined by ISO standard 8859.</span></span> <span data-ttu-id="06f0a-117">*コンテンツタイプ: text/plain、charset = ISO-8859-1* (例:)</span><span class="sxs-lookup"><span data-stu-id="06f0a-117">*Content-type: text/plain; charset=ISO-8859-1*  (for example)</span></span> 
    
     <span data-ttu-id="06f0a-118">*Content-Transfer-Encoding: quoted-printable*</span><span class="sxs-lookup"><span data-stu-id="06f0a-118">*Content-Transfer-Encoding: quoted-printable*</span></span> 
    
- <span data-ttu-id="06f0a-119">25% 以上の文字の上位ビットが設定されている場合、添付ファイルはバイナリになります。</span><span class="sxs-lookup"><span data-stu-id="06f0a-119">If 25% or more of the characters have the high bit set, the attachment is binary.</span></span> <span data-ttu-id="06f0a-120">Base64 アルゴリズムを使用してエンコードされます。</span><span class="sxs-lookup"><span data-stu-id="06f0a-120">It is encoded using the Base64 algorithm.</span></span> <span data-ttu-id="06f0a-121">*コンテンツタイプ: application/オクテットストリーム* (既定では、ファイル拡張子に基づいて)</span><span class="sxs-lookup"><span data-stu-id="06f0a-121">*Content-type: application/octet-stream*  (by default; based on file extension)</span></span> 
    
     * <span data-ttu-id="06f0a-122">コンテンツ転送エンコード: base64 \*</span><span class="sxs-lookup"><span data-stu-id="06f0a-122">Content-Transfer-Encoding: base64 \*</span></span> 
    
<span data-ttu-id="06f0a-123">送信メッセージの場合、コンテンツタイプはファイル名の3文字の拡張子から派生する必要があります。</span><span class="sxs-lookup"><span data-stu-id="06f0a-123">On outbound messages, the content-type should be derived from the filename's three-letter extension.</span></span> <span data-ttu-id="06f0a-124">このマッピングはシステムレジストリに存在します。MIME コンテンツタイプが定義されている場合は、"コンテンツタイプ" という名前の文字列値があります。</span><span class="sxs-lookup"><span data-stu-id="06f0a-124">This mapping exists in the system registry; under there is a string value named "Content Type" that gives the MIME content type if one is defined.</span></span> <span data-ttu-id="06f0a-125">TIFF イメージファイルの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="06f0a-125">This example is for a TIFF image file:</span></span>
  
<span data-ttu-id="06f0a-126">HKEY_LOCAL_MACHINE \\</span><span class="sxs-lookup"><span data-stu-id="06f0a-126">HKEY_LOCAL_MACHINE\\</span></span>
  
<span data-ttu-id="06f0a-127">ソフトウェア</span><span class="sxs-lookup"><span data-stu-id="06f0a-127">Software\\</span></span>
  
<span data-ttu-id="06f0a-128">製</span><span class="sxs-lookup"><span data-stu-id="06f0a-128">Microsoft\\</span></span>
  
<span data-ttu-id="06f0a-129">クラス</span><span class="sxs-lookup"><span data-stu-id="06f0a-129">Classes\\</span></span>
  
<span data-ttu-id="06f0a-130">.tif</span><span class="sxs-lookup"><span data-stu-id="06f0a-130">.tif</span></span>
  
<span data-ttu-id="06f0a-131">コンテンツタイプ = "image/tiff"</span><span class="sxs-lookup"><span data-stu-id="06f0a-131">Content Type = "image/tiff"</span></span>
  
<span data-ttu-id="06f0a-132">ファイル拡張子がマッピングされていない場合は、既定の*アプリケーション/オクテット*ストリームを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="06f0a-132">If there is no mapping for the file extension, the default  *application/octet*  stream should be used.</span></span> 
  
<span data-ttu-id="06f0a-133">受信メッセージの場合、添付ファイルのコンテンツタイプは常に MAPI プロパティ**PR_ATTACH_MIME_TAG** ([PidTagAttachMimeTag](pidtagattachmimetag-canonical-property.md)) にコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="06f0a-133">On inbound messages, the content-type for an attachment should always be copied to the MAPI property **PR_ATTACH_MIME_TAG** ([PidTagAttachMimeTag](pidtagattachmimetag-canonical-property.md)).</span></span> <span data-ttu-id="06f0a-134">添付ファイルに対してファイル名が定義されている場合でも、 **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) および**PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) プロパティで、コンテンツタイプによってマッピングされた拡張子を使用する必要があります。.</span><span class="sxs-lookup"><span data-stu-id="06f0a-134">Even if a filename is defined for an attached file, the extension mapped by the content-type should be used in the **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) and **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) properties.</span></span>
  
<span data-ttu-id="06f0a-135">*name*パラメーターは、RFC 821 によって正式に非推奨になりました。</span><span class="sxs-lookup"><span data-stu-id="06f0a-135">The  *name*  parameter is officially deprecated by RFC 821.</span></span> <span data-ttu-id="06f0a-136">標準が進化するにつれて、Microsoft は添付ファイル名の代替マッピングを指定することを検討します。</span><span class="sxs-lookup"><span data-stu-id="06f0a-136">As standards evolve, Microsoft will consider specifying an alternate mapping for attached filenames.</span></span> 
  
<span data-ttu-id="06f0a-137">送信添付メッセージは、\* content-type として送信されます: message/rfc822 \* 添付メッセージ内のメッセージは、適切な場所に再帰的にエンコードされます。</span><span class="sxs-lookup"><span data-stu-id="06f0a-137">Outbound attached messages are sent as \* Content-type: message/rfc822 \*  Messages within attached messages are encoded recursively, in their proper place.</span></span> <span data-ttu-id="06f0a-138">コンテンツタイプの受信メッセージコンテンツパーツ *: マルチパート/ダイジェスト*は、埋め込みメッセージにもマップされます。</span><span class="sxs-lookup"><span data-stu-id="06f0a-138">Inbound message content parts with  *Content-Type: multipart/digest*  are also mapped to embedded messages.</span></span> 
  
<span data-ttu-id="06f0a-139">メッセージの内容をエンコードする際に、tnef を含む uuencode が使用されている場合、すべての添付ファイルのプロパティとコンテンツが tnef ストリームに含まれます。</span><span class="sxs-lookup"><span data-stu-id="06f0a-139">If uuencode with TNEF is used while encoding message content, all attachment properties and content are in the TNEF stream.</span></span> <span data-ttu-id="06f0a-140">tnef 自体は、tnef なしで記述された、winmail.dat という名前の単一のバイナリ添付ファイルです。</span><span class="sxs-lookup"><span data-stu-id="06f0a-140">The TNEF itself is a single, binary attached file named Winmail.dat, encoded as described for Uuencode without TNEF.</span></span>
  
<span data-ttu-id="06f0a-141">TNEF が使用されていない場合、添付ファイルはすべて、メッセージテキストの後、バイナリと uuencode として処理されます。</span><span class="sxs-lookup"><span data-stu-id="06f0a-141">If uuencode is used without TNEF, all attached files are treated as binary and uuencoded, following the message text.</span></span> <span data-ttu-id="06f0a-142">ファイル名は、uuencode ヘッダーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="06f0a-142">The file name is present in the uuencode header:</span></span>
  
 <span data-ttu-id="06f0a-143">開始 0755 winmail.dat</span><span class="sxs-lookup"><span data-stu-id="06f0a-143">begin 0755 Winmail.dat</span></span> 
  
 <span data-ttu-id="06f0a-144">...データ...</span><span class="sxs-lookup"><span data-stu-id="06f0a-144">... data ...</span></span> 
  
 <span data-ttu-id="06f0a-145">end</span><span class="sxs-lookup"><span data-stu-id="06f0a-145">end</span></span> 
  
<span data-ttu-id="06f0a-146">添付されたメッセージは、メッセージテキストに textized ます。</span><span class="sxs-lookup"><span data-stu-id="06f0a-146">Attached messages are textized into the message text.</span></span> <span data-ttu-id="06f0a-147">添付されたメッセージの階層は常に平坦化されます。つまり、添付されたメッセージ内のメッセージは最上位レベルにプルアウトされます。</span><span class="sxs-lookup"><span data-stu-id="06f0a-147">The hierarchy of attached messages is always flattened; that is, messages within attached messages are pulled out to the top level.</span></span>
  
<span data-ttu-id="06f0a-148">埋め込み OLE オブジェクトは破棄されます。</span><span class="sxs-lookup"><span data-stu-id="06f0a-148">Embedded OLE objects are discarded.</span></span>
  
<span data-ttu-id="06f0a-149">添付ファイルのレンダリング位置は、TNEF のプロパティ**PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) を使用して、文字どおり転送されます。</span><span class="sxs-lookup"><span data-stu-id="06f0a-149">Attachment rendering positions are transmitted literally, using the property **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) in the TNEF.</span></span> <span data-ttu-id="06f0a-150">TNEF が使用されていない場合は、失われます。</span><span class="sxs-lookup"><span data-stu-id="06f0a-150">If TNEF is not used, they are lost.</span></span> <span data-ttu-id="06f0a-151">レンダリング位置のない受信添付ファイル (TNEF がない場合を含む) は、レンダリング位置が0xffffffff に設定されます。つまり、メッセージテキストに位置がありません。</span><span class="sxs-lookup"><span data-stu-id="06f0a-151">Incoming attachments with no rendering position (including when there is no TNEF) have their rendering position set to 0xFFFFFFFF, that is, no position in the message text.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="06f0a-152">関連項目</span><span class="sxs-lookup"><span data-stu-id="06f0a-152">See also</span></span>



[<span data-ttu-id="06f0a-153">インターネットメールの属性から MAPI プロパティへのマッピング</span><span class="sxs-lookup"><span data-stu-id="06f0a-153">Mapping of Internet Mail Attributes to MAPI Properties</span></span>](mapping-of-internet-mail-attributes-to-mapi-properties.md)

