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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3fbd7205901616695bcdcd012601afd252ac05f3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355644"
---
# <a name="pidtagoriginaldisplaybcc-canonical-property"></a>PidTagOriginalDisplayBcc 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
元のメッセージのブラインド カーボン コピー (BCC) 受信者の表示名を格納します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ORIGINAL_DISPLAY_BCC、PR_ORIGINAL_DISPLAY_BCC_A、PR_ORIGINAL_DISPLAY_BCC_W  <br/> |
|識別子:  <br/> |0x0072  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |一般的なメッセージング  <br/> |
   
## <a name="remarks"></a>注釈

これらのプロパティには、セミコロンで区切られたリストが含まれる。 これらは MAPI によって提供され、配信レポートまたは配信不能レポートまたは読み取りまたは読み取り以外のレポートが生成されると **、PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) から直接コピーされます。 これらのプロパティは、メッセージ クラスで定義されている他のメッセージに存在する可能性があります。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> 電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

