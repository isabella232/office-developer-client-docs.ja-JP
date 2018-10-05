---
title: PidTagNormalizedSubject 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagNormalizedSubject
api_type:
- HeaderDef
ms.assetid: 2000e6e8-d908-4814-8093-28f8011250c8
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 54a0f438dacc8a1c7838eb538ec05c5c263f1b0a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393230"
---
# <a name="pidtagnormalizedsubject-canonical-property"></a>PidTagNormalizedSubject 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
削除任意のプレフィックスを持つメッセージの件名が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_NORMALIZED_SUBJECT、PR_NORMALIZED_SUBJECT_A、PR_NORMALIZED_SUBJECT_W  <br/> |
|識別子:  <br/> |0x0E1D  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |メール  <br/> |
   
## <a name="remarks"></a>備考

これらのプロパティは、メッセージ ・ ストアでは、計算またはトランスポート プロバイダーが**あるの PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) と**されて**([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) のプロパティからの次のようにします。
  
- **されて**と**あるの PR_SUBJECT**の最初の部分文字列では、 **PR_NORMALIZED_SUBJECT**と関連するプロパティが**あるの PR_SUBJECT**の内容にプリフィックスを削除した設定です。 
    
- **されて**が削除され、次の規則を使用して**あるの PR_SUBJECT**から再計算**されて**がある場合は、**あるの PR_SUBJECT**の最初の部分文字列ではありません: 文字列が**あるの PR_SUBJECT**に含まれている場合コロンとスペースの後に数字以外の文字を 1 ~ 3 から始まるとコロン、空白文字列のプレフィックスになります。 数値、空白、および句読点の文字は、文字の有効なプレフィックスではありません。 
    
- **されて**がない場合は、前の手順に記載されているルールを使用して**あるの PR_SUBJECT**から計算されます。 このし、プロパティが**あるの PR_SUBJECT**の内容を削除するプレフィックスを持つ。 
    
 **メモ****されて**空の文字列がある場合、**あるの PR_SUBJECT**このプロパティは、同じです。 
  
最終的には、このプロパティには、**あるの PR_SUBJECT**の接頭辞の後の部分があります。 プレフィックスがない場合、このプロパティが**あるの PR_SUBJECT**と同じになります。
  
 **されて**このプロパティは、 [IMAPIProp::SaveChanges](imapiprop-savechanges.md)の実装の一部として計算する必要があります。 コミットされた後になるまで、クライアント アプリケーションで値を[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドのメッセージを表示しない**IMAPIProp::SaveChanges**の呼び出しによって、です。 
  
256 文字は、通常は短い文字列は、件名のプロパティと、メッセージ ストア プロバイダーがそれらのオブジェクトのリンクと埋め込み (OLE) の**IStream**インターフェイスをサポートする義務を負いません。 クライアントは、 **IMAPIProp**インターフェイスを介してアクセスを最初に試行し、MAPI_E_NOT_ENOUGH_MEMORY が返された場合にのみ、 **IStream**に頼る必要があります常に。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルのオブジェクトを処理します。
    
[[MS OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> プロパティは、連絡先、個人用配布リストの許可の操作を指定します。
    
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

