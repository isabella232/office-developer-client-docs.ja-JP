---
title: PidNameRightsManagementLicense 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameRightsManagementLicense
api_type:
- COM
ms.assetid: ca3c9317-7873-4f37-b78f-b35467c81c29
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 889b823a55c39ebc19e52c8cc9a1d078a5732a01
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315023"
---
# <a name="pidnamerightsmanagementlicense-canonical-property"></a>PidNameRightsManagementLicense 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
権限が管理された電子メール メッセージの使用ライセンスをキャッシュします。
  
|||
|:-----|:-----|
|分名:  <br/> |なし  <br/> |
|プロパティ セット:  <br/> |PS_PUBLIC_STRINGS  <br/> |
|プロパティ名:  <br/> |DRMLicense  <br/> |
|データの種類 :   <br/> |PT_MV_BINARY  <br/> |
|エリア:  <br/> |セキュリティで保護されたメッセージング  <br/> |
   
## <a name="remarks"></a>注釈

プロパティが権限管理の電子メール メッセージに存在する場合、この複数バイナリ プロパティの最初の値には、権限管理電子メール メッセージの ZLIB ([RFC1950] で指定されている) 圧縮使用ライセンスが含まれている必要があります。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。
    
[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)
  
> 権限で管理されたエンコードされたメッセージのプロパティを指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

