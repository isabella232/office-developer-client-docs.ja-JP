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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 431a212b6e024d695fe2de084080996d8b1054d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360411"
---
# <a name="pidtaginternetreferences-canonical-property"></a>PidTagInternetReferences 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
マルチパーパスインターネットメール内線 (MIME) メッセージの参照ヘッダーフィールドの値を格納します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_INTERNET_REFERENCES、PR_INTERNET_REFERENCES_A、PR_INTERNET_REFERENCES_W  <br/> |
|識別子:  <br/> |0x1039  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |MIME  <br/> |
   
## <a name="remarks"></a>解説

参照ヘッダーフィールドを生成するには、クライアントはこれらのプロパティを必要な値に設定する必要があります。 MIME ライターは、これらのプロパティの値を References header フィールドにコピーする必要があります。
  
これらのプロパティの値を設定するには、MIME クライアントは参照ヘッダーフィールドに必要な値を書き込む必要があります。 MIME リーダーは、参照ヘッダーフィールドの値をこれらのプロパティにコピーする必要があります。 MIME リーダーは、64 kb を超えた場合、これらのプロパティの値を切り捨てます。
  
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

