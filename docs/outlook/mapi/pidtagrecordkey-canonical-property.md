---
title: PidTagRecordKey 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecordKey
api_type:
- COM
ms.assetid: a12fb9a2-799d-4112-b26c-4b2854c47cc2
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7a3ae7db1fb97e97f7d0939b67f139af62477bf7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355266"
---
# <a name="pidtagrecordkey-canonical-property"></a>PidTagRecordKey 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
特定のオブジェクトの一意のバイナリ比較識別子を含みます。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_RECORD_KEY  <br/> |
|識別子:  <br/> |0x0ff9  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |ID プロパティ  <br/> |
   
## <a name="remarks"></a>解説

このプロパティを設定すると、コンテンツテーブル内の行を検索するなど、オブジェクトへの参照を簡単に見つけることができます。 このプロパティを使用してオブジェクトを開くことはできません。その目的のためにエントリ識別子を使用します。
  
添付ファイルサブオブジェクトは、このプロパティでメッセージ内で一意に識別する必要があります。 この識別子は、メッセージを閉じてからもう一度開いた後に維持することが保証されている唯一の添付ファイルの特性です。 ストアプロバイダーは、この保証を確実にするために、セッション間でこのプロパティを保持する必要があります。
  
フォルダーの場合、このプロパティには、フォルダー階層テーブルで使用されるキーが含まれています。 通常、これは**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティで提供される値と同じです。
  
メッセージストアの場合、このプロパティは**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md)) プロパティと同じです。
  
メッセージストアオブジェクトでは、このプロパティはすべてのストアプロバイダーで一意である必要があります。 そのための方法の1つとして、ストアの**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) プロパティの値を、 [GUID](guid.md)構造または特定のメッセージストアに固有の他の値と組み合わせて使用することができます。 
  
このプロパティは、imapiprop [:: SaveChanges](imapiprop-savechanges.md)メソッドを最初に呼び出した後、 [imapiprop:: GetProps](imapiprop-getprops.md)メソッドを使用して常に使用できます。 プロバイダーによっては、インスタンス化の直後に使用できるようにすることができます。 
  
クライアントまたはサービスプロバイダーは、memcmp を使用してこのプロパティの値を比較できます。 これはエントリ識別子の値には使用できません。 ただし、このプロパティは同じメッセージストアまたはアドレス帳コンテナー内で一意であることが保証されています。異なるコンテナーからの2つのオブジェクトは、このプロパティの値を持つことができます。
  
record キーと検索キーの違いの1つは、record キーがオブジェクトに固有であるのに対して、検索キーは他のオブジェクトにコピーできるということです。 たとえば、オブジェクトの2つのコピーは同じ**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) 値を持つことができますが、このプロパティには異なる値を指定する必要があります。
  
次の表は、 **PR_ENTRYID**、 **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) およびこのプロパティの重要な相違点をまとめたものです。 
  
|**特性**|**PR_ENTRYID**|**PR_RECORD_KEY**|**PR_SEARCH_KEY**|
|:-----|:-----|:-----|:-----|
|attachment オブジェクトに必要  <br/> |いいえ  <br/> |はい  <br/> |いいえ  <br/> |
|folder オブジェクトで必要  <br/> |はい  <br/> |はい  <br/> |いいえ  <br/> |
|メッセージストアオブジェクトに必要  <br/> |はい  <br/> |はい  <br/> |いいえ  <br/> |
|状態オブジェクトに必要です  <br/> |はい  <br/> |いいえ  <br/> |いいえ  <br/> |
|クライアントによるのが可能  <br/> |いいえ  <br/> |いいえ  <br/> |はい  <br/> |
|**SaveChanges**を呼び出す前に使用できます。 <br/> |考え  <br/> |考え  <br/> |[その他のメッセージ]  <br/> |
|コピー操作で変更  <br/> |はい  <br/> |はい  <br/> |いいえ  <br/> |
|コピー後にクライアントによって変更される  <br/> |いいえ  <br/> |いいえ  <br/> |はい  <br/> |
|一意の範囲  <br/> |世界全体  <br/> |プロバイダーインスタンス  <br/> |世界全体  <br/> |
|二項比較 (memcmp と同じ)  <br/> |No-- **imapisupport:: compareentryids**を使用します。 <br/> |はい  <br/> |はい  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルオブジェクトを処理します。
    
[[OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> ユーザー、連絡先、グループ、およびリソースのリストのプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 代替名としてリストされているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

