---
title: PidTagOriginalDisplayBcc 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalDisplayBcc
api_type:
- COM
ms.assetid: 7bf66f0c-3095-4b4a-a32e-db278e1adc5a
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 20f70f9e7bfecd955eb6bfb1c05c6b2010cb52cd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563409"
---
# <a name="pidtagoriginaldisplaybcc-canonical-property"></a>PidTagOriginalDisplayBcc 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
元のメッセージのブラインド カーボン コピー (BCC) 受信者の表示名が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ORIGINAL_DISPLAY_BCC、PR_ORIGINAL_DISPLAY_BCC_A、PR_ORIGINAL_DISPLAY_BCC_W  <br/> |
|識別子:  <br/> |0x0072  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|領域:  <br/> |メッセージ全般  <br/> |
   
## <a name="remarks"></a>注釈

これらのプロパティには、セミコロンで区切られたリストが含まれています。 MAPI によって提供されて、配信または配信不能レポート、読み取りまたは nonread のレポートが生成されるときに、 **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) から直接コピーされます。 これらのプロパティは、他のメッセージをそのメッセージ クラスで定義されている可能性があります。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。
    
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

