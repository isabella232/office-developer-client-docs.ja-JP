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
ms.openlocfilehash: 8257c3c3583072d16e96e6ea9bba4632fc78f9ef
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339229"
---
# <a name="pidtagsubjectprefix-canonical-property"></a>PidTagSubjectPrefix 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
通常、メッセージに何らかのアクション (転送の場合は "FW:" など) を示す件名のプレフィックスが含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SUBJECT_PREFIX、PR_SUBJECT_PREFIX_A、PR_SUBJECT_PREFIX_W  <br/> |
|識別子:  <br/> |0x003d  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |一般的なメッセージング  <br/> |
   
## <a name="remarks"></a>解説

これらのプロパティは、すべてのメッセージオブジェクトで推奨されます。 
  
件名のプレフィックスは、1つ以上の英数字で構成され、その後にコロンとスペース (プレフィックスの一部) が続きます。 コロンの前に英数字以外の文字を含めることはできません。 プレフィックスを指定しない場合は、空の文字列、またはこのプロパティが設定されていないことがあります。 
  
これらのプロパティが明示的に設定されている場合、文字列の長さは任意で、任意の英数字を使用できますが、 **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) プロパティの先頭にある部分文字列に一致する必要があります。 これらのプロパティが送信者によって設定されておらず、計算する必要がある場合、そのコンテンツはより制限されます。 プレフィックスを計算する規則は、 **PR_SUBJECT**が1、2、または3文字 (アルファベットのみ) で始まり、その後にコロンとスペースが続く必要があるということです。 このようなサブ文字列が**PR_SUBJECT**の先頭にある場合は、これらのプロパティの文字列になります (また、 **PR_SUBJECT**の先頭にも留まりません)。 それ以外の場合、これらのプロパティは未設定のままです。 
  
これらのプロパティと**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) は、 [imapiprop:: SaveChanges](imapiprop-savechanges.md)実装の一部として計算する必要があります。 クライアントは、imapiprop: **: SaveChanges**呼び出しでコミットされるまで、値に対して[imapiprop:: GetProps](imapiprop-getprops.md)にプロンプトを表示しません。 
  
件名のプロパティは通常、256文字未満の小さな文字列で、メッセージストアプロバイダーは、それらの OLE **IStream**インターフェイスをサポートする義務がありません。 クライアントは、常に**imapiprop**インターフェイスを使用してアクセスを試行し、 **MAPI_E_NOT_ENOUGH_MEMORY**が返された場合にのみ**IStream**に頼る必要があります。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルオブジェクトを処理します。
    
[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> 電子メールメッセージオブジェクトで許容されるプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 代替名としてリストされているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

