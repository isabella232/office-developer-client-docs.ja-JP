---
title: PidTagContainerFlags 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContainerFlags
api_type:
- HeaderDef
ms.assetid: 66b8d333-227e-464d-8cf9-cd8a5ff15efb
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c13acd1c3b759602a5fbe07c21ca8b784e0fe4d1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802592"
---
# <a name="pidtagcontainerflags-canonical-property"></a>PidTagContainerFlags 標準プロパティ

  
  
**適用対象**: Outlook 
  
アドレス帳コンテナーの機能を記述するフラグのビットマスクを格納します。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_CONTAINER_FLAGS  <br/> |
|識別子:  <br/> |0x3600  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|領域:  <br/> |アドレス帳  <br/> |
   
## <a name="remarks"></a>注釈

1 つ以上次のフラグのビットマスクを設定できます。
  
AB_FIND_ON_OPEN 
  
> コンテナーの内容を表示する前に制限を要求するダイアログ ボックスが表示されます。 
    
AB_MODIFIABLE 
  
> エントリに追加され、コンテナーから削除します。 このフラグでは、コンテナー内のすべてのエントリを変更できるかどうかは示されません。
    
AB_RECIPIENTS 
  
> コンテナーには、受信者を保持できます。 このフラグでは、いずれかの受信者は、コンテナーに実際に存在するかどうか、またはかどうか、追加または削除は表示されません。 
    
AB_SUBCONTAINERS 
  
> コンテナーは、コンテナーの子を保持できます。 このフラグは、すべてのサブコンテナーは、コンテナーに実際に存在するかどうかもあるかどうか、ことができますが追加または削除には表示されません。 [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md)をサポートするためにコンテナーの AB_SUBCONTAINERS を設定する必要があります。 
    
AB_UNMODIFIABLE 
  
> エントリを追加またはコンテナーから削除されることはできません。 このフラグでは、コンテナー内のすべてのエントリを変更できるかどうかは示されません。 
    
オンライン サービスまたはサーバーへの低速の接続に使用されるコンテナーの AB_FIND_ON_OPEN フラグを強くお勧めします。 AB_FIND_ON_OPEN の設定を持つコンテナーが開かれたときに表示されているメッセージング ユーザーを制限するユーザーに、[**検索**] ダイアログ ボックスが表示されます。 メッセージングのユーザーを制限する部分の仕様は、内容の表示を劇的に短縮できます。 
  
AB_MODIFIABLE または AB_UNMODIFIABLE のいずれかのフラグを設定する必要があります。 あるコンテナーがわからないかどうか変更するか、変更がユーザーのアクセス権に依存する場合の例を示すためには、両方のフラグを設定できます。 この例では、クライアント アプリケーションは呼び出しを試みるし、コンテナーの機能を確認するのにはリターン コードを調査する必要があります。 クライアントは、通常、AB_MODIFIABLE を調べることによって開始します。 設定されている場合、クライアントは、コンテナーを変更しようとして、戻り値をチェックするための呼び出しを行います。 
  
AB_MODIFIABLE フラグはすることができますエントリの種類を示していないコンテナーに追加します。 これを確認するには、クライアントが、コンテナーの**PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) のプロパティを開くに適切な[OpenProperty](imapiprop-openproperty.md)メソッドを使用する必要があります。 開始**PR_CREATE_TEMPLATES**原因が返され、テーブルのコンテナーの one-off コンテナー内に作成できるエントリの種類を一覧表示します。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> プロパティとユーザー、連絡先、グループ、およびリソースのリストの操作を指定します。
    
[[MS NSPI]](http://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)
  
> ネーム サービス プロバイダー インターフェイス (NSPI) サーバーとクライアントの通信を処理します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 関連付けられているプロパティとして記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

