---
title: PidTagPrimarySendAccount 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagPrimarySendAccount
api_type:
- COM
ms.assetid: 2f268b3b-2e4c-4aea-8879-bdd0ac1df35c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 2c32cc61fea63cd38215c30e04e8a467d4901cc9
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387315"
---
# <a name="pidtagprimarysendaccount-canonical-property"></a>PidTagPrimarySendAccount 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージを送信するために使用される最初のサーバーの名前を示す文字列が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_PRIMARY_SEND_ACCOUNT  <br/> |
|識別子:  <br/> |0x0E28  <br/> |
|データの種類 :   <br/> |PT_UNICODE  <br/> |
|エリア:  <br/> |Account  <br/> |
   
## <a name="remarks"></a>備考

メールを送信するクライアントを使用する必要があります最初のサーバーを指定します。 これらのプロパティの形式は、実装に依存します。 これらのプロパティを通じて、メールを送信するサーバーを決定するのには、クライアントで使用できますが、オプションと値は、サーバーに意味を持ちません。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 関連付けられているプロパティとして記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

