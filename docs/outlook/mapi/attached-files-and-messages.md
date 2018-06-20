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
ms.openlocfilehash: 489930b35d24d2691c9b9fbb59b0fa95707a0618
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799675"
---
# <a name="attached-files-and-messages"></a>添付ファイルとメッセージ

  
  
**適用されます**: Outlook 
  
メッセージの内容をエンコード中に TNEF で MIME を使用すると、すべての添付ファイルのプロパティとコンテンツが TNEF ストリームでは。 自体 TNEF は、TNEF なしの MIME のエンコード、Winmail.dat という名前の 1 つ、バイナリ添付ファイルです。 
  
TNEF に MIME を使用する場合、添付ファイルは、MIME メッセージのコンテンツの一部として送信されます。 ファイル名は、添付ファイルの*コンテンツ タイプ*ヘッダーに*name*パラメーターに配置されます。 添付ファイルの文字セットは、*コンテンツ タイプ*に*文字セット*パラメーターに配置します。コンテンツ転送エンコードは、全体の添付ファイルのコンテンツをスキャンすることによって決定されます。 URL の添付ファイルは、特別に処理されます。 
  
- 場合は、添付ファイルは、URL (拡張子を持つ添付ファイルです。)、URL 内に定義されているアクセス ・ モードは、匿名 FTP と、外部メッセージとしてエンコードされ、ファイル (URL) の内容は、外部のメッセージのヘッダーにコピーされます。 *コンテンツの種類: メッセージ/外部ボディ; アクセスの種類 = つけ加え* (コンテンツ転送エンコード: 7 ビットであると見なされます)。 
    
- 7 ビットの文字が見つかるし、行を超えると 140 文字の長さでない、だけの場合、添付ファイルは、ASCII テキストです。 *コンテンツの種類: テキスト/形式です。文字セット、us-ascii コンテンツ転送エンコードを =: 7 ビット* 
    
- 場合か、長い行を 25% に 8 ビットの文字が見つかると、添付ファイルのコンテンツがテキストで、文字セットは、ロケールによって決まります。 ISO 8859 の標準で定義されている文字セットから選択する必要があります。 *コンテンツの種類: テキスト/形式; charset = ISO 8859-1* (例) 
    
     *コンテンツ転送エンコード: 引用符で囲まれた印刷可能な* 
    
- 25% 以上の文字には、上位ビットが設定がある場合、添付ファイルはバイナリです。 Base64 アルゴリズムを使用してエンコードされます。 *コンテンツの種類: アプリケーションまたはオクテット ストリーム* (既定ではファイルの拡張子に基づいて) 
    
     * Base64 のコンテンツ転送エンコード: * 
    
送信メッセージは、コンテンツの種類必要がありますから派生するファイル名の 3 文字の拡張子。 システム レジストリにこのマッピングが存在します。下で文字列値の名前は「コンテンツの種類」が定義されている場合、MIME コンテンツの種類を示す。 この例では、TIFF イメージ ファイルです。
  
HKEY_LOCAL_MACHINE\
  
Software\
  
Microsoft\
  
Classes\
  
.tif
  
コンテンツ タイプ =「画像/tiff」
  
ファイル拡張子のマッピングがない場合、既定の*アプリケーションまたはオクテット*ストリームを使用してください。 
  
受信したメッセージ、添付ファイルのコンテンツの種類が常に MAPI プロパティの**PR_ATTACH_MIME_TAG** ([PidTagAttachMimeTag](pidtagattachmimetag-canonical-property.md)) にコピーしてください。 **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) と**PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) のプロパティ] でコンテンツ タイプにマップされている拡張機能を使用する必要がある場合でも、添付ファイルのファイル名が定義されると、.
  
*Name*パラメーターは、RFC 821 で正式に廃止されます。 標準の出現に伴い、マイクロソフトは接続されているファイル名の代替マッピングを指定することを検討します。 
  
として添付されたメッセージの送信が送信されます * コンテンツの種類: メッセージと rfc822 * 添付されたメッセージ内のメッセージは、適切な場所で、エンコードを再帰的にします。 受信メッセージのコンテンツ部分を*コンテンツの種類: マルチパート/ダイジェスト*埋め込みメッセージにマッピングされます。 
  
メッセージの内容をエンコード中に TNEF を uuencode を使用すると、すべての添付ファイルのプロパティとコンテンツが TNEF ストリームでは。 自体 TNEF は、TNEF なしでも、Uuencode のエンコード、Winmail.dat という名前の 1 つのバイナリ添付ファイルです。
  
TNEF なし uuencode を使用する場合は、すべての添付ファイルがバイナリ形式とエンコードされていない、次のメッセージのテキストとして扱われます。 ファイル名は、uuencode ヘッダー内に存在します。
  
 0755 Winmail.dat を開始します。 
  
 . データ. 
  
 end 
  
添付されたメッセージは、メッセージ テキストに textized します。 添付されたメッセージの階層は常に平坦化します。添付されたメッセージ内のメッセージが引き出されている最上位レベルにします。
  
埋め込み OLE オブジェクトは破棄されます。
  
添付ファイルのレンダリング位置は、 **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) のプロパティを使用して、TNEF でそのままで送信されます。 TNEF を使用しない場合に失われます。 (TNEF が存在しない場合を含む) のレンダリング位置で受信した添付ファイルには、その描画位置の設定は、0 xffffffff にないメッセージのテキスト内の位置があります。
  
## <a name="see-also"></a>関連項目



[MAPI プロパティにインターネットのメール属性のマッピング](mapping-of-internet-mail-attributes-to-mapi-properties.md)

