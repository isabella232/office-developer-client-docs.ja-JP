---
title: PidLidFileUnderId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFileUnderId
api_type:
- COM
ms.assetid: 917431a9-fd90-4b4d-b042-886e3dbf47c0
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7af30866a5fd2846327223b7a58c6de91f5fef7a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355707"
---
# <a name="pidlidfileunderid-canonical-property"></a>PidLidFileUnderId 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
他の連絡先の名前のプロパティが変更されたときに、([PidLidFileUnder](pidlidfileunder-canonical-property.md)) プロパティの**dispidfileunder**値を生成して再計算する方法を指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidfile過小 id  <br/> |
|プロパティセット:  <br/> |PSETID_Address  <br/> |
|ロング ID (LID):  <br/> |0x00008006  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |連絡先  <br/> |
   
## <a name="remarks"></a>解説

このプロパティが指定されていない場合、または次の表に記載されていない値または[[OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)に設定されている場合は、アプリケーションは独自のロジックを選択して、[その他の連絡先名のプロパティが変更されたときに、 **dispidfileunder**値を再計算できます。 
  
次の表では、表記<PropertyName>を使用して "PropertyName の値" を指定しています。 たとえば、 **PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md)) プロパティの値が "Smith" で、 **PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md)) プロパティの値が "ben" の場合は、"ben Smith" と<PidTagGivenName> <PidTagSurname>いう文字列を指定します。 表で、"\r" はキャリッジリターン文字を指定します。 "\n" は改行文字を指定し<space> 、スペース文字を表します。
  
|****dispidfile過小 id**プロパティの値**|**プロパティの**下の dispidfileunder**説明**|
|:-----|:-----|
|0x00000000  <br/> |空の PT_UNICODE。  <br/> |
|0x00003001  <br/> |"\<PidTagDisplayName\>"  <br/> |
|0x00003A06  <br/> |"\<PidTagGivenName\>"  <br/> |
|0x00003a11  <br/> |"\<PidTagSurname\>"  <br/> |
|0x00003a16  <br/> |"\<PidTagCompanyName\>"  <br/> |
|0x00008017  <br/> |"\<PidTagSurname\>,\<space\>\<PidTagGivenName\>\<space\>"\<\>  <br/> |
|0x00008018  <br/> |"\<PidTagCompanyName\>\r\n\<PidTagSurname\>、\<space\>\<PidTagGivenName\>\<space\>"\<\>  <br/> |
|0x00008019  <br/> |"\<PidTagSurname\>,\<space\>\<PidTagGivenName\>\>space PidTagMiddleName\>\r\n\<PidTagCompanyName\>"\<\<  <br/> |
|0x00008030  <br/> |"\<PidTagSurname\>\<\>PidTagGivenName\<space\>PidTagMiddleName\>"\<  <br/> |
|0x00008031  <br/> |"\<PidTagSurname\>\<space\>\<PidTagGivenName space\>PidTagMiddleName\>"\<\>\<  <br/> |
|0x00008032  <br/> |"\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<PidTagGivenName\>\<space\>"\<\>  <br/> |
|0x00008033  <br/> |"\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<space\>\<PidTagGivenName space\>PidTagMiddleName\>"\<\>\<  <br/> |
|0x00008034  <br/> |"\<PidTagSurname\>\<PidTagGivenName\>\>space PidTagMiddleName\>\r\n\<PidTagCompanyName\>"\<\<  <br/> |
|0x00008035  <br/> |"\<PidTagSurname\>\<space\>\<\>PidTagGivenName space\>PidTagMiddleName \r\n PidTagCompanyName"\<\>\<\>\<  <br/> |
|0x00008036  <br/> |"\<PidTagSurname\>\<space\>\>\>PidTagGivenName\>space PidTagMiddleName\>space\>PidTagGeneration\<"\<\<\<\<  <br/> |
|0x00008037  <br/> |"\<PidTagGivenName\>\<space\>\>\>PidTagMiddleName\>space PidTagSurname\>space\>PidTagGeneration\<"\<\<\<\<  <br/> |
|0x00008038  <br/> |"\<PidTagSurname\>\<PidTagGivenName\>\>space\>PidTagMiddleName\>space\>PidTagGeneration"\<\<\<\<  <br/> |
|0xfffffffd  <br/> |連絡先を表示するときに、アプリケーションは、その連絡先のプロパティの現在の値**** を使用して、この表の前の値の1つに対して、 **dispidfileunder id**の "最適な一致" を検索する必要があることを指定します。  <br/> |
|0xfffffffe  <br/> |連絡先を表示するときに、アプリで、選択した項目に一致するように、 **dispidfile過小 id**および update **dispidfileの**適切な既定値 (言語ロケールに応じて) を選択する必要があることを指定します。  <br/> |
|0xffffffff  <br/> |の**dispidfileunder**ユーザーが指定した PT_UNICODE で、別の連絡先の名前のプロパティが変更されたときには変更できません。  <br/> |
   
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

