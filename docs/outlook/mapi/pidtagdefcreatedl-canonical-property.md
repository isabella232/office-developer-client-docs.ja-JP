---
title: PidTagDefCreateDl 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefCreateDl
api_type:
- HeaderDef
ms.assetid: 172dc15b-7bda-403f-a93a-446b2f9ff1d3
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ff5d35104e9effc27c405b716cb61cf4643677b3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359956"
---
# <a name="pidtagdefcreatedl-canonical-property"></a>PidTagDefCreateDl 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
既定の配布リストのテンプレートエントリ識別子を含みます。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_DEF_CREATE_DL  <br/> |
|識別子:  <br/> |0x3611  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |アドレス帳  <br/> |
   
## <a name="remarks"></a>解説

クライアントアプリケーションは、このプロパティを使用して、コンテナー内に配布リストを作成します。 エントリ作成のサポートは、アドレス帳コンテナーでは省略可能です。これをサポートしていないものは、このプロパティを公開する必要はありません。 
  
このプロパティは、配布リストの**PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) プロパティに表示できるエントリを指定します。 識別子を取得した後、クライアントは[IABContainer:: createentry](iabcontainer-createentry.md)メソッドへの呼び出しでその識別子を使用します。 このエントリは、既定の配布リストのテンプレートを表します。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 関連するプロパティとしてリストされているプロパティの定義が含まれます。
    
## <a name="see-also"></a>関連項目



[IABLogon::CompareEntryIDs](iablogon-compareentryids.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

