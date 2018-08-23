---
title: PidTagMappingSignature 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMappingSignature
api_type:
- HeaderDef
ms.assetid: a5e9f807-12a9-4bc9-a6a5-17579e747ffa
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 6017871b9567406af0898eede0d5659b468b3343
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581035"
---
# <a name="pidtagmappingsignature-canonical-property"></a>PidTagMappingSignature 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
特定の MAPI オブジェクトの名前付きプロパティのマッピングの署名が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_MAPPING_SIGNATURE  <br/> |
|識別子:  <br/> |0x0FF8  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|領域:  <br/> |その他  <br/> |
   
## <a name="remarks"></a>注釈

名前付きプロパティを持つオブジェクトがこのプロパティを公開することをお勧めします。 という名前の別の 1 つのオブジェクトからプロパティをコピーするとき、クライアント アプリケーションは両方のオブジェクトの**PR_MAPPING_SIGNATURE**プロパティを確認する必要があります。 このプロパティの使用方法は、コピーされたプロパティの名前と id の間の変換を最小限にできます。 
  
特定の MAPI オブジェクトのこのプロパティが存在しない場合、オブジェクトは、固有のマッピングが、独自の名前と識別子があります。 ここで、クライアントは、ソース オブジェクトとし、目的のオブジェクトの[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)メソッドで[IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md)メソッドを呼び出す必要があります。 
  
2 つのオブジェクトは、同じ**PR_MAPPING_SIGNATURE**値を持つ、クライアントでは、識別子を名前に識別子の名前を変換する必要はありません。 クライアントがメソッドを呼び出して[IMAPIProp::GetProps](imapiprop-getprops.md)ソースとし、 [IMAPIProp::SetProps](imapiprop-setprops.md)メソッドで先にします。 これは、名前付きプロパティは、ユーザー設定のコピーを実行するクライアント、およびプロバイダーは、 [IMAPIProp::CopyTo](imapiprop-copyto.md)メソッドと[IMAPIProp::CopyProps](imapiprop-copyprops.md)メソッドを実装するには便利です。 
  
名前付きプロパティとの名前と識別子のマッピングの詳細については、 [MAPI 名前付きプロパティ](mapi-named-properties.md)を参照してください。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> プロパティとユーザー、連絡先、グループ、およびリソースのリストの操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPINAMEID](mapinameid.md)


[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

