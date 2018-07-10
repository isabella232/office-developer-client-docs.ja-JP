---
title: PidLidFileUnderId の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 08e2403be35b87393d22f9109f59c0572c53073b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801990"
---
# <a name="pidlidfileunderid-canonical-property"></a>PidLidFileUnderId の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
生成し、その他の連絡先の名前のプロパティの変更時に**dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) プロパティの値を再計算する方法を指定します。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |dispidFileUnderId  <br/> |
|プロパティを設定します。  <br/> |PSETID_Address  <br/> |
|長い ID (LID):  <br/> |0x00008006  <br/> |
|データを入力します。  <br/> |PT_LONG  <br/> |
|領域:  <br/> |連絡先  <br/> |
   
## <a name="remarks"></a>備考

このプロパティがないか、または[[MS OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)で、次の表で詳細にない値に設定、アプリケーションはその他の連絡先の名前のプロパティの変更と**dispidFileUnder**の値を再計算するのには、独自のロジックを選択できます。 
  
次の表では、表記法に<PropertyName>」プロパティ名の値」を指定するために使用します。 たとえば、 **PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md)) プロパティの値は、チェック ボックスをオフ、および**PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md)) プロパティの値が「佐藤」、"<PidTagGivenName> <PidTagSurname>""Ben Smith"という文字列を指定します。 キャリッジ リターン文字を指定する「\r」の表で、"\n"は、ライン フィード文字を指定し、、<space>空白文字を表します。
  
|****DispidFileUnderId**プロパティの値**|****DispidFileUnder**プロパティの説明**|
|:-----|:-----|
|0x00000000  <br/> |空の PT_UNICODE。  <br/> |
|0x00003001  <br/> |"\<PidTagDisplayName\>」  <br/> |
|0x00003A06  <br/> |"\<PidTagGivenName\>」  <br/> |
|0x00003A11  <br/> |"\<PidTagSurname\>」  <br/> |
|0x00003A16  <br/> |"\<PidTagCompanyName\>」  <br/> |
|0x00008017  <br/> |"\<PidTagSurname\>、\<スペース\>\<PidTagGivenName\>\<スペース\>\<PidTagMiddleName\>」  <br/> |
|0x00008018  <br/> |"\<PidTagCompanyName\>\r\n\<PidTagSurname\>、\<スペース\>\<PidTagGivenName\>\<スペース\>\<PidTagMiddleName\>」  <br/> |
|0x00008019  <br/> |"\<PidTagSurname\>、\<スペース\>\<PidTagGivenName\>\<スペース\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>」  <br/> |
|0x00008030  <br/> |"\<PidTagSurname\>\<PidTagGivenName\>\<スペース\>\<PidTagMiddleName\>」  <br/> |
|0x00008031  <br/> |"\<PidTagSurname\>\<スペース\>\<PidTagGivenName\>\<スペース\>\<PidTagMiddleName\>」  <br/> |
|0x00008032  <br/> |"\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<PidTagGivenName\>\<スペース\>\<PidTagMiddleName\>」  <br/> |
|0x00008033  <br/> |"\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<スペース\>\<PidTagGivenName\>\<スペース\>\<PidTagMiddleName\>」  <br/> |
|0x00008034  <br/> |"\<PidTagSurname\>\<PidTagGivenName\>\<スペース\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>」  <br/> |
|0x00008035  <br/> |"\<PidTagSurname\>\<スペース\>\<PidTagGivenName\>\<スペース\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>」  <br/> |
|0x00008036  <br/> |"\<PidTagSurname\>\<スペース\>\<PidTagGivenName\>\<スペース\>\<PidTagMiddleName\>\<スペース\>\<PidTagGeneration\>」  <br/> |
|0x00008037  <br/> |"\<PidTagGivenName\>\<スペース\>\<PidTagMiddleName\>\<スペース\>\<PidTagSurname\>\<スペース\>\<PidTagGeneration\>」  <br/> |
|0x00008038  <br/> |"\<PidTagSurname\>\<PidTagGivenName\>\<スペース\>\<PidTagMiddleName\>\<スペース\>\<PidTagGeneration\>」  <br/> |
|0xfffffffd  <br/> |、連絡先を表示するには、ときに、アプリケーション必要がありますしようとする**dispidFileUnder**およびその他の連絡先のプロパティの現在の値を使用して、次の表に示した値のいずれかに**dispidFileUnderId**の最適な"を検索するかを指定します。  <br/> |
|0xfffffffe  <br/> |指定、連絡先を表示するには、ときにアプリケーションする必要があります (言語のロケール) に基づく適切な既定値を選択して、 **dispidFileUnderId**の選択に一致するように**dispidFileUnder**を更新します。  <br/> |
|0 xffffffff  <br/> |**dispidFileUnder**は、ユーザーが指定した PT_UNICODE と、別の連絡先の名前のプロパティが変更されたときに変更されません。  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> プロパティは、連絡先、個人用配布リストの許可の操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)
