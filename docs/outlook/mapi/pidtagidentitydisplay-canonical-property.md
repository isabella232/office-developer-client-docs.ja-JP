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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 6cfc4d6eab5b2f19bcfd4c7e2a8fc9fa1494afa4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585578"
---
# <a name="pidtagidentitydisplay-canonical-property"></a>PidTagIdentityDisplay 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
メッセージング システム内で定義されているように、サービス プロバイダーの id の表示名が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_IDENTITY_DISPLAY、PR_IDENTITY_DISPLAY_A、PR_IDENTITY_DISPLAY_W  <br/> |
|識別子:  <br/> |0x3E00  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|領域:  <br/> |MAPI のステータス  <br/> |
   
## <a name="remarks"></a>注釈

状態テーブル内の列としてのみですが、任意のオブジェクトのプロパティとして、これらのプロパティは表示されません。 状態テーブルの行を公開するサービス ・ プロバイダーの id の一部であります。 プロバイダーの識別情報は通常、サーバー上のアカウントを参照が、プロバイダーは、メッセージング システム内で定義された表現を参照できます。 
  
Id プロパティのいずれかを使用する際、サービス プロバイダーは、それらのすべてを提供する必要があります。 同じメッセージ サービスに属しているプロバイダーには、id プロパティに同じ値を公開する必要があります。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[IMAPISession::QueryIdentity](imapisession-queryidentity.md)


[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

