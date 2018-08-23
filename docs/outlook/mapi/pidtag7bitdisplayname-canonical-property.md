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
ms.openlocfilehash: 15ff5ded3c26a4283572a0f64f4e41452c7699f0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566839"
---
# <a name="pidtag7bitdisplayname-canonical-property"></a>PidTag7BitDisplayName 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
メッセージング ユーザーの名前の 7 ビット ASCII 表現が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_7BIT_DISPLAY_NAME、PR_7BIT_DISPLAY_NAME_A、PR_7BIT_DISPLAY_NAME_W  <br/> |
|識別子:  <br/> |0x39FF  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|領域:  <br/> |アドレス帳  <br/> |
   
## <a name="remarks"></a>注釈

これらのプロパティは、7 ビットの文字セットに**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) のプロパティをマップします。 インターネットや特定の X.400 リンクなど、いくつかのメッセージング システムでは、7 ビット ASCII の 128 文字コード セットに制限されます。 このようなメッセージング システムへのゲートウェイは、これを取得するには、直接の[IAddrBook::PrepareRecips](iaddrbook-preparerecips.md)メソッドを呼び出すことによって、パフォーマンスを向上することができますプロパティは、コード変換のための余分な処理を回避します。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> プロパティとユーザー、連絡先、グループ、およびリソースのリストに対する操作を指定します。
    
[[MS NSPI]](http://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)
  
> NSPI サーバーとクライアントの通信を処理します。
    
[[MS OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> クライアントとサーバー間でデータを転送するために使用される順序とデータのフローを処理します。
    
[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルのオブジェクトを処理します。
    
[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> プロパティは、電子メール メッセージの許可の操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapitags.h
  
> 関連付けられているプロパティとして記載されているプロパティの定義が含まれています。
    
Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

