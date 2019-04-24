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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: fbeb63bbae23f8f7f78c92d3abed6bea1c3ac85d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286440"
---
# <a name="pidtagproviderordinal-canonical-property"></a>PidTagProviderOrdinal 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロバイダーテーブル内のサービスプロバイダーの位置の0から始まるインデックスを格納します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_PROVIDER_ORDINAL  <br/> |
|識別子:  <br/> |0x300d  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |MAPI 共通  <br/> |
   
## <a name="remarks"></a>解説

このプロパティは MAPI で計算されます。
  
[IMsgServiceAdmin:: getprovidertable](imsgserviceadmin-getprovidertable.md)メソッドを呼び出して、プロバイダーテーブルを取得します。 このプロパティのプロバイダテーブルを並べ替えて、トランスポート順序を表示します。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 代替名としてリストされているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

