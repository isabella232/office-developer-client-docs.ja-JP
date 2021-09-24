---
title: PidTagServiceUid 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagServiceUid
api_type:
- COM
ms.assetid: 9d99a3b6-d0b4-4e8a-8f08-f46fdeb6b3e7
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 87cd61590895231b57e3eb835f2898901ebea0a3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59550429"
---
# <a name="pidtagserviceuid-canonical-property"></a>PidTagServiceUid 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ サービス [の MAPIUID](mapiuid.md) 構造を格納します。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SERVICE_UID  <br/> |
|識別子:  <br/> |0x3D0C  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |MAPI プロファイル  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、プロファイル セクション オブジェクトの MAPI によって計算されます。 MAPI は、同じメッセージ サービスに属しているすべてのプロバイダーをグループ化するために使用します。 このプロパティは、ほとんどの [IMsgServiceAdmin](imsgserviceadminiunknown.md) メソッドにパラメーターとして指定されます。 Mapisvc.inf には表示されません。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

