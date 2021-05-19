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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7af30866a5fd2846327223b7a58c6de91f5fef7a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355707"
---
# <a name="pidlidfileunderid-canonical-property"></a>PidLidFileUnderId 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
他の連絡先名のプロパティが変更された場合に **、dispidFileUnder** [(PidLidFileUnder)](pidlidfileunder-canonical-property.md)プロパティの値を生成および再計算する方法を指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidFileUnderId  <br/> |
|プロパティ セット:  <br/> |PSETID_Address  <br/> |
|長い ID (LID):  <br/> |0x00008006  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |Contact  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティが見つからないか、下の表または [[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)の詳細ではない値に設定されている場合、アプリケーションは、他の連絡先名プロパティの変更に応じ、独自のロジックを選択して **dispidFileUnder** の値を再計算できます。 
  
次の表では、表記を <PropertyName> 使用して "PropertyName の値" を指定します。 たとえば **、PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md)) プロパティの値が "Smith" で **、PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md)) プロパティの値が "Ben" の場合、" <PidTagGivenName> <PidTagSurname> " は "Ben Smith" という文字列を指定します。 表の "\r" は復帰文字を指定し、"\n" は改行文字を指定し、スペース文字 <space> を表します。
  
|****dispidFileUnderId** プロパティの値**|****dispidFileUnder プロパティの** 説明**|
|:-----|:-----|
|0x00000000  <br/> |空PT_UNICODE。  <br/> |
|0x00003001  <br/> |" \< PidTagDisplayName \> "  <br/> |
|0x00003A06  <br/> |" \< PidTagGivenName \> "  <br/> |
|0x00003A11  <br/> |" \< PidTagSurname \> "  <br/> |
|0x00003A16  <br/> |" \< PidTagCompanyName \> "  <br/> |
|0x00008017  <br/> |" \< PidTagSurname \> , space \< \> \< PidTagGivenName space \> \< \> \< PidTagMiddleName \> "  <br/> |
|0x00008018  <br/> |" \< PidTagCompanyName \>\r\n\< \> PidTagSurname 、 space \< \> \< PidTagGivenName \> \< スペース \> \< PidTagMiddleName \> "  <br/> |
|0x00008019  <br/> |" \< PidTagSurname \> 、 space \< \> \< PidTagGivenName スペース \> \< \> \< PidTagMiddleName\r\n\> \< PidTagCompanyName \> "  <br/> |
|0x00008030  <br/> |" \< PidTagSurname \> \< PidTagGivenName \> \< スペース \> \< PidTagMiddleName \> "  <br/> |
|0x00008031  <br/> |" \< PidTagSurname \> \< スペース \> \< PidTagGivenName \> \< スペース \> \< PidTagMiddleName \> "  <br/> |
|0x00008032  <br/> |" \< PidTagCompanyName \>\r\n\< PidTagSurname \> \< \> \< \> \< PidTagGivenName スペース PidTagMiddleName \> "  <br/> |
|0x00008033  <br/> |" \< PidTagCompanyName \>\r\n\< \> \< PidTagSurname スペース \> \< \> \< \> \< PidTagGivenName スペース PidTagMiddleName \> "  <br/> |
|0x00008034  <br/> |" \< PidTagSurname \> \< PidTagGivenName \> \< スペース \> \< PidTagMiddleName\r\n\> \< PidTagCompanyName \> "  <br/> |
|0x00008035  <br/> |" \< PidTagSurname \> \< スペース \> \< PidTagGivenName \> \< スペース \> \< PidTagMiddleName\r\n\> \< PidTagCompanyName \> "  <br/> |
|0x00008036  <br/> |" \< PidTagSurname \> \< スペース \> \< PidTagGivenName \> \< スペース \> \< PidTagMiddleName スペース \> \< \> \< PidTagGeneration \> "  <br/> |
|0x00008037  <br/> |" \< PidTagGivenName \> \< スペース \> \< PidTagMiddleName \> \< スペース \> \< PidTagSurname スペース \> \< \> \< PidTagGeneration \> "  <br/> |
|0x00008038  <br/> |" \< PidTagSurname \> \< PidTagGivenName \> \< スペース \> \< PidTagMiddleName \> \< スペース \> \< PidTagGeneration \> "  <br/> |
|0xfffffffd  <br/> |連絡先を表示するときに、アプリケーションが **dispidFileUnder** および他の連絡先プロパティの現在の値を使用して **、dispidFileUnderId** をこの表の前の値の 1 つに対して "最適な一致" を見つける必要があります。  <br/> |
|0xfffffffe  <br/> |連絡先を表示するときに、アプリケーションが **dispidFileUnderId** の適切な既定値 (言語ロケールに従って) を選択し、選択に一致する **dispidFileUnder** を更新する必要があります。  <br/> |
|0xffffffff  <br/> |**dispidFileUnder** はユーザー提供のPT_UNICODEであり、別の連絡先名プロパティが変更された場合は変更できません。  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> 連絡先と個人用配布リストで許容されるプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

