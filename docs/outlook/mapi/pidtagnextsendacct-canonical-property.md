---
title: PidTagNextSendAcct 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagNextSendAcct
api_type:
- HeaderDef
ms.assetid: b7429c2e-0d9d-4921-9f56-9ecad817f8cb
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 76584e248f03deac62af94e4638fcead15594b3e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581133"
---
# <a name="pidtagnextsendacct-canonical-property"></a>PidTagNextSendAcct 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
クライアントが電子メールの送信に使用する現在開こうとしているサーバーを指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_NEXT_SEND_ACCT  <br/> |
|識別子:  <br/> |0x0E29  <br/> |
|データの種類 :   <br/> |PT_UNICODE  <br/> |
|領域:  <br/> |Outlook アプリケーション  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティの形式は、実装に依存します。 このプロパティに電子メールを送信するサーバーを決定するのには、クライアントで使用できますが、オプションし、値は、サーバーに意味を持ちません。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> IETF RFC2445、RFC2446、RFC2447、および予定と会議のオブジェクトに変換します。
    
[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

