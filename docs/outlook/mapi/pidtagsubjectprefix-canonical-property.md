---
title: PidTagSubjectPrefix 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSubjectPrefix
api_type:
- COM
ms.assetid: 07fcb881-d873-45bf-b048-30f41d0d8d85
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: be2d30f511540b2eb7aa6e55531753811aaa580d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803616"
---
# <a name="pidtagsubjectprefix-canonical-property"></a>PidTagSubjectPrefix 標準プロパティ

  
  
**適用対象**: Outlook 
  
通常次のように、メッセージのいくつかのアクションを示す件名のプレフィックスが含まれています"FW:"転送します。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |されて、PR_SUBJECT_PREFIX_A、PR_SUBJECT_PREFIX_W  <br/> |
|識別子:  <br/> |0x003D  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|領域:  <br/> |メッセージ全般  <br/> |
   
## <a name="remarks"></a>注釈

これらのプロパティは、すべてのメッセージ オブジェクトに対して推奨されています。 
  
件名のプレフィックスは、1 つまたは複数文字の英数字、続いてコロンとスペース (これは、プレフィックスの一部である) で構成されています。 コロンの前に任意の英数字以外の文字が含まれていない必要があります。 プレフィックスがない場合は、このプロパティが設定されていない、空の文字列で表現できます。 
  
これらのプロパティは、明示的に設定されている場合は文字列は任意の長さにして、任意の英数字を使用が、**あるの PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) プロパティの先頭の部分文字列に一致しなければなりません。 これらのプロパティでは、送信者が設定されていないと、計算する必要がある場合、その内容より制限されています。 接頭辞を計算するためのルールは、**あるの PR_SUBJECT**が 1、2、または 3 文字で始まる必要があります (アルファベットのみ)、コロンとスペースの後にします。 このような部分が**あるの PR_SUBJECT**の先頭にある場合、これらのプロパティの文字列になります (および**あるの PR_SUBJECT**の先頭のままでも)。 それ以外の場合、これらのプロパティは設定されていないままです。 
  
これらのプロパティと**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) は、 [IMAPIProp::SaveChanges](imapiprop-savechanges.md)の実装の一部として計算する必要があります。 クライアントは、いない、コミットされた後になるまでの値の[IMAPIProp::GetProps](imapiprop-getprops.md)を促す必要がある**IMAPIProp::SaveChanges**の呼び出しによって、です。 
  
256 文字は、通常は短い文字列は、件名のプロパティと、メッセージ ストア プロバイダーがこれらの OLE **IStream**インターフェイスをサポートするために義務を負いません。 クライアントは、 **IMAPIProp**インターフェイスを介してアクセスを最初に試行し、 **MAPI_E_NOT_ENOUGH_MEMORY**が返された場合にのみ、 **IStream**に頼る必要があります常に。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルのオブジェクトを処理します。
    
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

