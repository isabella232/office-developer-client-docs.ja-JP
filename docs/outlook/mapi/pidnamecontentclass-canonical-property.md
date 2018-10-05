---
title: PidNameContentClass 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameContentClass
api_type:
- COM
ms.assetid: 6f623345-b30e-452f-a822-9308b455697a
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 51788a49d1c0d01ef7ff5daca853000a8f1e34a0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384543"
---
# <a name="pidnamecontentclass-canonical-property"></a>PidNameContentClass 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[RFC3282] のコンテンツ クラスのヘッダー フィールドの値が含まれています。
  
|||
|:-----|:-----|
|フレンドリ名:  <br/> |なし  <br/> |
|プロパティを設定します。  <br/> |PS_INTERNET_HEADERS  <br/> |
|プロパティ名:  <br/> |コンテンツ クラス  <br/> |
|データの種類 :   <br/> |PT_UNICODE  <br/> |
|エリア:  <br/> |メール  <br/> |
   
## <a name="remarks"></a>備考

多目的インターネット メッセージの拡張機能 (MIME) クライアントはこのプロパティの値を設定するのには、目的の値を持つコンテンツ クラスのヘッダー フィールドを記述しなければなりません。 MIME のリーダーは、このプロパティの値をコンテンツ クラスのヘッダー フィールドの値をコピーする必要があります。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> メッセージ オブジェクト インターネット標準の電子メールの表記規則からに変換します。
    
[[MS OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)
  
> 権限管理でエンコードされたメッセージのプロパティを指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

