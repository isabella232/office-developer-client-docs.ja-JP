---
title: PidTagDefaultProfile 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagDefaultProfile
api_type:
- HeaderDef
ms.assetid: 47f745a4-5a9c-42af-b076-a72548ef4d31
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e6c3f957b349e226c2dde2f0afff59e4861f3581
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59555462"
---
# <a name="pidtagdefaultprofile-canonical-property"></a>PidTagDefaultProfile 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージング ユーザー プロファイルが MAPI 既定のプロファイルの場合は TRUE を含む。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_DEFAULT_PROFILE  <br/> |
|識別子:  <br/> |0x3D04  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|エリア:  <br/> |MAPI プロファイル  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、任意のオブジェクトのプロパティとして表示されるのではなく、プロファイル テーブルの列としてのみ表示されます。 クライアント アプリケーションは [、IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md) メソッドを使用して既定のプロファイルを指定できます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[PidTagDefaultStore 標準プロパティ](pidtagdefaultstore-canonical-property.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

