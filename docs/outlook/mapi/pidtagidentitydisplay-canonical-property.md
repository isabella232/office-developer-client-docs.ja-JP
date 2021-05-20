---
title: PidTagIdentityDisplay 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIdentityDisplay
api_type:
- HeaderDef
ms.assetid: ad9756c1-c1f9-4ab3-a58a-31e574dd9530
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d6e189f78dec2fc92f1804be93e7885b61734b03
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431422"
---
# <a name="pidtagidentitydisplay-canonical-property"></a>PidTagIdentityDisplay 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージング システム内で定義されているサービス プロバイダーの ID の表示名を格納します。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_IDENTITY_DISPLAY、PR_IDENTITY_DISPLAY_A、PR_IDENTITY_DISPLAY_W  <br/> |
|識別子:  <br/> |0x3E00  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |MAPI の状態  <br/> |
   
## <a name="remarks"></a>注釈

これらのプロパティは、任意のオブジェクトのプロパティとして表示されるのではなく、状態テーブルの列としてのみ表示されます。 これは、状態テーブル行を公開するサービス プロバイダーの ID の一部です。 プロバイダーの ID は通常、サーバー上のアカウントを参照しますが、プロバイダーがメッセージング システム内で定義する任意の表現を参照できます。 
  
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

