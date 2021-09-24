---
title: PidTagEmsAbServer 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagEmsAbServer
api_type:
- HeaderDef
ms.assetid: de942619-2507-8fe0-bc81-f9da9ef7266f
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 4529b06949ef4f32a3f337a289d285949541f9ee
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59550646"
---
# <a name="pidtagemsabserver-canonical-property"></a>PidTagEmsAbServer 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
オフライン シナリオのアドレス帳コンテナーのパス、またはアドレス帳コンテナーがオンライン シナリオに存在するグローバル カタログ サーバーの完全修飾ドメイン名を指定します。
  
## 

|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_EMS_AB_SERVER、PR_EMS_AB_SERVER_A、PR_EMS_AB_SERVER_W  <br/> |
|識別子:  <br/> |0xFFFE  <br/> |
|データの種類 :   <br/> |PT_TSTRING  <br/> |
|エリア:  <br/> |アドレス帳  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティのプロパティの種類は、Unicode プラットフォーム **上の** シンボルを使用してコンパイルされると PT_UNICODE にリセットされ、シンボルでコンパイルされていない場合は PT_STRING8 に `UNICODE` リセット `UNICODE` されます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義を提供します。
    
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

