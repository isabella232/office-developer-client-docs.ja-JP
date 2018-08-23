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
ms.openlocfilehash: 48c068599506e5c050c69594caca46f28be83b0b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565803"
---
# <a name="pidtagdefcreatedl-canonical-property"></a>PidTagDefCreateDl 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
既定の配布リストのテンプレートのエントリ id が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_DEF_CREATE_DL  <br/> |
|識別子:  <br/> |0x3611  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|領域:  <br/> |アドレス帳  <br/> |
   
## <a name="remarks"></a>注釈

クライアント アプリケーションでは、このプロパティを使用して、コンテナー内の配布リストを作成します。 エントリの作成のサポートはオプションのアドレス帳コンテナーです。サポートしていないものは、このプロパティを公開する必要はありません。 
  
このプロパティでは、配布リストの**PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) のプロパティで表示可能なエントリを指定します。 Id を入手すると、クライアントは、それを[IABContainer::CreateEntry](iabcontainer-createentry.md)メソッドの呼び出しで使用します。 エントリは、既定の配布リスト用のテンプレートを表します。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 関連付けられているプロパティとして記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[IABLogon::CompareEntryIDs](iablogon-compareentryids.md)


[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

