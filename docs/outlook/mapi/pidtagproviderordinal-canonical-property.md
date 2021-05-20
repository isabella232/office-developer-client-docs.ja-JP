---
title: PidTagProviderOrdinal 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderOrdinal
api_type:
- COM
ms.assetid: d062b54d-7c32-4369-ab69-f7193773a1c0
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: fbeb63bbae23f8f7f78c92d3abed6bea1c3ac85d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438352"
---
# <a name="pidtagproviderordinal-canonical-property"></a>PidTagProviderOrdinal 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロバイダー テーブル内のサービス プロバイダーの位置の 0 から始るインデックスを格納します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_PROVIDER_ORDINAL  <br/> |
|識別子:  <br/> |0x300D  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |MAPI 共通  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは MAPI によって計算されます。
  
[IMsgServiceAdmin::GetProviderTable メソッドを](imsgserviceadmin-getprovidertable.md)呼び出して、プロバイダー テーブルを取得します。 このプロパティのプロバイダー テーブルを並べ替え、トランスポートの順序を表示します。 
  
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

