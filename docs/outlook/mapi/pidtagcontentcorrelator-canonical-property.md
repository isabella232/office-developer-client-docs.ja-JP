---
title: PidTagContentCorrelator 標準プロパティ
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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 6398acf71e62157cf5a6eb7e6caf22130fa9f9d0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568806"
---
# <a name="pidtagcontentcorrelator-canonical-property"></a>PidTagContentCorrelator 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
元のメッセージを含むレポートを一致するようにメッセージの送信者を使用できる値が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_CONTENT_CORRELATOR  <br/> |
|識別子:  <br/> |0x0007  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|領域:  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>注釈

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
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

