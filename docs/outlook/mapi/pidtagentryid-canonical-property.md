---
title: PidTagEntryId の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagEntryId
api_type:
- HeaderDef
ms.assetid: ca02e873-c2d2-4d58-8df8-c05fbcdc8fba
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 971462b9e85878677b57ec7b53fe46aa64db6dba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802744"
---
# <a name="pidtagentryid-canonical-property"></a>PidTagEntryId の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
開き、特定の MAPI オブジェクトのプロパティを編集するに使用される MAPI エントリの識別子が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_ENTRYID  <br/> |
|識別子:  <br/> |0x0FFF  <br/> |
|データを入力します。  <br/> |PT_BINARY  <br/> |
|領域:  <br/> |ID プロパティ  <br/> |
   
## <a name="remarks"></a>備考

このプロパティは、 **OpenEntry**をインスタンス化するためにオブジェクトを識別し、すべての**IMAPIProp**の適切な派生インターフェイスからプロパティへのアクセスが用意されています。 
  
このプロパティは、すべてのメッセージング ユーザーのベース アドレスのプロパティのいずれかです。 
  
このプロパティは、長期的または短期的な識別子のいずれかを含めることができます。 短期的な識別子は、簡単かつ迅速に、構造がの範囲と現在のセッションとワークステーションを通常の期間に制限されてです。 一般的にテーブルの行や、ダイアログ ボックスのエントリなどの一時的な性質のオブジェクトの使用はあり、放棄し。 広範な長期保存性の高いオブジェクトには、長期的な識別子が使用されます。 
  
このプロパティは、常に[IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドへの最初の呼び出しの後、 [IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを使用します。 一部のサービス プロバイダーを使用する利用可能なインスタンス化後すぐに。 プロバイダーは、 **GetProps**から長期のエントリ id を常に返す必要があります。 したがって、長期的な短期的な識別子に変換、単にオブジェクトを開くし、このプロパティを**GetProps**。 
  
次の表は、 **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) と**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))、このプロパティの間の重要な違いをまとめたものです。 
  
|**特性**|**PR_ENTRYID**|**PR_RECORD_KEY**|**PR_SEARCH_KEY**|
|:-----|:-----|:-----|:-----|
|添付ファイルのオブジェクトで必要な  <br/> |いいえ  <br/> |はい  <br/> |いいえ  <br/> |
|フォルダー オブジェクトで必要な  <br/> |はい  <br/> |はい  <br/> |いいえ  <br/> |
|メッセージ ストア オブジェクトで必要な  <br/> |はい  <br/> |はい  <br/> |いいえ  <br/> |
|状態オブジェクトで必要な  <br/> |はい  <br/> |いいえ  <br/> |いいえ  <br/> |
|クライアントによって作成されました。  <br/> |いいえ  <br/> |いいえ  <br/> |はい  <br/> |
|**Savechanges メソッド**の呼び出しの前に使用可能です <br/> |プロバイダーの実装に依存します。  <br/> |プロバイダーの実装に依存します。  <br/> |メッセージは、[はい] です。 他のユーザーには、プロバイダーの実装に依存します。  <br/> |
|コピー操作で変更  <br/> |はい  <br/> |はい  <br/> |いいえ  <br/> |
|コピー後にクライアントによって変更可能です  <br/> |いいえ  <br/> |いいえ  <br/> |はい  <br/> |
|内で一意  <br/> |全体の世界  <br/> |プロバイダーのインスタンス  <br/> |全体の世界  <br/> |
|バイナリ (ため) と同じように匹敵します。  <br/> |使用しない[IMAPISupport:: CompareEntryIDs](imapisupport-compareentryids.md) <br/> |はい  <br/> |はい  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルのオブジェクトを処理します。
    
[[MS OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> プロパティとユーザー、連絡先、グループ、およびリソースのリストの操作を指定します。
    
[[MS OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> メッセージ オブジェクト インターネット標準の電子メールの表記規則からに変換します。
    
[[MS OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> 順序と、クライアントとサーバー間のデータ転送のフローを処理します。
    
[[MS OXCPERM]](http://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)
  
> サーバーに格納されているフォルダーのアクセス許可の一覧の取得を処理します。
    
[[MS OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> 接続し、別のユーザーに代わって動作する場合は、デリゲート、およびメッセージと予定表のオブジェクトとの対話としてメールボックスを構成するためのメソッドを指定します。
    
[[MS OXWAVLS]](http://msdn.microsoft.com/library/69a276d8-5fc3-40ba-acd0-31cf42e6af58%28Office.15%29.aspx)
  
> スキーマとユーザーとリソースの利用可能時間情報を要求するために使用するメソッドを指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[PidTagStoreEntryId の標準的なプロパティ](pidtagstoreentryid-canonical-property.md)


[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

