---
title: PidTagRecordKey の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: bd655c6245d25948d1dea1daace6a0644b47e378
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803313"
---
# <a name="pidtagrecordkey-canonical-property"></a>PidTagRecordKey の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
特定のオブジェクトのバイナリ比較が可能な一意の識別子が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_RECORD_KEY  <br/> |
|識別子:  <br/> |0x0FF9  <br/> |
|データを入力します。  <br/> |PT_BINARY  <br/> |
|領域:  <br/> |ID プロパティ  <br/> |
   
## <a name="remarks"></a>備考

このプロパティには、内容のテーブル内の行を検索するなどのオブジェクトへの参照を検索が容易になります。 このプロパティは、オブジェクトを開くには使用できません。目的のためのエントリ id を使用します。
  
添付ファイルのサブオブジェクトは、このプロパティによって、メッセージ内で一意に識別する必要があります。 この識別子は、常に同じメッセージが閉じられ、再オープン後に保証されるだけの添付ファイル特性です。 ストア プロバイダーは、この保証を確認するのにはセッション間でこのプロパティを保持する必要があります。
  
フォルダーは、このプロパティには、フォルダーの階層テーブルで使用されるキーが含まれています。 通常これは、 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティによって提供されるものと同じ値です。
  
メッセージ ・ ストアのこのプロパティでは、 **PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md)) のプロパティと同じです。
  
メッセージ ストア オブジェクトでこのプロパティは、一意なすべてのストア プロバイダーで。 これを行う方法の 1 つでは、 [GUID](guid.md)構造体、またはその他の値が特定のメッセージ ストアに固有のストア (そのプロバイダーの種類に固有) の**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) プロパティの値を結合します。 
  
このプロパティは、常に[IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドへの最初の呼び出しの後、 [IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを使用します。 一部のプロバイダーを使用する利用可能なインスタンス化後すぐに。 
  
クライアントまたはサービス プロバイダーでは、ためを使用して、このプロパティの値を比較できます。 エントリの識別子の値のことではありません。 ただし、このプロパティが保証される、同じメッセージ ・ ストア内で一意であるか、アドレス帳コンテナーです。別のコンテナーからの 2 つのオブジェクトには、このプロパティの値と同じことができます。
  
レコードおよび検索キーの 1 つの違いは、レコードのキー、オブジェクトに固有の他のオブジェクトに検索キーをコピーすることができますが、です。 などのオブジェクトの 2 つのコピーは同じ**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) の値を持つことができますが、このプロパティに異なる値を持つ必要があります。
  
**PR_ENTRYID**、 **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))、このプロパティの間で重要な相違点を次の表にまとめます。 
  
|**特性**|**PR_ENTRYID**|**PR_RECORD_KEY**|**PR_SEARCH_KEY**|
|:-----|:-----|:-----|:-----|
|添付ファイルのオブジェクトで必要な  <br/> |いいえ  <br/> |はい  <br/> |いいえ  <br/> |
|フォルダー オブジェクトで必要な  <br/> |はい  <br/> |はい  <br/> |いいえ  <br/> |
|メッセージ ストア オブジェクトで必要な  <br/> |はい  <br/> |はい  <br/> |いいえ  <br/> |
|状態オブジェクトで必要な  <br/> |はい  <br/> |いいえ  <br/> |いいえ  <br/> |
|クライアントで作成可能  <br/> |いいえ  <br/> |いいえ  <br/> |はい  <br/> |
|**Savechanges メソッド**の呼び出しの前に使用可能です <br/> |かもしれません  <br/> |かもしれません  <br/> |メッセージは他の人をたぶんはい  <br/> |
|コピー操作で変更  <br/> |はい  <br/> |はい  <br/> |いいえ  <br/> |
|コピー後にクライアントによって変更可能です  <br/> |いいえ  <br/> |いいえ  <br/> |はい  <br/> |
|内で重複しています.  <br/> |全体の世界  <br/> |プロバイダーのインスタンス  <br/> |全体の世界  <br/> |
|バイナリ (ため) と同じように匹敵します。  <br/> |いいえ--を使用して**IMAPISupport:: CompareEntryIDs** <br/> |はい  <br/> |はい  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルのオブジェクトを処理します。
    
[[MS OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> プロパティとユーザー、連絡先、グループ、およびリソースのリストの操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

