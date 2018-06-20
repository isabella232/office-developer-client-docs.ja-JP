---
title: PidTagSearchKey の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: fcab369a-a1f4-4425-a272-e35046914a4d
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 169afc3b8cf982c4767802542b900ae80822cd01
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803501"
---
# <a name="pidtagsearchkey-canonical-property"></a>PidTagSearchKey の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
検索の相関関係を持つオブジェクトを識別するバイナリの比較可能なキーが含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_SEARCH_KEY  <br/> |
|識別子:  <br/> |0x300B  <br/> |
|データを入力します。  <br/> |PT_BINARY  <br/> |
|領域:  <br/> |ID プロパティ  <br/> |
   
## <a name="remarks"></a>備考

このプロパティは、メッセージのコピーなどの関連オブジェクトのトレースを提供し、重複した受信者などの不要なアイテムの検索が容易になります。
  
MAPI は、メッセージの受信者の検索キーを構築するための特定の規則を使用します。 検索キーが (大文字で)、アドレスの種類を連結することによって形成されるコロン ':'、電子メール アドレスを標準の形式、および終端の null 文字です。 正規の形式は、ここでは、大文字・小文字の区別のアドレスが表示され、大文字小文字が区別されていないアドレスは、大文字に変換することを意味します。 これは、メッセージの相関関係の維持に重要です。
  
メッセージのオブジェクトのこのプロパティは、すぐに次のメッセージの作成、 [IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを使用します。 その他のオブジェクトでは、 [IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドへの最初の呼び出しの後に利用可能です。 このプロパティは変更可能なので、信頼性の高い**SaveChanges**の呼び出しがすべての値を設定または[IMAPIProp::SetProps](imapiprop-setprops.md)メソッドによって変更をコミットするまでの**GetProps**を通じて入手することはできません。 
  
プロファイルの場合、MAPI は、ハード コーディングされたプロファイル セクション**MUID_PROFILE_INSTANCE**、1 つのプロパティとしては、このプロパティを使用しても提供します。 このキーが作成されると、すべてのプロファイル間で一意であることが保証され、 **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)) は、ことができます、たとえば、削除され、同じ名前で再作成するよりも信頼性の高いことができます。
  
**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))、 **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))、このプロパティの間の重要な相違点を次の表にまとめます。
  
|**特性**|PR_ENTRYID。|PR_RECORD_KEY。|PR_SEARCH_KEY。|
|:-----|:-----|:-----|:-----|
|添付ファイルのオブジェクトで必要な  <br/> |いいえ  <br/> |はい  <br/> |いいえ  <br/> |
|フォルダー オブジェクトで必要な  <br/> |はい  <br/> |はい  <br/> |いいえ  <br/> |
|メッセージ ストア オブジェクトで必要な  <br/> |はい  <br/> |はい  <br/> |いいえ  <br/> |
|状態オブジェクトで必要な  <br/> |はい  <br/> |いいえ  <br/> |いいえ  <br/> |
|クライアントで作成可能  <br/> |いいえ  <br/> |いいえ  <br/> |はい  <br/> |
|**SaveChanges**の前に使用可能です <br/> |プロバイダーの実装に依存します。  <br/> |プロバイダーの実装に依存します。  <br/> |メッセージは、[はい] です。 他のユーザーが、プロバイダーの実装によって異なります。  <br/> |
|コピー操作で変更  <br/> |はい  <br/> |はい  <br/> |いいえ  <br/> |
|コピー後にクライアントによって変更可能です  <br/> |いいえ  <br/> |いいえ  <br/> |はい  <br/> |
|内で重複しています.  <br/> |全体の世界  <br/> |プロバイダーのインスタンス  <br/> |全体の世界  <br/> |
|バイナリ (ため) と同じように匹敵します。  <br/> |いいえ-- [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md)を使用して、 <br/> |はい  <br/> |はい  <br/> |
   
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



[PidTagResponsibility の標準的なプロパティ](pidtagresponsibility-canonical-property.md)
  
[PidTagStoreRecordKey の標準的なプロパティ](pidtagstorerecordkey-canonical-property.md)


[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

