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
# <a name="attachment-tables"></a>添付ファイル テーブル

**適用対象**: Outlook 2013 | Outlook 2016 
  
添付ファイル テーブルには、送信済みメッセージまたは構成下のメッセージに関連付けられているすべての添付ファイル オブジェクトに関する情報が含まれています。 
  
メッセージの [IMAPIProp::SaveChanges](imapiprop-savechanges.md) メソッドへの呼び出しによって保存された添付ファイルだけがテーブルに含まれます。 添付ファイル テーブルは、メッセージ ストア プロバイダーによって実装され、クライアント アプリケーションとトランスポート プロバイダーによって使用されます。 
  
添付ファイル テーブルにアクセスするには、次のいずれかを呼び出します。
  
- [IMessage::GetAttachmentTable](imessage-getattachmenttable.md)
    
- [IMAPIProp::OpenProperty](imapiprop-openproperty.md)、 プロパティ **(** [PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) PR_MESSAGE_ATTACHMENTSを要求します。
    
添付ファイル テーブルは動的です。
  
メッセージ ストア プロバイダーは、添付ファイル テーブルでの並べ替えをサポートする必要はありません。 並べ替えがサポートされていない場合は、テーブルをレンダリング位置 (PR_RENDERING_POSITION **(** [PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) プロパティで順番に表示する必要があります。
  
メッセージ ストア プロバイダーも、添付ファイル テーブルの制限をサポートする必要はありません。 制限をサポートしていないプロバイダーは [、IMAPITable::Restrict](imapitable-restrict.md) MAPI_E_NO_SUPPORT [IMAPITable::FindRow](imapitable-findrow.md)の実装から、この値を返します。
  
添付ファイル テーブルは小さい場合があります。必須の列セットには 4 つの列しか含めありません。
  
- **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) 
    
- **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) 
    
- **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) 
    
- **PR_RENDERING_POSITION**
    
 **PR_ATTACH_NUM** は非送信可能で、メッセージ内の添付ファイルを一意に識別するための値を含む。 このプロパティは、多くの場合、テーブルの行のインデックスとして使用されます。 **PR_ATTACH_NUM** の寿命が短い。添付ファイルを含むメッセージが開いている間のみ有効です。 添付ファイル テーブルが開いている限り、その値は一定に保たれ保証されます。 
  
 **PR_INSTANCE_KEY、** ほぼすべてのテーブルで必要です。 特定の行を一意に識別するために使用されます。 
  
 **PR_RECORD_KEY** は、比較のためにオブジェクトを一意に識別するために一般的に使用されます。 PR_ATTACH_NUM **とは** 異 **PR_RECORD_KEYは、** 長期エントリ識別子と同じスコープを持つ必要があります。メッセージを閉じて再度開いた後でも、使用可能で有効なままです。 MAPI でのレコード キーの使用の詳細については、「MAPI レコードと [検索キー」を参照してください](mapi-record-and-search-keys.md)。
  
 **PR_RENDERING_POSITION** リッチ テキスト メッセージに添付ファイルを表示する方法を示します。 PR_BODY ([PidTagBody](pidtagbody-canonical-property.md)) プロパティに格納されているメッセージ コンテンツの最初の文字を **オフセット 0** または -1 (0xFFFFFFFF) に設定して、メッセージ テキスト内で添付ファイルを表示しなきことを示します。 また **、PR_RENDERING_POSITION** 設定しない場合もオプションです。 
  
添付ファイル テーブルをレンダリング位置で並べ替えた場合、メッセージ ストア プロバイダーは署名された値 (PT_LONG) として処理します。 したがって、レンダリング位置が -1 の添付ファイルは、有効なオフセットを反映するレンダリング位置を持つ添付ファイルの前に並べ替えされます。 
  
プレーン テキスト メッセージで添付ファイルをレンダリングする方法の詳細については、「プレーン テキストで [添付ファイルをレンダリングする」を参照してください](rendering-an-attachment-in-plain-text.md)。 
  
リッチ テキスト形式 (RTF) などの書式設定されたテキストで添付ファイルをレンダリングする方法については、「RTF テキストで添付ファイルをレンダリングする」 [を参照してください](rendering-an-attachment-in-rtf-text.md)。
  
メッセージ ストア プロバイダーの一般的なプロパティの中には、計算や取得が容易なので、添付ファイル テーブルに含まれるものがあります。
  
|||
|:-----|:-----|
|**PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md))  <br/> |**PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md))  <br/> |
|**PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md))  <br/> |**PR_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md))  <br/> |
|**PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md))  <br/> |**PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md))  <br/> |
|**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))  <br/> |**PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md))  <br/> |
|**PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))  <br/> |**PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md))  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))  <br/> |
   
## <a name="see-also"></a>関連項目

- [MAPI テーブル](mapi-tables.md)

