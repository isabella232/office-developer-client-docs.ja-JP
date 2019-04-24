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
ms.openlocfilehash: 19889a1f48a6088f0d5ad224f7e9189b112622fa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280606"
---
# <a name="pidtagruleprovider-canonical-property"></a>PidTagRuleProvider 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ルールを設定するアプリケーションの名前が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_RULE_PROVIDER、PR_RULE_PROVIDER_A、PR_RULE_PROVIDER_W  <br/> |
|識別子:  <br/> |0x6681  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |サーバー側のルール  <br/> |
   
## <a name="remarks"></a>解説

遅延アクションには、ルールの処理を解釈して実行する必要があるコードを識別するためのプロパティが必要です。
  
メールボックスとフォルダーに格納されているルールは、ルールプロバイダ文字列でそのルールを所有するアプリケーションに関連付けられます。 ルールプロバイダーは、ルールテーブルのルールを設定して処理します。 また、このようなルールが設定されている場合は、遅延アクションを処理する手段も提供されます。 遅延アクションは、インフォメーションストアによって暗黙的に作成されます。 別のストアに移動またはコピー操作を行う場合、プロバイダーが遅延アクションルールを設定している場合は、ルールが発生し、遅延アクションが作成されるときにアクションを実行するハンドラーを指定する必要があります。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)
  
> サーバー上の受信電子メールメッセージを操作します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 代替名としてリストされているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

