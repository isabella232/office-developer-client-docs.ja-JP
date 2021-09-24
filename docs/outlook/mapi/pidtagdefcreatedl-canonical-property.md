---
title: PidTagDefCreateDl 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagDefCreateDl
api_type:
- HeaderDef
ms.assetid: 172dc15b-7bda-403f-a93a-446b2f9ff1d3
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 16b9af522adfba01e76a97aeb228c4414b48b79c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59550730"
---
# <a name="pidtagdefcreatedl-canonical-property"></a>PidTagDefCreateDl 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
既定の配布リストのテンプレート エントリ識別子が含まれる。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_DEF_CREATE_DL  <br/> |
|識別子:  <br/> |0x3611  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |アドレス帳  <br/> |
   
## <a name="remarks"></a>注釈

クライアント アプリケーションは、このプロパティを使用してコンテナー内に配布リストを作成します。 エントリの作成のサポートは、アドレス帳コンテナーではオプションです。このプロパティをサポートしていないユーザーは、このプロパティを公開する必要はありません。 
  
このプロパティは、配布リストの PR_CREATE_TEMPLATES **(** [PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) プロパティに表示されるエントリを指定します。 識別子を取得した後、クライアントは [IABContainer::CreateEntry](iabcontainer-createentry.md) メソッドの呼び出しで識別子を使用します。 このエントリは、既定の配布リストのテンプレートを表します。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[IABLogon::CompareEntryIDs](iablogon-compareentryids.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

