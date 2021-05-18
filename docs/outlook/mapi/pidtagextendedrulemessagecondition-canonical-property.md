---
title: PidTagExtendedRuleMessageCondition 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExtendedRuleMessageCondition
api_type:
- HeaderDef
ms.assetid: 891851e1-e4a4-4c20-a26c-7223bcca35f7
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7c444485c3a443694e2902343a02da5605bde39f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316332"
---
# <a name="pidtagextendedrulemessagecondition-canonical-property"></a>PidTagExtendedRuleMessageCondition 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
拡張ルール条件の内部に含まれる名前付きプロパティに関する情報が含まれる。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_EXTENDED_RULE_MSG_CONDITION  <br/> |
|識別子:  <br/> |0x0E9A  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |ルール  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、FAI メッセージで設定する必要があります。 このプロパティは、PR_RULE_CONDITION **(** [PidTagRuleCondition)](pidtagrulecondition-canonical-property.md)と同じ目的を提供しますが、使用される名前付きプロパティに関する追加情報が含まれている。 この条件プロパティ値の任意の部分に含まれるすべての文字列値は、Unicode 形式である必要があります。
  
このバイナリ プロパティの形式については [、「[MS-OXORULE] 」を参照してください](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)。
  
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



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

