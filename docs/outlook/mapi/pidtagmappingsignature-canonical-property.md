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
ms.openlocfilehash: d12e8510686f51698981c47327f79ef40d3ec342
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342548"
---
# <a name="pidtagmappingsignature-canonical-property"></a>PidTagMappingSignature 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
特定の MAPI オブジェクトの名前付きプロパティのマッピングシグネチャが含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_MAPPING_SIGNATURE  <br/> |
|識別子:  <br/> |0x0ff8  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |その他  <br/> |
   
## <a name="remarks"></a>解説

名前付きプロパティを持つオブジェクトは、このプロパティを公開することをお勧めします。 クライアントアプリケーションは、あるオブジェクトから別のオブジェクトに名前付きプロパティをコピーするときに、両方のオブジェクトの**PR_MAPPING_SIGNATURE**プロパティをチェックする必要があります。 このプロパティを使用すると、コピーされたプロパティの名前と識別子の間の変換を最小限に抑えることができます。 
  
指定した MAPI オブジェクトに対してこのプロパティが存在しない場合、オブジェクトには名前と識別子の固有のマッピングがあります。 この場合、クライアントは、ソースオブジェクトに対して[imapiprop:: GetNamesFromIDs](imapiprop-getnamesfromids.md)メソッドを呼び出してから、宛先オブジェクトの[imapiprop:: getidsfromnames](imapiprop-getidsfromnames.md)メソッドを呼び出す必要があります。 
  
2つのオブジェクトの**PR_MAPPING_SIGNATURE**値が同じである場合、クライアントは名前を識別子と識別子に変換する必要はありません。 クライアントは単に、ソースで[imapiprop:: GetProps](imapiprop-getprops.md)メソッドを呼び出すことができます。その後、宛先の[imapiprop:: setprops](imapiprop-setprops.md)メソッドを呼び出すことができます。 これは、名前付きプロパティのカスタムコピーを実行するクライアント、および[imapiprop:: CopyTo](imapiprop-copyto.md)および[imapiprop:: copyprops](imapiprop-copyprops.md)メソッドを実装しているプロバイダーにとって便利です。 
  
名前付きプロパティと名前と識別子のマッピングの詳細については、「 [MAPI の名前付きプロパティ](mapi-named-properties.md)」を参照してください。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> ユーザー、連絡先、グループ、およびリソースのリストのプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 代替名としてリストされているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPINAMEID](mapinameid.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

