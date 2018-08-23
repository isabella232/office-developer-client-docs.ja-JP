---
title: PidTagSendInternetEncoding 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSendInternetEncoding
api_type:
- COM
ms.assetid: ae408b4f-dee3-484b-a19c-f472cfa95996
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b6814df2b28961be7e8c07a2d19932988605dc87
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803515"
---
# <a name="pidtagsendinternetencoding-canonical-property"></a>PidTagSendInternetEncoding 標準プロパティ

  
  
**適用対象**: Outlook 
  
環境設定のエンコーディングのビットマスクを格納します。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SEND_INTERNET_ENCODING  <br/> |
|識別子:  <br/> |0x3A71  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|領域:  <br/> |Address  <br/> |
   
## <a name="remarks"></a>注釈

使用するエンコード オプションを指定するには、このプロパティを設定します。 
  
このプロパティには、次のフラグが含まれています。
  
BODY_ENCODING_HTML 
  
> Html 形式でメッセージのテキストをエンコードします。 ENCODING_MIME フラグが設定されていない場合、このフラグは無視されます。 
    
BODY_ENCODING_TEXT_AND_HTML 
  
> 多目的インターネット メール拡張 (MIME) の複数の代替手段として、テキストと HTML を使用してメッセージのテキストをエンコードします。 ENCODING_MIME フラグが設定されていない場合、このフラグは無視されます。 
    
ENCODING_MIME 
  
> MIME を使用してメッセージをエンコードします。 このフラグが設定されていない場合、MAPI は、テキスト形式でメッセージのテキストと、UUENCODE の添付ファイルをエンコードします。 
    
ENCODING_PREFERENCE 
  
> このビットマスクで他のフラグを使用して、エンコーディングを判断します。 このフラグが設定されていない場合は、MAPI はエンコードを決定するメッセージング システムに残ります。 
    
MAC_ATTACH_ENCODING_APPLEDOUBLE 
  
> Apple の二重モードで、Macintosh の添付ファイルをエンコードします。 ENCODING_MIME フラグが設定されていない場合、このフラグは無視されます。 
    
MAC_ATTACH_ENCODING_APPLESINGLE 
  
> Apple の 1 つのモードで、Macintosh の添付ファイルをエンコードします。 ENCODING_MIME フラグが設定されていない場合、このフラグは無視されます。 
    
MAC_ATTACH_ENCODING_UUENCODE 
  
> Macintosh 添付ファイルを UUENCODE でエンコードします。 ENCODING_MIME フラグが設定されている場合は、このフラグは無視され、BinHex エンコーディングが代わりに使用します。 
    
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> プロパティとユーザー、連絡先、グループ、およびリソースのリストの操作を指定します。
    
[[MS OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> メッセージ オブジェクト インターネット標準の電子メールの表記規則からに変換します。
    
[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルのオブジェクトを処理します。
    
[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
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

