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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348441"
---
# <a name="pidlidaddressbookproviderarraytype-canonical-property"></a>PidLidAddressBookProviderArrayType 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
連絡先の電子メールアドレスの状態を指定し、ビットフラグのセットを表します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidABPArrayType  <br/> |
|プロパティセット:  <br/> |PSETID_Address  <br/> |
|ロング ID (LID):  <br/> |0x00008029  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |連絡先  <br/> |
   
## <a name="remarks"></a>解説

**dispidABPArrayType**プロパティの値は、連絡先オブジェクトの状態を指定するフラグの組み合わせである必要があります。 各フラグは、次の表で指定されています。 このプロパティが設定されている場合は、 **dispidabpemaillist** ([PidLidAddressBookProviderEmailList](pidlidaddressbookprovideremaillist-canonical-property.md)) プロパティも設定する必要があります。 これら2つのプロパティは、互いに同期しておく必要があります。 たとえば、 **dispidABPArrayType**にビット "0x00000001 set" が含まれている場合、 **dispidabpemaillist**の値の1つは "0x00000000" である必要があります。 
  
|**若干**|**説明**|
|:-----|:-----|
|0x00000001  <br/> |Email1 が連絡先に対して定義されている。  <br/> |
|0x00000002  <br/> |Email2 が連絡先に対して定義されている。  <br/> |
|0x00000004  <br/> |Email3 が連絡先に対して定義されている。  <br/> |
|0x00000008  <br/> |連絡先に対して会社の fax が定義されている。  <br/> |
|0x00000010  <br/> |自宅 fax は連絡先に対して定義されています。  <br/> |
|0x00000020  <br/> |連絡先に対して、プライマリ fax が定義されている。  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> 連絡先および個人用配布リストに対して許容されるプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

