---
title: PidTagSearchKey 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: fcab369a-a1f4-4425-a272-e35046914a4d
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 9e6b9ddf37c1db8ea28ae2f82caed2a487e551e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345466"
---
# <a name="pidtagsearchkey-canonical-property"></a>PidTagSearchKey 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
検索の相関オブジェクトを識別する2つの比較可能なキーが含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SEARCH_KEY  <br/> |
|識別子:  <br/> |0x300b  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |ID プロパティ  <br/> |
   
## <a name="remarks"></a>解説

このプロパティは、メッセージのコピーなどの関連オブジェクトのトレースを提供し、重複した受信者などの不必要な出現を検索しやすくします。
  
MAPI では、メッセージの受信者の検索キーを作成するための特定のルールを使用します。 検索キーは、アドレスの種類 (大文字で表記)、コロン文字 ': '、標準形式の電子メールアドレス、および終端の null 文字を連結して形成されます。 ここでは、大文字と小文字が区別され、大文字と小文字が区別されないアドレスが大文字に変換されることを意味します。 これは、メッセージ間の相互関係を維持するために重要です。
  
message オブジェクトの場合、このプロパティは、メッセージの作成直後に[imapiprop:: GetProps](imapiprop-getprops.md)メソッドを通じて使用できます。 その他のオブジェクトの場合は、 [imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドを最初に呼び出した後に使用できます。 このプロパティは変更可能なので、 **SaveChanges**呼び出しが[imapiprop:: setprops](imapiprop-setprops.md)メソッドによって設定または変更された値をコミットするまでは、 **GetProps**経由で取得することはできません。 
  
プロファイルの場合、MAPI は、 **MUID_PROFILE_INSTANCE**というハードコードされたプロファイルセクションを furnishes します。このプロパティは、このプロパティを単一のプロパティとして使用します。 このキーは、作成されたすべてのプロファイル間で一意であることが保証されており、 **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)) プロパティよりも信頼性が高くなることがあります。たとえば、削除されて同じ名前で再作成されます。
  
次の表は、 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))、 **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))、およびこのプロパティの重要な相違点をまとめたものです。
  
|**特性**|PR_ENTRYID * * * *|PR_RECORD_KEY * * * *|PR_SEARCH_KEY * * * *|
|:-----|:-----|:-----|:-----|
|attachment オブジェクトに必要  <br/> |いいえ  <br/> |はい  <br/> |いいえ  <br/> |
|folder オブジェクトで必要  <br/> |はい  <br/> |はい  <br/> |いいえ  <br/> |
|メッセージストアオブジェクトに必要  <br/> |はい  <br/> |はい  <br/> |いいえ  <br/> |
|状態オブジェクトに必要です  <br/> |はい  <br/> |いいえ  <br/> |いいえ  <br/> |
|クライアントによるのが可能  <br/> |いいえ  <br/> |いいえ  <br/> |はい  <br/> |
|**SaveChanges**の前に使用可能 <br/> |プロバイダーの実装によって異なります。  <br/> |プロバイダーの実装によって異なります。  <br/> |メッセージの場合は、はい。 その他の場合は、プロバイダーの実装によって異なります。  <br/> |
|コピー操作で変更  <br/> |はい  <br/> |はい  <br/> |いいえ  <br/> |
|コピー後にクライアントによって変更可能  <br/> |いいえ  <br/> |いいえ  <br/> |はい  <br/> |
|一意の範囲  <br/> |世界全体  <br/> |プロバイダーインスタンス  <br/> |世界全体  <br/> |
|二項比較 (memcmp と同じ)  <br/> |No-- [imapisupport:: compareentryids](imapisupport-compareentryids.md)を使用します。 <br/> |はい  <br/> |はい  <br/> |
   
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



[PidTagResponsibility 標準プロパティ](pidtagresponsibility-canonical-property.md)
  
[PidTagStoreRecordKey 標準プロパティ](pidtagstorerecordkey-canonical-property.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

