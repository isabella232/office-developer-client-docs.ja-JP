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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359494"
---
# <a name="pidtagruleid-canonical-property"></a>PidTagRuleId 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ルールが最初に作成されたときに、メッセージングサーバーがルールごとに生成する一意の識別子を指定します。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_RULE_ID  <br/> |
|識別子:  <br/> |0x6674  <br/> |
|データの種類 :   <br/> |PT_I8  <br/> |
|エリア:  <br/> |サーバー側のルール  <br/> |
   
## <a name="remarks"></a>解説

クライアントは、新しいルールを作成するときにこのプロパティを指定する必要はありませんが、ルールを変更または削除するときにこのプロパティを指定する必要があります。
  
ルールを削除する場合、クライアントが渡す必要のあるプロパティは**PR_RULE_ID**のみであり、その他のプロパティに渡すことはできません。 サーバーは、このプロパティ以外のプロパティを無視する必要があります。 ルールを追加するときは、クライアントは**PR_RULE_ID**を渡すことはできません。そのためには、 **PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md))、 **PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md))、 **PR_RULE_PROVIDER** ([PidTagRuleProvider](pidtagruleprovider-canonical-property.md)) プロパティ。 ルールを変更する場合、クライアントは**PR_RULE_ID**を渡す必要があり、変更する必要がある残りのプロパティを渡す必要があります。 
  
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



[PidTagRuleCondition 標準プロパティ](pidtagrulecondition-canonical-property.md)
  
[PidTagRuleActions 標準プロパティ](pidtagruleactions-canonical-property.md)
  
[PidTagRuleProvider 標準プロパティ](pidtagruleprovider-canonical-property.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

