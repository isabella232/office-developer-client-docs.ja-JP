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
# <a name="attachment-tables"></a>添付ファイル テーブル

**適用対象**: Outlook 
  
添付ファイル テーブルには、すべての送信されたメッセージや、メッセージは、コンポジションに関連付けられている添付ファイルのオブジェクトに関する情報が含まれています。 
  
テーブルには、メッセージの[IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドを呼び出すことによって保存されている添付ファイルだけが含まれます。 添付ファイル テーブルはメッセージ ストア プロバイダーによって実装され、クライアント アプリケーションおよびトランスポート プロバイダーによって使用されます。 
  
次のいずれかを呼び出すことによって、添付ファイル テーブルにアクセスできます。
  
- [IMessage::GetAttachmentTable](imessage-getattachmenttable.md)
    
- [IMAPIProp::OpenProperty](imapiprop-openproperty.md)、 **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) のプロパティを要求します。
    
添付ファイル テーブルでは、動的です。
  
メッセージ ストア プロバイダーは、その添付ファイル テーブルの並べ替えをサポートする必要はありません。 描画位置の順序でテーブルを表示する必要があります並べ替えがサポートされていない場合、 **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) のプロパティです。
  
メッセージ ストア プロバイダーも、添付ファイル テーブルの制限をサポートするために必要ありません。 制限をサポートしていないプロバイダーでは、 [IMAPITable::Restrict](imapitable-restrict.md)と[IMAPITable::FindRow](imapitable-findrow.md)の実装から MAPI_E_NO_SUPPORT を返します。
  
添付ファイル テーブル小さいこともあります。必要な列のセットでは、のみ 4 つの列があります。
  
- **PR_ATTACH_NUM**([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) 
    
- **PR_INSTANCE_KEY**([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) 
    
- **PR_RECORD_KEY**([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) 
    
- **PR_RENDERING_POSITION**
    
 **PR_ATTACH_NUM**は nontransmittable であるため、メッセージ内の添付ファイルを一意に識別する値を含んでいます。 このプロパティは、テーブルの行に、インデックスとしてよく使用されます。 **PR_ATTACH_NUM**には、短い寿命です。添付ファイルを含むメッセージを開いている間のみ有効です。 添付ファイル テーブルが開いている限り一定に保つには、その値が保証されます。 
  
 ほぼすべてのテーブルでは、 **PR_INSTANCE_KEY**が必要です。 特定の行を一意に識別に使用されます。 
  
 **PR_RECORD_KEY**は、比較のためのオブジェクトを一意に識別する通常使用されます。 **PR_RECORD_KEY**は**PR_ATTACH_NUM**とは異なり、長期的なエントリ id と同じスコープを持つメッセージが閉じられ、再オープン後も使用可能で有効なを維持します。 MAPI でのレコードのキーの使用に関する詳細については、 [MAPI の記録と検索キー](mapi-record-and-search-keys.md)を参照してください。
  
 **PR_RENDERING_POSITION**では、リッチ テキスト メッセージに添付ファイルを表示する方法を示します。 または-1 (0 xffffffff)、メッセージ内で添付ファイルを表示されないことを示す 0 が相殺される ([PidTagBody](pidtagbody-canonical-property.md)) である**PR_BODY**プロパティに格納されているメッセージの内容の最初の文字で、文字単位のオフセットを設定することができます。すべてのテキストです。 **PR_RENDERING_POSITION**を設定しないとは、また、オプションです。 
  
描画位置を指定して、添付ファイル テーブルが並べ替えられて、メッセージ ストア プロバイダーは符号付きの値 (PT_LONG) として扱います。 したがって、-1 のレンダリング位置を持つ添付ファイルは、有効なオフセットを反映するためのレンダリング位置を持つ添付ファイルの前に並べ替えられます。 
  
テキスト形式のメッセージの添付ファイルのレンダリングの詳細については、[テキスト形式の添付ファイルのレンダリング](rendering-an-attachment-in-plain-text.md)を参照してください。 
  
添付ファイルをリッチ テキスト形式 (RTF) などの書式設定されたテキストのレンダリング方法の詳細については、 [rtf 形式のテキストの添付ファイルのレンダリング](rendering-an-attachment-in-rtf-text.md)を参照してください。
  
メッセージ ストア プロバイダーよくは、添付ファイル テーブルでは簡単に計算または取得するためのプロパティは次のとおりです。
  
|||
|:-----|:-----|
|**PR_ATTACH_ENCODING**([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md))  <br/> |**PR_ATTACH_EXTENSION**([PidTagAttachExtension](pidtagattachextension-canonical-property.md))  <br/> |
|**PR_ATTACH_FILENAME**([PidTagAttachFilename](pidtagattachfilename-canonical-property.md))  <br/> |**PR_ATTACH_LONG_FILENAME**([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md))  <br/> |
|**PR_ATTACH_PATHNAME**([PidTagAttachPathname](pidtagattachpathname-canonical-property.md))  <br/> |**PR_ATTACH_LONG_PATHNAME**([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md))  <br/> |
|**PR_ATTACH_METHOD**([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))  <br/> |**PR_ATTACH_TAG**([PidTagAttachTag](pidtagattachtag-canonical-property.md))  <br/> |
|**PR_CREATION_TIME**([PidTagCreationTime](pidtagcreationtime-canonical-property.md))  <br/> |**PR_ATTACH_TRANSPORT_NAME**([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md))  <br/> |
|**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_LAST_MODIFICATION_TIME**([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))  <br/> |
   
## <a name="see-also"></a>関連項目

- [MAPI テーブル](mapi-tables.md)

