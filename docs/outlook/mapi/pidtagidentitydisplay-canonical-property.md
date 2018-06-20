---
title: PidTagIdentityDisplay の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: b88fc54f1db26277d8a8d5e54fcff0ae164b0eac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802846"
---
# <a name="pidtagidentitydisplay-canonical-property"></a>PidTagIdentityDisplay の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
メッセージング システム内で定義されているように、サービス プロバイダーの id の表示名が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_IDENTITY_DISPLAY、PR_IDENTITY_DISPLAY_A、PR_IDENTITY_DISPLAY_W  <br/> |
|識別子:  <br/> |0x3E00  <br/> |
|データを入力します。  <br/> |PT_STRING8、PT_UNICODE  <br/> |
|領域:  <br/> |MAPI のステータス  <br/> |
   
## <a name="remarks"></a>備考

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
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

