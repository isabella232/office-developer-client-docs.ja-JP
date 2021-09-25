---
title: PidTagEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagEntryId
api_type:
- HeaderDef
ms.assetid: ca02e873-c2d2-4d58-8df8-c05fbcdc8fba
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 42e105ee5addca6445c3ee0ef667c873192d66e6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616510"
---
# <a name="pidtagentryid-canonical-property"></a>PidTagEntryId 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
特定の MAPI オブジェクトのプロパティを開いて編集するために使用される MAPI エントリ識別子が含まれる。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ENTRYID  <br/> |
|識別子:  <br/> |0x0FFF  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |ID プロパティ  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは **、OpenEntry** がインスタンス化するオブジェクトを識別し、IMAPIProp の適切な派生インターフェイスを介してすべてのプロパティへの **アクセスを提供します**。 
  
このプロパティは、すべてのメッセージング ユーザーの基本アドレス プロパティの 1 つです。 
  
このプロパティには、長期識別子または短期識別子を含めできます。 短期的な識別子は、作成が簡単かつ高速ですが、スコープと期間は制限されます(通常は現在のセッションとワークステーションに限定されます)。 一般に、テーブル行やダイアログ ボックスエントリなどの一時的な性質のオブジェクトに使用され、破棄されます。 長期的な識別子は、より広範囲で長期的な性質のオブジェクトに使用されます。 
  
このプロパティは [、IMAPIProp::SaveChanges](imapiprop-getprops.md) メソッドの最初の呼び出しに続く [IMAPIProp::GetProps](imapiprop-savechanges.md) メソッドを通じて常に使用できます。 一部のサービス プロバイダーは、インスタンス化の直後に利用できます。 プロバイダーは、常に GetProps から長期エントリ識別子を **返す必要があります**。 したがって、短期的な識別子を長期的に変換するには、オブジェクトを開き **、GetProps** を使用してこのプロパティを取得します。 
  
次の表に、このプロパティ 、PR_RECORD_KEY **(** [PidTagRecordKey)](pidtagrecordkey-canonical-property.md)、および PR_SEARCH_KEY ([PidTagSearchKey)](pidtagsearchkey-canonical-property.md)の重要な違 **い** を示します。 
  
|**特性**|**PR_ENTRYID**|**PR_RECORD_KEY**|**PR_SEARCH_KEY**|
|:-----|:-----|:-----|:-----|
|添付ファイル オブジェクトに必須  <br/> |いいえ  <br/> |はい  <br/> |いいえ  <br/> |
|フォルダー オブジェクトに必須  <br/> |はい  <br/> |はい  <br/> |いいえ  <br/> |
|メッセージ ストア オブジェクトで必須  <br/> |はい  <br/> |はい  <br/> |いいえ  <br/> |
|状態オブジェクトで必須  <br/> |はい  <br/> |いいえ  <br/> |いいえ  <br/> |
|クライアントによって作成される  <br/> |いいえ  <br/> |いいえ  <br/> |はい  <br/> |
|SaveChanges の呼び **出し前に使用可能** <br/> |プロバイダーの実装によって異なります  <br/> |プロバイダーの実装によって異なります  <br/> |メッセージの場合は、はい。 その他の場合は、プロバイダーの実装に依存します。  <br/> |
|コピー操作で変更された  <br/> |はい  <br/> |はい  <br/> |いいえ  <br/> |
|コピー後にクライアントが変更可能  <br/> |いいえ  <br/> |いいえ  <br/> |はい  <br/> |
|内で一意  <br/> |ワールド全体  <br/> |プロバイダー インスタンス  <br/> |ワールド全体  <br/> |
|バイナリ比較 (memcmp と同様)  <br/> |[IMAPISupport:: CompareEntryIDs を使用しない](imapisupport-compareentryids.md) <br/> |はい  <br/> |はい  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージ オブジェクトと添付ファイル オブジェクトを処理します。
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> ユーザー、連絡先、グループ、およびリソースの一覧のプロパティと操作を指定します。
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> インターネット標準の電子メール規則からメッセージ オブジェクトに変換します。
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> クライアントとサーバー間のデータ転送の順序とフローを処理します。
    
[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)
  
> サーバーに保存されているフォルダーのアクセス許可リストの取得を処理します。
    
[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> メールボックスを代理人として接続および構成するためのメソッド、および他のユーザーの代理として動作するメッセージ オブジェクトと予定表オブジェクトとのやり取りを指定します。
    
[[MS-OXWAVLS]](https://msdn.microsoft.com/library/69a276d8-5fc3-40ba-acd0-31cf42e6af58%28Office.15%29.aspx)
  
> ユーザーとリソースの可用性情報を要求するために使用するスキーマとメソッドを指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[PidTagStoreEntryId 標準プロパティ](pidtagstoreentryid-canonical-property.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

