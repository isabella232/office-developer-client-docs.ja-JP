---
title: PidTagDefCreateDl の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 3fb86fba3b0ff8a79858fad59dca61069aff6db9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802674"
---
# <a name="pidtagdefcreatedl-canonical-property"></a>PidTagDefCreateDl の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
既定の配布リストのテンプレートのエントリ id が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_DEF_CREATE_DL  <br/> |
|識別子:  <br/> |0x3611  <br/> |
|データを入力します。  <br/> |PT_BINARY  <br/> |
|領域:  <br/> |アドレス帳  <br/> |
   
## <a name="remarks"></a>備考

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
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

