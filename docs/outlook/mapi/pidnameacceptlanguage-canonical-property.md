---
title: PidNameAcceptLanguage 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidNameAcceptLanguage
api_type:
- COM
ms.assetid: 4b202bc1-f718-446a-950f-634ffee47baf
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3e1f03e7834a4a67ce7ea61b2e4eaac6ea02a597
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579321"
---
# <a name="pidnameacceptlanguage-canonical-property"></a>PidNameAcceptLanguage 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[RFC3282] ヘッダー フィールドAccept-Language含まれています。
  
|||
|:-----|:-----|
|分名:  <br/> |AcceptLanguage  <br/> |
|プロパティ セット:  <br/> |PS_INTERNET_HEADERS  <br/> |
|プロパティ名:  <br/> |Accept-Language  <br/> |
|データの種類 :   <br/> |PT_UNICODE  <br/> |
|エリア:  <br/> |メール  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティの値を設定するには、Multipurpose Internet Message Extensions (MIME) クライアントは、目的の値を持つ Accept-Language ヘッダー フィールドを記述する必要があります。 MIME クライアントは、代わりに X-Accept-Language ヘッダー フィールドを書き込む場合があります。 MIME リーダーは、いずれかのヘッダー フィールドの値をこのプロパティの値にコピーする必要があります。 両方のヘッダー フィールドが存在する場合、MIME リーダーはヘッダー フィールドのAccept-Language使用する必要があります。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> インターネット標準の電子メール規則からメッセージ オブジェクトに変換します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

