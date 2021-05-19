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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d12e8510686f51698981c47327f79ef40d3ec342
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342548"
---
# <a name="pidtagmappingsignature-canonical-property"></a>PidTagMappingSignature 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
特定の MAPI オブジェクトの名前付きプロパティのマッピング署名を格納します。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_MAPPING_SIGNATURE  <br/> |
|識別子:  <br/> |0x0FF8  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |その他  <br/> |
   
## <a name="remarks"></a>注釈

名前付きプロパティを持つオブジェクトは、このプロパティを公開する必要があります。 クライアント アプリケーションは、1 つの **オブジェクトから別** PR_MAPPING_SIGNATUREに名前付きプロパティをコピーするときに、両方のオブジェクトのプロパティをチェックする必要があります。 このプロパティを使用すると、コピーされたプロパティの名前と識別子の変換を最小限に抑える可能性があります。 
  
特定の MAPI オブジェクトに対してこのプロパティが存在しない場合、オブジェクトには、名前と識別子の独自のマッピングがあります。 この場合、クライアントはソース オブジェクトの [IMAPIProp:::GetNamesFromIDs](imapiprop-getnamesfromids.md) メソッドを呼び出し、次に移行先オブジェクトの [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) メソッドを呼び出す必要があります。 
  
2 つのオブジェクトの値 **PR_MAPPING_SIGNATURE、クライアント** は名前を識別子と識別子に変換する必要があります。 クライアントは、ソースで [IMAPIProp:::GetProps](imapiprop-getprops.md) メソッドを呼び出し、次に宛先の [IMAPIProp::SetProps](imapiprop-setprops.md) メソッドを呼び出すだけでできます。 これは、名前付きプロパティのカスタム コピーを実行するクライアントや [、IMAPIProp::CopyTo](imapiprop-copyto.md) メソッドと [IMAPIProp::CopyProps](imapiprop-copyprops.md) メソッドを実装するプロバイダーに便利です。 
  
名前付きプロパティと名前と識別子のマッピングの詳細については、「MAPI 名前付きプロパティ [」を参照してください](mapi-named-properties.md)。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> ユーザー、連絡先、グループ、およびリソースの一覧のプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPINAMEID](mapinameid.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

