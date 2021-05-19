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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7a3ae7db1fb97e97f7d0939b67f139af62477bf7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355266"
---
# <a name="pidtagrecordkey-canonical-property"></a>PidTagRecordKey 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
特定のオブジェクトの一意のバイナリと同等の識別子を含む。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_RECORD_KEY  <br/> |
|識別子:  <br/> |0x0FF9  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |ID プロパティ  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティを使用すると、コンテンツ テーブル内の行の検索など、オブジェクトへの参照を簡単に検索できます。 このプロパティは、オブジェクトを開くのに使用できません。その目的のためにエントリ識別子を使用します。
  
添付ファイルサブオブジェクトは、このプロパティによってメッセージ内で一意に識別する必要があります。 この識別子は、メッセージを閉じて再び開いた後も同じ状態を続け続け保証される唯一の添付ファイルの特性です。 ストア プロバイダーは、この保証を保証するために、セッション間でこのプロパティを保持する必要があります。
  
フォルダーの場合、このプロパティには、フォルダー階層テーブルで使用されるキーが含まれます。 通常、これはプロパティ ([PidTagEntryId](pidtagentryid-canonical-property.md) **)** プロパティPR_ENTRYID同じ値です。
  
メッセージ ストアの場合、このプロパティは PR_STORE_RECORD_KEY **(** [PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md)) プロパティと同じです。
  
メッセージ ストア オブジェクトでは、このプロパティは、すべてのストア プロバイダーで一意である必要があります。 これを行う方法の 1 つは、 **ストアの PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) プロパティの値 (プロバイダーの種類に固有) と [、GUID](guid.md) 構造または特定のメッセージ ストア固有の他の値を組み合わせることです。 
  
このプロパティは [、IMAPIProp::SaveChanges](imapiprop-getprops.md) メソッドの最初の呼び出しに続く [IMAPIProp::GetProps](imapiprop-savechanges.md) メソッドを通じて常に使用できます。 一部のプロバイダーでは、インスタンス化の直後に使用できます。 
  
クライアントまたはサービス プロバイダーは、memcmp を使用して、このプロパティの値を比較できます。 これは、エントリ識別子の値では使用できない。 ただし、このプロパティは、同じメッセージ ストアまたはアドレス帳コンテナー内で一意である必要があります。異なるコンテナーの 2 つのオブジェクトは、このプロパティの同じ値を持つ場合があります。
  
レコード キーと検索キーの違いは、レコード キーがオブジェクトに固有であるのに対し、検索キーを他のオブジェクトにコピーできるという違いがあります。 たとえば、オブジェクトの 2 つのコピーに同じ値[(PidTagSearchKey)](pidtagsearchkey-canonical-property.md)PR_SEARCH_KEYを指定できますが、このプロパティには異なる値が必要です。
  
次の表は、このプロパティ 、PR_ENTRYID **、** PR_SEARCH_KEY ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))**の間の** 重要な違いを示しています。 
  
|**特性**|**PR_ENTRYID**|**PR_RECORD_KEY**|**PR_SEARCH_KEY**|
|:-----|:-----|:-----|:-----|
|添付ファイル オブジェクトに必須  <br/> |いいえ  <br/> |はい  <br/> |いいえ  <br/> |
|フォルダー オブジェクトに必須  <br/> |はい  <br/> |はい  <br/> |いいえ  <br/> |
|メッセージ ストア オブジェクトで必須  <br/> |はい  <br/> |はい  <br/> |いいえ  <br/> |
|状態オブジェクトで必須  <br/> |はい  <br/> |いいえ  <br/> |いいえ  <br/> |
|クライアントによる折りたたみ可能  <br/> |いいえ  <br/> |いいえ  <br/> |はい  <br/> |
|SaveChanges への呼び出し **の前に使用可能** <br/> |多分  <br/> |多分  <br/> |メッセージ はい その他 多分  <br/> |
|コピー操作で変更された  <br/> |はい  <br/> |はい  <br/> |いいえ  <br/> |
|コピー後にクライアントが変更可能  <br/> |いいえ  <br/> |いいえ  <br/> |はい  <br/> |
|..内で一意です。  <br/> |ワールド全体  <br/> |プロバイダー インスタンス  <br/> |ワールド全体  <br/> |
|バイナリ比較 (memcmp と同様)  <br/> |いいえ -- **IMAPISupport:: CompareEntryIDs を使用する** <br/> |はい  <br/> |はい  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージ オブジェクトと添付ファイル オブジェクトを処理します。
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> ユーザー、連絡先、グループ、およびリソースの一覧のプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

