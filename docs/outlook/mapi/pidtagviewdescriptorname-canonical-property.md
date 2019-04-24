---
title: PidTagViewDescriptorName 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagViewDescriptorName
api_type:
- COM
ms.assetid: 1e689ee4-9e89-4328-beb9-05c80a6544a0
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ab906d83ae4ad46747fd9037728620db1d656d25
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360726"
---
# <a name="pidtagviewdescriptorname-canonical-property"></a>PidTagViewDescriptorName 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ビュー記述子の名前を格納します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_VD_NAME、PR_VD_NAME_A、PR_VD_NAME_W  <br/> |
|識別子:  <br/> |0x7006  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |メッセージクラスで定義された、パススルーテーブル  <br/> |
   
## <a name="remarks"></a>解説

これらのプロパティは、ビュー定義を含むフォルダー関連付け情報 (fai) メッセージに対して、空ではない文字列に設定する必要があります。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)
  
> カテゴリの共有リストや稼働時間など、クライアントおよびサーバーの構成データの場所とプロパティを指定します。
    
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

