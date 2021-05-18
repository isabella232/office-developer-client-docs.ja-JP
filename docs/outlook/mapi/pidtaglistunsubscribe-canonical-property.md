---
title: PidTagListUnsubscribe 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagListUnsubscribe
api_type:
- HeaderDef
ms.assetid: 4e6bfbc7-7586-43cc-9380-daa0fe3d85a5
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e057ab2ca0c75d5c0d749ebde8f1bdfb4f1ae66a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278880"
---
# <a name="pidtaglistunsubscribe-canonical-property"></a>PidTagListUnsubscribe 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
多目的インターネット メール拡張機能 (MIME) メッセージのヘッダー フィールドの値List-Unsubscribeします。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_LIST_UNSUBSCRIBE、PR_LIST_UNSUBSCRIBE_A、PR_LIST_UNSUBSCRIBE_W  <br/> |
|識別子:  <br/> |0x1045  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |その他  <br/> |
   
## <a name="remarks"></a>注釈

ヘッダー フィールドを生成List-Unsubscribe、クライアントは、これらのプロパティを目的の値に設定する必要があります。 MIME ライターは、これらのプロパティの値をヘッダー フィールドのList-Unsubscribeする必要があります。
  
これらのリスト サーバー関連のプロパティの値を設定するには、MIME クライアントが次の表で指定したヘッダー フィールドを記述する必要があります。
  
|**Property**|**優先ヘッダー フィールド名**|**代替ヘッダー フィールド名**|
|:-----|:-----|:-----|
|**PR_LIST_UNSUBSCRIBE** <br/> |List-Unsubscribe  <br/> |X-List-Unsubscribe  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> インターネット標準の電子メール規則からメッセージ オブジェクトに変換します。
    
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

