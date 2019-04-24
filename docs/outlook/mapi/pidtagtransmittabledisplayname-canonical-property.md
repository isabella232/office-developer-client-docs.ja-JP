---
title: PidTagTransmittableDisplayName 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTransmittableDisplayName
api_type:
- COM
ms.assetid: aadd9086-b936-4067-bf7d-f54fc50e3c83
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e66fe8d3621c122ccc19bdde169f20f7d47a148d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331858"
---
# <a name="pidtagtransmittabledisplayname-canonical-property"></a>PidTagTransmittableDisplayName 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
セキュリティで保護された形式の受信者の表示名が含まれており、変更することはできません。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_TRANSMITABLE_DISPLAY_NAME、PR_TRANSMITABLE_DISPLAY_NAME_A、PR_TRANSMITABLE_DISPLAY_NAME_W  <br/> |
|識別子:  <br/> |0x3a20  <br/> |
|データの種類 :   <br/> |PT_UNICODE、PT_STRING8  <br/> |
|エリア:  <br/> |Address  <br/> |
   
## <a name="remarks"></a>解説

これらのプロパティは、すべてのアドレス帳プロバイダーで実装する必要があります。 これには、メッセージと共に送信される受信者の表示名のバージョンが含まれています。 ほとんどのアドレス帳プロバイダーでは、これらのプロパティは**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティと同じ値になります。 セキュリティで保護された表示名のないプロバイダーは、PT_ERROR と MAPI の名前を引用符で囲んで、表示名を変更します。
  
クライアントアプリケーションは、このプロパティを使用して、エントリの改ざんまたは "スプーフィング" を防止できます。 スプーフィングの例として、john doe を john (男の人) doe として送信することが挙げられます。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> ユーザー、連絡先、グループ、およびリソースのリストのプロパティと操作を指定します。
    
[[MS-CHAP]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)
  
> ネームサービスプロバイダインターフェイス (NSPI) サーバーとのクライアントの通信を処理します。
    
[[OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> クライアントとサーバー間のデータ転送の順序と流れを処理します。
    
[[OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルオブジェクトを処理します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 関連するプロパティとしてリストされているプロパティの定義が含まれます。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

