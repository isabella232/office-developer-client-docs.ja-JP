---
title: PidTag7BitDisplayName 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTag7BitDisplayName
api_type:
- HeaderDef
ms.assetid: 803d7c4e-ed80-4d5b-988f-27068a8ccd63
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e5177d47749c2f60a883bd12fbba27045114c601
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315814"
---
# <a name="pidtag7bitdisplayname-canonical-property"></a>PidTag7BitDisplayName 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージングユーザー名の7ビットの ASCII 表記を含みます。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_7BIT_DISPLAY_NAME、PR_7BIT_DISPLAY_NAME_A、PR_7BIT_DISPLAY_NAME_W  <br/> |
|識別子:  <br/> |0x39ff  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |アドレス帳  <br/> |
   
## <a name="remarks"></a>解説

これらのプロパティは、 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティを7ビット文字セットにマッピングします。 インターネットや特定の x-blade リンクなど、一部のメッセージングシステムは、128文字の7ビット ASCII コードセットに制限されています。 このようなメッセージングシステムへのゲートウェイは、 [IAddrBook::P reparerecips](iaddrbook-preparerecips.md)メソッドを直接呼び出してこのプロパティを取得することによって、パフォーマンスを向上させることができます。これにより、コード変換のためのその他の処理を回避できます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> ユーザー、連絡先、グループ、およびリソースのリストに対するプロパティと操作を指定します。
    
[[MS-CHAP]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)
  
> クライアントの NSPI サーバーとの通信を処理します。
    
[[OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> クライアントとサーバーの間でデータを転送するために使用される順序とデータフローを処理します。
    
[[OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルオブジェクトを処理します。
    
[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> 電子メールメッセージに対して許容されるプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダーファイル

Mapitags
  
> 関連するプロパティとしてリストされているプロパティの定義が含まれます。
    
mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

