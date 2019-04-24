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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e057ab2ca0c75d5c0d749ebde8f1bdfb4f1ae66a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278880"
---
# <a name="pidtaglistunsubscribe-canonical-property"></a>PidTagListUnsubscribe 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
マルチパーパスインターネットメール内線 (MIME) メッセージのリスト購読のヘッダーフィールドの値を格納します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_LIST_UNSUBSCRIBE、PR_LIST_UNSUBSCRIBE_A、PR_LIST_UNSUBSCRIBE_W  <br/> |
|識別子:  <br/> |0x1045  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |その他  <br/> |
   
## <a name="remarks"></a>解説

リストの購読取り消しヘッダーフィールドを生成するには、クライアントはこれらのプロパティを目的の値に設定する必要があります。 MIME ライターは、これらのプロパティの値をリスト購読中止ヘッダーフィールドにコピーする必要があります。
  
これらのリストサーバーに関連するプロパティの値を設定するには、次の表で指定されているように、MIME クライアントはヘッダーフィールドを記述する必要があります。
  
|**Property**|**優先ヘッダーフィールド名**|**代替ヘッダーフィールド名**|
|:-----|:-----|:-----|
|**PR_LIST_UNSUBSCRIBE** <br/> |リスト-登録解除  <br/> |X-リスト-登録解除  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> インターネット標準の電子メールの規則からメッセージオブジェクトに変換します。
    
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

