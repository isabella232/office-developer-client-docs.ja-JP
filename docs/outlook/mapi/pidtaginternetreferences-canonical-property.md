---
title: PidTagInternetReferences 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInternetReferences
api_type:
- HeaderDef
ms.assetid: 645fe61d-414a-455e-b034-db3cfd003b9d
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 431a212b6e024d695fe2de084080996d8b1054d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360411"
---
# <a name="pidtaginternetreferences-canonical-property"></a>PidTagInternetReferences 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
多目的インターネット メール拡張機能 (MIME) メッセージの [参照] ヘッダー フィールドの値を格納します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_INTERNET_REFERENCES、PR_INTERNET_REFERENCES_A、PR_INTERNET_REFERENCES_W  <br/> |
|識別子:  <br/> |0x1039  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |MIME  <br/> |
   
## <a name="remarks"></a>注釈

参照ヘッダー フィールドを生成するには、クライアントがこれらのプロパティを目的の値に設定する必要があります。 MIME ライターは、これらのプロパティの値を References ヘッダー フィールドにコピーする必要があります。
  
これらのプロパティの値を設定するには、MIME クライアントが目的の値を References ヘッダー フィールドに書き込む必要があります。 MIME リーダーは、参照ヘッダー フィールドの値をこれらのプロパティにコピーする必要があります。 MIME リーダーの長さが 64 KB を超えると、これらのプロパティの値が切り詰められることがあります。
  
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

