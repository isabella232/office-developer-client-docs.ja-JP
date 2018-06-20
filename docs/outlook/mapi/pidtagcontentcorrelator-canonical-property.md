---
title: PidTagContentCorrelator の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContentCorrelator
api_type:
- HeaderDef
ms.assetid: 0bf78879-2f9f-4c29-b1f4-2f4882d8464d
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 2290e6751778f17defc8d1007ff62c88f1b75465
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802601"
---
# <a name="pidtagcontentcorrelator-canonical-property"></a>PidTagContentCorrelator の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
元のメッセージを含むレポートを一致するようにメッセージの送信者を使用できる値が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_CONTENT_CORRELATOR  <br/> |
|識別子:  <br/> |0x0007  <br/> |
|データを入力します。  <br/> |PT_BINARY  <br/> |
|領域:  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>備考

バイナリ文字列の内容は、メッセージの発信者によって定義されます。 メッセージへの応答として生成されるすべてのレポートには、送信メッセージ、このプロパティのセットをコピーしてください。 場合、
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 関連付けられているプロパティとして記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

