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
# <a name="attached-files-and-messages"></a>添付ファイルとメッセージ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージの内容をエンコードする際に、tnef の MIME を使用する場合は、すべての添付ファイルのプロパティとコンテンツが tnef ストリームに含まれています。 tnef 自体は、tnef なしで記述された、winmail.dat という名前の単一のバイナリ添付ファイルです。 
  
mime が TNEF なしで使用される場合、添付ファイルは mime メッセージコンテンツのパーツとして送信されます。 filename は、添付ファイルの*content-type*ヘッダーの*name*パラメーターに配置されます。 添付ファイルの文字セットは、*コンテンツタイプ*の*charset*パラメーターに配置されます。また、コンテンツ転送エンコードは、添付ファイルコンテンツ全体をスキャンすることによって決定されます。 URL の添付ファイルは、特別に扱われます。 
  
- 添付ファイルが URL (拡張子が付いた添付ファイル) の場合。url) を指定し、それに定義されているアクセスモードが匿名 FTP である場合は、外部メッセージとしてエンコードされ、ファイル (URL) の内容が外部メッセージのヘッダーにコピーされます。 *コンテンツタイプ: メッセージ/外部-本文、アクセスタイプ = 無効化-ftp* (コンテンツ転送エンコード: 7bit が想定されています。) 
    
- 7ビット文字のみが検索され、長さが140文字を超える行がない場合、添付ファイルは ASCII テキストになります。 *コンテンツタイプ: text/plain。charset = us-ascii コンテンツ転送エンコード: 7bit* 
    
- long 行または最大 25% の8ビット文字が検出された場合、添付ファイルのコンテンツはテキストであり、文字セットはロケールによって決定されます。 ISO 規格8859で定義されている文字セットから選択する必要があります。 *コンテンツタイプ: text/plain、charset = ISO-8859-1* (例:) 
    
     *Content-Transfer-Encoding: quoted-printable* 
    
- 25% 以上の文字の上位ビットが設定されている場合、添付ファイルはバイナリになります。 Base64 アルゴリズムを使用してエンコードされます。 *コンテンツタイプ: application/オクテットストリーム* (既定では、ファイル拡張子に基づいて) 
    
     * コンテンツ転送エンコード: base64 * 
    
送信メッセージの場合、コンテンツタイプはファイル名の3文字の拡張子から派生する必要があります。 このマッピングはシステムレジストリに存在します。MIME コンテンツタイプが定義されている場合は、"コンテンツタイプ" という名前の文字列値があります。 TIFF イメージファイルの例を次に示します。
  
HKEY_LOCAL_MACHINE \
  
ソフトウェア
  
製
  
クラス
  
.tif
  
コンテンツタイプ = "image/tiff"
  
ファイル拡張子がマッピングされていない場合は、既定の*アプリケーション/オクテット*ストリームを使用する必要があります。 
  
受信メッセージの場合、添付ファイルのコンテンツタイプは常に MAPI プロパティ**PR_ATTACH_MIME_TAG** ([PidTagAttachMimeTag](pidtagattachmimetag-canonical-property.md)) にコピーする必要があります。 添付ファイルに対してファイル名が定義されている場合でも、 **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) および**PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) プロパティで、コンテンツタイプによってマッピングされた拡張子を使用する必要があります。.
  
*name*パラメーターは、RFC 821 によって正式に非推奨になりました。 標準が進化するにつれて、Microsoft は添付ファイル名の代替マッピングを指定することを検討します。 
  
送信添付メッセージは、* content-type として送信されます: message/rfc822 * 添付メッセージ内のメッセージは、適切な場所に再帰的にエンコードされます。 コンテンツタイプの受信メッセージコンテンツパーツ *: マルチパート/ダイジェスト*は、埋め込みメッセージにもマップされます。 
  
メッセージの内容をエンコードする際に、tnef を含む uuencode が使用されている場合、すべての添付ファイルのプロパティとコンテンツが tnef ストリームに含まれます。 tnef 自体は、tnef なしで記述された、winmail.dat という名前の単一のバイナリ添付ファイルです。
  
TNEF が使用されていない場合、添付ファイルはすべて、メッセージテキストの後、バイナリと uuencode として処理されます。 ファイル名は、uuencode ヘッダーに表示されます。
  
 開始 0755 winmail.dat 
  
 ...データ... 
  
 end 
  
添付されたメッセージは、メッセージテキストに textized ます。 添付されたメッセージの階層は常に平坦化されます。つまり、添付されたメッセージ内のメッセージは最上位レベルにプルアウトされます。
  
埋め込み OLE オブジェクトは破棄されます。
  
添付ファイルのレンダリング位置は、TNEF のプロパティ**PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) を使用して、文字どおり転送されます。 TNEF が使用されていない場合は、失われます。 レンダリング位置のない受信添付ファイル (TNEF がない場合を含む) は、レンダリング位置が0xffffffff に設定されます。つまり、メッセージテキストに位置がありません。
  
## <a name="see-also"></a>関連項目



[インターネットメールの属性から MAPI プロパティへのマッピング](mapping-of-internet-mail-attributes-to-mapi-properties.md)

