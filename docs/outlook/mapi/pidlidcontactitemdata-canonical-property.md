---
title: PidLidContactItemData の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidContactItemData
api_type:
- COM
ms.assetid: 411e8f81-c2b9-440a-9e9a-d6add5e4be63
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 510920af290fa1cfe13fc1a85ba72f902532c539
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801859"
---
# <a name="pidlidcontactitemdata-canonical-property"></a>PidLidContactItemData の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
連絡先情報を表示する場合に使用されます。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |dispidContactItemData  <br/> |
|プロパティを設定します。  <br/> |PSETID_Address  <br/> |
|長い ID (LID):  <br/> |0x00008007  <br/> |
|データを入力します。  <br/> |PT_MV_LONG  <br/> |
|領域:  <br/> |連絡先  <br/> |
   
## <a name="remarks"></a>備考

存在する場合、プロパティには、各アプリケーションのユーザー インターフェイスに表示されるフィールドに対応する 6 つのエントリが必要です。
  
|**複数値プロパティに 1 から始まるインデックス**|**値は、次のいずれかである必要があります。**|**説明**|
|:-----|:-----|:-----|
|1  <br/> |0x00000001  <br/> |アプリケーションは、連絡先の自宅の住所を表示する必要があります。  <br/> |
|1  <br/> |0x00000002、0x00000000 または  <br/> |アプリケーションでは、取引先担当者の作業時間を表示する必要があります。  <br/> |
|1  <br/> |0x00000003  <br/> |アプリケーションを表示する必要があります、連絡先の他のアドレスです。  <br/> |
|2  <br/> |0x00008080  <br/> |アプリケーションでは、Email1 を表示する必要があります。  <br/> |
|2  <br/> |0x00008090  <br/> |アプリケーションは、電子メール 2 を表示する必要があります。  <br/> |
|2  <br/> |0x000080A0  <br/> |アプリケーションは、電子メール 3 を表示する必要があります。  <br/> |
|3,4,5,6  <br/> |電話のプロパティのいずれかまたは[[MS OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)で指定されている fax 番号のいずれかの PropertyID。  <br/> |アプリケーションでは、対応するプロパティを表示する必要があります。  <br/> |
   
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
