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
ms.openlocfilehash: 4aa800b504e7ffb07d94ace6d8dc30c1463ed637
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318138"
---
# <a name="attachment-tables"></a>添付ファイル テーブル

**適用対象**: Outlook 2013 | Outlook 2016 
  
添付ファイルテーブルには、送信されたメッセージまたは複合下のメッセージに関連付けられているすべての attachment オブジェクトに関する情報が含まれています。 
  
表には、メッセージの[imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドへの呼び出しによって保存された添付ファイルのみが含まれています。 添付ファイルテーブルは、メッセージストアプロバイダーによって実装され、クライアントアプリケーションとトランスポートプロバイダーによって使用されます。 
  
添付ファイルテーブルには、次のどちらかを呼び出すことによってアクセスできます。
  
- [IMessage::GetAttachmentTable](imessage-getattachmenttable.md)
    
- [imapiprop:: openproperty](imapiprop-openproperty.md)。 **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) プロパティを要求しています。
    
添付ファイルテーブルは動的です。
  
メッセージストアプロバイダーは、添付ファイルテーブルでの並べ替えをサポートする必要はありません。 並べ替えがサポートされていない場合は、 **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) プロパティを使用して、表を表示する順序を指定する必要があります。
  
メッセージストアプロバイダーは、添付ファイルテーブルの制限をサポートする必要もありません。 制限をサポートしないプロバイダーは、 [IMAPITable:: Restrict](imapitable-restrict.md)と[IMAPITable:: FindRow](imapitable-findrow.md)の実装から MAPI_E_NO_SUPPORT を返します。
  
添付ファイルテーブルは小規模にすることができます。必要な列セットには、次の4つの列のみがあります。
  
- **PR_ATTACH_NUM**([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) 
    
- **PR_INSTANCE_KEY**([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) 
    
- **PR_RECORD_KEY**([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) 
    
- **PR_RENDERING_POSITION**
    
 **PR_ATTACH_NUM**はノン、メッセージ内の添付ファイルを一意に識別する値を格納します。 このプロパティは、多くの場合、テーブルの行のインデックスとして使用されます。 **PR_ATTACH_NUM**の寿命は短くなります。添付ファイルを含むメッセージが開いている場合にのみ有効です。 このプロパティの値は、添付ファイルテーブルが開いている間は常に一定であることが保証されます。 
  
 **PR_INSTANCE_KEY**は、ほぼすべてのテーブルで必要です。 このメソッドは、特定の行を一意に識別するために使用されます。 
  
 **PR_RECORD_KEY**は、通常、比較目的でオブジェクトを一意に識別するために使用されます。 **PR_ATTACH_NUM**とは異なり、 **PR_RECORD_KEY**には長期間のエントリ id と同じスコープがあります。メッセージが閉じられてからもう一度開かれた後でも、利用可能な状態になります。 mapi でのレコードキーの使用の詳細については、「 [mapi レコードおよび検索キー](mapi-record-and-search-keys.md)」を参照してください。
  
 **PR_RENDERING_POSITION**は、添付ファイルがリッチテキストメッセージでどのように表示されるかを示します。 **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) プロパティに格納されているメッセージの内容の最初の文字をオフセット0、または-1 (0xffffffff) に設定して、添付ファイルをメッセージ内にレンダリングしないことを示す、文字単位のオフセットに設定できます。文字列を入力します。 **PR_RENDERING_POSITION**を設定しないこともオプションです。 
  
添付ファイルテーブルがレンダリング位置で並べ替えられている場合、メッセージストアプロバイダーはそれを符号付きの値 (PT_LONG) として扱います。 そのため、-1 のレンダリング位置の添付ファイルは、有効なオフセットを反映するレンダリング位置に添付される前に並べ替えられます。 
  
テキスト形式の添付ファイルのレンダリングの詳細については、「[添付ファイルをテキスト形式でレンダリング](rendering-an-attachment-in-plain-text.md)する」を参照してください。 
  
リッチテキスト形式 (rtf) など、書式設定されたテキストで添付ファイルをレンダリングする方法については、「[添付ファイルを rtf テキスト形式でレンダリングする](rendering-an-attachment-in-rtf-text.md)」を参照してください。
  
一部のプロパティメッセージストアプロバイダーは、次のように簡単に計算または取得できるため、添付ファイルテーブルに含まれています。
  
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

