---
title: PidLidAddressBookProviderArrayType 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAddressBookProviderArrayType
api_type:
- COM
ms.assetid: ca4eb6c2-98e9-4dbc-9f5a-f0f257456ead
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 68396f210aab465da9cec4a74a3c24cc4e8578a5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393090"
---
# <a name="pidlidaddressbookproviderarraytype-canonical-property"></a>PidLidAddressBookProviderArrayType 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
連絡先の電子メール アドレスの状態を指定して、ビット フラグのセットを表します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidABPArrayType  <br/> |
|プロパティを設定します。  <br/> |PSETID_Address  <br/> |
|長い ID (LID):  <br/> |0x00008029  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |Contact  <br/> |
   
## <a name="remarks"></a>備考

**DispidABPArrayType**プロパティの値は、連絡先オブジェクトの状態を指定するフラグの組み合わせである必要があります。 個々 のフラグは、次の表で指定されます。 このプロパティが設定されている場合、 **dispidABPEmailList** ([PidLidAddressBookProviderEmailList](pidlidaddressbookprovideremaillist-canonical-property.md)) する必要がありますプロパティ、同様です。 互いに同期された 2 つのプロパティを保持する必要があります。 などの場合は**dispidABPArrayType**では、ビットが"0x00000001"が設定されて、 **dispidABPEmailList**の値のいずれかの必要があります"0x00000000"です。 
  
|**ビット**|**説明**|
|:-----|:-----|
|0x00000001  <br/> |連絡先の Email1 が定義されています。  <br/> |
|0x00000002  <br/> |連絡先の電子メール 2 が定義されています。  <br/> |
|0x00000004  <br/> |連絡先の電子メール 3 が定義されています。  <br/> |
|0x00000008  <br/> |連絡先の勤務先ファックスが定義されています。  <br/> |
|0x00000010  <br/> |連絡先の自宅の fax が定義されています。  <br/> |
|0x00000020  <br/> |連絡先のプライマリ fax が定義されています。  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> プロパティは、連絡先、個人用配布リストの許可の操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

