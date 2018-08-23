---
title: PidTagDefCreateMailuser 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefCreateMailuser
api_type:
- HeaderDef
ms.assetid: e8293dc9-f2f1-4065-89f4-e734a8db63df
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 21fdff2aa713905a27a3d0cc5545ceb59f030378
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586859"
---
# <a name="pidtagdefcreatemailuser-canonical-property"></a>PidTagDefCreateMailuser 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
ユーザー オブジェクトのメッセージングの既定のテンプレートのエントリ id が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_DEF_CREATE_MAILUSER  <br/> |
|識別子:  <br/> |0x3612  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|領域:  <br/> |アドレス帳  <br/> |
   
## <a name="remarks"></a>注釈

クライアント アプリケーションでは、このプロパティを使用して、コンテナー内のメッセージングのユーザー オブジェクトを作成します。 エントリの作成のサポートはオプションのアドレス帳コンテナーです。サポートしていないものは、このプロパティを公開する必要はありません。 
  
このプロパティでは、メッセージング ユーザーの**PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) のプロパティで表示可能なエントリを指定します。 Id を入手すると、クライアントは、それを[IABContainer::CreateEntry](iabcontainer-createentry.md)メソッドの呼び出しで使用します。 エントリは、既定のメッセージング ユーザーのテンプレートを表します。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 関連付けられているプロパティとして記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

