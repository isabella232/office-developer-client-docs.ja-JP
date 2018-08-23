---
title: PidTagRuleProviderData 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleProviderData
api_type:
- COM
ms.assetid: b04a277c-b483-4f54-b360-311034b9a7ee
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f4f1070b89971c631fd855a6f84d56b699152421
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566846"
---
# <a name="pidtagruleproviderdata-canonical-property"></a>PidTagRuleProviderData 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
クライアントの設定は、クライアントが排他的に使用する不透明なプロパティです。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_RULE_PROVIDER_DATA  <br/> |
|識別子:  <br/> |0x6684  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|領域:  <br/> |サーバー側のルール  <br/> |
   
## <a name="remarks"></a>注釈

サーバーは、クライアントが設定されている場合、このプロパティの値を保持する必要がありますが、ルールの評価および処理中にその内容を無視する必要があります。
  
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
  
> 関連付けられているプロパティとして記載されているプロパティの定義が含まれています。 
    
## <a name="see-also"></a>関連項目



[PidTagRuleProvider 標準プロパティ](pidtagruleprovider-canonical-property.md)


[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

