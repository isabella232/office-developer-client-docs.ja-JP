---
title: PidTagEntryId 標準プロパティ
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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: feb34cdbf8ba917936c3272bcaaf6eff040ddc3a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328589"
---
# <a name="pidtagentryid-canonical-property"></a>PidTagEntryId 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
特定の mapi オブジェクトのプロパティを開いて編集するために使用する mapi エントリ識別子を含みます。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ENTRYID  <br/> |
|識別子:  <br/> |0x0FFF  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |ID プロパティ  <br/> |
   
## <a name="remarks"></a>解説

このプロパティは、インスタンス化する**openentry**のオブジェクトを識別し、 **imapiprop**の適切な派生インターフェイスを使用して、そのすべてのプロパティにアクセスできるようにします。 
  
このプロパティは、すべてのメッセージングユーザーのベースアドレスプロパティの1つです。 
  
このプロパティには、長期間または短期識別子のいずれかを含めることができます。 短時間の識別子は簡単に作成できますが、そのスコープと期間は、通常現在のセッションとワークステーションに制限されます。 これらのオブジェクトは、テーブルの行やダイアログボックスのエントリなど、一時的な性質を持つオブジェクトでよく使用され、破棄されます。 長期間の識別子は、より広範囲で長期的な性質を持つオブジェクトに使用されます。 
  
このプロパティは、imapiprop [:: SaveChanges](imapiprop-savechanges.md)メソッドを最初に呼び出した後、 [imapiprop:: GetProps](imapiprop-getprops.md)メソッドを使用して常に使用できます。 一部のサービスプロバイダーは、インスタンス化後すぐに使用できるようにすることができます。 プロバイダーは常に、 **GetProps**から長期のエントリ id を返す必要があります。 そのため、短い用語識別子を長期に変換するには、単にオブジェクトを開き、 **GetProps**を使用してこのプロパティを取得します。 
  
次の表は、このプロパティ、 **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))、および**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) の重要な相違点をまとめたものです。 
  
|**特性**|**PR_ENTRYID**|**PR_RECORD_KEY**|**PR_SEARCH_KEY**|
|:-----|:-----|:-----|:-----|
|attachment オブジェクトに必要  <br/> |いいえ  <br/> |はい  <br/> |いいえ  <br/> |
|folder オブジェクトで必要  <br/> |はい  <br/> |はい  <br/> |いいえ  <br/> |
|メッセージストアオブジェクトに必要  <br/> |はい  <br/> |はい  <br/> |いいえ  <br/> |
|状態オブジェクトに必要です  <br/> |はい  <br/> |いいえ  <br/> |いいえ  <br/> |
|クライアントによって作成  <br/> |いいえ  <br/> |いいえ  <br/> |はい  <br/> |
|**SaveChanges**の呼び出し前に使用できます。 <br/> |プロバイダーの実装によって異なります。  <br/> |プロバイダーの実装によって異なります。  <br/> |メッセージの場合は、はい。 その他の場合は、プロバイダーの実装によって異なります。  <br/> |
|コピー操作で変更  <br/> |はい  <br/> |はい  <br/> |いいえ  <br/> |
|コピー後にクライアントによって変更可能  <br/> |いいえ  <br/> |いいえ  <br/> |はい  <br/> |
|内で一意  <br/> |世界全体  <br/> |プロバイダーインスタンス  <br/> |世界全体  <br/> |
|二項比較 (memcmp と同じ)  <br/> |使用しない[imapisupport:: compareentryids](imapisupport-compareentryids.md) <br/> |はい  <br/> |はい  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルオブジェクトを処理します。
    
[[OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> ユーザー、連絡先、グループ、およびリソースのリストのプロパティと操作を指定します。
    
[[OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> インターネット標準の電子メールの規則からメッセージオブジェクトに変換します。
    
[[OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> クライアントとサーバー間のデータ転送の順序と流れを処理します。
    
[[OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)
  
> サーバーに格納されているフォルダーのアクセス許可リストの取得を処理します。
    
[[OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> 代理人としてメールボックスに接続して構成するためのメソッド、および別のユーザーの代理として実行されたときに、メッセージおよび予定表オブジェクトとの相互作用を指定します。
    
[[OXWAVLS]](https://msdn.microsoft.com/library/69a276d8-5fc3-40ba-acd0-31cf42e6af58%28Office.15%29.aspx)
  
> ユーザーとリソースの空き時間情報を要求するために使用するスキーマとメソッドを指定します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 代替名としてリストされているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[PidTagStoreEntryId 標準プロパティ](pidtagstoreentryid-canonical-property.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

