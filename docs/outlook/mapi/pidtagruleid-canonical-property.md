---
title: PidTagRuleId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleId
api_type:
- COM
ms.assetid: 341e8db0-52b7-4ba7-aaa6-eedf2783b4e8
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 8d88838893836c550136be9556299258b44e3e49
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398060"
---
# <a name="pidtagruleid-canonical-property"></a>PidTagRuleId 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ルールが最初に作成したとき、各ルールのメッセージング サーバーが生成されます一意の識別子を指定します。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_RULE_ID  <br/> |
|識別子:  <br/> |0x6674  <br/> |
|データの種類 :   <br/> |PT_I8  <br/> |
|エリア:  <br/> |サーバー側のルール  <br/> |
   
## <a name="remarks"></a>備考

新しいを作成するとき、クライアントがこのプロパティを指定する必要がありますルールが変更またはルールを削除するときに指定する必要があります。
  
ルールを削除するとプロパティのみが、クライアントに渡す必要があります**PR_RULE_ID**は、他のすべてのプロパティで渡さないでください。 サーバーは、このプロパティ以外のプロパティを無視する必要があります。 ルールを追加するには、クライアントが**PR_RULE_ID**に渡す必要があります。 されません、 **PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md))、 **PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md)) と**PR_RULE_PROVIDER** ([に渡す必要があります。PidTagRuleProvider](pidtagruleprovider-canonical-property.md)) のプロパティです。 ルールを変更するには、クライアントが**PR_RULE_ID**に渡す必要があり、変更する必要があるプロパティの残りの部分に渡す必要があります。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)
  
> サーバー上の受信電子メール メッセージを操作します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[PidTagRuleCondition 標準プロパティ](pidtagrulecondition-canonical-property.md)
  
[PidTagRuleActions 標準プロパティ](pidtagruleactions-canonical-property.md)
  
[PidTagRuleProvider 標準プロパティ](pidtagruleprovider-canonical-property.md)


[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

