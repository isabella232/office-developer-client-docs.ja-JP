---
title: PidTagSubjectPrefix 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagSubjectPrefix
api_type:
- COM
ms.assetid: 07fcb881-d873-45bf-b048-30f41d0d8d85
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 2c2bece089bc985111695f5bb54098d3fc6c4f0f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624455"
---
# <a name="pidtagsubjectprefix-canonical-property"></a>PidTagSubjectPrefix 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
通常、メッセージに対する何らかのアクション (転送用の "FW:" など) を示す件名プレフィックスが含まれる。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SUBJECT_PREFIX、PR_SUBJECT_PREFIX_A、PR_SUBJECT_PREFIX_W  <br/> |
|識別子:  <br/> |0x003D  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |一般的なメッセージング  <br/> |
   
## <a name="remarks"></a>注釈

これらのプロパティは、すべてのメッセージ オブジェクトで推奨されます。 
  
件名のプレフィックスは、1 つ以上の英数字で構成され、その後にコロンとスペース (プレフィックスの一部) が続きます。 コロンの前に英数字以外の文字を含めることはできません。 プレフィックスがない場合は、空の文字列で表したり、このプロパティを設定したりすることはできません。 
  
これらのプロパティが明示的に設定されている場合、文字列は任意の長さであり、任意の英数字を使用できますが **、PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) プロパティの先頭にある部分文字列と一致する必要があります。 これらのプロパティが送信者によって設定されていないので、計算する必要がある場合、それらのプロパティの内容はさらに制限されます。 プレフィックスを計算するルールは、PR_SUBJECT 1 文字、2 **文字、または** 3 文字 (アルファベットのみ) の後にコロンとスペースが続く必要がある点です。 このような部分文字列が PR_SUBJECT の先頭に見つかった場合は、これらのプロパティの文字列になります (また、これらのプロパティの先頭に **PR_SUBJECT)。** それ以外の場合、これらのプロパティは未設定のままです。 
  
これらのプロパティと **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) は [、IMAPIProp::SaveChanges](imapiprop-savechanges.md) 実装の一部として計算する必要があります。 クライアントは [、IMAPIProp::SaveChanges](imapiprop-getprops.md) 呼び出しによってコミットされるまで **、IMAPIProp::GetProps** の値を求める必要があります。 
  
件名のプロパティは、通常、256 文字未満の小さな文字列であり、メッセージ ストア プロバイダーは、OLE **IStream** インターフェイスをサポートする義務はありません。 クライアントは常に最初に **IMAPIProp** インターフェイスを介してアクセスを試み **、IStream** にアクセス **MAPI_E_NOT_ENOUGH_MEMORY** 必要があります。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージ オブジェクトと添付ファイル オブジェクトを処理します。
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> 電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

