---
title: PidTagDefCreateMailuser 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagDefCreateMailuser
api_type:
- HeaderDef
ms.assetid: e8293dc9-f2f1-4065-89f4-e734a8db63df
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7734c759fe9b5954dd38ecb74e9423455348fff3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59550723"
---
# <a name="pidtagdefcreatemailuser-canonical-property"></a>PidTagDefCreateMailuser 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
既定のメッセージング ユーザー オブジェクトのテンプレート エントリ識別子を格納します。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_DEF_CREATE_MAILUSER  <br/> |
|識別子:  <br/> |0x3612  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |アドレス帳  <br/> |
   
## <a name="remarks"></a>注釈

クライアント アプリケーションは、このプロパティを使用して、コンテナー内にメッセージング ユーザー オブジェクトを作成します。 エントリの作成のサポートは、アドレス帳コンテナーではオプションです。このプロパティをサポートしていないユーザーは、このプロパティを公開する必要はありません。 
  
このプロパティは、メッセージング ユーザーの PR_CREATE_TEMPLATES **(** [PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) プロパティに表示されるエントリを指定します。 識別子を取得した後、クライアントは [IABContainer::CreateEntry](iabcontainer-createentry.md) メソッドの呼び出しで識別子を使用します。 このエントリは、既定のメッセージング ユーザーのテンプレートを表します。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

