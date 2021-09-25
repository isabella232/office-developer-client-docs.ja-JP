---
title: PidTagServiceName 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagServiceName
api_type:
- COM
ms.assetid: 9a63d647-7504-42fc-b317-6b02b89070eb
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 390a298753c0e98635c55da11a4ae28588735b4e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591417"
---
# <a name="pidtagservicename-canonical-property"></a>PidTagServiceName 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MapiSvc.inf ファイル内のユーザーが設定したメッセージ サービスの名前を含みます。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SERVICE_NAME、PR_SERVICE_NAME_A、PR_SERVICE_NAME_W  <br/> |
|識別子:  <br/> |0x3D09  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |MAPI プロファイル  <br/> |
   
## <a name="remarks"></a>注釈

これらのプロパティに含まれる名前は、メッセージ サービスに固有です。 MapiSvc.inf の [サービス] セクションから取得されます。
  
これらのプロパティは、メッセージ サービス テーブルの列として表示され、サービスのフィルター処理に使用できます。 サービスを識別してフィルター処理するために使用されますので、値をローカライズする必要があります。
  
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

