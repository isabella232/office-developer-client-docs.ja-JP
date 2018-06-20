---
title: PidTagExtendedRuleMessageActions の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExtendedRuleMessageActions
api_type:
- HeaderDef
ms.assetid: 1cf277d4-76ec-4902-9e54-f1780cee49bf
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 5425496a5b7845daabf736978e6ed24518451fe0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802755"
---
# <a name="pidtagextendedrulemessageactions-canonical-property"></a>PidTagExtendedRuleMessageActions の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
フォルダー関連情報 (FAI) メッセージで使用される名前付きプロパティに関する追加情報が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_EXTENDED_RULE_MSG_ACTIONS  <br/> |
|識別子:  <br/> |0x0E99  <br/> |
|データを入力します。  <br/> |PT_BINARY  <br/> |
|領域:  <br/> |ルール  <br/> |
   
## <a name="remarks"></a>備考

このプロパティは、FAI メッセージを設定する必要があります。 このプロパティは、 **PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md)) と同じ役目を果たしますが、アクションについての情報と同様に、ルールとルールの処理に保存されている名前付きプロパティのバージョンに関する追加情報が含まれていますこのルールによって実行されます。 アクションを格納するために使用するアクション バッファーの一部に含まれるすべての文字列値は、Unicode 形式である必要があります。
  
このバイナリのプロパティの形式については、 [[MS OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)を参照してください。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照が用意されています。
    
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
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

