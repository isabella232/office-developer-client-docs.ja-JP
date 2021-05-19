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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 9e6b9ddf37c1db8ea28ae2f82caed2a487e551e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345466"
---
# <a name="pidtagsearchkey-canonical-property"></a>PidTagSearchKey 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
検索の関連オブジェクトを識別するバイナリ比較可能なキーが含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SEARCH_KEY  <br/> |
|識別子:  <br/> |0x300B  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |ID プロパティ  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、メッセージ コピーなどの関連オブジェクトのトレースを提供し、重複する受信者などの不要な発生を見つけ出すのを容易にします。
  
MAPI は、メッセージ受信者の検索キーを作成するための特定のルールを使用します。 検索キーは、アドレスの種類 (大文字)、コロン文字 ':'、電子メール アドレスを標準形式で連結し、終端の null 文字を連結して形成されます。 ここでの標準の形式は、大文字と小文字を区別するアドレスが正しい場合に表示され、大文字と小文字を区別しないアドレスが大文字に変換されていることを意味します。 これは、メッセージ間の相関関係を保持する場合に重要です。
  
メッセージ オブジェクトの場合、このプロパティは、メッセージの作成直後に [IMAPIProp::GetProps](imapiprop-getprops.md) メソッドを使用して使用できます。 他のオブジェクトでは [、IMAPIProp::SaveChanges](imapiprop-savechanges.md) メソッドの最初の呼び出しに従って使用できます。 このプロパティは変更可能なので **、SaveChanges** 呼び出しが [IMAPIProp::SetProps](imapiprop-setprops.md)メソッドによって設定または変更された値をコミットするまで **、GetProps** を使用して取得することはできません。 
  
プロファイルの場合、MAPI は、このプロパティを **単** 一のプロパティとして、MUID_PROFILE_INSTANCE という名前のハードコードされたプロファイル セクションも提供します。 このキーは、これまでに作成されたプロファイル間で一意であることを保証され **、PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)) プロパティよりも信頼性が高く、たとえば、同じ名前で削除および再作成できます。
  
次の表に、PR_ENTRYID **(** [PidTagEntryId)](pidtagentryid-canonical-property.md)、PR_RECORD_KEY **(** [PidTagRecordKey)](pidtagrecordkey-canonical-property.md)、およびこのプロパティの重要な違いを示します。
  
|**特性**|PR_ENTRYID****|PR_RECORD_KEY****|PR_SEARCH_KEY****|
|:-----|:-----|:-----|:-----|
|添付ファイル オブジェクトに必須  <br/> |いいえ  <br/> |はい  <br/> |いいえ  <br/> |
|フォルダー オブジェクトに必須  <br/> |はい  <br/> |はい  <br/> |いいえ  <br/> |
|メッセージ ストア オブジェクトで必須  <br/> |はい  <br/> |はい  <br/> |いいえ  <br/> |
|状態オブジェクトで必須  <br/> |はい  <br/> |いいえ  <br/> |いいえ  <br/> |
|クライアントによる折りたたみ可能  <br/> |いいえ  <br/> |いいえ  <br/> |はい  <br/> |
|**SaveChanges の前に使用可能** <br/> |プロバイダーの実装によって異なります  <br/> |プロバイダーの実装によって異なります  <br/> |メッセージの場合は、はい。 その他の場合は、プロバイダーの実装によって異なります。  <br/> |
|コピー操作で変更された  <br/> |はい  <br/> |はい  <br/> |いいえ  <br/> |
|コピー後にクライアントが変更可能  <br/> |いいえ  <br/> |いいえ  <br/> |はい  <br/> |
|..内で一意です。  <br/> |ワールド全体  <br/> |プロバイダー インスタンス  <br/> |ワールド全体  <br/> |
|バイナリ比較 (memcmp と同様)  <br/> |いいえ -- [IMAPISupport::CompareEntryIDs を使用する](imapisupport-compareentryids.md) <br/> |はい  <br/> |はい  <br/> |
   
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



[PidTagResponsibility 標準プロパティ](pidtagresponsibility-canonical-property.md)
  
[PidTagStoreRecordKey 標準プロパティ](pidtagstorerecordkey-canonical-property.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

