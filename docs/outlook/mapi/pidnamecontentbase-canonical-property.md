---
title: PidNameContentBase 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameContentBase
api_type:
- COM
ms.assetid: ab197ace-6e7d-4ec5-9f6d-4a63a1eda11c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 501b54cfb7846a91aec7172cbe1d846c24704923
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331501"
---
# <a name="pidnamecontentbase-canonical-property"></a>PidNameContentBase 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[RFC3282] コンテンツベースのヘッダーフィールド値を含みます。
  
|||
|:-----|:-----|
|フレンドリ名:  <br/> |bodycontentbase  <br/> |
|プロパティセット:  <br/> |PS_INTERNET_HEADERS  <br/> |
|プロパティ名:  <br/> |コンテンツベース  <br/> |
|データの種類 :   <br/> |PT_UNICODE  <br/> |
|エリア:  <br/> |電子メール  <br/> |
   
## <a name="remarks"></a>解説

このプロパティの値を設定するには、mime (インターネットメッセージ拡張機能) クライアントは、メッセージ本文にマッピングされている mime エンティティのコンテンツベースのヘッダーフィールドに必要な値を書き込む必要があります。 mime リーダーは、この mime エンティティのコンテンツベースヘッダーフィールドの値をこのプロパティの値にコピーする必要があります。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> インターネット標準の電子メールの規則からメッセージオブジェクトに変換します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

