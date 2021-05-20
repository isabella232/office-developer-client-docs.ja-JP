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
# <a name="attached-files-and-messages"></a>添付ファイルとメッセージ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ コンテンツのエンコード中に TNEF を含む MIME を使用すると、すべての添付ファイルプロパティとコンテンツが TNEF ストリームに含まれます。 TNEF 自体は Winmail.dat という名前の単一のバイナリ添付ファイルで、TNEF のない MIME でエンコードされています。 
  
TNEF なしで MIME を使用する場合、添付ファイルは MIME メッセージ コンテンツ パーツとして送信されます。 ファイル名は、添付ファイル  *の*  *Content-type*  ヘッダーの name パラメーターに配置されます。 添付ファイルの文字セットは  *、charset*  パラメーターに  *Content-type に配置されます*  。コンテンツ転送エンコードは、添付ファイルのコンテンツ全体をスキャンすることで決まります。 URL 添付ファイルは特別に扱います。 
  
- 添付ファイルが URL (拡張子が付いている添付ファイル) の場合。URL)、およびその中で定義されているアクセス モードは匿名 FTP であり、外部メッセージとしてエンコードされ、ファイルのコンテンツ (URL) は外部メッセージのヘッダーにコピーされます。 *コンテンツ タイプ: メッセージ/外部本文、access-type=anon-ftp (Content-Transfer-Encoding:*  7bit が想定されます)。 
    
- 7 ビット文字だけが見つかり、行の長さが 140 文字を超えない場合、添付ファイルは ASCII テキストです。 *コンテンツ タイプ: テキスト/プレーン。charset=us-ascii Content-Transfer-Encoding: 7bit* 
    
- 長い行または最大 25% の 8 ビット文字が見つかった場合、添付ファイルのコンテンツはテキストであり、文字セットはロケールによって決まります。 ISO 標準 8859 で定義されている文字セットから選択する必要があります。 *コンテンツ タイプ: テキスト/プレーン、charset=ISO-8859-1*  (たとえば) 
    
     *Content-Transfer-Encoding: quoted-printable* 
    
- 25% 以上の文字にハイ ビットが設定されている場合、添付ファイルはバイナリになります。 Base64 アルゴリズムを使用してエンコードされます。 *コンテンツタイプ: application/octet-stream*  (既定では、ファイル拡張子に基づく) 
    
     * Content-Transfer-Encoding: base64 * 
    
送信メッセージでは、コンテンツ タイプはファイル名の 3 文字の拡張子から派生する必要があります。 このマッピングは、システム レジストリに存在します。の下には、MIME コンテンツ タイプが定義されている場合に MIME コンテンツ タイプを与える "Content Type" という名前の文字列値があります。 次の例は、TIFF イメージ ファイル用です。
  
HKEY_LOCAL_MACHINE\
  
Software\
  
Microsoft\
  
クラス\
  
.tif
  
コンテンツ タイプ = "image/tiff"
  
ファイル拡張子のマッピングがない場合は、既定の  *アプリケーション/オクテット ストリームを*  使用する必要があります。 
  
受信メッセージでは、添付ファイルのコンテンツ タイプは常に MAPI プロパティ [(PidTagAttachMimeTag)](pidtagattachmimetag-canonical-property.md)にコピー **PR_ATTACH_MIME_TAGする** 必要があります。 添付ファイルに対してファイル名が定義されている場合でも、PR_ATTACH_FILENAME ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) プロパティおよび **PR_ATTACH_EXTENSION** **(** [PidTagAttachExtension](pidtagattachextension-canonical-property.md)) プロパティで、コンテンツ タイプによってマップされた拡張子を使用する必要があります。
  
name  *パラメーター*  は、RFC 821 によって正式に非推奨です。 標準が進化するにつれて、添付ファイル名の代替マッピングの指定を検討します。 
  
送信添付メッセージは * Content-type: message/rfc822 * 添付メッセージ内のメッセージは、適切な場所で再帰的にエンコードされます。 *Content-Type: マルチパート/* ダイジェストを持つ受信メッセージ コンテンツ パーツも、埋め込みメッセージにマップされます。 
  
メッセージ コンテンツのエンコード中に TNEF を含む uuencode を使用すると、すべての添付ファイルのプロパティとコンテンツが TNEF ストリームに含まれます。 TNEF 自体は Winmail.dat という名前の単一のバイナリ添付ファイルで、TNEF のない Uuencode で記述されています。
  
TNEF を使用せずに uuencode を使用すると、添付ファイルはすべてバイナリと uuencoded として処理され、メッセージ テキストに続いて処理されます。 ファイル名は uuencode ヘッダーに存在します。
  
 begin 0755 Winmail.dat 
  
 ...data ... 
  
 end 
  
添付されたメッセージは、メッセージ テキストにテキスト化されます。 添付メッセージの階層は常にフラット化されます。つまり、添付メッセージ内のメッセージはトップ レベルにプルアウトされます。
  
埋め込み OLE オブジェクトは破棄されます。
  
添付ファイルのレンダリング位置は、TNEF のプロパティ PR_ATTACH_RENDERING **(** [PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) を使用して、文字通り送信されます。 TNEF を使用しない場合、それらは失われます。 レンダリング位置がない受信添付ファイル (TNEF がない場合を含む) は、レンダリング位置を 0xFFFFFFFF に設定します。つまり、メッセージ テキスト内の位置はありません。
  
## <a name="see-also"></a>関連項目



[インターネット メール属性の MAPI プロパティへのマッピング](mapping-of-internet-mail-attributes-to-mapi-properties.md)

