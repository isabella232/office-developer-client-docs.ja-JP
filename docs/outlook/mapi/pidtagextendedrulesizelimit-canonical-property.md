---
title: PidTagExtendedRuleSizeLimit の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 01d25614780f10f30d9e1314ea7f60ad3fbb4af0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802742"
---
# <a name="pidtagextendedrulesizelimit-canonical-property"></a>PidTagExtendedRuleSizeLimit の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
最大のサイズ (バイト単位)、ユーザーは「拡張」ルールを 1 つに蓄積します。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_EXTENDED_RULE_SIZE_LIMIT  <br/> |
|識別子:  <br/> |0x0E9B  <br/> |
|データを入力します。  <br/> |PT_LONG  <br/> |
|領域:  <br/> |ルール  <br/> |
   
## <a name="remarks"></a>備考

ログオン オブジェクトでこのプロパティを設定すると、クライアントはこのプロパティで指定された値] の下の**PR_EXTENDED_RULE_MSG_CONDITION** ([PidTagExtendedRuleMessageCondition](pidtagextendedrulemessagecondition-canonical-property.md)) のプロパティのサイズを維持する必要があります。 逆に、クライアントは大きすぎるバイナリ プロパティを設定する場合、サーバーはエラーを返す必要があります。
  
拡張ルールの詳細については、 [[MS OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)を参照してください。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)
  
> コア メッセージのストア オブジェクトの許可された操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)
