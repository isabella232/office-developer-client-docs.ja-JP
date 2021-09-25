---
title: PidLidLogEnd 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidLogEnd
api_type:
- COM
ms.assetid: 621459ea-adf5-4420-9f0f-6f31b9b95508
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3c8445e3fcec1c3fe7be91ba16ba4cd7395d526e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583780"
---
# <a name="pidlidlogend-canonical-property"></a>PidLidLogEnd 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ジャーナル メッセージの終了日時を表します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidLogEnd  <br/> |
|プロパティ セット:  <br/> |PSETID_Log  <br/> |
|長い ID (LID):  <br/> |0x00008708  <br/> |
|データの種類 :   <br/> |PT_SYSTIME  <br/> |
|エリア:  <br/> |ジャーナル  <br/> |
   
## <a name="remarks"></a>注釈

アクティビティが協定世界時 (UTC) で終了した時刻で、 **これは dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) プロパティと等しく **、dispidLogStart** ([PidLidLogStart](pidlidlogstart-canonical-property.md)) プロパティ以上である必要があります。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。
    
[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)
  
> ジャーナルに対して許容されるプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

