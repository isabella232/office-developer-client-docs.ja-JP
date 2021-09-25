---
title: PidTagRuleId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagRuleId
api_type:
- COM
ms.assetid: 341e8db0-52b7-4ba7-aaa6-eedf2783b4e8
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 9b8cca70214543658f708beb81785617d79406c5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624560"
---
# <a name="pidtagruleid-canonical-property"></a>PidTagRuleId 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ルールの最初の作成時にメッセージング サーバーが各ルールに対して生成する一意の識別子を指定します。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_RULE_ID  <br/> |
|識別子:  <br/> |0x6674  <br/> |
|データの種類 :   <br/> |PT_I8  <br/> |
|エリア:  <br/> |サーバー側のルール  <br/> |
   
## <a name="remarks"></a>注釈

クライアントは、新しいルールを作成するときにこのプロパティを指定する必要がありますが、ルールを変更または削除するときに指定する必要があります。
  
ルールを削除する場合、クライアントが渡す必要がある唯一のプロパティはPR_RULE_IDプロパティを渡す必要があります。 サーバーは、このプロパティ以外のプロパティを無視する必要があります。 ルールを追加する場合、クライアントは **PR_RULE_ID** で渡す必要があります。PR_RULE_CONDITION (  [PidTagRuleCondition](pidtagrulecondition-canonical-property.md)) **、PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md)) プロパティ、および PR_RULE_PROVIDER **(** [PidTagRuleProvider](pidtagruleprovider-canonical-property.md)) プロパティを渡す必要があります。 ルールを変更する場合、クライアントは PR_RULE_IDを渡す必要があります。変更する必要がある他のプロパティを渡す必要があります。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)
  
> サーバー上の受信メール メッセージを操作します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[PidTagRuleCondition 標準プロパティ](pidtagrulecondition-canonical-property.md)
  
[PidTagRuleActions 標準プロパティ](pidtagruleactions-canonical-property.md)
  
[PidTagRuleProvider 標準プロパティ](pidtagruleprovider-canonical-property.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

