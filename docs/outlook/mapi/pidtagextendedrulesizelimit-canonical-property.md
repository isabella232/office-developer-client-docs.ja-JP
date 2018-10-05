---
title: PidTagExtendedRuleSizeLimit 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExtendedRuleSizeLimit
api_type:
- HeaderDef
ms.assetid: 87186764-fb58-4cdf-804d-bb13c5a8cb65
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 347d84021b7e9ece925acb99e8b539ba608337a9
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384998"
---
# <a name="pidtagextendedrulesizelimit-canonical-property"></a>PidTagExtendedRuleSizeLimit 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
最大のサイズ (バイト単位)、ユーザーは「拡張」ルールを 1 つに蓄積します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_EXTENDED_RULE_SIZE_LIMIT  <br/> |
|識別子:  <br/> |0x0E9B  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |ルール  <br/> |
   
## <a name="remarks"></a>備考

ログオン オブジェクトでこのプロパティを設定すると、クライアントはこのプロパティで指定された値] の下の**PR_EXTENDED_RULE_MSG_CONDITION** ([PidTagExtendedRuleMessageCondition](pidtagextendedrulemessagecondition-canonical-property.md)) のプロパティのサイズを維持する必要があります。 逆に、クライアントは大きすぎるバイナリ プロパティを設定する場合、サーバーはエラーを返す必要があります。
  
拡張ルールの詳細については、 [[MS OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)を参照してください。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)
  
> コア メッセージのストア オブジェクトの許可された操作を指定します。
    
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

