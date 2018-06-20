---
title: PidTagPriority の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagPriority
api_type:
- COM
ms.assetid: 0f3a628f-5f8e-4716-98cc-868bd3400ba9
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 67f482e347db1b69a248c542f2cb172c41d6f9f1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803182"
---
# <a name="pidtagpriority-canonical-property"></a>PidTagPriority の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
メッセージの相対的な優先順位が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_PRIORITY  <br/> |
|識別子:  <br/> |0x0026  <br/> |
|データを入力します。  <br/> |PT_LONG  <br/> |
|領域:  <br/> |Email  <br/> |
   
## <a name="remarks"></a>備考

このプロパティは、 **PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md)) は混同しないでください。 重要性は、優先順位は、順序や速度のメッセージがメッセージング システムのソフトウェアが送信することを示します。 ユーザーに値を示します。 高い優先度は、通常より高いコストを示します。 重要度が高く通常は、ユーザー インターフェイスで別のディスプレイに関連付けられています。
  
レポート メッセージの優先度は、報告されている元のメッセージの優先順位と同じにする必要があります。
  
このプロパティは、次の値の 1 つだけ持つことができます。
  
PRIO_NONURGENT 
  
> メッセージが緊急ではありません。
    
PRIO_NORMAL 
  
> メッセージには、通常の優先順位があります。
    
PRIO_URGENT 
  
> メッセージは、緊急です。
    
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。
    
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

