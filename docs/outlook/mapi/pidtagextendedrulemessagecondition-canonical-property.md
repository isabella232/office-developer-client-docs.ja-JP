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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 92008a387bb0130207af012df209a3aa6881d40e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593173"
---
# <a name="pidtagextendedrulemessagecondition-canonical-property"></a>PidTagExtendedRuleMessageCondition 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
拡張ルールの条件の内で含まれている任意の名前付きプロパティに関する情報が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_EXTENDED_RULE_MSG_CONDITION  <br/> |
|識別子:  <br/> |0x0E9A  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|領域:  <br/> |Rules  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、FAI メッセージを設定する必要があります。 **PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md)) と同じ役目を果たしますが、使用する名前付きプロパティに関する追加情報が含まれています。 この条件のプロパティの値の任意の部分に含まれるすべての文字列値は、Unicode 形式である必要があります。
  
このバイナリのプロパティの形式については、 [[MS OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)を参照してください。
  
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

