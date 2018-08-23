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
ms.openlocfilehash: 4cd865fbc443a20ebf4b4cd9722fe52c44d5eddc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573811"
---
# <a name="pidtagproviderordinal-canonical-property"></a>PidTagProviderOrdinal 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
プロバイダー テーブル内のサービス プロバイダーの位置の 0 から始まるインデックスが含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_PROVIDER_ORDINAL  <br/> |
|識別子:  <br/> |0x300D  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|領域:  <br/> |一般的な MAPI  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、MAPI によって計算されます。
  
プロバイダー テーブルを取得するには、 [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md)メソッドを呼び出します。 トランスポートの順番を表示するには、このプロパティのプロバイダー テーブルを並べ替えます。 
  
## <a name="related-resources"></a>関連リソース

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

