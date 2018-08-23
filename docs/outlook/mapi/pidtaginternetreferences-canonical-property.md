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
ms.openlocfilehash: b0e01d3f56ef01984f281e7fae5990ccb0eade88
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593334"
---
# <a name="pidtaginternetreferences-canonical-property"></a>PidTagInternetReferences 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
多目的インターネット メール拡張 (MIME) メッセージの参照のヘッダー フィールドの値が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_INTERNET_REFERENCES、PR_INTERNET_REFERENCES_A、PR_INTERNET_REFERENCES_W  <br/> |
|識別子:  <br/> |0x1039  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|領域:  <br/> |MIME  <br/> |
   
## <a name="remarks"></a>注釈

参照ヘッダー フィールドを生成するには、クライアントは、目的の値にこれらのプロパティを設定する必要があります。 MIME ライターは、参照のヘッダー フィールドにこれらのプロパティの値をコピーする必要があります。
  
これらのプロパティの値を設定するのには MIME クライアントは、参照のヘッダー フィールドに目的の値を記述する必要があります。 MIME のリーダーは、これらのプロパティへの参照のヘッダー フィールドの値をコピーする必要があります。 長さは 64 KB を超えている場合、MIME のリーダーはこれらのプロパティの値を切り捨てることがあります。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> メッセージ オブジェクト インターネット標準の電子メールの表記規則からに変換します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

