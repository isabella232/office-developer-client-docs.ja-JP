---
title: PidTagServiceUid 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceUid
api_type:
- COM
ms.assetid: 9d99a3b6-d0b4-4e8a-8f08-f46fdeb6b3e7
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: eabcaaf1db6149ef200e640f5af152758261581b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582253"
---
# <a name="pidtagserviceuid-canonical-property"></a>PidTagServiceUid 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
メッセージ サービスの[MAPIUID](mapiuid.md)構造体が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SERVICE_UID  <br/> |
|識別子:  <br/> |0x3D0C  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|領域:  <br/> |MAPI プロファイル  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、プロファイル セクション オブジェクトを MAPI によって計算されます。 同じメッセージ サービスに属するすべてのプロバイダーをグループ化するのには MAPI を使用します。 このプロパティは、ほとんどの[IMsgServiceAdmin](imsgserviceadminiunknown.md)メソッドのパラメーターとして提供されます。 Mapisvc.inf には表示する必要があります。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

