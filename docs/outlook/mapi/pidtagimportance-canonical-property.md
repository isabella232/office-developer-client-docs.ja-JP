---
title: PidTagImportance 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagImportance
api_type:
- HeaderDef
ms.assetid: 274dd444-a863-4b53-bdbc-3763c375c43c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 12fa3d0d1c5cc84c42049f4a208ea961f6631bcd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566209"
---
# <a name="pidtagimportance-canonical-property"></a>PidTagImportance 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
メッセージの重要度のメッセージの送信者の意見を示す値が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_IMPORTANCE  <br/> |
|識別子:  <br/> |0x0017  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|領域:  <br/> |メッセージ全般  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、 **PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md)) は混同しないでください。 重要性は、優先順位は、順序や速度のメッセージがメッセージング システムのソフトウェアが送信することを示します。 ユーザーに値を示します。 高い優先度は、通常より高いコストを示します。 重要度が高く通常は、ユーザー インターフェイスで別のディスプレイに関連付けられています。 
  
このプロパティは、次の値の 1 つだけ持つことができます。
  
IMPORTANCE_LOW 
  
> メッセージには重要度が低い。
    
IMPORTANCE_HIGH 
  
> メッセージには重要度が高い。
    
IMPORTANCE_NORMAL 
  
> メッセージには、通常の重要性があります。
    
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルのオブジェクトを処理します。
    
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

