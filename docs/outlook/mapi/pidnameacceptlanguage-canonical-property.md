---
title: PidNameAcceptLanguage 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameAcceptLanguage
api_type:
- COM
ms.assetid: 4b202bc1-f718-446a-950f-634ffee47baf
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d2c2fb31b722e76034b08077632c817d6adde802
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802301"
---
# <a name="pidnameacceptlanguage-canonical-property"></a>PidNameAcceptLanguage 標準プロパティ

  
  
**適用対象**: Outlook 
  
[RFC3282] Accept-language ヘッダー フィールドの値が含まれています。
  
|||
|:-----|:-----|
|フレンドリ名:  <br/> |AcceptLanguage  <br/> |
|プロパティを設定します。  <br/> |PS_INTERNET_HEADERS  <br/> |
|プロパティ名:  <br/> |Accept-Language  <br/> |
|データの種類 :   <br/> |PT_UNICODE  <br/> |
|領域:  <br/> |メール  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティの値を設定するには、多目的のインターネット メッセージの拡張機能 (MIME) クライアントが目的の値を持つ、Accept-language ヘッダー フィールドを記述しておきます。 MIME クライアントでは、X-ブラウザーの言語のヘッダー フィールドを代わりに書き込むことがあります。 MIME のリーダーは、このプロパティの値をいずれかのヘッダー フィールドの値をコピーする必要があります。 両方のヘッダー フィールドが存在する場合は、MIME のリーダーは、Accept-language ヘッダー フィールドを使用してください。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> メッセージ オブジェクト インターネット標準の電子メールの表記規則からに変換します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

