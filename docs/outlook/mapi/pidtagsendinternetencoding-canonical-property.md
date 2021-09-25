---
title: PidTagSendInternetEncoding 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagSendInternetEncoding
api_type:
- COM
ms.assetid: ae408b4f-dee3-484b-a19c-f472cfa95996
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 92bfef3b339649b18b755cfa231954ebec84d4fe
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586972"
---
# <a name="pidtagsendinternetencoding-canonical-property"></a>PidTagSendInternetEncoding 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
エンコードの基本設定のビットマスクが含まれる。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SEND_INTERNET_ENCODING  <br/> |
|識別子:  <br/> |0x3A71  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |Address  <br/> |
   
## <a name="remarks"></a>注釈

使用するエンコード オプションを示すために、このプロパティを設定します。 
  
このプロパティには、次のフラグが含まれます。
  
BODY_ENCODING_HTML 
  
> HTML でメッセージ テキストをエンコードします。 このフラグは、フラグが設定されていないENCODING_MIME無視されます。 
    
BODY_ENCODING_TEXT_AND_HTML 
  
> テキストと HTML を使用してメッセージ テキストを多目的インターネット メール拡張機能 (MIME) マルチパート代替としてエンコードします。 このフラグは、フラグが設定されていないENCODING_MIME無視されます。 
    
ENCODING_MIME 
  
> MIME を使用してメッセージをエンコードします。 このフラグを設定しない場合、MAPI はメッセージ テキストをプレーン テキストでエンコードし、添付ファイルは UUENCODE でエンコードします。 
    
ENCODING_PREFERENCE 
  
> エンコードを決定するには、このビットマスクの他のフラグを使用します。 このフラグが設定されていない場合、MAPI はメッセージング システムに送信してエンコードの決定を行います。 
    
MAC_ATTACH_ENCODING_APPLEDOUBLE 
  
> Apple ダブル モードで Macintosh 添付ファイルをエンコードします。 このフラグは、フラグが設定されていないENCODING_MIME無視されます。 
    
MAC_ATTACH_ENCODING_APPLESINGLE 
  
> Apple シングル モードで Macintosh 添付ファイルをエンコードします。 このフラグは、フラグが設定されていないENCODING_MIME無視されます。 
    
MAC_ATTACH_ENCODING_UUENCODE 
  
> UUENCODE で Macintosh 添付ファイルをエンコードします。 このフラグENCODING_MIME設定すると、このフラグは無視され、代わりに BinHex エンコードが使用されます。 
    
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> ユーザー、連絡先、グループ、およびリソースの一覧のプロパティと操作を指定します。
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> インターネット標準の電子メール規則からメッセージ オブジェクトに変換します。
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージ オブジェクトと添付ファイル オブジェクトを処理します。
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> 電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

