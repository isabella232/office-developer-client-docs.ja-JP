---
title: PidTagXCoordinate 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagXCoordinate
api_type:
- COM
ms.assetid: 030d5c21-ab02-4047-bf2d-9a402a1e9102
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 87df676dccdb067302d62da2bd1fda6b634ed4f8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436196"
---
# <a name="pidtagxcoordinate-canonical-property"></a>PidTagXCoordinate 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ダイアログ ボックス コントロールの開始位置 (左上隅) の x 座標を標準のダイアログ 単位でWindowsします。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_XPOS  <br/> |
|識別子:  <br/> |0x3F05  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |MAPI 表示テーブル  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは **、PR_YPOS** ([PidTagYCoordinate)](pidtagycoordinate-canonical-property.md) **、PR_DELTAX** ([PidTagDeltaX)](pidtagdeltax-canonical-property.md)、および **PR_DELTAY** ([PidTagDeltaY](pidtagdeltay-canonical-property.md)) プロパティの位置とサイズをダイアログ ボックス コントロールに設定します。
  
## <a name="related-resources"></a>関連リソース

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

