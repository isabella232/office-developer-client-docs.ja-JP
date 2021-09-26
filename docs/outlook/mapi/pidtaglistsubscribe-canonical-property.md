---
title: PidTagListSubscribe 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagListSubscribe
api_type:
- HeaderDef
ms.assetid: 97387a82-8e40-4c76-818c-2229fac12e01
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c1bc4b7b968bd375e041666725842ec8d4e95519
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583395"
---
# <a name="pidtaglistsubscribe-canonical-property"></a>PidTagListSubscribe 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
多目的インターネット メール拡張機能 (MIME) メッセージのヘッダー フィールドの値List-Subscribeします。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_LIST_SUBSCRIBE、PR_LIST_SUBSCRIBE_A、PR_LIST_SUBSCRIBE_W  <br/> |
|識別子:  <br/> |0x1044  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |その他  <br/> |
   
## <a name="remarks"></a>注釈

ヘッダー フィールドをList-Subscribeするには、クライアントがこれらのプロパティの値を目的の値に設定する必要があります。 MIME ライターは、これらのプロパティの値をヘッダー フィールドのList-Subscribeする必要があります。
  
このようなサーバー関連のプロパティの値を設定するには、MIME クライアントが次の表で指定したヘッダー フィールドを記述する必要があります。
  
|**プロパティ**|**優先ヘッダー フィールド名**|**代替ヘッダー フィールド名**|
|:-----|:-----|:-----|
|**PidTagListSubscribe** <br/> |List-Subscribe  <br/> |X-List-Subscribe  <br/> |
   
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

