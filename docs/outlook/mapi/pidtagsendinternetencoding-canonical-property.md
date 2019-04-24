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
ms.openlocfilehash: e157fa640026d13362084b30ad73cdb66a0b35b5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342673"
---
# <a name="pidtagsendinternetencoding-canonical-property"></a>PidTagSendInternetEncoding 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
エンコード設定のビットマスクを含みます。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SEND_INTERNET_ENCODING  <br/> |
|識別子:  <br/> |0x3a71  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |Address  <br/> |
   
## <a name="remarks"></a>解説

このプロパティを設定して、使用するエンコードオプションを指定します。 
  
このプロパティには、次のフラグが含まれています。
  
BODY_ENCODING_HTML 
  
> メッセージテキストを HTML 形式でエンコードします。 ENCODING_MIME フラグが設定されていない場合、このフラグは無視されます。 
    
BODY_ENCODING_TEXT_AND_HTML 
  
> テキストと HTML を使用して、メッセージテキストをエンコードするマルチパーパスインターネットメール拡張機能 (MIME) マルチパートの代替手段として使用します。 ENCODING_MIME フラグが設定されていない場合、このフラグは無視されます。 
    
ENCODING_MIME 
  
> MIME を使用してメッセージをエンコードします。 このフラグが設定されていない場合、MAPI はテキスト形式のメッセージテキストと UUENCODE の添付ファイルをエンコードします。 
    
ENCODING_PREFERENCE 
  
> このビットマスクの他のフラグを使用して、エンコーディングを決定します。 このフラグが設定されていない場合、MAPI はメッセージングシステムにメッセージを発信して、エンコード決定を行います。 
    
MAC_ATTACH_ENCODING_APPLEDOUBLE 
  
> Macintosh の添付ファイルを Apple のダブルモードでエンコードします。 ENCODING_MIME フラグが設定されていない場合、このフラグは無視されます。 
    
MAC_ATTACH_ENCODING_APPLESINGLE 
  
> Macintosh の添付ファイルを Apple のシングルモードでエンコードします。 ENCODING_MIME フラグが設定されていない場合、このフラグは無視されます。 
    
MAC_ATTACH_ENCODING_UUENCODE 
  
> UUENCODE で Macintosh の添付ファイルをエンコードします。 ENCODING_MIME フラグが設定されている場合、このフラグは無視され、代わりに BinHex エンコードが使用されます。 
    
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> ユーザー、連絡先、グループ、およびリソースのリストのプロパティと操作を指定します。
    
[[OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> インターネット標準の電子メールの規則からメッセージオブジェクトに変換します。
    
[[OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルオブジェクトを処理します。
    
[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> 電子メールメッセージオブジェクトに対して許容されるプロパティと操作を指定します。
    
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

