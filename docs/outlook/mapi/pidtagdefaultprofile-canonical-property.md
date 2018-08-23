---
title: PidTagDefaultProfile 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefaultProfile
api_type:
- HeaderDef
ms.assetid: 47f745a4-5a9c-42af-b076-a72548ef4d31
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a315f1564f2980ad16ce2ba3da2308960f7d4b88
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578893"
---
# <a name="pidtagdefaultprofile-canonical-property"></a>PidTagDefaultProfile 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
メッセージング ユーザー プロファイルが既定の MAPI プロファイルの場合、TRUE が格納されます。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_DEFAULT_PROFILE  <br/> |
|識別子:  <br/> |0x3D04  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|領域:  <br/> |MAPI プロファイル  <br/> |
   
## <a name="remarks"></a>注釈

プロファイル テーブルに列としてのみですが、任意のオブジェクトのプロパティとしては、このプロパティは表示されません。 クライアント アプリケーションは、既定のプロファイルを指定するのには[IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md)メソッドを使用することができます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 関連付けられているプロパティとして記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[PidTagDefaultStore 標準プロパティ](pidtagdefaultstore-canonical-property.md)


[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

