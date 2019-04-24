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
ms.openlocfilehash: e5659113b1c6579913042ae0c8dfcd03e9802621
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359480"
---
# <a name="pidtagservicename-canonical-property"></a>PidTagServiceName 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
mapisvc.inf ファイル内のユーザーによって設定されたメッセージサービスの名前を格納します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SERVICE_NAME、PR_SERVICE_NAME_A、PR_SERVICE_NAME_W  <br/> |
|識別子:  <br/> |0x3d09  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |MAPI プロファイル  <br/> |
   
## <a name="remarks"></a>解説

これらのプロパティに含まれる名前は、メッセージサービスに固有のものです。 これは、mapisvc.inf の [サービス] セクションから取得されます。
  
これらのプロパティは、メッセージサービステーブルの列として表示され、サービスのフィルター処理に使用できます。 サービスを識別してフィルター処理するために使用されるため、この値はローカライズしないでください。
  
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

