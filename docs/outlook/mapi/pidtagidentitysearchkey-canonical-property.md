---
title: PidTagIdentitySearchKey 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagIdentitySearchKey
api_type:
- HeaderDef
ms.assetid: 5fe55ba7-4ecd-4a43-ab5b-2ef595c2cdd9
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7f57192e5233e27b43e89f92fc2f3ed2d5a48349
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59555336"
---
# <a name="pidtagidentitysearchkey-canonical-property"></a>PidTagIdentitySearchKey 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージング システム内で定義されているサービス プロバイダーの ID の検索キーを格納します。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_IDENTITY_SEARCH_KEY  <br/> |
|識別子:  <br/> |0x3E05  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |MAPI の状態  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、任意のオブジェクトのプロパティとして表示されるのではなく、状態テーブルの列としてのみ表示されます。 これは、状態テーブル行を公開するサービス プロバイダーの ID の一部です。 プロバイダーの ID は通常、サーバー上のアカウントを参照しますが、プロバイダーがメッセージング システム内で定義する任意の表現を参照できます。 
  
ID プロパティを提供するサービス プロバイダーは、すべての ID プロパティを提供する必要があります。 同じメッセージ サービスに属するプロバイダーは、ID プロパティに同じ値を公開する必要があります。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[IMAPISession::QueryIdentity](imapisession-queryidentity.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

