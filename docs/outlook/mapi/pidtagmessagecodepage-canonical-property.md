---
title: PidTagMessageCodepage 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageCodepage
api_type:
- HeaderDef
ms.assetid: eef73e34-470c-4c37-94ce-ea95fe83bc10
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 49f2c1c0b8af21f837582698763c17b9c41e1923
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387231"
---
# <a name="pidtagmessagecodepage-canonical-property"></a>PidTagMessageCodepage 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージに使用されるコード ページが含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_MESSAGE_CODEPAGE  <br/> |
|識別子:  <br/> |0x3FFD  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |Common  <br/> |
   
## <a name="remarks"></a>備考

このプロパティをゼロ (0) に設定されている場合、フォルダーのオブジェクトのコード ページが使用されます。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルのオブジェクトを処理します。
    
[[MS OXPFOAB]](https://msdn.microsoft.com/library/258a07a7-34a7-4373-87c1-cddf51447d00%28Office.15%29.aspx)
  
> オフライン アドレス帳 (OAB) のデータをサーバーからクライアントに配信する方法を指定します。
    
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

