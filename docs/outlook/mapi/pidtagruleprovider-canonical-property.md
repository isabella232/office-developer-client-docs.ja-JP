---
title: PidTagRuleProvider 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleProvider
api_type:
- COM
ms.assetid: 64f80a03-9ba4-495a-9666-b3a909335cb6
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3a80669f3d8f3d262cc8787f60efb3bc4b24d4b6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589442"
---
# <a name="pidtagruleprovider-canonical-property"></a>PidTagRuleProvider 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
ルールを設定するアプリケーションの名前が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_RULE_PROVIDER、PR_RULE_PROVIDER_A、PR_RULE_PROVIDER_W  <br/> |
|識別子:  <br/> |0x6681  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|領域:  <br/> |サーバー側のルール  <br/> |
   
## <a name="remarks"></a>注釈

これらのコードを識別するプロパティを解釈し、規則の操作を実行する必要がありますアクションの必要性を延期します。
  
メールボックスおよびフォルダーに格納されているルールは、ルールのプロバイダー文字列でそれらを所有するアプリケーションに関連付けられます。 ルール プロバイダーは、設定し、ルール テーブル内のルールを処理します。 このようなルールが設定されている場合に、遅延されたアクションを処理する手段も用意されています。 遅延アクションは、インフォメーション ストアによって暗黙的に作成されます。 別のストアに移動またはコピー操作の場合は、遅延処理のルールを設定するプロバイダーが備わっていること、ルールが実行され、遅延アクションが作成されるときにアクションを実行するハンドラー。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)
  
> サーバー上の受信電子メール メッセージを操作します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

