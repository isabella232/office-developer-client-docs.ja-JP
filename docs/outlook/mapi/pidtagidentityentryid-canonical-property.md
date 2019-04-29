---
title: PidTagIdentityEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIdentityEntryId
api_type:
- HeaderDef
ms.assetid: 61a9d403-e0e5-45c3-8d18-4d53207ab927
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 099df2211e87e253ab1be520378b3a2b2ca7d4c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423336"
---
# <a name="pidtagidentityentryid-canonical-property"></a>PidTagIdentityEntryId 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージングシステム内での定義に従って、サービスプロバイダーの id のエントリ識別子を格納します。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_IDENTITY_ENTRYID  <br/> |
|識別子:  <br/> |0x3e01  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |MAPI の状態  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、オブジェクトのプロパティとして表示されませんが、ステータステーブルの列としてのみ表示されます。 これは、サービスプロバイダーの id の一部であり、状態テーブルの行を公開します。 通常、プロバイダーの id は、サーバー上でそのアカウントを参照しますが、メッセージングシステム内でプロバイダーが定義する任意の表現を参照できます。 
  
この proprerty は、通常、適切なアドレス帳エントリ識別子に設定されます。 
  
すべての id プロパティを提供するサービスプロバイダー。 同じメッセージサービスに属するプロバイダーは、identity プロパティに同じ値を公開する必要があります。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 代替名としてリストされているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[IMAPISession::QueryIdentity](imapisession-queryidentity.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

