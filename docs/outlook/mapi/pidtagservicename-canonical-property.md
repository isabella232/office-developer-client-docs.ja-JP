---
title: PidTagServiceName 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceName
api_type:
- COM
ms.assetid: 9a63d647-7504-42fc-b317-6b02b89070eb
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d950ee21c0c4c41e84c0fe1f8104219e63f84cec
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592676"
---
# <a name="pidtagservicename-canonical-property"></a>PidTagServiceName 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
MapiSvc.inf ファイルのユーザーによって設定されたメッセージ サービスの名前が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SERVICE_NAME、PR_SERVICE_NAME_A、PR_SERVICE_NAME_W  <br/> |
|識別子:  <br/> |0x3D09  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|領域:  <br/> |MAPI プロファイル  <br/> |
   
## <a name="remarks"></a>注釈

これらのプロパティに含まれている名前は、メッセージ サービスに固有です。 MapiSvc.inf の [サービス] セクションからなります。
  
これらのプロパティは、メッセージ サービス テーブル内の列として表示され、サービスをフィルター処理に使用することができます。 サービスを特定するためには、値をローカライズしない必要があります。
  
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

